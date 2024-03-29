---
description: Saiba mais sobre como usar tags de apresentação e modelo no Search&amp;Promote.
solution: Target
title: Modelos
topic-legacy: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
exl-id: f8cc4b5c-4e75-426b-8234-76af8bb0f4c5
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '15148'
ht-degree: 2%

---

# Modelos{#templates}

## Modelos {#concept_A5CFB6BD805D49459A96219AF1B17842}

## Tags de modelo de apresentação {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

Uma lista de tags e atributos de pesquisa/comercialização do site para modelos de apresentação.


Um modelo de apresentação é um arquivo HTML que inclui tags de modelo de apresentação definidas por pesquisa/merchandising de site. Essas tags indicam como os resultados da pesquisa que os clientes veem são formatados.

Consulte [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Você pode selecionar entre os seguintes grupos de tags de apresentação:

* [Declarações](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [Resultados](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [Aspectos](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [Caminho](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [Menus](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [Pesquisas recentes](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [Você quis dizer](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [Preencher automaticamente](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [Loja](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [Zonas](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [Indicadores de loop](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [Idioma Diverso](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## Declarações {#section_82C5CA734D2941EB858FEFE3B695D2EC}

As declarações são tags especiais de declaração guiada que podem ser definidas no topo de um modelo de apresentação de nível superior. Quaisquer declarações subsequentes são ignoradas, incluindo declarações em modelos incluídos.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-content-type-header content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Por padrão, o template de apresentação é enviado de volta com um tipo MIME de texto/html. Você pode alterar o tipo de conteúdo usado com essa tag. </p> <p>Declare essa tag o mais alto possível em seu modelo de apresentação. Não adicione outro texto na mesma linha com essa tag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-declare&gt; </span> </p> </td> 
   <td colname="col2"> <p> Se estiver retornando XML, você poderá usar essa tag para criar a declaração XML. Transforme essa tag na primeira linha do modelo de apresentação. Ao usar essa tag, o tipo de conteúdo é automaticamente definido como text/xml, a menos que você a substitua por <span class="codeph"> &lt;guided-content-type-header&gt; </span> na primeira linha. Se você não especificar um charset, o padrão será UTF-8. Essa tag resulta na seguinte saída em seu documento XML: </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes" ?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultados {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag guided-results define os limites de um loop de resultados. Qualquer conjunto de resultados pode ser acessado especificando um atributo <span class="codeph"> gsname </span>. Se nenhum <span class="codeph"> gsname </span> for fornecido, os resultados de pesquisa padrão serão exibidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Para criar um link para um determinado resultado, use a tag <span class="codeph"> guided-result-link </span>. Ao definir um atributo <span class="codeph"> gsname </span>, você pode usar um campo do índice em vez da tag "loc" padrão que faz referência ao "search-url". Quaisquer outros atributos, como classe e destino, também podem ser transmitidos, que são gerados na tag de âncora resultante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-img gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag <span class="codeph"> &lt;guided-result-img&gt; </span> ajuda a criar tags de imagem em vez de incorporar variáveis dentro de uma tag <span class="codeph"> img </span> bruta. </p> <p>Especifique o campo a ser usado para o caminho da imagem no atributo <span class="codeph"> gsname </span>. O resultado é uma tag <span class="codeph"> img </span> com qualquer atributo HTML padrão que você tenha definido, passado. Assim, o exemplo a seguir: </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>becomes: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided-result-field gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Qualquer informação a ser apresentada nos resultados é exibida como uma tag <span class="codeph"> &lt;guided-result-field&gt; </span> (exceto ao usar tags de geração automática como a tag <span class="codeph"> &lt;guided-result-img&gt; </span>). </p> <p>Especifique o nome do campo Search index em <span class="codeph"> gsname </span>. A sequência exata transmitida é a saída no modelo. </p> <p>Você pode especificar uma opção de escape se quiser que esse campo escape de forma diferente do que foi especificado no modelo de transporte. </p> <p>Essa codificação é aplicada sobre qualquer codificação especificada no modelo de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if-result-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags condicionais é verdadeiro se houver conteúdo no campo específico a ser exibido. Se não houver conteúdo, a condição será false. Você pode usar as tags para decidir se o HTML circundante é exibido ou não, se um valor não existe, ou se uma imagem diferente é exibida, e assim por diante. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"&nbsp;/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"&nbsp;/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <code> &lt;guided-if[-not]-result-wrap&gt; 
      &lt;guided-else-result-wrap&gt; 
      &lt;/guided-if[-not]-result-wrap&gt; </code> </p> </td> 
   <td colname="col2"> <p>Ao exibir resultados em colunas, essa tag é usada para identificar se o resultado atual marca o final de uma coluna. </p> <p>Quando a condição Booleana é verdadeira, HTML é adicionado ao final do resultado para terminar a linha e iniciar uma nova. Quando for a última, uma nova linha não será iniciada. </p> <p>Consulte <span class="codeph"> &lt;guided-if-not-last&gt; </span> para saber mais sobre essa tag. </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-results-found&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna um 1 se a solicitação de pesquisa de back-end retornou resultados e 0 se não retornou. Se nenhum <span class="codeph"> gsname </span> for especificado, a tag assumirá a pesquisa primária. Essa tag é útil para transmitir lógica às rotinas do JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o número total de resultados no conjunto de resultados especificado. Assume a pesquisa padrão quando nenhum <span class="codeph"> gsname </span> é fornecido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o número do resultado menor na página para o conjunto de resultados especificado. Assume a pesquisa padrão quando nenhum <span class="codeph"> gsname </span> é fornecido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o número do resultado superior na página para o conjunto de resultados especificado. Assume a pesquisa padrão quando nenhum <span class="codeph"> gsname </span> é fornecido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-results-found&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Mostra o conteúdo quando os resultados são encontrados. Ou não mostra resultados em HTML quando os resultados não são encontrados. </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-title /&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag <span class="codeph"> &lt;guided-result-title&gt; </span> fornece o valor do campo do modelo de transporte de título especificado com <span class="codeph"> &lt;title&gt; </span> tag de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description /&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag <span class="codeph"> &lt;guided-result-description&gt; </span> fornece o valor do campo de modelo de transporte de descrição especificado com a tag de transporte <span class="codeph"> &lt;description&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc /&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag &lt; <span class="codeph"> guided-result-loc&gt; </span> fornece o valor do campo do modelo de transporte loc especificado com a tag de transporte <span class="codeph"> &lt;loc&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-result-field&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>True se houver conteúdo no campo específico a ser exibido. Se não houver conteúdo, a condição será false. Use as tags para decidir se o HTML circundante é exibido ou não, se um valor não existe, ou se uma imagem diferente é exibida, e assim por diante. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta tag fornece um loop pela tabela de atributos definida no modelo de transporte com a tag de transporte <span class="codeph"> &lt;attribute_table&gt; </span> . Existe uma tag <span class="codeph"> &lt;guided-result-attribute-table-field&gt; </span> para exibir valores de campos da tabela de atributos. Além disso, é possível usar a tag simples <span class="codeph"> guided-result-field </span> dentro do loop para exibir outros campos de resultado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Exibe o campo da tabela do atributo conforme definido no modelo de transporte. </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;guided-result-attribute-table&amp;nbsp;gsname=&quot;downloads&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;li&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;a&amp;nbsp;href=&quot; lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-result-attribute-attribute-table -field&amp;nbsp;gsname=&quot;download_title&quot;&amp;nbsp;/&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/a&amp;gt;&amp;nbsp;(&amp;lt;guided-result-field&amp;nbsp;gsname=&quot;title&quot;/&amp;gt;)
    &amp;nbbsp sp;&amp;nbsp;&amp;lt;/li&amp;gt;
    &amp;lt;/guided-result-attribute-table&amp;gt;
    
    &amp;lt;/ul&amp;gt;
    
    ...
    
    &amp;lt;/guided-results&amp;gt;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera as informações de rastreamento encontradas nos dados de rastreamento na seção geral da saída de dados JSON pelo modelo de transporte para a pesquisa fornecida. </p> <p>Se nenhum nome de pesquisa for fornecido, <span class="codeph"> padrão </span> será assumido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;guided-result-trace /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera o conteúdo JSON encontrado em resultados &gt; informações de rastreamento da saída de dados JSON pelo modelo de transporte para o resultado de pesquisa atual. </p> <p>Essa tag é válida somente no loop <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aspectos {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

As facetas são componentes de navegação que permitem detalhar os resultados da pesquisa. Você pode usar as tags de faceta para exibir várias facetas no modelo de apresentação. Você faz referência a aspectos por nome.

Consulte [Sobre facetas](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Consulte [Sobre o Facet Rail](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

Consulte [Sobre Aspectos Dinâmicos](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> <span class="codeph"> &lt;guided-dynamic-facets&gt;&lt;/guided-dynamic-facets&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>Um contexto de loop para quaisquer aspectos dinâmicos de uma determinada pesquisa. </p> <p>A tag do modelo de apresentação <span class="codeph"> &lt;guided-facet&gt; </span> é editada para que o atributo gsname seja automaticamente fornecido pelo contexto de loop <span class="codeph"> &lt;guided-dynamic-facets&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o rótulo de exibição da faceta. </p> <p>Se a faceta usar a tag <span class="codeph"> &lt;display-name&gt; </span> no modelo de transporte, o conteúdo dessa tag se tornará o rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-rail&gt;&lt;/guided-facet-rail&gt; </span> </p> </td> 
   <td colname="col2"> <p> Define uma seção no modelo de apresentação que é usada como um padrão de repetição para cada faceta no painel de facetas. </p> <p> Cada faceta que pertence ao painel de facetas usa esta seção para avaliar sua saída. </p> <p>Este é um exemplo de um painel de faceta: </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>Observe que as tags a seguir não precisam do atributo <span class="codeph"> gsname </span> quando dentro da tag <span class="codeph"> &lt;guided-facet-Rail&gt; </span> o valor é determinado dinamicamente no tempo de pesquisa e é substituído corretamente: </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">aspecto guiado </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">guided-facet-display-name </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">contagem total de facetas guiadas </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">guided-facet-undo-link </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">guided-facet-undo-path </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">comportamento orientado de faceta </li> 
    </ul> <p>Os critérios de classificação na página <span class="wintitle"> Facet Rail </span> determinam a posição das facetas. Você pode escolher a ordem de classificação na lista suspensa Método de classificação de aspectos . </p> <p> 
     <!--NEW 02/27/2014-->Como opção, essa tag pode aceitar um valor de atributo gsname de  <span class="codeph"> _dynamic_facets  </span>, que fornece um contexto de loop para quaisquer aspectos dinâmicos para essa pesquisa. Esse painel de facetas predefinido também é exposto na interface do usuário das Regras de negócios para a ação <span class="codeph"> empurrar o aspecto X no painel de facetas '_dynamic_facets' para posicionar Y </span>". </p> <p>Consulte <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">Sobre o Facet Rail </a>. </p> <p>Consulte também <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Sobre Aspectos Dinâmicos </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" <span class="varname"> 60px </span>" width=" <span class="varname"> 120px </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Use a tag <span class="codeph"> guiada-faceta </span> para definir uma área dentro da qual todas as tags de faceta se relacionam a uma faceta específica. Essa tag também é uma tag booleana que oculta todo o conteúdo se nenhum valor na faceta existir. Nesse caso, não faz sentido colocar os valores de faceta). </p> <p>Os atributos de altura e largura são opcionais e as dimensões são especificadas em pixels (px). O Visual Rule Builder (VRB) usa esses dois atributos e exibe uma caixa pontilhada como um espaço reservado interativo quando a faceta está oculta. </p> <p> Quando o nome de exibição está na faceta e a faceta está oculta, o nome também fica oculto. No entanto, se o nome estiver fora da faceta, você só poderá ocultar o nome se uma tag <span class="codeph"> zone </span> ou uma tag <span class="codeph"> guided-if-facet-visible </span> estiver envolta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é verdadeira quando o número de valores de faceta está acima do limite de comprimento definido na configuração. Use-o para exibir uma faceta como um elemento de interface do usuário diferente (como uma lista truncada ou uma caixa de rolagem) quando a lista for muito longa. </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-option&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Também é possível usar essa condição fora do contexto de um bloco nomeado <span class="codeph"> guided-facet </span> referenciando uma faceta específica diretamente por meio do uso do atributo <span class="codeph"> gsname </span>. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é verdadeira quando a faceta é clicada pelo menos uma vez e um valor de faceta é selecionado no momento. Ele é usado para mostrar ou ocultar tags HTML ou gs , dependendo se uma faceta foi clicada. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Também é possível usar essa condição fora do contexto de um bloco nomeado <span class="codeph"> guided-facet </span> referenciando uma faceta específica diretamente por meio do uso do atributo <span class="codeph"> gsname </span>. </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é verdadeira quando há apenas um valor de faceta. Use a tag para alterar a exibição da faceta quando ela não tiver capacidade de refinar os resultados. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Também é possível usar essa condição fora do contexto de um bloco nomeado <span class="codeph"> guided-facet </span> referenciando uma faceta específica diretamente por meio do uso do atributo <span class="codeph"> gsname </span>. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if&gt;&lt;/guided-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é verdadeira quando a faceta é de seleção múltipla. Use a tag para alterar a exibição da faceta dentro das tags <span class="codeph"> &lt;guided-facet-Rail&gt; </span> ou <span class="codeph"> &lt;guided-dynamic-facets&gt; </span>. </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;guided-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;....
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet-Rail&amp;gt;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-values&gt; facetname  </span>"]&gt;&lt;/guided-facet-values&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Esta é a tag iteradora do loop de valores de faceta. Você pode defini-lo no contexto de um bloco <span class="codeph"> guiado-faceta </span> nomeado, nesse caso, você pode omitir o <span class="codeph"> <span class="varname"> gsname </span> </span>. Ou você pode defini-lo fora de qualquer bloco <span class="codeph"> guiado-faceta </span>, mas isso exigiria o atributo <span class="codeph"> <span class="varname"> gsname </span> </span> para identificar qual conjunto de valores de faceta é exibido. </p> <p>Também é possível usar essa tag para exibir os valores de faceta fora do contexto de um bloco nomeado <span class="codeph"> guided-facet </span>. Você faz referência a uma faceta específica diretamente usando o atributo <span class="codeph"> <span class="varname"> gsname </span> </span>. </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10º </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera a string do valor da faceta atual. </p> <p>Por padrão, o valor é HTML escaped. Você pode usar a opção de escape para alterar como o valor é evitado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11º </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-count /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera o número de resultados que correspondem ao valor de aspecto atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12º </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-facet-value-link&gt;&lt;/guided-facet-value-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cria um link ao redor da string de valor de faceta para o visitante do site clicar. O caminho é gerado automaticamente para limitar os resultados pelo valor de aspecto atual. Ele suporta a transmissão de qualquer atributo diretamente para a tag de âncora. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-value-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13º </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <code> &lt;guided-if-facet-value-selected&gt; 
      &lt;guided-else-facet- 
      value-selected&gt; 
      &lt;/guided-if-facet-value-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Altera a exibição do valor da faceta quando ele está selecionado no momento. Se já tiver sido escolhido, na maioria dos casos, já não é vinculável. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value/&gt;&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt;&nbsp;&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14. </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-facet-value-ghost&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Altera a exibição do valor da faceta quando ele é um valor fantasma. Quando um valor de faceta é um valor fantasma, ele normalmente é exibido em itálico para indicar que o valor está ausente ou "fantasma". </p> <p>O seguinte trecho de código é um exemplo de um bloco de faceta: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;i&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(0)&lt;/i&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="link"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;) 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15. </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-undo-link gsname=" <span class="varname"> facetname </span>"&gt;&lt;/guided-facet-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Exibe um link para desfazer para uma determinada faceta. Se houver facetas de várias seleções, esse link desmarque todos os valores de facetas fornecidos. Dê um nome à faceta. Se a faceta não estiver selecionada no momento, o link será o caminho atual. </p> <p>Este é um exemplo do uso dessa tag: </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-long [gsname="facetname"]&gt; 
      &lt;guided-else-facet-long&gt;&lt;/guided-if-facet-long&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é verdadeira quando o número de valores de faceta está acima do limite de comprimento definido na configuração. Use-o para exibir uma faceta como um elemento diferente da interface do usuário (como uma lista truncada ou uma caixa de rolagem) quando a lista for muito longa. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="long_facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>Também é possível usar essa condição fora do contexto de um bloco nomeado <span class="codeph"> guided-facet </span> referenciando uma faceta específica diretamente por meio do uso do atributo <span class="codeph"> <span class="varname"> gsname </span> </span>. </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é verdadeira quando a faceta é clicada pelo menos uma vez e um valor de faceta é selecionado no momento. Ele pode ser usado para mostrar ou ocultar tags HTML ou gs , dependendo se uma faceta é clicada. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Também é possível usar essa condição fora do contexto de um bloco nomeado <span class="codeph"> guided-facet </span> referenciando uma faceta específica diretamente por meio do uso do atributo <span class="codeph"> gsname </span>. </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-single [gsname="facetname"]&gt; 
      &lt;guided-else-facet-single&gt;&lt;/guided-if-facet-single&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é verdadeira quando há apenas um valor de faceta. Ele pode ser usado para alterar a exibição da faceta quando não tem capacidade de refinar os resultados. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>Também é possível usar essa condição fora do contexto de um bloco nomeado <span class="codeph"> guided-facet </span> referenciando uma faceta específica diretamente por meio do uso do atributo <span class="codeph"> <span class="varname"> gsname </span> </span>. </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-has-values [gsname="facetname"]&gt; 
      &lt;guided-else-facet-has-values&gt;&lt;/guided-if-facet-has-values&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição permite verificar se a faceta especificada tem algum valor. Você pode usá-lo para mostrar outra faceta em vez de vazia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera o número total de resultados que estão dentro de uma determinada faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname=" <span class="varname"> associated custom facet value </span>"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera a string de um valor associado à faceta. Você pode ter 0 ou mais campos associados a uma faceta. Ter campos associados é raro e ser compatível com isso, basta configurar o template de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-value gsname=" <span class="varname"> associated custom facet value </span>" /&gt;&lt;guided-else-facet-value&gt;&lt;/guided-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Testa se o valor da faceta tem um valor de campo associado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link&gt; valor  </span>"]+&gt;&lt;/guided-facet-link&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Cria um link ao redor da string de valor de faceta para o cliente clicar. O caminho é gerado automaticamente para limitar os resultados pelo valor de aspecto atual. Ele suporta a transmissão de qualquer atributo diretamente para a tag de âncora. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cria seu próprio link para um valor de faceta. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>Por padrão, o valor é URL escaped. Entretanto, é possível adicionar outra camada de codificação especificando qual modo de escape você deseja usar por meio do parâmetro escape. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-children&gt;&lt;/guided-facet-value-children&gt; </span> </p> </td> 
   <td colname="col2"> <p>Como <span class="codeph"> &lt;guided-facet-values&gt; </span> itera por cada valor de faceta, esta tag itera por todos os valores secundários de uma faceta aninhada. Dentro dessa tag, use as tags de faceta típicas para criar links, criar links para desfazer e exibir valores de faceta. Essa tag deve estar dentro de <span class="codeph"> &lt;guided-facet-values&gt; </span> porque faz o loop aninhado. </p> <p>Um exemplo de uso dessa tag é o seguinte: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&lt;guided-if-facet-value-has-children&gt; 
      &nbsp;&nbsp;&nbsp;&lt;guided-facet-value-children&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-facet-value-children&gt; 
      &nbsp;&nbsp;&lt;/guided-if-facet-value-has-children&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-has-children&gt; 
      &lt;guided-else-facet- 
      value-has-children&gt; 
      &lt;/guided-if-facet-value-has-children&gt; </code> </p> </td> 
   <td colname="col2"> <p>Testa se o valor da faceta atual tem valores filhos. Recomendado para usar antes de usar as tags <span class="codeph"> &lt;guided-facet-children&gt; </span>. A cláusula "else" é opcional. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-above-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-above-length-threshold&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Determina se o valor da faceta atual dentro do loop de valores de faceta está acima do limite de comprimento. Normalmente, é usado para exibir apenas valores abaixo do limite em uma faceta longa (a menos que o usuário tenha selecionado anteriormente um link "Ver mais" exibido abaixo da faceta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-equals-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-equals-length-threshold&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Determina se o valor da faceta atual no loop de valores de faceta é igual ao limite de comprimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Exibe um link para desfazer para um determinado valor de faceta selecionado. Use-o para exibir um link para desfazer ao lado de um valor de faceta selecionado. Como esse link desfazer apenas desfaz o valor selecionado em particular, ele é diferente de <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> que desmarca todos os valores selecionados. </p> <p> <p>Observação:  Se a faceta não tiver um comportamento de seleção múltipla, os dois links desfazer terão o mesmo comportamento. Ou seja, a faceta só pode ter um valor selecionado. </p> </p> <p>Se a faceta não estiver selecionada no momento, o link será o caminho atual. Use essa tag somente em um loop <span class="codeph"> guided-facet-values </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crie seu próprio link para desfazer o valor da faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crie seu próprio link para desfazer a faceta. </p> <p> Semelhante à tag <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> , exceto que fornece o caminho bruto para criar seu próprio link para desfazer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-matches facetname="facetname" value="value"&gt;&lt;guided-else-facet-value-matches&gt; 
      &lt;/guided-if-facet-value-matches&gt; </code> </p> </td> 
   <td colname="col2"> <p>Exiba o HTML condicionalmente quando a faceta em questão tiver o "valor" de valor único ou selecionado. Esse conjunto de tags geralmente é usado para exibir uma faceta com base no valor selecionado em outra faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-behavior gsname=" <span class="varname"> facetname </span>" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Determine o comportamento de uma faceta, como normal, aderente ou de várias seleções. É útil para clientes que recebem resultados XML e desejam alterar dinamicamente como a faceta é exibida com base em seu comportamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>O conteúdo que essa tag envolve é oculto ou revelado com base no estado de visibilidade da faceta. Se uma regra de negócios ocultar ou revelar a faceta diretamente, qualquer conteúdo dentro da faceta será oculto ou revelado. Não é necessário que essas tags contornem a faceta. </p> <p> Um uso comum para essa tag é ocultar o nome de exibição quando o nome estiver fora da faceta. A vinculação dessa tag ao redor do nome de exibição faz com que o nome desapareça quando a faceta estiver oculta. </p> <p>Essa tag substitui a zona e tem muitos dos mesmos benefícios de desempenho que o uso de zonas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Caminho {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

Consulte [Sobre navegação estrutural](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb&gt; breadcrumbname  </span>"]&gt;&lt;/guided-breadcrumb&gt; </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>A tag de loop da navegação estrutural. Qualquer conteúdo entre as tags de abertura e fechamento é repetido para cada número de consulta do estado atual. </p> <p>Se <span class="codeph"> <span class="varname"> gsname </span> </span> for omitido, a navegação estrutural chamada "default" será usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link&gt;&lt;/guided-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cria um link na navegação estrutural. O comportamento padrão é o comportamento "goto". Se o link se comportar de forma diferente, use o atributo opcional <span class="codeph"> <span class="varname"> gsname </span> </span> para especificar "remover" ou "soltar". Qualquer atributo incluído na tag é passado para a tag de âncora resultante. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag value imprime o valor transformado da iteração de navegação estrutural atual. Ele é usado somente no contexto de um bloco <span class="codeph"> guided-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag label gera um rótulo para um valor de navegação estrutural detalhando qual faceta foi selecionada para gerar esse item de navegação estrutural. Ela é usada somente no contexto de um bloco <span class="codeph"> guided-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;:&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <code> &lt;guided-if-breadcrumb-label&gt; 
      &lt;guided-else- 
      breadcrumb-label&gt; 
      &lt;guided-if-breadcrumb-label /&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa tag condicional é usada para exibir condicionalmente o conteúdo se o valor da navegação estrutural atual tiver um rótulo. É usado para exibir somente rótulos e conteúdo relacionado quando um rótulo realmente existe. Ela é usada somente no contexto de um bloco <span class="codeph"> guided-breadcrumb </span>. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Usado para criar seu próprio link de navegação estrutural. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Menus {#section_1D489ADF041F4351A66E5D5742125CA8}

Consulte [Sobre menus](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta é a tag do iterador de loop de valor de menu. Use o atributo <span class="codeph"> gsname </span> para identificar qual conjunto de itens de menu será exibido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link&gt;&lt;/guided-menu-item-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Fornece o URL para refinar a pesquisa atual para o item de menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>Normalmente, um menu é exibido em um controle selecionado em um modelo. Essa tag facilita a construção do controle selecionado, pois gera o HTML para gerar a opção do controle selecionado. </p> <p>Por exemplo, o seguinte bloco de código: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>Pode gerar HTML da mesma forma: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a string do valor associado ao menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a string do rótulo associado ao menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a string do caminho. Use a tag se desejar adicionar um parâmetro ao caminho e criar um link personalizado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Retorna 1 ou 0 indicando se o item de menu atual está selecionado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

As tags de navegação da página podem ser usadas para criar um conjunto de links que permitem que um usuário pague pelos resultados da pesquisa.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-pages&gt;&lt;/guided-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag de loop para a navegação da página. Qualquer conteúdo entre as tags de abertura e fechamento é repetido para cada página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cria um link na navegação da página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link gsname="first|prev|next|last|viewall|viewpages"&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cria um link para a primeira, a anterior, a próxima ou a última página. Também é possível criar um link para exibir todas as páginas em uma página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-number /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retorna uma string com o número de página atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags condicionais é verdadeiro se a página que está atualmente repetida estiver selecionada. Normalmente, é usado para exibir de forma diferente o número da página no controle de navegação da página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> Esse conjunto de tags condicionais é verdadeiro se a página atual tiver uma página anterior. Normalmente, é usado para exibir um link anterior na navegação da página, quando faz sentido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> Esse conjunto de tags condicionais é verdadeiro se a página atual tiver uma próxima página. Normalmente, é usado para exibir um link anterior na navegação da página, quando faz sentido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> Quando uma pesquisa retorna um grande conjunto de resultados, talvez você não queira oferecer a capacidade de exibir todos os resultados. Portanto, você pode usar esse conjunto de tags condicionais para determinar quando exibir o link Exibir todos . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>Você pode usar esse conjunto de tags condicionais para determinar quando exibir o link Exibir páginas . Normalmente, é usado para permitir que um cliente visualize determinadas páginas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10º </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guided-else-page-link&amp;gt;
    &amp;lt;/guided-if[-not]-page-link&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Testa se a navegação da página tem uma primeira página, página anterior, próxima página e assim por diante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11º </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-total /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retorna uma string com o número total de páginas de resultados de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>Use a tag <span class="codeph"> de paginação guiada </span> para definir uma área na qual todas as tags de paginação se relacionam a uma configuração de paginação específica caso você tenha poucas Configurações de navegação de página definidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13º </p> </td> 
   <td colname="col1"> <p> 

    next|last|viewall|viewall|viewpages]/&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Cria seu próprio link na navegação da página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14. </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Testa se a página mais alta na navegação da página é igual ao número total de páginas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15. </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Testa se a página mais baixa na navegação da página é igual à página mais baixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>Testa se há uma única página de resultados ou várias páginas de resultados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pesquisas recentes {#section_8CD907521F584257B475595B01A5964B}

Você pode usar tags de pesquisas recentes para criar um conjunto de links que permitem que um usuário execute rapidamente uma pesquisa anterior, como no exemplo a seguir:

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

Consulte [Configurando pesquisas recentes](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches&gt;&lt;/guided-recent-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag de loop para pesquisas recentes. Qualquer conteúdo entre as tags de abertura e fechamento é repetido para cada página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permite criar um link para uma pesquisa recente. Ele suporta a transmissão de qualquer atributo HTML diretamente para a tag âncora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar o caminho relativo do URL para uma pesquisa recente, em um loop <span class="codeph"> guided-recent-search </span>. Normalmente, você usaria <span class="codeph"> guided-recent-search-link </span>. No entanto, se você quiser criar seu próprio link, poderá usar essa tag. Este é um exemplo: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar o termo de consulta associado a uma pesquisa recente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-link&gt;&lt;/guided-recent-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite que você ofereça aos clientes a capacidade de apagar pesquisas salvas recentemente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o caminho que <span class="codeph"> &lt;guided-recent-search-clear-link&gt; </span> usa para que você possa criar seu próprio link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-recent-search&amp;gt;   &lt;/p>  &lt;/td>
<td colname="col2"> <p>Permite exibir as pesquisas recentes quando um cliente realizou uma pesquisa recente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Você quis dizer {#section_C1EB3B9D8E1242798A6E04609D1E3543}

Você pode usar as tags Você quis dizer para criar um conjunto de links para sugestões quando uma pesquisa não retornar resultados e o termo Pesquisa não estiver no dicionário da conta. Este é um exemplo de uso das tags Você quis dizer :

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

Consulte [Sobre você quis dizer](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestions&gt;&lt;/guided-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta é a tag de loop para fazer looping nas sugestões. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-link&gt;&lt;/guided-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cria um link para a sugestão fornecida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-suggestion-value /&gt; </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permite testar se há sugestões. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a string do caminho para a sugestão. Você pode usá-lo para criar sua própria tag de âncora. Normalmente, <span class="codeph"> guided-sugestion-link </span> é usado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Uma sugestão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-result-count /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Contagem de resultados para a sugestão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permite testar se a pesquisa automática por sugestão em resultados zero foi realizada, caso esse recurso esteja ativado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-suggestion-original-query /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a consulta original se a pesquisa automática foi executada. </p> <p>Exemplo de uso: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira se houver sugestões devido a uma contagem de resultados baixa, caso esse recurso esteja ativado. </p> <p>Este é um exemplo de uso dessa tag: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
      &nbsp;&nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;. 
      &nbsp;&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt; 
      &lt;/guided-if-suggestion-low-results&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Preencher automaticamente {#section_897316BEE1454E839A56B565CA4AF018}

As tags a seguir podem ser usadas para adicionar o preenchimento automático ao formulário de pesquisa. As tags head-content e form-content são necessárias para que a função de preenchimento automático funcione corretamente. Recomenda-se usar as tags em vez de codificar o Javascript e o CSS de preenchimento automático no modelo de apresentação. O motivo é que as tags permitem que seus modelos capturem quaisquer novas IDs de cache de derrota sempre que você alterar as configurações de preenchimento automático sem precisar atualizar manualmente o modelo.

Consulte [Sobre a Conclusão Automática](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-autocomplete&gt; &lt;guided-else-autocomplete&gt; &lt;/guided-if-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecta se o recurso de preenchimento automático está ativado. Você poderia usar as tags para, opcionalmente, coletar o cabeçalho e o conteúdo do formulário necessários para o preenchimento automático. Por sua vez, isso permite que você ative e desative o recurso e não precise alterar os modelos de apresentação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Usado no cabeçalho do modelo de apresentação e substituído pelo script CSS apropriado inclui para preenchimento automático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Usado no formulário de pesquisa (entre as tags <span class="codeph"> &lt;form&gt; </span> e <span class="codeph"> &lt;/form&gt; </span> ) do modelo de apresentação, em vez de codificar as tags de preenchimento automático no formulário. As tags são substituídas pelo HTML apropriado que é necessário para fazer o preenchimento automático funcionar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera os links para o JavaScript de preenchimento automático. Para melhor desempenho, é recomendável colocar essa tag perto da parte inferior da página antes de fechar a tag "body" . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Armazenar {#section_A33E25DB5E67404A823BD9618665B773}

Use as tags a seguir para testar e exibir a loja em que um usuário está no momento.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-store /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera a loja atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store-defined&gt; &lt;guided-else-store-defined&gt; &lt;/guided-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecta se o usuário está em uma loja. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store gsname="store"&gt; &lt;guided-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecta se o usuário está no armazenamento que o parâmetro <span class="codeph"> gsname </span> especifica. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zonas {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-zone gsname="zone area"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Você pode envolver qualquer conteúdo em tags de zona para criar uma zona fora dessa área. Isso permite usar regras comerciais para exibir a zona conforme necessário. Por padrão, as zonas são sempre exibidas. Você pode usar os parâmetros de pesquisa e de faceta opcionais para indicar qual pesquisa ou faceta está associada à zona. Essa funcionalidade permite que o software ignore pesquisas ou facetas quando uma zona está oculta, melhorando o desempenho do tempo de pesquisa. Os atributos de altura e largura são opcionais e são usados para configurar como o espaço reservado é exibido no Construtor visual de regras quando uma zona é removida. </p> <p> Use a tag <span class="codeph"> guided-if-facet[-not]-visible </span> em vez da zona onde for possível. Ele simplifica o modelo de apresentação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone area"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags permite o teste se uma zona estiver sendo exibida no momento. É útil quando você tem conteúdo em outro lugar da página que deseja exibir apenas quando a zona for exibida. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Indicadores de loop {#section_387322CA0AA843A2ACF2795C328673E9}

Você pode usar cada um dos seguintes indicadores de loop em qualquer um desses blocos de loop:

* resultados guiados
* valores de faceta guiada
* navegação estrutural guiada
* itens de menu guiado
* páginas guiadas

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira quando a iteração atual é a primeira iteração do loop. Isso não significa necessariamente o primeiro resultado ou a primeira página, mas o primeiro mostrado. Se o visitante do site estiver na página 2 de um conjunto de resultados que seja 10 por página, a primeira iteração será resultado 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira quando a iteração atual é a última iteração do loop. Isso não significa necessariamente o último resultado ou a última página, mas o último mostrado no contexto atual (página). Se o visitante do site estiver na página 1 de um conjunto de resultados que contém 200 resultados, mas apenas 10 resultados por página, a última iteração será resultado 10 em vez de resultado 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira quando a iteração atual é uma iteração ímpar do loop (versus uma iteração par). Isso é útil para exibir cores de linha variáveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira quando a iteração atual é uma iteração par do loop (versus uma iteração ímpar). Isso é útil para exibir cores de linha variáveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira quando a iteração atual é uma iteração par do loop. Isso é útil para exibir cores de linha variáveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclui o texto entre eles se a iteração atual não for a primeira ou a última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclui o texto entre eles se a iteração atual for a primeira ou a última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Um número inteiro (começando em 0) cujo valor é incrementado para cada iteração do loop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Um número inteiro (começando em 1) cujo valor é incrementado para cada iteração do loop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Idioma Diverso {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

As tags a seguir estão disponíveis para permitir que você faça coisas mais avançadas com seu modelo, como criar sua própria mini faceta.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-current-path&gt; </span> </p> </td> 
   <td colname="col2"> <p>Fornece o caminho atual usado. Normalmente, é usado para criar um link que adiciona um novo parâmetro à pesquisa existente. Por padrão, o caminho é URL escapado. Você pode especificar qual modo de escape deseja usar por meio do parâmetro escape. </p> <p>Exemplo: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>Neste exemplo, uma regra de processamento de pesquisa usa lang para selecionar a versão em francês. </p> <p>O caminho atual sempre tem pelo menos um parâmetro de consulta. Se não houver nenhum outro parâmetro de consulta, ele será definido como <span class="codeph"> q=* </span> facilitando a adição de mais parâmetros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> Caminho básico  </span> </p> </td> 
   <td colname="col2"> <p> Se quiser criar um link usando o basepath, use <span class="codeph"> / </span> no início do <span class="codeph"> href </span> e adicione parâmetros. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-query-param gsname="query_parameter"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar o valor existente de um parâmetro de consulta que está no URL. Se o seu parâmetro não existir, essa tag retornará uma string vazia. Se você não especificar uma opção de escape a sequência de caracteres retornada é automaticamente um escape HTML, você pode especificar um escape de HTML ou URL. </p> <p>Exemplo: </p> <p> 

    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;q&quot;&amp;nbsp;/&amp;gt;
    dá&amp;nbsp;o&amp;nbsp;value&amp;nbsp;calças
    
    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;lang&quot;&amp;nbsp;/&amp;gt;
    dá nbsp;você&amp;nbsp;o&amp;nbsp;value&amp;nbsp;en
    
    &amp;lt;guided-query-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/&amp;gt;
    dá&amp;nbsp;an&amp;nbsp;empty&amp;nbsp;string
    &amp;nbsp;
    &amp;nbsp;nbsp; nbsp; bsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;   &lt;/p>  &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-query-param-name gsname="param#" offset="offset_number" /&gt; </span> </p> </td> 
   <td colname="col2"> <p>A Pesquisa guiada tem a noção de um número de consulta, que é usado no controle de navegação estrutural. <span class="codeph"> guided-query-param-name  </span> permite definir parâmetros como parte de um link no modelo de apresentação, onde a Pesquisa guiada calcula o número de consulta correto para você. O <span class="codeph"> gsname </span> contém um "x", que a Pesquisa guiada substitui pelo número correto. O valor de deslocamento pode ser 0 - 15, onde 0 indica que o próximo número de consulta disponível é usado. Um 1 indica que você deseja adicionar 1, e assim por diante. </p> <p>Combinado com <span class="codeph"> guided-current-path </span>, você pode criar seu próprio link de mini faceta ou permitir um nível de detalhamento adicional. </p> <p>Exemplo: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="q#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="x#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category"&nbsp;&gt;Category:Men&lt;/a&gt;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code> </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=Jeans&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=product-type"&nbsp;&gt;Cat:Men&nbsp;-&nbsp;Product:Jeans&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-include gsfile="filename" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Permite incluir outros arquivos de modelo. Essa funcionalidade significa que você pode criar vários modelos usando submodelos como módulos. </p> <p>No exemplo a seguir, os arquivos <span class="filepath"> de navegação estrutural </span> e <span class="filepath"> facetas </span> são incluídos: </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>As inclusões dinâmicas não são compatíveis. Em outras palavras, <span class="codeph"> gsfile </span> não pode ser uma variável. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p> Identifica quanto tempo a pesquisa demorou. O valor de tempo de pesquisa retornado é especificado em ms. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retorna a contagem de pesquisas de núcleos usadas para criar a página de resultados de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-if-fall-through-search&gt;&lt;/guided-if-fall-through-search&gt; </span> </p> </td> 
   <td colname="col2"> <p>Testa se a contagem de pesquisas principais é maior que uma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira quando a iteração atual é uma iteração par do loop (versus uma iteração ímpar). Isso é útil para exibir cores de linha variáveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Essa condição é verdadeira quando a iteração atual é uma iteração par do loop. Isso é útil para exibir cores de linha variáveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclui o texto entre eles se a iteração atual não for a primeira ou a última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Inclui o texto entre eles se a iteração atual for a primeira ou a última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13º </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permite verificar se você está ou não na pesquisa inicial (a consulta foi o resultado de uma pesquisa na caixa de pesquisa). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14. </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Você pode usar essa tag no modelo para salvar você da codificação rígida da ação do formulário de pesquisa. Ele detecta quando você está no ambiente Preparado ou Ao vivo e as alterações são feitas de forma correspondente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15. </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-query-param-defined gsname="query_parameter"&gt; &lt;guided-else-query-param-defined&gt; &lt;/guided-if-query-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags permite testar quais parâmetros de CGI são definidos no caminho de pesquisa. Você pode testar os valores dos parâmetros somente se eles estiverem definidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-query-number&gt; </span> </p> </td> 
   <td colname="col2"> <p>O mecanismo de pesquisa guiada que direciona o modelo tem a noção de números de consulta flutuantes em que cada novo link gerado pelo mecanismo usa o próximo número de consulta disponível. Essa tag permite que você capture o próximo número ou deslocamentos da consulta para que possa criar links personalizados que aprofundem o conjunto de resultados. Offset permite deslocar para o próximo número de query. Por exemplo, se você selecionou uma faceta, o próximo número da consulta é 2, com um deslocamento de 1, o número da consulta retornado é 3. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar o valor existente de uma variável personalizada que suas regras de processamento definem. Se você não especificar uma opção de escape a cadeia de caracteres retornada é um escape HTML automático, poderá especificar <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span> ou <span class="codeph"> 0 </span>. Se você usar uma regra de processamento para copiar um parâmetro CGI de entrada para uma variável personalizada e, em seguida, exibir ou usar essa variável no modelo com escape definido como nenhum ou js, será possível criar uma vulnerabilidade XSS na pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Habilita o teste se uma variável personalizada estiver definida nas regras de processamento (limpeza de consulta, processamento pré-pesquisa e processamento pós-pesquisa). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="searchname" field="fieldname"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite exibir o conteúdo de um campo geral definido no template de transporte. Se você não especificar uma opção de escape, a cadeia de caracteres retornada será codificada no formato especificado no modelo de transporte para esse campo. A especificação de uma opção de escape se aplica sobre qualquer formato em que você estiver codificando o campo como no modelo de transporte. Você pode especificar <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span> ou <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="searchname" field="fieldname"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite o teste se o conteúdo de um campo geral, conforme definido no modelo de transporte, existir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar o valor de um cookie, supondo que o cookie esteja disponível. Se você não especificar uma opção de escape a cadeia de caracteres retornada é um escape HTML automático, poderá especificar <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span> ou <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Habilita o teste se houver um cookie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="banner area"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera o banner para uma determinada área. Os atributos opcionais de largura e altura são usados no Construtor visual de regras para permitir a exibição de um espaço reservado significativo para permitir que os usuários selecionem um banner. Por padrão, os banners não são escapados. Em vez disso, você deseja inserir HTML no template de apresentação. No entanto, se você estiver criando um modelo JSON, considere usar a opção de escape js . </p> <p>Exemplo: </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="banner area"&gt; &lt;guided-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ativa o teste se uma área de banner estiver definida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25. </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-mode&gt; &lt;guided-else-simulator-mode&gt; &lt;/guided-if-simulator-mode&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite detectar quando você está visualizando sua pesquisa no Simulador ou no Construtor visual de regras. Normalmente, é usado para exibir informações de depuração adicionais para você. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rules&gt; &lt;guided-else-tnt-business-rules&gt; &lt;/guided-if-tnt-business-rules&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite detectar se você tem alguma regra comercial referenciando uma campanha <span class="keyword"> Adobe Target </span>. Normalmente, é usada como parte da integração com <span class="keyword"> Adobe Target </span> para evitar a ocorrência dos servidores <span class="keyword"> Target </span> quando não é necessário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Por padrão, os redirecionamentos são executados automaticamente. No entanto, se você configurou pesquisa/merchandising do site para retornar uma resposta XML ou JSON ao seu aplicativo da Web, é possível optar por analisar a resposta 302/301 no aplicativo da Web ou enviar o redirecionamento para você como parte do conjunto de resultados. Se você estiver transmitindo o redirecionamento como parte do conjunto de resultados, essa tag poderá ser usada no modelo para exibir o local de redirecionamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Quando você configura a pesquisa/comercialização do site para redirecionar redirecionamentos no conjunto de resultados, esse conjunto de tags pode ser usado para determinar se há um redirecionamento para a saída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-lt /&gt; &lt;guided-gt /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags permite que você incorpore tags de modelo guiadas em atributos HTML. </p> <p>Exemplo: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags de modelo de transporte {#reference_227D199F5A7248049BE1D405C0584751}

Os modelos de transporte são modelos XML que passam dados da pesquisa de backend para a camada de apresentação da Pesquisa guiada.

<!-- 

r_transport_template_tags.xml

 -->

Na camada de apresentação, você pode ter um único modelo de apresentação que apresente os resultados de várias pesquisas. Cada pesquisa pode usar o mesmo modelo de transporte ou um modelo de transporte personalizado para passar os dados para a camada de apresentação.

Como o modelo de transporte é usado apenas para transmitir dados para a camada de apresentação, ele não tem nenhum HTML preocupado com a exibição dos resultados de pesquisa. O modelo de transporte usa tags XML de modelo de transporte para transmitir os resultados da pesquisa para preencher os componentes de Pesquisa guiada, como facetas, navegação estrutural e menus. Dentro dessas tags, as tags de modelo de pesquisa padrão são usadas para exibir os valores reais.

Consulte [Edição de uma apresentação ou de um modelo de transporte](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

Consulte [Pesquisar marcas de modelo](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tag do modelo de transporte </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>As tags XML raiz que a camada de apresentação usa para detectar o que é analisado do modelo de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>As tags delimitam as tags do modelo de pesquisa que fornecem dados de resumo com base no conjunto de resultados. Normalmente, essas tags contêm tags de pesquisa para o número total de resultados, resultado menor e resultado mais alto. Você pode definir qualquer número de campos globais adicionais desejados com a tag <span class="codeph"> de campo geral </span> , como no exemplo a seguir: </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>As tags são vinculadas aos resultados da pesquisa, de modo que a Pesquisa guiada saiba onde procurá-las. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>As tags são vinculadas a cada resultado de pesquisa, de modo que a Pesquisa guiada reconheça onde o conteúdo de um único resultado de pesquisa começa e termina, como no exemplo a seguir: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite executar um loop por cada item em uma lista de vários valores para um único resultado. Use essa tag somente em um resultado. Sua finalidade é permitir a iteração sobre atributos que pertencem a um campo de resultado, como no exemplo a seguir: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>Transmite os resultados que preenchem as facetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;dynamic-facet&gt;&lt;/dynamic-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Você pode designar uma faceta como uma faceta dinâmica e como membro de um painel de facetas. No entanto, seu tratamento é independente em relação às tags de modelo de apresentação relacionadas. </p> <p>Em outras palavras, o aninhamento de um contexto de loop do painel de facetas em um contexto de loop de facetas dinâmico, ou vice-versa, não é permitido. </p> <p>Para facetas dinâmicas e retornadas, somente as facetas dinâmicas que foram retornadas para uma determinada pesquisa são visíveis no contexto de loop do painel de facetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Cada faceta tem suas próprias tags de faceta, onde o parâmetro name corresponde ao nome da faceta. As tags de pesquisa são usadas nas tags de faceta para os valores de faceta, como no exemplo a seguir: </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> As contas que usam facetas com slot podem usar a tag dinâmica e a tag de nomes para exibição. Ambas as tags ajudam a facilitar o mapeamento entre facetas com slot e aspectos reais ao criar regras de negócios. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>O atributo <span class="codeph"> separator </span> permite alterar o delimitador usado ao gerar dados de campo de exibição de pesquisa para listas. O padrão é uma vírgula. </p> <p>Geralmente, o delimitador usado deve ser algo que não aparece imediatamente no conteúdo do campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p> Encapsule suas sugestões de Você quis dizer com as tags para que a Pesquisa guiada reconheça quais nós XML contêm sugestões. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">Sobre você quis dizer</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Vincule cada sugestão Você quis dizer com tags, como no exemplo a seguir: </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p>Consulte <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">Sobre você quis dizer</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pesquisar tags de modelo {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

Um modelo de pesquisa é um arquivo HTML que inclui tags de modelo definidas por pesquisa/comercialização do site. Essas tags indicam como os resultados da pesquisa são formatados. A referência a seguir contém uma breve descrição de cada tag de modelo de pesquisa e seus atributos.

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>Use somente as tags do modelo de pesquisa nos arquivos do modelo de transporte (.tpl).

Você pode selecionar entre os seguintes grupos de tags de modelo de pesquisa e material de referência.

As tags válidas somente no loop de resultados incluem o seguinte:

* [Sobre as tags de loop Resultados](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [Tags de string de loop de resultados](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Tags condicionais do loop de resultados](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Tags de link da âncora do loop de resultados](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Tags condicionais de posição de loop](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

As tags válidas em todo o modelo incluem o seguinte:

* [Tags da lista de valores do campo](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [Tags de loop da lista de valores do campo](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [Sugerir tags](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [Tags de string de modelo](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [Tags de link de âncora do modelo](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [Tags condicionais do modelo](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [Tags de controle de formulário de modelo](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

Tópicos de referência do modelo de pesquisa

* [Sequências de caracteres do formato de data](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [Identificadores de idioma](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [Especificação do cabeçalho HTTP do tipo de conteúdo](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [Especificação de um conjunto de caracteres em um modelo HTML](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [Especificação de um conjunto de caracteres em um modelo XML](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [Inclusão de um modelo de pesquisa em outro](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## Sobre as tags de loop Resultados {#section_D4DC7B4560144663972E8DBC3369C629}

A tag de loop de resultados é o método de trabalho do sistema de modelo. Quando a tag é encontrada durante uma pesquisa, o HTML é repetido e outras tags entre as tags de loop de resultados inicial e final, substituindo quaisquer outras tags pelos resultados da pesquisa.

`<search-results> ... </search-results>`

As tags de loop de resultados rodam o HTML que mostra os resultados da pesquisa. O HTML entre as tags é repetido para cada resultado e é exibido na página.

As tags a seguir são válidas somente no loop de resultados:

* [Tags de string de loop de resultados](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Tags condicionais do loop de resultados](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Tags de link da âncora do loop de resultados](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Tags condicionais de posição de loop](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## Tags de sequência de loop de resultados {#section_80D68334E8D04A33937A6E58ABAAA320}

As tags a seguir retornam uma string.

Consulte [Sobre as tags de loop de Resultados](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o índice numérico do resultado atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o título da página do resultado atual. O atributo de comprimento opcional é usado para limitar o comprimento das sequências de caracteres exibidas, com um padrão de 80 caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-bodytext length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o texto do corpo, começando na parte superior da página. Os termos relevantes são mostrados em negrito. O atributo de comprimento opcional é usado para limitar o comprimento das sequências de caracteres exibidas, com um padrão de 80 caracteres. O atributo de codificação é opcional e pode codificar caracteres de saída com codificação HTML (padrão), codificação Javascript, codificação Perl ou nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Retorna a descrição do resultado atual. Se a meta tag de descrição existir e o atributo de conteúdo não estiver vazio, esse texto será exibido. Caso contrário, o início do texto do corpo da página será exibido. O atributo de comprimento opcional é usado para limitar o comprimento das sequências de caracteres exibidas, com um padrão de 80 caracteres. </p> <p>O atributo <span class="codeph"> opcional de codificação </span> controla se a saída é codificada em HTML, codificada em JavaScript, Codificada em Perl, codificada em URL ou não, para saída na página de resultados. O valor padrão da codificação <span class="codeph"> </span> é <span class="codeph"> html </span>. Normalmente, não é necessário especificar o atributo de codificação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-score rank="dynamic/static/dynamic-raw/static-raw/final-raw" precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a pontuação do resultado atual, que é um número 0 - 100. Se você tiver definido um campo de classificação em <span class="uicontrol"> Opções </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>, poderá exibir a classificação de página dinâmica definindo o atributo de classificação como dinâmico ( <span class="codeph"> &lt;search-score rank="dynamic"&gt; </span>). Você pode exibir a classificação de página estática definindo o atributo de classificação como estático ( <span class="codeph"> &lt;search-score rank="static"&gt; </span>). Você pode usar o atributo de precisão opcional para especificar o número de casas decimais a serem exibidas. O padrão é 0, que exibe a pontuação inteira). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a data do resultado atual. O valor de texto opcional "nenhum" será exibido se não houver uma data associada ao resultado atual. Se o valor opcional "nenhum" não for fornecido, o texto "Nenhuma data" será exibido se não houver uma data associada ao resultado atual. </p> <p>O atributo "date-format" tem uma cadeia de caracteres de formato de data no estilo UNIX, como "%A, %B %d, %Y" (para "segunda-feira, 25 de julho de 2016"). O padrão "gmt" é "yes" e controla se a parte de tempo da string de data deve ser saída em GMT ("yes") ou no fuso horário da conta ("no"). </p> <p>O atributo "language" controla o idioma e as convenções de localidade da string de data de saída. "0" (padrão) significa "Usar idioma da conta". "2" significa "Usar Idioma do Documento". O valor "language" "1" é reservado para uso futuro. Qualquer outro valor de "idioma" é interpretado como um identificador de idioma específico, por exemplo, "en_US" significa "inglês (Estados Unidos)". </p> <p>O atributo de comprimento opcional é usado para limitar o comprimento das sequências de caracteres exibidas, com um padrão de 80 caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o tamanho do resultado atual em bytes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o URL do resultado atual. </p> <p>Use o atributo opcional <span class="codeph"> length </span> para limitar o comprimento das sequências de caracteres exibidas, com um padrão de caracteres ilimitados. </p> <p>O atributo <span class="codeph"> de codificação </span> é opcional e pode codificar caracteres de saída com codificação HTML, codificação Javascript, codificação Perl ou nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-query length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna as partes do caminho e da consulta, incluindo o ponto de interrogação do URL do resultado atual. </p> <p>Use o atributo opcional <span class="codeph"> length </span> para limitar o comprimento das sequências de caracteres exibidas, com um padrão de caracteres ilimitados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna a próxima linha de contexto do termo de pesquisa. Os termos relevantes são mostrados em negrito. Chame essa tag repetidamente para exibir mais de uma linha de contexto para o resultado atual. </p> <p>Use o atributo opcional <span class="codeph"> length </span> para limitar o comprimento das sequências de caracteres exibidas, com um padrão de 80 caracteres. O atributo <span class="codeph"> length </span> é ignorado se essa tag for colocada por conjuntos de tags <span class="codeph"> &lt;search-if-context&gt; </span> ou <span class="codeph"> &lt;search-if-any-context&gt; </span> que contêm um atributo de comprimento. </p> <p>O atributo <span class="codeph"> de codificação </span> é opcional e pode codificar caracteres de saída com codificação HTML (padrão), codificação Javascript, codificação Perl ou nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quotes="yes/no" commas="yes/no" units="miles/kilometers" separator="|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag avançada exibe o conteúdo do campo de metadados (url, título, desc, chaves, target, corpo, alt, data, charset e idioma ou campos definidos em <span class="uicontrol"> Opções </span> &gt; <span class="uicontrol"> Metadados </span> &gt; Definições) especificados no atributo <span class="codeph"> name </span>, para o resultado atual. Por exemplo: </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>Gera o título da página para um resultado de pesquisa. Se o atributo opcional <span class="codeph"> nenhum </span> for especificado, seu valor será exibido na página de resultados somente se não houver conteúdo associado ao campo. </p> <p>Os atributos <span class="codeph"> date-format </span>, <span class="codeph"> gmt </span> e <span class="codeph"> language </span> só são relevantes se o tipo de conteúdo do campo especificado for <span class="codeph"> date </span>. </p> <p>O atributo <span class="codeph"> date-format </span> tem uma cadeia de caracteres de formato de data no estilo UNIX como <span class="codeph"> %A, %B %d, %Y </span> (para segunda-feira, 25 de julho de 2016). <span class="codeph"> o gmt  </span> assume como padrão  <span class="codeph"> sim  </span> e controla se a parte de tempo da string de data é saída em GMT (  <span class="codeph"> sim  </span>) ou o fuso horário da conta (  <span class="codeph"> não  </span>). </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Sequências de caracteres do formato de data</a>. </p> <p>O atributo <span class="codeph"> de idioma </span> controla as convenções de idioma e localidade da string de data de saída. <span class="codeph"> 0  </span> (padrão) significa "Usar idioma da conta". <span class="codeph"> 2  </span> significa "Usar idioma do documento". O valor <span class="codeph"> do idioma </span> <span class="codeph"> 1 </span> é reservado para uso futuro). Qualquer outro valor <span class="codeph"> de idioma </span> é interpretado como um identificador de idioma específico, por exemplo, <span class="codeph"> en_US </span> significa "Inglês (Estados Unidos)". </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificadores de idioma</a>. </p> <p>O atributo opcional <span class="codeph"> length </span> é usado para limitar o comprimento das sequências de caracteres exibidas, com um padrão de 80 caracteres. </p> <p>O atributo <span class="codeph"> opcional de codificação </span> controla se a saída é codificada em HTML, codificada em JavaScript, Codificada em Perl, codificada em URL ou não, para saída na página de resultados. O valor padrão da codificação <span class="codeph"> </span> é <span class="codeph"> html </span>. Normalmente, não é necessário especificar o atributo de codificação. </p> <p>O atributo <span class="codeph"> opcional aspas </span> controla se a saída dos itens individuais é rodeada por aspas duplas (ou aspas simples, se <span class="codeph"> encoding=perl </span>). O valor padrão de <span class="codeph"> aspas </span> é <span class="codeph"> não </span>. </p> <p>O atributo opcional <span class="codeph"> de vírgulas </span> controla se a saída de itens individuais é separada por vírgulas. O valor padrão de <span class="codeph"> vírgulas </span> é <span class="codeph"> sim </span>. O atributo <span class="codeph"> de vírgulas </span> é ignorado para campos de tipo não listado. </p> <p>O atributo <span class="codeph"> unidades </span> opcional controla as unidades de distância aplicadas a um campo de saída de pesquisa de proximidade. O valor padrão de <span class="codeph"> unidades </span> é determinado a partir da configuração "Unidades padrão" do campo de tipo de local associado ao campo de saída de pesquisa de proximidade especificado. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Sobre pesquisa de proximidade</a>. </p> <p>O atributo <span class="codeph"> separator </span> opcional define o caractere único, ou delimitador, que é inserido entre os valores da saída para campos de tipo de lista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt; ...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag cria um loop para enumerar valores de campos de metadados (url, título, desc, chaves, target, corpo, alt, data, charset e idioma ou campos definidos em <span class="uicontrol"> Opções </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>) para o resultado atual. Não aninhe esta tag dentro de outra tag <span class="codeph"> &lt;search-display-field-values&gt; </span> . O atributo <span class="codeph"> name </span> especifica o nome do campo que contém os valores a serem enumerados. Essa tag é mais útil com campos que têm o atributo <span class="uicontrol"> Lista de permissões </span> marcado (em <span class="uicontrol"> Opções </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag gera o valor do campo de metadados (url, título, desc, chaves, target, corpo, alt, data, charset e idioma ou campos definidos em <span class="uicontrol"> Opções </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>) para a iteração de loop <span class="codeph"> &lt;search-display-field-values&gt; </span> atual. Esta tag só é válida dentro de um loop <span class="codeph"> &lt;search-display-field-values&gt; </span>. Os atributos <span class="codeph"> date-format </span>, <span class="codeph"> gmt </span> e <span class="codeph"> language </span> só são relevantes se o tipo de conteúdo do nome do campo especificado na tag <span class="codeph"> &lt;search-display-field-values&gt; </span> de inclusão for <span class="codeph"> date </span>. O atributo <span class="codeph"> date-format </span> pega uma cadeia de caracteres de formato de data no estilo UNIX como <span class="codeph"> "%A </span>, <span class="codeph"> %B </span> <span class="codeph"> %d </span>, <span class="codeph"> %Y </span>" (para "segunda-feira, 25 de julho de 2016"). O atributo <span class="codeph"> gmt </span> assume como padrão <span class="codeph"> sim </span> e controla se a parte de tempo da cadeia de data é de saída em GMT ( <span class="codeph"> sim </span>) ou o fuso horário da conta ( <span class="codeph"> não </span>). </p> <p>O atributo <span class="codeph"> de idioma </span> controla as convenções de idioma e localidade da string de data de saída. <span class="codeph"> 0  </span> (padrão) significa "Usar idioma da conta". Qualquer outro valor <span class="codeph"> de idioma </span> é interpretado como um identificador de idioma específico, por exemplo, <span class="codeph"> en_US </span> significa "Inglês (Estados Unidos)". </p> <p>O atributo <span class="codeph"> opcional de codificação </span> controla se a saída é codificada em HTML, codificada em JavaScript, Codificada em Perl, codificada em URL ou não, para saída na página de resultados. O valor padrão da codificação <span class="codeph"> </span> é <span class="codeph"> html </span>. Normalmente, não é necessário especificar o atributo de codificação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14. </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera o número total de valores no resultado atual para o campo de metadados (url, título, desc, chaves, target, corpo, alt, data, charset e idioma ou campos definidos em <span class="uicontrol"> Opções </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>) especificado com o atributo de nome. Essa tag pode aparecer em qualquer lugar no loop de resultados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15. </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera o contador ordinal (1, 2, 3 e assim por diante) para a iteração de loop <span class="codeph"> &lt;search-display-field-values&gt; </span> atual. Esta tag só é válida dentro de um loop <span class="codeph"> &lt;search-display-field-values&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inicia um contexto de loop para qualquer campo de aspecto dinâmico retornado para esta pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera o nome do campo de faceta dinâmica atual, para essa iteração de loop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18º </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Gera informações relacionadas à colocação do resultado atual, por exemplo, quaisquer ações baseadas em resultados que afetaram a posição do resultado. </p> <p>O formato de saída dessa tag é JSON, como no exemplo a seguir: </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>O atributo <span class="codeph"> de codificação </span> é opcional; o valor padrão é <span class="codeph"> html </span>. </p> <p> <p>Observação:  Esta tag só tem saída se <span class="codeph"> sp_trace=1 </span> for especificado com os parâmetros de consulta de pesquisa principais. </p> </p> <p>Consulte a linha 48 na tabela localizada em <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> Backend search CGI parameters</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags condicionais do loop de resultados {#section_35C367969E384A06A9865E388F1F9360}

As tags a seguir incluem condicionalmente o HTML entre elas.

Consulte [Sobre as tags de loop de Resultados](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt; ...  &lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt; ...  &lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o HTML entre elas se a próxima chamada para <span class="codeph"> &lt;search-title&gt; </span> retornar (ou não retornar) o texto do título do documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt; ... /search-if-description&gt;  </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt; ...  &lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> Essas tags incluem o HTML entre elas se a próxima chamada para <span class="codeph"> &lt;search-description&gt; </span> retornar (ou não retornar) o texto da descrição do documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bodytext&gt; ...  &lt;/search-if-bodytext&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bodytext&gt; ...  &lt;/search-if-not-bodytext&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o HTML entre elas se a próxima chamada para <span class="codeph"> &lt;search-body-text&gt; </span> retornar (ou não retornar) o texto do corpo do documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt; ...  &lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt; ...  &lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o HTML entre elas se a próxima chamada para <span class="codeph"> &lt;search-context&gt; </span> retornar (ou não retornar) uma string de contexto não vazia. O atributo length substitui o atributo length em qualquer tag <span class="codeph"> &lt;search-context&gt; </span> fechada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; ... /search-if-any-context&gt;  </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt; ...  &lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o HTML entre elas se houver (ou não) uma string de contexto associada ao resultado. O atributo length substitui o atributo length em qualquer tag <span class="codeph"> &lt;search-context&gt; </span> fechada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" upper="yy" rank="dynamic/static/dynamic-raw/static-raw/final-raw"&gt; ...  &lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower="XX" upper="yy" rank="dynamic/static"&gt; ...  &lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o HTML entre elas se a pontuação do resultado atual for (ou não for) entre XX e YY. Útil para adicionar marcadores ou gráficos para mostrar a relevância do resultado. Se você tiver definido um campo de tipo de classificação em <span class="uicontrol"> Opções </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>, poderá verificar a classificação de página dinâmica definindo o atributo de classificação como dinâmico ( <span class="codeph"> &lt;search-if-score rank="dynamic" lower=XX upper=YY&gt; </span>). Você pode verificar a classificação de página estática definindo o atributo de classificação como estático ( <span class="codeph"> &lt;search-if-score rank="static" lower=XX upper=YY&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt; ...  &lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt; ...  &lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags avançadas incluem o HTML entre elas com base no fato de o campo especificado no atributo "name" ter ou não conteúdo. Se o atributo "valor" opcional for especificado, as tags incluirão o HTML entre elas, com base no fato de o valor especificado corresponder (ou não) ao valor do campo no resultado atual. Essas tags funcionam somente no loop de resultados (entre <span class="codeph"> &lt;search-results&gt; </span> e <span class="codeph"> &lt;/search-results&gt; </span> tags). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags de link da âncora de loop de resultados {#section_C5FAEF520E9E42ADAD1F90651922AA02}

Consulte [Sobre as tags de loop de Resultados](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ...  &lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse par de tags cria um link de âncora em torno do HTML entre elas. Quando o link é clicado, a página de resultados é exibida. Um atributo de destino opcional especifica a janela nomeada na qual os navegadores compatíveis com quadros devem exibir a página de resultados. </p> <p>Defina o atributo hbx-enable como "sim" para aproveitar as vantagens da análise disponível por meio do HBX. Defina hbx-linboy-name com o nome de um campo Meta-data que você gostaria de rastrear. Por exemplo, para rastrear os resultados da pesquisa por número de SKU, defina hbx-linboy-name como o nome do campo Meta-data que contém as informações de SKU. </p> <p>Campos do tipo data não são suportados no momento. O valor de hbx-linboy-name é anexado à ID do link na âncora gerada. O valor do atributo hbx-linboy-none é anexado à ID do link sempre que o campo Metadados nomeado estiver vazio. O valor de hbx-linboy-length limita o número de caracteres obtidos e exibidos da tag Meta. O número padrão de caracteres é 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link target="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt; ...  &lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse par de tags é semelhante às tags <span class="codeph"> &lt;search-link&gt; ... &lt;/search-link&gt; </span> . Quando os links de âncora gerados são clicados, a página de resultados é exibida, mas com a página rolada para a tag de âncora mais próxima antes do resultado. Para links de PDF, o visualizador do Acrobat exibe a página que contém o resultado. Um atributo de destino opcional especifica a janela nomeada na qual os navegadores compatíveis com quadros devem exibir a página de resultados. </p> <p>Defina o atributo hbx-enable como "sim" para aproveitar as vantagens da análise disponível por meio do HBX. Defina hbx-linboy-name com o nome de um campo Meta-data que você gostaria de rastrear. Por exemplo, para rastrear os resultados da pesquisa por número de SKU, defina hbx-linboy-name como o nome do campo Meta-data que contém as informações de SKU. </p> <p>Campos do tipo data não são suportados no momento. O valor de hbx-linboy-name é anexado à ID do link na âncora gerada. O valor do atributo hbx-linboy-none é anexado à ID do link sempre que o campo Metadados nomeado estiver vazio. O valor de hbx-linboy-length limita o número de caracteres obtidos e exibidos da tag Meta. O número padrão de caracteres é 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt; ...  &lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt; ...  &lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o HTML entre elas se um atributo de valor especificar uma extensão que corresponde ao final do URL para o resultado. Essa tag é útil para incluir um gráfico nos resultados da pesquisa com base na extensão do link. O atributo value é uma lista de uma ou mais extensões (separadas por espaço) da seguinte maneira: VALUE=".pdf" ou VALUE=".html .htm". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags condicionais de posição de loop {#section_E0C29DDA09E043C9A396F36334F05EBB}

As tags a seguir incluem condicionalmente o texto entre elas. Eles só podem aparecer dentro das tags &quot;looping&quot;: &lt; `search-results>` e `<search-field-values>`. Eles são usados para testar a posição do resultado atual dentro do conjunto de resultados.

Consulte [Sobre as tags de loop de Resultados](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt; ...  &lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt; ...  &lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o texto entre elas se o resultado atual for (ou não for) o primeiro resultado na página (quando usado dentro de <span class="codeph"> &lt;search-results&gt; </span>) ou o primeiro valor de campo (quando usado dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt; ...  &lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt; ...  &lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o texto entre elas se o resultado atual for (ou não for) o último resultado na página (quando usado dentro de <span class="codeph"> &lt;search-results&gt; </span>) ou o último valor de campo (quando usado dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). Essa tag pode ser usada para inserir um separador entre os resultados. Por exemplo, isso insere uma tag <span class="codeph"> &lt;hr&gt; </span> entre os resultados: </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt; ...  &lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt; ...  &lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o texto entre elas se o resultado atual não for o primeiro nem o último resultado na página (quando usado dentro de <span class="codeph"> &lt;search-results&gt; </span>) ou se não for o primeiro nem o último valor do campo (quando usado dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). A versão not da tag testa se o resultado é o primeiro ou o último. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt; ...  &lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt; ...  &lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o texto entre elas se o resultado atual for (ou não for) um resultado alternativo na página (quando usado dentro de <span class="codeph"> &lt;search-results&gt; </span>) ou um valor de campo alternativo (quando usado dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). Os resultados "alternativos" são o segundo, o quarto, o sexto e assim por diante, na página. Este exemplo aplica uma classe diferente a linhas de tabela alternativas. Observe o uso de <span class="codeph"> &lt;search-lt&gt; </span> e <span class="codeph"> &lt;search-gt&gt; </span> para permitir que a tag <span class="codeph"> &lt;search-if-alt&gt; </span> seja colocada "dentro" da tag <span class="codeph"> &lt;tr&gt; </span>. </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt; ...  &lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt; ...  &lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem o texto entre elas se o resultado atual for (ou não for) um resultado par numerado (quando usado dentro de <span class="codeph"> &lt;search-results&gt; </span>) ou um valor de campo par numerado (quando usado dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). Um resultado de pesquisa é par se seu valor <span class="codeph"> &lt;search-index&gt; </span> for par. Em outras palavras, se sua posição dentro de todo o conjunto de resultados for par. Isso pode ser diferente de <span class="codeph"> &lt;search-if-alt&gt; </span> que testa a posição de um resultado na página, não dentro do conjunto de resultados inteiro. Os dois quadros seguintes ilustram a diferença: </p> </td> 
  </tr> 
 </tbody> 
</table>

### Primeira página, sp_n=1

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Índice </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
   <th colname="col3" class="entry"> <p>Mesmo? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Primeiro resultado </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Segundo resultado </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Terceiro resultado </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Quarto resultado </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Quinto resultado </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
  </tr> 
 </tbody> 
</table>

### Página posterior, sp_n=10

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Índice </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
   <th colname="col3" class="entry"> <p>Mesmo? </p> </th> 
   <th colname="col4" class="entry"> <p>Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>10º </p> </td> 
   <td colname="col2"> <p>Décimo resultado </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11º </p> </td> 
   <td colname="col2"> <p>Décimo primeiro resultado </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12º </p> </td> 
   <td colname="col2"> <p>Décimo segundo resultado </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13º </p> </td> 
   <td colname="col2"> <p>Décimo terceiro resultado </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14. </p> </td> 
   <td colname="col2"> <p>Décimo quarto resultado </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
  </tr> 
 </tbody> 
</table>

Finalmente, observe que `<search-if-even>` é sempre o mesmo que `<search-if-alt>` para valores de campo de pesquisa, pois valores de campo não são paginados.

## Tags de lista de valores de campo {#section_D3298B5F976447DBA0032B883DCC91B1}

Os seguintes valores de campo de saída de tags avançadas e dados relacionados do conjunto inteiro de resultados de pesquisa. Essas tags só produzem saída para campos especificados pelos parâmetros CGI `sp-sfvl-field` na consulta de pesquisa.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list name="field-name" quotes="yes/no" commas="yes/no" data="values/counts/results" separator="X" sortby="none/values/counts/results" max-items="XX" date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag exibe uma lista de valores de campo exclusivos, contagens de valor ou contagens de resultado em todo o conjunto de resultados. </p> <p>Essa tag só gera saída para campos especificados pelos parâmetros CGI <span class="codeph"> sp_sfvl_field </span> na consulta de pesquisa. O atributo opcional "aspas" controla se a saída de itens individuais é rodeada por aspas duplas (ou aspas simples, se encoding=perl). O valor padrão de "aspas" é "sim". O atributo opcional "vírgulas" controla se a saída de itens individuais é separada por vírgulas. O valor padrão de "vírgulas" é "sim". O atributo opcional "data" controla se cada valor de campo exclusivo é de saída (data="values"), a contagem total de cada valor de campo exclusivo é de saída (data="count") ou o número de resultados que contém cada valor exclusivo (data="results") é de saída. O valor padrão de "dados" é "valores". Para campos que não são do tipo lista, data="count" e data="results" são equivalentes. O atributo separator define o caractere único, ou delimitador, a ser inserido entre os valores da saída. O atributo opcional "sortby" controla a ordem da saída; Sortby="none" significa sem uma ordem específica, sortby="values" significa classificar por valores de campo (em ordem crescente ou decrescente de acordo com a propriedade Sorting do campo), sortby="count" significa classificar em ordem decrescente de contagens de valor de campo e ordenar por="results" significa classificar em ordem decrescente do número de resultados que contém cada valor. </p> <p>Observe que sortby="count" e sortby="results" são equivalentes para campos de tipo não listado. O atributo opcional "itens máximos" limita o número de itens a serem enviados. O valor padrão de "itens máximos" é -1, o que significa "saída de todos os itens". </p> <p>Existe um limite absoluto de 100 para itens máximos. Os atributos "date-format", "gmt" e "language" só são relevantes se o tipo de conteúdo do campo especificado for "date". O atributo "date-format" tem uma cadeia de caracteres de formato de data no estilo UNIX, como "%A, %B %d, %Y" (para "segunda-feira, 25 de julho de 2016"). O padrão "gmt" é "yes" e controla se a parte de tempo da string de data deve ser saída em GMT ("yes") ou no fuso horário da conta ("no"). </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Sequências de caracteres do formato de data</a>. </p> <p>O atributo "language" controla o idioma e as convenções de localidade da string de data de saída. "0" (padrão) significa "Usar idioma da conta". Qualquer outro valor de "idioma" é interpretado como um identificador de idioma específico, por exemplo, "en_US" significa "inglês (Estados Unidos)". O atributo opcional "encoding" controla se os caracteres da string de saída são codificados em HTML, codificados em JavaScript, codificados em Perl, codificados em URL ou não, para saída na página de resultados. O valor padrão de "encoding" é "html". </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificadores de idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag exibe informações de contagem para uma determinada lista de valores de campo de pesquisa. Há três usos distintos para essa tag. Se somente o atributo "name" for fornecido, essa tag resultará no número de valores exclusivos para o campo nomeado em todo o conjunto de resultados. Se os atributos "name" e "value" forem fornecidos, essa tag resultará na contagem total do valor fornecido dentro de todo o conjunto de resultados (para results="no") ou na contagem total de resultados contendo o valor especificado em todo o conjunto de resultados (para results="yes"). O valor padrão de "resultados" é "não". Observação: Para campos de tipo não listado, results="yes" e results="no" são equivalentes. O valor de "results" é ignorado se o atributo "value" não for fornecido. Essa tag só gera saída para campos especificados pelos parâmetros CGI <span class="codeph"> sp-sfvl-field </span> na consulta de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-list-count name="field-name" value="field-value"&gt; ...  &lt;/search-if-field-value-list-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-list-count name="field-name" value="field-value"&gt; ...  &lt;/search-if-not-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags exibem o HTML entre elas se a chamada equivalente para <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> com os atributos fornecidos retornasse (ou não) um valor maior que zero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-list-count name="field-name"&gt; ...  &lt;/search-if-single-field-value-list-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags exibem o conteúdo entre elas se a chamada equivalente para <span class="codeph"> &lt;search-field-value-list-count name="field-name" value="field-value"&gt; </span> com os atributos fornecidos retornasse (ou não) um único valor. Normalmente, isso é usado quando uma conta está usando slots de facetas. Com slots de faceta, você geralmente só deseja exibir o slot de valor quando o slot de nome associado tem um único item. Fazer essa verificação no template de transporte é mais eficiente do que fazer isso na camada de apresentação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags de loop da lista de valores do campo {#section_0717FA09F0FC449CB916883B0500A60E}

As tags avançadas a seguir enumeram os valores de campo de saída e os dados relacionados de todo o conjunto de resultados de pesquisa usando uma construção de loop. Essas tags só produzem saída para campos especificados pelos parâmetros CGI `sp-sfvl-field` na consulta de pesquisa.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt; ...  &lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag cria um loop para enumerar valores de campo e dados relacionados para um campo específico em todo o conjunto de resultados. Não aninhe esta tag dentro de outra tag <span class="codeph"> &lt;search-field-values&gt; </span>. O atributo "name" especifica o nome do campo que contém os valores a serem enumerados. O atributo opcional "sortby" controla a ordem de enumeração: "none" significa sem uma ordem específica, "values" significa classificar por valores de campo (em ordem crescente ou decrescente de acordo com a propriedade Sorting do campo), sortby="count" significa classificar em ordem decrescente de contagens de valor de campo, e sortby="results" significa classificar em ordem decrescente do número de resultados que contém cada valor. </p> <p>Observe que sortby="count" e sortby="results" são equivalentes para campos de tipo não listado. . O atributo opcional "itens máximos" limita o número de iterações ao valor especificado. O valor padrão para "itens máximos" é -1, o que significa "enumerar todos os valores". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag gera o valor do campo para a iteração de loop &lt;search-field-values&gt; atual. Esta tag só é válida dentro de um loop <span class="codeph"> &lt;search-field-values&gt; </span>. Os atributos "date-format", "gmt" e "language" só são relevantes se o tipo de conteúdo do nome do campo especificado na tag &lt;search-field-values&gt; de inclusão for "date". O atributo "date-format" tem uma cadeia de caracteres de formato de data no estilo UNIX, como "%A, %B %d, %Y" (para "segunda-feira, 25 de julho de 2020"). </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Sequências de caracteres do formato de data</a>. </p> <p>O atributo opcional "encoding" controla se os caracteres da string de saída são codificados em HTML, codificados em JavaScript, codificados em Perl, codificados em URL ou não, para saída na página de resultados. O valor padrão de "encoding" é "none". Normalmente, não é necessário especificar o atributo de codificação. O padrão "gmt" é "yes" e controla se a parte de tempo da string de data deve ser saída em GMT ("yes") ou no fuso horário da conta ("no"). O atributo "language" controla o idioma e as convenções de localidade da string de data de saída. "0" (padrão) significa "Usar idioma da conta". Qualquer outro valor de "idioma" é interpretado como um identificador de idioma específico, por exemplo, "en_US" significa "inglês (Estados Unidos)". </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificadores de idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag gera a contagem associada à iteração de loop <span class="codeph"> &lt;search-field-values&gt; </span> atual. A contagem de saída é o número de resultados em todo o conjunto de resultados que contém o valor do campo (results="yes") ou a contagem total do valor do campo em todo o conjunto de resultados. O valor padrão de "resultados" é "não". </p> <p>Para campos de tipo não listado, results="yes" e results="no" são equivalentes. Esta tag só é válida dentro de um loop <span class="codeph"> &lt;search-field-values&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag gera o contador ordinal para a iteração de loop <span class="codeph"> &lt;search-field-values&gt; </span> atual. Esta tag só é válida dentro de um loop <span class="codeph"> &lt;search-field-values&gt; </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sugerir tags {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

A sugestão oferece um &quot;Você quer dizer?&quot; amigável serviço para sugerir termos de pesquisa alternativos. Se um usuário tiver escrito incorretamente um termo de pesquisa, por exemplo, Sugerir pode ajudar o usuário a encontrar resultados sugerindo uma ortografia correta. O sistema também pode sugerir palavras-chave relacionadas que possam ajudar um usuário a descobrir resultados. Ao gerar sugestões, o serviço Sugerir usa dois dicionários: um com base no idioma da conta (definido em **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]** > **[!UICONTROL Language]**) e o outro com base exclusivamente nas palavras-chave no índice da conta.

>[!NOTE]
>
>O serviço Suggest não funciona para chinês, japonês ou coreano.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-suggestions&gt; ...  &lt;/search-if-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Marque essas tags com qualquer tag de modelo "Sugerir", como <span class="codeph"> &lt;search-sugestion&gt; </span>, <span class="codeph"> &lt;search-sugestion-link&gt; </span> e assim por diante. Se a pesquisa gerar sugestões, o mecanismo de pesquisa gerará e processará tudo entre a tag de abertura e fechamento. Se a pesquisa não gerar sugestões, nenhum do conteúdo aninhado será gerado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestions&gt; ...  &lt;/search-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag gera o loop "Sugestão", que contém uma lista de termos de pesquisa sugeridos (por exemplo, "intenção", "intenção" e "intenção", para um query originalmente inserido como "intenção"). Ao gerar a lista de termos, o mecanismo de pesquisa repete qualquer tag de modelo e/ou HTML aninhada até cinco vezes, que é o número máximo de sugestões. Use o atributo count para especificar o número de sugestões geradas (entre 0 e 5). </p> <p>A tag <span class="codeph"> &lt;search-sugestões&gt; </span> pode aparecer várias vezes na página para repetir a lista de sugestões. Várias sugestões são classificadas de acordo com o número de resultados cada produtividade. </p> <p>Aninhe a tag <span class="codeph"> &lt;search-recommendations&gt; </span> entre as tags <span class="codeph"> &lt;search-if-sugestivas&gt; </span> abertas e ocultas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-link&gt; ...  &lt;/search-suggestion-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag gera um link para a consulta de pesquisa original usando o termo de pesquisa sugerido selecionado em vez do termo original. A tag aceita e simplesmente imprime qualquer atributo HTML, como classe, destino e estilo. A tag também pode aceitar um atributo de URL, cujo valor é usado como URL base para o link gerado. As tags só podem aparecer dentro do loop <span class="codeph"> &lt;search-sugestões&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-text /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag imprime o termo de consulta sugerido no momento (por exemplo, "pretende" para uma consulta originalmente inserida como "intenções"). A tag não tem atributos e só pode aparecer dentro do loop <span class="codeph"> &lt;search-sugestões&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-suggestions&gt; ...  &lt;/search-if-not-suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Se a pesquisa não gerar sugestões, o mecanismo de pesquisa gerará e processará tudo entre a tag de abertura e fechamento. Se a pesquisa gerar sugestões, nenhum do conteúdo aninhado será gerado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if&gt; ...  &lt;/search-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags condicionais incluem o HTML entre elas com base no fato de o termo sugerido ser o primeiro termo no loop Sugerir. As tags devem aparecer entre as tags open e close <span class="codeph"> &lt;search-sugestion&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if&gt; ...  &lt;/search-if&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags condicionais incluem o HTML entre elas com base no fato de o termo sugerido ser o último termo no loop Sugerir. As tags devem aparecer entre as tags open e close <span class="codeph"> &lt;search-sugestion&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag retorna o índice numérico do termo de pesquisa sugerido atual. A tag deve aparecer entre as tags <span class="codeph"> &lt;search-sugestion&gt; </span> e fechar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag retorna o número total de termos de pesquisa sugeridos gerados. A tag deve aparecer entre as tags <span class="codeph"> &lt;search-sugestion&gt; </span> e fechar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-suggestion-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag retorna o número total de resultados para o termo de pesquisa sugerido. A tag deve aparecer entre as tags <span class="codeph"> &lt;search-sugestion&gt; </span> e fechar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags de string de modelo {#section_67E3D529661F4F03A1FF469D9D658CAF}

As tags a seguir exibem uma string no HTML nesse ponto do modelo.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>A tag do corpo HTML com qualquer configuração de Cor do link de pesquisa que a Seção de aparência básica define no link Modelo . Adicione um atributo de plano de fundo a essa tag para exibir imagens de plano de fundo na página de resultados. Qualquer atributo de cor adicionado a essa tag substitui as configurações de Cor do link de pesquisa que a seção Aparência básica define. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>O HTML para o Cabeçalho de resultados da pesquisa, conforme definido na seção Aparência básica sob o link Modelo . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-cdata&gt; ...  &lt;/search-cdata&gt; </span> </p> </td> 
   <td colname="col2"> <p>As tags search-data são substituídas por seus equivalentes XML: <span class="codeph"> &lt;search-cdata&gt; </span> é substituído por <span class="codeph"> &lt;![CDATA[" e a tag &lt;/search-cdata&gt; </span> é substituída por " <span class="codeph"> ]]&gt; </span>". Um analisador XML não analisa nenhuma informação entre a tag de abertura e fechamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-query query-number="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>A consulta que o visitante inseriu. O atributo avançado e opcional "número de consulta" controla qual sequência de consulta numerada é gerada por essa tag. Por exemplo, <span class="codeph"> &lt;search-query-number=1&gt; </span> gera o conteúdo do parâmetro de cgi <span class="codeph"> sp_q_1 </span>. Se "query-number" não for especificado, ou se o query-number for "0", a consulta principal ( <span class="codeph"> sp_q </span>) será realizada. O atributo opcional "encoding" controla se a saída é codificada em HTML, codificada em JavaScript, Codificada em Perl, codificada ou não em URL, para saída na página de resultados. O valor padrão de "encoding" é "html". Normalmente, não é necessário especificar o atributo de codificação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>A contagem total de resultados desta pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>A contagem de resultados relatados para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>O número do primeiro resultado relatado para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-upper&gt; </span> </p> </td> 
   <td colname="col2"> <p>O número do último resultado relatado para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>O número de resultados relatados para a página anterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>O número de resultados relatados para a próxima página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p>O tempo em segundos para esta pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>O HTML do logotipo de Pesquisa configurado para sua conta, se houver. Este logotipo é a imagem que dá crédito à pesquisa/comercialização do site </p> <p>A maioria das contas não tem um logotipo de pesquisa associado no momento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>A coleção dos resultados desta pesquisa. O atributo opcional "all" é usado para fornecer o nome da coleção que representa o site inteiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14. </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt; ...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insere tags de formulário de início e fim. Insere o método e os atributos de ação na tag de início de formulário. Aceita atributos adicionais incluindo o atributo dir="RTL" para linguagem, bem como os atributos "name" e "onSubmit" relacionados ao JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15. </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insere uma tag de entrada de formulário que especifica o número da conta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insere uma tag de entrada de formulário que especifica o número da galeria. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-query query-number="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insere uma tag de entrada de formulário que especifica a string de consulta. O atributo avançado e opcional "número de consulta" controla qual consulta numerada é usada para a tag de entrada do formulário. Por exemplo, <span class="codeph"> &lt;search-input-query query-number=1&gt; </span> gera uma tag de entrada de formulário para a consulta <span class="codeph"> sp_q_1 </span>. Se "query-number" não for especificado, ou se "query-number" for "0", uma tag de entrada para a consulta principal <span class="codeph"> sp_q </span> será inserida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collections all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insere uma tag de seleção de formulário e o HTML associado que exibe o menu de seleção de coleções. O atributo opcional "all" é usado para fornecer o nome da coleção que representa o site inteiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insere a saída de uma das tags de modelo de Pesquisa em outras tags HTML ou modelo na página de resultados. <span class="codeph"> &lt;search-lt&gt; </span> insere um caractere menor que. O uso de <span class="codeph"> &lt;search-lt&gt; </span> e <span class="codeph"> &lt;search-gt&gt; </span> fornece uma maneira de escapar da definição de uma tag para que você possa usar as tags do modelo de Pesquisa como valores de atributo. Quando o modelo é renderizado em resposta a uma pesquisa, um sinal de menos que (&lt;) substitui a tag <span class="codeph"> &lt;search-lt&gt; </span>. Por exemplo, <span class="codeph"> &lt;search-link&gt; </span> é equivalente a <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Insere a saída de uma das tags de modelo de Pesquisa em outras tags HTML ou modelo na página de resultados. <span class="codeph"> &lt;search-gt&gt; </span> insere um caractere maior que. O uso de <span class="codeph"> &lt;search-lt&gt; </span> e <span class="codeph"> &lt;search-gt&gt; </span> fornece uma maneira de escapar da definição de uma tag para que você possa usar outras tags de modelo como valores de atributo. Quando o modelo é renderizado em resposta a uma pesquisa, um sinal de maior que (&gt;) substitui a tag <span class="codeph"> &lt;search-gt&gt; </span>. Por exemplo, <span class="codeph"> &lt;search-link&gt; </span> é equivalente a <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21º </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Retorna o valor do parâmetro cgi chamado "param-name" da solicitação de pesquisa atual. O atributo opcional "encoding" controla se a saída é codificada em HTML, codificada em JavaScript, Codificada em Perl, codificada ou não em URL, para saída na página de resultados. O valor padrão de "encoding" é "html". Normalmente, não é necessário especificar o atributo de codificação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22º </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>O atributo <span class="codeph"> de codificação </span> é opcional; o valor padrão é <span class="codeph"> json </span>. </p> <p> <p>Observação:  Esta tag só tem saída se <span class="codeph"> sp_trace=1 </span> for especificado com os parâmetros de consulta de pesquisa principais. </p> </p> <p>Consulte a linha 48 na tabela localizada em <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> Backend search CGI parameters</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags de link de âncora do modelo {#section_3A51D27616C541E2B818CC52B2B856BA}

Veja a seguir as tags que fazem com que um link de âncora rode o HTML entre elas. Quando clicado, o link de âncora solicita outra página de resultados para exibição. O atributo opcional &quot;count&quot; solicita muitos resultados na página para exibição. Se não especificado, a contagem solicitada na página atual é usada. O atributo avançado e opcional &quot;URL&quot; controla o domínio para o qual o link associado é direcionado. Por padrão, o domínio é `https://search.atomz.com/search/`, mas você pode alterá-lo usando o atributo de URL.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>Exibe a página seguinte ou anterior dos resultados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Classifica os resultados por data ou relevância. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summaries URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summaries URL="https://search.yourdomain.com/search/"&gt; ...  &lt;/search-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Mostra ou oculta os resumos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags condicionais do modelo {#section_18D9BC66DE484881932FD2F7EA9D170D}

Tags que permitem incluir HTML condicionalmente entre elas.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt; ...  &lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt; ...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem HTML se a página atual contiver quaisquer resultados de pesquisa (ou não). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt; ...  &lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt; ...  &lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt; ...  &lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt; ...  &lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem HTML se a página anterior ou a página seguinte tiver resultados associados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt; ...  &lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt; ...  &lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt; ...  &lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt; ...  &lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem HTML se a página atual for ou não classificada por relevância ou data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summaries&gt; ...  &lt;/search-if-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summaries&gt; ...  &lt;/search-if-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem HTML se a página atual estiver mostrando ou ocultando resumos. Você pode usar essas tags para incluir ou excluir qualquer parte do resultado da pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collections&gt; ...  &lt;/search-if-input-collections&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collections&gt; ...  &lt;/search-if-not-input-collections&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem HTML se uma coleção foi especificada na geração de resultados de pesquisa para a página atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt; ...  &lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt; ...  &lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem HTML se o parâmetro CGI <span class="codeph"> sp_advanced=1 </span> foi especificado para a consulta de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt; ...  &lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt; ...  &lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags incluem ou excluem o HTML entre elas se o parâmetro especificado for ou não inválido. </p> <p>Atualmente, somente o parâmetro <span class="codeph"> sp_q_location[_#] </span> é compatível. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt; ...  &lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt; ...  &lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags avançadas incluem o HTML entre elas com base no fato de o parâmetro CGI especificado no atributo "name" ter o valor especificado no atributo "value". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt; ...  &lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt; ...  &lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags avançadas incluem o HTML entre elas se a página atual for ou não classificada pelo nome de campo fornecido. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tags de controle de formulário de modelo {#section_45AFC414ACA74825B72FEAA8456F8DD2}

Tags que permitem controlar o estado de seleção padrão de caixas de seleção, botões de opção e caixas de listagem em um `<form>` no modelo de pesquisa.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Adicionar tag </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input&gt; </span> </p> </td> 
   <td colname="col2"> <p>Usado em um modelo no lugar de uma tag <span class="codeph"> &lt;input&gt; </span> . Quando a tag é gravada no navegador, a palavra <span class="codeph"> input </span> substitui <span class="codeph"> search-input </span> e todas as outras informações na tag são geradas como estão. Além disso, se o nome <span class="codeph"> </span> especificado na tag for listado como um parâmetro CGI e se o valor <span class="codeph"> </span> especificado na tag for o valor desse parâmetro CGI, a palavra <span class="codeph"> marcado </span> será adicionada ao final da tag. Dessa forma, você pode tornar automaticamente o botão de opção padrão ou o estado da caixa de seleção em seu resultado de pesquisa igual ao da consulta atual. </p> <p>Por exemplo, o código HTML de uma caixa de seleção pode ser semelhante ao seguinte: </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact"&gt;Sem correspondência de som  </span> </p> <p>O código de modelo correspondente para essa caixa de seleção é o seguinte: </p> <p> <span class="codeph"> &lt;search-input type="checkbox" name="sp_w" value="exact"&gt;Sem correspondência de som  </span> </p> <p>Se a string do parâmetro CGI para a consulta contiver <span class="codeph"> sp_w=exato </span>, a tag gravada no navegador com os resultados da pesquisa se parecerá com a seguinte (a palavra <span class="codeph"> marcada </span> é inserida no final da tag): </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact" checked=""&gt;Sem correspondência de som  </span> </p> <p>Se a string do parâmetro CGI para a consulta não contiver <span class="codeph"> sp_w=exato </span>, a tag gravada no navegador com os resultados da pesquisa se parecerá com a seguinte (a palavra <span class="codeph"> marcada </span> não está listada na tag ): </p> <p> <span class="codeph"> &lt;input type="checkbox" name="sp_w" value="exact"&gt;Sem correspondência de som  </span> </p> <p>A tag <span class="codeph"> &lt;search-input&gt; </span> é útil para colocar caixas de seleção e botões de opção em seu modelo de pesquisa. Se você tiver caixas de seleção ou botões de opção que deseja adicionar ao <span class="codeph"> &lt;form&gt; </span> no modelo de pesquisa, use <span class="codeph"> &lt;search-input...&gt; </span> no lugar de <span class="codeph"> &lt;input..&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt; ...  &lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;search-option&gt; ...  &lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>As caixas de listagem suspensas em uma tag <span class="codeph"> &lt;form&gt; </span> são iniciadas com uma tag <span class="codeph"> &lt;select&gt; </span> e terminadas com uma tag <span class="codeph"> &lt;/select&gt; </span>. O nome <span class="codeph"> </span> do parâmetro CGI associado é listado dentro da tag <span class="codeph"> &lt;select&gt; </span>. Após a tag <span class="codeph"> &lt;select&gt; </span>, há uma lista de tags <span class="codeph"> &lt;option&gt; </span> que especificam os valores a serem exibidos na caixa de listagem. </p> <p>As tags <span class="codeph"> &lt;search-select&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span>, <span class="codeph"> &lt;search-option&gt; </span> e <span class="codeph"> &lt;/search-option&gt; </span> fornecem funcionalidade semelhante à tag <span class="codeph"> &lt;search-input&gt; </span>. Ou seja, a palavra <span class="codeph"> selecionada </span> é adicionada automaticamente no final da tag <span class="codeph"> &lt;option&gt; </span> enviada para o navegador se o nome <span class="codeph"> </span> na tag <span class="codeph"> &lt;search-select&gt; </span> for listado como um parâmetro CGI e se o valor <span class="codeph"> </span> desse parâmetro CGI for listado como o valor <span class="codeph"> </span> em uma tag <span class="codeph"> &lt;search-option&gt; </span> específica. Dessa forma, você pode automaticamente fazer a opção da caixa de listagem padrão em seu resultado de pesquisa igual à query atual. </p> <p>Por exemplo, uma caixa de listagem típica tem a seguinte aparência: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>O código de modelo correspondente para essa caixa de listagem é o seguinte: </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>Se você tiver caixas de listagem que deseja adicionar ao <span class="codeph"> &lt;form&gt; </span> em seu modelo de pesquisa, use <span class="codeph"> &lt;search-select...&gt; </span> no lugar de <span class="codeph"> &lt;select..&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span> no lugar de <span class="codeph"> &lt;/select&gt; </span>, <span class="codeph"> &lt;search-option...&gt; </span> no lugar de <span class="codeph"> &lt;option..&gt; </span> e <span class="codeph"> &lt;/search-option&gt; </span> no lugar de <span class="codeph"> &lt;/option&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ...  &lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas tags avançadas criam um link de âncora ao redor do HTML entre elas. Quando essa âncora é clicada, uma página de resultados classificados no campo especificado é exibida. O atributo <span class="codeph"> count </span> opcional especifica o número de resultados a serem exibidos na página de resultados. Se <span class="codeph"> count </span> for omitido, a contagem usada na página atual será usada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sequências de caracteres de formato de data {#section_4BBDBBEF2B96414497617CD4B52D96E4}

Você pode usar as seguintes especificações de conversão nas sequências de caracteres do formato de data:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sequência de caracteres do formato de data </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%Um </p> </td> 
   <td colname="col2"> <p> Corresponde à representação nacional do nome completo do dia da semana, por exemplo, "Segunda-feira". A configuração em <span class="uicontrol"> Linguística </span> &gt; <span class="uicontrol"> Palavras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina a representação nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Sobre palavras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> Corresponde à representação nacional do nome abreviado do dia da semana, em que a abreviação é os três primeiros caracteres, por exemplo "Mon". A configuração em <span class="uicontrol"> Linguística </span> &gt; <span class="uicontrol"> Palavras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina a representação nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Sobre palavras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> Corresponde à representação nacional do nome completo do mês, por exemplo "junho". A configuração em <span class="uicontrol"> Linguística </span> &gt; <span class="uicontrol"> Palavras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina a representação nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Sobre palavras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> Corresponde à representação nacional do nome abreviado do mês, em que a abreviação é os três primeiros caracteres, por exemplo "Jun". A configuração em <span class="uicontrol"> Linguística </span> &gt; <span class="uicontrol"> Palavras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina a representação nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Sobre palavras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>Equivalente a "%m/%d/%y", por exemplo "07/25/13". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> Corresponde ao dia do mês como um número decimal (01-31). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> Corresponde ao dia do mês como um número decimal (1-31). Um branco precede um único dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> Corresponde ao relógio de 24 horas como um número decimal (00-23). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> Corresponde à representação nacional do nome abreviado do mês, em que a abreviação corresponde aos três primeiros caracteres, por exemplo "Jun" (o mesmo que %b). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> Corresponde ao relógio de 12 horas como um número decimal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> Corresponde ao dia do ano como um número decimal (001-366). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> Corresponde ao (relógio de 24 horas como um número decimal (0-23). Um branco precede um único dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> Corresponde ao relógio de 12 horas da hora como um número decimal (1-12). Um branco precede um único dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> Corresponde ao minuto como um número decimal (00-59). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> Corresponde ao mês como um número decimal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> Corresponde à representação nacional de "ante meridiem" ou "post meridiem", conforme apropriado, por exemplo "PM". A configuração em <span class="uicontrol"> Linguística </span> &gt; <span class="uicontrol"> Palavras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina a representação nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Sobre palavras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>Equivalente a "%H:%M", por exemplo, "13:23". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>Equivalente a "%I:%M:%S %p", por exemplo, "01:23:45 PM". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> Corresponde o segundo como um número decimal (00-60). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>Equivalente a "%H:%M:%S", por exemplo, "13:26:47". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> Corresponde ao número da semana do ano (domingo como primeiro dia da semana) como um número decimal (00-53). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>Equivalente a "%e-%b-%Y", por exemplo, "25-jul-2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> Corresponde ao ano com século como um número decimal, por exemplo, "2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> Corresponde ao ano sem século como um número decimal (00-99). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> Corresponde ao nome do fuso horário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> Corresponde "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Identificadores de idioma {#section_0490DECC00E34691ADE5A9ED90A6D911}

A tabela a seguir contém os identificadores de idioma para cada idioma suportado. Você pode usar esses identificadores como valores para o atributo opcional &quot;idioma&quot; nas seguintes tags de modelo:

* `search-date` e `search-display-field`.

   Consulte [Tags de sequência de loop de resultados](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320).

* `search-field-value-list` Consulte  [Tags da lista de valores do campo](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1).

* `search-field-value` Consulte  [Tags de loop da lista de valores do campo](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Idioma  </p> </th> 
   <th colname="col2" class="entry"> <p>Identificador de idioma </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Búlgaro (Bulgária) </p> </td> 
   <td colname="col2"> <p> bg_BG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (China) </p> </td> 
   <td colname="col2"> <p> zh_CN </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (Hong Kong) </p> </td> 
   <td colname="col2"> <p> zh_HK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (Singapura) </p> </td> 
   <td colname="col2"> <p>zh_SG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (Taiwan) </p> </td> 
   <td colname="col2"> <p> zh_TW </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tcheco (República Tcheca) </p> </td> 
   <td colname="col2"> <p> cs_CZ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dinamarquês (Dinamarca) </p> </td> 
   <td colname="col2"> <p> da_DK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Holandês (Bélgica) </p> </td> 
   <td colname="col2"> <p> nl_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Holandês (Países Baixos) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglês (Austrália) </p> </td> 
   <td colname="col2"> <p> en_AU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglês (Canadá) </p> </td> 
   <td colname="col2"> <p> en_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglês (Grã-Bretanha) </p> </td> 
   <td colname="col2"> <p> en_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglês (Estados Unidos) </p> </td> 
   <td colname="col2"> <p> en_US </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francês (Bélgica) </p> </td> 
   <td colname="col2"> <p> fr_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francês (Canadá) </p> </td> 
   <td colname="col2"> <p>fr_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Finlandês (Finlândia) </p> </td> 
   <td colname="col2"> <p> fi_FI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francês (França) </p> </td> 
   <td colname="col2"> <p> fr_FR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francês (Suíça) </p> </td> 
   <td colname="col2"> <p> fr_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alemão (Áustria) </p> </td> 
   <td colname="col2"> <p> de_AT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alemão (Alemanha) </p> </td> 
   <td colname="col2"> <p> de_DE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alemão (Suíça) </p> </td> 
   <td colname="col2"> <p> de_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Grego (Grécia) </p> </td> 
   <td colname="col2"> <p> el_GR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gaélico Irlandês (Irlanda) </p> </td> 
   <td colname="col2"> <p> ga_IE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Italiano (Itália) </p> </td> 
   <td colname="col2"> <p> it_IT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japonês (Japão) </p> </td> 
   <td colname="col2"> <p> ja_JP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Coreano (Coreia) </p> </td> 
   <td colname="col2"> <p> ko_KR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Norueguês (Noruega) </p> </td> 
   <td colname="col2"> <p> no_NO </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Polonês (Polônia) </p> </td> 
   <td colname="col2"> <p> pl_PL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Português (Brasil) </p> </td> 
   <td colname="col2"> <p> pt_BR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Português (Portugal) </p> </td> 
   <td colname="col2"> <p> pt_PT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Russo (Antiga União Soviética) </p> </td> 
   <td colname="col2"> <p> ru_SU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Eslovaco (Eslováquia) </p> </td> 
   <td colname="col2"> <p> sk_SK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Eslovaco (Eslovênia) </p> </td> 
   <td colname="col2"> <p>sl_SI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Espanhol (México) </p> </td> 
   <td colname="col2"> <p> es_MX </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Espanhol (Espanha) </p> </td> 
   <td colname="col2"> <p> es_ES </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sueco (Suécia) </p> </td> 
   <td colname="col2"> <p> sv_SE </p> </td> 
  </tr> 
 </tbody> 
</table>

## Especificação do cabeçalho HTTP do tipo de conteúdo {#section_AEED823E9938448A9EDB2F286D9CFD90}

Você pode especificar o cabeçalho de resposta HTTP Tipo de conteúdo usando a seguinte tag:

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

Os atributos `content` e `charset` são opcionais. Essa tag deve aparecer o mais cedo possível no template. Também é recomendável que ele seja exibido antes de `<search-html-meta-charset>` ou `<search-xml-decl>`, pois afeta o comportamento dessas tags.

Se você não especificar o atributo `content`, o valor de `MIME-type` assumirá como padrão o valor definido em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Se você especificar um atributo `content`, ele será usado como o atributo `content` padrão para a tag `<search-html-meta-charset>`.

Se você não especificar o atributo `charset`, nenhum valor `charset` será gravado no cabeçalho `content-type`.

Se você especificar `charset="1"`, o valor real para `charset-name` é o valor do parâmetro CGI `sp_f`. Se nenhum parâmetro CGI `sp_f` for enviado com a pesquisa, o valor real de `charset-name` será lido das configurações da sua conta. Você pode exibir ou alterar o conjunto de caracteres associado à sua conta em **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulte [Configurar as informações pessoais do usuário](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Você pode escolher um nome de conjunto de caracteres específico listando-o como o valor `charset`, como `charset="iso-8859-1"` ou `charset="Shift-JIS"`.

Se você especificar um atributo `charset`, ele será usado como o atributo `charset` padrão para as tags `<search-html-meta-charset>` e `<search-xml-decl>` , além de ser enviado para o cabeçalho `content-type`.

## Especificação de um conjunto de caracteres em um modelo HTML {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

Os modelos de resultado de pesquisa HTML padrão especificam o conjunto de caracteres associado à conta atual por meio da seguinte tag:

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

Os atributos de conteúdo e charset são opcionais. Essa tag deve aparecer na seção HTML `<head>` do template. Essa tag resulta na seguinte tag na página HTML gerada do modelo:

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

Se você não especificar o atributo de conteúdo, o valor real de `MIME-type` assumirá um dos dois valores como padrão. Se a tag `<search-content-type-header>` especificou um atributo `content`, esse valor será usado. Caso contrário, o valor usado é o definido na guia **[!UICONTROL Templates]** > **[!UICONTROL Settings]** > **[!UICONTROL Content Type]**.

Se você não especificar o atributo `charset`, o valor real de `charset-name` assumirá um dos dois valores como padrão. Se a tag `<search-content-type-header>` especificou um atributo `charset`, esse valor será usado. Caso contrário, o valor real de `charset-name` será lido das configurações da sua conta. Você pode exibir ou alterar o conjunto de caracteres associado à sua conta em **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulte [Configurar as informações pessoais do usuário](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Se você especificar `charset="1"`, o valor real para `charset-name` é o valor do parâmetro CGI `sp_f`. Se nenhum parâmetro CGI `sp_f` for enviado com a pesquisa, o valor real de `charset-name` será o valor definido na tag `<search-content-type-header>`, se tiver sido especificado, ou o valor definido nas configurações da sua conta.

Você pode especificar um nome de conjunto de caracteres específico, como em `charset="charset-name"`. Por exemplo, `charset="iso-8859-1"` ou `charset="Shift-JIS"`.

A tag `<search-html-meta-charset>` é opcional. Se você removê-lo, o navegador assume os valores padrão para `content-type`, que são os seguintes: `content="text/html; charset=ISO-8859-1"`. Você também pode optar por substituir a tag `<search-html-meta-charset>` por sua própria tag `http-equiv`.

## Especificação de um conjunto de caracteres em um modelo XML {#section_17DC31CDCC104F5F8081466B41A96E9D}

O modelo de resultado da pesquisa XML padrão especifica o conjunto de caracteres associado à conta atual por meio da seguinte tag:

`<search-xml-decl [charset="charset-name"]>`

O atributo `charset` é opcional. Essa tag deve aparecer na parte superior do modelo, mas após qualquer tag `<search-content-type-header>` . Essa tag resulta na seguinte tag no documento XML gerado a partir do modelo:

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

Se você não especificar o `charset`, o valor real de `charset-name` assumirá um dos dois valores como padrão. Se `<search-content-type-header>` especificou um atributo `charset`, então esse valor é usado. Caso contrário, o valor real de `charset-name` será lido das configurações da sua conta. Você pode exibir ou alterar o conjunto de caracteres associado à sua conta em **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulte [Configurar as informações pessoais do usuário](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Se você especificar `charset="1"`, o valor real para `charset-name` é o valor do parâmetro CGI `sp_f`. Se nenhum parâmetro CGI `sp_f` for enviado com a pesquisa, o valor real de `charset-name` será o valor definido na tag `<search-content-type-header>`, se for especificado, ou o valor definido nas configurações da conta.

Você pode especificar um nome de conjunto de caracteres específico, como em `charset="charset-name"`, se desejar. Por exemplo, `charset="iso-8859-1" or charset="Shift-JIS"`.

Você pode optar por substituir a tag `<search-xml-decl>` por sua própria tag `?xml`.

## Inclusão de um modelo de pesquisa em outro {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

Para incluir um modelo de pesquisa em outro, use a tag `<search-include>` , definindo o atributo de arquivo para o nome do arquivo de modelo que deseja incluir, como no exemplo a seguir:

`<search-include file="seo/seo_search_title.tpl" />`

Os segmentos do modelo de pesquisa SEO estão na subpasta `seo/` e os modelos de pesquisa normais estão na subpasta `templates/`. Somente arquivos .tpl são significativos para incluir neste contexto.

## Gerenciamento de vários modelos de transporte para seu site {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

Você pode controlar a aparência dos resultados de pesquisa em seu site usando modelos de transporte de pesquisa diferentes para cada área.

<!-- 

r_managing_multiple_templates.xml

 -->

Para realizar esse tipo de funcionalidade de pesquisa, você pode gerenciar seus modelos de transporte em pesquisa/merchandising do site. Ou você pode gerenciar os modelos de transporte em Publicar. Como pesquisa/merchandising no site, a opção Publicar permite editar, visualizar e publicar vários modelos de transporte de pesquisa.

Para configurar seus formulários de pesquisa para usar um modelo de transporte específico (diferente do padrão), use o parâmetro de consulta `sp_t` . Por exemplo, suponha que você tenha um modelo de pesquisa chamado &quot;clearance&quot; para a área de vendas marcada do site. Use o formulário de pesquisa HTML padrão com o seguinte código de formulário adicional:

`<input type=hidden name="sp_t" value="clearance">`

Quando um cliente clica em um formulário padrão que contém essa linha de código, o modelo de transporte de pesquisa &quot;clearance&quot; é exibido junto com seus resultados de pesquisa.

Consulte [Uso de coleções em formulários de pesquisa](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Consulte [Uso de quadros com formulários](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Amostra de formulário de pesquisa avançada](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).
