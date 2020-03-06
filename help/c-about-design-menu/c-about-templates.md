---
description: Você pode usar Modelos para gerenciar seus modelos de apresentação e modelos de transporte.
seo-description: Você pode usar Modelos para gerenciar seus modelos de apresentação e modelos de transporte.
seo-title: Sobre Modelos
solution: Target
title: Sobre Modelos
topic: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
translation-type: tm+mt
source-git-commit: 60cedaac1846e384a37699a42bf7fda33828e1c0

---


# Sobre Modelos{#about-templates}

Você pode usar **[!UICONTROL Templates]** para gerenciar seus modelos de apresentação e de transporte.

## Sobre Modelos {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

Você pode adicionar, editar, copiar, renomear ou excluir modelos de apresentação e modelos de transporte. Quando você clica em um nome de modelo existente na tabela Modelos, ele é aberto em uma janela do editor (ou visualizador) onde você pode fazer suas alterações.

É possível reverter quaisquer alterações feitas nos modelos usando o recurso Histórico na lista suspensa do nome do modelo na tabela Modelos.

Você pode reduzir o peso da página de um modelo de apresentação marcando a caixa de **[!UICONTROL Minimize]** seleção correspondente do modelo na tabela do modelo. Ao reduzir o peso da página do modelo, você minimiza dinamicamente o JavaScript e o CSS em linha. Você também remove o espaço em branco redundante no HTML. Minimizar o peso da página do modelo de apresentação pode ajudar a fornecer os resultados da pesquisa mais rapidamente.

Você pode visualizar a aparência do modelo minimizado clicando na lista suspensa ao lado do nome do arquivo e, em seguida, clicando em **[!UICONTROL Preview minimized]**. Se você minimizar o modelo de apresentação principal, lembre-se de ativar a minimização para modelos incluídos (com `guided-include` tag), pois essa opção não é herdada.

Mesmo se você minimizar um modelo de apresentação, ainda poderá editar a versão &quot;não minimizada&quot; do mesmo modelo.

