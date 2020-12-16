---
description: Você pode usar tags meta SEO (Search Engine Otimization) para ajudar a personalizar certos elementos de suas páginas e, assim, melhorar o posicionamento do mecanismo de pesquisa.
seo-description: Você pode usar tags meta SEO (Search Engine Otimization) para ajudar a personalizar certos elementos de suas páginas e, assim, melhorar o posicionamento do mecanismo de pesquisa.
seo-title: Sobre o SEO
solution: Target
subtopic: SEO
title: Sobre o SEO
topic: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 1%

---


# Sobre SEO{#about-seo}

Você pode usar tags meta SEO (Search Engine Otimization) para ajudar a personalizar certos elementos de suas páginas e, assim, melhorar o posicionamento do mecanismo de pesquisa.

## Usando SEO {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B}

Você pode definir cada um desses elementos como um texto inicial seguido por uma lista de palavras. A lista de palavras pode incluir o seguinte:

* Frases de pesquisa populares no site durante um período selecionado (por exemplo, &quot;mês passado&quot;), sujeitas às exclusões personalizadas.
* Conjuntos de valores de um ou mais campos da pesquisa da página.
* Palavras e frases estáticas que você define em uma lista

Os elementos de página mais comuns que as pessoas usam para SEO são o título da página e as tags meta &quot;palavras-chave&quot; e &quot;descrição&quot;. É possível definir configurações para esses três elementos de página. Além disso, você pode definir essas três configurações para cada um dos três tipos de páginas: Pesquisar páginas de resultados, páginas de navegação e páginas de detalhes do item.

Quando você salva ou pré-visualização suas configurações de SEO, pequenos segmentos de modelos de pesquisa (transporte) são gerados que podem ser incluídos em outros modelos de pesquisa com a tag do modelo `<search-include>`. Por exemplo, você pode incluir o campo Título das páginas de resultados da pesquisa em outro modelo com o seguinte:

```
<search-include file="seo/seo_search_title.tpl" />
```

Os nove valores possíveis para o atributo `file` da tag `<search-include>` para os campos SEO são os seguintes:

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

Primeiro, use `<search-include>` conforme descrito acima para incluir os campos desejados em um modelo de pesquisa XML, em um elemento `<general>`.

Em seguida, delimite cada tag `<search-include>` com tags `<general-field>` e `</general-field>`, dando os nomes de campo no atributo `name` como no exemplo a seguir:

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

Em seguida, no modelo de apresentação, você pode usar as tags `<guided-general-field>` para inserir os campos nomeados sempre que precisar, como no exemplo a seguir:

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

Observe o uso do atributo `gsname` para especificar, neste caso, a pesquisa &quot;padrão&quot;.

No total, você pode definir nove campos SEO diferentes que podem ser usados em suas páginas da Web. Eles incluem o seguinte:

* Páginas de resultados da pesquisa - título, descrição e palavras-chave
* Páginas de navegação - título, descrição e palavras-chave
* Páginas de detalhes do item - título, descrição e palavras-chave

Todos os nove campos são definidos com configurações semelhantes. Na verdade, os nomes dos nove campos, como o campo &quot;título&quot; em &quot;Páginas de resultados da pesquisa&quot;, são apenas sugestões de como usá-los. Você pode usar qualquer um dos campos em qualquer contexto nos modelos de apresentação e modelos de pesquisa.

