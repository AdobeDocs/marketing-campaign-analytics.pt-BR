---
title: Modelos de treinamento e pontuação
description: Saiba como treinar e pontuar modelos.
feature: Models
exl-id: c4fbe13e-4548-421b-ba90-274fc42f4be2
autotag-review: '2026-05-01T09:03:34.273Z'
TQID: 'https://experienceleague.adobe.com/mvt9xE7FRLCEa9mD52LgW6bIJfHJMUd1cC4ipuebAhQ'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
  - id: d822825b-9821-40d5-9b0d-42a9e3f317c5
    internal-label: Plans
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
    internal-label: Datasets
  - id: f40f1683-8300-4054-aab8-77da06ad63ff
    internal-label: Models
subfeature_v2:
  - id: cb40363e-1205-4921-971c-9ee6bdb18329
    internal-label: Scoring data
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 2%
---
# Modelos de treinamento e pontuação

{{mm-mca-rebranding}}

Depois de [criar](/help/models/build.md) um modelo, ele é automaticamente treinado e classificado. Você pode treinar novamente ou pontuar um modelo manualmente.

## Treinamento

Considere treinar novamente um modelo quando quiser incluir novos dados de marketing incremental e de fatores. Por exemplo, durante o último trimestre, a dinâmica do mercado mudou ou sua distribuição de dados de marketing mudou significativamente.

Para treinar novamente um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Train]**. Como alternativa, selecione ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** na barra de ação azul.

   Na caixa de diálogo **[!UICONTROL Train model]**, selecione a opção para:

   * **[!UICONTROL Train model with last 2 years of marketing data]** ou
   * **[!UICONTROL Train model using specific date range of data]**.
     Especifique o intervalo de datas. Você pode usar o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de datas. Você deve selecionar um intervalo de dados com no mínimo um ano.

   ![Retreinar um modelo](../assets/retrain-model.png)

1. Selecione **[!UICONTROL Train]** para treinar novamente o modelo.


Você só poderá treinar novamente um modelo quando ele for treinado com êxito.


## Pontuação


Você pode pontuar incrementalmente um modelo com base em novos dados de marketing ou repontuar um modelo para um intervalo de datas específico.

Considere pontuar um modelo quando quiser:

* Corrija dados de marketing incorretos. Por exemplo, os dados de pesquisa paga recentes incluídos no treinamento e na pontuação do modelo perderam uma semana de dados.
* Use os novos dados de marketing incrementais que se tornaram disponíveis por meio de atualizações nos conjuntos de dados configurados como parte de seus dados harmonizados.

Para pontuar ou repontuar um modelo:

1. Selecione ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** no painel esquerdo.

1. Selecione ![Mais](/help/assets/icons/More.svg) para um modelo e, no menu de contexto, selecione **[!UICONTROL Score]**. Como alternativa, selecione ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** na barra de ação azul.

   Na caixa de diálogo **[!UICONTROL Score marketing data]**, selecione a opção para:

   * **[!UICONTROL Score new marketing data from *mm/dd/aaaa *]**, para pontuar seu modelo de forma incremental usando novos dados de marketing, ou
   * **[!UICONTROL Score specific date range of marketing data]** para pontuar para um intervalo de datas específico.
     Especifique o intervalo de datas. Você pode usar o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de datas.

   ![Pontuar novamente um modelo](../assets/rescore-model.png)

1. Selecione **[!UICONTROL Score]**. Ao restaurar um modelo usando um intervalo de dados específico, você verá uma caixa de diálogo **[!UICONTROL Existing model is replaced]**, solicitando a confirmação da substituição do modelo por novas pontuações para o intervalo de datas selecionado. Selecione **[!UICONTROL Replace model]** para confirmar.

>[!IMPORTANT]
>
>A pontuação de um modelo não altera nenhum plano já criado com base no modelo rescored. Para usar o novo modelo ressaltado em um plano, é necessário criar um novo plano.