Você pode usar as regras de pré-pesquisa, pós-pesquisa e de negócios para determinar quando usar um de seus outros modelos de apresentação. É comum ter uma regra como &quot;Para cada pesquisa, defina o modelo direcionado como xxxx&quot;. Com tal regra em vigor, quando você altera o modelo &quot;Padrão&quot; na tabela Modelos, ele parece não ter efeito.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Sobre modelos de apresentação {#section_ACDDEA5C499E481C828A517C230D4596}

Os modelos de apresentação são modelos HTML que um cliente vê quando está visualizando os resultados de sua pesquisa em seu site.

Na camada de apresentação, você pode ter um único modelo de apresentação que apresenta os resultados de várias pesquisas de várias fontes. Você pode definir quantos modelos de apresentação desejar e até mesmo definir modelos de apresentação que outros modelos compartilham usando `include` comandos. O modelo de apresentação é onde todos os componentes do Design, como facetas, menus e navegações estruturais, se juntam. Para exibir os vários componentes de design, você deve usar tags de modelo de apresentação.

Consulte Tags de modelo de [apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Quando você tem mais de um modelo de apresentação, define em que condições os vários modelos de apresentação são usados. Você pode selecionar qual modelo de apresentação usar com base nos parâmetros CGI e cookies recebidos. Ou você pode alternar qual modelo de apresentação está usando com base no resultado de uma pesquisa anterior.

Ao usar vários modelos de apresentação, certifique-se de indicar qual modelo deseja que os resultados da pesquisa apareçam inicialmente. É possível fazer isso usando a **[!UICONTROL Default]** coluna da tabela Modelos.

## Sobre modelos de transporte {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

Os modelos de transporte podem ser modelos XML ou JSON que transmitem dados da pesquisa de back-end para a camada de apresentação da Pesquisa guiada.

Por padrão, sua conta está configurada para usar modelos de transporte XML. No entanto, se você preferir usar JSON para passar seus dados para a Pesquisa guiada, entre em contato com a Adobe Consulting que pode ajudá-lo.

Na camada de apresentação, você pode ter um único modelo de apresentação que apresenta os resultados de várias pesquisas. Cada pesquisa pode usar o mesmo modelo de transporte ou um modelo de transporte personalizado para passar os dados para a camada de apresentação. Como o modelo de transporte é usado apenas para passar dados para a camada de apresentação, ele não deve ter nenhum HTML usado para exibir os resultados da pesquisa. O modelo usa tags de modelo de transporte para passar os resultados da pesquisa e os resultados para preencher os aspectos. Dentro dessas tags, as tags padrão do modelo de pesquisa são usadas para exibir os valores reais.

Consulte [Pesquisar marcas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modelo.

**Tags específicas do modelo de transporte XML**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tag do modelo de transporte XML </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essas são as tags raiz XML que a camada de apresentação usa para detectar o que ela deve analisar fora do modelo de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags delimita tags de modelo de pesquisa que fornecem dados de resumo com base no conjunto de resultados. Normalmente, essas tags contêm tags de pesquisa para o número total de resultados, o resultado mais baixo e o resultado mais alto. Você pode definir qualquer número de campos globais adicionais que desejar com a tag de campo <span class="codeph"> geral </span> . </p> <p> <b>Exemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags está envolvido nos resultados da pesquisa, de modo que a Pesquisa guiada saiba onde procurá-las. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;resultado&gt;&lt;/resultado&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags é vinculado a cada resultado de pesquisa, de modo que a Pesquisa guiada reconheça onde o conteúdo de um único resultado de pesquisa começa e termina. </p> <p> <b>Exemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Essa tag permite executar um loop por cada item em uma lista de vários valores para um único resultado. Use a tag somente em um resultado. Seu objetivo principal é permitir que você itere sobre atributos pertencentes a um campo de resultado. </p> <p> <b>Exemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facetas&gt;&lt;/facetas&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags transmite os resultados que preenchem as facetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cada faceta deve ter suas próprias marcas de aspecto, onde o parâmetro name corresponde ao nome da faceta. As tags de pesquisa são usadas dentro das tags de aspecto para os valores de aspecto. </p> <p>Consulte <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> Sobre aspectos </a>. </p> <p> <b>Exemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/facets&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;sugestões&gt;&lt;/sugestões&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags vincula suas sugestões de Você quis dizer para que a Pesquisa guiada reconheça quais nós XML contêm sugestões. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;sugestão&gt;&lt;/sugestão&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esse conjunto de tags vincula cada sugestão Você quis dizer. </p> <p> <b>Exemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;value&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/value&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;count&gt;&lt;search-suggestion-result-count&nbsp;/&gt;&lt;/count&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-if-suggestions&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Tags específicas do modelo de transporte JSON**

Sabe-se que passar JSON versus XML do mecanismo de pesquisa é mais rápido porque é uma carga menor e um analisador mais rápido. No entanto, tenha cuidado ao usar JSON para garantir que a saída seja JSON estrita, pois o analisador não está perdoando.

Se você for novo no JSON, poderá usar os seguintes links e exemplos para ajudá-lo a começar:

* Uma introdução ao JSON. Consulte [https://www.json.org/](https://www.json.org/).
* Teste seu JSON para garantir que ele seja válido. Consulte [https://jsonlint.com/](https://jsonlint.com/).

**Exemplo de modelo JSON**

```
{ 
 "general": 
 { 
  "total" : "<search-total />", 
  "lower" : "<search-lower />", 
  "upper" : "<search-upper />", 
  "rbt-trigger-list" : "<search-rbta-trigger-id-list>", 
  "fields" :  
  [ 
   { 
    "name" : "seo_search_title", 
    "value" : "<search-include file="seo/seo_search_title.tpl" />" 
   }, 
   { 
    "name" : "seo_search_keywords", 
    "value" : "<search-include file="seo/seo_search_keywords.tpl" />" 
   } 
  ] 
 }, 
 
 <search-if-suggestions> 
 "suggestions": 
  [ 
  <search-suggestions> 
  { 
   "suggestion":"<search-suggestion-text />", 
   "count": "<search-suggestion-result-count>" 
  }<search-if-not-last-suggestion>,</search-if-not-last-suggestion> 
  </search-suggestions> 
 ], 
 </search-if-suggestions> 
 
 "facets" : 
 [ 
  { 
   "name" : "leveli", 
   "values" : [ <search-field-value-list name="leveli" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="leveli" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" :"levelii", 
   "values" : [<search-field-value-list name="levelii" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="levelii" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" : "brand", 
   "values" : [<search-field-value-list name="brand" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="brand" quotes="no" sortby="values" data="results" />] 
  }, 
 ], 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    }, 
    { 
     "name" : "title", 
     "value" : "<search-display-field name="title" encoding="json"/>" 
    }, 
    { 
     "name" : "img_url_thumbnail", 
     "value" : "<search-display-field name="img_url_thumbnail" encoding="json"/>" 
    }, 
    { 
     "name" : "description", 
     "value" : "<search-display-field name="description" encoding="json"/>" 
    }, 
    { 
     "name" : "mdi", 
     "value" : "<SEARCH-RBTA-DISPLAY-MDI-FIELD>" 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Exemplo de seção de resultado JSON com uma tabela de atributos de resultados**

```
{ 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    } 
   ], 
   "tables" : 
   [ 
    { 
     "name" : "downloads", 
     "fields" : 
     [ 
      { 
       "name" : "download_title", 
       "value" : <search-display-field name="download_title" encoding="json"/> 
      }, 
      { 
       "name" : "download_link", 
       "value" : <search-display-field name="download_link" encoding="json"/> 
      } 
     ] 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Exemplo de seção JSON Facet para uma faceta com campos associados**

```
{ 
 facets" : 
 [ 
  { 
   "name" : "t1", 
   "values" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
   "counts" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="results" sortby="values" />], 
   "custom-fields" : 
   [ 
    { 
     "name" : "taxonmyId", 
     "value" : [<search-field-value-list name="tax1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />] 
    } 
   ] 
  } 
 ] 
}
```

**Exemplo de seção JSON Facet para aspectos com slot**

```
{ 
  "facets" : 
  [  
   { 
    "name" : "fvalue0", 
                  "dynamic" : 1, 
                  "display-names" : [<search-field-value-list name="fname0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "values" : [<search-field-value-list name="fvalue0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "counts" : [<search-field-value-list name="fvalue0" quotes="no" commas="yes" data="results" sortby="values" />] 
   } 
  ] 
} 
```

## Adicionar uma nova apresentação ou um novo arquivo de modelo de transporte {#task_73199757B6E748CAA604902FF913F012}

Você pode usar **[!UICONTROL Add Template]** para adicionar modelos de apresentação (.tmpl) ou modelos de transporte (.tpl) à [!DNL Templates] página.

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**Para adicionar uma nova apresentação ou um novo arquivo de modelo de transporte**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, clique em **[!UICONTROL Add New Template]**.
1. Na caixa de [!DNL Add Template] diálogo, defina as opções desejadas.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | Opção | Descrição |
   |--- |--- |
   | Novo nome de arquivo | Especifica o nome do modelo que você deseja adicionar. A extensão de arquivo adequada é adicionada automaticamente ao nome do arquivo, com base no tipo de modelo selecionado.  Os modelos de apresentação têm uma extensão de arquivo .tmpl; Os modelos de transporte têm uma extensão de arquivo .tpl. |
   | Novo tipo de modelo | Permite que você escolha uma apresentação ou um modelo de transporte que deseja adicionar.  Consulte [Sobre Modelos](../c-about-design-menu/c-about-templates.md). |

   Consulte também [Edição de uma apresentação ou de um modelo](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.
1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Na [!DNL Templates] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma apresentação ou um modelo de transporte {#task_800E0E2265C34C028C92FEB5A1243EC3}

Você pode usar o Editor de modelos para exibir e editar o conteúdo de sua apresentação e os arquivos de modelo de transporte.

<!-- 

t_editing_a_template.xml

 -->

Você pode editar e testar a apresentação em etapas e os modelos de transporte, enquanto os visitantes do seu site continuam a usar as versões ao vivo dos seus modelos. Você testa seu modelo preparado usando a versão preparada do URL do domínio de pesquisa. Por exemplo, você pode testar o modelo de transporte preparado executando uma consulta preparada ( `sp_staged=1`) com `sp_t` o nome definido para o modelo de transporte. Quando estiver satisfeito com a forma como o layout é exibido, você pode usar **[!UICONTROL Push Live]** de dentro do editor de modelo para colocar o modelo ao vivo. Depois que o modelo é exibido, os visitantes do site começam a usá-lo.

Use a referência de tag do modelo de apresentação para saber como conectar o modelo de apresentação aos componentes de Pesquisa guiada, como facetas, navegações estruturais e menus.

Consulte Tags de modelo de [apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Use a referência de tag do modelo de transporte para saber mais sobre as tags a serem usadas nos modelos de transporte.

Consulte Tags de modelo [de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, clique em uma apresentação ou no nome de um arquivo de modelo de transporte.
1. Na [!DNL Template Editor] página, faça as alterações desejadas nas tags e na codificação.

   Tenha cuidado com as mudanças que você faz no [!DNL Template Editor]; não há nenhum recurso Desfazer. Se você fizer uma alteração indesejada e quiser voltar à versão anterior do arquivo, clique em **[!UICONTROL Cancel]** para retornar à tabela de modelos (assumindo que não salvou nenhuma de suas alterações até esse ponto). Se você já salvou as alterações, poderá usá-las **[!UICONTROL History]** no editor para revertê-las.
1. (Opcional) Clique em **[!UICONTROL Insert Symbol]** para inserir caracteres e símbolos especiais que não tenham teclas correspondentes em teclados em inglês dos EUA.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Feche a página Editor de modelos quando terminar; você retornará à página Modelos.

## Copiando uma apresentação ou um arquivo de modelo de transporte {#task_B744AB3384C84DD59C33CD25E18C2C90}

Você pode usar **[!UICONTROL Copy Template]** para economizar tempo duplicando um modelo de Apresentação existente (.tmpl) ou um modelo de Transporte (.tpl) e adicioná-lo à página Modelos.

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

É necessário alterar o nome do modelo, o tipo de modelo ou ambos. Se você não fizer alterações, o modelo não será copiado.

Você deve ter um modelo já adicionado para poder copiar um modelo.

Consulte [Adicionar uma nova apresentação ou arquivo](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de modelo de transporte.

**Para copiar uma apresentação ou um arquivo de modelo de transporte**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, na lista suspensa ao lado do nome do modelo que você deseja copiar, clique em **[!UICONTROL Copy]**.
1. Na caixa de [!DNL Copy Template] diálogo, defina uma ou mais das opções desejadas.
1. Clique em **[!UICONTROL Copy]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Renomear uma apresentação ou um arquivo de modelo de transporte {#task_CC30050FC2DE4898BF44379D8378EB31}

Você pode usar [!DNL Rename Template] para alterar o nome de um modelo de apresentação existente (.tmpl) ou de um modelo de transporte (.tpl).

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

Você também pode alterar o tipo de modelo, se desejado.

Você já deve ter um modelo adicionado para renomear um modelo.

Consulte [Adicionar uma nova apresentação ou arquivo](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de modelo de transporte.

**Para renomear uma apresentação ou um arquivo de modelo de transporte**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, na lista suspensa ao lado do nome de um modelo que você deseja renomear, clique em **[!UICONTROL Rename]**.
1. Na caixa de [!DNL Rename Template] diálogo, defina uma ou mais das opções desejadas.
1. Clique em **[!UICONTROL Rename]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma apresentação ou um arquivo de modelo de transporte {#task_67E532C2B83A449687737E3B06C5AA58}

Você pode usar **[!UICONTROL Delete Template]** para remover um modelo de apresentação existente (.tmpl) ou um modelo de transporte (.tpl).

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

Você já pode ter uma versão correspondente do modelo preparado que é enviado ao vivo. Em caso positivo, certifique-se de colocar o modelo excluído ao vivo usando **[!UICONTROL Staging]** para que ele também seja excluído do ambiente ativo. Ou você pode usar **[!UICONTROL Push Live]** na página Modelos.

Consulte [Sobre armazenamento temporário](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

Você já deve ter um modelo adicionado para poder excluir um modelo.

Consulte [Adicionar uma nova apresentação ou arquivo de modelo de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**Para excluir uma apresentação ou um arquivo de modelo de transporte**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, na lista suspensa ao lado do nome do modelo que você deseja excluir, clique em **[!UICONTROL Delete]**.
1. Na caixa de [!DNL Delete Template] diálogo, clique em **[!UICONTROL Delete.]**
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A visualização do modelo de apresentação foi minimizada {#task_1757B6207CC74221AE4BFFE5674D320B}

Você pode usar **[!UICONTROL Preview minimized]** para ver como seria a espessura reduzida de uma página de um modelo de apresentação se optar por minimizá-lo.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

Se você minimizar o modelo de apresentação principal, lembre-se de ativar a minimização para modelos incluídos (com tag de inclusão guiada), pois essa opção não é herdada.

Consulte [Reduzindo o peso da página de um modelo de apresentação em...](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

Você já deve ter um modelo adicionado para visualizar o modelo minimizado.

Consulte [Adicionar uma nova apresentação ou arquivo de modelo de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

Você pode visualizar o código XML de um arquivo de modelo de transporte.

Consulte [Visualizar o XML de um arquivo de modelo de transporte](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**Para visualizar o modelo de apresentação minimizado**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, na lista suspensa ao lado do nome do modelo de apresentação, clique em **[!UICONTROL Preview minimized]**.

   Use a **[!UICONTROL Type]** coluna na tabela Modelos para classificar os modelos por Apresentação e Transporte.
1. (Opcional) Na [!DNL Preview Minimized Template] página, marque **[!UICONTROL Wrap lines]** para ler as tags na janela definida.
1. Clique em **[!UICONTROL Close]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Redução do peso da página de um modelo de apresentação em seu site {#task_B09BB3CE89714DEAAE8D9A899CF3009E}

Você pode reduzir a espessura da página de um modelo de apresentação usando a **[!UICONTROL Minimize]** opção na tabela de modelo.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

Ao reduzir o peso da página do modelo, você minimiza dinamicamente o JavaScript e o CSS em linha. Você também remove o espaço em branco redundante no HTML. Minimizar o peso da página do modelo de apresentação pode ajudar a fornecer os resultados da pesquisa mais rapidamente.

Você também pode visualizar a aparência do modelo de apresentação minimizado usando **[!UICONTROL Preview minimized]**.

Consulte [Visualizar o modelo de apresentação minimizado](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, na [!DNL Minimize] coluna, marque a caixa de seleção de um ou mais arquivos de modelo de apresentação que você deseja enviar como mínimo em seu site.

   Use a **[!UICONTROL Type]** coluna na [!DNL Templates] tabela para classificar os modelos por Apresentação e Transporte.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurar o arquivo de modelo de apresentação padrão para usar em seu site {#task_C1E8CE817E4D43E096167A347C54DD53}

Quando você tem vários modelos de apresentação, pode indicar qual modelo será usado inicialmente para exibir os resultados da pesquisa.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

Você pode usar as regras de pré-pesquisa, pós-pesquisa e de negócios para determinar quando um de seus outros modelos de apresentação deve ser usado.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

É comum ter uma regra como &quot;Para cada pesquisa, defina o modelo de apresentação direcionada como xxxx.&quot; Com tal regra em vigor, a alteração do modelo &quot;padrão&quot; na página Modelos parece não ter efeito.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, na [!DNL Default] coluna, clique no botão de opção para o arquivo de modelo de apresentação correspondente que você deseja servir como padrão.

   Use a **[!UICONTROL Type]** coluna na [!DNL Templates] tabela para classificar os modelos por Apresentação e Transporte.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualização do XML de um arquivo de modelo de transporte {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

Você pode usar [!DNL Preview] para revisar o XML de um modelo de transporte que você adicionou.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

Você deve ter um modelo de transporte já adicionado para visualizar o XML do modelo.

Consulte [Adicionar uma nova apresentação ou arquivo](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de modelo de transporte.

É possível visualizar arquivos de modelo de apresentação minimizados para exibir a espessura reduzida da página.

Consulte [Visualizar o modelo de apresentação minimizado](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**Para visualizar o XML de um arquivo de modelo de transporte**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Na [!DNL Templates] página, na lista suspensa ao lado do nome de um modelo de transporte, clique em **[!UICONTROL Preview]**.

   Use a **[!UICONTROL Type]** coluna na [!DNL Templates] tabela para classificar os modelos por Apresentação e Transporte.
1. Feche a janela de visualização e volte para [!DNL site search/merchandising].
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