Consulte também [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Consulte também [Marcas de modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

Consulte também [Pesquisar marcas de modelo](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Consulte também [Configurar uma lista de palavras dos resultados da pesquisa](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).

## Configuração de uma lista de palavra de resultados de pesquisa {#task_A459A3734EC04042BA52C81184251DD4}

Você pode configurar a lista de palavras e frases de resultado de pesquisa incluídas em títulos de página, descrições e palavras-chave.

**Para configurar uma lista de palavra dos resultados da pesquisa**

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
      <td colname="col1"> <p>Título | Descrição | Start de palavras-chave com </p> </td> 
      <td colname="col2"> <p>O texto que você deseja exibir na frente da palavra lista. </p> <p>Por exemplo, você pode desejar que a lista de palavras-chave comece com a palavra "Marcas". </p> </td> 
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
      <td colname="col2"> <p>Lista as palavras que você deseja adicionar ao título da página de resultados da pesquisa, ao título da página de navegação ou ao título da página de detalhes do item. </p> <p>Clique em <b>Editar</b> para adicionar palavras à lista. </p> <p>É possível adicionar uma palavra ou frase por linha. Quando terminar, clique em <b>Salvar alterações</b> e feche a página para retornar à página principal do SEO. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover estas palavras e frases (exceto dos valores de campo incluídos) </p> </td> 
      <td colname="col2"> <p>Lista as palavras que você deseja remover do título da página de resultados da pesquisa, do título da página de navegação ou do título da página de detalhes do item. </p> <p>Clique em <b>Editar</b> para adicionar palavras à lista de remoção. </p> <p>É possível adicionar uma palavra ou frase por linha. Quando terminar, clique em <b>Salvar alterações</b> e feche a página para retornar à página principal do SEO. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Clique em **Saída de amostra de Pré-visualização** para pré-visualização dos valores resultantes para os campos SEO que você definiu.

   Consulte [Pré-visualização das meta tags SEO que você configurou](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL SEO Search Results Word List], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuração de uma lista de palavras de páginas de navegação {#task_D7A1D765A92A4D6C94E672B3A86ECB5A}

Você pode configurar a lista de palavras e frases de páginas de navegação incluídas nos títulos, descrições e palavras-chave da página.

**Para configurar uma lista de palavras de páginas de navegação**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Browse Pages]**.
1. Na página [!DNL SEO Browse Pages Word List], nos respectivos grupos [!DNL Title], [!DNL Description] e [!DNL Keywords], defina as opções desejadas.

   Consulte a tabela de opções em [Configurar uma lista de palavras dos resultados da pesquisa](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Opcional) Clique em **Saída de amostra de Pré-visualização** para pré-visualização dos valores resultantes para os campos SEO que você definiu.

   Consulte [Pré-visualização das meta tags SEO que você configurou](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL SEO Browse Pages Word List], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurar uma lista de palavra detalhada do item {#task_761538C519B34164BE189F13C39B2495}

Você pode configurar a lista de palavras e frases detalhadas do item incluídas nos títulos, descrições e palavras-chave da página.

**Para configurar uma lista de palavra detalhada do item**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Item Detail Pages]**.
1. Na página [!DNL SEO Item Detail Word List], nos respectivos grupos [!DNL Title], [!DNL Description] e [!DNL Keywords], defina as opções desejadas.

   Consulte a tabela de opções em [Configurar uma lista de palavras dos resultados da pesquisa](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Opcional) Clique em **Saída de amostra de Pré-visualização** para pré-visualização dos valores resultantes para os campos SEO que você definiu.

   Consulte [Pré-visualização das meta tags SEO que você configurou](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL SEO Item Detail Word List], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Pré-visualização das meta tags SEO que você configurou {#task_3F97949E193C4F92A104AD117FE49621}

É possível pré-visualização os valores resultantes para os campos SEO que você define para ver o que é inserido onde você os usa.

Os campos SEO podem conter valores de campo incluídos, portanto, os resultados da pesquisa podem depender do query de pesquisa especificado.

**Para pré-visualização das meta tags SEO que você configurou**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Na página SEO, clique em **Saída de amostra de Pré-visualização**.
1. Na página [!DNL SEO Preview], no campo [!DNL Enter sample query], digite o termo do query que deseja pesquisar.
1. Clique em **Pesquisa**.

   Os campos Título, Descrição e Palavras-chave resultantes mostram o conteúdo inserido em uma página com base no query de pesquisa que você acabou de inserir.
1. Clique em **Fechar** para voltar à página principal do SEO.
