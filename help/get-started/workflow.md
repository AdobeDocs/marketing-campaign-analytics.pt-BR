---
title: Fluxo de trabalho do Marketing Campaign Analytics
description: Entenda o fluxo de trabalho típico do Marketing Campaign Analytics.
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
autotag-review: '2026-05-01T09:15:33.908Z'
TQID: 'https://experienceleague.adobe.com/aOlJN-eYN6Cl-qohzpJbleuQeJFxx3cdxWknVUbmn5I'
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
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
    internal-label: Schemas
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
    internal-label: Aggregate datasets
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
    internal-label: Event datasets
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
    internal-label: Ingest data
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
    internal-label: Summary datasets
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
    internal-label: Conversions
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
    internal-label: Dataset mapping
  - id: ba4fd72c-282e-4fb6-abc1-08e6fb87b2ad
    internal-label: Dataset rules
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
    internal-label: Harmonized fields
  - id: b2d4aeb9-eabe-49f6-8edb-bb2862d5980b
    internal-label: Marketing touchpoints
  - id: c89e26b6-808d-4500-8b01-450a63466999
    internal-label: Build model
  - id: a9505d76-24a1-4ffe-bd01-6ac32d5af453
    internal-label: Model insights
  - id: cb40363e-1205-4921-971c-9ee6bdb18329
    internal-label: Scoring data
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
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 1%
---
# Fluxo de trabalho do Marketing Campaign Analytics

Veja este vídeo para obter uma introdução ao fluxo de trabalho do usuário no Marketing Campaign Analytics.

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Um fluxo de trabalho típico no Marketing Campaign Analytics consiste nas seguintes atividades:

![Texto alternativo](/help/assets/ApplicationWorkflow.svg)

|  | Atividade | Descrição |
|---|---|---|
| ![Dados](/help/assets/icons/Data.svg){width="100"} | [**Assimilar dados**](../ingest-data/overview.md) | Assimilar dados de eventos do Experience Platform (por exemplo, Adobe Analytics, Web SDK, outras fontes), dados agregados de canais de marketing (por exemplo, TV, jardins murados, email, atividades próprias e operadas), dados de fatores externos de clientes (por exemplo, alterações de preço no serviço de assinatura) e dados de fatores internos (por exemplo, planos de feriados). |
| ![VerificaçãoDeDados](/help/assets/icons/DataCheck.svg){width="100"} | [**Harmonizar dados**](../harmonize-data/overview.md) | Configure regras de mapeamento e regras de resolução de conflitos para unir os vários conjuntos de dados de marketing necessários para medir e planejar o desempenho da campanha no Marketing Campaign Analytics. |
| ![ConfigArquivo](/help/assets/icons/FileGear.svg){width="100"} | [**Criar modelos**](../models/overview.md) | Crie instâncias de modelo com pontos de contato de marketing (por exemplo, canais), definições de conversão e fatores internos e externos. |
| ![DadosDoArquivo](/help/assets/icons/FileData.svg){width="100"} | [**Treinar e pontuar modelos**](../models/overview.md) | Crie pontuações agregadas e em nível de evento usando treinamento e pontuação de aprendizado de máquina do. |
| ![GráficoDeArquivos](/help/assets/icons/FileChart.svg){width="100"} | [**Criar planos**](../plans/overview.md) | Criar e construir planos. Determine a melhor alocação de fundos de marketing para atingir um objetivo comercial usando a saída dos modelos da Marketing Campaign Analytics. |
| ![Painel](/help/assets/icons/Dashboard.svg){width="100"} | [**Painel de visão geral**](../dashboard/overview.md) | Obtenha insights sobre dados, modelos e planos harmonizados usando várias visualizações configuráveis. |

{style="table-layout:auto"}

Uma visão geral de como os dados de entrada podem fluir para o Marketing Campaign Analytics e como o Marketing Campaign Analytics pode produzir dados de saída para sua própria interface, mas também para outras soluções, como o Customer Journey Analytics, é ilustrada abaixo.

![Fluxo de dados de saída de entrada do Marketing Campaign Analytics](../assets/mm-input-output.png)

<!--
The detailed data-oriented flowchart below illustrates how:

* harmonized data is based on:

  * experience event data (originating from Analytics source connector, collected through Experience Platform SDKs and APIs, ingested through source connectors, or using streaming ingestion),
  * aggregate or summary data from walled gardens (like Facebook, YouTube), traffic sources, or offline advertising data, and 
  * definitions of harmonized fields and dataset rules.

* a model is based on:

  * the conversion and marketing touchpoint definitions resulting from the harmonized data and 
  * non-marketing aggregate or summary data containing internal or external factors.

* mult-touch attribution event scores can potentially be fed back into Experience Platform data lake for use in subsequent model configuration, training and scoring.

![Comprehensive workflow](/help/assets/comprehensive-workflow.svg)
-->
