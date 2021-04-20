---
description: Search& amp; Notas de versão do Promote 8.12.0.
solution: Target
title: Search& amp; Notas de versão do Promote 8.12.0 (16/01/2014)
topic: Release Notes,Site search and merchandising
uuid: 4db10eb4-11bf-4483-a7f2-87981d9c7a50
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 72%

---


# Notas de versão do Search &amp; Promote 8.12.0 (16/01/2014){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Novos recursos e aprimoramentos </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adição de dicionários decorrentes </p> </td> 
   <td colname="col2"> <p> </p> <p> Foram adicionados dicionários decorrentes nos idiomas indonésio e turco. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" format="dita" scope="local"> Sobre dicionários</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Exportar relatórios </p> </td> 
   <td colname="col2"> <p> 
     <!--3683368-->Agora é possível exportar dados para CSV a partir dos seguintes relatórios: 
     <ul id="ul_93B619DBB3444F64BD6D7F9E969AB1E1"> 
      <li id="li_96DDE1A196834845A0FA319903C5934B"> <p>Relatório de termos </p> </li> 
      <li id="li_4F1A19DE98C84F8CAD963EEA2B38ED7A"> <p>Relatório de termos de pesquisa nula </p> </li> 
      <li id="li_A7716C62C4D44CD69D411C3FEE246D96"> <p>Relatório de solicitação de pesquisa </p> </li> 
     </ul> </p> <p>Consulte <a href="../c-about-reports-menu/c-about-reports-menu.md#concept_5F901459C7AB461BAB30B305957EB00C" format="dita" scope="local"> Sobre o menu Relatórios</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Não associar </p> </td> 
   <td colname="col2"> <p>Agora, você pode controlar as duas palavras que não devem ser associadas em resultados de pesquisas, como "Sweatshirt" e "Shirt". </p> <p> <p>Observação: Esse recurso não é habilitado por padrão. Entre em contato com o Adobe Customer Care para ativar o recurso no Search&amp;Promote para que você possa usá-lo. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correções**

* Não foi possível adicionar resultados em uma zona Recomendada que estivesse fora do critério de lapidamento selecionado atualmente.
* Não foi possível salvar as regras com base em resultados em uma conta com pesquisa somente por HTTPS.
* A configuração de uma regra de negócios para &quot;não é celular&quot; não funcionou.

   Consulte [Sobre as Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* A realização de uma pesquisa de filtro de inventário não gerou resultados.
* O pedido de lapidamento do tamanho não era atualizado.
* Adição da opção para uma definição de regra &quot;personalizada&quot; para a página Limpeza de consulta.

   Consulte [Sobre as Regras de Limpeza de Consulta](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C).

* O relatório Termos estava repetindo entradas se não houvesse dados suficientes.

   Consulte [Exibindo o Relatório de termos ou o Relatório de termos de pesquisa nulo..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Mover uma única regra de negócios em tempo real funcionava no modo Estágios, mas falhava no modo Em tempo real.
* As edições com preenchimento automático para Incluir ou Excluir listas não eram salvas no Histórico e, por isso, não podiam ser desfeitas.

   Consulte [Sobre a Conclusão Automática](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

