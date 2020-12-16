---
description: 'null'
seo-description: nulo
seo-title: Search&amp;Notas de versão do Promote 15.1.1 (15/01/2015)
solution: Target
title: Search&amp;Notas de versão do Promote 15.1.1 (15/01/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 17%

---


# Notas de versão do Search &amp; Promote 15.1.1 (15/01/2015){#search-promote-release-notes}

## Novo recurso {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Anteriormente, fenômenos linguísticos, como lematização, sinônimos e outros, costumavam ser aplicados a palavras-chave nas regras de Pesquisa guiada. Agora você pode desativar esta expansão para que a palavra-chave possa ser usada como ela é.

   Quando quiser aplicar condições de disparo a uma regra de negócios, em [!DNL Advanced Rule Builder], após **[!UICONTROL If any/all of the following conditions are met]**, na primeira lista suspensa, selecione **[!UICONTROL keyword]** e selecione o novo operador **[!UICONTROL equal exact]** na segunda lista suspensa.

   Consulte [Sobre Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Correções e aprimoramentos {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] e  [!DNL Advanced Rule Builder] não trunca mais o valor do campo MDI (ID do Documento de comercialização).
* As falhas de indexação relacionadas a RBTA foram corrigidas.
* A edição de uma regra comercial existente que tenha o status &quot;aprovada&quot; agora revoga o status &quot;aprovada&quot;. Você deve usar [!DNL Advanced Rule Builder] para marcar novamente a opção **[!UICONTROL Approved]** e depois salvar a regra como de costume. Se você não aprovar novamente uma regra editada, o status da regra será automaticamente definido como WIP (Trabalho em andamento) na página [!DNL Business Rules].
* Uma nova opção **[!UICONTROL Advanced Search]** está disponível na página [!DNL Business Rules] para melhor filtragem de regras.
* Adicionada a condição **[!UICONTROL contains word]** aos acionadores de regras em [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules] e [!DNL Business Rules], para permitir que você especifique facilmente as quebras de palavras.
* Melhorias feitas em notas de regras de negócios, como quando você visualização uma regra, agora é possível recuperar o histórico de notas dessa regra. Além disso, as notas agora estão conectadas em **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Query com valores diferentes de `sp_i` não são mais executados pelo redirecionador [!DNL Adobe Analytics].

   Consulte a linha 15 na tabela em [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

