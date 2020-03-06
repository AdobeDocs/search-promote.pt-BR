---
description: É possível personalizar a saída em qualquer formato baseado em texto, incluindo XML ou JSON.
seo-description: É possível personalizar a saída em qualquer formato baseado em texto, incluindo XML ou JSON.
seo-title: Saída da pesquisa guiada
solution: Target
title: Saída da pesquisa guiada
topic: Appendices,Site search and merchandising
uuid: 234fd563-f249-42b0-88ca-c89b44f8df77
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Saída da pesquisa guiada{#guided-search-output}

É possível personalizar a saída em qualquer formato baseado em texto, incluindo XML ou JSON.

## Uso da saída da pesquisa guiada {#concept_2A1BA3AD413848A1AC2A3ABC4FFE481F}

O formato de saída é personalizável para suportar a facetagem, a classificação e outras decisões específicas de implementação tomadas durante o processo de design. Você pode adaptar o próprio formato para simplificar o desenvolvimento do front-end do cliente, se necessário.

A saída inteira está contida em `<result>` tags, e a maioria dos dados dinâmicos está entre `<![CDATA[ ]]>` tags. Essa organização permite que os resultados contenham HTML e outras entidades não XML.

Quando os links para outras páginas são fornecidos, eles são apresentados na forma de um URL relativo. Esse resultado também inclui os parâmetros da string de consulta passados para gerar o resultado desejado.

## Noções básicas sobre a implementação da Pesquisa guiada {#section_95483980930C4325BAB50A40BD47245A}

Quando você iniciar uma implementação de Pesquisa guiada, lembre-se de que isso [!DNL Adobe Search&Promote] é responsável pela Camada de negócios. Ou seja, a lógica que envolve os resultados e facetas que são mostrados a um cliente em um determinado momento.

Quando você implementa o front-end do aplicativo Web que analisa e exibe os resultados como HTML, restrinja a funcionalidade para exibir somente. Em outras palavras, qualquer lógica do lado do servidor usada para criar a Camada de apresentação não toma as decisões sobre o que apresentar ao cliente, a menos que seja necessário. As Regras de negócios não funcionarão como esperado se o script front-end estiver alterando os resultados da pesquisa.

[!DNL Adobe Search&Promote] mantém o estado do usuário das opções de refinamento de pesquisa selecionadas por meio dos parâmetros de URL. Todos os `<link>` nós contêm os parâmetros relevantes das seleções do cliente. Esses parâmetros podem incluir trilhas de navegação, paginação, classificação e seleções de facetas. Quando aplicável, `<undolink>` os nós são retornados para permitir que um cliente faça &quot;back out&quot; de uma seleção. Aspectos e navegações estruturais oferecem esses tipos de links.

## Trabalhar com o Search Server {#section_8DBEACDECD714E59BDED6315E6041B8D}

Uma API semelhante a REST é usada com a qual você pode interagir para realizar pesquisas e receber resultados. Os formatos mais comuns usados para os resultados são XML ou JSON.

O URI de base está associado a uma conta específica e a um ambiente de preparo ou ao vivo. Você pode solicitar vários aliases para o URI básico do seu gerente de conta. Por exemplo, uma empresa ficcional chamada Megacorp tem os dois URLs básicos a seguir associados à conta:

* `https://search.megacorp.com `
* `https://stage.megacorp.com`

O URI anterior realiza buscas em relação ao índice ativo e ao URI anterior em relação ao índice de preparo.

As solicitações de pesquisa consistem no URI base e em um conjunto de parâmetros CGI ou pares de valores chave que indicam a pesquisa desejada para a conta associada ao URI base.

Há suporte para três formatos de parâmetros CGI. Por padrão, sua conta é configurada para separar parâmetros CGI com ponto-e-vírgula ( `;`), como no exemplo a seguir:

* `https://search.megacorp.com?q=shoes ;page=2`

Se preferir, você pode fazer com que seu gerente de conta configure sua conta para usar e comercial ( `&`) para separar os parâmetros CGI, como no exemplo a seguir:

* `https://search.megacorp.com?q=shoes &page=2`

Um terceiro formato, chamado de formato SEO, também é suportado quando uma barra ( `/`) é usada no lugar do separador e sinal de igual para gerar links &quot;limpos&quot;, como no exemplo a seguir:

* `https://search.megacorp.com/q/shoes/page/2`

Sempre que o formato SEO for usado para enviar uma solicitação, todos os links de saída serão retornados no mesmo formato.

## Parâmetros de consulta de pesquisa {#section_7ADA5E130E3040C9BE85D0D68EDD3223}

A tabela a seguir descreve os parâmetros padrão de consulta de pesquisa &quot;predefinidos&quot; que você pode usar. As regras de processamento e as regras de negócios podem ser criadas com base em parâmetros de consulta definidos pelo usuário para implementar uma lógica de negócios personalizada relevante para a sua empresa. Você pode trabalhar com a equipe de consultoria para obter documentação sobre esses parâmetros.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Parâmetro de consulta de pesquisa </p> </th> 
   <th colname="col2" class="entry"> <p>Exemplo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q= string </span> </p> </td> 
   <td colname="col3"> <p> Especifica a string de consulta para a pesquisa. Esse parâmetro mapeia para o parâmetro de pesquisa de backend <span class="codeph"> sp_q </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q#= string </span> </p> </td> 
   <td colname="col3"> <p>Parâmetros <span class="codeph"> q </span> e <span class="codeph"> x numerados </span> permitem lapidar ou pesquisar em um determinado campo. </p> <p>O parâmetro <span class="codeph"> q </span> define o termo que você está procurando na faceta como o parâmetro <span class="codeph"> x numerado correspondente denota </span> . Por exemplo, se você tiver duas facetas com nome de tamanho e cor, você pode ter algo como o seguinte: </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color </span> </p> <p>Esse parâmetro mapeia para os parâmetros de pesquisa de backend <span class="codeph"> sp_q_exato_# </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> x# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> x#= string </span> </p> </td> 
   <td colname="col3"> <p> Parâmetros <span class="codeph"> q </span> e <span class="codeph"> x numerados </span> permitem lapidar ou pesquisar em um determinado campo. </p> <p>O parâmetro <span class="codeph"> q </span> define o termo que você está procurando na faceta como o parâmetro <span class="codeph"> x numerado correspondente denota </span> . Por exemplo, se você tiver duas facetas com nome de tamanho e cor, você pode ter algo como o seguinte: </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color </span> </p> <p>Esse parâmetro mapeia para os parâmetros de pesquisa de backend <span class="codeph"> sp_x_# </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> coleção </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> collection= string </span> </p> </td> 
   <td colname="col3"> <p> Especifica a coleção a ser usada para a pesquisa. Esse parâmetro mapeia para o parâmetro de pesquisa <span class="codeph"> sp_k </span> backend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> count </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> count= número </span> </p> </td> 
   <td colname="col3"> <p> Especifica a contagem total de resultados que são mostrados. O padrão é definido em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Pesquisar </span> &gt; <span class="uicontrol"> Pesquisas </span>. Esse parâmetro mapeia para o parâmetro de pesquisa <span class="codeph"> sp_c </span> backend. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> page </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> page= número </span> </p> </td> 
   <td colname="col3"> <p> Especifica a página de resultados que são retornados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> classificação </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> classificação= campo </span> </p> </td> 
   <td colname="col3"> <p> Especifica o campo de classificação a ser usado para classificação estática. O campo deve ser do tipo Classificação com relevância maior que 0. Esse parâmetro mapeia para o parâmetro de backend <span class="codeph"> sp_sr </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gs_store </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> gs_store= string </span> </p> </td> 
   <td colname="col3"> <p> Especifica a loja a ser pesquisada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espécie </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> sort= número </span> </p> </td> 
   <td colname="col3"> <p> Especifica a ordem de classificação. "0" é o padrão e classifica por pontuação de relevância; "1" ordena por data; "-1" não classifica. </p> <p>Os usuários podem especificar um nome de campo para o valor do parâmetro <span class="codeph"> sp_s </span> . Por exemplo, <span class="codeph"> sp_s=title </span> classifica os resultados de acordo com os valores contidos no campo de título. Quando um nome de campo é usado para o valor de um parâmetro <span class="codeph"> sp_s </span> , os resultados são classificados por esse campo e depois classificados por relevância. </p> <p>Para ativar esse recurso, faça o seguinte: </p> 
    <ol id="ol_3894F81EA7BF4827A84DE8662111ABEF"> 
     <li id="li_C040C0B88F174A4885E1A8E721FD032A">No menu do produto, clique em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>. </li> 
     <li id="li_2E83C3A46D1B4BF991EABAD9D3E52B7D">Na página Definições <span class="wintitle"> preparadas </span> , execute um dos procedimentos a seguir: 
      <ul id="ul_8018FEE10E0A4C96A74F84A897080580"> 
       <li id="li_E9A7CE43E2734F4D9522A1283CA111FB">Click <span class="uicontrol"> Add New Field </span>. </li> 
       <li id="li_9D2434A321924FBD874569CA9AD2EEF7">Clique em <span class="uicontrol"> Editar </span> para obter um nome de campo específico. </li> 
      </ul> </li> 
     <li id="li_90D5E3F4AC0A4A6189934A5589F69903">Na lista <span class="wintitle"> suspensa Classificação </span> , clique em <span class="uicontrol"> Crescente </span> ou <span class="uicontrol"> Decrescente </span>. <p>Esse parâmetro mapeia para o parâmetro de pesquisa de backend <span class="codeph"> sp_s </span> . </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

## Integração com seu sistema {#section_91261B19A44A4E579B3FC9FAB9AD3665}

Veja a seguir recomendações para integração com seu sistema.

* Comunicando-se com o servidor de pesquisa.

   Você pode se comunicar com os servidores da [!DNL Adobe Search&Promote] Web usando solicitações http GET. Seus servidores geram essas solicitações ou no lado do cliente executando uma solicitação Ajax.
* Salvando o histórico de pesquisa.

[!DNL Adobe Search&Promote] é apátrida onde todo o estado é passado na solicitação http.
* Analisando os resultados retornados.

   É recomendável usar um analisador XML baseado em SAX para analisar a resposta XML. Se você estiver gerando uma solicitação Ajax, configure [!DNL Adobe Search&Promote] para retornar respostas JSON para essas solicitações para facilitar a análise da resposta.

## Saída JSON de pesquisa guiada {#reference_EB8182A564DE4374BB84158F2AABEF74}

Tabelas que descrevem a saída de resposta JSON padrão.

Consulte também Saída [JSON de pesquisa](../c-appendices/c-guidedsearchoutput.md#reference_EB8182A564DE4374BB84158F2AABEF74)guiada.

Você pode revisar a resposta JSON para o seguinte:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_88519CAAD25F4BD49D5E517077745B0E)
* [Trilha](../c-appendices/c-guidedsearchoutput.md#section_A7DB0F1DA9ED4CBCAE18395122F3E01E)
* [Aspectos](../c-appendices/c-guidedsearchoutput.md#section_65932C95931743A1BFAF1DF16D7E6D92)
* [Cabeçalho e consulta](../c-appendices/c-guidedsearchoutput.md#section_1D57062259CA46E0B4F598FA4EB37065)
* [Paginação](../c-appendices/c-guidedsearchoutput.md#section_504E7AB570BD49AF9839530DC438EE96)
* [Pesquisas recentes](../c-appendices/c-guidedsearchoutput.md#section_525816A0355C48F8970D89B8FC3F1FFF)
* [Resultados](../c-appendices/c-guidedsearchoutput.md#section_41AC56BB0A084BF59379B06C8BEF2157)
* [Formulário de pesquisa](../c-appendices/c-guidedsearchoutput.md#section_434DA13EA295474C99FFE9F14801CD0E)
* [Classificar](../c-appendices/c-guidedsearchoutput.md#section_558853CD376F4D71BACF211D53085D55)
* [Sugestões](../c-appendices/c-guidedsearchoutput.md#section_6EC104E1DDD94AC799B65E6E61A2FB3C)
* [Zonas](../c-appendices/c-guidedsearchoutput.md#section_AE53A498B440465EAF2286F2AE87D548)

## Banners {#section_88519CAAD25F4BD49D5E517077745B0E}

Exemplo:

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em banners </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um nó de banner individual. Você pode ter vários nós de banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;área&gt; </span> </p> </td> 
   <td colname="col2"> <p> A área na página da Web onde o banner é exibido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;conteúdo&gt; </span> </p> </td> 
   <td colname="col2"> <p> O conteúdo HTML da área do banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Trilha {#section_A7DB0F1DA9ED4CBCAE18395122F3E01E}

No exemplo a seguir, cada vez que o cliente se restringe ainda mais pelas facetas, a seleção é adicionada à navegação estrutural. Cada item é representado como um `<breadcrumb-item>`.

Exemplo:

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags na navegação estrutural </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um link relativo para os resultados da pesquisa que mostra a exibição desejada. Clicar em um link de navegação estrutural leva o cliente a uma visualização em que todos os refinamentos subsequentes são removidos. Outras opções também estão disponíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Texto voltado para o cliente para o item de navegação estrutural. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aspectos {#section_65932C95931743A1BFAF1DF16D7E6D92}

As facetas são opções de refinamento que oferecem aos clientes a capacidade de filtrar nos resultados. As facetas são normalmente usadas para categorização, intervalos de preços, seleções de cores e refinamento de outros atributos. Os metadados no índice são o que move as facetas.

É comum ocultar ou mostrar as facetas de categorização à medida que um cliente se desloca para baixo na categorização. O nível mais alto de categorização (categoria) é conhecido como Nível 1. Quando um cliente clica em uma opção de Camada 1, as opções de refinamento de Camada 2 (subcategoria) aparecem e as opções de Camada 1 desaparecem. Quando um cliente clica em uma opção de Camada 2, as opções de refinamento de Camada 3 (subcategoria) são exibidas e as opções de Camada 2 desaparecem. Como observado acima, essas opções são ocultas e exibidas - seu aplicativo da Web não é afetado por elas.

Cada aspecto está contido em `<facet-item>` tags. No exemplo a seguir, ele mostra uma faceta que permite ao cliente refinar os resultados da pesquisa por &quot;feriado&quot;.

Exemplo:

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item> 
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em aspectos </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Título voltado para o cliente para a faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Rótulo voltado para o cliente para a opção de aspecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Link relativo para resultados que a opção refina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número de resultados nesse conjunto de resultados refinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Quando um valor de faceta é selecionado, o nó retorna um "link para desfazer" que permite que um cliente volte para fora dos resultados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cabeçalho e consulta {#section_1D57062259CA46E0B4F598FA4EB37065}

Exemplo:

```xml
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

Usadas em conjunto, essas tags apresentam uma mensagem como: &quot;Mostrando os resultados 1-16 de 621 para &#39;ano novo&#39;.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags no cabeçalho e na consulta </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> A consulta de palavra-chave enviada com a solicitação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultados inferiores&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número do item do primeiro resultado nesta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultados superiores&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número do item do último resultado desta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número total de resultados que correspondem à consulta do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um campo opcional que se aplica globalmente aos resultados da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Paginação {#section_504E7AB570BD49AF9839530DC438EE96}

Exemplo:

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags na paginação </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número total de páginas de resultados, com base no número de resultados dividido pelo número de resultados por página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a primeira página no conjunto de resultados, a menos que o cliente já esteja visualizando a página 1. Nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a última página do conjunto de resultados, a menos que o cliente esteja visualizando a última página. Nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a página anterior no conjunto de resultados, a menos que o cliente esteja visualizando a página 1; nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a última página do conjunto de resultados, a menos que o cliente esteja visualizando a última página. Nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x" </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para um número de página específico. Dez números de página contíguos são mostrados. Na página 1, seriam as páginas 1 a 10. No final do conjunto de resultados (neste caso, 39), seriam as páginas 30-39. Por exemplo, no centro do conjunto de resultados, página 15, seriam as páginas 11-20. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> seleted="true"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Aplicado como um atributo à página selecionada no momento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pesquisas recentes {#section_525816A0355C48F8970D89B8FC3F1FFF}

Pesquisas recentes é um recurso baseado em cookies que só funciona se você repassar as informações do cookie para os servidores.

Exemplo:

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em pesquisas recentes </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;pesquisa recente&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um nó de pesquisa recente individual. Você pode ter vários nós de pesquisa recentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;termo de pesquisa&gt; </span> </p> </td> 
   <td colname="col2"> <p> O termo que o cliente pesquisou anteriormente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Links para a pesquisa anterior. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultados {#section_41AC56BB0A084BF59379B06C8BEF2157}

O conjunto Resultados é uma área personalizável da resposta JSON. Cada índice é único nos mecanismos de nomeação de campo dos metadados. Há campos comuns que são retornados para cada resultado, como título, descrição e URL. Mas, todos os metadados definidos para uma página no índice podem se tornar disponíveis para uso em cada nó de resultado. Categorização, preços, cores e miniaturas são apenas algumas das opções que podem ser aplicadas a um resultado para produzir resultados de pesquisa mais atraentes.

O formato Resultados é personalizado com base nos metadados específicos da sua implementação. Todos os dados por resultado para exibição nos resultados, incluindo URLs de imagem em miniatura, estão contidos aqui.

Além disso, é possível configurar várias zonas de resultado dentro da página, como &quot;Resultados em destaque&quot;, ou separar as seções de resultados &quot;Produtos&quot; e &quot;Conteúdo&quot;. Nesses casos, várias zonas de resultado são fornecidas no HTML, embora as facetas estejam associadas apenas ao conjunto de resultados principal.

Exemplo:

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags nos resultados </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número de série do resultado dentro desse conjunto de resultados. Neste exemplo, onde dez resultados são mostrados por página, na página 2 dos resultados, o primeiro item teria um índice de 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultado-título&gt; </span> </p> </td> 
   <td colname="col2"> <p> O título voltado para o cliente para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> O URL desta página. É usado para criar um hiperlink que permite ao cliente clicar nos resultados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulário de pesquisa {#section_434DA13EA295474C99FFE9F14801CD0E}

Exemplo:

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags no formulário de pesquisa </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Opcional. Quando presente no JSON, um valor de 1 indica que sua conta está vinculada ao <span class="keyword"> Test&amp;Target </span> e tem pelo menos uma regra de negócios que está em um teste A:B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;completar automaticamente&gt; </span> </p> </td> 
   <td colname="col2"> <p> Opcional. Ao usar o preenchimento automático, esse nó está presente para indicar que o CSS e o JavaScript estão presentes na página, juntamente com o conteúdo que está no formulário. Normalmente, esses campos não são alterados a menos que alguém tenha alterado uma configuração de preenchimento automático. Nesses casos, o campo xxx_cache_ver é incrementado para forçar uma invalidação do conteúdo em cache no navegador do cliente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> O CSS associado ao preenchimento automático. É recomendável colocar essa tag no topo da página para melhorar a renderização da página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Conteúdo que é necessário dentro de sua pesquisa para que o utilitário de preenchimento automático se conecte ao controle correto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> JavaScript personalizado que é necessário para completar automaticamente. É recomendável colocar essa tag abaixo na página para melhorar a renderização da página. O JavaScript da IU também é necessário para o preenchimento automático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém todos os parâmetros ocultos (nome e valor) a serem incluídos no formulário de pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Classificar {#section_558853CD376F4D71BACF211D53085D55}

O exemplo a seguir mostra os dados de um menu de classificação de três opções. O menu permite que o cliente classifique por relevância, título ou classificação. O item atualmente selecionado inclui um atributo &quot;seleted=true&quot;. &quot;. Sempre ofereça uma opção de relevância para permitir que um cliente retorne aos resultados de pesquisa padrão que foram exibidos originalmente.

Exemplo:

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags no menu Classificar </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> O texto voltado para o cliente para a opção. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Representa o valor do parâmetro da string de consulta "classificar" para essa opção. Essa tag não é necessária se o valor <span class="codeph"> &lt;link&gt; </span> for usado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Para as opções não selecionadas, o parâmetro <span class="codeph"> &lt;link&gt; </span> contém o link relativo que retorna o mesmo conjunto de resultados, classificado pelo novo parâmetro de classificação. Este campo está em branco para a opção de classificação atualmente selecionada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sugestões {#section_6EC104E1DDD94AC799B65E6E61A2FB3C}

As sugestões são retornadas quando há apenas alguns resultados ou nenhum resultado. Este nó contém termos que geram consultas bem-sucedidas e podem ser exibidos em uma página &quot;Sem Resultados&quot;. O link também é retornado para que um cliente possa ir para a nova consulta.

Exemplo:

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em sugestões </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Um link relativo usado para criar um hiperlink para pesquisar os resultados do termo de sugestão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>O termo sugerido. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zonas {#section_AE53A498B440465EAF2286F2AE87D548}

Exemplo:

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em zonas </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zona&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um nó de zona individual. Você pode ter vários nós de zona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> O nome da zona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;mostrar&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 ou 0 para indicar se a zona é ou não exibida. O conteúdo real da zona pode ser uma área estática na sua página da Web ou nos resultados da pesquisa, como os melhores vendedores ou produtos relacionados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Saída XML de pesquisa guiada {#reference_D93E859A277643068B10AE7A61C973EA}

Tabelas que descrevem a saída de resposta XML padrão.

Você pode revisar a resposta XML para o seguinte:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_6A19EC26DD3B494194AAA788151B78B5)
* [Trilha](../c-appendices/c-guidedsearchoutput.md#section_E48A71B0EBDB4EDDA7587009AD865488)
* [Aspectos](../c-appendices/c-guidedsearchoutput.md#section_5CEB1F966C004FFEA3CF675638966E25)
* [Cabeçalho e consulta](../c-appendices/c-guidedsearchoutput.md#section_802835E19BCB48239C6770A1B72DFFF8)
* [Paginação](../c-appendices/c-guidedsearchoutput.md#section_72DB86DDE1284B1EA295CFFBC16A3150)
* [Pesquisas recentes](../c-appendices/c-guidedsearchoutput.md#section_BCA2DDD17F264CF6BA11634E1A514E28)
* [Resultados](../c-appendices/c-guidedsearchoutput.md#section_EC496F5CA2634158891455E2F6DF6833)
* [Formulário de pesquisa](../c-appendices/c-guidedsearchoutput.md#section_F92D8C3D37174A10A4E26CAFF3F3DF89)
* [Classificar](../c-appendices/c-guidedsearchoutput.md#section_32DC50A103BF491BA3665A5CADCCAADE)
* [Sugestões](../c-appendices/c-guidedsearchoutput.md#section_D81BCE46F0AF443695DF9C4BA084B716)
* [Zonas](../c-appendices/c-guidedsearchoutput.md#section_15D8AA585F3246799968BA88EE2C9FC2)

## Banners {#section_6A19EC26DD3B494194AAA788151B78B5}

Exemplo:

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em banners </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um nó de banner individual. Você pode ter vários nós de banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;área&gt; </span> </p> </td> 
   <td colname="col2"> <p> A área na página da Web onde o banner é exibido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;conteúdo&gt; </span> </p> </td> 
   <td colname="col2"> <p> O conteúdo HTML da área do banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Trilha {#section_E48A71B0EBDB4EDDA7587009AD865488}

No exemplo a seguir, cada vez que o cliente se restringe ainda mais pelas facetas, a seleção é adicionada à navegação estrutural. Cada item é representado como um `<breadcrumb-item>`.

Exemplo:

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags na navegação estrutural </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um link relativo para os resultados da pesquisa que mostra a exibição desejada. Clicar em um link de navegação estrutural leva o cliente a uma visualização em que todos os refinamentos subsequentes são removidos. Outras opções também estão disponíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Texto voltado para o cliente para o item de navegação estrutural. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aspectos {#section_5CEB1F966C004FFEA3CF675638966E25}

As facetas são opções de refinamento que oferecem aos clientes a capacidade de filtrar nos resultados. As facetas são normalmente usadas para categorização, intervalos de preços, seleções de cores e refinamento de outros atributos. Os metadados no índice são o que move as facetas.

É comum ocultar ou mostrar as facetas de categorização à medida que um cliente se desloca para baixo na categorização. O nível mais alto de categorização (categoria) é conhecido como Nível 1. Quando um cliente clica em uma opção de Camada 1, as opções de refinamento de Camada 2 (subcategoria) aparecem e as opções de Camada 1 desaparecem. Quando um cliente clica em uma opção de Camada 2, as opções de refinamento de Camada 3 (subcategoria) são exibidas e as opções de Camada 2 desaparecem. Como observado acima, essas opções são ocultas e exibidas - seu aplicativo da Web não é afetado por elas.

Cada aspecto está contido em `<facet-item>` tags. No exemplo a seguir, ele mostra uma faceta que permite ao cliente refinar os resultados da pesquisa por &quot;feriado&quot;.

Exemplo:

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item>  
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em aspectos </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Título voltado para o cliente para a faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Rótulo voltado para o cliente para a opção de aspecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Link relativo para resultados que a opção refina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número de resultados nesse conjunto de resultados refinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Quando um valor de faceta é selecionado, o nó retorna um "link para desfazer" que permite que um cliente volte para fora dos resultados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cabeçalho e consulta {#section_802835E19BCB48239C6770A1B72DFFF8}

Exemplo:

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

Usadas em conjunto, essas tags apresentam uma mensagem como: &quot;Mostrando os resultados 1-16 de 621 para &#39;ano novo&#39;.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags no cabeçalho e na consulta </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> A consulta de palavra-chave enviada com a solicitação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultados inferiores&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número do item do primeiro resultado nesta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultados superiores&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número do item do último resultado desta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número total de resultados que correspondem à consulta do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um campo opcional que se aplica globalmente aos resultados da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Paginação {#section_72DB86DDE1284B1EA295CFFBC16A3150}

Exemplo:

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags na paginação </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número total de páginas de resultados, com base no número de resultados dividido pelo número de resultados por página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a primeira página no conjunto de resultados, a menos que o cliente já esteja visualizando a página 1. Nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a última página do conjunto de resultados, a menos que o cliente esteja visualizando a última página. Nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a página anterior no conjunto de resultados, a menos que o cliente esteja visualizando a página 1; nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para a última página do conjunto de resultados, a menos que o cliente esteja visualizando a última página. Nesse caso, está em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x" </span> </p> </td> 
   <td colname="col2"> <p> Contém um link relativo para um número de página específico. Dez números de página contíguos são mostrados. Na página 1, seriam as páginas 1 a 10. No final do conjunto de resultados (neste caso, 39), seriam as páginas 30-39. Por exemplo, no centro do conjunto de resultados, página 15, seriam as páginas 11-20. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> seleted="true"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Aplicado como um atributo à página selecionada no momento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pesquisas recentes {#section_BCA2DDD17F264CF6BA11634E1A514E28}

Pesquisas recentes é um recurso baseado em cookies que só funciona se você repassar as informações do cookie para os servidores.

Exemplo:

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em pesquisas recentes </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;pesquisa recente&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um nó de pesquisa recente individual. Você pode ter vários nós de pesquisa recentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;termo de pesquisa&gt; </span> </p> </td> 
   <td colname="col2"> <p> O termo que o cliente pesquisou anteriormente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Links para a pesquisa anterior. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultados {#section_EC496F5CA2634158891455E2F6DF6833}

O conjunto Resultados é uma área personalizável da resposta XML. Cada índice é único nos mecanismos de nomeação de campo dos metadados. Há campos comuns que são retornados para cada resultado, como título, descrição e URL. Mas, todos os metadados definidos para uma página no índice podem se tornar disponíveis para uso em cada nó de resultado. Categorização, preços, cores e miniaturas são apenas algumas das opções que podem ser aplicadas a um resultado para produzir resultados de pesquisa mais atraentes.

O formato Resultados é personalizado com base nos metadados específicos da sua implementação. Todos os dados por resultado para exibição nos resultados, incluindo URLs de imagem em miniatura, estão contidos aqui.

Além disso, é possível configurar várias zonas de resultado dentro da página, como &quot;Resultados em destaque&quot;, ou separar as seções de resultados &quot;Produtos&quot; e &quot;Conteúdo&quot;. Nesses casos, várias zonas de resultado são fornecidas no HTML, embora as facetas estejam associadas apenas ao conjunto de resultados principal.

Exemplo:

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags nos resultados </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> O número de série do resultado dentro desse conjunto de resultados. Neste exemplo, onde dez resultados são mostrados por página, na página 2 dos resultados, o primeiro item teria um índice de 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultado-título&gt; </span> </p> </td> 
   <td colname="col2"> <p> O título voltado para o cliente para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> O URL desta página. É usado para criar um hiperlink que permite ao cliente clicar nos resultados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulário de pesquisa {#section_F92D8C3D37174A10A4E26CAFF3F3DF89}

Exemplo:

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags no formulário de pesquisa </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Opcional. Quando presente no XML, um valor de 1 indica que sua conta está vinculada ao <span class="keyword"> Test&amp;Target </span> e tem pelo menos uma regra de negócios que está em um teste A:B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;completar automaticamente&gt; </span> </p> </td> 
   <td colname="col2"> <p> Opcional. Ao usar o preenchimento automático, esse nó está presente para indicar que o CSS e o JavaScript estão presentes na página, juntamente com o conteúdo que está no formulário. Normalmente, esses campos não são alterados a menos que alguém tenha alterado uma configuração de preenchimento automático. Nesses casos, o campo xxx_cache_ver é incrementado para forçar uma invalidação do conteúdo em cache no navegador do cliente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> O CSS associado ao preenchimento automático. É recomendável colocar essa tag no topo da página para melhorar a renderização da página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Conteúdo que é necessário dentro de sua pesquisa para que o utilitário de preenchimento automático se conecte ao controle correto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> JavaScript personalizado que é necessário para completar automaticamente. É recomendável colocar essa tag abaixo na página para melhorar a renderização da página. O JavaScript da IU também é necessário para o preenchimento automático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contém todos os parâmetros ocultos (nome e valor) a serem incluídos no formulário de pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Classificar {#section_32DC50A103BF491BA3665A5CADCCAADE}

O exemplo a seguir mostra os dados de um menu de classificação de três opções. O menu permite que o cliente classifique por relevância, título ou classificação. O item atualmente selecionado inclui um atributo &quot;seleted=true&quot;. &quot;. Sempre ofereça uma opção de relevância para permitir que um cliente retorne aos resultados de pesquisa padrão que foram exibidos originalmente.

Exemplo:

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags no menu Classificar </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> O texto voltado para o cliente para a opção. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Representa o valor do parâmetro da string de consulta "classificar" para essa opção. Essa tag não é necessária se o valor <span class="codeph"> &lt;link&gt; </span> for usado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Para as opções não selecionadas, o parâmetro <span class="codeph"> &lt;link&gt; </span> contém o link relativo que retorna o mesmo conjunto de resultados, classificado pelo novo parâmetro de classificação. Este campo está em branco para a opção de classificação atualmente selecionada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sugestões {#section_D81BCE46F0AF443695DF9C4BA084B716}

As sugestões são retornadas quando há apenas alguns resultados ou nenhum resultado. Este nó contém termos que geram consultas bem-sucedidas e podem ser exibidos em uma página &quot;Sem Resultados&quot;. O link também é retornado para que um cliente possa ir para a nova consulta.

Exemplo:

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em sugestões </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Um link relativo usado para criar um hiperlink para pesquisar os resultados do termo de sugestão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>O termo sugerido. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zonas {#section_15D8AA585F3246799968BA88EE2C9FC2}

Exemplo:

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tags em zonas </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zona&gt; </span> </p> </td> 
   <td colname="col2"> <p> Um nó de zona individual. Você pode ter vários nós de zona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> O nome da zona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;mostrar&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 ou 0 para indicar se a zona é ou não exibida. O conteúdo real da zona pode ser uma área estática na sua página da Web ou nos resultados da pesquisa, como os melhores vendedores ou produtos relacionados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Saída XML de pesquisa guiada para o Adobe Experience Manager {#reference_DBE13C606C3A4BB185DE53F88D0D3048}

Tabelas que descrevem a saída de resposta XML padrão para o AEM (Adobe Experience Manager).

Consulte também . [Saída XML de pesquisa guiada](../c-appendices/c-guidedsearchoutput.md#reference_D93E859A277643068B10AE7A61C973EA)

Você pode revisar a resposta XML para o seguinte:

* [Banners](../c-appendices/c-guidedsearchoutput.md#section_B16EDC5533FA4494AC9983AA7357CBE3)
* [Trilha de navegação](../c-appendices/c-guidedsearchoutput.md#section_49EA7043FBE44315A79A4E738BE30114)
* [Campos personalizados](../c-appendices/c-guidedsearchoutput.md#section_38DD31AFE5DD4263A63644AFF484E0F4)
* [Aspectos](../c-appendices/c-guidedsearchoutput.md#section_BE98990E3DD748A1BD4E0CA322314B79)
* [Cabeçalho](../c-appendices/c-guidedsearchoutput.md#section_5305B1DC5774439485CA0665DB683F9C)
* [Menus e classificação](../c-appendices/c-guidedsearchoutput.md#section_A34CBB645DBF4C70A12A5B7E81211295)
* [Paginação](../c-appendices/c-guidedsearchoutput.md#section_E52F81C6A6EB4B8F996157B657EC540F)
* [Consulta](../c-appendices/c-guidedsearchoutput.md#section_3DAA1013F09742869B80F6A361816E6C)
* [Pesquisas recentes](../c-appendices/c-guidedsearchoutput.md#section_17F942F6EC07456DABED7A483AC08446)
* [Resultados](../c-appendices/c-guidedsearchoutput.md#section_155A80B8C4F641678DD9C8F257108412)
* [Formulário de pesquisa](../c-appendices/c-guidedsearchoutput.md#section_9E4B99D4FEDC49629F6C7E866F3A7493)
* [Sugestões](../c-appendices/c-guidedsearchoutput.md#section_2899FACB9AD84F60B3687C1B4EF09E15)
* [Modelo](../c-appendices/c-guidedsearchoutput.md#section_1E2BB2F274B04F5491A4CCCC38F507BD)
* [Zonas](../c-appendices/c-guidedsearchoutput.md#section_26C4A947E7B1474A8E37D86D9579B93E)

## Banners {#section_B16EDC5533FA4494AC9983AA7357CBE3}

A pesquisa/comercialização do site pode gerenciar os banners de um cliente, conectando os banners em várias partes de uma página da Web.

Exemplo de banner:

A seguir está um exemplo de um banner colocado na área das páginas chamada &quot;parte superior&quot;.

```xml
   <banners> 
       <banner> 
           <area><![CDATA[top]]></area> 
           <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
       </banner> 
    </banners> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>banners </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>Contém nós de banner 0-n que indicam cada área de banner e o conteúdo que está conectado a essa área. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>banner </p> </td> 
   <td colname="col2"> <p>banners </p> </td> 
   <td colname="col3"> <p>Um nó de banner individual. Você pode ter vários nós de banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>área </p> </td> 
   <td colname="col2"> <p>banner </p> </td> 
   <td colname="col3"> <p>A área na página da Web onde o banner é exibido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>content </p> </td> 
   <td colname="col2"> <p>banner </p> </td> 
   <td colname="col3"> <p>O conteúdo do banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Trilha de navegação {#section_49EA7043FBE44315A79A4E738BE30114}

Várias navegações estruturais são suportadas. Você pode definir navegações estruturais e seu comportamento correspondente em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**. Além disso, é necessário atribuir um nome exclusivo para cada navegação estrutural definida. O nó XML de navegação estrutural repete todas as navegações estruturais definidas. É recomendável que você exiba apenas uma navegação estrutural nos resultados da pesquisa.

No exemplo a seguir, cada vez que o cliente se restringe ainda mais pelas facetas, a seleção é adicionada à navegação estrutural. Cada item é representado como um `<breadcrumb-item>`.

Exemplo de nó de navegação estrutural:

```xml
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;sp_cs=UTF-8;view=xml]]></link> 
   <value><![CDATA[mens]]></value> 
                <label><![CDATA[]]></label> 
      </breadcrumb-item> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;q1=Channel;sp_cs=UTF-8;view=xml;x1=brand]]></link> 
   <value><![CDATA[Channel]]></value> 
                <label><![CDATA[brand]]></label> 
      </breadcrumb-item> 
   </breadcrumb> 
    </breadcrumbs> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>navegações estruturais </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p> Contém nós de navegação estrutural de 0-n que definem cada navegação estrutural. A maioria dos clientes tem apenas uma trilha de navegação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>trilha </p> </td> 
   <td colname="col2"> <p>navegações estruturais </p> </td> 
   <td colname="col3"> <p> Contém os nós filhos que definem a definição de uma navegação estrutural. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>trilha </p> </td> 
   <td colname="col3"> <p> O nome da trilha de navegação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>item de navegação estrutural </p> </td> 
   <td colname="col2"> <p>Um item individual na navegação estrutural. Cada item denota uma etapa na trilha à medida que o usuário diminui o conjunto de resultados. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>item de navegação estrutural </p> </td> 
   <td colname="col3"> <p> Um link relativo para os resultados da pesquisa que mostra a exibição desejada. Clicar em um link de navegação estrutural leva o cliente a uma visualização em que todos os refinamentos subsequentes são removidos. Outras opções também estão disponíveis, como soltar e remover. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>item de navegação estrutural </p> </td> 
   <td colname="col3"> <p> Texto voltado para o cliente para o item de navegação estrutural. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>item de navegação estrutural </p> </td> 
   <td colname="col3"> <p> A tag label gera um rótulo para um valor de navegação estrutural detalhando qual aspecto foi selecionado para gerar esse item de navegação estrutural. É usado apenas no contexto de um bloco guided-breadcrumb. Para a etapa de termo de consulta, isso está em branco. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Campos personalizados {#section_38DD31AFE5DD4263A63644AFF484E0F4}

Campos personalizados são uma coleção diversa de variáveis com um contexto global. Normalmente, é usado para passar as variáveis para fins de SEO que são definidas nos metadados da página de resultados da pesquisa.

Exemplo de nó de campos personalizados:

```xml
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>campos personalizados </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p> Pode conter nós filhos 0-n que definem campos personalizados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>campo personalizado </p> </td> 
   <td colname="col2"> <p>campos personalizados </p> </td> 
   <td colname="col3"> <p> Opcional. Contém um valor para um determinado campo personalizado indicado pelo atributo name. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aspectos {#section_BE98990E3DD748A1BD4E0CA322314B79}

As facetas são opções de refinamento que oferecem aos clientes a capacidade de filtrar nos resultados. As facetas são normalmente usadas para categorização, intervalos de preços, seleções de cores e refinamento de outros atributos. As facetas são criadas sobre os metadados no índice.

É comum ocultar ou mostrar as facetas de categorização à medida que um cliente se desloca para baixo na categorização. O nível mais alto de categorização (categoria) é conhecido como Nível 1. Quando um cliente clica em uma opção de Camada 1, as opções de refinamento de Camada 2 (subcategoria) aparecem e as opções de Camada 1 desaparecem. Quando um cliente clica em uma opção de Camada 2, as opções de refinamento de Camada 3 (subcategoria) são exibidas e as opções de Camada 2 desaparecem. Como observado acima, essas opções são ocultas e exibidas; seu aplicativo da Web não os afeta.

Cada aspecto está contido em `<facet-item>` tags. No exemplo a seguir, ele mostra uma faceta que permite ao cliente refinar os resultados da pesquisa por &quot;feriado&quot;.

Exemplo de bloco de facetas:

```xml
<facets>          
     <facet> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undo-link> 
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;q2=Mens;sp_staged=1;view=xml;x1=brand;x2=leveli]]></link> 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undolink> 
      </facet-value> 
      </facet> 
     <facet> 
         <facet-title><![CDATA[Sub-Category]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>0</selected> 
      <facet-value>           
              <label><![CDATA[Apparel]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans;q3=Apparel;sp_staged=1;view=xml;x1=leveli;x2=brand;x3=levelii]]></link> 
       <count><![CDATA[3]]></count>                         
      </facet-value>   
      </facet>         
     <facet> 
         <facet-title><![CDATA[Brand]]></facet-title> 
                <behavior><![CDATA[multi-select]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undo-link> 
      <facet-value>        
              <label><![CDATA[Amoura]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Amoura;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[9]]></count>                         
      </facet-value>   
      <facet-value>         
              <label><![CDATA[Armora]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[12]]></count>                        
      </facet-value>   
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Armora Jeans]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora+Jeans;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undolink> 
      </facet-value>   
      <facet-value>           
              <label><![CDATA[Art of Grooming]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Art+of+Grooming;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count>                         
      </facet-value>   
      <facet-value>          
              <label><![CDATA[Bear Co.]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Bear+Co.;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[1]]></count> 
      </facet-value> 
      <facet-value>      
              <label><![CDATA[Citizens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Citizens;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[D&amp;B]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|D%26B;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[17]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[David Yuri]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|David+Yuri;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[2]]></count>    
      </facet-value>   
      </facet> 
    </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>facetas </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>O nó facetas do contêiner que tem 0-n nós filhos representando cada aspecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>faceta </p> </td> 
   <td colname="col2"> <p>facetas </p> </td> 
   <td colname="col3"> <p> Uma única instância de faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facet-title </p> </td> 
   <td colname="col2"> <p>faceta </p> </td> 
   <td colname="col3"> <p>Título voltado para o cliente para a faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>comportamento </p> </td> 
   <td colname="col2"> <p>faceta </p> </td> 
   <td colname="col3"> <p>O comportamento da faceta. Por exemplo, normal, fixo ou seleção múltipla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>selecionado </p> </td> 
   <td colname="col2"> <p>faceta </p> </td> 
   <td colname="col3"> <p>1 se a faceta tiver um valor selecionado, caso contrário, 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>desfazer link </p> </td> 
   <td colname="col2"> <p>faceta </p> </td> 
   <td colname="col3"> <p> Presente somente quando a faceta selecionada. O link Desfazer reverte toda a faceta. Por exemplo, quando é uma faceta de seleção múltipla, ela cancela a seleção de todas as opções selecionadas para a faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>valor de faceta </p> </td> 
   <td colname="col2"> <p>faceta </p> </td> 
   <td colname="col3"> <p>Contém todos os itens de aspecto individuais pertencentes à faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>selecionado </p> </td> 
   <td colname="col2"> <p>valor de faceta </p> </td> 
   <td colname="col3"> <p>Se o item atual com a faceta estiver selecionado, esse nó estará presente e definido como "true". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>valor de faceta </p> </td> 
   <td colname="col3"> <p>Rótulo voltado para o cliente para a opção de aspecto. Por padrão, isso já deve ser feito com escape HTML. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>valor de faceta </p> </td> 
   <td colname="col3"> <p> Link relativo para resultados que a opção refina ainda mais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>count </p> </td> 
   <td colname="col2"> <p>valor de faceta </p> </td> 
   <td colname="col3"> <p>O número de resultados nesse conjunto de resultados refinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>desfazer link </p> </td> 
   <td colname="col2"> <p>valor de faceta </p> </td> 
   <td colname="col3"> <p>Quando um valor de faceta é selecionado, o nó retorna um "link de desfazer" que permite que um cliente selecione novamente essa seleção de faceta individual. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cabeçalho {#section_5305B1DC5774439485CA0665DB683F9C}

Exemplo:

```xml
xml version="1.0" encoding="utf-8" standalone="yes" 
```

## Menus e classificação {#section_A34CBB645DBF4C70A12A5B7E81211295}

Os menus para classificar os resultados são suportados e a alteração do número de resultados a serem retornados por página. Também oferece suporte a um menu de navegação que é útil para usar &quot;pesquisar como navegação&quot;. Uma conta pode definir vários menus do mesmo tipo e usar qualquer um dos menus para a apresentação.

Nó de menus de exemplo:

O exemplo a seguir mostra os dados de um menu de classificação de três opções e de um menu de navegação. O menu de classificação permite que o cliente classifique por relevância, título ou classificação. O item atualmente selecionado inclui um atributo &quot;seleted=true&quot;. &quot;. Sempre ofereça uma opção de relevância para permitir que um cliente retorne aos resultados de pesquisa padrão que foram exibidos originalmente.

```xml
<menus> 
        <menu> 
           <name><![CDATA[sort]]></name>         
             <item selected="true"> 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>   
                    <item> 
                        <label><![CDATA[WOMEN'S]]></label> 
          <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[MEN'S]]></label> 
          <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
          <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
          <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
          <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
          <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[GIFTS & HOME]]></label> 
          <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[CHILDREN & TOYS]]></label> 
          <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[ELECTRONICS]]></label> 
          <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link> 
                    </item> 
        </menu> 
    </menus> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>menus </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>Contém 0-n nós secundários que definem cada menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Todos os aplicativos </p> </td> 
   <td colname="col2"> <p>menus </p> </td> 
   <td colname="col3"> <p>Uma única instância de um menu (corresponde a um menu definido em <span class="uicontrol"> Design </span> &gt; <span class="uicontrol"> Navegação </span> &gt; <span class="uicontrol"> Menus </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>Todos os aplicativos </p> </td> 
   <td colname="col3"> <p>Nome do menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>item </p> </td> 
   <td colname="col2"> <p>Todos os aplicativos </p> </td> 
   <td colname="col3"> <p>Define cada item no menu. O atributo opcional selecionado será definido como true se o item de menu especificado estiver selecionado no momento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>O texto voltado para o cliente para o item de menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>Representa o valor do item de menu (o valor do parâmetro de consulta que o menu também está definido). Essa tag não é necessária se o valor &lt;link&gt; for usado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>item </p> </td> 
   <td colname="col3"> <p>Para as opções não selecionadas, o parâmetro &lt;link&gt; contém o link relativo que retorna o mesmo conjunto de resultados, mas com a opção de menu aplicada. Este campo está em branco para a opção de classificação atualmente selecionada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Paginação {#section_E52F81C6A6EB4B8F996157B657EC540F}

Os conjuntos de resultados são divididos em várias páginas. Normalmente, os clientes exibem de 10 a 20 resultados em uma única página. Os resultados subsequentes são exibidos na próxima página. O XML de paginação permite criar um conjunto de links de navegação para que seus clientes possam navegar, página por página, pelos conjuntos de resultados. Há quatro links de navegação disponíveis: primeiro, último, próximo e anterior. Cada tipo de link permite que os clientes se movam rapidamente pelas páginas para que possam revisar e refinar o que estão procurando, com facilidade.

O exemplo a seguir mostra a paginação de uma pesquisa que está na primeira página com a paginação configurada para mostrar links para cinco páginas.

Exemplo de paginação:

```xml
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
        </pages> 
    </pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>paginação </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p> O número total de páginas de resultados, com base no número de resultados dividido pelo número de resultados por página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total de páginas </p> </td> 
   <td colname="col2"> <p>paginação </p> </td> 
   <td colname="col3"> <p>O número total de páginas nas quais os resultados da pesquisa são distribuídos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>páginas </p> </td> 
   <td colname="col2"> <p>paginação </p> </td> 
   <td colname="col3"> <p>Contém nós de página 0-n que definem cada página na paginação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>página </p> </td> 
   <td colname="col2"> <p>páginas </p> </td> 
   <td colname="col3"> <p>Existem quatro nós de página especiais: primeiro, último, anterior e seguinte. Essas quatro páginas são opcionais e aparecem no conjunto de resultados somente se fizerem sentido. Por exemplo, se você estiver na página 1, não há nenhum link "anterior". Todas as outras páginas indicam uma posição. O número de páginas listadas depende do "número de links para páginas" configurado na interface do usuário da paginação. O atributo "seleted" indica a página na qual o cliente está no momento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Consulta {#section_3DAA1013F09742869B80F6A361816E6C}

Exemplo de nó de consulta:

```xml
    <query> 
        <user-query><![CDATA[mens]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[265]]></total-results> 
    </query> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>query </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p> Um nó global que fornece uma visão geral da consulta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>consulta do usuário </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> A palavra-chave que foi pesquisada. Se você <span class="uicontrol"> quis dizer procurar </span> automaticamente um termo sugerido devido ao termo original não resultar em resultados, ele será refletido na nova palavra-chave que foi pesquisada (consulte o nó de sugestões para obter a palavra-chave original). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resultados mais baixos </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> O número do item do primeiro resultado nesta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resultados superiores </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> O número do item do último resultado desta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total de resultados </p> </td> 
   <td colname="col2"> <p>query </p> </td> 
   <td colname="col3"> <p> O número total de resultados que correspondem à consulta do usuário. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pesquisas recentes {#section_17F942F6EC07456DABED7A483AC08446}

Pesquisas recentes é um recurso baseado em cookies que só funciona se você repassar as informações do cookie para os servidores de pesquisa/comercialização do site.

Exemplo de pesquisas recentes:

```xml
    <recent-searches> 
        <clear-link><![?q=womens&gscr=clear]]></clear-link> 
        <recent-search> 
            <link><![?q=mens]]></link> 
            <label><![CDATA[mens]]></label> 
        <recent-search> 
    </recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>pesquisas recentes </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>O nó só estará presente se a pesquisa tiver pesquisas recentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>clear-link </p> </td> 
   <td colname="col2"> <p>pesquisas recentes </p> </td> 
   <td colname="col3"> <p>O caminho relativo que apaga todas as pesquisas recentes do cliente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pesquisa recente </p> </td> 
   <td colname="col2"> <p>pesquisas recentes </p> </td> 
   <td colname="col3"> <p>Define pesquisas recentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>pesquisa recente </p> </td> 
   <td colname="col3"> <p>O caminho para criar um link que executa uma pesquisa realizada recentemente pelo usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>label </p> </td> 
   <td colname="col2"> <p>pesquisa recente </p> </td> 
   <td colname="col3"> <p>Rótulo de exibição voltado para o cliente para a pesquisa recente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultados {#section_155A80B8C4F641678DD9C8F257108412}

O conjunto Resultados é uma área personalizável da resposta XML. Cada índice é único nos mecanismos de nomeação de campo dos metadados. Há campos comuns que são retornados para cada resultado, como título, descrição e URL. Mas, todos os metadados definidos para uma página no índice podem se tornar disponíveis para uso em cada nó de resultado. Categorização, preços, cores e miniaturas são apenas algumas das opções que podem ser aplicadas a um resultado para produzir resultados de pesquisa mais atraentes.

O formato de resultados é personalizado com base nos metadados específicos da sua implementação. Todos os dados por resultado para exibição nos resultados, incluindo URLs de imagem em miniatura, estão contidos aqui.

Além disso, é possível configurar várias zonas de resultado dentro da página, como &quot;Resultados em destaque&quot;, ou separar as seções de resultados &quot;Produtos&quot; e &quot;Conteúdo&quot;. Nesses casos, várias zonas de resultado são fornecidas no HTML, embora as facetas estejam associadas apenas ao conjunto de resultados principal.

Exemplo de nó de resultados:

```xml
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
                    <field name="sku"><![CDATA[200190]]></field> 
                    <field name="pagename"><![CDATA[Relaxed Paint Splattered]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>   
         <result> 
                    <field name="index"><![CDATA[2]]></field> 
                    <field name="sku"><![CDATA[200195]]></field> 
                    <field name="pagename"><![CDATA[Tumbled Jeans]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[235]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>    
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
                    <field name="sku"><![CDATA[200196]]></field> 
                    <field name="pagename"><![CDATA[Montana Relaxed]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[220]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>         
        </result-set>   
    </results> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>resultados </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>O nó do contêiner para conjuntos de resultados 0-n. Conjuntos de resultados zero significa que você está em uma página de aterrissagem especial sem resultados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>conjunto de resultados </p> </td> 
   <td colname="col2"> <p>resultados </p> </td> 
   <td colname="col3"> <p>Uma pesquisa recebida pode acionar várias pesquisas. Cada conjunto de resultados contém os resultados de uma pesquisa nomeada específica que foi realizada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>conjunto de resultados </p> </td> 
   <td colname="col3"> <p>O nome da pesquisa à qual o conjunto de resultados pertence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>resultado </p> </td> 
   <td colname="col2"> <p>conjunto de resultados </p> </td> 
   <td colname="col3"> <p>Contém todos os campos associados a um resultado individual para o conjunto de resultados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>campo </p> </td> 
   <td colname="col2"> <p>resultado </p> </td> 
   <td colname="col3"> <p>O atributo name define o nome do campo no índice que é exibido. O valor é o valor real para esse campo. Alguns resultados podem ter campos ausentes que não são relevantes para esse resultado individual. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulário de pesquisa {#section_9E4B99D4FEDC49629F6C7E866F3A7493}

O Formulário de pesquisa é incluído no conjunto de resultados para permitir que os clientes criem seus formulários de pesquisa dinamicamente. Esta etapa é opcional. A maioria dos clientes tem um formulário de pesquisa fixo. No entanto, permite que os clientes determinem se o formulário de pesquisa precisa de uma mbox Test&amp;Target, com base em ter pelo menos uma regra de negócios que faça um teste A:B. Da mesma forma, permite que os clientes escolham automaticamente o CSS e o JavaScript de preenchimento automático mais recente.

Exemplo de XML de formulário de pesquisa:

```xml
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>formulário de pesquisa </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>Contém dados para dirigir o formulário de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>include-tnt-mbox </p> </td> 
   <td colname="col2"> <p> formulário de pesquisa </p> </td> 
   <td colname="col3"> <p>Tecnicamente, você só precisa de uma mbox no formulário de pesquisa quando tem pelo menos uma regra comercial fazendo um teste A:B do Test&amp;Target. Este nó indica se você precisa de uma mbox ou se não permite reduzir o número de ocorrências nos servidores do Test&amp;Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>preenchimento automático </p> </td> 
   <td colname="col2"> <p>formulário de pesquisa </p> </td> 
   <td colname="col3"> <p>Ocupa nó filho relacionado ao preenchimento automático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ativado </p> </td> 
   <td colname="col2"> <p>preenchimento automático </p> </td> 
   <td colname="col3"> <p>Defina como 1 quando a conta de pesquisa estiver usando o preenchimento automático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>css </p> </td> 
   <td colname="col2"> <p> preenchimento automático </p> </td> 
   <td colname="col3"> <p> CSS para preenchimento automático. Coloque esse nó o mais alto possível na página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> formulário-content </p> </td> 
   <td colname="col2"> <p>preenchimento automático </p> </td> 
   <td colname="col3"> <p>Conteúdo inserido no formulário de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javascript </p> </td> 
   <td colname="col2"> <p>preenchimento automático </p> </td> 
   <td colname="col3"> <p>JavaScript para completar automaticamente. Coloque esse nó o mais baixo possível na página. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sugestões {#section_2899FACB9AD84F60B3687C1B4EF09E15}

Os clientes podem configurar a funcionalidade de três maneiras: **[!UICONTROL Did You Mean]** faça sugestões devido a nenhum resultado, pesquise automaticamente a primeira sugestão quando não houver resultados ou faça sugestões devido a baixos resultados (quando as sugestões tiverem uma contagem de resultados mais alta). Todas as sugestões produzem resultados.

Esse nó de sugestões contém os termos que geram consultas bem-sucedidas. O link também é retornado para que um cliente possa ir para a nova consulta.

Exemplo de saída para fazer sugestão devido a 0 resultados:

```xml
    <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>0</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=arcade;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[arcade]]></word> 
 </suggestion-item>    
    </suggestions>
```

Exemplo de saída para pesquisar automaticamente em relação a uma sugestão:

```xml
    <suggestions> 
        <auto-searched>1</auto-searched> 
        <orig-query><![CDATA[arcace]]></orig-query> 
        <suggestions-low-results>0</suggestions-low-results>         
    </suggestions> 
```

Exemplo de saída para fazer sugestão devido a baixos resultados:

```xml
   <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>1</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=coffee;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[coffee]]></word> 
 </suggestion-item>  
    </suggestions> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>sugestão </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p> Contém nós filhos que definem sugestão, se houver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pesquisado automaticamente </p> </td> 
   <td colname="col2"> <p>sugestões </p> </td> 
   <td colname="col3"> <p> Se presente, indica se a pesquisa/comercialização do site pesquisou automaticamente um novo termo devido a nenhum resultado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>consulta de procedimento </p> </td> 
   <td colname="col2"> <p>sugestões </p> </td> 
   <td colname="col3"> <p> Quando a pesquisa/comercialização do site pesquisa automaticamente em relação à primeira sugestão, a consulta do usuário no nó de consulta mostra a palavra-chave que é pesquisada. Este nó mostra o termo de consulta original. Combinar os dois permite que os clientes criem estruturas como "Procurando por arco em vez de arco". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sugestões-resultados baixos </p> </td> 
   <td colname="col2"> <p>sugestões </p> </td> 
   <td colname="col3"> <p>Se estiver presente, indica se a pesquisa/comercialização do site está fazendo sugestões devido ao termo de pesquisa atual, resultando em baixos resultados e uma sugestão resultando em resultados consideravelmente maiores. Os dois limites são configuráveis em <span class="uicontrol"> Você quis dizer </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>item de sugestão </p> </td> 
   <td colname="col2"> <p>sugestões </p> </td> 
   <td colname="col3"> <p>Contém nós 0-n que denotam as várias sugestões. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>item de sugestão </p> </td> 
   <td colname="col3"> <p>Contém o caminho para criar um link para o termo sugerido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>palavra </p> </td> 
   <td colname="col2"> <p>item de sugestão </p> </td> 
   <td colname="col3"> <p> Contém a palavra sugerida. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Modelo {#section_1E2BB2F274B04F5491A4CCCC38F507BD}

A capacidade de alternar uma experiência de pesquisa de clientes com base nos resultados é suportada. Parte disso envolve alternar entre diferentes modelos com um layout diferente dos resultados da pesquisa. Por exemplo, você pode ter um modelo com uma exibição em grade de produtos para quando tiver muitos produtos. Ou você pode ter um modelo de &quot;destaque&quot; ao exibir um único resultado que tenha mais detalhes. Você também pode ter um modelo &quot;sem resultados&quot; quando uma pesquisa não produz resultados. O nó do modelo indica qual modelo é usado para exibir os resultados da pesquisa.

Exemplo de modelo:

```xml
<template><![CDATA[grid]]></template>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>modelo </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>Indica o nome do modelo usado para exibir os resultados da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zonas {#section_26C4A947E7B1474A8E37D86D9579B93E}

Zonas são seções das páginas que podem ser ativadas ou desativadas pelas regras de negócios. Uma zona pode conter qualquer conteúdo incluindo, mas não limitado a, aspectos, pesquisas, navegações estruturais, conteúdo estático. As zonas na página da Web do cliente devem mapear para as mesmas áreas que pesquisa/comercialização do site.

Exemplo de nós de zona:

```xml
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nó </p> </th> 
   <th colname="col2" class="entry"> <p>Nó pai </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>zonas </p> </td> 
   <td colname="col2"> <p>resultados do cliente </p> </td> 
   <td colname="col3"> <p>Contém zonas 0-n. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zona </p> </td> 
   <td colname="col2"> <p>zonas </p> </td> 
   <td colname="col3"> <p> Um nó de zona individual. Você pode ter vários nós de zona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>zona </p> </td> 
   <td colname="col3"> <p>O nome da zona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mostrar </p> </td> 
   <td colname="col2"> <p>1 ou 0, indicando se a zona correspondente ao nome da zona é exibida ou oculta. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplos {#reference_64B7D8D228AF4B8D90EDF4DE507B0F84}

Exemplo de saída para uma pesquisa * em um site ficcional chamado Geometrixx e um exemplo de modelo de apresentação usado para produzir a saída de exemplo.

* [Exemplo de saída](../c-appendices/c-guidedsearchoutput.md#section_515C000A18B847D59097D0A9CCC02636)
* [Exemplo de modelo de apresentação](../c-appendices/c-guidedsearchoutput.md#section_AD42571DFB88491AA7F0FDF0929EBE97)

## Exemplo de saída {#section_515C000A18B847D59097D0A9CCC02636}

Exemplo de saída para uma pesquisa * em um site ficcional chamado Geometrixx.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[*]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[1337]]></total-results> 
    </query> 
 
    <custom-fields> 
 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name>

             <item selected="true"> 
 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item>

             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=*;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>

                    <label><![CDATA[WOMEN'S]]></label> 
      <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link>

                    <label><![CDATA[MEN'S]]></label> 
      <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
      <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link>

                    <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
      <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
      <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link>

                    <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
      <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link>

                    <label><![CDATA[GIFTS & HOME]]></label> 
      <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link>

                    <label><![CDATA[CHILDREN & TOYS]]></label> 
      <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link>

                    <label><![CDATA[ELECTRONICS]]></label> 
      <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link>

        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
       
  <breadcrumb-item> 
    <link><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></link> 
    <value><![CDATA[*]]></value> 
                        <label><![CDATA[]]></label> 
   </breadcrumb-item> 
          
   </breadcrumb> 
 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched>0</auto-searched> 
         
        <suggestions-low-results>0</suggestions-low-results> 
         
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
      
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

        </pages> 
    </pagination> 
 
    <facets>  
         
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected>0</selected>

      <facet-value> 
           
              <label><![CDATA[Womens]]></label> 
 
       <link><![CDATA[?i=1;q=*;q1=Womens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[219]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Mens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[202]]></count> 
                         
      </facet-value> 
   
      <facet-value>

              <label><![CDATA[Beauty &amp; Fragrance]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Beauty+%26+Fragrance;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[169]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Children &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Children+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[209]]></count> 
                         
      </facet-value>

      <facet-value> 
           
              <label><![CDATA[Electronics &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Electronics+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[200]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Gifts &amp; Home]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Gifts+%26+Home;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[156]]></count>

      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Jewelry &amp; Accessories]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Jewelry+%26+Accessories;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[182]]></count> 
                         
      </facet-value> 
   
      </facet-item> 
  
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
               
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[2]]></field> 
      <field name="brand"><![CDATA[One For All]]></field> 
      <field name="price"><![CDATA[145]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[208]]></field> 
 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[4]]></field> 
      <field name="brand"><![CDATA[Vera Watson]]></field> 
      <field name="price"><![CDATA[850]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Dresses,  
          Day]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[5]]></field> 
 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[6]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[80]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[7]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[85]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[8]]></field> 
      <field name="brand"><![CDATA[Woolberry]]></field> 
 
      <field name="price"><![CDATA[280]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[9]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[10]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[55]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[11]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[45]]></field> 
 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[12]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[47]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
      
        </result-set>   
    </results>

    <banners> 
         
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
            </banner>

    </banners> 
 
    <zones> 
        <zone> 
 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

## Exemplo de modelo de apresentação {#section_AD42571DFB88491AA7F0FDF0929EBE97}

A seguir está um exemplo de modelo de apresentação usado para produzir a saída de exemplo acima.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[<guided-query-param gsname="q" />]]></user-query> 
 <lower-results><![CDATA[<guided-results-lower>]]></lower-results> 
 <upper-results><![CDATA[<guided-results-upper>]]></upper-results> 
 <total-results><![CDATA[<guided-results-total>]]></total-results> 
    </query> 
 
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[<guided-general-field gsname="default" field="seo_search_keywords"/>]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name> 
     <guided-menu gsname="sort"> 
         <guided-if-menu-item-selected> 
             <item selected="true"> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
        <guided-else-menu-item-selected> 
             <item> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[<guided-menu-item-path />]]></link>     
             </item> 
        </guided-if-menu-item-selected> 
    </guided-menu> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name> 
            <guided-menu gsname="ss_head_nav"> 
                <guided-if-menu-item-selected> 
                    <item selected="true"> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                <guided-else-menu-item-selected> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                </guided-if-menu-item-selected> 
            </guided-menu>  
        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
      <guided-breadcrumb gsname="default"> 
  <breadcrumb-item> 
    <link><![CDATA[<guided-breadcrumb-path gsname="goto">]]></link> 
    <value><![CDATA[<guided-breadcrumb-value />]]></value> 
                        <label><![CDATA[<guided-breadcrumb-label>]]></label> 
   </breadcrumb-item> 
         </guided-breadcrumb> 
   </breadcrumb> 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched><guided-if-suggestion-autosearch>1<guided-else-suggestion-autosearch>0</guided-if-suggestion-autosearch></auto-searched> 
        <guided-if-suggestion-autosearch><orig-query><![CDATA[<guided-suggestion-original-query/>]]></orig-query></guided-if-suggestion-autosearch> 
        <suggestions-low-results><guided-if-suggestion-low-results>1<guided-else-suggestion-low-results>0</guided-if-suggestion-low-results></suggestions-low-results> 
        <guided-suggestions> 
     <suggestion-item> 
         <link><![CDATA[<guided-suggestion-path />]]></link> 
  <word><![CDATA[<guided-suggestion />]]></word> 
     </suggestion-item> 
 </guided-suggestions> 
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[<guided-page-total />]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[<guided-page-path gsname="first" />]]></page> 
     <page position="last"><![CDATA[<guided-page-path gsname="last" />]]></page> 
     <guided-if-page-prev><page position="prev"><![CDATA[<guided-page-path gsname="prev" />]]></page></guided-if-page-prev> 
     <guided-if-page-next><page position="next"><![CDATA[<guided-page-path gsname="next" />]]></page></guided-if-page-next> 
     <guided-if-page-viewall><page position="viewall"><![CDATA[<guided-page-path gsname="viewall" />]]></page></guided-if-page-viewall> 
     <guided-if-page-viewpages><page position="viewall"><![CDATA[<guided-page-path gsname="viewpages" />]]></page></guided-if-page-viewpages> 
 
     <guided-pages> 
                <guided-if-page-selected><page position="<guided-page-number />" selected="true"><![CDATA[<guided-page-path />]]></page> 
  <guided-else-page-selected><page position="<guided-page-number />"><![CDATA[<guided-page-path />]]></page> 
  </guided-if-page-selected> 
     </guided-pages> 
        </pages> 
    </pagination> 
 
    <facets>  
        <guided-facet gsname="leveli"> 
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected><guided-if-facet-selected>1<guided-else-facet-selected>0</guided-if-facet-selected></selected> 
                <guided-if-facet-selected><undo-link><![CDATA[<guided-facet-undo-path gsname="leveli">]]></undo-link></guided-if-facet-selected> 
  <guided-facet-values> 
      <facet-value> 
          <guided-if-facet-value-selected><selected><![CDATA[true]]></selected></guided-if-facet-value-selected> 
              <label><![CDATA[<guided-facet-value>]]></label> 
       <link><![CDATA[<guided-facet-value-path />]]></link> 
       <count><![CDATA[<guided-facet-count>]]></count> 
                        <guided-if-facet-value-selected><undolink><![CDATA[<guided-facet-value-undo-path />]]></undolink></guided-if-facet-value-selected> 
      </facet-value> 
  </guided-facet-values> 
      </facet-item> 
 </guided-facet> 
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
            <guided-results gsname="default">   
         <result> 
                    <field name="index"><![CDATA[<guided-result-index />]]></field> 
      <field name="brand"><![CDATA[<guided-result-field gsname="brand" />]]></field> 
      <field name="price"><![CDATA[<guided-result-field gsname="price" />]]></field> 
      <field name="foundIn"><![CDATA[<guided-if-result-field gsname="leveli"><!--tmpl_var name='leveli'-->, </guided-if-result-field> 
            <guided-if-result-field gsname="levelii"><!--tmpl_var name='levelii'-->, </guided-if-result-field> 
          <guided-if-result-field gsname="leveliii"><!--tmpl_var name='leveliii'--></guided-if-result-field>]]></field> 
         </result>   
     </guided-results> 
        </result-set>   
    </results> 
 
    <guided-if-recent-searches> 
    <recent-searches> 
        <clear-link><guided-recent-searches-clear-path/></clear-link> 
        <guided-recent-searches> 
            <recent-search> 
                <link><guided-recent-searches-path></link> 
                <label><guided-recent-searches-value></label> 
            <recent-search> 
        </guided-recent-searches> 
    </recent-searches> 
    </guided-if-recent-searches> 
 
    <banners> 
        <guided-if-banner-set gsname="top"> 
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<guided-banner gsname="top">]]></content> 
            </banner> 
        </guided-if-banner-set> 
        <guided-if-banner-set gsname="bottom"> 
            <banner> 
                <area><![CDATA[bottom]]></area> 
                <content><![CDATA[<guided-banner gsname="bottom">]]></content> 
            </banner> 
        </guided-if-banner-set> 
    </banners> 
 
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display><guided-if-zone gsname="brand-facet">1<guided-else-zone>0</guided-if-zone></display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox><guided-if-tnt-business-rules>1<guided-else-tnt-business-rules>0</guided-if-tnt-business-rules></include-tnt-mbox> 
        <autocomplete> 
            <enabled><guided-if-autocomplete>1<guided-else-autocomplete>0</guided-if-autocomplete></enabled> 
            <css><![CDATA[<guided-ac-css/>]]></css> 
            <form-content><![CDATA[<guided-ac-form-content/>]]></form-content> 
            <javascript><![CDATA[<guided-ac-javascript/>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

