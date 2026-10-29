---
title: Conversões
description: Saiba como criar conversões para usar como parte da harmonização de seus dados no Marketing Campaign Analytics.
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
autotag-review: '2026-05-01T09:15:50.061Z'
TQID: 'https://experienceleague.adobe.com/5m8Z9cc9d42019sNXkstXDn6cOo-2yzzQWCw0VG1YrY'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
subfeature_v2:
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 9%
---
# Conversões {#conversions}

{{mm-mca-rebranding}}

{{mm-mca-rebranding}}

>[!CONTEXTUALHELP]
>id="harmonizeddata_conversions_create"
>title="Conversão"
>abstract="Os eventos de conversão são objetivos de negócios que identificam o impacto das atividades de marketing. Exemplos: pedidos de comércio eletrônico, compras em loja e visitas ao site, e muito mais."


Os eventos de conversão são objetivos de negócios que identificam o impacto das atividades de marketing. Exemplos: pedidos de comércio eletrônico, compras na loja, visitas a sites e assim por diante.

Você define conversões de marketing para análise de atribuição.

## Gerenciar conversões

Para ver uma tabela das conversões disponíveis, na interface do Marketing Campaign Analytics:

1. Selecione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** no painel esquerdo.

1. Selecione **[!UICONTROL Conversions]** na barra superior. Você verá uma tabela das conversões.

As colunas da tabela especificam detalhes sobre a conversão:

| Nome da coluna | Detalhes |
| --- | ---|
| Nome | O nome da conversão. |
| Receita | A métrica de dados harmonizada a ser usada para calcular a receita de uma conversão. |
| Métrica de conversão | A métrica de dados harmonizada a ser usada como a métrica de conversão para análise. Isso indica o resultado numérico principal do negócio, como: pedidos, receita, número de assinaturas e muito mais. |
| Categoria | A regra de conversão a ser aplicada, em que uma dimensão de conversão é usada para classificar o tipo de conversão. |
| Criado | Data e hora de criação da conversão. |
| Última modificação | Data e hora da última modificação da conversão. |


## Adicionar uma conversão

Para adicionar uma conversão, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** no Marketing Campaign Analytics:

1. Selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. No diálogo **[!UICONTROL Create conversion]**:

   1. Digite um nome para **[!UICONTROL Conversion]**, por exemplo `Store Conversions`.

   1. Defina o **[!UICONTROL Conversion category]**.

      1. Selecione um valor de **[!UICONTROL *Selecionar harmonizar...*]**, por exemplo `Conversion types`.

      1. Selecione um valor para o operador ![Divisa](/help/assets/icons/ChevronDown.svg), por exemplo **[!UICONTROL is]**.

      1. Selecione um valor em **[!UICONTROL *Selecione o valor *]**ou insira um valor, por exemplo **[!UICONTROL Store]**.

   1. Selecione um campo harmonizado de **[!UICONTROL Conversion metric for analysis]**, por exemplo **[!UICONTROL Orders]**.

   1. Selecione um campo harmonizado de **[!UICONTROL Revenue field]**, por exemplo **[!UICONTROL Gross Demand]**.

   1. Para criar a conversão, selecione **[!UICONTROL Create]**. Para cancelar a criação de uma conversão, selecione **[!UICONTROL Cancel]**.

      ![Texto alternativo](/help/assets/create-conversion.png)

1. Quando criada, a conversão é adicionada à tabela de conversões.


## Exibir detalhes

Para exibir detalhes de uma conversão:

1. Selecione ![Mais](/help/assets/icons/More.svg) ao passar o mouse sobre um nome de conversão na tabela.

1. Selecione ![Exibir](/help/assets/icons/ViewDetail.svg) **Exibir detalhes**. Uma caixa de diálogo mostra detalhes da conversão. Consulte [Adicionar uma conversão](#add-a-conversion) para obter mais informações. Selecione **[!UICONTROL Cancel]** para fechar a caixa de diálogo.

## Exibir relatório

Para exibir um relatório de uma conversão:

1. Selecione ![Mais](/help/assets/icons/More.svg) ao passar o mouse sobre um nome de conversão na tabela.

1. Selecione ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Exibir relatório**. Uma caixa de diálogo mostra um relatório da conversão.

   ![Relatório de exibição de conversão](../assets/conversion-view-report.png)

   * Para alterar a granularidade sobre a qual relatar, selecione um valor no menu suspenso **[!UICONTROL Weekly]**.
   * Para alterar o período para o relatório, insira uma data de início e término ou use o ![Calendário](/help/assets/icons/Calendar.svg) para definir um período no pop-up do calendário.

1. Selecione **[!UICONTROL Close]** para fechar a caixa de diálogo.

## Excluir uma conversão

Para excluir uma conversão:

1. Selecione ![Excluir](/help/assets/icons/Delete.svg) **Excluir** ao passar o mouse sobre um nome de conversão na tabela.
1. Na caixa de diálogo de confirmação **[!UICONTROL Delete conversion]**, selecione **[!UICONTROL Delete]** para excluir permanentemente a conversão.
