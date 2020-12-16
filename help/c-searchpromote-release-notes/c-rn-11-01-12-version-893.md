---
description: 'null'
seo-description: nulo
seo-title: Search&amp;Notas de versão do Promote 8.9.3 (01/11/2012)
solution: Target
title: Search&amp;Notas de versão do Promote 8.9.3 (01/11/2012)
topic: Release Notes,Site search and merchandising
uuid: 7bc7bcb6-f47f-4e05-94e5-a22a13a187b7
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 84%

---


# Notas de versão do Search &amp; Promote 8.9.3 (01/11/2012){#search-promote-release-notes}

## Notas de versão do Search &amp; Promote 8.9.3 (01/11/2012) {#concept_85F5B4B4C40C43FEA3AD63E6EA5593CF}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Novos recursos e aprimoramentos </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Facet Rail </p> </td> 
   <td colname="col2"> <p> 
     <!--3309390--> Adicionada a nova opção <span class="uicontrol">Facet Rail</span> para ajudá-lo a ter melhor controle sobre a ordem de famílias de colunas e nomes de colunas (por contagem, em ordem alfabética). </p> <p>Consulte <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">Sobre o Facet Rail</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Facetas aninhadas </p> </td> 
   <td colname="col2"> <p> Adicionado suporte para alternar a classificação de tipos de colunas aninhadas. </p> <p>Consulte <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">Sobre o Facet Rail</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Campo de notas nas regras de classificação </p> </td> 
   <td colname="col2"> <p> 
     <!--3063772--> Adicionado um campo de <span class="wintitle">Notas</span> de várias linhas para a caixa de diálogo <span class="wintitle">Adicionar métrica de classificação</span> e na caixa de diálogo <span class="wintitle">Editar métrica de classificação</span> para classificar regras e definições de regras de grupo. </p> <p>Notas de regra de classificação são exibidas na página <span class="wintitle">Definir Regras de classificação</span>. Notas de regras de grupo aparecem ao editar a definição. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" format="dita" scope="local">Sobre regras de classificação</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regras de negócios </p> </td> 
   <td colname="col2"> <p> 
     <!--3331637--> Aprimorado o suporte de página de chegada pela remoção de resultados naturais em uma regra comercial usando a nova opção <span class="uicontrol">Remover Todos os Resultados</span>. </p> <p>Use essa nova opção junto com outras ações de regras comerciais para criar "páginas de chegada gravadas" . Ou seja, você precisa criar conteúdos de página exclusivamente por ações de regra comercial e descartar os resultados "naturais" da pesquisa. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" format="dita" scope="local">Adicionar uma nova regra comercial</a> ou <a href="../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087" format="dita" scope="local">Editar uma regra comercial</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Banners e regras de negócios </p> </td> 
   <td colname="col2"> <p> Adicionada uma opção de suporte na qual você pode cancelar de forma condicional a publicação de banners quando a regra comercial que faz referência ao banner é ativada. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correções**

* Regras de negócios trabalhadas com inconsistência quando existe um índice [!DNL Stage].
* Regras de classificação automática agora são aplicadas a páginas iniciais gravadas.

   Consulte a tabela de opções em [Adicionar uma regra de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

* [!DNL promosearch.cgi] não retornava promoções.

   Consulte [Sobre pesquisadores](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

* As regras de envio que fazem referência a muitos banners às vezes falhavam.

   Consulte [Sobre banners](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA).

* **[!UICONTROL Did You Mean]** o cache de query de pesquisa agora está desativado.

   Consulte [Sobre você quis dizer](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

