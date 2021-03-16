---
description: Search& amp; Notas de versão do Promote 8.9.4.
solution: Target
title: Search& amp; Notas de versão do Promote 8.9.4 (17/01/2013)
topic: Notas de versão, Pesquisa e comercialização do site
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 33%

---


# Notas de versão do Search &amp; Promote 8.9.4 (17/01/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Novos recursos e aprimoramentos </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Regras </p> </td> 
   <td colname="col2"> <p> A capacidade de criar anotações em linha durante a criação de Regras de limpeza de consulta, Regras pré-pesquisa e Regras pós-pesquisa foi adicionada. O campo de anotações permite que você documente e explique as regras. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> Sobre as Regras de Limpeza de Consulta</a>. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> Sobre as regras de pré-pesquisa</a>. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> Sobre as regras pós-pesquisa</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pesquisa guiada </p> </td> 
   <td colname="col2"> <p> Adição de tags de Pesquisa guiada para indicar o tempo total de uma pesquisa. </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> - Identifica quanto tempo a pesquisa demorou. O valor de tempo de pesquisa retornado é especificado em ms. </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> - Retorna a contagem de pesquisas de núcleos usadas para criar a página de resultados de pesquisa. </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> - Testa se a contagem de pesquisas principais é maior que 1. </p> <p>Consulte também Idioma diversos em <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> Tags de modelo de apresentação</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correções**

* O Relatório de termos agora ignora o caractere asterisco.

   Consulte [Exibindo o Relatório de termos ou o Relatório de termos de pesquisa nulo..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Abra **[!UICONTROL Reports > Null Search Terms Report]**, selecione um período e visualize o relatório. Clique em uma palavra do relatório para abrir a pesquisa e clique em Exibir relatório. O contador da pesquisa da palavra-chave que você clicou aumentou duas vezes. Isso agora foi corrigido.

   Consulte [Exibindo o Relatório de termos ou o Relatório de termos de pesquisa nulo..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Uma otimização de desempenho foi feita para quando você coloca as regras de negócios online.

   Consulte [Sobre as Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* A capacidade de excluir no [!DNL Breadcrumbs] não funcionava o tempo todo.

   Consulte [Sobre navegação estrutural](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* A menos que você tenha usado a regeneração, o recurso de nova classificação não permitia que nenhuma regra de classificação alterada entrasse em vigor nos resultados da pesquisa.

   Consulte [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

   Consulte [Sobre o Índice de Nova Classificação](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692).

