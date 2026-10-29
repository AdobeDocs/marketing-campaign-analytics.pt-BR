---
title: Pontos de contato de marketing
description: Saiba como criar pontos de contato de marketing para usar como parte da harmonização de seus dados no Marketing Campaign Analytics.
feature: Harmonized Data, Marketing Touch Points
exl-id: 42851107-7568-4bc9-92ca-3cba713a522e
autotag-review: '2026-05-01T09:13:36.558Z'
TQID: 'https://experienceleague.adobe.com/C6T9Ga2PICq3GBgEtsnZsB8C9xiO7hZXsdHfv7TqkLE'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
subfeature_v2:
  - id: b2d4aeb9-eabe-49f6-8edb-bb2862d5980b
    internal-label: Marketing touchpoints
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 12%
---
# Pontos de contato de marketing {#marketing-touchpoints}

{{mm-mca-rebranding}}

>[!CONTEXTUALHELP]
>id="harmonizeddata_marketingtouchpoints_create"
>title="Pontos de contato de marketing"
>abstract="Pontos de contato de marketing são eventos de marketing a nível de destinatário, pessoa e/ou cookie usados para avaliar o impacto dos investimentos em marketing nas conversões numéricas ou baseadas em receita."


Pontos de contato de marketing são eventos de marketing a nível de destinatário, pessoa e/ou cookie usados para avaliar o impacto dos investimentos em marketing nas conversões numéricas ou baseadas em receita.

Você define pontos de contato de marketing para ajudá-lo na análise de atribuição.

## Gerenciar pontos de contato de marketing

Para ver uma tabela dos pontos de contato de marketing disponíveis na interface do Marketing Campaign Analytics:

1. Selecione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** no painel esquerdo.

1. Selecione **[!UICONTROL Marketing touchpoint]** na barra superior. Você verá uma tabela dos pontos de contato de marketing. Se mais páginas estiverem disponíveis, use a ![Seta para a esquerda](/help/assets/icons/ChevronLeft.svg) ou a ![Seta para a direita](/help/assets/icons/ChevronRight.svg) em **[!UICONTROL Page _x _de_x_]** para se mover entre as páginas da tabela.

As colunas da tabela especificam detalhes sobre o ponto de contato de marketing:

| Nome da coluna | Detalhes |
| --- | ---|
| Nome | O nome do ponto de contato de marketing. |
| Métrica de gasto | A métrica de dados harmonizada a ser usada para calcular o gasto com pontos de contato. |
| Métrica de volume | A métrica de dados harmonizada a ser usada para calcular o volume de pontos de contato. |
| Regra | A regra de ponto de contato a ser usada. |
| Criado | Data e hora de criação do ponto de contato de marketing. |
| Última modificação | Data e hora da última modificação do ponto de contato de marketing. |


## Adicionar um ponto de contato de marketing

Para adicionar um ponto de contato de marketing, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Marketing touchpoint]** no Marketing Campaign Analytics:

1. Selecione ![Adicionar](/help/assets/icons/AddCircle.svg) Adicionar ponto de contato de marketing.

1. Na caixa de diálogo **[!UICONTROL Marketing touchpoint]**

   1. Digite um nome para **[!UICONTROL Touchpoint Name]**, por exemplo `Luma Touchpoint`.

   1. Defina um **[!UICONTROL Touchpoint rule]**.

      1. Selecione um valor de **[!UICONTROL *Selecione harmonizado *]**, por exemplo **[!UICONTROL Brand]**.

      1. Selecione um valor para o operador ![Divisa](/help/assets/icons/ChevronDown.svg), por exemplo **[!UICONTROL is]**.

      1. Selecione um valor em **[!UICONTROL *Selecione o valor *]**&#x200B;ou insira um valor, por exemplo **[!DNL Luma]**.

   1. Selecione um campo harmonizado de **[!UICONTROL Touchpoint volume]**, por exemplo **[!UICONTROL Impressions]**.

   1. Selecione um campo harmonizado de **[!UICONTROL Touchpoint spend]**, por exemplo **[!UICONTROL Cost]**.

      ![Ponto de contato de marketing](/help/assets/create-touchpoint.png)

   1. Para criar o ponto de contato de marketing, selecione **[!UICONTROL Create]**. Para cancelar a criação de um ponto de contato de marketing, selecione **[!UICONTROL Cancel]** .

1. Quando criado, o ponto de contato é adicionado à tabela de pontos de contato de marketing.


## Exibir detalhes

Para exibir detalhes de um ponto de contato de marketing:

1. Selecione ![Mais](/help/assets/icons/More.svg) ao passar o mouse sobre um nome de ponto de contato de marketing na tabela.

1. Selecione ![Exibir](/help/assets/icons/ViewDetail.svg) **Exibir**. Uma caixa de diálogo mostra detalhes do ponto de contato de marketing. Consulte [Adicionar um ponto de contato de marketing](#add-a-marketing-touchpoint) para obter mais informações. Selecione **[!UICONTROL Cancel]** para fechar a caixa de diálogo.


## Exibir relatório

Para exibir um relatório de um ponto de contato de marketing:

1. Selecione ![Mais](/help/assets/icons/More.svg) ao passar o mouse sobre um nome de ponto de contato de marketing na tabela.

1. Selecione ![GraphTrend](/help/assets/icons/GraphTrend.svg) **Exibir relatório**. Uma caixa de diálogo mostra um relatório do ponto de contato de marketing.

   ![Relatório de exibição do ponto de contato de marketing](../assets/marketingtouchpoint-view-report.png)

   * Para alterar a granularidade sobre a qual relatar, selecione um valor no menu suspenso **[!UICONTROL Weekly]**.
   * Para alterar o período para o relatório, insira uma data de início e término ou use o ![Calendário](/help/assets/icons/Calendar.svg) para definir um período no pop-up do calendário.

1. Selecione **[!UICONTROL Close]** para fechar a caixa de diálogo.

## Excluir um ponto de contato de marketing

Para excluir um ponto de contato de marketing:

1. Selecione ![Excluir](/help/assets/icons/Delete.svg) **Excluir** ao passar o mouse sobre um nome de ponto de contato de marketing na tabela.
1. Na caixa de diálogo de confirmação **[!UICONTROL Delete touchpoint]**, selecione **[!UICONTROL Delete]** para excluir permanentemente o ponto de contato de marketing.

