---
description: Use o menu Rastreamento para definir a data e as máscaras de URL, senhas, tipos de conteúdo, conexões, definições de formulário e pontos de entrada de URL.
seo-description: Use o menu Rastreamento para definir a data e as máscaras de URL, senhas, tipos de conteúdo, conexões, definições de formulário e pontos de entrada de URL.
seo-title: Sobre o menu Rastreamento
solution: Target
subtopic: Crawling
title: Sobre o menu Rastreamento
topic: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '11033'
ht-degree: 0%

---


# Sobre o menu Rastreamento{#about-the-crawling-menu}

Use o menu Rastreamento para definir a data e as máscaras de URL, senhas, tipos de conteúdo, conexões, definições de formulário e pontos de entrada de URL.

## Sobre pontos de entrada de URL {#concept_5D857E3B5C124E85BC0B5AE77A509573}

A maioria dos sites tem um ponto de entrada ou home page principal que um cliente visita inicialmente. Este ponto de entrada principal é o endereço URL a partir do qual o robô de pesquisa inicia o rastreamento de índice. No entanto, se o site tiver vários domínios ou subdomínios, ou se partes do site não estiverem vinculadas do ponto de entrada principal, você poderá usar os Pontos de entrada do URL para adicionar mais pontos de entrada.

Todas as páginas do site abaixo de cada ponto de entrada de URL especificado são indexadas. Você pode combinar pontos de entrada de URL com máscaras para controlar exatamente quais partes de um site você deseja indexar. É necessário recriar o índice do site antes que os efeitos das configurações de Pontos de entrada do URL fiquem visíveis para os clientes.

O ponto de entrada principal normalmente é o URL do site que você deseja indexar e pesquisar. Você configura esse ponto de entrada principal em Configurações da conta.

