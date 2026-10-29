---
title: Criar planos
description: Saiba como criar planos no Marketing Campaign Analytics.
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
TQID: https://experienceleague.adobe.com/8p0uU5IAWbhwE9L0nVC-au5uyAh05jAJW47l0Jgucy4
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Mix Modeler
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
source-wordcount: '983'
ht-degree: 0%
---
# Criar planos

{{mm-mca-rebranding}}

No Marketing Campaign Analytics, crie um plano usando o assistente de plano. No assistente de plano, você pode configurar os detalhes e orçamentos ou as métricas de destino do seu plano e o modelo subjacente a ser usado para o seu plano. Depois de especificar detalhes, orçamento, métricas de direcionamento e modelo, você pode seguir com um plano recomendado por IA ou editar o gasto por canal. Você tem a opção de definir configurações avançadas na receita média por conversão e custos de canal.

Você precisa definir a meta em relação à qual deseja maximizar seu plano. Essa meta pode ser um orçamento que você pode gastar ou uma meta que deseja alcançar. Se a meta for um alvo, você também precisará especificar valores para a métrica de alvo a ser usada: conversão, receita, CPA ou ROI.

Para criar um plano, na interface ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** do Marketing Campaign Analytics, selecione **[!UICONTROL Create plan]**.


1. Na tela **[!UICONTROL Plan creation]**:

   1. Na seção **[!UICONTROL Setup]**:

      1. Digite um **[!UICONTROL Plan name]**, por exemplo `Goal based plan`. Digite um **[!UICONTROL Description]**, por exemplo `A goal based plan`.
      1. Selecione um **[!UICONTROL Model]** de **[!UICONTROL _Selecione uma opção.._.]**

         ![Configuração do Plano](/help/assets/plan-setup.png)

   1. Na seção **[!UICONTROL Goal]**, selecione a meta para a qual deseja otimizar seu plano. Você pode selecionar entre

      * **[!UICONTROL I have a budget to spend]**

        ![Planejar orçamento](../assets/plan-budget.png)

        Essa opção permite inserir orçamentos para um ou mais intervalos de datas.

        1. No container **[!UICONTROL Optimize]**:
           1. Selecione uma conversão no menu suspenso **[!UICONTROL Select conversion]**.
           1. Selecione um modelo no menu suspenso **[!UICONTROL Select model]**.
        1. Especifique um **[!UICONTROL Date range]**, digitando datas ou selecionando um intervalo de datas usando ![Calendário](/help/assets/icons/Calendar.svg).
        1. Insira um **[!UICONTROL Budget]**.
           Para adicionar intervalos de datas adicionais, cada um com seu orçamento, selecione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
           Para excluir um intervalo de datas e o orçamento associado, selecione ![Fechar](/help/assets/icons/Close.svg).
        1. Para definir um orçamento máximo opcional no qual você deseja restringir o plano:
           1. Ligar **[!UICONTROL Maximize budget]**.
           1. Especificar o valor do orçamento máximo. O valor deve ser igual ou superior ao valor total dos orçamentos especificados para os intervalos de datas.


      * **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

        ![Público alvo do plano](../assets/plan-target.png)

        1. No container **[!UICONTROL Optimize]**
           1. Selecione uma conversão no menu suspenso **[!UICONTROL Select conversion]**.
           1. Selecione uma métrica de destino no menu suspenso **[!UICONTROL Select target metric]**. Você pode selecionar entre **[!UICONTROL Conversion]**, **[!UICONTROL CPA]**, **[!UICONTROL Revenue]** ou **[!UICONTROL ROI]**.
           1. Selecione um modelo no menu suspenso **[!UICONTROL Select model]**.
        1. Especifique um Intervalo de datas, digitando datas ou selecionando um intervalo de datas usando ![Calendário](/help/assets/icons/Calendar.svg).
        1. Insira um valor para a métrica de destino selecionada. Por exemplo, um número para **[!UICONTROL Total Conversions]**, uma porcentagem para **[!UICONTROL Paid Marketing ROI]** ou valores de moeda para **[!UICONTROL Paid Marketing CPA]** e **[!UICONTROL Total Revenue]**.
           Para adicionar intervalos de datas adicionais, cada um com sua métrica de destino, selecione ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.
           Para excluir um intervalo de datas e uma métrica de destino associada, selecione ![Fechar](/help/assets/icons/Close.svg).
        1. Para definir um orçamento máximo opcional no qual você deseja restringir o plano:
           1. Ligar **[!UICONTROL Maximize budget]**.
           1. Especificar o valor do orçamento máximo.


   1. Selecione **[!UICONTROL Next]**.

1. No diálogo **[!UICONTROL Done with all required fields]**:

   ![Plano concluído](/help/assets/plan-done-required-fields.png)

   * Selecione ![NovoPlano](/help/assets/icons/NewPlan.svg) **[!UICONTROL Create plan now]** se quiser gerar um plano recomendado de IA com ROI previsto. Selecione **[!UICONTROL OK]**. Seu plano foi criado.





   * Selecione ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** se desejar editar o orçamento do canal e definir configurações avançadas antes de criar um plano com ROI previsto.  Selecione **[!UICONTROL OK]** para definir os gastos do canal em **[!UICONTROL Spend selection]** na próxima etapa.


     >[!IMPORTANT]
     >
     >As informações abaixo só serão relevantes se você tiver selecionado a ![TableEdit](/help/assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]**


