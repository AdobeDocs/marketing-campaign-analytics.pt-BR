---
title: Campos harmonizados
description: Saiba como definir campos para usar como parte da harmonização de seus dados no Marketing Campaign Analytics.
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
autotag-review: '2026-05-01T09:13:17.577Z'
TQID: 'https://experienceleague.adobe.com/ZmBwgBCVOPCVJ1pdniya3RvjWagTQuLSQoxluuDQLbc'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
    internal-label: Marketing Campaign Analytics
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
    internal-label: Harmonized data
subfeature_v2:
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
    internal-label: Dataset mapping
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
    internal-label: Harmonized fields
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 9d6bd798e97d36d49b7753dc9574b102efb3d6bf
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 11%
---
# Campos harmonizados

{{mm-mca-rebranding}}

Campos harmonizados permitem definir campos para os mesmos dados conceitualmente, originários de diferentes fontes, cada uma com sua própria definição desses dados. Por exemplo, uma métrica de cliques pode ser definida e nomeada de forma diferente dependendo da fonte de dados. Um campo harmonizado de cliques permite definir uma nomenclatura comum para uma métrica de cliques com base nessas diferentes fontes de dados de cliques.

Campos harmonizados permitem definir os campos que deseja usar como parte do fluxo de trabalho de dados harmonizados. Os campos definidos podem ser usados na definição de regras de conjunto de dados, pontos de contato de marketing e conversões.

## Domínios de harmonização global

Os campos de harmonização global disponíveis por padrão no Marketing Campaign Analytics são:


| Nome do campo | Nome de exibição | Categoria | Tipo de dados | Comentário |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| marca | Marca | Dimensão | String |           |
| campaign | Campaign | Dimensão | String |           |
| canal | Canal | Dimensão | String |           |
| channel_id | ID do canal | Dimensão | String |           |
| channel_type_at_source | Tipo De Canal No Source | Dimensão | String |           |
| canal | Canal | Dimensão | String |           |
| cliques | Cliques | Métrica | Número |           |
| conversiontype | Tipo de conversão | Dimensão | String |           |
| custo | Custo | Métrica | Currency |           |
| conjunto de dados | Conjunto de dados | Dimensão | String |           |
| date_type | Tipo de data | Dimensão | String | dia, semana |
| emails enviados | Emails enviados | Métrica | Número |           |
| event_date | Data | Dimensão | Data e hora |           |
| demanda_bruta | Demanda Bruta | Métrica | Currency |           |
| impressões | Impressões | Métrica | Número |           |
| data_da_última_atualização | Data da última atualização | Dimensão | Data e hora |           |
| linkvisitors | Vincular visitas | Métrica | Número |           |
| mediatype | Tipo de mídia | Dimensão | String |           |
| net_sales | Vendas Líquidas | Métrica | Currency |           |
| pedidos | Pedidos | Métrica | Número |           |
| sourcetype | Tipo de Source | Dimensão | String |           |
| gasto | Gastos | Métrica | Currency |           |
| fonte de tráfego | Traffic Source | Dimensão | String |           |

{style="table-layout:auto"}

É possível adicionar, editar ou excluir seus próprios campos harmonizados sobre esses campos harmonizados globais.

## Gerenciar campos harmonizados

Para ver uma tabela dos campos harmonizados disponíveis, na interface do Marketing Campaign Analytics:

1. Selecione ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** no painel esquerdo.

