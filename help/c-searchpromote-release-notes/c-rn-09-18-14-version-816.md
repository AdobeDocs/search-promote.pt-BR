---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Notas de versão do Promote 8.16.0 (18/9/2014)
solution: Target
title: Search&amp;Notas de versão do Promote 8.16.0 (18/9/2014)
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.16.0 Release Notes (9/18/2014){#search-promote-release-notes}

## Search&amp;Promote 8.16.0 Release Notes (9/18/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## New features {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Cache de resultados de pesquisa no Guided Search 3 (GS3) - Para ter essa configuração de recurso personalizada para você, de modo que possa usá-la em sua conta, entre em contato com seu Gerente de conta técnico da Adobe.
* Atualizações verticais para campos alterados com frequência - agora você pode atualizar rapidamente todos os valores para um conjunto de campos de metadados sem a necessidade de indexar seu conteúdo completamente.

   Consulte a opção Campo de atualização vertical na tabela em [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) de tag meta e [Sobre atualização](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)vertical.

   This feature can only be used on [!DNL Adobe Search&Promote] accounts that use Index Connector. Para ter essa configuração de recurso personalizada na sua conta, entre em contato com seu Gerente de conta técnico da Adobe.

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* Corrected the Index Connector parsing of XML feeds that contained `?>` string.
* Os feeds SFTP do Conector de índice foram corrigidos quando a contagem mínima do documento era executada.
* A exportação de relatório do Microsoft Excel agora é compatível com UTF8.
* Pesquisa guiada: a compilação de aspectos era lenta.
* Carregador de atributos: os dados agregados possuíam chaves duplicadas.
* Solucionado o problema que gerava uma ordem de execução incorreta da Regra de negócio quando uma regra individual era executada.
* Links de anulação de ação eram gerados pela Pesquisa guiada.
* Adicionada uma nova operação de controle remoto (`sp_lines=N`) que permite verificar o progresso e o status do rastreamento de índice em execução.

   Consulte [Sobre controle remoto para indexação](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* Necessário enviar informações auth ao obter informações excluídas durante a ampliação do Conector de índice.
* The [!DNL Change Log] report now identifies the user who initiates a manual index operation.

   See [Viewing the Change Log](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* When you export a [!DNL Terms Report], you are no longer limited to 500 or less items in the report.

   Consulte [Visualizando o Relatório de termos ou o Relatório de termos de pesquisa nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* A configuração **[!UICONTROL Strip HTML]** do Conector de índice estava sempre marcada.
* Inconsistent search results were experienced with the **[!UICONTROL Common Phrases]** feature.
* Os nomes de atribuição estava sendo exibidos de forma truncada nos resumos da lista de regras.
* Ao implementar uma Regra de negócio individual, todas a Regras de negócio estavam sendo implementadas.

