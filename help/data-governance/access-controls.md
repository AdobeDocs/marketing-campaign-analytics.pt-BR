---
title: Controles de acesso
description: Saiba como configurar controles de acesso no Marketing Campaign Analytics.
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
autotag-review: '2026-05-01T09:20:37.287Z'
TQID: 'https://experienceleague.adobe.com/ThO2ylnzexAPA1qczBJ5EEfHErHphVQ3XjXug71w6A0'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
    internal-label: Datasets
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
    internal-label: Administration
subfeature_v2:
  - id: abe9e290-7d2f-4131-b71e-ef9900865044
    internal-label: Access control
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 3%
---
# Controles de acesso

{{mm-mca-rebranding}}

O controle de acesso do Marketing Campaign Analytics é fornecido por meio do Experience Platform no [Adobe Admin Console](https://adminconsole.adobe.com/) e de [Permissões](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) no Experience Platform. Essa funcionalidade aproveita perfis de produto no Admin Console, que vinculam usuários com permissões e sandboxes.

Para obter mais informações sobre o controle de acesso, consulte [Visão geral do controle de acesso](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/home).

## Controle de acesso baseado em função

Consulte [Administração](../main-guide/administration.md) sobre como configurar permissões de acesso com base em função para usuários e grupos de usuários do Marketing Campaign Analytics no Experience Platform.

## Controle de acesso baseado em atributos

[O controle de acesso baseado em atributos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) é um recurso do Experience Platform que permite aos administradores controlar o acesso a objetos e/ou recursos específicos com base em atributos. Os atributos podem ser metadados adicionados a um objeto, como um rótulo adicionado a um campo ou segmento de esquema. Um administrador define políticas de acesso que incluem atributos para gerenciar permissões de acesso do usuário.

Essa funcionalidade permite rotular campos de esquema do Experience Data Model (XDM) com rótulos que definem escopos organizacionais ou de uso de dados. Em paralelo, os administradores podem usar a interface de administração de usuários e funções para definir políticas de acesso em campos de esquema XDM. E gerencie melhor o acesso fornecido aos usuários ou grupos de usuários (usuários internos, externos ou de terceiros). Além disso, o controle de acesso baseado em atributos permite que os administradores gerenciem o acesso a segmentos específicos.

Por meio do controle de acesso baseado em atributos, os administradores podem controlar o acesso dos usuários a dados pessoais confidenciais (SPD) e a informações de identificação pessoal (PII) em todos os fluxos de trabalho e recursos da plataforma. Os administradores podem definir funções de usuário que tenham acesso somente a campos e dados específicos que correspondam a esses campos.

Ao configurar regras do conjunto de dados para conjuntos de dados harmonizados, o [controle de acesso baseado em atributos](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) da Experience Platform é aplicado em nível de campo. Um campo é restrito quando um rótulo é anexado a um campo de esquema. E uma política ativa é ativada para negar acesso a esse campo. Como resultado:

* você não vê os campos de esquema restritos ao criar uma regra de conjunto de dados,
* não é possível exibir ou editar o mapeamento de um ou mais campos de esquema restritos para você. Ao editar ou exibir uma regra de conjunto de dados contendo esses campos restritos, você verá a tela a seguir.
  ![Ação não permitida](/help/assets/action-not-permitted.png)
