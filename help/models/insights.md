---
title: Informações do modelo
description: Saiba como obter detalhes sobre seu modelo, como visão geral histórica, insights do modelo e qualidade do modelo no Marketing Campaign Analytics.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
autotag-review: '2026-05-01T08:59:31.397Z'
TQID: 'https://experienceleague.adobe.com/zoUwqJXQ0z2ttUwvF1cn5ukSvn8-Cxhpv5lXlWENkQo'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
    internal-label: Datasets
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
    internal-label: Models
  - id: fe1c9ae8-a908-4ae1-a0b6-fcf35177b134
    internal-label: Marketing touch attribution
subfeature_v2:
  - id: a9505d76-24a1-4ffe-bd01-6ac32d5af453
    internal-label: Model insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 5dfbd7542422d93969c2ffe44475d847693e8910
workflow-type: tm+mt
source-wordcount: '3122'
ht-degree: 10%
---
# Insights do modelo

{{mm-mca-rebranding}}

Cada visualização em insights de modelo foi projetada para ajudar você a:

* Visualizar e quantificar o impacto das atividades de marketing da organização.
* Identificar os canais de alto desempenho.
* Identificar os canais que podem precisar de otimização.

Esses insights ajudam a oferecer suporte à priorização e alocação de recursos.

Para exibir insights do modelo, na interface ![Modelos](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** em [!DNL Marketing Campaign Analytics]:

1. Na tabela **[!UICONTROL Models]**, selecione o nome de um modelo que tenha um **[!UICONTROL Last run status]** de ![StatusGreen](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Success]**.

1. No menu de contexto, selecione **[!UICONTROL Model Insights]**.


As seguintes guias estão disponíveis:

* [Insights do modelo](#model-insights)
* [Análise de canal](#channel-analysis)
* [Fatores](#factors) [!BADGE beta]
* [Atribuição](#attribution) (somente para modelos habilitados para MTA)
* [Diagnóstico](#diagnostics)
* [Visão geral histórica](#historical-overview).

Se a [modelagem completa do funnel](./overview.md#full-funnel-modeling) estiver habilitada para o modelo, selecione o estágio do funnel (**[!UICONTROL Upper funnel]**, **[!UICONTROL Lower funnel]**, **[!UICONTROL Full funnel]**) no menu suspenso **[!UICONTROL Funnel stage]** para o qual deseja ver os insights do modelo.

É possível alterar o período de data no qual as visualizações em cada uma das guias se baseiam. Insira um período de data ou selecione ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um período de data.

## Desvio do modelo

{{release-limited-testing-section}}

Se for detectado um desvio de modelo no modelo, você verá uma caixa de diálogo **[!UICONTROL Model drift detected]** com opções para ser lembrada mais tarde ou para [**[!UICONTROL Retrain]**](overview.md#retrain) imediatamente o modelo. Se você selecionar **[!UICONTROL Remind me later]**, será lembrado no dia seguinte ou no próximo logon.

![Desvio de modelo detectado na caixa de diálogo](/help/assets/model-drift-dialog.png)

## Insights do modelo {#model-insights-section}

A guia **[!UICONTROL Model insights]** mostra visualizações para [Contribuição por data e mídia base](#contribution-by-date-and-base-media), [Contribuição por canal](#contribution-by-channel), [Resumo do desempenho de marketing](#marketing-performance-summary) e [Curvas de resposta marginal](#marginal-response-curves). A guia também fornece uma tabela [Detalhamento do ponto de contato](#touchpoint-breakdown).

![Modelo - Insights do modelo](/help/assets/model-insights-insights.png)

* Você pode passar o mouse sobre elementos de gráficos individuais em cada visualização para exibir um popover com mais detalhes.

* Para baixar um arquivo CSV contendo os dados da visualização, selecione ![Baixar](/help/assets/icons/Download.svg).

* Para baixar dados completos de insights do modelo no formato do Microsoft® Excel, selecione ![Baixar](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Contribuição por data e mídia base

Essa visualização de gráfico empilhado é ordenada da seguinte maneira:

* A base é exibida na parte inferior.
* Os canais de não gastos são exibidos no meio.
* Os canais de gasto são exibidos na parte superior.

Essa visualização representa a proporção de contribuição obtida pela base, por canais de gastos e por canais não gastos em um intervalo de datas. Esta visualização é útil para mostrar a incrementalidade. A base representa o que teria acontecido sem qualquer marketing, e o atributo de canais não gastos mais canais gastos (sobre a base) do impacto do seu marketing. Em resumo, não gastar mais gastar equivale ao impacto incremental de seus esforços de marketing e a visualização fornece um insight fácil no valor gerado pelo marketing.

### Contribuição por canal

Uma visualização de rosca que mostra uma distribuição da contribuição por vários canais. Essa visualização mostra incrementalidade através da lente dos canais com melhor desempenho. A visualização ajuda a oferecer suporte à priorização e à alocação de orçamento.

Você pode selecionar quais canais de mídia serão exibidos na visualização:

* Para se concentrar apenas na contribuição de canais de mídia paga, selecione **[!UICONTROL Paid media]**.
* Para ver a contribuição de todos os canais, selecione **[!UICONTROL All media]**.


### Resumo de desempenho de marketing {#marketing-performance-summary}

>[!CONTEXTUALHELP]
>id="models_insights_undefinedchannels"
>title="Canais indefinidos"
>abstract="Canais indefinidos são incluídos, mas não têm conversões atribuídas."

Uma visualização de gráfico de barras horizontal que mostra o desempenho do ROI ou CPA de cada canal. Esta visualização destaca o ROI/CPA de seus investimentos em marketing. Os canais são classificados em ordem decrescente com base no ROI/CPA. A visualização ajuda a identificar quais canais são mais eficazes e quais podem precisar de otimização.

Somente para modelos baseados em receita:

* Para configurar o **[!UICONTROL Metric]** desejado para a visualização, selecione entre **[!UICONTROL ROI]** (receita - gasto) / gasto) ou **[!UICONTROL ROAS]** (receita / gasto).
* Para configurar como a métrica selecionada é exibida, selecione entre **[!UICONTROL %]** ou **[!UICONTROL $]** para **[!UICONTROL Show as]**.

Canais indefinidos são incluídos na visualização, mas não têm conversões atribuídas.


### Curvas de resposta marginal

O gráfico de linhas visualiza e compara os retornos marginais gerados pelo investimento em seus canais de marketing.  E identifica o ponto de gasto atual e o ponto de equilíbrio marginal (em que seu retorno incremental é menor do que seu gasto incremental). Como resultado, essa visualização ajuda você a entender quando seu investimento em marketing começa a ter menos impacto.

A curva, o ponto de gasto atual, o ponto de equilíbrio marginal e os valores correspondentes são calculados com base no intervalo de dados selecionado e no canal selecionado.

Para alterar o canal:

* Selecione um canal no menu suspenso **[!UICONTROL Channel]** para atualizar a visualização de um canal específico.

## Fluxo do funnel

{{release-limited-testing-section}}

Se a [modelagem completa do funnel](./overview.md#full-funnel-modeling) estiver habilitada para o modelo e você tiver selecionado funnel completo no menu suspenso do Funnel stage, uma visualização de fluxo do Funnel estará disponível.

>[!BEGINTABS]

>[!TAB Fluxo do Funnel]

![Fluxo do Funnel](/help/assets/model-funnel-flow.png)

>[!TAB Passe o mouse sobre o fluxo do funnel]

![Todas as sinergias do canal de planos](/help/assets/model-funnel-flow-hover.png)

>[!ENDTABS]

Passe o mouse sobre qualquer fluxo para ver um pop-up com mais detalhes para o fluxo específico do funnel.

O canal associado à conversão superior de funnel selecionada (conforme definido em [Conversões](/help/harmonize-data/conversions.md)) é exibido no centro da visualização (por exemplo: **[!UICONTROL Store]**).

### Detalhamento do ponto de contato

A tabela de detalhamento de ponto de contato mostra os detalhamentos semanais do ponto de contato para todos os canais ou para os canais selecionados, semanalmente, exibindo as métricas principais associadas a cada um. A tabela permite uma fácil comparação, identificação de tendências e rastreamento de desempenho em um nível de canal mais granular. Esta tabela complementa explicitamente a visualização [Contribuição por data e mídia base](#contribution-by-date-and-base-media) e a visualização [Contribuição por canal](#contribution-by-channel).

![Detalhamento do ponto de contato](../assets/touchpoint-breakdown.png)

As seguintes colunas estão disponíveis:

| Coluna | Descrição |
|---|---|
| **[!UICONTROL Date range]** | A semana para relatar. |
| **[!UICONTROL Touchpoint]** | O canal de ponto de contato específico. |
| **[!UICONTROL ROI]** | A porcentagem de (**[!UICONTROL Revenue]** - **[!UICONTROL Spend]**) / **[!UICONTROL Spend]**. |
| **[!UICONTROL Revenue]** | A receita do intervalo de datas. |
| **[!UICONTROL CPA]** | **[!UICONTROL Spend]** / **[!UICONTROL Conversions]**. |
| **[!UICONTROL Conversions]** | As conversões do intervalo de datas. |
| **[!UICONTROL Spend]** | O gasto para o intervalo de dados. |

Para selecionar um canal específico ou todos os canais, selecione no menu suspenso **[!UICONTROL View]**.

Para baixar o conteúdo da tabela de detalhamento Touchpoint, selecione ![Baixar](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]**.


## Análise de canal

A guia **[!UICONTROL Channel analysis]** mostra visualização para **[!UICONTROL Channel synergies]** e **[Estoque de canal]**.


### Sinergias de canal

A visualização de sinergias de canal ajuda a identificar como os canais de marketing interagem para criar efeitos multiplicativos, além de suas contribuições individuais.

A matriz do mapa de calor fornece uma representação visual dos valores de sinergia entre pares de canais de gastos. Essa matriz ajuda os profissionais de marketing a entender como os canais interagem para impulsionar o desempenho. Para cada modelo, os valores de sinergia são normalizados de 0 a 10. Esses valores quantificam a *sinergia do próximo dólar*, que estima a eficiência com que dois canais trabalham juntos quando cada um recebe um dólar adicional de gasto nos níveis atuais.

Este quadro de despesas de nível superior oferece uma medida realista da força de sinergia relativa, uma vez que o quadro tem em conta as condições reais de despesas nos dados de formação e, como tal, permite decisões de otimização mais informadas.

Se a [modelagem completa do funnel](./overview.md#full-funnel-modeling) estiver habilitada para o modelo, você verá uma visualização para sinergias de canal do funnel Superior e para sinergias de canal do funnel Inferior.

>[!BEGINTABS]

>[!TAB Mostrar menos sinergias de canal]

![Planejar menos sinergias do canal](/help/assets/model-channel-synergies-less.png)

>[!TAB Mostrar todas as sinergias de canal]

![Todas as sinergias do canal de planos](/help/assets/model-channel-synergies-all.png)

>[!TAB Sinergias do Funnel]

![Planejar sinergias do funnel do canal](/help/assets/model-channel-synergies-funnel.png)

>[!ENDTABS]


* Para mostrar todas as sinergias, selecione **[!UICONTROL Show all]**.

* Para selecionar menos sinergias, selecione **[!UICONTROL Show less]**

* Para mostrar detalhes de uma sinergia, passe o mouse sobre uma célula na visualização.

* Para baixar um arquivo CSV que representa a matriz, selecione ![Baixar](/help/assets/icons/Download.svg) **[!UICONTROL Download]**.

>[!NOTE]
>
>Se a guia **[!UICONTROL Channel synergy]** não estiver visível para um modelo existente, treine novamente o modelo para habilitar a funcionalidade e a visualização.


### Adstock do canal

As visualizações de adstock de canal mostram uma visualização para cada adstock de canal configurado. As visualizações ajudam você a entender como o impacto dos gastos com marketing para cada canal persiste e se deteriora com o tempo e além da exposição inicial. A visualização fornece uma visualização realista do transporte de canais através da incorporação de dinâmicas temporais que são aprendidas a partir do modelo.

Cada gráfico individual representa um único canal de marketing e mostra sua curva adstock. Essa curva modela como o efeito de uma unidade de exposição transita para períodos futuros. A curva ilustra a taxa em que o impacto na conversão diminui e ajuda os profissionais de marketing a comparar por quanto tempo diferentes canais continuam a influenciar o desempenho após o investimento inicial.

Canais com curvas de decaimento mais lentas (caudas mais longas) indicam impacto sustentado ao longo do tempo. Canais com quedas acentuadas refletem efeitos mais imediatos e de curta duração. O período máximo de lookback configurado para esse canal determina o comprimento de cada curva.

>[!BEGINTABS]

>[!TAB Mostrar todos os adstock]

![Planejar sinergias de canal](/help/assets/model-channel-adstock-all.png)

>[!TAB Mostrar o adstock selecionado]

![Planejar sinergias de canal](/help/assets/model-channel-adstock-selected.png)

>[!ENDTABS]

* Se a [modelagem completa do funnel](./overview.md#full-funnel-modeling) estiver habilitada para o modelo, selecione funnel Superior ou funnel Inferior no menu suspenso Funnel stage.
* Para exibir visualizações de estoque para **[!UICONTROL All channels]** ou uma visualização de estoque para um canal individual (por exemplo, **[!UICONTROL Paid Social Facebook]**), selecione no menu suspenso **[!UICONTROL Channel]**.


## Fatores {#factors}

>[!CONTEXTUALHELP]
>id="models_factors_factorcontributionbreakdown"
>title="Detalhamento da contribuição do fator"
>abstract="O detalhamento da contribuição dos fatores mostra a proporção das conversões base que podem ser atribuídas aos vários fatores incluídos no modelo.<br/><br/>A base pura representa as conversões subjacentes que ocorrem independentemente dos pontos de contato de marketing e dos fatores incluídos no modelo. Isso inclui conversões impulsionadas por valor da marca, compras repetidas, demanda orgânica e tendências de mercado de longo prazo e sazonalidade."


A guia Fatores [!BADGE beta] mostra insights relacionados ao fator externo.

![Fatores](/help/assets/factors.png)

Essa visualização ajuda você a entender o efeito incremental que vários fatores internos e externos têm na linha de base das conversões. Por exemplo, condições econômicas ou atividades promocionais.

Use o menu suspenso **[!UICONTROL Factors]** para selecionar quais fatores você deseja exibir.

<!-- need to update the image when we do have a proper example -->

Para baixar um arquivo CSV contendo os dados da tabela, selecione ![Baixar](/help/assets/icons/Download.svg).

Se nenhum dado estiver disponível, você verá a mensagem ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## Atribuição {#attribution}

>[!CONTEXTUALHELP]
>id="models_attribution_breakdownbychannel"
>title="Detalhamento por canal"
>abstract="**[!UICONTROL Breakdown by channel]** é um detalhamento por tipo de canal para os pontos de contato definidos, com base no esquema de evento de experiência do cliente. Selecione ![Mais](/help/assets/icons/More.svg) e **[!UICONTROL Breakdown by touchpoint]** para mostrar um detalhamento por ponto de contato."


>[!CONTEXTUALHELP]
>id="models_attribution_breakdownbytouchpointposition"
>title="Detalhamento por posição de ponto de contato"
>abstract="Essa visualização mostra um detalhamento das conversões atribuídas por posição do ponto de contato e em todos os caminhos de conversão. A visualização compara se um ponto de contato contribui melhor em uma posição do que nas demais opções e do que outros pontos em qualquer posição."



>[!NOTE]
>
>A guia Atribuição só está disponível para modelos habilitados para MTA.

Usando a guia [!UICONTROL Attribution], você pode entender a eficácia dos pontos de contato e campanhas de marketing que têm dados de nível de evento.  Consulte [Modelo de compilação](build.md).

Os seguintes modelos de atribuição são compatíveis:

* Com base no modelo selecionado em [!DNL Marketing Campaign Analytics]:
  * Algorítmico - Influenciado
  * Algorítmico - Incremental
* Baseado em regra:
  * Unidades de decaimento
  * Primeiro contato
  * Último contato
  * Linear
  * Ushape

Consulte [Atribuição multitoque](../get-started/about.md#multi-touch-attribution) para obter uma introdução sobre o recurso de atribuição multitoque em [!DNL Marketing Campaign Analytics].

Selecione um ou mais modelos de atribuição no menu suspenso **[!UICONTROL Attribution Model]**. Os modelos de atribuição selecionados se aplicam a todas as visualizações na guia Atribuição.

![Atribuição](/help/assets/model-insights-attribution.png)

As pontuações do evento granular de atribuição multitoque do Marketing Campaign Analytics são alinhadas às [!DNL Marketing Campaign Analytics] pontuações e aos ROIs gerais. Essas pontuações também são disponibilizadas como conjuntos de dados no Experience Platform.

A guia Atribuição consiste nas seguintes visualizações:

### Visão geral

A visualização [!UICONTROL Overview] mostra, para os modelos de atribuição selecionados, os totais e as porcentagens de conversões. Selecionar mais modelos adiciona círculos adicionais à visualização, cada um com sua própria cor correspondente à legenda.

Para ver um pop-up com detalhes de um modelo de atribuição, passe o mouse sobre qualquer um dos círculos na visualização.

### Tendências

A visualização [!UICONTROL Daily trends], [!UICONTROL Weekly trends] ou [!UICONTROL Monthly trends] mostra, para os modelos de atribuição selecionados, as tendências de conversão diárias, semanais ou mensais.

Para escolher o período, selecione **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** ou **[!UICONTROL Monthly trends]** de ![Mais](/help/assets/icons/More.svg).

Para ver os detalhes, passe o mouse sobre a linha de dados de um modelo de atribuição específico para exibir um popover que mostra o número total de conversões desses dados.

### Detalhamento

A visualização [!UICONTROL Breakdown] é um detalhamento por canal ou ponto de contato das conversões para cada um dos modelos de atribuição selecionados. Essa visualização pode ser útil para tomar decisões sobre a eficácia de cada canal ou ponto de contato.

Para escolher o tipo de detalhamento, selecione **[!UICONTROL Breakdown by channel]** ou **[!UICONTROL Breakdown by touchpoint]** de ![Mais](/help/assets/icons/More.svg).

Para ver detalhes, passe o mouse sobre qualquer um dos elementos do gráfico.

### Principais campanhas

A visualização Campanhas principais mostra uma tabela das campanhas principais com colunas para Nome da campanha, Canal, Tipo de mídia e Conversões incrementais. Essa visualização pode ajudar a informar sua equipe sobre a eficácia de uma campanha específica para um determinado canal e fornecer insights sobre em quais campanhas você deve investir ainda mais.

Para classificar a tabela em ordem crescente ↑ ou decrescente ↓ para Canal, Tipo de mídia ou Conversões incrementais, selecione o cabeçalho da coluna e alterne a classificação.

Para expandir a tabela em uma caixa de diálogo separada, selecione **[!UICONTROL Expand]** de ![Mais](/help/assets/icons/More.svg).

A caixa de diálogo **[!UICONTROL Top campaigns]** expandida mostra a mesma tabela com colunas de adição para:

* Conversões incrementais
* Conversões influenciadas
* Conversões de primeiro contato
* Conversões de último contato

  Você pode selecionar cada um dos cabeçalhos de coluna adicionais para classificar a tabela em ordem crescente ou decrescente.

Para fechar a caixa de diálogo Campanhas principais expandida, selecione **[!UICONTROL Close]**.


### Detalhamento por posição de ponto de contato

A visualização [!UICONTROL Breakdown by touchpoint position] é um detalhamento das conversões atribuídas por posição do ponto de contato e do ponto de contato em todos os caminhos de conversão. Este gráfico ajuda a comparar se um ponto de contato contribui melhor em uma posição do que as posições restantes e outros pontos de contato em qualquer posição.

>[!NOTE]
>
>A soma da contribuição percentual para um modelo de atribuição em todos os pontos de contato e posições deve ser igual a 100.


As posições [!UICONTROL Starter], [!UICONTROL Player] e [!UICONTROL Closer] são definidas da seguinte maneira:

| Position | Descrição |
|---|---|
| [!UICONTROL Starter] | Essa posição indica se o ponto de contato é o primeiro contato em um caminho de conversão. |
| [!UICONTROL Player] | Essa posição indica se o ponto de contato não é o primeiro ou o último contato que leva à conversão. |
| [!UICONTROL Closer] | Essa posição indica se o ponto de contato é o último contato antes da conversão. |


### Principais caminhos de conversão

A visualização [!UICONTROL Top conversion paths] mostra os 5 principais caminhos de conversão com base nos modelos de atribuição selecionados.

Para cada caminho de conversão, você verá:

* o número de canais que têm impacto,
* o total de caminhos atribuídos,
* a porcentagem de caminhos atribuídos para esse caminho de conversão em relação ao total de caminhos atribuídos,
* para cada canal, a porcentagem de contribuição do modelo de atribuição e
* a soma dessas porcentagens de contribuição do modelo de atribuição de canal.


## Diagnóstico {#diagnostics}

>[!CONTEXTUALHELP]
>id="models_diagnostics_modelassessment"
>title="Gráficos de avaliação de modelo"
>abstract="As visualizações de avaliação de modelo detalham as conversões reais em relação às previstas ou residuais."


>[!CONTEXTUALHELP]
>id="models_diagnostics_modeltrainingfitmetrics"
>title="Métricas de ajuste do modelo"
>abstract="Mostra uma visão geral de várias métricas de ajuste de treinamento de modelo."


>[!CONTEXTUALHELP]
>id="models_diagnostics_pathstouched"
>title="Caminhos tocados"
>abstract="Caminhos tocados é a porcentagem de caminhos que atingem a conversão e a porcentagem de caminhos que não atingem a conversão para cada ponto de contato."


>[!CONTEXTUALHELP]
>id="models_diagnostics_efficiencymeasure"
>title="Medida de eficiência"
>abstract="A medida de eficiência gerada pelo modelo de atribuição algorítmica indica a importância relativa de um ponto de contato para uma conversão independente do volume do ponto de contato. Isso é medido em uma escala de 1 a 5. Observe que um volume maior de pontos de contato não garante uma eficiência mais alta."


>[!CONTEXTUALHELP]
>id="models_diagnostics_totalvolume"
>title="Volume total"
>abstract="O volume total é o número agregado de vezes que um usuário chega a um ponto de contato. E inclui os pontos de contato que aparecem em um caminho que o alcança, bem como caminhos que não resultam em conversão."


>[!CONTEXTUALHELP]
>id="models_diagnostics_modeldateinfo"
>title="Data do modelo a partir de"
>abstract="Os dados desta tabela são gerados apenas para períodos específicos.  A data **[!UICONTROL As of]** indica quando os dados foram gerados e se baseia nos dados da data especificada até um ano atrás."


A guia **[!UICONTROL Diagnostics]** mostra visualizações para:

* **[!UICONTROL Model Assessment]** visualizações que consistem em:

  ![Avaliação de modelo](../assets/model-assessment.png)

  * Um gráfico que pode ser detalhado em conversões reais versus previstas ou residuais.
    Para detalhar a visualização, selecione uma das seguintes opções na lista **[!UICONTROL Breakdown]**.

    * **[!UICONTROL Actual vs Predicted]**: esta opção compara valores reais a previsões de modelo. Idealmente, os valores previstos devem se alinhar com os valores reais, embora seja esperado algum desvio. Desvios ou padrões grandes ou sistemáticos podem indicar relações e dados ausentes ou possíveis vieses.

    * **[!UICONTROL Residuals]**: esta opção mostra a diferença entre valores reais e previstos. Um modelo bem-sucedido tem resíduos que são distribuídos aleatoriamente, sem padrões claros ou aumento da disseminação. Tendências estruturadas ou alargamento de resíduos podem indicar relações ausentes e problemas de dados ou variância.

  * Uma tabela que mostra as seguintes colunas para cada métrica de conversão:

    * **[!UICONTROL Actual Conversion]**
    * **[!UICONTROL Predicted Conversion]**
    * **[!UICONTROL Residual Conversion]**
    * **[!UICONTROL R<sup>2</sup>]**, uma pontuação que informa como os dados se ajustam ao modelo de regressão (a adequação do ajuste).
    * **[!UICONTROL MAPE]** (Erro Percentual Absoluto Médio), que é um dos KPIs mais usados para medir a precisão da previsão e expressa o erro de previsão como uma porcentagem do valor real.
    * **[!UICONTROL RMSE]** (Erro de Média Quadrada de Raiz): que mostra o erro médio, ponderado de acordo com o quadrado do erro.

  Para baixar um arquivo CSV contendo os dados da tabela, selecione ![Baixar](/help/assets/icons/Download.svg).

* Tabela **[!UICONTROL Model training fit metrics]** que é exibida para cada métrica de conversão:

  ![Tabela de métricas de ajuste de treinamento de modelo](../assets/model-training-fit-metrics.png)

  * **[!UICONTROL Training R<sup>2</sup>]**: indica a proporção de variação nos valores reais explicados pelas previsões do modelo, variando de 0 a 1.
  * **[!UICONTROL Training sMAPE]** (Erro de Porcentagem Absoluta Média simétrica): mede o erro de porcentagem média nos dados de treinamento. Valores mais baixos indicam melhor precisão.
  * **[!UICONTROL Training RMSE]** (Erro de Raiz Média Quadrada): Mede o erro de porcentagem média nos dados de treinamento. Penaliza mais erros maiores do que o MAPE. RMSE mais baixo sugere melhor precisão preditiva, mas é sensível a outliers.
  * **[!UICONTROL Out-of-sample sMAPE]**: Avalia a porcentagem de erro em dados não vistos, equilibrando previsões demais e inferiores. Ajuda a avaliar a generalização. Atualmente, o Marketing Campaign Analytics avalia o erro percentual usando o último trimestre dos dados de treinamento como um conjunto de controle.
  * **[!UICONTROL Out-of-sample RMSE]**: Avalia a porcentagem de erro em dados não vistos, equilibrando previsões demais e inferiores. Ajuda a avaliar a generalização. Atualmente, [!DNL Marketing Campaign Analytics] avalia o erro percentual usando o último trimestre dos dados de treinamento como um conjunto de controle. O RMSE penaliza mais erros maiores do que o MAPE.


* Tabela **[!UICONTROL Touchpoint effectiveness]**, que representa o resultado do modelo algorítmico da IA de atribuição.

  ![Tabela de eficácia do ponto de contato](../assets/touchpoint-effectiveness.png)

  Os dados desta tabela são gerados apenas para períodos específicos. Selecione **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) para obter mais detalhes.

  A visualização mostra, em ordem decrescente de [!UICONTROL Efficiency measure] ![Ordem decrescente](/help/assets/icons/SortOrderDown.svg), para cada ponto de contato:

  * **[!UICONTROL Paths touched]**: visualiza a porcentagem de caminhos que atingem a conversão e a porcentagem de caminhos que não atingem a conversão. Para um ponto de contato, você verá mais conversões atribuídas quando a taxa de conversão de atribuição estiver alta. Essa proporção compara a porcentagem de caminhos que levam à conversão com a porcentagem de caminhos que *não* levam à conversão.
  * **[!UICONTROL Efficiency measure]**: gerada pelo modelo de atribuição algorítmica, a medida de eficiência indica a importância relativa de um ponto de contato em direção à conversão, independentemente do volume do ponto de contato. A eficiência é medida em uma escala de 1 a 5. Observe que um volume maior de pontos de contato não garante uma eficiência mais alta.
  * **[!UICONTROL Total volume]**: O número agregado de vezes que um usuário toca um ponto de contato. O número inclui os pontos de contato que aparecem em um caminho que alcança a conversão, assim como os caminhos *não* que resultam na conversão.


### Detecção de desvio de modelo

>[!AVAILABILITY]
>
>A funcionalidade descrita nesta seção está na fase de Teste limitado da versão e pode ainda não estar disponível em seu ambiente. Essa nota é removida quando a funcionalidade do geralmente está disponível. Para obter informações sobre o processo de lançamento [!DNL Marketing Campaign Analytics], consulte [versões de recursos do Marketing Campaign Analytics](/help/releases/latest.md).
>

Se for detectado descompasso de modelo, você verá uma notificação **[!UICONTROL Model drift detected]** na parte superior.

![Notificação de descompasso do modelo](/help/assets/model-drift-notification.png)

Selecione **[!UICONTROL Hide]** para ocultar a notificação. A notificação reaparecerá no dia seguinte ou no próximo logon.


## Visão geral histórica

A guia Visão geral histórica mostra visualizações para:

![Modelo - Visão geral histórica](/help/assets/model-insights-historical-overview.png)


### Conversão e gasto por trimestre fiscal e produto

Esta visualização representa a conversão e a distribuição de gastos em vários trimestres dentro do intervalo de datas especificado. A visualização ajuda a identificar trimestres de alto desempenho nos quais o gasto está gerando conversões.


### Gastos por canal

Esta visualização representa a distribuição de gastos em vários canais dentro do intervalo de datas especificado. A visualização permite a identificação rápida de quais canais recebem mais gastos.


### Gastos com Touchpoint

Esta visualização representa a distribuição de gastos em pontos de contato pagos para cada trimestre dentro do intervalo de datas especificado. A visualização permite compreender quais pontos de contato são priorizados em canais e trimestres específicos. A visualização ajuda a identificar padrões e tendências de gasto do canal, especialmente canais com gasto baixo e pouco frequente ao longo do tempo.

Para exibir um canal alternativo com base em gastos para essa visualização:

* Selecione um canal de **[!UICONTROL Channels]**.


### Volume do ponto de contato

Essa visualização representa a distribuição do volume em todos os pontos de contato para cada trimestre dentro do intervalo de datas especificado.

Para exibir um canal alternativo baseado em volume para essa visualização:

* Selecione um canal de **[!UICONTROL Channels]**.

