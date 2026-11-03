---
title: Visão geral de modelos
description: Saiba como criar, treinar, pontuar e gerenciar modelos de aprendizado de máquina no Marketing Campaign Analytics para medir e prever resultados de marketing.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
autotag-review: '2026-05-01T08:59:10.903Z'
TQID: 'https://experienceleague.adobe.com/T37YTKQlT1mUIfGkJwQkLLGkP0WfTs6jUbZpskPUHgo'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a234aebd-3855-4376-a64d-29b38411e0c5
    internal-label: Marketing mix modeling
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
    internal-label: Models
  - id: fe1c9ae8-a908-4ae1-a0b6-fcf35177b134
    internal-label: Marketing touch attribution
subfeature_v2:
  - id: a9505d76-24a1-4ffe-bd01-6ac32d5af453
    internal-label: Model insights
  - id: c89e26b6-808d-4500-8b01-450a63466999
    internal-label: Build model
  - id: cb40363e-1205-4921-971c-9ee6bdb18329
    internal-label: Scoring data
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: c75532d37a87f39cb61eabd58333b39895cf3a69
workflow-type: tm+mt
source-wordcount: '1329'
ht-degree: 0%
---
# Visão geral dos modelos

{{mm-mca-rebranding}}

A funcionalidade do modelo no Marketing Campaign Analytics permite configurar, treinar e pontuar modelos específicos para seus objetivos comerciais. O treinamento e a pontuação oferecem suporte ao aprendizado de transferência orientado por IA entre a atribuição multitoque e a modelagem de mix de marketing.

Os modelos são baseados nos dados harmonizados que você cria como parte do fluxo de trabalho do aplicativo.

Um modelo no Marketing Campaign Analytics é um modelo de aprendizado de máquina empregado para medir e prever um resultado especificado com base em investimentos de marketing. Pontos de contato de marketing e dados de nível de resumo podem ser usados como uma entrada. O Marketing Campaign Analytics permite criar variantes de modelos com base em diferentes conjuntos de variáveis, dimensões e resultados, como receitas, unidades vendidas e clientes potenciais.

Um modelo requer:

* Uma conversão.
* Um ou mais pontos de contato de marketing (canais) compostos de dados de nível de resumo, dados de pontos de contato de marketing (dados do evento) ou ambos.
* Uma janela de pesquisa configurável.
* Uma janela de treinamento configurável.

Um modelo pode incluir opcionalmente:

* Fatores externos.
* Fatores internos.
* Conhecimento prévio das contribuições de marketing de outras fontes, como experiência prévia das partes interessadas, testes incrementais e outros modelos.
* Gastar compartilhamento, que usa compartilhamento de gasto relativo como proxy quando os dados de marketing são escassos.

Quando um modelo é criado pela primeira vez, a criação inicia imediatamente o processo de treinamento e pontuação. Após a conclusão da execução inicial de treinamento e pontuação, os insights do modelo ficam disponíveis para revisão. Um modelo é subsequentemente retreinado. Além disso, quando os dados são adicionados ao modelo, é necessária uma pontuação manual do modelo. O novo treinamento e a nova pontuação são um processo iterativo à medida que surgem novas descobertas e informações, e são necessários ajustes para obter um modelo mais adequado aos seus objetivos de negócios.

## Modelagem completa do funnel

{{release-limited-testing-section}}

A modelagem completa do funnel permite modelar os estágios reais de sua funnel. Por exemplo, desde a inscrição no boletim informativo até uma compra. A modelagem completa do funnel mostra como o marketing impulsiona os clientes por meio desse funnel. A modelagem completa do funnel oferece crédito dos canais funnel superiores pelas conversões que esses canais influenciam downstream e reconcilia os resultados para que as contribuições sejam adicionadas corretamente sem contagem dupla.

Use a modelagem completa do funnel para modelar em um KPI superior do funnel com um KPI inferior do funnel.

* Exemplos de KPIs superiores do funnel são assinaturas de boletins informativos e outras métricas de percepção da marca.
* Exemplos de métricas inferiores do funnel são métricas de conversão típicas, como receita e pedidos.

As táticas superiores do funnel geralmente recebem menos crédito em um modelo MMM com foco em conversão. A modelagem completa do funnel ajuda você a entender:

* Quais táticas de mídia e marketing contribuíram para a meta superior do funnel.
* Quais táticas de mídia e marketing causaram impacto indireto na meta de conversão. Os pesos superiores do modelo do funnel são uma entrada para o modelo inferior do funnel para oferecer maior peso à mídia e às táticas de marketing, quando relevante.

