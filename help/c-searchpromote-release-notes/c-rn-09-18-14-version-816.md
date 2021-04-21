---
description: Search& amp; Notas de versão do Promote 8.16.0.
solution: Target
title: Search& amp; Notas de versão do Promote 8.16.0 (18/9/2014)
topic-legacy: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
exl-id: 929d6f97-4939-4e37-aded-6a746757b960
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 39%

---

# Notas de versão do Search &amp; Promote 8.16.0 (18/09/2014){#search-promote-release-notes}

## Notas de versão do Search &amp; Promote 8.16.0 (18/09/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## Novos recursos {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Armazenamento de resultados de pesquisa em cache no Guided Search 3 (GS3) - Para ter essa configuração de recurso personalizada para que você possa usá-la em sua conta, entre em contato com seu Gerente de conta técnico do Adobe.
* Atualizações verticais para campos alterados com frequência - Agora você pode atualizar rapidamente todos os valores de um conjunto de campos de metadados sem precisar reindexar completamente seu conteúdo.

   Consulte a opção Campo de atualização vertical na tabela em [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) e [Sobre atualização vertical](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

   Esse recurso só pode ser usado em contas [!DNL Adobe Search&Promote] que usam Conector de índice. Para ter essa configuração de recurso personalizada na sua conta, entre em contato com seu Gerente de conta técnico da Adobe.

## Correções e aprimoramentos {#section_22D1AFC99F394D569898828A0D3C419D}

* Correção da análise dos feeds XML do Conector de índice que continham `?>` sequência de caracteres.
* Os feeds SFTP do Conector de índice foram corrigidos quando a contagem mínima do documento era executada.
* A exportação de relatório do Microsoft Excel agora é compatível com UTF8.
* Pesquisa guiada: a compilação de aspectos era lenta.
* Carregador de atributos: os dados agregados possuíam chaves duplicadas.
* Solucionado o problema que gerava uma ordem de execução incorreta da Regra de negócio quando uma regra individual era executada.
* Links de anulação de ação eram gerados pela Pesquisa guiada.
* Adicionada uma nova operação de controle remoto (`sp_lines=N`) que permite verificar o progresso e o status do rastreamento de índice em execução.

   Consulte [Sobre o controle remoto para indexação](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* Necessário enviar informações auth ao obter informações excluídas durante a ampliação do Conector de índice.
* O relatório [!DNL Change Log] agora identifica o usuário que inicia uma operação de índice manual.

   Consulte [Exibindo o Log de alterações](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* Ao exportar um [!DNL Terms Report], você não está mais limitado a 500 itens ou menos no relatório.

   Consulte [Exibindo o Relatório de termos ou o Relatório de termos de pesquisa nulo..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* A configuração **[!UICONTROL Strip HTML]** do Conector de índice estava sempre marcada.
* Resultados de pesquisa inconsistentes eram exibidos no recurso **[!UICONTROL Common Phrases]**.
* Os nomes de atribuição estava sendo exibidos de forma truncada nos resumos da lista de regras.
* Transmitir uma regra de negócios individual era colocar todas as regras de negócios online.
