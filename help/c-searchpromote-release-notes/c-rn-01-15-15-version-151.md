---
description: Search& amp; Notas de versão do Promote 15.1.1.
solution: Target
title: Search& amp; Notas de versão do Promote 15.1.1 (15/01/2015)
topic: Notas de versão, Pesquisa e comercialização do site
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 16%

---


# Notas de versão do Search &amp; Promote 15.1.1 (15/01/2015){#search-promote-release-notes}

## Novo recurso {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Anteriormente, fenômenos linguísticos, como lematização, sinônimos e outros, costumavam ser aplicados a palavras-chave nas regras de Pesquisa guiada. Agora você pode desativar esta expansão para que a palavra-chave possa ser usada como ela é.

   Quando quiser aplicar condições de ativação a uma regra de negócios, no [!DNL Advanced Rule Builder], depois de **[!UICONTROL If any/all of the following conditions are met]**, na primeira lista suspensa, selecione **[!UICONTROL keyword]** e selecione o novo operador **[!UICONTROL equal exact]** na segunda lista suspensa.

   Consulte [Sobre as Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Correções e aprimoramentos {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] e  [!DNL Advanced Rule Builder] não truncará mais o valor de campo MDI (ID de documento de merchandising).
* As falhas de indexação relacionadas a RBTA foram corrigidas.
* A edição de uma regra comercial existente que tenha o status de &quot;aprovada&quot; agora revoga o status de &quot;aprovada&quot;. Você deve usar [!DNL Advanced Rule Builder] para marcar novamente a opção **[!UICONTROL Approved]** e, em seguida, salvar a regra como de costume. Se você não aprovar novamente uma regra editada, o status da regra é automaticamente definido para WIP (Trabalho em progresso) na página [!DNL Business Rules] .
* Uma nova opção **[!UICONTROL Advanced Search]** está disponível na página [!DNL Business Rules] para filtragem aprimorada das regras.
* Adição da condição **[!UICONTROL contains word]** aos acionadores de regras em [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules] e [!DNL Business Rules], para que você possa especificar facilmente as quebras de palavras.
* Melhorias feitas nas notas de regras de negócios, como ao visualizar uma regra, agora é possível recuperar o histórico de notas dessa regra. Além disso, agora as notas estão conectadas em **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Consultas com valores `sp_i` diferentes de zero não são mais executadas pelo redirecionador [!DNL Adobe Analytics].

   Consulte a linha 15 na tabela em [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

