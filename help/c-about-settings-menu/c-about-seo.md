---
description: Você pode usar meta tags SEO (Otimização do mecanismo de pesquisa) para ajudar a adaptar determinados elementos de suas páginas e, portanto, melhorar a posição do mecanismo de pesquisa.
solution: Target
subtopic: SEO
title: Sobre a SEO
topic: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 1%

---


# Sobre SEO{#about-seo}

Você pode usar meta tags SEO (Otimização do mecanismo de pesquisa) para ajudar a adaptar determinados elementos de suas páginas e, portanto, melhorar a posição do mecanismo de pesquisa.

## Uso de SEO {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B}

Você pode definir cada um desses elementos como uma parte do texto inicial seguida de uma lista de palavras. A lista de palavras pode incluir o seguinte:

* Frases de pesquisa populares no site durante um período de tempo selecionado (por exemplo, &quot;último mês&quot;), sujeitas às suas exclusões personalizadas.
* Conjuntos de valores de um ou mais campos da pesquisa de onde a página veio.
* Palavras estáticas e frases definidas em uma lista

Os elementos de página mais comuns que as pessoas usam para SEO são o título da página e as metatags de &quot;palavras-chave&quot; e &quot;descrição&quot;. Você pode definir configurações para esses três elementos de página. Além disso, você pode definir essas três configurações para cada um dos três tipos de páginas: Páginas de resultados da pesquisa, Páginas de navegação e Páginas de detalhes do item.

Ao salvar ou visualizar suas configurações de SEO, são gerados pequenos segmentos de modelos de pesquisa (transporte) que podem ser incluídos em outros modelos de pesquisa com a tag de modelo `<search-include>`. Por exemplo, você pode incluir o campo Título das páginas dos resultados da pesquisa em outro modelo com o seguinte:

```
<search-include file="seo/seo_search_title.tpl" />
```

Os nove valores possíveis para o atributo `file` da tag `<search-include>` para campos SEO são os seguintes:

* `seo/seo_search_title.tpl`
* `seo/seo_search_description.tpl`
* `seo/seo_search_keywords.tpl`
* `seo/seo_browse_title.tpl`
* `seo/seo_browse_description.tpl`
* `seo/seo_browse_keywords.tpl`
* `seo/seo_item_title.tpl`
* `seo/seo_item_description.tpl`
* `seo/seo_item_keywords.tpl`

Para usar campos SEO em um modelo de apresentação, conclua várias etapas.

Primeiro, use `<search-include>` conforme descrito acima para incluir os campos desejados em um modelo de pesquisa XML, dentro de um elemento `<general>`.

Em seguida, rode cada tag `<search-include>` com tags `<general-field>` e `</general-field>`, dando os nomes de campo no atributo `name` como no exemplo a seguir:

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

Em seguida, no modelo de apresentação, você pode usar tags `<guided-general-field>` para inserir os campos nomeados sempre que precisar, como no exemplo a seguir:

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

Observe o uso do atributo `gsname` para especificar, nesse caso, a pesquisa &quot;padrão&quot;.

Juntos, você pode definir nove campos de SEO diferentes que podem ser usados em suas páginas da Web. Eles incluem:

* Páginas de resultados da pesquisa - título, descrição e palavras-chave
* Páginas de navegação - título, descrição e palavras-chave
* Páginas de detalhes do item - título, descrição e palavras-chave

Todos os nove campos são definidos com configurações semelhantes. Na verdade, os nomes dos nove campos, como o campo &quot;título&quot; em &quot;Páginas de resultados da pesquisa&quot;, são apenas sugestões de como você pode usá-los. Você pode usar qualquer um dos campos em qualquer contexto nos modelos de apresentação e de pesquisa.

