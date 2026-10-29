---
title: Visão geral dos dados de assimilação
description: Saiba como assimilar dados na Marketing Campaign Analytics.
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
autotag-review: '2026-05-01T09:11:34.506Z'
TQID: 'https://experienceleague.adobe.com/bCjm1mvGkSSpD6oke4baWwZftqjyjv4u-1sBDtOYsJY'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
    internal-label: Datasets
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
    internal-label: Schemas
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
    internal-label: Aggregate datasets
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
    internal-label: Summary datasets
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
    internal-label: Ingest data
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
    internal-label: Event datasets
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 17%
---
# Visão geral dos dados de assimilação

{{mm-mca-rebranding}}

O Marketing Campaign Analytics funciona com dados de nível de evento, dados de esforço de marketing agregados ou resumidos de vários jardins murados. E com dados agregados ou resumidos de qualquer outra fonte, como publicidade offline, fatores internos ou fatores externos.

Os clientes podem usar qualquer tipo de dados assimilados na Experience Platform como conjuntos de dados e que se baseie em esquemas que usam o XDM ExperienceEvent ou as Métricas de resumo XDM como a classe base.

Por exemplo:

* Dados coletados usando o conector de origem do Adobe Analytics. E transformados em conjuntos de dados em conformidade com a versão padrão ou personalizada do esquema do Adobe Analytics.
* Dados coletados usando o Experience Platform Web SDK, Mobile SDK ou a API do Edge Network Server para coletar interações do cliente na Web, em dispositivos móveis ou em qualquer outro tipo de dispositivo.
* Dados agregados ou resumidos de jardins murados (como Facebook, YouTube), fontes de tráfego ou dados de publicidade offline.
* Dados agregados ou resumidos não relacionados à comercialização que contêm fatores internos ou externos úteis para a criação de modelos.

Você pode usar qualquer tipo de mecanismo, compatível com o Experience Platform, para assimilar o nível do evento da experiência, agregar dados de esforço de marketing e dados de outras fontes. Como os SDKs do Experience Platform, APIs, conectores de origem, assimilação em lote e por transmissão. Para saber mais sobre como assimilar seus dados no Experience Platform para uso no Adobe Marketing Campaign Analytics, consulte a [visão geral da Assimilação de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ingestion/home).

## Diretrizes

Para assimilar dados na Experience Platform para uso com o Marketing Campaign Analytics, siga estas diretrizes:

* Não deve haver qualquer sobreposição nos dados incrementais adicionados aos conjuntos de dados.
* Todos os dados de uma única fonte devem ter a mesma granularidade.
* Data e granularidade são campos obrigatórios no esquema subjacente para todos os dados agregados assimilados como conjuntos de dados
* Canal é um campo obrigatório no esquema subjacente para todos os esforços de marketing/dados de gastos assimilados como conjuntos de dados.


## Exemplos

Encontre abaixo alguns exemplos de dados normalmente usados no Marketing Campaign Analytics, além dos dados do evento de experiência mais padrão.

+++ Dados agregados do esforço de marketing

| Geografia | Data | Tipo de data | Canal | Campaign | Click | Ganho | Engajamento | impressão | Abertura | Próprio | Enviado | Gastos |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 2021-10-31 | dia | EMAIL | | 12752 | | | | | | 1132945 | |
| AMER | 2021-10-31 | dia | FB | | 148844 | | | | | | | 42111 |
| AMER | 2021-10-31 | dia | YT | | | | 2314452 | | | | | 10540 |
| JPN | 2021-10-21 | dia | EMAIL | | 21089 | | | | | | 3283626 | |
| JPN | 2021-10-21 | dia | SOCIAL | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ Dados de conversão agregados

| Geografia | Data | Tipo de data | Produto | Unidades Vendidas | Receita |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | dia | Economia do criador | 603 | 36537.68 |
| EMEA | 2021-09-13 | dia | Metaverso | 55 | 21704.37 |
| JPN | 2022-05-30 | dia | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | dia | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ Dados de fatores externos

| Dados | Tipo de data | Fator | Valor |
|---|:---:|:---:|:---|
| 2020-08-02 | semana | SPX | 3325.866 |
| 2020-08-09 | semana | SPX | 3364.158 |
| 2020-08-16 | semana | SPX | 3385.858 |
| 2020-08-23 | semana | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Para trabalhar com dados na Marketing Campaign Analytics, você precisa dos dados coletados nos conjuntos de dados e modelados de acordo com os esquemas na Experience Platform. A interface do Marketing Campaign Analytics fornece acesso fácil à interface do usuário de Esquemas e Conjuntos de dados do Experience Platform.


## Validar

Para validar se os dados estão disponíveis corretamente no Marketing Campaign Analytics, você pode fazer o seguinte:

* Use visualizações na [Visão geral](/help/overview.md).
* Baixe e inspecione dados de [Dados harmonizados](/help/harmonize-data/overview.md) em conjuntos de dados harmonizados.

Para validar se seus dados foram assimilados corretamente no Experience Platform, você pode [gravar e executar consultas SQL usando o Serviço de Consulta do Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/query/home).


>[!MORELIKETHIS]
>
>Consulte para obter mais detalhes sobre como gerenciar esquemas e conjuntos de dados:
>
>* [Esquemas](schemas.md)
>* [Conjuntos de dados](datasets.md)
