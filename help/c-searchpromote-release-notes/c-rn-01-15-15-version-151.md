---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Notas de versão do Promote 15.1.1 (15/01/2015)
solution: Target
title: Search&amp;Notas de versão do Promote 15.1.1 (15/01/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 15.1.1 Release Notes (01/15/2015){#search-promote-release-notes}

## Novo recurso {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Anteriormente, fenômenos linguísticos, como lematização, sinônimos e outros, costumavam ser aplicados a palavras-chave nas regras de Pesquisa guiada. Agora você pode desativar esta expansão para que a palavra-chave possa ser usada como ela é.

   Quando quiser aplicar condições de disparo a uma regra de negócios, na lista suspensa [!DNL Advanced Rule Builder], a seguir **[!UICONTROL If any/all of the following conditions are met]**, selecione **[!UICONTROL keyword]** e selecione o novo operador **[!UICONTROL equal exact]** na segunda lista suspensa.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] e [!DNL Advanced Rule Builder] não trunca mais o valor do campo MDI (ID do documento de comercialização).
* As falhas de indexação relacionadas a RBTA foram corrigidas.
* A edição de uma regra comercial existente que tenha o status &quot;aprovado&quot; agora revoga o status &quot;aprovado&quot;. You must use [!DNL Advanced Rule Builder] to recheck the option **[!UICONTROL Approved]**, and then save the rule as usual. If you do not reapprove an edited rule, the rule&#39;s status is automatically set to WIP (Work In Progress) on the [!DNL Business Rules] page.
* A new **[!UICONTROL Advanced Search]** option is now available on the [!DNL Business Rules] page for improved filtering of rules.
* Adicionada **[!UICONTROL contains word]** condição aos acionadores de regras em [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules]e [!DNL Business Rules], para que você possa especificar facilmente as quebras de palavras.
* Melhorias feitas em notas de regras de negócios, como quando você exibe uma regra, agora é possível recuperar o histórico de notas dessa regra. Além disso, as notas agora estão conectadas em **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Queries with nonzero `sp_i` values are no longer run through the [!DNL Adobe Analytics] redirector.

   Consulte a linha 15 na tabela em Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend.

