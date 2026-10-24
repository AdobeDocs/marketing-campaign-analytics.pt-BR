---
title: Harmonizar visão geral dos conjuntos de dados
description: Saiba como harmonizar dados no Mix Modeler.
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
TQID: https://experienceleague.adobe.com/9ki9Q-ZAmwmiyYFt-EAaa1ybylaoMauTvoxQ9ux1IEI
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Mix Modeler
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
subfeature_v2:
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
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
    internal-label: Data quality
autotag-review: '2026-05-01T09:10:10.340Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 17%
---
# Harmonizar visão geral dos conjuntos de dados

Os dados no Mix Modeler são de natureza diferente, dependendo da fonte de dados. Os dados podem ser:

* dados agregados ou resumidos, por exemplo, coletados de fontes de dados muradas ou dados de publicidade offline coletados (como gastos) da execução de uma campanha em outdoor, um evento ou uma campanha de publicidade física,
* dados do evento, por exemplo, de fontes de dados primárias. Esses dados de evento podem ser coletados por meio do conector de origem do Adobe Analytics na Adobe Analytics, ou por meio da API do Experience Platform Web, Mobile SDK ou Edge Network, ou por meio de dados assimilados usando conectores de origem.

O serviço de harmonização do Mix Modeler assimila os dados agregados e do evento em uma visualização de dados consistente. Essa visualização de dados é a fonte para os modelos no Mix Modeler. O serviço usa a maior granularidade entre os diferentes conjuntos de dados. Por exemplo, se um conjunto de dados tiver uma granularidade de dados mensais e os conjuntos de dados restantes tiverem granularidade semanal e diária, o serviço de harmonização criará uma visualização de dados usando granularidade mensal.

## Fatores

Os fatores são fundamentais para a criação de modelos e você deseja entender o que afeta os negócios de forma holística. Os fatores podem não estar relacionados aos dados de marketing.

* Fatores internos são específicos para sua organização e podem afetar suas conversões. Por exemplo, sua temporada de vendas, promoções e muito mais.

* Fatores externos são fatores fora do controle de sua organização, mas que ainda podem afetar as conversões realizadas. Exemplos são CPI, S&amp;P 500 e outros.

A funcionalidade Fatores no Mix Modeler usa um fluxo de trabalho de fatores harmonizado. Esse fluxo de trabalho simplifica o modo como os fatores são gerenciados, oferece consistência entre modelos e fornece uma experiência intuitiva.

Como parte do workflow de fatores harmonizados:

1. Defina campos harmonizados para fatores de um conjunto de dados de fator em [regras do conjunto de dados](/help/harmonize-data/dataset-rules.md#create-a-dataset-rule).
1. [Sincronizar](/help/harmonize-data/dataset-rules.md#sync-data) seus dados harmonizados.
1. [Use os fatores](/help/models/build.md#configure) na sua configuração de modelo.

### Migração

Você pode ter modelos que ainda não adotaram o fluxo de trabalho de fatores harmonizados e usar o fluxo de trabalho de fatores baseado no conjunto de dados do Experience Platform. Esses modelos continuam a exibir seus fatores baseados no conjunto de dados original até que os modelos sejam atualizados com novos fatores que são baseados no fluxo de trabalho de fatores harmonizados.

Ao duplicar um modelo que usa o fluxo de trabalho de fatores baseados no conjunto de dados:

* Se o modelo não tiver sido harmonizado, a antiga configuração do fator não será transferida para o modelo duplicado. É necessário adicionar fatores usando o novo workflow de fatores harmonizados.
* Se o modelo tiver sido harmonizado, os fatores transitam e são retidos ou atualizados.

## Um exemplo de dados harmonizados

Imagine que você tenha os seguintes conjuntos de dados disponíveis para o Mix Modeler.

**Conjunto de dados 1**

Contém o conjunto de dados de esforço de marketing da YouTube, com uma granularidade do conjunto de dados agregado para diariamente.

| Data | Tipo de data | Canal | Campaign | Marca | Geografia | Cliques | Gastos |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | dia | YouTube | Y_Fall_02 | BrandX | EUA | 10000 | 100 |
| 01-01-2022 | dia | YouTube | Y_Fall_02 | BrandX | EUA | 1000 | 10 |
| 01-03-2022 | dia | YouTube | Y_Fall_01 | MarcaY | CA | 10000 | 100 |
| 01-04-2022 | dia | YouTube | Y_Summer_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**Conjunto de dados 2**

Contém o conjunto de dados de esforço de marketing do Facebook, com uma granularidade do conjunto de dados agregado para semanal.

| Data | Tipo de data | Canal | Campaign | Geografia | Cliques | Gastos |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | semana | Facebook | FB_Fall_01 | EUA | 8000 | 100 |
| 01-08-2022 | semana | Facebook | FB_Fall_02 | EUA | 1000 | 10 |
| 01-08-2022 | semana | Facebook | FB_Fall_01 | EUA | 7000 | 100 |
| 01-16-2022 | semana | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**Conjunto de dados 3**

Um conjunto de dados de conversão, com uma granularidade do conjunto de dados agregado para diariamente.

| Data | Tipo de data | Geografia | Meta | Receita |
|--- |:---: |---|---|---:|
| 01-01-2022 | dia | EUA | Moda | 200 |
| 01-08-2022 | dia | EUA | Moda | 10 |
| 01-08-2022 | dia | EUA | Joias | 1100 |
| 01-16-2022 | dia | CA | Joias | 80 |

{style="table-layout:auto"}


**Conjunto de dados 4**

Um exemplo de conjunto de dados de evento de experiência (eventos do Web SDK) do cliente.

| Carimbo de data e hora | Namespace de identidade | Identificação de identidade | Canal | Cliques |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


Você deseja criar um conjunto de dados harmonizado, com uma granularidade definida como semanal. Os dados do evento são agregados à granularidade da semana e adicionados ao conjunto de dados harmonizado. O resultado é:

**Conjunto de dados harmonizado**

| Data | Tipo de data | Canal | Campaign | Marca | Geografia | Meta | Cliques | Gastos | Receita |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | semana | YouTube | Y_Fall_02 | BrandX | EUA | Null | 11000 | 110 | Null |
| 01-03-2022 | semana | YouTube | Y_Fall_01 | MarcaY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | semana | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | semana | Facebook | FB_Fall_01 | Null | EUA | Null | 8000 | 100 | Null |
| 01-08-2022 | semana | Facebook | FB_Fall_02 | Null | EUA | Null | 1000 | 10 | Null |
| 01-08-2022 | semana | Facebook | FB_Fall_01 | Null | EUA | Null | 7000 | 100 | Null |
| 01-16-2022 | semana | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | semana | Null | Null | Null | EUA | Moda | Null | Null | 200 |
| 01-03-2022 | semana | Null | Null | Null | EUA | Moda | Null | Null | 10 |
| 01-03-2022 | semana | Null | Null | Null | EUA | Joias | Null | Null | 1100 |
| 01-10-2022 | semana | Null | Null | Null | CA | Joias | Null | Null | 80 |
| 01-01-2022 | semana | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | semana | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## Configurar dados harmonizados

Para criar um conjunto de dados harmonizado, como no [exemplo](#an-example-of-harmonized-data) simplificado, siga estas etapas:

1. Defina [campos harmonizados](fields.md) adicionais que você deseja usar além dos campos harmonizados globais já disponíveis.
1. Configure [regras do conjunto de dados](dataset-rules.md) para mapear campos do conjunto de dados agregado (fator ou resumo) ou da experiência para campos harmonizados.
1. Defina [pontos de contato de marketing](marketing-touchpoints.md) usando os campos harmonizados padrão e adicionais que você definiu.
1. Defina [conversões](conversions.md) usando os campos harmonizados padrão e adicionais que você definiu.


## Exibir dados harmonizados

Para ver seus dados harmonizados, na interface do Mix Modeler:

1. Selecione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** no painel esquerdo.

1. Selecione **[!UICONTROL Harmonized data]** na barra superior. Um resumo de seus dados harmonizados é mostrado com base nos campos, nas regras do conjunto de dados, nos pontos de contato de marketing e nas conversões definidos.

   1. Para redefinir o período no qual se baseia a recapitulação de dados harmonizados, insira um intervalo de datas para **[!UICONTROL Date range]** ou use o ![Calendário](/help/assets/icons/Calendar.svg) para selecionar um intervalo de dados.

   1. Para modificar as colunas de campo harmonizado exibidas para a tabela de dados Harmonizada, use ![Configurações](/help/assets/icons/Setting.svg) para abrir a caixa de diálogo **[!UICONTROL Column settings]**.

      1. Selecione ![SelectBox](/help/assets/icons/SelectBox.svg) uma ou mais colunas de **[!UICONTROL AVAILABLE COLUMNS]** e use ![Divisa direita](/help/assets/icons/ChevronRight.svg) para adicionar essas colunas a **[!UICONTROL SELECTED COLUMNS]**. Todos os campos harmonizados padrão que você definiu (incluindo campos relacionados a conjuntos de dados de fator, como **[!UICONTROL Factor Name]**, **[!UICONTROL Factor Value]**, **[!UICONTROL Factor Type]** e **[!UICONTROL Factor Value Type]**) estão disponíveis.

      1. Selecione ![SelectBox](/help/assets/icons/SelectBox.svg) uma ou mais colunas de **[!UICONTROL SELECTED COLUMNS]** e use ![Divisa à esquerda](/help/assets/icons/ChevronLeft.svg) para remover as colunas selecionadas e retornar essas colunas de volta para **[!UICONTROL AVAILABLE COLUMNS]**.

      1. Selecione uma coluna de **[!UICONTROL DEFAULT SORT]** e alterne entre **[!UICONTROL Ascending]** ou **[!UICONTROL Descending]**.

      1. Para alterar a ordem das colunas exibidas, você pode mover uma coluna em **[!UICONTROL SELECTED COLUMNS]** para cima e para baixo por meio da ação de arrastar e soltar.

   1. Selecione **[!UICONTROL Submit]** para enviar suas alterações de configuração de coluna. Selecione **[!UICONTROL Close]** para cancelar as alterações feitas.

1. Se mais páginas estiverem disponíveis, use a ![Seta para a esquerda](/help/assets/icons/ChevronLeft.svg) ou a ![Seta para a direita](/help/assets/icons/ChevronRight.svg) em **[!UICONTROL Page _x _de_x_]** para se mover entre as páginas.

1. Como opção, é possível baixar os dados harmonizados.

   1. Selecione ![Baixar](/help/assets/icons/Download.svg) [!BADGE beta].
   1. No pop-up, selecione ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**.
   1. Digite um **[!UICONTROL Report name]**, por exemplo `Test Report`.
   1. Selecione ![FileCSV](/help/assets/icons/FileCSV.svg) **[!UICONTROL Report]**.

   Um relatório CSV com um título baseado no nome do relatório fornecido e na data e hora atuais (por exemplo, `Test Report_2025_04_23_9-5-18.csv`) é baixado para a pasta de download padrão.


## Práticas recomendadas

Ao criar seu conjunto de dados harmonizado, aplique as seguintes práticas recomendadas.

### Esquema

* Evite incompatibilidades de tipo de dados. As incompatibilidades ocorrem quando o tipo de dados de um campo nos registros dos seus conjuntos de dados assimilados não está em conformidade com o tipo de dados configurado para esse campo no esquema subjacente.
* Evite tipos de esquema incorretos. Tipos de esquema incorretos ocorrem quando você tenta assimilar um tipo específico de dados usando um conjunto de dados que não corresponde ao esquema para esses dados. Por exemplo, você tenta assimilar dados de resumo usando um conjunto de dados de fator externo.

### Mapeamento de dados

* Verifique se você configurou as identidades corretamente para cada um dos conjuntos de dados do evento.

### Qualidade dos dados

* Use o formato de data e hora de maneira consistente para todos os registros em conjuntos de dados que exigem dados com carimbo de data e hora.
* Use a mesma granularidade (dia ou semana) para registros em conjuntos de dados agregados ou resumidos.

### Cálculo de dados

* Evite linhas duplicadas em um conjunto de dados.
* Certifique-se de que cada conjunto de dados carregado seja específico para um canal exclusivo e um tipo de conversão. Pontos de contato ou conversões duplicados em vários conjuntos de dados afetam a saída e a qualidade do modelo.

