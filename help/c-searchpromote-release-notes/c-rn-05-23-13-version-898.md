---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Notas de versão do Promote 8.9.8 (23/05/2013)
solution: Target
title: Search&amp;Notas de versão do Promote 8.9.8 (23/05/2013)
topic: Release Notes,Site search and merchandising
uuid: ff4bfc53-1d0e-4b7d-83ad-54c81d3f9769
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9.8 Release Notes (05/23/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Novo recurso </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Frases comuns - suporte para combinação exata </p> </td> 
   <td colname="col2"> <p> Frases comuns contêm termos de duas ou mais palavras que são pesquisadas como um todo, como "boot cut" ou "tank top" - e não como partes separadas. Uma frase comum possui um significado exclusivo e diferente de cada parte individual que a compõe. </p> <p> Mantenha um dicionário de frases comuns relacionadas ao seu negócio. Quando um cliente realizar uma consulta de pesquisa contendo várias palavras, será feita uma pesquisa no dicionário em busca da mesma combinação de palavras. </p> <p>É possível adicionar, editar ou excluir frases comuns. Você também pode reunir frases comuns similares aos dicionários do domínio. Por exemplo, é possível reunir frases comuns por vestuário, tecido, joias, medidas, compras e geral. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-common-phrases.md#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local"> Sobre frases comuns </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correções e melhorias**

* The backend search CGI parameter `sp_date_range_#` did not work for user-defined fields.

   Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend.

* Reverting **[!UICONTROL History]** version did not update the URL entrypoints field content.

   Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   Consulte também [Sobre pontos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

* A codificação de JSON não gerenciava caracteres codificados incorretamente.
* Foi adicionado suporte que permite encaminhar online remotamente um índice por etapas.

   Consulte [Sobre controle remoto para indexação](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

