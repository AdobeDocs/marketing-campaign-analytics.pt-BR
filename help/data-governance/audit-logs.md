---
title: Logs de auditoria
description: Saiba como acessar logs de auditoria do Marketing Campaign Analytics.
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
autotag-review: '2026-05-01T09:16:13.122Z'
TQID: 'https://experienceleague.adobe.com/ZH89ZDOEMDwbvU5QnPtpkDft0U121-JDrhgEBPDuV3Q'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
    internal-label: Data governance
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
    internal-label: Administration
subfeature_v2:
  - id: bf7ac0fc-effb-4f0c-b93f-658412718d3c
    internal-label: Audits
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 6%
---
# Logs de auditoria

{{mm-mca-rebranding}}

Para aumentar a transparência e a visibilidade das atividades realizadas no sistema, a atividade do usuário no fluxo de trabalho do Marketing Campaign Analytics é capturada nos logs de auditoria do Experience Platform para entender quaisquer alterações orientadas pelo usuário nas categorias do Marketing Campaign Analytics. Esses registros formam uma trilha de auditoria que pode ajudar na solução de problemas e ajudar sua empresa a cumprir com as políticas corporativas de gerenciamento de dados e os requisitos normativos.

<!-- 
DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Marketing Campaign Analytics, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

Um log de auditoria informa quem executou qual ação e quando. Cada ação registrada em um log contém metadados que indicam o tipo de ação, a data e a hora, a ID do email do usuário que executou a ação e atributos adicionais relevantes ao tipo de ação. Ele rastreia as ações de criação, atualização e exclusão realizadas pelos usuários no Marketing Campaign Analytics.

Para inspecionar o log de auditoria, na interface do Marketing Campaign Analytics:

1. Selecione ![Lista de Tarefas](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]** de **[!UICONTROL PRIVACY]**.

1. Em **[!UICONTROL Audits]**, você pode encontrar o **[!UICONTROL Activity log]**. O log de atividades mostra entradas para as seguintes categorias, ações e status do Marketing Campaign Analytics.

   | Categoria | Ação | Status |
   |---|---|---|
   | Regra do conjunto de dados do Marketing Campaign Analytics | Criar | Permitir ou negar |
   | Regra do conjunto de dados do Marketing Campaign Analytics | Atualização | Permitir ou negar |
   | Regra do conjunto de dados do Marketing Campaign Analytics | Excluir | Permitir ou negar |
   | Campo do Marketing Campaign Analytics | Criar | Permitir ou negar |
   | Campo do Marketing Campaign Analytics | Atualização | Permitir ou negar |
   | Campo do Marketing Campaign Analytics | Excluir | Permitir ou negar |
   | Marketing Campaign Analytics Marketing Touchpoint | Criar | Permitir ou negar |
   | Marketing Campaign Analytics Marketing Touchpoint | Atualização | Permitir ou negar |
   | Marketing Campaign Analytics Marketing Touchpoint | Excluir | Permitir ou negar |
   | Conversão do Marketing Campaign Analytics | Criar | Permitir ou negar |
   | Conversão do Marketing Campaign Analytics | Atualização | Permitir ou negar |
   | Conversão do Marketing Campaign Analytics | Excluir | Permitir ou negar |
   | Modelo do Marketing Campaign Analytics | Criar | Permitir ou negar |
   | Modelo do Marketing Campaign Analytics | Atualização | Permitir ou negar |
   | Modelo do Marketing Campaign Analytics | Excluir | Permitir ou negar |
   | Modelo do Marketing Campaign Analytics | Pontuação | Permitir ou negar |
   | Modelo do Marketing Campaign Analytics | Clonar | Permitir ou negar |
   | Modelo do Marketing Campaign Analytics | Treinar / Treinar novamente | Permitir ou negar |
   | Modelo do Marketing Campaign Analytics | Baixar / Salvar metadados | Permitir ou negar |
   | Plano do Marketing Campaign Analytics | Criar | Permitir ou negar |
   | Plano do Marketing Campaign Analytics | Atualização | Permitir ou negar |
   | Plano do Marketing Campaign Analytics | Alterar modelo associado | Permitir ou negar |
   | Harmonização de dados do Marketing Campaign Analytics | Sincronização do acionador | Permitir ou negar |


1. Selecione uma entrada no Log de atividades para abrir um painel e obter mais detalhes.

   ![Auditoria do Marketing Campaign Analytics](/help/assets/mix-modeler-audit.png)

1. Para filtrar no intervalo **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** ou **[!UICONTROL Date]**, selecione ![Filtro](/help/assets/icons/Filter.svg).

1. Para modificar as colunas exibidas no Log de atividades, selecione ![Colunas](/help/assets/icons/ColumnSetting.svg) e, na caixa de diálogo **[!UICONTROL Customize table]**, selecione as colunas a serem exibidas. Selecione **[!UICONTROL Apply]** para aplicar a seleção, **[!UICONTROL Cancel]** para cancelar a seleção.

1. Para baixar o log de auditoria, selecione ![Baixar](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**. Na caixa de diálogo **[!UICONTROL Download log]**, selecione **[!UICONTROL CSV]** ou **[!UICONTROL JSON]** como o formato e selecione **[!UICONTROL Download]**.

## Acesso a logs de auditoria

Quando o recurso é ativado para sua organização, os logs de auditoria são coletados automaticamente conforme a atividade ocorre. Não é necessário ativar a coleta de log de auditoria manualmente.

Para exibir e exportar logs de auditoria, você deve ter recebido a permissão de controle Acesso aos logs de auditoria. Para saber como gerenciar permissões individuais para recursos do Marketing Campaign Analytics, consulte a [documentação de controle de acesso](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/home).
