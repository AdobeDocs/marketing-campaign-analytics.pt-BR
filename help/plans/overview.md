---
title: Visão geral dos planos
description: Saiba como exibir, selecionar e executar ações em planos no Marketing Campaign Analytics.
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
autotag-review: '2026-05-01T09:05:53.776Z'
TQID: 'https://experienceleague.adobe.com/OZjW5A4DP1raHwQgA5RSrbyFAwEp5gKPrzezj59nnFA'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
  - id: d822825b-9821-40d5-9b0d-42a9e3f317c5
    internal-label: Plans
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
    internal-label: Models
subfeature_v2:
  - id: d7b067e6-4f39-41e9-a081-7650346a84cd
    internal-label: Build plans
  - id: b2520ae7-8f6c-4952-935e-aacc2c10256f
    internal-label: Compare plans
  - id: e6c284e0-b6e6-4f82-bf96-e96bb5157b90
    internal-label: Plan insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%
---
# Visão geral dos planos

{{mm-mca-rebranding}}

Os planos no Marketing Campaign Analytics permitem alocar orçamentos por unidade de negócios e canal. A funcionalidade de planejamento está integrada aos resultados dos modelos treinados com base em seus dados harmonizados.

Um plano descreve os investimentos discricionários (por exemplo, orçamentos) que uma empresa pretende gastar em projetos relacionados a marketing durante um determinado período. Esses investimentos estão ao serviço de KPIs comuns (por exemplo, pedidos, receita). Os planos podem incluir despesas de canais como publicidade paga, conteúdo da Web patrocinado, eventos.

Um plano exige:

- um modelo,
- um intervalo de dados,
- um orçamento.

Um plano pode incluir, opcionalmente:

- uma janela de reconhecimento configurada,
- várias datas de voo com cada uma tendo um orçamento de target,
- restrições de orçamento mínimo e máximo por canal e data de voo.

Se um modelo usado para seu plano for pontuado em novos dados, será necessário criar um novo plano para considerar os dados recuperados.


## Criar planos

Para criar um plano, use o assistente de criação de plano do Marketing Campaign Analytics. Consulte [Planos de compilação](build.md) para obter mais detalhes.


## Gerenciar planos

Para exibir uma tabela de seus planos atuais, na interface do Marketing Campaign Analytics:

1. Selecione ![](/help/assets/icons2/FileChart.svg) **[!UICONTROL Plans]** no painel esquerdo.

1. Você verá uma tabela dos planos atuais e seus status.

   As colunas da tabela especificam detalhes sobre os planos.

   | Nome da coluna | Detalhes |
   |---|---|
   | **[!UICONTROL Name]** | Nome do plano |
   | **[!UICONTROL Model]** | O modelo usado como base para o plano. |
   | **[!UICONTROL Date range]** | O intervalo de datas completo de um plano. |
   | **[!UICONTROL Budget]** | O orçamento total de um plano. |
   | **[!UICONTROL Plan target]** | A métrica de destino definida para um plano baseado em destino. |
   | **[!UICONTROL Forecasted return]** | O [retorno previsto](/help/main-guide/glossary.md) para um plano |
   | **[!UICONTROL Forecasted ROI]** | O [ROI previsto](/help/main-guide/glossary.md) para um plano. |
   | **[!UICONTROL Forecasted conversion]** | A [conversão prevista](/help/main-guide/glossary.md) para um plano |
   | **[!UICONTROL Forecasted CPA]** | O [CPA previsto](/help/main-guide/glossary.md)para um plano |
   | **[!UICONTROL Status]** | O status de um plano:<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Failed]**,<br/>![StatusBlue](/help/assets/icons/StatusBlue.svg) **[!UICONTROL Processing]** ou<br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Complete]**. |

   Você pode usar ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) para selecionar ![Checkmark](/help/assets/icons/Checkmark.svg) as colunas a serem exibidas na tabela.

   Para classificar a tabela em qualquer coluna na ordem crescente de ![ArrowMoveUp](/help/assets/icons2/ArrowMoveUp.svg) ou decrescente de ![ArrowMoveDown](/help/assets/icons2/ArrowMoveDown.svg)selecione o título da coluna.

   Para classificar ou redimensionar a coluna **[!UICONTROL Name]**, **[!UICONTROL Model]** ou **[!UICONTROL Date range]**, selecione **[!UICONTROL Name]** ![DivisaInferior](/help/assets/icons/ChevronDown.svg), **[!UICONTROL Model]** ![DivisaInferior](/help/assets/icons/ChevronDown.svg) ou **[!UICONTROL Date range]** ![DivisaInferior](/help/assets/icons/ChevronDown.svg). No menu de contexto, selecione **[!UICONTROL Sort ascending]**, **[!UICONTROL Sort descending]** ou **[!UICONTROL Resize column]**. Como alternativa, você pode passar o mouse sobre o separador de colunas dessas colunas para redimensionar uma coluna.

1. Use a ![Pesquisa](/help/assets/icons/Search.svg) para pesquisar e filtrar a tabela para um ou mais planos específicos.

### Planejar insights

Para exibir os insights de um plano e editar um plano:

1. Selecione ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** no painel esquerdo.

1. Selecione o nome do plano.

Você foi redirecionado para [Planejar insights](insights.md).


### Duplicação de um plano

Para duplicar um plano:

- Selecione ![Mais](/help/assets/icons/More.svg) para um plano. No menu de contexto, selecione **[!UICONTROL Duplicate]**.
- Como alternativa, selecione um plano na tabela ![SelectBox](/help/assets/icons/SelectBox.svg) e selecione ![Copy](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]** na barra de ação azul.

Um novo plano, com um nome composto pelo nome do plano original anexado com **[!UICONTROL (Copy)] (_n_)**, foi criado. Você é redirecionado automaticamente para [Criação do plano](build.md) para fornecer detalhes atualizados para o plano copiado.

- Os detalhes (como Descrição, Orçamento e mais) do plano original são copiados.
- As restrições de orçamento do plano original são copiadas para o plano recém-criado.
- Você tem a opção de selecionar outro modelo como base para o plano copiado.
  - Para pontos de contato ou canais que existem no plano copiado, mas não existem no modelo recém-selecionado, todas as restrições para esses pontos de contato ou canais são removidas do plano.
  - Para pontos de contato ou canais que não existem no plano copiado, mas existem no modelo recém-selecionado, as restrições são definidas como:
    - um valor mínimo de `0`,
    - um valor máximo alinhado com o orçamento da faixa de voo do plano.



### Comparar planos

Para comparar planos:

1. Selecione dois planos na tabela.
1. Selecione ![Comparar](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]** na barra de ação azul. Você vê a interface do usuário **[!UICONTROL Compare plans]**.


### Excluir planos

Para deletar um plano:

1. Selecione ![Mais](/help/assets/icons/More.svg) para um plano. No menu de contexto, selecione **[!UICONTROL Delete]**. <br/>Como alternativa, selecione um plano na tabela ![SelectBox](/help/assets/icons/SelectBox.svg) e selecione ![Delete](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** da barra de ação azul.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete plan]** para excluir o plano. Selecione **[!UICONTROL Cancel]** para cancelar.

Para excluir vários planos:

1. Selecione vários planos.
1. Na barra de ações azul, selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** para excluir os planos.
1. Selecione **[!UICONTROL Delete]** na caixa de diálogo de confirmação **[!UICONTROL Delete *x *planos]**&#x200B;para excluir os planos. Selecione **[!UICONTROL Cancel]**&#x200B;para cancelar.