Consulte [Definição das definições da sua conta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Depois de especificar o ponto de entrada principal do URL, você pode especificar outros pontos de entrada que deseja rastrear em ordem. Frequentemente, você especificará pontos de entrada adicionais para páginas da Web que não estão vinculadas de páginas no ponto de entrada principal. Especifique pontos de entrada adicionais quando o site abranger mais de um domínio, como no exemplo a seguir:

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

Você qualifica cada ponto de entrada com uma ou mais das seguintes palavras-chave separadas por espaço na tabela abaixo. Essas palavras-chave afetam como a página é indexada.

**Importante**: Certifique-se de separar uma determinada palavra-chave do ponto de entrada e uma da outra por um espaço; uma vírgula não é um separador válido.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Palavra-chave </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Se você não quiser indexar o texto na página do ponto de entrada, mas quiser seguir os links da página, adicione 
     <code>
       noindex 
     </code> após o ponto de entrada. </p> <p>Separe a palavra-chave do ponto de entrada por um espaço, como no exemplo a seguir: </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>Essa palavra-chave equivale a uma meta tag de robôs com 
     <code>
       content="noindex" 
     </code>) entre a variável 
     <code>
       &lt;head&gt; 
     </code>... 
     <code>
       &lt;/head&gt; 
     </code> tags da página do ponto de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Se você quiser indexar o texto na página do ponto de entrada, mas não quiser seguir nenhum dos links da página, adicione 
     <code>
       nofollow 
     </code> após o ponto de entrada. </p> <p>Separe a palavra-chave do ponto de entrada por um espaço, como no exemplo a seguir: </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>Essa palavra-chave equivale a uma meta tag de robôs com 
     <code>
       content="nofollow" 
     </code> entre 
     <code>
       &lt;head&gt; 
     </code>... 
     <code>
       &lt;/head&gt; 
     </code> marca de uma página de ponto de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formulário </p> </td> 
   <td colname="col2"> <p> Quando o ponto de entrada for uma página de logon, 
     <code>
       form 
     </code> é normalmente usado para que o robô de pesquisa possa enviar o formulário de logon e receber os cookies apropriados antes de rastrear o site. Quando a palavra-chave "formulário" é usada, a página do ponto de entrada não é indexada e o robô de pesquisa não marca a página do ponto de entrada como rastreada. Use 
     <code>
       nofollow 
     </code> se você não quiser que o robô de pesquisa siga os links da página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte também [Sobre tipos de conteúdo](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

Consulte também [Sobre o Conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84).

## Adicionando vários pontos de entrada de URL que você deseja indexar {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Se o site tiver vários domínios ou subdomínios e você quiser que eles sejam rastreados, você poderá usar pontos de entrada de URL para adicionar mais URLs.

Para definir o ponto de entrada principal do URL do site, use Configurações da conta.

Consulte [Definição das definições da sua conta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

**Para adicionar vários pontos de entrada de URL que você deseja indexar**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**.
1. Na página [!DNL URL Entrypoints], no campo [!DNL Entrypoints], insira um endereço de URL por linha.
1. (Opcional) Na lista suspensa **[!UICONTROL Add Index Connector Configurations]**, selecione um conector de índice que deseja adicionar como ponto de entrada para indexação.

   A lista suspensa só estará disponível se você tiver adicionado anteriormente uma ou mais definições de conector de índice.

   ![](assets/url_entrypoints_index_connector.png)

   Consulte [Adicionar uma definição de Conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre as máscaras de URL {#concept_8039DFC53FF3410AA494D602F71BA164}

As máscaras de URL são padrões que determinam qual de seu site documentos o robô de pesquisa indexa ou não índices.

Certifique-se de recriar o índice do site para que os resultados das máscaras de URL fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

A seguir estão dois tipos de máscaras de URL que você pode usar:

* Incluir máscaras de URL
* Excluir máscaras de URL

Inclua máscaras de URL para informar ao robô de pesquisa qualquer documentos que corresponda ao padrão da máscara.

Excluir máscaras de URL instrui o robô de pesquisa a indexar documentos correspondentes.

À medida que o robô de pesquisa viaja de um link para outro site, ele encontra URLs e procura máscaras que correspondam a esses URLs. A primeira correspondência determina se o URL deve ser incluído ou excluído do índice. Se nenhuma máscara corresponder a um URL encontrado, esse URL será descartado do índice.

Incluir máscaras de URL para URLs de ponto de entrada são geradas automaticamente. Esse comportamento garante que todos os documentos encontrados em seu site sejam indexados. Também elimina convenientemente os links que &quot;deixam&quot; seu site. Por exemplo, se uma página indexada se vincula a https://www.yahoo.com, o robô de pesquisa não indexa esse URL porque não corresponde à máscara de inclusão gerada automaticamente pelo URL do ponto de entrada.

Cada máscara de URL especificada deve estar em uma linha separada.

A máscara pode especificar qualquer um dos seguintes:

* Um caminho completo como em `https://www.mydomain.com/products.html`.
* Um caminho parcial como em `https://www.mydomain.com/products`.
* Um URL que usa curingas como em `https://www.mydomain.com/*.html`.
* Uma expressão regular (para usuários avançados).

   Para tornar uma máscara uma expressão regular, insira a palavra-chave `regexp` entre o tipo de máscara ( `exclude` ou `include`) e a máscara de URL.

Este é um exemplo simples de máscara de exclusão de URL:

```
exclude https://www.mydomain.com/photos
```

Como este exemplo é uma máscara de URL excluída, qualquer documento que corresponda ao padrão não é indexado. O padrão corresponde a qualquer item encontrado, tanto arquivos quanto pastas, de modo que `https://www.mydomain.com/photos.html` e `https://www.mydomain.com/photos/index.html`, que correspondem ao URL excluído, não sejam indexados. Para corresponder somente arquivos na pasta `/photos/`, a máscara de URL deve conter uma barra à direita, como no exemplo a seguir:

```
exclude https://www.mydomain.com/photos/
```

O exemplo de máscara de exclusão a seguir usa um curinga. Ele instrui o robô de pesquisa a ignorar arquivos com a extensão &quot;.pdf&quot;. O robô de pesquisa não adiciona esses arquivos ao índice.

```
exclude *.pdf
```

Uma máscara de URL simples de inclusão é a seguinte:

```
include https://www.mydomain.com/news/
```

Somente documentos vinculados por meio de uma série de links de um ponto de entrada de URL, ou que são usados como um ponto de entrada de URL propriamente dito, são indexados. A listagem exclusiva de um URL de documento como uma máscara de URL de inclusão não indexa um documento desvinculado. Para adicionar documentos não vinculados ao seu índice, você pode usar o recurso de Pontos de entrada de URL.

Consulte [Sobre pontos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Incluir máscaras e excluir máscaras podem trabalhar em conjunto. Você pode excluir uma grande parte do seu site da indexação ao criar uma máscara de URL excluída e ainda incluir uma ou mais páginas excluídas com uma máscara de URL de inclusão. Por exemplo, suponha que o URL do ponto de entrada seja o seguinte:

```
https://www.mydomain.com/photos/
```

O robô de pesquisa rastreia e indexa todas as páginas em `/photos/summer/`, `/photos/spring/` e `/photos/fall/` (assumindo que haja links para pelo menos uma página em cada diretório da pasta `photos`). Esse comportamento ocorre porque os caminhos de link permitem que o robô de pesquisa localize os documentos nas pastas `/summer/`, `/spring/` e `/fall/` correspondem à máscara de inclusão gerada automaticamente pelo URL do ponto de entrada.

Você pode optar por excluir todas as páginas na pasta `/fall/` com uma máscara de URL excluída, como no exemplo a seguir:

```
exclude https://www.mydomain.com/photos/fall/
```

Ou, inclua seletivamente apenas `/photos/fall/redleaves4.html` como parte do índice com a seguinte máscara de URL:

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Para que os dois exemplos de máscara acima funcionem conforme desejado, a máscara de inclusão é listada primeiro, como a seguir:

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

Como o robô de pesquisa segue as direções na ordem em que estão listados, o robô de pesquisa primeiro inclui `/photos/fall/redleaves4.html` e exclui o restante dos arquivos na pasta `/fall`.

Se as instruções forem especificadas do modo contrário, como a seguir:

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Em seguida, `/photos/fall/redleaves4.html` não está incluído, mesmo que a máscara especifique que está incluída.

Uma máscara de URL que aparece primeiro sempre tem precedência sobre uma máscara de URL que aparece posteriormente nas configurações de máscara. Além disso, se o robô de pesquisa encontrar uma página que corresponda a uma máscara de URL de inclusão e uma máscara de URL de exclusão, a máscara listada primeiro sempre terá prioridade.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Sobre o uso de palavras-chave com máscaras de URL {#section_7609A7A6D79B482ABCA8900886541AAB}

Você pode qualificar cada máscara de inclusão com uma ou mais palavras-chave separadas por espaço, que afetam como as páginas correspondentes são indexadas.

Uma vírgula não é válida como separador entre a máscara e a palavra-chave; você só pode usar espaços.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Palavra-chave </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Se você não quiser indexar o texto nas páginas que correspondem à máscara de URL, mas quiser seguir os links de páginas correspondentes, adicione 
     <code>
       noindex 
     </code> após a máscara de URL de inclusão. Certifique-se de separar a palavra-chave da máscara por um espaço, como no exemplo a seguir: </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>O exemplo acima especifica que o robô de pesquisa segue todos os links dos arquivos com a variável 
     <code>
       .swf 
     </code>, mas desativa a indexação de todo o texto contido nesses arquivos. </p> <p>A variável 
     A palavra-chave <code>
       noindex 
     </code> é equivalente a uma tag meta de robô com 
     <code>
       content="noindex" 
     </code> entre 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> tags de páginas correspondentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Se você quiser indexar o texto nas páginas que correspondem à máscara de URL, mas não quiser seguir os links da página correspondente, adicione 
     <code>
       nofollow 
     </code> após a máscara de URL de inclusão. Certifique-se de separar a palavra-chave da máscara por um espaço, como no exemplo a seguir: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>A variável 
     A palavra-chave <code>
       nofollow 
     </code> é equivalente a uma tag meta de robô com 
     <code>
       content="nofollow" 
     </code> entre 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> tags de páginas correspondentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>Usado para incluir e excluir máscaras. </p> <p>Qualquer máscara de URL precedida por 
     <code>
       regexp 
     </code> é tratado como uma expressão regular. Se o robô de pesquisa encontrar documentos que correspondam a uma máscara de URL de expressão regular excluída, esses documentos não serão indexados. Se o robô de pesquisa encontrar documentos que correspondam a uma máscara de URL de expressão regular de inclusão, esses documentos serão indexados. Por exemplo, suponha que você tenha a seguinte máscara de URL: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>O robô de pesquisa exclui arquivos correspondentes, como 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>Se você tivesse a seguinte máscara de URL de expressão regular excluída: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>O robô de pesquisa não deve incluir nenhum URL que contenha um parâmetro CGI, como 
     <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code>. </p> <p>Se você tivesse a seguinte máscara de URL de expressão regular: </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>O robô de pesquisa segue todos os links de arquivos com a extensão ".swf". A variável 
     A palavra-chave <code>
       noindex 
     </code> também especifica que o texto dos arquivos correspondentes não é indexado. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adicionar máscaras de URL para indexar ou não indexar partes do site {#task_E1AFC17C746048B8843013D979E082C1}

Você pode usar [!DNL URL Masks] para definir quais partes do site você deseja ou não deseja rastrear e indexar.

Use o campo Testar máscaras de URL para testar se um documento está ou não incluído depois de indexar.

Certifique-se de recriar o índice do site para que os resultados das máscaras de URL fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para adicionar máscaras de URL para indexar ou não partes de seu site**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**.
1. (Opcional) Na página [!DNL URL Masks], no campo **[!UICONTROL Test URL Masks]**, insira uma máscara de URL de teste em seu site e clique em **[!UICONTROL Test]**.
1. No campo [!DNL URL Masks], digite `include` (para adicionar um site que você deseja rastrear e indexar) ou digite `exclude` (para impedir que um site seja rastreado e indexado), seguido pelo endereço da máscara de URL.

   Insira um endereço de máscara de URL por linha. Exemplo:

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre máscaras de data {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

Você pode usar máscaras de data para incluir ou excluir arquivos dos resultados da pesquisa com base na idade do arquivo.

Certifique-se de recriar o índice do site para que os resultados das máscaras de URL fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

A seguir estão dois tipos de máscaras de data que você pode usar:

* Incluir máscaras de data (&quot;incluir dias&quot; e &quot;incluir data&quot;)

   Incluir os arquivos de índice de máscaras de data que estão datados na data especificada ou antes dela.
* Excluir máscaras de data (&quot;dias excluídos&quot; e &quot;data de exclusão&quot;)

   Exclua os arquivos de índice de máscaras de data que estão datados na data especificada ou antes dela.

Por padrão, a data do arquivo é determinada a partir das informações da tag meta. Se nenhuma tag Meta for encontrada, a data de um arquivo será determinada a partir do cabeçalho HTTP recebido do servidor quando o robô de pesquisa baixar um arquivo.

Cada máscara de data especificada deve estar em uma linha separada.

A máscara pode especificar qualquer um dos seguintes:

* Um caminho completo como em `https://www.mydomain.com/products.html`
* Um caminho parcial como em `https://www.mydomain.com/products`
* Um URL que usa curingas `https://www.mydomain.com/*.html`
* Uma expressão normal. Para tornar uma máscara uma expressão regular, insira a palavra-chave `regexp` antes do URL.

As máscaras de data de inclusão e exclusão podem especificar uma data de uma das duas maneiras a seguir. As máscaras só serão aplicadas se os arquivos correspondentes tiverem sido criados na data especificada ou antes dela:

1. Um número de dias. Por exemplo, suponha que sua máscara de data seja a seguinte:

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   O número de dias especificado é contado de volta. Se o arquivo tiver data igual ou anterior à data de chegada, a máscara será aplicada.

1. Uma data real usando o formato AAAA-MM-DD. Por exemplo, suponha que sua máscara de data seja a seguinte:

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   Se o documento correspondente for datado na data especificada ou antes dela, a máscara de data será aplicada.

Este é um exemplo simples de máscara de data de exclusão:

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

Como esta é uma máscara de data de exclusão, qualquer arquivo que corresponda ao padrão não é indexado e tem 90 dias ou mais. Quando você exclui um documento, nenhum texto é indexado e nenhum link é seguido desse arquivo. O arquivo é efetivamente ignorado. Neste exemplo, os arquivos e as pastas podem corresponder ao padrão de URL especificado. Observe que `https://www.mydomain.com/docs/archive.html` e `https://www.mydomain.com/docs/archive/index.html` correspondem ao padrão e não são indexados se tiverem 90 dias ou mais. Para corresponder somente os arquivos na pasta `/docs/archive/`, a máscara de data deve conter uma barra à direita, como a seguir:

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

As máscaras de data também podem ser usadas com curingas. A máscara de exclusão a seguir diz ao robô de pesquisa para ignorar arquivos com a extensão &quot;.pdf&quot; que estão datados de 2011-02-15 até 2011. O robô de pesquisa não adiciona arquivos correspondentes ao índice.

```
exclude-date 2011-02-15 *.pdf
```

Incluir máscara de data semelhante, somente os arquivos correspondentes são adicionados ao índice. O exemplo de máscara de data de inclusão a seguir instrui o robô de pesquisa a indexar o texto de quaisquer arquivos com zero dias de idade ou mais antigos na área `/docs/archive/manual/` do site.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

Incluir máscaras e excluir máscaras podem trabalhar em conjunto. Por exemplo, você pode excluir uma grande parte do seu site da indexação ao criar uma máscara de data de exclusão e ainda incluir uma ou mais páginas excluídas com uma máscara de URL de inclusão. Se o URL do ponto de entrada for o seguinte:

```
https://www.mydomain.com/archive/
```

O robô de pesquisa rastreia e indexa todas as páginas em `/archive/summer/`, `/archive/spring/` e `/archive/fall/` (assumindo que haja links para pelo menos uma página em cada pasta da pasta `archive`). Esse comportamento ocorre porque os caminhos de link permitem que o robô de pesquisa &quot;localize&quot; os arquivos nas pastas `/summer/`, `/spring/` e `/fall/` e os URLs das pastas correspondem à máscara de inclusão gerada automaticamente pelo URL do ponto de entrada.

Consulte [Sobre pontos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Consulte [Definição das definições da sua conta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Você pode optar por excluir todas as páginas com mais de 90 dias na pasta `/fall/` com uma máscara de data de exclusão, como a seguir:

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Você pode incluir seletivamente apenas `/archive/fall/index.html` (independentemente da idade - qualquer arquivo com 0 dias ou mais corresponde) como parte do índice com a seguinte máscara de data:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

Para que os dois exemplos de máscara acima funcionem conforme desejado, é necessário lista a máscara de inclusão primeiro, como a seguir:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Como o robô de pesquisa segue as direções na ordem em que são especificados, o robô de pesquisa primeiro inclui `/archive/fall/index.html` e exclui o restante dos arquivos na pasta `/fall`.

Se as instruções forem especificadas do modo contrário, como a seguir:

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

Em seguida, `/archive/fall/index.html` não é incluído, mesmo que a máscara especifique que deve ser. Uma máscara de data que aparece primeiro sempre tem precedência sobre uma máscara de data que pode aparecer posteriormente nas configurações de máscara. Além disso, se o robô de pesquisa encontrar uma página que corresponda a uma máscara de data de inclusão e uma máscara de data de exclusão, a máscara listada primeiro sempre terá prioridade.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Sobre o uso de palavras-chave com máscaras de data {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

Você pode qualificar cada máscara de inclusão com uma ou mais palavras-chave separadas por espaço, que afetam como as páginas correspondentes são indexadas.

Uma vírgula não é válida como separador entre a máscara e a palavra-chave; você só pode usar espaços.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Palavra-chave </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Se você não quiser indexar o texto nas páginas que estão datadas na data especificada pela máscara de inclusão ou antes dela, adicione 
     <code>
       noindex 
     </code> depois da máscara de data de inclusão, como a seguir: </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Certifique-se de separar a palavra-chave da máscara com um espaço. </p> <p>O exemplo acima especifica que o robô de pesquisa segue todos os links de arquivos com a extensão ".swf" com 10 dias de idade ou mais. No entanto, desativa a indexação de todo o texto contido nesses arquivos. </p> <p>Talvez você queira verificar se o texto dos arquivos mais antigos não está indexado, mas segue todos os links desses arquivos. Nesses casos, use uma máscara de data de inclusão com a palavra-chave "noindex" em vez de usar uma máscara de data de exclusão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Se você quiser indexar o texto nas páginas que estão datadas na data especificada pela máscara de inclusão ou antes dela, mas não quiser seguir os links da página correspondente, adicione 
     <code>
       nofollow 
     </code> depois da máscara de data de inclusão, como a seguir: </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Certifique-se de separar a palavra-chave da máscara com um espaço. </p> <p>A variável 
     A palavra-chave <code>
       nofollow 
     </code> é equivalente a uma tag meta de robô com 
     <code>
       content="nofollow" 
     </code> entre 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> marca de páginas correspondentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>data do servidor </p> </td> 
   <td colname="col2"> <p>Usado para incluir e excluir máscaras. </p> <p>O robô de pesquisa geralmente baixa e analisa cada arquivo antes de verificar as máscaras de data. Esse comportamento ocorre porque alguns tipos de arquivo podem especificar uma data dentro do próprio arquivo. Por exemplo, um documento HTML pode incluir tags meta que definem a data do arquivo. </p> <p>Se você vai excluir muitos arquivos com base na data deles e não quiser colocar uma carga desnecessária nos servidores, você pode usar 
     <code>
       server-date 
     </code> após o URL na máscara de data. </p> <p>Esta palavra-chave instrui o robô de pesquisa a confiar na data do arquivo que é retornado pelo servidor em vez de analisar cada arquivo. Por exemplo, a máscara de data de exclusão a seguir ignora as páginas que correspondem ao URL se os documentos tiverem 90 dias ou mais, de acordo com a data retornada pelo servidor nos cabeçalhos HTTP: </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> Se a data retornada pelo servidor tiver 90 dias ou mais, 
     <code>
       server-date 
     </code> especifica que os documentos excluídos não serão baixados do servidor. O resultado significa um tempo de indexação mais rápido para seus documentos e uma carga reduzida colocada em seus servidores. If 
     <code>
       server-date 
     </code> não está especificado, o robô de pesquisa ignora a data retornada pelo servidor nos cabeçalhos HTTP. Em vez disso, cada arquivo é baixado e verificado para ver se a data é especificada. Se nenhuma data for especificada no arquivo, o robô de pesquisa usará a data retornada pelo servidor. </p> <p>Não deve usar 
     <code>
       server-date 
     </code> se seus arquivos contiverem comandos que substituem a data do servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> Use para incluir e excluir máscaras. </p> <p>Qualquer máscara de data precedida por 
     <code>
       regexp 
     </code> é tratado como uma expressão regular. </p> <p>Se o robô de pesquisa encontrar arquivos que correspondem a uma máscara de data de expressão regular excluída, ele não indexará esses arquivos. </p> <p>Se o robô de pesquisa encontrar arquivos que correspondem a uma máscara de data de expressão regular de inclusão, ele indexará esses documentos. </p> <p>Por exemplo, suponha que você tenha a seguinte máscara de data: </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>A máscara diz ao robô de pesquisa para excluir arquivos correspondentes com 180 dias ou mais. Ou seja, arquivos que contêm a palavra "arquivar" em seu URL. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adicionar máscaras de data para indexar ou não indexar partes do site {#task_0010543C55F648D2B5DEFEFAD60FAF04}

Você pode usar máscaras de data para incluir ou excluir arquivos dos resultados de pesquisa do cliente com base na idade dos arquivos.

Use os campos **[!UICONTROL Test Date]** e **[!UICONTROL Test URL]** para testar se um arquivo está ou não incluído depois de indexar.

Certifique-se de recriar o índice do site para que os resultados das máscaras de URL fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para adicionar máscaras de data para indexar ou não partes do site**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**.
1. (Opcional) Na página [!DNL Date Masks], no campo **[!UICONTROL Test Date]**, digite uma data formatada como AAAA-MM-DD (por exemplo, `2011-07-25`); no campo **[!UICONTROL Test URL]**, insira uma máscara de URL do seu site e clique em **[!UICONTROL Test]**.
1. No campo [!DNL Date Masks], insira um endereço de máscara de data por linha.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre senhas {#concept_3EDBD731725D46B891F834D4472774DC}

Para acessar partes do seu site protegidas com a Autenticação básica HTTP, você pode adicionar uma ou mais senhas.

Antes que os efeitos das configurações de Senha fiquem visíveis para os clientes, é necessário recriar o índice do site.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Na página [!DNL Passwords], digite cada senha em uma única linha. A senha consiste em um URL ou realm, um nome de usuário e uma senha, como no exemplo a seguir:

```
https://www.mydomain.com/ myname mypassword
```

Em vez de usar um caminho de URL, como acima, você também pode especificar um realm.

Para determinar o realm correto a ser usado, abra uma página da Web protegida por senha com um navegador e observe a caixa de diálogo &quot;Digitar senha de rede&quot;.

![](assets/realms.gif)

O nome do território, neste caso, é &quot;My Site Realm&quot;.

Usando o nome do realm acima, sua senha pode ser semelhante ao seguinte:

```
My Site Realm myusername mypassword
```

Se o site tiver vários domínios, você poderá criar várias senhas inserindo um nome de usuário e senha para cada domínio em uma linha separada, como no exemplo a seguir:

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

Você pode combinar senhas que contêm URLs ou realms para que sua lista de senha tenha a seguinte aparência:

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

Na lista acima, a primeira senha é usada que contém um realm ou URL que corresponde à solicitação de autenticação do servidor. Mesmo se o arquivo em `https://www.mysite.com/path1/path2/index.html` estiver em `Realm3`, por exemplo, `name2` e `password2` serão usados porque a senha definida com o URL está listada acima daquela definida com o realm.

## Adicionar senhas para acessar áreas do site que exigem autenticação {#task_DED19D476FF04B48BB6456D5ECB8628A}

Você pode usar Senhas para acessar áreas protegidas por senha do seu site para fins de rastreamento e indexação.

Antes que os efeitos de sua senha sejam adições visíveis aos clientes, recrie o índice do site

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para adicionar senhas para acessar áreas de seu site que exigem autenticação**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**.
1. Na página [!DNL Passwords], no campo **[!UICONTROL Passwords]**, insira um realm ou URL e o nome de usuário e senha associados, separados por um espaço.

   Exemplo de uma senha de realm e uma senha de URL em linhas separadas:

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   Adicione apenas uma senha por linha.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre os tipos de conteúdo {#concept_6FEA1355C0374500B4C53090C34A8A07}

Você pode usar [!DNL Content Types] para selecionar os tipos de arquivos que deseja rastrear e indexar para esta conta.

Os tipos de conteúdo que você pode escolher rastrear e indexar incluem documentos PDF, documentos de texto, filmes de Flash Adobe, arquivos de aplicativos do Microsoft Office como Word, Excel e Powerpoint e texto em arquivos MP3. O texto encontrado nos tipos de conteúdo selecionados é pesquisado junto com todo o outro texto do site.

Antes que os efeitos das configurações de Tipos de conteúdo fiquem visíveis para os clientes, é necessário recriar o índice do site.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Sobre a indexação de arquivos de música MP3 {#section_AD2E28BEEE3E46629E2B05C34A963673}

Se você selecionar a opção **[!UICONTROL Text in MP3 Music Files]** na página [!DNL Content Types], um arquivo MP3 será rastreado e indexado de uma das duas maneiras. A primeira e mais comum é a partir de uma tag href de âncora em um arquivo HTML, como a seguir:

```
<a href="MP3-file-URL"></a>
```

A segunda maneira é digitar o URL do arquivo MP3 como um ponto de entrada de URL.

Consulte [Sobre pontos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Um arquivo MP3 é reconhecido pelo tipo MIME &quot;audio/mpeg&quot;.

Esteja ciente de que os tamanhos de arquivos de música MP3 podem ser bastante grandes, mesmo que geralmente contenham apenas uma pequena quantidade de texto. Por exemplo, arquivos MP3 podem armazenar opcionalmente itens como nome do álbum, nome do artista, título da música, gênero da música, ano de lançamento e um comentário. Estas informações são armazenadas no final do ficheiro no que é chamado TAG. Os arquivos MP3 que contêm informações TAG são indexados da seguinte maneira:

* O título da música é tratado como o título de uma página HTML.
* O comentário é tratado como uma descrição definida para uma página HTML.
* O gênero é tratado como uma palavra-chave definida para uma página HTML.
* O nome do artista, o nome do álbum e o ano de lançamento são tratados como o corpo de uma página HTML.

Observe que cada arquivo MP3 rastreado e indexado em seu site conta como uma página.

Se seu site contém muitos arquivos MP3 grandes, você pode exceder o limite de bytes de indexação para sua conta. Se isso acontecer, você poderá desmarcar **[!UICONTROL Text in MP3 Music Files]** na página [!DNL Content Types] para impedir a indexação de todos os arquivos MP3 em seu site.

Se você quiser apenas impedir a indexação de determinados arquivos MP3 em seu site, execute um dos procedimentos a seguir:

* Coloque as tags de âncora que se vinculam aos arquivos MP3 com as tags `<nofollow>` e `</nofollow>`. O robô de pesquisa não segue os links entre essas tags.

* Adicione os URLs dos arquivos MP3 como máscaras de exclusão.

   Consulte [Sobre máscaras de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

## Selecionar tipos de conteúdo para rastrear e indexar {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

Você pode usar [!DNL Content Types] para selecionar os tipos de arquivos que deseja rastrear e indexar para esta conta.

Os tipos de conteúdo que você pode escolher rastrear e indexar incluem documentos PDF, documentos de texto, filmes de Flash Adobe, arquivos de aplicativos do Microsoft Office como Word, Excel e Powerpoint e texto em arquivos MP3. O texto encontrado nos tipos de conteúdo selecionados é pesquisado junto com todo o outro texto do site.

Antes que os efeitos das configurações de Tipos de conteúdo fiquem visíveis para os clientes, é necessário recriar o índice do site.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Para rastrear e indexar arquivos MP3 chineses, japoneses ou coreanos, conclua as etapas abaixo. Em seguida, em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, especifique o conjunto de caracteres usado para codificar os arquivos MP3.

Consulte [Acerca das injeções](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

**Para selecionar tipos de conteúdo para rastrear e indexar**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.
1. Na página [!DNL Content Types], verifique os tipos de arquivos que você deseja rastrear e indexar em seu site.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre conexões {#concept_E2F3B7E7521147479E5948A94BB3A40B}

Você pode usar o Connections para adicionar até dez conexões HTTP que o robô de pesquisa usa para indexar seu site.

Aumentar o número de conexões pode reduzir significativamente a quantidade de tempo que leva para concluir um rastreamento e um índice. No entanto, esteja ciente de que cada conexão adicional aumenta a carga no servidor.

## Adicionar conexões para aumentar a velocidade de indexação {#task_3E9B83E43C1842A19066355A15C4A6FB}

Você pode reduzir o tempo necessário para indexar seu site usando o Connections para aumentar o número de conexões HTTP simultâneas que o rastreador usa. Você pode adicionar até dez conexões.

Esteja ciente de que cada conexão adicional aumenta a carga colocada no servidor.

**Para adicionar conexões para aumentar a velocidade de indexação**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**.
1. Na página [!DNL Parallel Indexing Connections], no campo **[!UICONTROL Number of Connections]**, digite o número de conexões (1-10) que deseja adicionar.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre o envio de formulário {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

Você pode usar o envio de formulário para ajudá-lo a reconhecer e processar formulários em seu site.

Durante o rastreamento e a indexação do site, cada formulário encontrado é comparado às definições de formulário adicionadas. Se um formulário corresponder a uma definição de formulário, ele será enviado para indexação. Se um formulário corresponder a mais de uma definição, ele será enviado uma vez para cada definição correspondente.

## Adicionar definições de formulário para indexar formulários em seu site {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

Você pode usar [!DNL Form Submission] para ajudar a processar formulários reconhecidos em seu site para fins de indexação.

Certifique-se de recriar o índice do site para que os resultados das alterações fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para adicionar definições de formulário para indexar formulários em seu site**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Na página [!DNL Form Submission], clique em **[!UICONTROL Add New Form]**.
1. Na página [!DNL Add Form Definition], defina as opções [!DNL Form Recognition] e [!DNL Form Submission].

   As cinco opções na seção [!DNL Form Recognition] na página [!DNL Form Definition] são usadas para identificar formulários nas páginas da Web que podem ser processados.

   As três opções na seção [!DNL Form Submission] são usadas para especificar os parâmetros e valores enviados com um formulário para o servidor da Web.

   Insira um parâmetro de reconhecimento ou submissão por linha. Cada parâmetro deve incluir um nome e um valor.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <b>Reconhecimento de formulário</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de URL da página </p> </td> 
      <td colname="col2"> <p>Identifique a página da Web ou as páginas que contêm o formulário. Para identificar um formulário que aparece em uma única página, insira o URL dessa página como no exemplo a seguir: </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>Para identificar formulários que aparecem em várias páginas, especifique uma máscara de URL que use curingas para descrever as páginas. Para identificar formulários encontrados em qualquer página do ASP em <code> https://www.mydomain.com/register/ </code>, por exemplo, especifique o seguinte: </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>Também é possível usar uma expressão regular para identificar várias páginas. Especifique apenas 
      Palavra-chave <code>
        regexp 
      </code> antes da máscara de URL, como no exemplo a seguir: </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de URL de ação </p> </td> 
      <td colname="col2"> <p>Identifica o atributo action da variável 
      tag <code>
        &lt;form&gt; 
      </code>. </p> <p>Como a máscara de URL da página, a máscara de URL de ação pode assumir a forma de um único URL, um URL com curingas ou uma expressão regular. </p> <p>A máscara de URL pode ser qualquer uma das seguintes: 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> Um caminho completo, como no seguinte: <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> Um caminho parcial, como no seguinte: <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> Um URL que usa curingas como no seguinte: <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> Uma expressão regular como a seguinte: <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>Se você não quiser indexar o texto nas páginas identificadas por uma máscara de URL ou por uma máscara de URL de ação, ou se não quiser que os links sejam seguidos nessas páginas, use a variável 
      <code>
        noindex 
      </code> e 
      <code>
        nofollow 
      </code> palavras-chave. É possível adicionar essas palavras-chave às suas máscaras usando máscaras de URL ou pontos de entrada. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> Sobre pontos de entrada de URL </a>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> Sobre máscaras de URL </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de nome do formulário </p> </td> 
      <td colname="col2"> <p>Identifica formulários se a variável 
      As tags <code>
        &lt;form&gt; 
      </code> em suas páginas da Web contêm um atributo de nome. </p> <p>Você pode usar um nome simples ( 
      <code>
        login_form 
      </code>), um nome com um caractere curinga ( 
      <code>
        form* 
      </code>) ou uma expressão regular ( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>Geralmente, esse campo pode ser deixado em branco, pois os formulários normalmente não têm um atributo name. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de ID de formulário </p> </td> 
      <td colname="col2"> <p>Identifica formulários se a variável 
      As tags <code>
        &lt;form&gt; 
      </code> em suas páginas da Web contêm um atributo id. </p> <p>Você pode usar um nome simples ( 
      <code>
        login_form 
      </code>), um nome com um caractere curinga ( 
      <code>
        form* 
      </code>) ou uma expressão regular ( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>Geralmente, esse campo pode ser deixado em branco, pois os formulários normalmente não têm um atributo name. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetros </p> </td> 
      <td colname="col2"> <p>Identifique formulários que contêm ou não contêm um parâmetro nomeado ou um parâmetro nomeado com um valor específico. </p> <p>Por exemplo, para identificar um formulário que contém um parâmetro de email predefinido para rick_brough@mydomain.com, um parâmetro de senha, mas não um parâmetro de nome, você deve especificar as seguintes configurações de parâmetro, uma por linha: </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Envio de formulário</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Substituir URL de ação </p> </td> 
      <td colname="col2"> <p>Especifique quando o público alvo do envio do formulário é diferente do especificado no atributo action do formulário. </p> <p>Por exemplo, você pode usar essa opção quando o formulário for enviado por meio de uma função JavaScript que constrói um valor de URL diferente do encontrado no formulário. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Método de substituição </p> </td> 
      <td colname="col2"> <p>Especifique quando o público alvo do envio do formulário é diferente do que é usado no atributo action do formulário e quando o JavaScript enviado alterou o método. </p> <p>Os valores padrão para todos os parâmetros de formulário ( 
      tags <code>
        &lt;input&gt; 
      </code>, incluindo campos ocultos), o padrão 
      <code>
        &lt;option&gt; 
      </code> de uma 
      <code>
        &lt;select&gt; 
      </code> e o texto padrão entre 
      <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code> tags) são lidas da página da Web. No entanto, qualquer parâmetro listado na seção <span class="wintitle"> Submissão de formulário </span>, no campo <span class="uicontrol"> Parâmetros </span>, é substituído pelos padrões de formulário. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetros </p> </td> 
      <td colname="col2"> <p>É possível prefixar parâmetros de envio de formulário com a variável 
      Palavra-chave <code>
        not 
      </code>. </p> <p>Ao prefixar um parâmetro com 
      <code>
        not 
      </code>, ele não é enviado como parte do envio do formulário. Esse comportamento é útil para caixas de seleção que devem ser enviadas desmarcadas. </p> <p>Por exemplo, suponha que você deseja enviar os seguintes parâmetros: </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> O parâmetro de email com o valor 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> O parâmetro password com o valor 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> O parâmetro mycheckbox como desmarcado. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>Todos os outros 
      <code>
        &lt;form&gt; 
      </code> parâmetros como seus valores padrão </p> </li> 
      </ul> </p> <p>Seu parâmetro de envio de formulário seria semelhante ao seguinte: </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>O atributo de método do 
      A tag <code>
        &lt;form&gt; 
      </code> na página da Web é usada para decidir se os dados são enviados para o servidor usando o método GET ou o método POST. </p> <p>Se a variável 
      A tag <code>
        &lt;form&gt; 
      </code> não contém um atributo de método, o formulário é enviado usando o método de GET. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma definição de formulário {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

É possível editar uma definição de formulário existente se um formulário do seu site tiver sido alterado ou se for necessário alterar a definição.

Esteja ciente de que não há nenhum recurso [!DNL History] na página [!DNL Form Submission] para reverter quaisquer alterações feitas em uma definição de formulário.

Certifique-se de recriar o índice do site para que os resultados das alterações fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para editar uma definição de formulário**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Na página [!DNL Form Submission], clique em **[!UICONTROL Edit]** à direita de uma definição de formulário que você deseja atualizar.
1. Na página [!DNL Edit Form Definition], defina as opções [!DNL Form Recognition] e [!DNL Form Submission].

   Consulte a tabela de opções em [Adicionar definições de formulário para indexar formulários no seu site](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma definição de formulário {#task_C350FC0CDE344F2786215D544C048B5E}

É possível excluir uma definição de formulário existente se o formulário não existir mais em seu site ou se você não quiser mais processar e indexar um formulário específico.

Esteja ciente de que não há nenhum recurso [!DNL History] na página [!DNL Form Submission] para reverter quaisquer alterações feitas em uma definição de formulário.

Certifique-se de recriar o índice do site para que os resultados das alterações fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para excluir uma definição de formulário**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Na página [!DNL Form Submission], clique em **[!UICONTROL Delete]** à direita de uma definição de formulário que você deseja remover.

   Certifique-se de escolher a definição de formulário correta a ser excluída. Não há caixa de diálogo de confirmação de exclusão ao clicar em **[!UICONTROL Delete]** na próxima etapa.
1. Na página [!DNL Delete Form Definition], clique em **[!UICONTROL Delete]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre o Conector de índice {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

Use [!DNL Index Connector] para definir fontes de entrada adicionais para indexar páginas XML ou qualquer tipo de feed.

Você pode usar uma fonte de entrada de feed de dados para acessar o conteúdo armazenado em um formulário que é diferente do que normalmente é descoberto em um site usando um dos métodos de rastreamento disponíveis. Cada documento rastreado e indexado corresponde diretamente a uma página de conteúdo do site. No entanto, um feed de dados provém de um documento XML ou de um arquivo de texto delimitado por vírgula ou por tabulação e contém as informações de conteúdo a serem indexadas.

Uma fonte de dados XML consiste em estrofes XML, ou registros, que contêm informações que correspondem a documentos individuais. Esses documentos individuais são adicionados ao índice. Um feed de dados de texto contém registros separados delimitados por nova linha que correspondem a documentos individuais. Esses documentos individuais também são adicionados ao índice. Em ambos os casos, uma configuração de conector de índice descreve como interpretar o feed. Cada configuração descreve onde o arquivo reside e como os servidores o acessam. A configuração também descreve as informações de &quot;mapeamento&quot;. Ou seja, como os itens de cada registro são usados para preencher os campos de metadados no índice resultante.

Depois de adicionar uma definição de Conector de índice à página [!DNL Staged Index Connector Definitions], você pode alterar qualquer configuração, *exceto* para os valores Nome ou Tipo.

A página [!DNL Index Connector] mostra as seguintes informações:

* O nome dos conectores de índice definidos que você configurou e adicionou.
* Um dos seguintes tipos de fonte de dados para cada conector adicionado:

   * **Texto**  - Arquivos simples &quot;simples&quot;, delimitados por vírgulas, delimitados por tabulação ou outros formatos delimitados consistentemente.
   * **Feed**  - feeds XML.
   * **XML**  - Coleções de documentos XML.

* Se o conector está ativado ou não para a próxima pesquisa e indexação concluída.
* O endereço da fonte de dados.

Consulte também [Sobre o Conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## Como o processo de indexação funciona para configurações de Texto e Feed no Index Connector {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Etapa  </p> </th> 
   <th colname="col2" class="entry"> <p>Processo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Baixe a fonte de dados. </p> </td> 
   <td colname="col3"> <p>Para configurações de Texto e Feed, é um download de arquivo simples. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Analise a fonte de dados baixada em pseudo-documentos individuais. </p> </td> 
   <td colname="col3"> <p>Para <span class="uicontrol"> Texto </span>, cada linha de texto delimitada por nova linha corresponde a um documento individual e é analisada usando o delimitador especificado, como uma vírgula ou tabulação. </p> <p>Para <span class="uicontrol"> Feed </span>, os dados de cada documento são extraídos usando um padrão de expressão regular no seguinte formulário: </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Usando <span class="uicontrol"> Mapa </span> na página <span class="wintitle"> Adição de Conector de Índice </span>, crie uma cópia em cache dos dados e crie uma lista de links para o crawler. Os dados são armazenados em um cache local e são preenchidos com os campos configurados. </p> <p>Os dados analisados são gravados no cache local. </p> <p>Esse cache é lido posteriormente para criar os documentos HTML simples de que o crawler precisa. Por exemplo, </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>O elemento <span class="codeph"> &lt;title&gt; </span> só é gerado quando existe um mapeamento para o campo de metadados Title. Da mesma forma, o elemento <span class="codeph"> &lt;body&gt; </span> só é gerado quando existe um mapeamento para o campo de metadados do Corpo. </p> <p> <b>Importante</b>: Não há suporte para a atribuição de valores à tag meta de URL predefinida. </p> <p>Para todos os outros mapeamentos, as tags <span class="codeph"> &lt;meta&gt; </span> são geradas para cada campo que tem dados encontrados no documento original. </p> <p>Os campos de cada documento são adicionados ao cache. Para cada documento gravado no cache, um link também é gerado como nos seguintes exemplos: </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>O mapeamento da configuração deve ter um campo identificado como Chave primária. Esse mapeamento forma a chave usada quando os dados são obtidos do cache. </p> <p>O rastreador reconhece o índice URL <span class="codeph">: </span> prefixo do esquema, que pode então acessar os dados armazenados localmente em cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Rastrear o conjunto de documentos em cache. </p> </td> 
   <td colname="col3"> <p>O índice <span class="codeph">: </span> os links são adicionados à lista pendente do rastreador e são processados na sequência de rastreamento normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Processar cada documento. </p> </td> 
   <td colname="col3"> <p>O valor principal de cada link corresponde a uma entrada no cache, portanto, rastrear cada link resulta na busca dos dados do documento do cache. Em seguida, é "montado" em uma imagem HTML que é processada e adicionada ao índice. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Como o processo de indexação funciona para configurações XML no Conector de índice {#section_7F1551EA51854C5C99F284CE260526EB}

O processo de indexação para a configuração XML é semelhante ao processo para configurações de Texto e Feed com as seguintes pequenas alterações e exceções.

Como os documentos para rastreamentos XML já estão separados em arquivos individuais, as etapas 1 e 2 na tabela acima não se aplicam diretamente. Se você especificar um URL nos campos **[!UICONTROL Host Address]** e **[!UICONTROL File Path]** da página [!DNL Index Connector Add], ele será baixado e processado como um documento HTML normal. A expectativa é que o documento de download contenha uma coleção de links `<a href="{url}"...`, cada um dos quais aponta para um documento XML processado. Esses links são convertidos no seguinte formulário:

```
<a href="index:<ic_config_name>?url="{url}">
```

Por exemplo, se a configuração do Adobe retornasse os seguintes links:

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

Na tabela acima, a etapa 3 não se aplica e a etapa 4 é concluída no momento da pesquisa e indexação.

Como alternativa, você pode combinar seus documentos XML com outros documentos que foram descobertos naturalmente pelo processo de rastreamento. Nesses casos, você pode usar regras de regravação ( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**) para alterar os URLs dos documentos XML e direcioná-los para o Conector de índice.

Consulte [Sobre as Regras de URL de Recuperação de Listas de Rastreamento](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Por exemplo, suponha que você tenha a seguinte regra de regravação:

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

Essa regra converte qualquer URL que termine com `.xml` em um link do Conector de índice. O rastreador reconhece e regrava o esquema de URL `index:`. O processo de download é redirecionado pelo servidor Apache do Conector de índice no primário. Cada documento baixado é examinado usando o mesmo padrão de expressão comum usado nos Feeds. Nesse caso, no entanto, o documento HTML fabricado não é salvo no cache. Em vez disso, é entregue diretamente ao crawler para processamento de índice.

## Como configurar vários Conectores de índice {#section_C2B14C0F06354A57AEF6238FF3814E5D}

É possível definir várias configurações do Conector de índice para qualquer conta. As configurações são automaticamente adicionadas à lista suspensa em **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]**, conforme mostrado na ilustração a seguir:

![](assets/url_entrypoints_index_connector.png)

Selecionar uma configuração na lista suspensa adiciona o valor ao final da lista de pontos de entrada de URL.

>[!NOTE]
>
>Embora as configurações do Conector de índice desativado sejam adicionadas à lista suspensa, não é possível selecioná-las. Se você selecionar a mesma configuração do Conector de índice pela segunda vez, ela será adicionada ao final da lista e a instância anterior será excluída.

Para especificar um ponto de entrada Conector de índice para um rastreamento incremental, é possível adicionar entradas usando o seguinte formato:

```
index:<indexconnector_configuration_name>
```

O rastreador processa cada entrada adicionada se ela for encontrada na página Conectores de índice e estiver ativada.

Observação: Como cada URL de documento é construído usando o nome de configuração do Conector de índice e a chave primária do documento, certifique-se de usar o mesmo nome de configuração do Conector de índice ao executar atualizações incrementais! Isso permite que [!DNL Adobe Search&Promote] atualize corretamente documentos indexados anteriormente.

Consulte também [Sobre pontos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

**O uso dos mapas de configuração ao adicionar um conector de índice**

No momento em que você adiciona um Conector de índice, é possível usar opcionalmente o recurso **[!UICONTROL Setup Maps]** para baixar uma amostra de sua fonte de dados. Os dados são examinados para determinar a adequação da indexação.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Se você escolher o tipo Conector de índice... </p> </th> 
   <th colname="col2" class="entry"> <p>O recurso Configurar Mapas... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texto </p> </td> 
   <td colname="col2"> <p>Determina o valor do delimitador tentando tabulações primeiro e, em seguida, barras verticais ( <span class="codeph"> | </span>) e finalmente vírgulas ( <span class="codeph">, </span>). Se você já tiver especificado um valor delimitador antes de clicar em <span class="uicontrol"> Configurar Mapas </span>, esse valor será usado. </p> <p>O esquema de melhor ajuste resulta no preenchimento dos campos de Mapa com suposições nos valores apropriados de Tag e Campo. Além disso, uma amostra dos dados analisados é exibida. Certifique-se de selecionar <span class="uicontrol"> Cabeçalhos na Primeira Linha </span> se você sabe que o arquivo inclui uma linha de cabeçalho. A função de configuração usa essas informações para identificar melhor as entradas de mapa resultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feed </p> </td> 
   <td colname="col2"> <p>Faz o download da fonte de dados e executa uma análise XML simples. </p> <p>Os identificadores XPath resultantes são exibidos nas linhas de tag da tabela Mapa e valores similares em Campos. Essas linhas identificam apenas os dados disponíveis e não geram as definições XPath mais complicadas. No entanto, ainda é útil, pois descreve os dados XML e identifica os valores de Item. </p> <p> <p>Observação:  A função Setup Maps baixa a fonte XML inteira para executar sua análise. Se o arquivo for grande, essa operação poderá expirar. </p> </p> <p>Quando bem-sucedida, essa função identifica todos os itens XPath possíveis, muitos dos quais não são desejáveis para uso. Certifique-se de examinar as definições de mapa resultantes e remover as que você não precisa ou deseja. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>Faz o download do URL de um documento individual representativo, não da lista do link principal. Esse único documento é analisado usando o mesmo mecanismo usado com Feeds, e os resultados são exibidos. </p> <p>Antes de clicar em <span class="uicontrol"> Adicionar </span> para salvar a configuração, certifique-se de alterar o URL de volta para o documento de lista do link primário. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Importante**: O recurso Configurar Mapas pode não funcionar para grandes conjuntos de dados XML, pois seu analisador de arquivos tenta ler o arquivo inteiro na memória. Como resultado, você pode experimentar uma condição de falta de memória. No entanto, quando o mesmo documento é processado no momento da indexação, ele não é lido na memória. Em vez disso, documentos grandes são processados &quot;em trânsito&quot; e não são lidos inteiramente na memória primeiro.

**O uso da Pré-visualização ao adicionar um Conector de índice**

No momento em que você adiciona um Conector de índice, é possível usar opcionalmente o recurso **[!UICONTROL Preview]** para validar os dados, como se você os salvasse. Ele executa um teste em relação à configuração, mas sem salvar a configuração na conta. O teste acessa a fonte de dados configurada. No entanto, ele grava o cache de download em um local temporário; ele não entra em conflito com a pasta de cache principal que o crawler de indexação usa.

A pré-visualização processa apenas um padrão de cinco documentos, conforme controlado por Acct:IndexConnector-Pré-visualização-Max-Documentos. Os documentos visualizados são exibidos no formulário de origem, à medida que são apresentados ao rastreador de indexação. A exibição é semelhante a um recurso &quot;Fonte de Visualização&quot; em um navegador da Web. É possível navegar pelos documentos no conjunto de pré-visualizações usando links de navegação padrão.

A pré-visualização não suporta configurações XML porque esses documentos são processados diretamente e não são baixados para o cache.

## Adicionando uma definição de Conector de índice {#task_96779B651A654E1F871F55D6DBBC8886}

Cada configuração do Conector de índice define uma fonte de dados e mapeamentos para relacionar os itens de dados definidos para essa fonte aos campos de metadados no índice.

Antes que os efeitos da definição nova e ativada fiquem visíveis para os clientes, recrie o índice do site.

**Para adicionar uma definição de Conector de índice**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Na página [!DNL Stage Index Connector Definitions], clique em **[!UICONTROL Add New Index Connector]**.
1. Na página [!DNL Index Connector Add], defina as opções de conector desejadas. As opções disponíveis dependem do **[!UICONTROL Type]** selecionado.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome </p> </td> 
      <td colname="col2"> <p>O nome exclusivo da configuração do Conector de índice. É possível usar caracteres alfanuméricos. Os caracteres "_" e "-" também são permitidos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo </p> </td> 
      <td colname="col2"> <p>A fonte de seus dados. O tipo de fonte de dados selecionado afeta as opções resultantes disponíveis na página <span class="wintitle"> Adicionar </span> Conector de índice. Você pode escolher entre as seguintes opções: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texto </span> <p>Arquivos de texto simples, delimitados por vírgulas, delimitados por tabulação ou outros formatos consistentemente delimitados. Cada linha de texto delimitada por nova linha corresponde a um documento individual e é analisada usando o delimitador especificado. </p> <p>É possível mapear cada valor, ou coluna, para um campo de metadados, referenciado pelo número da coluna, começando em 1 (um). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>Faz o download de um documento XML primário que contém várias "linhas" de informações. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>Faz o download de um documento XML primário que contém links ( 
      <code>
        &lt;a&gt; 
      </code>) para documentos XML individuais. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fonte de dados: Texto</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativado </p> </td> 
      <td colname="col2"> <p>Ativa a configuração "on" para rastrear e indexar. Ou, você pode desativar a configuração para evitar o rastreamento e a indexação. </p> <p> <b>Observação</b>: As configurações do Conector de índice desativado serão ignoradas se forem encontradas em uma lista de ponto de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Endereço do host </p> </td> 
      <td colname="col2"> <p>Especifica o endereço do host do servidor no qual os dados estão localizados. </p> <p>Se desejar, você pode especificar um caminho URI completo (Uniform Resource Identifier) para o documento da fonte de dados, como nos seguintes exemplos: </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>ou </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>O URI é dividido nas entradas apropriadas para os campos Endereço do host, Caminho do arquivo, Protocolo e, opcionalmente, Nome do usuário e Senha. </p> <p>Especifica o endereço IP ou URL do sistema host em que o arquivo de fonte de dados é encontrado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o arquivo de texto simples, delimitado por vírgulas, delimitado por tabulação ou outro arquivo de formato delimitado consistentemente. </p> <p>O caminho é relativo à raiz do endereço do host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo incremental </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o arquivo de texto simples, delimitado por vírgulas, delimitado por tabulação ou outro arquivo de formato delimitado consistentemente. </p> <p>O caminho é relativo à raiz do endereço do host. </p> <p>Este arquivo, se especificado, é baixado e processado durante operações de Índice Incremental. Se nenhum arquivo for especificado, o arquivo listado em Caminho do arquivo será usado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo vertical </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o arquivo de texto simples, delimitado por vírgulas, delimitado por tabulação ou outro arquivo de formato delimitado consistentemente a ser usado durante uma Atualização Vertical. </p> <p>O caminho é relativo à raiz do endereço do host. </p> <p>Este arquivo, se especificado, é baixado e processado durante as operações de Atualização vertical. </p> <p> <b>Observação</b>: Este recurso não está ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Exclui o caminho do arquivo </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o arquivo de texto simples, contendo um único valor de identificador de documento por linha. </p> <p>O caminho é relativo à raiz do endereço do host. </p> <p>Este arquivo, se especificado, é baixado e processado durante operações de Índice Incremental. Os valores encontrados neste arquivo são usados para construir solicitações "delete" para remover documentos indexados anteriormente. Os valores neste arquivo devem corresponder aos valores encontrados nos arquivos Caminho de arquivo completo ou incremental, na coluna identificada como <span class="uicontrol"> Chave primária </span>. </p> <p> <b>Observação</b>: Este recurso não está ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica o protocolo usado para acessar o arquivo. Você pode escolher entre as seguintes opções: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Se necessário, você pode inserir as credenciais de autenticação adequadas para acessar o servidor HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Se necessário, você pode inserir as credenciais de autenticação adequadas para acessar o servidor HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Você deve inserir as credenciais de autenticação adequadas para acessar o servidor FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Você deve inserir as credenciais de autenticação adequadas para acessar o servidor SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Arquivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tempo limite </p> </td> 
      <td colname="col2"> <p>Especifica o tempo limite, em segundos, para conexões FTP, SFTP, HTTP ou HTTPS. Esse valor deve estar entre 30 e 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tentativas </p> </td> 
      <td colname="col2"> <p>Especifica o número máximo de tentativas para conexões FTP, SFTP, HTTP ou HTTPS com falha. Esse valor deve estar entre 0 e 10. </p> <p>Um valor zero (0) impedirá tentativas de repetição. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codificação </p> </td> 
      <td colname="col2"> <p>Especifica o sistema de codificação de caracteres usado no arquivo de fonte de dados especificado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Delimitador </p> </td> 
      <td colname="col2"> <p>Especifica o caractere que você deseja usar para delinear cada campo no arquivo de fonte de dados especificado. </p> <p>O caractere vírgula ( <span class="codeph"> , </span>) é um exemplo de um delimitador. A vírgula atua como um delimitador de campo que ajuda a separar campos de dados no arquivo de fonte de dados especificado. </p> <p>Selecione <span class="uicontrol"> Guia? </span> para usar o caractere de tabulação horizontal como delimitador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Cabeçalhos na primeira linha </p> </td> 
      <td colname="col2"> <p>Indica que a primeira linha do arquivo de fonte de dados contém apenas informações de cabeçalho, não dados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número mínimo de documentos para indexação </p> </td> 
      <td colname="col2"> <p>Se definido como um valor positivo, isso especifica o número mínimo de registros esperado no arquivo baixado. Se forem recebidos menos registros, a operação de índice será abortada. </p> <p> <b>Observação</b>: Este recurso não está ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> <p> <b>Observação</b>: Este recurso é usado somente durante operações de Índice completo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Especifica mapeamentos de coluna para metadados, usando números de coluna. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Coluna </span> <p> Especifica um número de coluna, com a primeira coluna sendo 1 (uma). Para adicionar novas linhas de mapa para cada coluna, em <span class="wintitle"> Ação </span>, clique em <span class="uicontrol"> + </span>. </p> <p>Não é necessário referenciar cada coluna na fonte de dados. Em vez disso, você pode optar por ignorar valores. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Campo </span> <p>Define o valor do atributo name usado para cada tag &lt;meta&gt; gerada. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metadados? </span> <p>Faz com que <span class="uicontrol"> o campo </span> se torne uma lista suspensa da qual você pode selecionar campos de metadados definidos para a conta atual. </p> <p>O valor <span class="uicontrol"> Field </span> pode ser um campo de metadados indefinido, se desejado. Um campo de metadados indefinido às vezes é útil para criar conteúdo usado pelo <span class="wintitle"> Script de filtragem </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Sobre o script de filtragem </a>. </p> <p>Quando o Conector de índice processa documentos XML com várias ocorrências em qualquer campo de mapa, os vários valores são concatenados em um único valor no documento em cache resultante. Por padrão, esses valores são combinados usando um delimitador de vírgula. No entanto, suponha que o valor <span class="wintitle"> Field </span> correspondente seja um campo de metadados definido. Além disso, esse campo tem o conjunto de atributos <span class="wintitle"> Lista de permissões </span>. Nesse caso, o valor Delimitadores de Lista do campo, que é o primeiro delimitador definido, é usado na concatenação. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Chave primária?  </span> <p>Somente uma definição de mapa é identificada como a chave primária. Esse campo se torna a referência exclusiva que é apresentada quando esse documento é adicionado ao índice. Esse valor é usado no URL do documento no Índice. </p> <p>Os valores <span class="uicontrol"> Primary Key </span> devem ser exclusivos em todos os documentos representados pela configuração do Index Connector - todos os duplicados encontrados serão ignorados. Se os documentos de origem não contiverem um único valor exclusivo para uso como <span class="uicontrol"> Chave Primária </span>, mas dois ou mais campos agrupados <i>podem</i> formar um identificador exclusivo, você poderá definir a <span class="uicontrol"> Chave Primária </span> combinando vários valores de <span class="uicontrol"> Coluna </span> com uma barra vertical ("|") delimitando os valores. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> Remover HTML?  </span> <p>Quando essa opção estiver marcada, todas as tags HTML encontradas nos dados desse campo serão removidas. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Ação </span> <p>Permite adicionar linhas ao mapa ou remover linhas do mapa. A ordem das linhas não é importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fonte de dados: Feed</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativado </p> </td> 
      <td colname="col2"> <p>Ativa a configuração "on" para rastrear e indexar. Ou, você pode desativar a configuração para evitar o rastreamento e a indexação. </p> <p> <b>Observação</b>: As configurações do Conector de índice desativado serão ignoradas se forem encontradas em uma lista de ponto de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Endereço do host </p> </td> 
      <td colname="col2"> <p>Especifica o endereço IP ou URL do sistema host em que o arquivo de fonte de dados é encontrado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o documento XML primário que contém várias "linhas" de informações. </p> <p>O caminho é relativo à raiz do endereço do host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo incremental </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o documento XML incremental que contém várias "linhas" de informações. </p> <p>O caminho é relativo à raiz do endereço do host. </p> <p>Este arquivo, se especificado, é baixado e processado durante operações de Índice Incremental. Se nenhum arquivo for especificado, o arquivo listado em Caminho do arquivo será usado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo vertical </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o documento XML que contém várias "linhas" esparsas de informações a serem usadas durante uma atualização vertical. </p> <p>O caminho é relativo à raiz do endereço do host. </p> <p>Este arquivo, se especificado, é baixado e processado durante as operações de Atualização vertical. </p> <p> <b>Observação</b>: Este recurso não está ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Exclui o caminho do arquivo </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o arquivo de texto simples, contendo um único valor de identificador de documento por linha. </p> <p>O caminho é relativo à raiz do endereço do host. </p> <p>Este arquivo, se especificado, é baixado e processado durante operações de Índice Incremental. Os valores encontrados neste arquivo são usados para construir solicitações "delete" para remover documentos indexados anteriormente. Os valores neste arquivo devem corresponder aos valores encontrados nos arquivos Caminho de arquivo completo ou incremental, na coluna identificada como <span class="uicontrol"> Chave primária </span>. </p> <p> <b>Observação</b>: Este recurso não está ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica o protocolo usado para acessar o arquivo. Você pode escolher entre as seguintes opções: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Se necessário, você pode inserir as credenciais de autenticação adequadas para acessar o servidor HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Se necessário, você pode inserir as credenciais de autenticação adequadas para acessar o servidor HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Você deve inserir as credenciais de autenticação adequadas para acessar o servidor FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Você deve inserir as credenciais de autenticação adequadas para acessar o servidor SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Arquivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Item </p> </td> 
      <td colname="col2"> <p>Identifica o elemento XML que pode ser usado para identificar linhas XML individuais no arquivo de fonte de dados especificado. </p> <p>Por exemplo, no fragmento Feed a seguir de um documento XML Adobe, o valor do ItemTag é <span class="codeph"> record </span>: </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt;&lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt;         &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt;         &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt;         &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número mínimo de documentos para indexação </p> </td> 
      <td colname="col2"> <p>Se definido como um valor positivo, isso especifica o número mínimo de registros esperado no arquivo baixado. Se forem recebidos menos registros, a operação de índice será abortada. </p> <p> <b>Observação</b>: Este recurso não está ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> <p> <b>Observação</b>: Este recurso é usado somente durante operações de Índice completo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite que você especifique mapeamentos de elemento para metadados XML, usando expressões XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Adicionar tag </span> <p>Especifica uma representação XPath dos dados XML analisados. Usando o documento Adobe XML de exemplo acima, na opção Item tag, ele pode ser mapeado usando a seguinte sintaxe: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>A sintaxe acima é traduzida como a seguinte: </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>O atributo <span class="codeph"> display url </span> do elemento <span class="codeph"> record </span> mapeia para o campo de metadados <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido num elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> title </span>, mapeia para o campo de metadados <span class="codeph"> title </span>. </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido no elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> descrição </span>, mapeia para o campo de metadados <span class="codeph"> desc </span>. </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido no elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> descrição </span>, mapeia para o campo de metadados <span class="codeph"> body </span>. </p> </li> 
      </ul> </p> <p>XPath é uma notação relativamente complicada. Mais informações estão disponíveis no seguinte local: </p> <p>Consulte <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Campo </span> <p>Define o valor do atributo name usado para cada tag <span class="codeph"> &lt;meta&gt; </span> gerada. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metadados? </span> <p>Faz com que <span class="uicontrol"> o campo </span> se torne uma lista suspensa da qual você pode selecionar campos de metadados definidos para a conta atual. </p> <p>O valor <span class="uicontrol"> Field </span> pode ser um campo de metadados indefinido, se desejado. Um campo de metadados indefinido às vezes é útil para criar conteúdo usado pelo <span class="wintitle"> Script de filtragem </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Sobre o script de filtragem </a>. </p> <p>Quando o Conector de índice processa documentos XML com várias ocorrências em qualquer campo de mapa, os vários valores são concatenados em um único valor no documento em cache resultante. Por padrão, esses valores são combinados usando um delimitador de vírgula. No entanto, suponha que o valor <span class="wintitle"> Field </span> correspondente seja um campo de metadados definido. Além disso, esse campo tem o conjunto de atributos <span class="wintitle"> Lista de permissões </span>. Nesse caso, o valor Delimitadores de Lista do campo, que é o primeiro delimitador definido, é usado na concatenação. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Chave primária?  </span> <p>Somente uma definição de mapa é identificada como a chave primária. Esse campo se torna a referência exclusiva que é apresentada quando esse documento é adicionado ao índice. Esse valor é usado no URL do documento no Índice. </p> <p>Os valores <span class="uicontrol"> Primary Key </span> devem ser exclusivos em todos os documentos representados pela configuração do Index Connector - todos os duplicados encontrados serão ignorados. Se os documentos de origem não contiverem um único valor exclusivo para uso como <span class="uicontrol"> Chave Primária </span>, mas dois ou mais campos reunidos <i>podem</i> formar um identificador exclusivo, você poderá definir a <span class="uicontrol"> Chave Primária </span> combinando várias definições <span class="uicontrol"> Tag </span> com uma barra vertical ("|") que delimita os valores. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> Remover HTML?  </span> <p>Quando essa opção estiver marcada, todas as tags HTML encontradas nos dados desse campo serão removidas. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> Usar para Excluir?  </span> <p>Usado apenas durante operações de Índice Incremental. Registros que correspondem a este padrão XPath identificam itens para exclusão. O valor <span class="uicontrol"> Primary Key </span> para cada registro é usado para construir solicitações "delete", como com Excluir caminho de arquivo. </p> <p> <b>Observação</b>: Este recurso não está ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Ação </span> <p>Permite adicionar linhas ao mapa ou remover linhas do mapa. A ordem das linhas não é importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fonte de dados: XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativado </p> </td> 
      <td colname="col2"> <p>Ativa a configuração "on" para rastrear e indexar. Ou, você pode desativar a configuração para evitar o rastreamento e a indexação. </p> <p> <b>Observação</b>: As configurações do Conector de índice desativado serão ignoradas se forem encontradas em uma lista de ponto de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Endereço do host </p> </td> 
      <td colname="col2"> <p>Especifica o endereço URL do sistema host no qual o arquivo de fonte de dados é encontrado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o documento XML primário que contém links ( 
      <code>
        &lt;a&gt; 
      </code>) para documentos XML individuais. </p> <p>O caminho é relativo à raiz do endereço do host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica o protocolo usado para acessar o arquivo. Você pode escolher entre as seguintes opções: </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>Se necessário, você pode inserir as credenciais de autenticação adequadas para acessar o servidor HTTP. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>Se necessário, você pode inserir as credenciais de autenticação adequadas para acessar o servidor HTTPS. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>Você deve inserir as credenciais de autenticação adequadas para acessar o servidor FTP. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>Você deve inserir as credenciais de autenticação adequadas para acessar o servidor SFTP. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> Arquivo </li> 
      </ul> </p> <p> <b>Observação</b>: A configuração Protocolo só é usada quando há informações especificadas nos campos Endereço do host e/ou Caminho do arquivo. Documentos XML individuais são baixados usando HTTP ou HTTPS, de acordo com suas especificações de URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Item </p> </td> 
      <td colname="col2"> <p>Identifica o elemento XML que define uma "linha" no arquivo de fonte de dados especificado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite que você especifique mapeamentos de coluna para metadados, usando números de coluna. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> Adicionar tag </span> <p>Especifica uma representação XPath dos dados XML analisados. Usando o documento Adobe XML de exemplo acima, sob a opção Item tag, é possível mapeá-lo usando a seguinte sintaxe: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>A sintaxe acima é traduzida como a seguinte: </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>O atributo <span class="codeph"> display url </span> do elemento <span class="codeph"> record </span> mapeia para o campo de metadados <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido num elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> title </span>, mapeia para o campo de metadados <span class="codeph"> title </span>. </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido no elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> descrição </span>, mapeia para o campo de metadados <span class="codeph"> desc </span>. </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido no elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> descrição </span>, mapeia para o campo de metadados <span class="codeph"> body </span>. </p> </li> 
      </ul> </p> <p>XPath é uma notação relativamente complicada. Mais informações estão disponíveis no seguinte local: </p> <p>Consulte <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> Campo </span> <p>Define o valor do atributo name usado para cada tag &lt;meta&gt; gerada. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> Metadados? </span> <p>Faz com que <span class="uicontrol"> o campo </span> se torne uma lista suspensa da qual você pode selecionar campos de metadados definidos para a conta atual. </p> <p>O valor <span class="uicontrol"> Field </span> pode ser um campo de metadados indefinido, se desejado. Um campo de metadados indefinido às vezes é útil para criar conteúdo usado pelo <span class="wintitle"> Script de filtragem </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Sobre o script de filtragem </a>. </p> <p>Quando o Conector de índice processa documentos XML com várias ocorrências em qualquer campo de mapa, os vários valores são concatenados em um único valor no documento em cache resultante. Por padrão, esses valores são combinados usando um delimitador de vírgula. No entanto, suponha que o valor <span class="wintitle"> Field </span> correspondente seja um campo de metadados definido. Além disso, esse campo tem o conjunto de atributos <span class="wintitle"> Lista de permissões </span>. Nesse caso, o valor Delimitadores de Lista do campo, que é o primeiro delimitador definido, é usado na concatenação. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> Chave primária?  </span> <p>Somente uma definição de mapa é identificada como a chave primária. Esse campo se torna a referência exclusiva que é apresentada quando esse documento é adicionado ao índice. Esse valor é usado no URL do documento no Índice. </p> <p>Os valores <span class="uicontrol"> Primary Key </span> devem ser exclusivos em todos os documentos representados pela configuração do Index Connector - todos os duplicados encontrados serão ignorados. Se os documentos de origem não contiverem um único valor exclusivo para uso como <span class="uicontrol"> Chave Primária </span>, mas dois ou mais campos reunidos <i>podem</i> formar um identificador exclusivo, você poderá definir a <span class="uicontrol"> Chave Primária </span> combinando várias definições <span class="uicontrol"> Tag </span> com uma barra vertical ("|") que delimita os valores. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> Remover HTML?  </span> <p>Quando essa opção estiver marcada, todas as tags HTML encontradas nos dados desse campo serão removidas. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> Ação </span> <p>Permite adicionar linhas ao mapa ou remover linhas do mapa. A ordem das linhas não é importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Clique em **[!UICONTROL Setup Maps]** para baixar uma amostra da sua fonte de dados. Os dados são examinados para determinar a adequação da indexação. Esse recurso está disponível apenas para tipos de texto e feed.
1. (Opcional) Clique em **[!UICONTROL Preview]** para testar o funcionamento real da configuração. Esse recurso está disponível apenas para tipos de texto e feed.
1. Clique em **[!UICONTROL Add]** para adicionar a configuração à página [!DNL Index Connector Definitions] e à lista suspensa [!DNL Index Connector Configurations] na página [!DNL URL Entrypoints].

   Consulte [Sobre pontos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).
1. Na página [!DNL Index Connector Definitions], clique em **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) Na página [!DNL Index Connector Definitions], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma definição de Conector de índice {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

Você pode editar um Conector de índice existente definido por você.

>[!NOTE]
>
>Nem todas as opções estão disponíveis para alteração, como Nome do conector de índice ou Tipo, na lista suspensa [!DNL Type].

**Para editar uma definição do Conector de índice**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Na página [!DNL Index Connector], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Edit]** para obter um nome de definição do Conector de índice cujas configurações você deseja alterar.
1. Na página [!DNL Index Connector Edit], defina as opções desejadas.

   Consulte a tabela de opções em [Adicionar uma definição de Conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Na página [!DNL Index Connector Definitions], clique em **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) Na página [!DNL Index Connector Definitions], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Exibindo as configurações de uma definição do Conector de índice {#task_D0B71A7426E54247BDB3468EC576D871}

Você pode revisar as configurações de uma definição de conector de índice existente.

Depois que uma definição do Conector de índice é adicionada à página [!DNL Index Connector Definitions], não é possível alterar a configuração Tipo. Em vez disso, você deve excluir a definição e adicionar uma nova.

**Para visualização das configurações de uma definição do Conector de índice**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Na página [!DNL Index Connector], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Edit]** para obter um nome de definição do Conector de índice cujas configurações você deseja revisar ou editar.

## Copiando uma definição do Conector de índice {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

É possível copiar uma definição existente do Conector de índice para usar como a base para um novo Conector de índice que você deseja criar.

Ao copiar uma definição de Conector de índice, a definição copiada é desativada por padrão. Para ativar ou &quot;ativar&quot; a definição, edite-a da página [!DNL Index Connector Edit] e selecione **[!UICONTROL Enable]**.

Consulte [Editar uma definição de Conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9).

**Para copiar uma definição do Conector de índice**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Na página [!DNL Index Connector], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Copy]** para obter um nome de definição do Conector de índice cujas configurações você deseja duplicado.
1. Na página [!DNL Index Connector Copy], digite o novo nome da definição.
1. Clique em **[!UICONTROL Copy]**.
1. (Opcional) Na página [!DNL Index Connector Definitions], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Renomeando uma definição de Conector de índice {#task_5132118FC21B47D99881E0ED425225D7}

Você pode alterar o nome de uma definição existente do Conector de índice.

Depois de renomear a definição, marque **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Certifique-se de que o nome da nova definição seja refletido na lista suspensa na página [!DNL URL Entrypoints].

Consulte [Adicionar vários pontos de entrada de URL que você deseja indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

**Para renomear uma definição de Conector de índice**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Na página [!DNL Index Connector], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Rename]** para o nome de definição do Conector de índice que você deseja alterar.
1. Na página [!DNL Index Connector Rename], digite o novo nome da definição no campo [!DNL Name].
1. Clique em **[!UICONTROL Rename]**.
1. Clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Se o nome do Conector de índice anterior estiver presente na lista, remova-o e adicione a entrada renomeada recentemente.

   Consulte [Adicionar vários pontos de entrada de URL que você deseja indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45). 1. (Opcional) Na página [!DNL Index Connector Definitions], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma definição de Conector de índice {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

É possível excluir uma definição existente do Conector de índice que não é mais necessária ou não é mais usada.

**Para excluir uma definição de Conector de índice**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Na página [!DNL Index Connector Definitions], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Delete]** para obter o nome de definição do Conector de índice que deseja remover.
1. Na página [!DNL Index Connector Delete], clique em **[!UICONTROL Delete]**.