1. Selecione **[!UICONTROL Fields]** na barra superior. Você vê uma tabela dos campos harmonizados. Se mais páginas estiverem disponíveis, use a ![Seta para a esquerda](/help/assets/icons/ChevronLeft.svg) ou a ![Seta para a direita](/help/assets/icons/ChevronRight.svg) em **[!UICONTROL Page _x _de_x_]** para se mover entre as páginas da tabela.

   As colunas da tabela especificam os detalhes sobre os campos harmonizados

   | Nome da coluna | Detalhes |
   | ---------------------- | ----------|
   | Nome do campo | O nome do campo harmonizado. |
   | Nome de exibição | O nome de exibição do campo harmonizado. Esse nome de exibição é usado ao definir regras de conjunto de dados, ponto de contato de marketing e definições de conversão. |
   | Categoria | Especifica se um campo de dados harmonizado é [!UICONTROL Dimension], [!UICONTROL Metric] ou [!UICONTROL Derived]. Uma categoria derivada é um campo harmonizado que usa uma definição de fórmula baseada em métricas. |
   | Tipo de dados | Especifica o tipo de dados ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]). |
   | Data de criação | Data e hora de criação do campo harmonizado. |
   | Proprietário | Indica se um campo harmonizado é padrão ([!UICONTROL Global]) ou se está definido por você ([!UICONTROL Client]). |
   | Última data de modificação | Data e hora da última modificação do campo harmonizado. |
   | Fórmula | Especifica a fórmula para um campo harmonizado com base em uma categoria derivada. |

   {style="table-layout:auto"}

1. Para pesquisar um campo harmonizado específico, use ![Pesquisar](/help/assets/icons/Search.svg) **[!UICONTROL *Pesquisar campo harmonizado *]**.


### Adicionar um campo harmonizado

Para adicionar um campo harmonizado, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** do Marketing Campaign Analytics:

1. Selecione ![Adicionar](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. No diálogo **[!UICONTROL Create]**:

   1. Digite um **[!UICONTROL Field name]**, por exemplo `region`.
   1. Digite um **[!UICONTROL Display name]**, por exemplo `Region`.
   1. Selecione um **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** ou **[!UICONTROL Derived]**.

      Ao selecionar **[!UICONTROL Derived]**, especifique um **[!UICONTROL Formula]**. Para criar uma expressão aritmética válida, combine uma ou mais métricas de **[!UICONTROL Insert Metric]** com um ou mais operadores **[!UICONTROL + - * / ( )]** . Por exemplo, `[orders]/[impressions]`

   1. Selecione um **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** ou **[!UICONTROL Date time]**, quando a Categoria selecionada for Dimension.
      - **[!UICONTROL Number]** ou **[!UICONTROL Currency]** quando a Categoria selecionada é Métrica ou Derivada.

   1. Selecione **[!UICONTROL Submit]** para adicionar o campo harmonizado. Selecione **[!UICONTROL Close]** para fechar a caixa de diálogo sem adicionar o campo harmonizado.

      ![Criar um campo](/help/assets/create-field.png)


### Editar um campo harmonizado

Você só pode editar campos harmonizados criados anteriormente (o proprietário é o cliente). Não é possível editar um campo harmonizado global.

Para editar um campo harmonizado, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** do Marketing Campaign Analytics:

1. Selecione o campo harmonizado que deseja editar. Por exemplo, **[!UICONTROL Region]**.

1. No painel **[!UICONTROL Edit harmonization values]**, modifique os valores para **[!UICONTROL Display name]**, **[!UICONTROL Category]** e **[!UICONTROL Data type]**. Consulte [Adicionar um campo harmonizado](#add-a-harmonized-field) para obter mais informações.

1. Selecione **[!UICONTROL Submit]** para aplicar as alterações ao campo harmonizado.

   ![Editar um campo](/help/assets/edit-field.png)

### Excluir um campo harmonizado

Você só pode excluir campos harmonizados criados anteriormente (o proprietário é o cliente). Não é possível excluir um campo harmonizado global.

Para excluir um campo harmonizado, na interface ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** da Marketing Campaign Analytics:

1. Selecione o campo harmonizado que deseja excluir, por exemplo **[!UICONTROL Region]**.

1. Selecione ![Excluir](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** do painel esquerdo **[!UICONTROL Edit harmonization values]**.

   >[!WARNING]
   >
   >   O campo será excluído imediatamente.