## Criar modelos

Para criar um modelo, use o fluxo de configuração de modelo guiado passo a passo da Marketing Campaign Analytics disponível ao selecionar **[!UICONTROL Open model canvas]**. Consulte [Criar modelos](build.md) para obter mais detalhes.

## Gerenciar modelos

Para exibir uma tabela dos modelos atuais, na interface do Marketing Campaign Analytics:

1. Selecione ![FileDataS2](/help/assets/icons2/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Você verá uma tabela dos modelos atuais.

   As colunas da tabela especificam detalhes sobre o modelo.

   | Nome da coluna | Detalhes |
   |---|---|
   | **[!UICONTROL Name]** | Nome do modelo. Se um modelo estiver habilitado para modelagem completa do funnel, você verá uma mensagem de [!BADGE funnel]{type=Informative} completa. |
   | **[!UICONTROL Description]** | Descrição do modelo. |
   | **[!UICONTROL Conversion event]** | A conversão selecionada para o modelo. |
   | **[!UICONTROL Run frequency]** | A frequência de execução do treinamento do modelo. |
   | **[!UICONTROL Last run]** | A data e hora do último treinamento do modelo. |
   | **[!UICONTROL Status]** | O status do modelo. |

   Para classificar a tabela em qualquer coluna em ordem crescente de ![ArrowMoveUpS2](/help/assets/icons2/ArrowMoveUp.svg) ou decrescente de ![ArrowMoveDownS2](/help/assets/icons2/ArrowMoveDown.svg), selecione o título da coluna.

   Para classificar ou redimensionar a coluna **[!UICONTROL Name]**, selecione **[!UICONTROL Name]** ![Divisa](/help/assets/icons/ChevronDown.svg). No menu de contexto, selecione **[!UICONTROL Sort ascending]**, **[!UICONTROL Sort descending]** ou **[!UICONTROL Resize column]**. Para redimensionar a coluna **[!UICONTROL Name]**, passe o mouse sobre o separador de colunas.

   O status relatado do modelo depende de onde um modelo está em seu ciclo de vida. Por exemplo, se um modelo é criado, (re)treinado com sucesso ou não, ou (re)pontuado com sucesso ou não.

   Na tabela abaixo:

   * ![Marca de seleção](/help/assets/icons/Checkmark.svg) - indica uma execução bem-sucedida de uma etapa no ciclo de vida do modelo.
   * ![Relógio](/help/assets/icons/Clock.svg) - indica uma execução em andamento atual de uma etapa no ciclo de vida do modelo.
   * ![Fechar](/help/assets/icons/Close.svg) - indica uma falha na execução de uma etapa no ciclo de vida do modelo.

   | Status | [Compilação](/help/models/build.md) | [Treinamento](/help/models/train-score.md#train) | [Pontuação](/help/models/train-score.md#score) | [Retreinar](/help/models/train-score.md#train) | [Pontuação](/help/models/train-score.md#score) |
   |---|:---:|:---:|:---:|:---:|:---:|
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | | | | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) | | | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) | | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) | |
   | Em andamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Relógio](/help/assets/icons/Clock.svg) |
   | Falha no treinamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) | | | |
   | Falha no treinamento | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) | |
   | Treinamento bem-sucedido | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | | | |
   | Treinamento bem-sucedido | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | |
   | Falha na pontuação | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) | | |
   | Falha na pontuação | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Fechar](/help/assets/icons/Close.svg) |
   | Pontuação bem-sucedida | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | | |
   | Pontuação bem-sucedida | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) | ![Marca de seleção](/help/assets/icons/Checkmark.svg) |

   {style="table-layout:fixed"}

1. Para alterar as colunas exibidas para a lista, selecione ![Configurações de coluna](/help/assets/icons/ColumnSetting.svg) e alterne as colunas em ![Verificar](/help/assets/icons/Checkmark.svg) ou desativar.

Você pode executar as seguintes ações em um modelo específico.

### Insights do modelo

A funcionalidade de insights do modelo só está disponível em modelos treinados e pontuados com êxito.

Para exibir os insights de um modelo:

1. Selecione ![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.
1. Selecione o nome do modelo.

Você foi redirecionado para [Informações sobre Modelos](insights.md).

### Exibir detalhes

Para exibir mais detalhes de um modelo:

1. Selecione ![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Informações](/help/assets/icons/Info.svg) para que um modelo mostre um pop-up com detalhes como **[!UICONTROL Description]**, **[!UICONTROL Run frequency]**, **[!UICONTROL Last run status]**, **[!UICONTROL Spend share]** e muito mais.




### Duplicar

É possível duplicar um modelo rapidamente.

1. Selecione ![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Duplicate]**.

Você é redirecionado para as etapas de criação de um novo modelo, com um nome proposto composto pelo nome do modelo original anexado com **[!UICONTROL (Copy)](_n_)**.

### Editar

É possível editar o nome, a descrição e a programação de treinamento e pontuação de um modelo.

1. Selecione ![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Edit]**.

   No diálogo **[!UICONTROL Edit model]**:

   ![Editar um modelo](../assets/model-edit.png)

   * Insira um(a) novo(a) **[!UICONTROL Name]** e **[!UICONTROL Description]**.

   * Para habilitar o agendamento, habilite **[!UICONTROL Enable schedule model training and scoring]**. Você só pode habilitar a programação para modelos treinados e pontuados.

     1. Selecione um **[!UICONTROL Scoring frequency]**:

        * **[!UICONTROL Daily]**: Insira uma hora válida (por exemplo `10:00 am`) ou use ![Clock](/help/assets/icons/Clock.svg) para definir a hora.
        * **[!UICONTROL Weekly]**: Selecione um dia da semana e insira uma hora válida (por exemplo `10:00 am`) ou use ![Relógio](/help/assets/icons/Clock.svg) para definir a hora.
        * **[!UICONTROL Monthly]**: Selecione um dia do mês no menu suspenso Executar em cada e insira um horário válido (por exemplo `10:00 am`) ou use ![Relógio](/help/assets/icons/Clock.svg) para definir o horário.

     1. Selecione um **[!UICONTROL Training frequency]** no menu suspenso: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** ou **[!UICONTROL None]**.

   * Se o modelo completo do funnel estiver ativado, uma atribuição desativada Ativar funnel completo estará visível. Não é possível modificar essa configuração.

   * Para [disponibilizar dados de pontuação para o Customer Journey Analytics](build.md#customer-journey-analytics), selecione **[!UICONTROL Enable scores for Customer Journey Analytics]**.

     Depois que as pontuações são ativadas para o Customer Journey Analytics, você não pode desativar essa configuração, a menos que o modelo seja excluído.

   * Para atualizar os [campos de relatórios de insights granulares](/help/models/build.md#granular-insights-reporting-fields), na seção **[!UICONTROL Granular Insights Reporting Fields]**:
     1. Selecione um ou mais campos harmonizados em **[!UICONTROL _Selecionar campos harmonizados_]** abaixo de **[!UICONTROL Includes]**. Os campos harmonizados selecionados são adicionados ao painel.
     1. Selecione **[!UICONTROL *Campo harmonizado *]**![CrossSize100](/help/assets/icons/CrossSize100.svg) para remover um campo harmonizado do contêiner com os campos harmonizados selecionados.
     1. Selecione **[!UICONTROL Clear all]** para remover todos os campos harmonizados selecionados.

     >[!IMPORTANT]
     >Qualquer modelo com MTA criado antes de 12 de janeiro de 2026 deve ser duplicado para habilitar insights de modelo granular.<br/>
     >A pontuação é necessária para que qualquer modelo existente reflita as dimensões granulares atualizadas nos dados de pontuação.
     >

1. Selecione **[!UICONTROL Save]**.

### Treinamento

Treine novamente um modelo quando quiser incluir novos dados de marketing incremental e de fatores. Consulte [Modelos de treinamento e pontuação](train-score.md#train) para obter mais informações.

### Pontuação

Você pode pontuar incrementalmente um modelo com base em novos dados de marketing ou repontuar um modelo para um intervalo de datas específico. Consulte [Modelos de treinamento e pontuação](train-score.md#score) para obter mais informações.

### Excluir modelos

Para excluir um modelo:

1. Selecione ![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.
1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Delete]**. Como alternativa, selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** da barra de ação azul.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete model]** para excluir o modelo. Selecione **[!UICONTROL Cancel]** para cancelar.

Para excluir vários modelos:

1. Selecione vários modelos.
1. Na barra de ação azul, selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para excluir os modelos.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete *x *modelos]**para excluir os modelos. Selecione **[!UICONTROL Cancel]**para cancelar.

