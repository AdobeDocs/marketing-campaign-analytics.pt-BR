---
title: Políticas
description: Saiba como acessar políticas do Marketing Campaign Analytics.
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
autotag-review: '2026-05-01T09:17:02.907Z'
TQID: 'https://experienceleague.adobe.com/uTMFYn3vc4-6JJefPhgFXGwaajrWQbgr9lW0y2s5B8U'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
  - id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
    internal-label: Data governance
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
    internal-label: Administration
subfeature_v2:
  - id: fd80ec6b-9b9e-448a-a6d0-b0c9a15da6b8
    internal-label: Policies
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 2%
---
# Políticas

{{mm-mca-rebranding}}

Depois de percorrer o fluxo de trabalho para criar um modelo e enviar a configuração do modelo, a [imposição de política](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) verifica se há violações. Se ocorrer uma violação de política, será exibido um popover indicando que uma ou mais políticas foram violadas. Essa verificação é para garantir que suas operações de dados e ações de marketing no Experience Platform estejam em conformidade com as políticas de uso de dados.

Por padrão, o Marketing Campaign Analytics verifica se há violações das políticas definidas pelo Adobe associadas aos seguintes rótulos e ações de marketing:

| Nome da política | Rótulo associado | Ação de marketing associada |
|---|---|---|
| Restringir análise de uso e medição baseada em usuário | C8 | Analytics |
| Restringir a ciência de dados | C9 | Ciência de dados |
| Restringir exportação de dados | C12 | Exportação de dados |

As violações também são verificadas para as políticas que você mesmo definiu e que contêm quaisquer ações de marketing listadas na tabela acima.

Ao violar uma política ao criar uma regra de conjunto de dados, você vê um popover que exibe informações sobre a violação da política.

Por exemplo:

- você habilitou a política [!UICONTROL Restrict data science] com o rótulo associado [!UICONTROL C9] e a ação de marketing associada [!UICONTROL Data Science],
- você aplicou o rótulo [!UICONTROL C9] - [!UICONTROL No data science] ao campo `totalCost` no esquema de Dados de conversão,
- você deseja configurar uma regra de conjunto de dados que, entre outras, mapeie o campo `totalCost` do esquema de Dados de conversão para o campo harmonizado com o nome `spend` (e o nome para exibição `Spend`).

Quando quiser salvar a regra do conjunto de dados, você verá um pop-up **[!UICONTROL Data governance policy violation detected]** exibindo uma lista de políticas violadas. Ao selecionar o nome da política, no [!UICONTROL Violation summary], você verá uma lista do [!UICONTROL Active data governance labels], contendo [!UICONTROL Entity], [!UICONTROL Type], [!UICONTROL Field] e [!UICONTROL Government labels] aplicados.

<!-- pending screenshot -->

Ao aplicar um rótulo de uso de dados a um campo de esquema que já é usado em dados harmonizados, você vê um popover que exibe informações sobre a violação de política.

Por exemplo:

- você configurou uma regra de conjunto de dados que, entre outras, mapeia o campo `totalCost` do seu esquema de Dados de conversão para o campo harmonizado com o nome `spend` (e o nome para exibição `Spend`).
- você sincronizou os dados harmonizados com êxito pelo menos uma vez (consulte [Regras do conjunto de dados - Sincronizar dados](/help/harmonize-data/dataset-rules.md#sync-data)).
- você habilita a política [!UICONTROL Restrict data science] com o rótulo associado [!UICONTROL C9] e a ação de marketing associada [!UICONTROL Data Science],
- você deseja aplicar o rótulo [!UICONTROL C9] - [!UICONTROL No data science] ao campo `totalCost` no esquema de Dados de conversão.

Quando quiser salvar a atualização do esquema, você verá um pop-up **[!UICONTROL Data governance policy violation detected]** exibindo uma lista de políticas violadas. Selecione o nome da política no [!UICONTROL Violation summary] para encontrar mais detalhes na lista [!UICONTROL Data Lineage].

<!-- pending screenshot -->

## Popovers de violação detectados

Os pop-ups detectados pela violação da política de governança de dados fornecem informações específicas sobre a violação. Você pode resolver essas violações por meio de configurações de política e outras medidas que não estejam diretamente relacionadas ao fluxo de trabalho de configuração. Por exemplo, você pode alterar os rótulos para que determinados campos sejam permitidos para fins de ciência de dados. Como alternativa, você também pode modificar a própria configuração do modelo, para que ele não use um objeto com um rótulo de uso de dados.

A seleção ![Privacidade](/help/assets/icons/Privacy.svg) **[!UICONTROL Policies]** no painel esquerdo fornece acesso à interface [!UICONTROL Policies] do Experience Platform, permitindo gerenciar suas políticas, rótulos e ações de marketing.

<!--
Currently,  Marketing Campaign Analytics does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[Visão geral das políticas de uso de dados](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/overview)
>
>

