---
title: Marketing Campaign Analytics Deep Dive
description: Explore a metodologia técnica por trás do Adobe Marketing Campaign Analytics, incluindo atribuição multitoque, modelagem de mix de marketing, aprendizado de transferência e otimização de orçamento.
feature: Administration
hide: true
TQID: 'https://experienceleague.adobe.com/vIeES6bmdXOt6GIEA5Mt--IbyJ5g64kf-gyb6oEK0Ro'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a234aebd-3855-4376-a64d-29b38411e0c5
    internal-label: Marketing mix modeling
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
    internal-label: Datasets
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
    internal-label: Models
  - id: fe1c9ae8-a908-4ae1-a0b6-fcf35177b134
    internal-label: Marketing touch attribution
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
    internal-label: Administration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
    internal-label: Experimentation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '2853'
ht-degree: 0%
---

# Mergulho profundo


O Adobe Marketing Campaign Analytics é uma plataforma unificada de medição alimentada por IA/ML que combina MTA (atribuição multitoque) e MMM (modelagem de mix de marketing) para fornecer insights de marketing precisos, escaláveis e que não se tornem obsoletos. Este artigo apresenta um detalhamento da metodologia, das opções de design e das inovações técnicas por trás do Marketing Campaign Analytics. E é baseado na [sessão deste Summit 2025](https://business.adobe.com/br/summit/2025/sessions/marketing-mix-modeling-at-adobe-learn-to-predict-s602.html){target="_blank"}, que apresenta um detalhamento da metodologia, opções de design e inovações técnicas por trás da Marketing Campaign Analytics.

À medida que a complexidade de marketing cresce, as abordagens tradicionais de medição ficam aquém. Dados fragmentados, a evolução das restrições de privacidade e a necessidade de velocidade e rigor tornam necessário repensar a avaliação do desempenho de marketing. A resposta da Adobe é o Marketing Campaign Analytics: um sistema integrado que usa aprendizagem de máquina para sintetizar várias fontes de dados e modelar paradigmas em uma estratégia coesa.


>[!TIP]
>
>Um dos principais benefícios do Marketing Campaign Analytics é a acessibilidade da solução para os profissionais de marketing. O aplicativo simplifica as complexidades da ciência de dados por meio de uma interface fácil de usar que não requer conhecimento de fundo da ciência de dados. Se você estiver interessado em um aprofundamento, este artigo explora as opções técnicas feitas ao desenvolver o Marketing Campaign Analytics. O artigo presume alguma familiaridade com conceitos (avançados) de ciência de dados.

Este artigo explica os componentes fundamentais com mais detalhes. Esses componentes fundamentais são:

* [atribuição multitoque](#multi-touch-attribution-mta)
* [modelagem de mix de marketing](#marketing-mix-modeling-mmm)
* [transferir aprendizado](#transfer-learning) (a troca inteligente de resultados entre a atribuição multitoque e a modelagem de mix de marketing)



## Atribuição multitoque (MTA)


### Visão geral

O modelo de atribuição multitoque (MTA) que capacita o Marketing Campaign Analytics baseia-se em um modelo de sobrevivência em tempo discreto treinado em dados no nível do evento. Os dados incluem pesquisas, cliques, visualizações de produto, adição a carrinhos e check-outs. Usando o aprendizado supervisionado, o modelo estima a probabilidade condicional de conversão em cada etapa da jornada do cliente. O modelo considera os caminhos de jornada do cliente de conversão e não conversão para medir como pontos de contato de marketing diferentes influenciam o comportamento do cliente ao longo do tempo. O caminho de não conversão é tão importante quanto o caminho de conversão. O contraste entre os dois caminhos ajuda a entender se um tipo específico de ponto de contato de marketing impulsiona a conversão de maneira eficaz. Por exemplo, se um tipo de ponto de contato aparecer com a mesma probabilidade em um caminho que não seja de conversão, esse ponto de contato não terá impacto na conversão. Esse comportamento é contrário a um ponto de contato que aparece com frequência em um caminho de conversão e não em um caminho que não seja de conversão.

![Dados de nível de evento](/help/assets/event-level-data.png)

### Principais conceitos

Os principais conceitos por trás da atribuição multitoque são:

* **Modelagem de interesse**: a conversão do cliente é modelada como uma acumulação de interesse ao longo do tempo.

  ![Juros sobre o aumento da exposição](/help/assets/exposure-increases-interest.jpg)

  Nesta abordagem, uma série de sinais de interesse impulsionam a probabilidade de conversão, cada um influenciado por

  * exposições anteriores aos meios,
  * impacto do adstock mediático (um modelo de como as respostas à criação de publicidade e às deteriorações nos mercados de consumo), e
  * outros fatores de base.



  Esses sinais são representados como *ϴ<sub>BL</sub>* + *ϴ<sub>E,tc-t1</sub>* + *ϴ<sub>E,tc-t2</sub>* e *ϴ<sub>S, tc-t3</sub>*, onde:

  * *ϴ*: ilustra os parâmetros do modelo (o que é aprendido com o modelo).
  * *tc*: a hora da conversão.
  * *tc-tx: tempo decorrido entre a exposição e a conversão, que é relevante para o modelo.
  * *BL*: linha de base.
  * *E*: email.
  * *S*: pesquisar.

  Na estrutura de modelagem, o objetivo é contabilizar explicitamente o tempo entre cada exposição de mídia e o momento da conversão (*tc-tx*), reconhecendo que as interações mais recentes pesam mais do que as mais antigas.

* **Mapeamento de probabilidade**: a probabilidade de conversão é derivada do nível de interesse usando uma função logística em forma de S.

  ![Probabilidade de conversão](/help/assets/probability-of-conversion.jpg)

  Por meio do aprendizado de máquina supervisionado que usa um modelo de sobrevivência em tempo discreto, a ilustração acima visualiza a jornada do cliente A para conversão. O nível de juros é exibido no eixo X e a probabilidade de conversão no eixo Y. Este mapeamento mostra que a segunda exposição de email (*ϴE, tc-t2*) tem o maior impacto na conversão. Conforme indicado por um salto significativo na probabilidade de conversão no momento dessa etapa.

* **Diminuição dos retornos**: pontos de contato adicionais têm menos impacto incremental à medida que o interesse cresce.

  A curva em forma de S, da ilustração acima, também mostra que expor o cliente a pontos de contato adicionais tem menos impacto incremental com níveis de interesse crescentes.

* **Modelo de sobrevivência em tempo discreto**: o uso de um modelo de sobrevivência em tempo discreto introduz mais flexibilidade no modelo, o que permite que ele capture nuances temporais no comportamento do cliente. O modelo de sobrevida em tempo discreto também relaxa algumas das suposições mais restritivas exigidas pelos modelos de sobrevida em tempo contínuo.

  ![Modelo de sobrevivência de tempo discreto](/help/assets/discrete-time-survival-model.jpg)

  Uma função de tempo contínuo modela o impacto do adstock de email no nível de interesse, em qualquer momento desde o momento da exposição: *ϴ<sub>E</sub>(Δt;⋋)*
  Uma função de tempo discreto modela o impacto do adstock de email no nível de interesse como janelas de tempo discretas usando parâmetros escalares: *ϴ<sub>E,i</sub> ≥ 0<sub>E,i+1</sub>*


### Benefícios

A abordagem de atribuição multitoque selecionada para o Marketing Campaign Analytics tem várias vantagens principais.

* Contabilize os caminhos de conversão e não conversão, garantindo assim uma estimativa mais precisa do impacto real da mídia.
* Incorpore o adstock e retornos decrescentes que modelam o comportamento real do cliente e evite suposições simplificadas que são frequentemente encontradas em modelos baseados em regras.
* Dimensione com eficiência para grandes conjuntos de dados devido à otimização para computação distribuída e processamento paralelo.
* Suporte atribuição intuitiva de ponto de contato que permite uma interpretação clara contrária a outros métodos, como Modelos ocultos de Markov.
* Oferece alto desempenho e alta precisão preditiva quando comparado a outros algoritmos de classificação.

A Marketing Campaign Analytics fornece uma [interface amigável do profissional de marketing](/help/models/insights.md#attribution) para os insights resultantes da atribuição multitoque.

![Insights de atribuição de modelo](/help/assets/model-insights-attribution.png)


Embora a atribuição multitoque forneça todos esses benefícios, a Marketing Campaign Analytics não depende totalmente dos insights de conversão dos dados no nível do evento. A modelagem de mix de marketing é outro componente fundamental para levar em consideração os dados agregados.

## Modelagem de mix de marketing (MMM)

A modelagem de mix de marketing (MMM) é baseada em dados de nível agregado e usa uma estrutura de modelo multiplicativa, em vez de aditiva, para refletir as interações de marketing reais.

![Dados de nível agregado](/help/assets/mmm-aggregate-data.jpg)

A ilustração mostra dados de nível agregado em formato tabular. Cada linha corresponde a um período (geralmente uma semana, às vezes um dia) e cada coluna representa uma variável. A tabela inclui:

* a coluna de conversão (a variável de resultado do modelo),
* colunas de mídia (por exemplo: pesquisar, exibir) e
* colunas de fatores (por exemplo, sazonalidade, promoções) para capturar influências internas ou externas fora do gasto de mídia que ainda afetam o desempenho da mídia.

O modelo prevê conversões da semana 4 usando os dados destacados em verde claro, incluindo os fatores dessa semana e entradas históricas de canais de mídia.

### Principais conceitos

Os principais conceitos por trás da modelagem de mix de marketing são:

* **Modelo multiplicativo**: vendas ou conversões são o produto de uma linha de base e multiplicadores de mídia.

  Então, em vez de usar um modelo aditivo:
  *Conversões semanais = Demanda da linha de base **+**&#x200B;Multiplicador da Pesquisa **+**&#x200B;Multiplicador da Exibição **+**....*
usar um modelo multiplicativo:
  *Conversões semanais = Demanda da linha de base **x**&#x200B;Multiplicador da Pesquisa **x**&#x200B;Multiplicador da Exibição **x**....*

  Ou em uma fórmula: ** Y = ⨍<sub>BL</sub>(X<sub>fatores</sub>;θ<sub>fatores</sub>) x ⨍<sub>S</sub>(X<sub>S</sub>;θ<sub>S</sub>) x ⨍<sub>D</sub>(X<sub>D</sub>;θ<sub>D</sub>)*

  Por exemplo:

  * Conversões reais da semana: 1730.
  * Conversões previstas para a semana: 1787,5 = 1100 x 1,25 x 1,3, onde:
    * 1100: demanda de linha de base prevista para a semana 4, uma função para os dados dos fatores 1 e 2 da semana 4.
    * 1,25: multiplicador de pesquisa previsto para a semana 4, uma função dos dados de pesquisa da semana 1 até a semana 4.
    * 1.3: multiplicador de exibição previsto para a semana 4, uma função para exibir dados da semana 1 até a semana 4.

  A diferença antecipada entre o que o modelo prevê (1787.5) e as conversões reais (1730) é o residual, que geralmente é pequeno em tamanho e não é algo para se preocupar.


* **Capturar adstock e diminuir o retorno**: Adstock é capturado usando decaimento exponencial e funções de potência.

  ![Capturando retornos de diminuição de estoque de anúncios](/help/assets/capturing-adstock-diminishing-return.jpg)


  O declínio exponencial de um estoque pode ser de cauda única ou de cauda dupla, dependendo de onde o impacto de pico ocorre após o investimento em mídia.

  Para cuidar de retornos decrescentes, a função de potência é aplicada: *x<sup>θ</sup>* para *θ ∈ (0,1*). Esta função de potência resulta em um gráfico côncavo para capturar a diminuição do retorno. O retorno decrescente é então capturado na função multiplicadora dentro do modelo MMM.


### Benefícios

Os benefícios da abordagem de modelagem de mix de marketing são baseados no fato de que o modelo multiplicativo suporta melhor os comportamentos de marketing esperados no mundo real. Por exemplo:

* Sinergia de mídia, em que os canais de mídia geralmente funcionam melhor em conjunto do que isoladamente.
* Impacto variável no tempo em que o mesmo nível de investimento em marketing pode gerar diferentes retornos em momentos diferentes devido a fatores externos.
* Recomendações de orçamento ao longo do tempo em que as condições de mercado ou as flutuações da linha de base esperadas ajudam a informar a alocação de orçamento ao longo do tempo.

O Marketing Campaign Analytics fornece uma [interface amigável do profissional de marketing](/help/models/insights.md#attribution) para os vários insights resultantes da modelagem de mix de marketing. Por exemplo, um detalhamento de contribuição do fator para mostrar a proporção das conversões base que podem ser atribuídas a vários fatores incluídos no modelo.


![Detalhamento da contribuição do fator](/help/assets/factors-example.png)


#### Exemplo

Este exemplo simplificado ilustra como uma abordagem de modelagem multiplicativa para uma loja online fictícia de tênis permite uma melhor alocação de orçamento do que o modelo aditivo.

![Abordagem de modelo multiplicativa](/help/assets/benefits-mmm.jpg)

##### Suposições

* A procura de absorventes é mais elevada no verão e mais baixa no inverno, como ilustrado pelo Total das contribuições de base.

* A estratégia padrão para o planejamento de marketing é gastar uma quantidade fixa de orçamento de marketing (US$ 840) durante todo o ano, onde cada mês recebe o mesmo orçamento.

* O Adstock é ignorado e a mídia paga é tratada como uma unidade. Esses pressupostos são independentes do modelo escolhido e não influenciam a comparação.

* Um orçamento constante no modelo aditivo significa uma contribuição constante em cada mês, que é refletida para o modelo aditivo no gráfico superior na coluna intermediária.

* No modelo multiplicativo, um orçamento constante significa multiplicadores constantes a cada mês. Para fornecer um impacto variável no tempo para o mesmo gasto mensal, o multiplicador trabalha com a demanda de linha de base. Esse efeito multiplicador é mostrado no gráfico inferior na coluna do meio.

##### Mover orçamentos

Existe alguma capacidade de se afastar de um orçamento fixo, mudando o orçamento, mas mantendo o orçamento total para US$ 840?

* No modelo aditivo, não há incentivo de uma perspectiva de modelagem para fazer uma alteração, pois não há interação com a linha de base. Ter um gasto fixo é ótimo. Se você mover $1 de novembro para maio, o ganho em maio é menor do que a queda em novembro devido à diminuição dos retornos.
* Num modelo multiplicativo, há espaço para se deslocar. Com base na linha base, você pode deslocar orçamentos dos meses de inverno para os meses de verão. O ganho no mês de verão é maior do que a perda no mês de inverno devido ao efeito multiplicador. A extensão do turno e para onde mudar é coberta pelos [algoritmos de otimização de orçamento](#budget-optimization) usados na modelagem de mix de marketing.



## Transferir aprendizado

Ao lado da atribuição multitoque e da modelagem de mix de marketing, a experimentação é outro pilar importante para resolver problemas de medição de marketing. Embora a experimentação não seja implementada na estrutura do Marketing Campaign Analytics, você pode usar a experimentação, como desativar o marketing em determinados mercados, para entender o impacto causal do marketing nas vendas.

A Adobe recomenda e emprega o aprendizado de transferência para combinar insights de atribuição de multitoque, modelagem de mix de marketing, experimentação e outras fontes de conhecimento anteriores.  Essa combinação pode ser descrita como uma abordagem em camadas. Cada camada tem lacunas para ilustrar as limitações na produção de um modelo coeso. Mas se empilhar as camadas da maneira correta, pode-se compensar as lacunas no modelo combinado.
Aplique essa analogia ao usar a combinação de atribuição multitoque, modelagem de mix de marketing, experimentação e fontes de conhecimento anteriores. Misture esses componentes de forma que a combinação sofra o mínimo de falhas em cada um dos componentes.

Em essência, o aprendizado de transferência é um algoritmo de otimização numérica em funcionamento. Como parte do treinamento do modelo, uma função de perda (para quantificar a diferença entre a saída prevista de um modelo e o valor real (verdade fundamental)) é configurada. E uma boa métrica de ajuste (para avaliar como as previsões de um modelo se alinham com os dados observados) é determinada. A transferência do aprendizado resolve a otimização numérica para obter thetas (parâmetros de modelo). Se houver uma ou mais fontes de informação, essa função do objetivo de otimização original será aumentada com outro termo. Esse termo mede a distância entre o que você forneceu como conhecimento prévio e o que o modelo produz para comparação.


### Aprendizado de transferência bidirecional

Quando você tem dados de nível de evento e dados de nível agregado, o aprendizado de transferência bidirecional envolve o seguinte fluxo de trabalho.

![Aprendizado de transferência bidirecional](/help/assets/bi-directional-transfer-learning.jpg)

| Etapa | Descrição |
|:---:|---|
| 1a | O modelo de MTA padrão é treinado em dados. Normalmente, um modelo de MTA é treinado em uma janela de tempo mais curta do que o modelo MMM. Os dados abrangem dados de eventos de canais online. |
| 1b | O modelo de MTA é treinado. Normalmente, um modelo MMM é treinado em janelas de tempo de pelo menos dois anos. Os dados abrangem fatores, canais online e offline. |
| 2 | O modelo de MTA é pontuado. |
| 3 | Os resultados do modelo de MTA pontuado são alimentados no MMM como aprendizado de transferência. |
| 4 | O modelo MMM é atualizado com a transferência de dados de aprendizado. Essa atualização significa que um novo conjunto de estimativas de parâmetros é usado para insights adicionais e otimização de orçamento. Os canais e a cobertura de tempo não mudam. |
| 5 | O modelo MMM é pontuado usando os dados agregados semanais dos canais. |
| 6 | O resultado do modelo MMM pontuado é alimentado no MTA como aprendizado de transferência. |
| 7 | As pontuações do MTA para dados a nível de evento são atualizadas usando a transferência de resultados de aprendizado e são usadas para insights adicionais. |

Considere o seguinte:

* O MTA é limitado em relação à cobertura do canal (somente dados a nível de evento da Web e dados móveis, por exemplo), mas é vantajoso devido à grande quantidade de dados. O aspecto principal do MTA é o desempenho relativo.
* O MMM entende a imagem mais holística com fatores, canais online e offline.
* A transferência do aprendizado do MTA para o MMM atualiza o modelo MMM. Os resultados do aprendizado de transferência influenciam os parâmetros que direcionam o *modelo* multiplicativo. A transferência do aprendizado do MMM para o MTA atualiza as *pontuações* do MTA. Não há necessidade de influenciar o modelo de MTA, pois as pontuações iniciais já são estatisticamente suficientes.

## Conhecimento prévio

Portanto, além do MTA, MMM e experimentação, há muitas outras fontes diferentes de conhecimento prévio que você pode usar opcionalmente para o planejamento de medição de marketing. Empresas diferentes têm diferentes fontes de conhecimento prévio. Os exemplos incluem participação nos gastos, modelos internos anteriores ou experiência no setor.

![Conhecimento anterior](/help/assets/prior-knowledge.jpg)

O processo de criação do modelo pode aproveitar todas essas fontes de informação por meio do mesmo processo de aprendizagem de transferência. Essas fontes de conhecimento anteriores são opcionais. Você não precisa ter fontes de conhecimento anteriores para que a modelagem de mix de marketing funcione. Se você não tiver conhecimento prévio, o modelo padrão será usado para gerar insights de pontuação e, em seguida, otimização de orçamento. Se você tiver entrada de conhecimento anterior, poderá usar o aprendizado de transferência para atualizar o modelo MMM.


## Otimização de orçamento

A otimização do orçamento baseia-se no modelo MMM multiplicativo explicado anteriormente,

Em um exemplo simples, há dois canais: pesquisar e exibir. E você tem um orçamento total. O objetivo é dividir o orçamento entre os dois canais para maximizar a conversão. A otimização numérica é usada para encontrar a combinação de orçamento ideal que maximiza a conversão sob a restrição do orçamento total. Por exemplo, imagine que sua restrição de orçamento total seja de US$ 130.000.

A fórmula de otimização de orçamento é: *Max ⨍(X<sub>S</sub>, X<sub>D</sub>) = ⨍<sub>BL</sub>(X<sub>fatores</sub>) x ⨍ ⨍<sub>S</sub>(X<sub>S</sub>) x<sub>D</sub>(X<sub>D</sub>)*, onde *X<sub>S</sub>* e *X<sub>D</sub>* são parâmetros e *X<sub>fatores</sub>* são previstos.

![Restrições de orçamento](/help/assets/budget-constraints.png)


### Restrições no nível do canal

Imagine que você tenha restrições adicionais de nível de canal:

* US$ 10 mil a US$ 80 mil para pesquisa.
* US$ 5 mil a US$ 70 mil para exibição.
* US$ 130 mil no total.

Como resultado, a combinação de orçamento elegível faz com que a superfície de otimização seja restringida. O algoritmo de otimização numérica ajuda a determinar a alocação de orçamento ideal.

### Em várias conversões

Além das restrições no nível do canal, planeje a alocação de orçamento ideal entre várias conversões.

![Otimização de orçamento entre conversões](/help/assets/planning-across-multiple-conversions.jpg)

Para acomodar a alocação de orçamento ideal entre conversões, uma média ponderada da função acima para cada uma das conversões é usada. A fórmula torna-se *⨍<sub>nova</sub>(X) = w<sub>1</sub>f<sub>1</sub>(X) + w<sub>2</sub>f<sub>2</sub>(X)*

Exemplos de otimização de orçamento em várias conversões são:

* Você deseja maximizar a receita total das vendas online e conversões de vendas na loja.
* Você deseja otimizar o sucesso a longo prazo usando o KPI de percepção da marca e as conversões de vendas.

No segundo exemplo, as unidades das duas conversões não são semelhantes (KPI de reconhecimento de marca versus conversões), mas isso não importa. As conversões ou modelos não precisam se referir aos mesmos canais e também podem se sobrepor. A otimização numérica encontra a melhor solução para o problema dentro das restrições fornecidas.


## Resumo

O Adobe Marketing Campaign Analytics é mais do que uma ferramenta de medição; o Marketing Campaign Analytics é um mecanismo de suporte a decisões e seus pontos fortes são:

* A habilidade de modelar a complexidade do mundo real com rigor estatístico
* Uma integração unificada de dados diversos e paradigmas de modelagem
* Uma arquitetura que não se torna obsoleta e se adapta às tendências de descontinuação de dados

A combinação da capacidade de interpretação com o desempenho tornou o Marketing Campaign Analytics central para a transformação do marketing orientado por dados da Adobe. O Marketing Campaign Analytics capacita as equipes de marketing a tomar decisões de investimento mais rápidas, inteligentes e alinhadas.