Consulte também [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Consulte também [Tags de modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

Consulte também [Pesquisar marcas de modelo](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Consulte também [Configuração de uma lista de palavras de resultados de pesquisa](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).

## Configurar uma lista de palavras de resultados de pesquisa {#task_A459A3734EC04042BA52C81184251DD4}

Você pode configurar a lista de palavras e frases de resultados de pesquisa incluídas em títulos, descrições e palavras-chave da página.

**Para configurar uma lista de palavras de resultados de pesquisa**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Na página [!DNL SEO Browse Pages Word List], nos respectivos grupos [!DNL Title], [!DNL Description] e [!DNL Keywords], defina as opções desejadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Título | Descrição | Palavras-Chave Começa com </p> </td> 
      <td colname="col2"> <p>O texto que você deseja exibir na frente da lista de palavras. </p> <p>Por exemplo, você pode desejar que a lista de Palavras-chave comece com a palavra "Marcas". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir pesquisas populares durante </p> </td> 
      <td colname="col2"> <p>O período de tempo para o qual as pesquisas são incluídas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Contagem máxima de pesquisa </p> </td> 
      <td colname="col2"> <p>O número máximo de pesquisas incluídas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir valores de campo </p> </td> 
      <td colname="col2"> <p>Os valores de campo incluídos na lista de palavras de resultados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adicionar Estas Palavras E Frases </p> </td> 
      <td colname="col2"> <p>Liste as palavras que deseja adicionar ao título da página de resultados da pesquisa, ao título da página de navegação ou ao título da página de detalhes do item. </p> <p>Clique em <b>Editar</b> para adicionar palavras à lista. </p> <p>Você pode adicionar uma palavra ou frase por linha. Quando terminar, clique em <b>Save Changes</b> e feche a página para retornar à página principal do SEO. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover estas palavras e frases (exceto dos valores de campo incluídos) </p> </td> 
      <td colname="col2"> <p>Liste as palavras que deseja remover do título da página de resultados da pesquisa, do título da página de navegação ou do título da página de detalhes do item. </p> <p>Clique em <b>Editar</b> para adicionar palavras à lista de remoção. </p> <p>Você pode adicionar uma palavra ou frase por linha. Quando terminar, clique em <b>Save Changes</b> e feche a página para retornar à página principal do SEO. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Clique em **Visualizar Saída de Amostra** para visualizar os valores resultantes para os campos SEO que você definiu.

   Consulte [Visualização das meta tags de SEO que você configurou](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL SEO Search Results Word List] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuração de uma lista de palavras de páginas de navegação {#task_D7A1D765A92A4D6C94E672B3A86ECB5A}

Você pode configurar a lista de palavras e frases de páginas de navegação incluídas em títulos, descrições e palavras-chave da página.

**Para configurar uma lista de palavras de páginas de navegação**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Browse Pages]**.
1. Na página [!DNL SEO Browse Pages Word List], nos respectivos grupos [!DNL Title], [!DNL Description] e [!DNL Keywords], defina as opções desejadas.

   Consulte a tabela de opções em [Configuração de uma lista de palavras de resultados de pesquisa](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Opcional) Clique em **Visualizar Saída de Amostra** para visualizar os valores resultantes para os campos SEO que você definiu.

   Consulte [Visualização das meta tags de SEO que você configurou](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL SEO Browse Pages Word List] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurar uma lista de palavras de detalhes do item {#task_761538C519B34164BE189F13C39B2495}

É possível configurar a lista de palavras e frases detalhadas do item incluídas em títulos, descrições e palavras-chave da página.

**Para configurar uma lista de palavras de detalhes do item**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Item Detail Pages]**.
1. Na página [!DNL SEO Item Detail Word List], nos respectivos grupos [!DNL Title], [!DNL Description] e [!DNL Keywords], defina as opções desejadas.

   Consulte a tabela de opções em [Configuração de uma lista de palavras de resultados de pesquisa](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Opcional) Clique em **Visualizar Saída de Amostra** para visualizar os valores resultantes para os campos SEO que você definiu.

   Consulte [Visualização das meta tags de SEO que você configurou](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL SEO Item Detail Word List] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Pré-visualização das meta tags de SEO que você configurou {#task_3F97949E193C4F92A104AD117FE49621}

É possível visualizar os valores resultantes para os campos de SEO definidos para ver o que é inserido onde você os usa.

Os campos SEO podem conter valores de campo incluídos, de modo que os resultados da pesquisa podem depender da consulta de pesquisa especificada.

**Para visualizar as meta tags de SEO que você configurou**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Na página SEO, clique em **Visualizar Saída de Amostra**.
1. Na página [!DNL SEO Preview], no campo [!DNL Enter sample query], digite o termo de consulta que deseja pesquisar.
1. Clique em **Pesquisa**.

   Os campos Título, Descrição e Palavras-chave resultantes mostram o conteúdo inserido em uma página com base na consulta de pesquisa recém-inserida.
1. Clique em **Fechar** para retornar à página principal do SEO.