1. Na seção **[!UICONTROL Spend selection]**, para cada intervalo de datas do orçamento, use a ![Divisa](/help/assets/icons/ChevronRight.svg) para abrir a exibição de distribuição de canal para esse intervalo de dados.

   Você pode usar dados de referência históricos se quiser usar dados e insights passados de gastos com marketing. Considerar dados históricos de referência para:

   * Melhore a alocação de orçamento destacando canais de alto desempenho e canais de baixo desempenho.
   * Suporte para análise de tendências.
   * Identifique estratégias eficazes e evite erros ao configurar planos.

   Se você selecionar um período de referência histórico, será possível alinhar-se às preferências de padrão de gasto anteriores e a funcionalidade de planejamento do Marketing Campaign Analytics poderá gerar planos que estejam dentro de suas expectativas. Esses planos devem, em última análise, aumentar a confiança das partes interessadas, garantir que os planos de marketing sejam estratégicos e eficientes e que estejam baseados em dados de desempenho comprovados e nas necessidades comerciais.

   ![Gastar seleção](/help/assets/plan-spend-selection.png)

   1. Selecione o **[!UICONTROL Spend pattern]**.

      * A opção padrão é **[!UICONTROL Automatic]**.
      * Selecione **[!UICONTROL Historical reference]** e insira um **[!UICONTROL Start date]** para fazer referência a dados de gastos com marketing anteriores já disponíveis para o Marketing Campaign Analytics. O **[!UICONTROL End date]** é determinado automaticamente com base no intervalo de datas para o qual você define o padrão de gastos. A data de início proposta é a primeira data disponível após a data de gasto de marketing. Para indicar que você selecionou um período de referência histórica inválido ou não existente, você vê um ![AlertRed](/help/assets/icons/AlertRed.svg).

   1. Para definir orçamentos para cada canal, insira um valor para **[!UICONTROL Min]** e **[!UICONTROL Max]** ou use os controles deslizantes.

   1. Para alternar entre entrada de moeda ou porcentagem, selecione **[!UICONTROL $]** ou **[!UICONTROL %]** para **[!UICONTROL View spend by]**. Essa alternância será desativada se você tiver selecionado métricas de destino que não são baseadas em moeda.

   1. Quando terminar, selecione **[!UICONTROL Create]**.
      ![Gastar seleção](/help/assets/plan-spend-selection.png)

   1. Selecione **[!UICONTROL Next]**.



1. Na seção **[!UICONTROL Advanced configurations]**, você pode inserir configurações avançadas opcionais.

   ![Resumo do plano](../assets/plan-advanced-configurations.png)

   * O nome do plano, o modelo, a faixa de datas e o orçamento total são resumidos.

   * Por padrão, o Marketing Campaign Analytics calcula automaticamente a receita média por conversão usando os dados sazonais históricos mais recentes. Em **[!UICONTROL Average Revenue per conversion]** você pode definir uma receita média específica por conversão.

     1. Para cada faixa de datas no orçamento:

        1. Selecione um intervalo de datas no menu suspenso **[!UICONTROL Date range]**.
        1. Insira um valor de **[!UICONTROL Average revenue]**.

     1. Selecione ![AddCircle](/help/assets/icons/AddCircle.svg). Adicione uma receita média personalizada por unidade de conversão para adicionar um intervalo de datas.
     1. Selecione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) para remover um intervalo de datas.

     >[!NOTE]
     >
     >Se o seu modelo não incluir dados históricos de receita, você deverá definir uma receita média por conversão para cada faixa de datas especificada para o seu orçamento.
     >

   * Por padrão, o Marketing Campaign Analytics calcula automaticamente os custos do canal usando os dados sazonais históricos mais recentes. Em **[!UICONTROL Channel costs]** você pode definir custos de canal personalizados.

     1. Para cada canal no modelo, defina um custo de canal personalizado.

        1. Selecione um canal no menu suspenso **[!UICONTROL Channel]**.
        1. Para cada faixa de datas no orçamento:
           1. Selecione um intervalo de datas no menu suspenso **[!UICONTROL Date range]**.
           1. Insira um valor de **[!UICONTROL Average revenue]**.
        1. Selecione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** para adicionar um intervalo de datas.
        1. Selecione ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) para remover um intervalo de datas.

     1. Selecione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** para adicionar um canal.
     1. Selecione ![CrossSize400](/help/assets/icons/CrossSize400.svg) para remover um canal personalizado.


1. Quando terminar, selecione **[!UICONTROL Create]**.

1. Na caixa de diálogo **[!UICONTROL Create plan]**, selecione **[!UICONTROL Create plan]** para criar seu plano. Selecione **[!UICONTROL Cancel]** para cancelar a criação do seu plano. Uma caixa de diálogo **[!UICONTROL No work is saved]** é exibida para confirmar.

