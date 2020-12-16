---
description: Use o menu Regras de regravação para definir o URL de pesquisa e as regras de título.
seo-description: Use o menu Regras de regravação para definir o URL de pesquisa e as regras de título.
seo-title: Sobre o menu Regras de regravação
solution: Target
subtopic: Rewrite Rules
title: Sobre o menu Regras de regravação
topic: Settings,Site search and merchandising
uuid: 77ee84dd-fdba-4d34-ae8e-2fe786599800
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '10216'
ht-degree: 0%

---


# Sobre o menu Regras de regravação {#about-the-rewrite-rules-menu}

Use o menu Regras de regravação para definir o URL de pesquisa e as regras de título.

## Sobre as Regras de URL da Loja de Listas de Rastreamento {#concept_B71CF4C8030A4A74A22C3BFE4DE3B865}

As Regras de URL de rastreamento especificam como os URLs encontrados no conteúdo da Web são reescritos. Você pode especificar um número ilimitado de regras e condições e pode manipular qualquer parte dos URLs encontrados.

<!-- 

c_about_crawl_list_store_url_rules.xml

 -->

As regras de rastreamento são mais úteis para regravar partes dinâmicas de um URL, como um identificador de sessão exclusivo para cada cliente que visita seu site. Você também pode usar regras de regravação para ocultar partes de um URL, como parâmetros de query, do robô de pesquisa. Por padrão, nenhuma regra é especificada e nenhuma regravação de URL é realizada.

À medida que um site é rastreado, os URLs de conteúdo incorporado são armazenados em uma lista temporária de páginas da Web adicionais para rastreamento. Antes de um URL ser adicionado a essa lista, as regras de regravação da Loja são aplicadas a ele. Normalmente, as regras de regravação de armazenamento são usadas para remover uma ID de sessão de um URL ou para aplicar uma ID de sessão específica para o rastreamento. Quando o robô de pesquisa recupera um URL da lista, as regras de regravação de recuperação são usadas para manipular partes desse URL novamente. Geralmente, as regras de recuperação são usadas para inserir dados sensíveis ao tempo de volta no URL. É este URL final que é usado para recuperar a página do seu site.

Consulte [Sobre as Regras de URL de Recuperação de Listas de Rastreamento](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Normalmente, você usa Regras de URL de loja exclusivamente. As Regras de URL de recuperação só são necessárias se os URLs contiverem dados dinâmicos, como uma ID de sessão, e se esses dados dinâmicos mudarem ao longo do tempo para permanecerem válidos. Nesse caso, use Regras de URL de loja para obter o estado mais recente dos dados dos URLs encontrados. Em seguida, use a opção Recuperar regras de URL para adicionar esses dados a cada URL quando o robô de pesquisa tentar recuperar a página.

Cada regra é especificada com uma diretiva de regra de regravação (RewriteRule) e uma ou mais condições de regravação opcionais (RewriteCond). A ordem das regras é importante. O conjunto de regras é repetido por regra. Quando uma regra corresponde, ela repete todas as condições de regravação correspondentes. Uma regra de URL de rastreamento é especificada da seguinte maneira:

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Quando um URL incorporado é encontrado, o robô de pesquisa tenta corresponder o URL ao Padrão de cada regra de rastreamento. Se o padrão corresponder, o mecanismo de regravação procurará as diretivas RewriteCond correspondentes. Se nenhuma condição estiver presente, o URL será substituído por um novo valor construído a partir da string Substituição e continuará com a próxima regra no conjunto de regras. Se houver condições, elas serão processadas na ordem em que estão listadas. O mecanismo de regravação tenta corresponder um padrão de condição (CondPattern) a uma string de teste (TestString). Se as duas corresponderem, a próxima condição será processada até que não haja mais condições disponíveis. Se todas as condições corresponderem, o URL será substituído pela Substituição especificada na regra. Se a condição não for atendida, o conjunto completo de condições e a regra correspondente falharão.

## Sobre as diretivas RewriteRule {#section_162122340BB34F12BB9A36DC9349092B}

Uma diretiva RewriteRule tem o seguinte formato:

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` pode ser uma expressão regular POSIX, que é aplicada ao URL atual. O &quot;URL atual&quot; pode ser diferente do URL solicitado original, pois regras anteriores podem já ter correspondido e alterado o URL.

Consulte [Expressões regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Não é possível usar o caractere &quot;não&quot; (&#39;!&#39;) para prefixar o padrão. O caractere &quot;não&quot; permite negar um padrão, ou seja, ser verdadeiro somente se o URL atual NÃO corresponder a esse padrão. O caractere &quot;não&quot; pode ser usado quando é melhor corresponder a um padrão negativo ou como uma regra padrão final.

>[!NOTE]
>
>Não é possível usar o caractere &quot;não&quot; e curingas agrupadas em um padrão. Além disso, não é possível usar um padrão negado quando a string de substituição contém $N.

Você pode usar parênteses para criar uma referência retroativa no padrão, que pode ser referenciada pela Substituição e CondPattern.

**** SubstituiçãoO URL é substituído pela string de substituição, que contém o seguinte:

Texto sem formatação: Texto que é passado inalterado.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Estes são os dois tipos de referências retroativas:

* **RewriteRule** BackreferencesElas correspondem às referências anteriores no RewriteRule Pattern correspondente e assumem a forma $N (0  &lt;> Por exemplo, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* **RewriteCond** BackreferencesEssas backreferences correspondem no último RewriteCond Cond CondPattern correspondente e assumem o formato %N (0)  &lt;>

Variáveis: São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE é uma string para o nome de uma variável definida. Consulte o sinalizador `*[E]*` para obter mais informações sobre como configurar variáveis de ambiente.

Funções: Essas são funções do formulário ${NAME_OF_FUNCTION:key}, onde NAME_OF_FUNCTION é o seguinte:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* O URL de escape codifica todos os caracteres em *key*.
* Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados; os espaços são convertidos em &#39;+&#39; e todos os outros caracteres são transformados em seu equivalente codificado em URL %xx.
* unescape transforma &#39;+&#39; de volta ao espaço e todos os caracteres codificados por URL %xx de volta em caracteres únicos.

>[!NOTE]
>
>Existe uma string de substituição especial: `'-'` isso significa &quot;substituição NO.&quot; A string `'-'` é frequentemente usada com o sinalizador C (cadeia), permitindo que você corresponda um URL a vários padrões antes que ocorra uma substituição.

**Sinalizadores**

(opcional) Inclua sinalizadores entre colchetes `[]`. Vários sinalizadores são separados por vírgulas.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Última regra. </p> <p>Interrompe o processo de regravação e não aplica regras adicionais de regravação. Use esse sinalizador para impedir qualquer processamento adicional no URL atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Próxima rodada. </p> <p> Executa novamente o processo de regravação (iniciando novamente com a primeira regra de regravação) usando o URL da última regra de regravação (não o URL original). Tenha cuidado para não criar um ciclo de vida! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Encadeado com a próxima regra. </p> <p>Encadeia a regra atual para a regra seguinte (que também pode ser encadeada à regra a seguir e assim por diante). Se uma regra corresponde, o processo de substituição continua como de costume. Se a regra não corresponder, todas as regras encadeadas subsequentes serão ignoradas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Nenhum caso. </p> <p> Faz com que o Padrão não diferencie maiúsculas de minúsculas (ou seja, não há diferença entre 'A-Z' e 'a-z') quando o padrão é comparado ao URL atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignore a regra ou as regras seguintes. </p> <p> Se a regra atual corresponder, esse sinalizador forçará o mecanismo de regravação a ignorar as regras de próximo número no conjunto de regras. Use esse sinalizador para criar construções pseudo if-then-else. A última regra da cláusula then torna-se um skip=N, onde N é o número de regras na cláusula else. </p> <p> <p>Observação:  Este sinalizador não é igual ao sinalizador 'chain|C'!) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Define a variável de ambiente. </p> <p>Cria uma variável ambiental "VAR" definida como valor VAL, onde VAL pode conter referências anteriores regulares do expressão, $N e %N, que são expandidas. Você pode usar esse sinalizador mais de uma vez para definir várias variáveis. As variáveis podem ser removidas posteriormente de referência em um padrão RewriteCond a seguir via %{VAR}. </p> <p>Use esse sinalizador para retirar e lembrar informações de URLs. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>As Regras de regravação da loja e as Regras de regravação da recuperação compartilham valores variáveis. Devido a esse comportamento, é possível definir uma variável para um valor de sessionid que diferencia tempo quando um URL incorporado é encontrado e armazenado. Quando o próximo URL é recuperado da lista temporária do armazenamento, o valor sessionid mais recente pode ser adicionado a ele antes que essa página seja recuperada.

**Exemplo de uma RewriteRule com uma função**

Suponha que você tenha um servidor que diferencia maiúsculas de minúsculas, que lida com as strings `"www.mydomain.com"` e `"www.MyDomain.com"` de forma diferente. Para que o servidor funcione corretamente, verifique se o domínio é sempre `"www.mydomain.com"`, mesmo que alguns documentos contenham links que façam referência a `"www.MyDomain.com."` Para isso, você pode usar a seguinte regra:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Essa regra de regravação usa a função `tolower` para regravar a parte de domínio de um URL, a fim de garantir que ela sempre esteja em minúsculas, como a seguir:

1. O Padrão `(^https://([^/]*)(.*)$)` contém uma referência retroativa `([^/]*)` que corresponde a todos os caracteres entre `https://` e o primeiro `/` no URL. O padrão também contém uma segunda referência retroativa `(.*)` que corresponde a todos os caracteres restantes no URL.

1. A Substituição `(https://${tolower:$1}$2)` diz ao mecanismo de pesquisa para regravar o URL usando a função `tolower` na primeira referência retroativa `(https:// ${tolower:$1}$2)` deixando o restante do URL intocado `(https://${tolower:$1} $2)`.

Assim, um URL do formulário `https://www.MyDomain.com/INTRO/index.Html` é regravado como `https://www.mydomain.com/INTRO/index.Html`.

## Sobre as diretivas RewriteCond {#section_CD5A19B2D3204F73B645411931FC34A1}

A diretiva RewriteCond define uma condição de regra. Quando um RewriteCond precede uma RewriteRule, a regra é usada somente se seu padrão corresponder ao título atual e se as condições adicionais se aplicarem. As condições de regravação assumem a seguinte forma:

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` é uma string que pode conter as seguintes construções:

Texto simples: Texto que é passado inalterado.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Estes são os dois tipos de referências retroativas:

* **RewriteRule** BackreferencesElas correspondem às referências anteriores no RewriteRule Pattern correspondente e assumem a forma $N (0  &lt;> Por exemplo, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RewriteCond** BackreferencesEssas backreferences correspondem no último RewriteCond Cond CondPattern correspondente e assumem o formato %N (0)&lt;>

Variáveis: São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE pode ser uma string para o nome de uma variável definida. Consulte o sinalizador RewriteRule *`[E]`* para obter mais informações sobre como configurar variáveis.

Funções: Essas são funções do formulário ${NAME_OF_FUNCTION:key}, onde NAME_OF_FUNCTION é o seguinte:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* URL de escape codifica todos os caracteres na chave. Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados, os espaços são convertidos em &#39;+&#39; e todos os outros caracteres são transformados em seu equivalente `%xx` codificado em URL.
* unescape transforma &#39;+&#39; de volta para o espaço e todos os caracteres codificados de URL `%xx` de volta em caracteres únicos.

**** CondPatternis é uma Expressão regular estendida padrão com algumas adições. A string de padrão pode ser prefixada com um caractere `!` (ponto de exclamação) para especificar um padrão não correspondente. Em vez de strings de expressão regulares reais, você pode usar uma das seguintes variantes especiais:

>[!NOTE]
>
>Você também pode prefixar todos esses testes com um ponto de exclamação (&#39;!&#39;) negar o seu significado.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sequência CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexicamente menos. </p> <p> Trata o CondPattern como uma string simples e o compara lexicamente ao TestString. True se TestString for lexicamente menor que CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexicamente maior. </p> <p> Trata o CondPattern como uma string simples e o compara lexicamente ao TestString. True se TestString for lexicamente maior que CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexicamente igual. </p> <p> Trata o CondPattern como uma string simples e o compara lexicamente ao TestString. True se TestString for lexicamente igual a CondPattern, ou seja, as duas strings serão exatamente iguais (caractere por caractere). Se CondPattern for apenas "" (duas aspas), isso compara TestString à string vazia. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sinalizadores**
 (opcional) Encaixe sinalizadores entre colchetes  `[]`. Vários sinalizadores são separados por vírgulas.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Nenhum caso. </p> <p>Esse sinalizador faz com que o teste não diferencie maiúsculas de minúsculas, ou seja, não há diferença entre 'A-Z' e 'a-z' tanto no TestString expandido quanto no CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>Ou a próxima condição. </p> <p>Use esse sinalizador para combinar condições de regras com um OU local em vez do E implícito. Sem esse sinalizador, você teria que escrever a segunda/regra várias vezes. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**

Algumas páginas da Web atribuem uma variável CGI &quot;sessionid&quot; na primeira vez que um visitante chega a um site. Essa variável é usada para identificar o visitante e, à medida que o visitante navega pelo site, a variável é transmitida. Como o robô de pesquisa se parece com um visitante do site, ele recebe um número &quot;sessionid&quot;. O robô de pesquisa mantém esse único valor &quot;sessionid&quot;, mesmo se uma segunda página do site tentar atribuir um novo valor. Para garantir isso, você precisa de duas regras de regravação.

A primeira regra é usada para identificar e armazenar a variável sessionid:

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

A RewriteRule usa um sinalizador E `([E=sessionid:$1])` para atribuir o valor atual do parâmetro CGI sessionid à variável `sessionid`. O `$1` refere-se à primeira referência retrospectiva, que está contida entre o primeiro conjunto de parênteses no Padrão de RewriteRule `([^&#]+)`.

A expressão regular `^&#]+` corresponde a parte de um URL entre a palavra `sessionid` e o caractere `**&**or**#**` seguinte. Como essa RewriteRule é usada apenas para criar o valor inicial para a variável sessionid, ela não regravará. Observe que o campo Substituição da regra está definido como `-` para indicar que nenhuma regravação é necessária.

O RewriteCond examina a variável `sessionid` ( `%{sessionid}`). Se ele não tiver nem mesmo um caractere único (!.+), em seguida, a RewriteRule corresponde.

Usando essa regra, o URL é lido como `https://www.domain.com/home/?sessionid=1234&function=start` e atribui o valor `1234` à variável `sessionid`.

A segunda regra é usada para regravar todos os URLs que correspondem ao seguinte padrão RewriteRule:

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

O padrão RewriteRule contém duas referências anteriores: `(.+)` e `(.*)`. A primeira referência retroativa corresponde a todos os caracteres antes de `sessionid`. A segunda referência retroativa corresponde a todos os caracteres após o encerramento `&` ou `#`.

O padrão de Substituição regrava o URL usando a primeira referência retroativa, seguida pela string &quot;sessionid=&quot;, seguida pelo valor da variável da ID da sessão definida pela primeira regra `%{sessionid}`, seguida pela segunda referência retroativa. `($1sessionid=%{sessionid} $2)`

Observe que esta RewriteRule não contém uma RewriteCond. Dessa forma, isso gera uma regravação para todos os URLs que correspondem a RewriteRule *Pattern*. Assim, se o valor da variável sessionid ( `%{sessionid}`) for `1234`, um URL do formulário `https://www.domain.com/products/?sessionid=5678&function=buy` será regravado como `https://www.domain.com/products/?sessionid=1234&function=buy`

## Confirmação {#section_B17088EF38244496BC1DDD4ECF75EB5B}

O software do mecanismo de regravação foi desenvolvido originalmente pelo Apache Group para uso no projeto do servidor HTTP Apache (https://www.apache.org/).

## Adicionando uma regra de URL do repositório de listas de rastreamento {#task_22DD40DF95584B12BE8E6ECFBF579BCD}

Você pode adicionar regras de URL do repositório de listas de rastreamento para especificar como os URLs encontrados no conteúdo da Web são regravados. Você pode especificar um número ilimitado de regras e condições e pode manipular qualquer parte dos URLs encontrados.

<!-- 

t_adding_a_crawl_list_store_url_rule.xml

 -->

**Para adicionar regras de URL do repositório de listas de rastreamento**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Store URL Rules]**.
1. No campo [!DNL Crawl List Store URL Rules], insira as regras desejadas.

   São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash).
1. (Opcional) Na página [!DNL Crawl List Store URL Rules], no campo [!DNL Test Crawl List Store URL Rules], digite um URL de teste cujas regras de rastreamento você deseja testar e clique em **Testar**.
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Crawl List Store URL Rules], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre a Lista de rastreamento Recuperar Regras de URL {#concept_EC8E2E48B99A458D8567B526C9827CBA}

As Regras de URL de rastreamento especificam como os URLs encontrados no conteúdo da Web são reescritos. Você pode especificar um número ilimitado de regras e condições e pode manipular qualquer parte dos URLs encontrados.

<!-- 

c_about_crawl_list_retrieve_url_rules.xml

 -->

Antes de os efeitos das regras serem visíveis para os clientes, recrie o índice do site.

As regras de rastreamento são mais úteis para regravar partes dinâmicas de um URL, como um identificador de sessão exclusivo para cada cliente que visita seu site. Você também pode usar regras de regravação para ocultar partes de um URL, como parâmetros de query, do robô de pesquisa. Por padrão, nenhuma regra é especificada e nenhuma regravação de URL é realizada.

À medida que um site é rastreado, os URLs de conteúdo incorporado são armazenados em uma lista temporária de páginas da Web adicionais para rastreamento. Quando o robô de pesquisa recupera um URL da lista, as Regras de regravação de recuperação são usadas para manipular partes desse URL. Normalmente, as regras de recuperação são usadas para inserir dados que fazem distinção de tempo em um URL. É este URL final que é usado para recuperar a página do seu site.

As Regras de regravação só são necessárias se os URLs contiverem dados dinâmicos, como uma ID de sessão, e se esses dados dinâmicos mudarem ao longo do tempo para permanecerem válidos. Nesse caso, use Regras de regravação de armazenamento para obter o estado mais recente dos dados dos URLs encontrados. Em seguida, use a opção Recuperar regras de regravação para adicionar esses dados a cada URL quando os robôs de pesquisa recuperarem a página.

Cada regra é especificada com uma diretiva de regra de regravação (RewriteRule) e uma ou mais condições de regravação opcionais (RewriteCond). A ordem das regras é importante. O conjunto de regras é repetido por regra. Quando uma regra corresponde, ela repete todas as condições de regravação correspondentes. Uma regra de URL de rastreamento é especificada da seguinte maneira:

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Quando um URL incorporado é encontrado, o robô de pesquisa tenta corresponder o URL ao Padrão de cada regra de rastreamento. Se o padrão corresponder, o mecanismo de regravação procurará as diretivas RewriteCond correspondentes. Se nenhuma condição estiver presente, o URL será substituído por um novo valor construído a partir da string Substituição e continuará com a próxima regra no conjunto de regras. Se houver condições, elas serão processadas na ordem em que estão listadas. O mecanismo de regravação tenta corresponder um padrão de condição (CondPattern) a uma string de teste (TestString). Se as duas corresponderem, a próxima condição será processada até que não haja mais condições disponíveis. Se todas as condições corresponderem, o URL será substituído pela Substituição especificada na regra. Se a condição não for atendida, o conjunto completo de condições e a regra correspondente falharão.

## Sobre as diretivas RewriteRule {#section_32B24B29627946398AFBC5F869A610CB}

Uma diretiva RewriteRule tem o seguinte formato:

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` pode ser uma expressão regular POSIX, que é aplicada ao URL atual. O &quot;URL atual&quot; pode ser diferente do URL solicitado original, pois regras anteriores podem já ter correspondido e alterado o URL.

Consulte [Expressões regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Não é possível usar o caractere &quot;não&quot; (&#39;!&#39;) para prefixar o padrão. O caractere &quot;não&quot; permite negar um padrão, ou seja, ser verdadeiro somente se o URL atual NÃO corresponder a esse padrão. O caractere &quot;não&quot; pode ser usado quando é melhor corresponder a um padrão negativo ou como uma regra padrão final.

>[!NOTE]
>
>Não é possível usar o caractere &quot;não&quot; e curingas agrupadas em um padrão. Além disso, não é possível usar um padrão negado quando a string de substituição contém $N.

Você pode usar parênteses para criar uma referência retroativa no padrão, que pode ser referenciada pela Substituição e CondPattern.

**** SubstituiçãoO URL é substituído pela string de substituição, que contém o seguinte:

Texto sem formatação: Texto que é passado inalterado.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Estes são os dois tipos de referências retroativas:

* **RewriteRule** BackreferencesElas correspondem às referências anteriores no RewriteRule Pattern correspondente e assumem a forma $N (0  &lt;> Por exemplo, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* ** RewriteCond Backreferences** Essas referências retroativas correspondem na última RewriteCond Cond CondPattern correspondente e têm o formato %N (0 &lt;= N &lt;= 9).

Variáveis: São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE é uma string para o nome de uma variável definida. Consulte o sinalizador *[E]* para obter mais informações sobre como configurar variáveis de ambiente.

Funções: Essas são funções do formulário ${NAME_OF_FUNCTION:key}, onde NAME_OF_FUNCTION é o seguinte:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* O URL de escape codifica todos os caracteres em *key*.
* Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados; os espaços são convertidos em &#39;+&#39; e todos os outros caracteres são transformados em seu equivalente codificado em URL %xx.
* unescape transforma &#39;+&#39; de volta ao espaço e todos os caracteres codificados por URL %xx de volta em caracteres únicos.

>[!NOTE]
>
>Existe uma string de substituição especial: &quot;-&quot; significa &quot;substituição de NO&quot;. A string &#39;-&#39; é usada com o sinalizador C (cadeia), permitindo que você corresponda um URL a vários padrões antes que ocorra uma substituição.

**Sinalizadores**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Última regra. </p> <p>Interrompe o processo de regravação e não aplica regras adicionais de regravação. Use esse sinalizador para impedir qualquer processamento adicional no URL atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Próxima rodada. </p> <p> Executa novamente o processo de regravação (iniciando novamente com a primeira regra de regravação) usando o URL da última regra de regravação (não o URL original). Tenha cuidado para não criar um ciclo de vida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Encadeado com a próxima regra. </p> <p>Encadeia a regra atual para a regra seguinte (que também pode ser encadeada à regra a seguir e assim por diante). Se uma regra corresponde, o processo de substituição continua como de costume. Se a regra não corresponder, todas as regras encadeadas subsequentes serão ignoradas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Nenhum caso. </p> <p> Faz com que o Padrão não diferencie maiúsculas de minúsculas (ou seja, não há diferença entre 'A-Z' e 'a-z') quando o padrão é comparado ao URL atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignore a regra ou as regras seguintes. </p> <p> Se a regra atual corresponder, esse sinalizador forçará o mecanismo de regravação a ignorar as regras de próximo número no conjunto de regras. Use esse sinalizador para criar construções pseudo if-then-else. A última regra da cláusula then torna-se um skip=N, onde N é o número de regras na cláusula else. </p> <p> <p>Observação:  Este sinalizador não é igual ao sinalizador 'chain|C'!) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Define a variável de ambiente. </p> <p>Cria uma variável ambiental "VAR" definida como valor VAL, onde VAL pode conter referências anteriores regulares do expressão, $N e %N, que são expandidas. Você pode usar esse sinalizador mais de uma vez para definir várias variáveis. As variáveis podem ser removidas posteriormente de referência em um padrão RewriteCond a seguir via %{VAR}. </p> <p>Use esse sinalizador para retirar e lembrar informações de URLs. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>As Regras de regravação da loja e as Regras de regravação da recuperação compartilham valores variáveis. Devido a esse comportamento, é possível definir uma variável para um valor de sessionid que diferencia tempo quando um URL incorporado é encontrado e armazenado. Quando o próximo URL é recuperado da lista temporária do armazenamento, o valor sessionid mais recente pode ser adicionado a ele antes que essa página seja recuperada.

**Exemplo de uma RewriteRule com uma função**

Suponha que você tenha um servidor que diferencia maiúsculas de minúsculas, que lida com as strings &quot;www.mydomain.com&quot; e &quot;www.MyDomain.com&quot; de forma diferente. Para que o servidor funcione corretamente, verifique se o domínio é sempre &quot;www.mydomain.com&quot;, mesmo que alguns documentos contenham links que façam referência a &quot;www.MyDomain.com&quot;. Para fazer isso, você pode usar a seguinte regra:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Essa regra de regravação usa a função `tolower` para regravar a parte de domínio de um URL, a fim de garantir que ela sempre esteja em minúsculas, como a seguir:

1. O Padrão `(^https://([^/]*)(.*)$)` contém uma referência retrospectiva ** `([^/]*)`** que corresponde a todos os caracteres entre `https://` e o primeiro `/` no URL. O padrão também contém uma segunda referência retroativa `(.*)` que corresponde a todos os caracteres restantes no URL.
1. A Substituição `(https://${tolower:$1}$2)` diz ao mecanismo de pesquisa para regravar o URL usando a função `tolower` na primeira referência retroativa `(https:// ${tolower:$1}$2)` deixando o restante do URL intocado `(https://${tolower:$1} $2)`.

Assim, um URL do formulário `https://www.MyDomain.com/INTRO/index.Html` é regravado como `https://www.mydomain.com/INTRO/index.Html`.

## Sobre as diretivas RewriteCond {#section_ADD642A24B68452CB98294A0BD687EC3}

A diretiva RewriteCond define uma condição de regra. Quando um RewriteCond precede uma RewriteRule, a regra é usada somente se seu padrão corresponder ao título atual e se as condições adicionais se aplicarem. As condições de regravação assumem a seguinte forma:

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` é uma string que pode conter as seguintes construções:

Texto simples: Texto que é passado inalterado.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Estes são os dois tipos de referências retroativas:

* **RewriteRule** BackreferencesElas correspondem às referências anteriores no RewriteRule Pattern correspondente e assumem a forma $N (0  &lt;> Por exemplo, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RewriteCond** BackreferencesEssas backreferences correspondem no último RewriteCond Cond CondPattern correspondente e assumem o formato %N (0)&lt;>

Variáveis: São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE pode ser uma string para o nome de uma variável definida. Consulte o sinalizador RewriteRule *`[E]`* para obter mais informações sobre como configurar variáveis.

Funções: Essas são funções do formulário ${NAME_OF_FUNCTION:key}, onde NAME_OF_FUNCTION é o seguinte:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* URL de escape codifica todos os caracteres na chave. Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados, os espaços são convertidos em &#39;+&#39; e todos os outros caracteres são transformados em seu equivalente codificado em URL %xx.
* unescape transforma &#39;+&#39; de volta ao espaço e todos os caracteres de codificação de URL %xx de volta em caracteres únicos.

**** CondPatternis é uma Expressão regular estendida padrão com algumas adições. A string de padrão pode ser prefixada com um &#39;!&#39; (ponto de exclamação) para especificar um padrão não correspondente. Em vez de strings de expressão regulares reais, você pode usar uma das seguintes variantes especiais:

>[!NOTE]
>
>Você também pode prefixar todos esses testes com um ponto de exclamação (&#39;!&#39;) negar o seu significado.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sequência CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexicamente menos. </p> <p> Trata o CondPattern como uma string simples e o compara lexicamente ao TestString. True se TestString for lexicamente menor que CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexicamente maior. </p> <p> Trata o CondPattern como uma string simples e o compara lexicamente ao TestString. True se TestString for lexicamente maior que CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexicamente igual. </p> <p> Trata o CondPattern como uma string simples e o compara lexicamente ao TestString. True se TestString for lexicamente igual a CondPattern, ou seja, as duas strings serão exatamente iguais (caractere por caractere). Se CondPattern for apenas "" (duas aspas), isso compara TestString à string vazia. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sinalizadores**
 (opcional) Encaixe sinalizadores entre colchetes  `[]`. Vários sinalizadores são separados por vírgulas.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Nenhum caso. </p> <p>Esse sinalizador faz com que o teste não diferencie maiúsculas de minúsculas, ou seja, não há diferença entre 'A-Z' e 'a-z' tanto no TestString expandido quanto no CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>Ou a próxima condição. </p> <p>Use esse sinalizador para combinar condições de regras com um OU local em vez do E implícito. Sem esse sinalizador, você teria que escrever a segunda/regra várias vezes. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**

Algumas páginas da Web atribuem uma variável CGI &quot;sessionid&quot; na primeira vez que um visitante chega a um site. Essa variável é usada para identificar o visitante e, à medida que o visitante navega pelo site, a variável é transmitida. Como o robô de pesquisa se parece com um visitante do site, ele recebe um número &quot;sessionid&quot;. O robô de pesquisa mantém esse único valor &quot;sessionid&quot;, mesmo se uma segunda página do site tentar atribuir um novo valor. Para garantir isso, você precisa de duas regras de regravação.

A primeira regra é usada para identificar e armazenar a variável sessionid:

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

A RewriteRule usa um sinalizador E `([E=sessionid:$1])` para atribuir o valor atual do parâmetro CGI sessionid à variável `sessionid`. O `$1` refere-se à primeira referência retrospectiva, que está contida entre o primeiro conjunto de parênteses no Padrão de RewriteRule `([^&#]+)`.

A expressão regular `^&#]+` corresponde a parte de um URL entre a palavra `sessionid` e o caractere próximo***&amp;**ou**#**. Como essa RewriteRule é usada apenas para criar o valor inicial para a variável sessionid, ela não regravará. Observe que o campo Substituição da regra está definido como `-` para indicar que nenhuma regravação é necessária.

O RewriteCond examina a variável `sessionid` ( `%{sessionid}`). Se ele não tiver nem mesmo um caractere único (!.+), em seguida, a RewriteRule corresponde.

Usando essa regra, o URL é lido como `https://www.domain.com/home/?sessionid=1234&function=start` e atribui o valor `1234` à variável `sessionid`.

A segunda regra é usada para regravar todos os URLs que correspondem ao seguinte padrão RewriteRule:

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

O padrão RewriteRule contém duas referências anteriores: `(.+)` e `(.*)`. A primeira referência retroativa corresponde a todos os caracteres antes de `sessionid`. A segunda referência retroativa corresponde a todos os caracteres após o encerramento `&` ou `#`.

O padrão de Substituição regrava o URL usando a primeira referência retroativa, seguida pela string &quot;sessionid=&quot;, seguida pelo valor da variável da ID da sessão definida pela primeira regra `%{sessionid}`, seguida pela segunda referência retroativa. `($1sessionid=%{sessionid} $2)`

Observe que esta RewriteRule não contém uma RewriteCond. Dessa forma, isso gera uma regravação para todos os URLs que correspondem a RewriteRule *Pattern*. Assim, se o valor da variável sessionid ( `%{sessionid}`) for `1234`, um URL do formulário `https://www.domain.com/products/?sessionid=5678&function=buy` será regravado como `https://www.domain.com/products/?sessionid=1234&function=buy`

## Confirmação {#section_EC3A1DAEB5A54C93A265CB119DF91E9F}

O software do mecanismo de regravação foi desenvolvido originalmente pelo Apache Group para uso no projeto do servidor HTTP Apache (https://www.apache.org/).

## Adicionar regras de URL de recuperação de lista de rastreamento {#task_94A28ED7DC404BFF9767DBB5ADEE6B7A}

Você pode adicionar regras de URL de recuperação de lista de rastreamento para especificar como URLs encontrados no conteúdo da Web são reescritos. As Regras de regravação só são necessárias se os URLs contiverem dados dinâmicos, como uma ID de sessão, e se esses dados dinâmicos mudarem ao longo do tempo para permanecerem válidos.

<!-- 

t_adding_crawl_list_retrieve_url_rules.xml

 -->

**Para adicionar lista de rastreamento, recupere regras de URL**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**.
1. No campo [!DNL Crawl List Retrieve URL Rules], insira as regras desejadas.

   São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash).
1. (Opcional) Na página [!DNL Crawl List Retrieve URL Rules], no campo [!DNL Test Crawl List Retrieve URL Rules], digite um URL de teste cujas regras de rastreamento você deseja testar e clique em **Testar**.
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Crawl List Retrieve URL Rules], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre as Regras de Título de Rastreamento {#concept_BD3A576987DA4D93A998B0B9CDDC3C79}

As Regras de Título de Rastreamento especificam como os títulos encontrados no conteúdo da Web são regravados antes de serem armazenados no índice de pesquisa.

<!-- 

c_about_crawl_title_rules.xml

 -->

Por exemplo, você pode usar uma regra de regravação para remover uma parte de um título, como o nome de uma organização. À medida que um site é rastreado, os títulos encontrados são armazenados em um buffer temporário. No entanto, antes que um título seja adicionado a esse buffer, as regras de título são aplicadas a ele. Por padrão, a pesquisa/comercialização do site não tem regras de título de rastreamento e não faz modificações de título.

Antes de os efeitos das regras serem visíveis para os clientes, recrie o índice do site.

É possível reverter rapidamente quaisquer alterações feitas nas Regras de título de rastreamento usando o recurso Histórico.

As regras podem consistir em dois elementos principais: RewriteRule e RewriteCond opcionais. Você pode especificar um número ilimitado de regras e condições. A ordem dessas regras é importante porque o conjunto de regras é repetido por regra. Quando uma regra corresponde, ela repete qualquer condição de regravação (opcional) correspondente. As regras de URL de rastreamento são especificadas da seguinte maneira:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Quando um título é encontrado, o robô de pesquisa tenta corresponder o título ao Padrão de cada regra de rastreamento. Se o padrão corresponder, o mecanismo de regravação procurará as diretivas RewriteCond correspondentes. Se nenhuma condição estiver presente, o URL será substituído por um novo valor construído a partir da string Substituição e continuará com a próxima regra no conjunto de regras. Se houver condições, elas serão processadas na ordem em que estão listadas. O mecanismo de regravação tenta corresponder um padrão de condição (CondPattern) a uma string de teste (TestString). Se as duas corresponderem, a próxima condição será processada até que não haja mais condições disponíveis. Se todas as condições corresponderem, o URL será substituído pela Substituição especificada na regra. Se a condição não for atendida, o conjunto completo de condições e a regra correspondente falharão.

Digite as Regras de URL de rastreamento na caixa de texto e clique em Salvar alterações. São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash). Para testar as regras de pesquisa, insira um URL de teste na caixa de texto &quot;Testar regras de regravação&quot; e clique em Testar.

## Diretiva RewriteRule {#section_669445C505754E838E14029D6583D9B6}

Cada diretiva RewriteRule define uma regra de regravação. As regras são aplicadas na ordem em que estão listadas. Uma regra de regravação assume o seguinte formato:

```
RewriteRule Pattern Substitution [Flags]
```

**O** padrão pode ser uma expressão regular POSIX, que é aplicada ao título atual. O &quot;título atual&quot; difere do título original, pois as regras anteriores já correspondem e o alteraram.

Consulte [Expressões regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Você pode usar o caractere &quot;não&quot; (&#39;!&#39;) para prefixar o padrão. O caractere &quot;não&quot; permite negar um padrão, ou seja, ser verdadeiro somente se o título atual NÃO corresponder ao padrão. O caractere &quot;não&quot; pode ser usado quando é melhor corresponder a um padrão negativo ou como uma regra padrão final. Observação: Não é possível usar o caractere &quot;não&quot; e curingas agrupadas em um padrão. Além disso, não é possível usar um padrão negado quando a string de substituição contém $N.

Você pode usar parênteses para criar uma referência retroativa, que pode ser referenciada pela Substituição e CondPattern.

**** SubstituiçãoO título é substituído pela string de substituição. A string pode conter o seguinte:

Texto sem formatação - texto que é transmitido sem alterações.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Estes são dois tipos de referências retroativas:

* Referências retroativas de RewriteRule

   Elas correspondem às referências anteriores no Padrão RewriteRule correspondente e assumem a forma $N (0 &lt;= N &lt;= 9). Por exemplo, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* Referências retroativas de RewriteCond

   Essas referências retroativas correspondem no último RewriteCond Cond CondPattern correspondente e assumem o formato %N (0 &lt;= N &lt;= 9).

Variáveis São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE pode ser uma string para o nome de uma variável definida. Consulte o sinalizador `[E]` para obter mais informações sobre como configurar variáveis de ambiente.

Funções São funções do formulário ${NAME_OF_FUNCTION: key} onde NAME_OF_FUNCTION é:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.

>[!NOTE]
>
>Existe uma string de substituição especial: &quot;-&quot; significa &quot;substituição de NO&quot;. A string &#39;-&#39; geralmente é útil com o sinalizador C (cadeia), permitindo que você corresponda um título a vários padrões antes que ocorra uma substituição.

**Sinalizadores** (opcional)

Os sinalizadores estão entre colchetes `[]`e vários sinalizadores são separados por vírgulas:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Última regra. </p> <p> Interrompe o processo de regravação e não aplica regras adicionais de regravação. Use esse sinalizador para impedir qualquer processamento adicional no título atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Próxima rodada. </p> <p> Executa novamente o processo de regravação (iniciando novamente com a primeira regra de regravação) usando o título da última regra de regravação, não o título original. Tenha cuidado para não criar um ciclo sem saída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Encadeado com a próxima regra. </p> <p>Encadeia a regra atual para a regra seguinte (que também pode ser encadeada à regra a seguir e assim por diante). Se uma regra corresponde, o processo de substituição continua como de costume. Se a regra não corresponder, todas as regras encadeadas subsequentes serão ignoradas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Nenhum caso. </p> <p>Faz com que o Padrão não diferencie maiúsculas de minúsculas (ou seja, não há diferença entre 'A-Z' e 'a-z') quando o padrão é comparado ao título atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignorar a regra ou as regras seguintes. </p> <p> Se a regra atual corresponder, esse sinalizador forçará o mecanismo de regravação a ignorar as regras de próximo número no conjunto de regras. Use-o para criar construções pseudo if-then-else. A última regra da cláusula then torna-se um skip=N, onde N é o número de regras na cláusula else. (Observação: Não é o mesmo que o sinalizador 'chain|C'!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Defina a variável ambiente. </p> <p> Cria uma variável ambiental "VAR" definida como valor VAL, onde VAL pode conter referências anteriores regulares do expressão, $N e %N, que é expandida. Você pode usar esse sinalizador mais de uma vez para definir várias variáveis. As variáveis podem ser referenciadas posteriormente em um padrão RewriteCond a seguir via %{VAR}. Use esse sinalizador para retirar e lembrar informações dos títulos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Diretiva RewriteCond (opcional) {#section_D664B71DE3884E0790531804C49A3222}

A diretiva RewriteCond define uma condição de regra. Quando um RewriteCond precede uma RewriteRule, a regra é usada somente se seu padrão corresponder ao título atual e se as condições adicionais se aplicarem.

As diretivas de condição de regravação assumem a seguinte forma:

```
RewriteCond TestString CondPattern [Flags] 
```

**** TestStringis é uma string que pode conter as seguintes construções:

Texto sem formatação - texto que é transmitido sem alterações.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Há dois tipos de referências retroativas:

* Referências retroativas de RewriteRuleCorrespondem às referências retroativas no Padrão RewriteRule correspondente e assumem a forma $N (0 &lt;= N &lt;= 9). Por exemplo, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* Referências retroativas de RewriteCondCorrespondem às referências retroativas na última correspondência de RewriteCond CondPattern e assumem a forma %N (0 &lt;= N &lt;= 9).

Variáveis São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE pode ser uma string para o nome de uma variável definida. Consulte o sinalizador `[E]` para obter mais informações sobre como configurar variáveis de ambiente.

Funções São funções do formato ${NAME_OF_FUNCTION:key}, onde NAME_OF_FUNCTION é:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* URL de escape codifica todos os caracteres na chave.
* Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados, os espaços são convertidos em &#39;+&#39; e todos os outros caracteres são transformados em seu equivalente codificado em URL %xx.
* unescape transforma &#39;+&#39; de volta ao espaço e todos os caracteres codificados por URL %xx de volta em caracteres únicos.

**** CondPatternis é uma Expressão regular estendida padrão com algumas adições. A string de padrão pode ser prefixada com um &#39;!&#39; (ponto de exclamação) para especificar um padrão não correspondente. Em vez de sequências de expressão regulares reais, você pode usar uma das seguintes variantes especiais.

>[!NOTE]
>
>Você pode prefixar todos esses testes com um ponto de exclamação (&#39;!&#39;) negar o seu significado.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sequência CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>É lexicamente menor. </p> <p>Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente menor que <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>É lexicamente maior. </p> <p>Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente maior que <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p> É lexicamente igual. </p> <p>Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente igual a <i>CondPattern</i>, ou seja, as duas strings serão exatamente iguais (caractere por caractere). Se <i>CondPattern</i> for apenas "" (duas aspas), isso compara <i>TestString</i> à string vazia. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sinalizadores** (opcional)

Os sinalizadores estão entre colchetes `[]`e vários sinalizadores são separados por vírgulas:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Nenhum caso. </p> <p> Torna o teste não sensível. Ou seja, não há diferença entre 'A-Z' e 'a-z' tanto no <i>TestString</i> expandido quanto no <i>CondPattern.</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p> Ou a próxima condição. </p> <p>Use esse sinalizador para combinar condições de regras com um OU local em vez do E implícito. Sem esse sinalizador, você teria que escrever a segunda/regra várias vezes. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**

Suponha que você tenha um site corporativo com um formato de título padrão: &quot;Minha Empresa&quot; seguido por um hífen e, em seguida, uma descrição específica da página (&quot;Minha Empresa - Bem-vindo&quot; ou &quot;Minha Empresa - Notícias&quot;, por exemplo). Deseja retirar &quot;Minha Empresa -&quot; do título e converter o título inteiro em letras maiúsculas quando indexar o site.

A regra de regravação a seguir usa a função toupper para regravar somente a parte descritiva de um título para maiúsculas:

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>}
```

O Padrão `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` da regra contém uma referência retroativa `(.*)` que corresponde ao conteúdo do título que segue &quot;Minha Empresa-&quot;. Lembre-se de que ao redor de uma parte de um padrão com parênteses ( ) cria uma referência retroativa que pode ser referenciada pela Substituição. Neste exemplo, a Substituição (${toupper:**$1**}) regrava aquela referência retroativa (**$1**) usando a função de toupper.

Assim, um título do formulário &quot;Minha Empresa - Bem-vindo&quot; é reescrito como &quot;BEM-VINDO&quot;.

**Reconhecimento**

O software do mecanismo de regravação foi desenvolvido originalmente pelo Apache Group para uso no projeto do servidor HTTP Apache (https://www.apache.org/).

## Adicionar regras de título de rastreamento {#task_272BB4C603BA4C9ABDBEEB398798B101}

Você pode adicionar regras de título de rastreamento para especificar como os títulos encontrados no conteúdo da Web são regravados antes de serem armazenados no índice de pesquisa.

<!-- 

t_adding_crawl_title_rules.xml

 -->

**Para adicionar regras de título de rastreamento**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl Title Rules]**.
1. No campo [!DNL Crawl Title Rules], insira as regras desejadas.

   São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash).
1. (Opcional) Na página [!DNL Crawl Title Rules], no campo [!DNL Test Crawl Title Rules], digite um URL de teste cujas regras de pesquisa você deseja testar e clique em **Testar**.
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Crawl Title Rules], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre as Regras de URL de pesquisa {#concept_017EC95E68844B6C8CC9F874F0EC8D3C}

As Regras de URL de pesquisa especificam como os URLs nos resultados de pesquisa do site devem ser exibidos. As regras operam em URLs completos. Qualquer parte do URL pode ser manipulada, incluindo argumentos de query nos quais as informações de ID da sessão são mantidas com frequência.

<!-- 

c_about_search_url_rules.xml

 -->

Normalmente, as regras de URL de pesquisa são usadas para inserir uma ID de sessão em um URL. No entanto, você também pode usar as regras de URL de pesquisa para alterar o nome do domínio exibido com seus resultados. Por padrão, nenhuma regra é especificada e nenhuma modificação de URL é executada.

As regras de URL de pesquisa podem consistir em dois elementos principais: RewriteRule e RewriteCond opcionais. Quando um URL é incluído como parte de um resultado de pesquisa, as regras são usadas para manipulá-lo. Você pode especificar um número ilimitado de regras e condições de URL de pesquisa. A ordem dessas regras é importante porque o conjunto de regras é repetido por regra. Quando uma regra corresponde, o software executa o loop por qualquer condição de regravação (opcional) correspondente. As regras de URL de rastreamento são especificadas da seguinte maneira:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Ao processar um URL, a pesquisa/comercialização do site tenta corresponder ao Padrão de cada regra de pesquisa. Se a correspondência falhar, o mecanismo de regravação interrompe imediatamente o processamento da regra e continua com a regra seguinte no conjunto. Se o padrão corresponder, o mecanismo de regravação procurará as instruções RewriteCond correspondentes. Se não houver condições, o URL será substituído por um novo valor. Esse valor é construído a partir da string Substituição e continua com a próxima regra no conjunto de regras. Se houver condições, a ordem listada será como elas serão processadas. O mecanismo de regravação tenta corresponder um padrão de condição (CondPattern) a uma string de teste (TestString). Se as duas corresponderem, a próxima condição será processada até que não haja mais condições disponíveis. Se todas as condições corresponderem, o URL será substituído pela Substituição especificada na regra. Se a condição não for atendida, o conjunto completo de condições e a regra correspondente falharão.

## Sobre a diretiva RewriteRule {#section_A3473B5B90B74DA1970213113A90591E}

Uma regra de regravação assume o seguinte formato:

```
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

**O** padrão pode ser uma expressão regular POSIX, que é aplicada ao URL atual. O &quot;URL atual&quot; pode ser diferente do URL original, pois as regras anteriores podem já ter correspondido e alterado.

Consulte [Expressões regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Você pode usar o caractere &quot;não&quot; (&#39;!&#39;) para prefixar o padrão. O caractere &quot;não&quot; permite negar um padrão. Em outras palavras, é verdadeiro somente se o URL atual NÃO corresponder ao padrão. Você pode usar o caractere &quot;não&quot; quando for melhor corresponder a um padrão negativo ou como uma regra padrão final. Observe que não é possível usar tanto o caractere &quot;não&quot; quanto os curingas agrupados em um padrão. Além disso, não é possível usar um padrão negado quando a string de substituição contém $N.

Você pode usar parênteses para criar uma referência retroativa, que pode ser referenciada pela Substituição e CondPattern.

**** SubstituiçãoO URL é completamente substituído pela string de substituição, que pode conter o seguinte:

Texto sem formatação - texto que é transmitido sem alterações.

Backreferences Fornece acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Há dois tipos de referências retroativas:

Referências retroativas de RewriteRuleCorrespondem às referências retroativas no Padrão RewriteRule correspondente e assumem a forma $N (0 &lt;= N &lt;= 9). Por exemplo, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

RewriteCond Backreferences - Correspondem às backreferences no último RewriteCond Cond CondPattern correspondente e assuma a forma %N (0 &lt;= N &lt;= 9).

Funções: Essas são funções do formulário ${NAME_OF_FUNCTION:key}, onde NAME_OF_FUNCTION é:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* O URL de escape codifica todos os caracteres em *key*.
* Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados; espaços são convertidos em &#39;+&#39;; todos os outros caracteres são transformados em seu equivalente codificado por URL %xx.
* unescape transforma &#39;+&#39; de volta ao espaço e todos os caracteres codificados por URL %xx de volta em caracteres únicos.

>[!NOTE]
>
>Existe uma string de substituição especial: &quot;-&quot; significa &quot;substituição de NO&quot;. A string &#39;-&#39; geralmente é útil em conjunto com o sinalizador C (cadeia). Ele permite que você corresponda um URL a vários padrões antes que uma substituição ocorra.

**Sinalizadores** (opcional)

Os sinalizadores estão entre colchetes `[]`e vários sinalizadores são separados por vírgulas:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Última regra. </p> <p> Pare o processo de regravação e não aplique regras adicionais de regravação. Use esse sinalizador para impedir qualquer processamento adicional no URL atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p> Próxima rodada. </p> <p>Execute novamente o processo de regravação (começando novamente com a primeira regra de regravação) usando o URL da última regra de regravação (não o URL original). Tenha cuidado para não criar um ciclo sem saída! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p> Encadeado com a próxima regra. </p> <p>Esse sinalizador encadea a regra atual à regra seguinte, que também pode ser encadeada à regra a seguir e assim por diante. Se uma regra corresponde, o processo de substituição continua como de costume. Se a regra não corresponder, todas as regras encadeadas subsequentes serão ignoradas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Nenhum caso. </p> <p>Este sinalizador faz com que o Padrão não diferencie maiúsculas de minúsculas. Em outras palavras, não há diferença entre 'A-Z' e 'a-z' quando o padrão é comparado ao URL atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignorar a regra ou as regras seguintes. </p> <p> Se a regra atual corresponder, esse sinalizador forçará o mecanismo de regravação a ignorar as regras de próximo número no conjunto de regras. Use-o para criar construções pseudo if-then-else. A última regra da cláusula then torna-se um skip=N, onde N é o número de regras na cláusula else. (Observação: Não é o mesmo que o sinalizador 'chain|C'!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Definir variável ambiental. </p> <p> Esse sinalizador cria uma variável ambiental "VAR" definida para o valor VAL. O VAL pode conter referências retroativas regulares de expressões, $N e %N, que são expandidas. Você pode usar esse sinalizador mais de uma vez para definir várias variáveis. As variáveis podem ser removidas posteriormente de referência em um padrão RewriteCond a seguir via %{VAR}. Use esse sinalizador para retirar e lembrar informações de URLs. </p> </td> 
  </tr> 
 </tbody> 
</table>

Observe que as Regras de regravação de armazenamento e as Regras de regravação de recuperação compartilham valores variáveis. Por isso, você pode definir uma variável para um valor de sessionid que diferencia tempo quando um URL incorporado é encontrado e armazenado. Quando o próximo URL é recuperado da lista temporária do armazenamento, o valor sessionid mais recente pode ser adicionado a ele antes que essa página seja recuperada.

**Exemplo**

Suponha que você tenha um servidor que diferencia maiúsculas de minúsculas. Ele lida com as strings &quot;www.mydomain.com&quot; e &quot;www.MyDomain.com&quot; de forma diferente. Para que o servidor funcione corretamente, é necessário garantir que o domínio seja sempre &quot;www.mydomain.com&quot;, mesmo que alguns documentos contenham links que fazem referência a &quot;www.MyDomain.com&quot;. Para fazer isso, você pode usar a seguinte regra:

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2 
```

Essa regra de regravação usa a função &quot;tolower&quot; para regravar a parte de domínio de um URL, a fim de garantir que ela esteja sempre em minúsculas:

1. O Padrão `(^https://([^/]*)(.*)$)` contém uma referência retroativa **`([^/]*)`** que corresponde a todos os caracteres entre &quot;https://&quot; e o primeiro &quot;/&quot; no URL. O padrão também contém uma segunda referência retroativa **(.*)** que corresponde a todos os caracteres restantes no URL.

1. A Substituição `(https://${tolower:$1}$2)` diz ao mecanismo de pesquisa para regravar o URL usando a função **tolower** na primeira referência retroativa `(https://**${tolower:$1**}$2)` deixando o restante do URL intocado `(https://${tolower:$1}*$2*)`.

Portanto, um URL do formulário `https://www.MyDomain.com/INTRO/index.Html` é regravado como `https://www.mydomain.com/INTRO/index.Html`

**Diretiva**  RewriteCond (Opcional)

A diretiva RewriteCond define uma condição de regra. Quando um RewriteCond precede uma RewriteRule, a regra é usada somente se seu padrão corresponder ao título atual e se as condições adicionais se aplicarem.

As diretivas de condição de regravação assumem a seguinte forma:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i>
```

** TestStringis é uma string que pode conter as seguintes construções:

Texto simples: Texto que é passado inalterado.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Há dois tipos de referências retroativas:

* ** RewriteRule Backreferences** Essas referências retroativas correspondem no Padrão RewriteRule correspondente e assumem a forma $N (0 &lt;= N &lt;= 9). Por exemplo, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond** BackreferencesEssas backreferences correspondem no último RewriteCond Cond CondPattern correspondente e assumem o formato %N (0)  &lt;>

Variáveis São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE pode ser uma string para o nome de uma variável definida. Consulte o sinalizador RewriteRule *`[E]`* para obter mais informações sobre como configurar variáveis.

>[!NOTE]
>
>As regras de regravação geralmente usam variáveis. Todos os parâmetros CGI do URL atual são automaticamente transformados em variáveis. Por exemplo, o URL de pesquisa `"https://search.atomz.com/search/?sp_a=sp00000000&sp_q="Product"&session=1234&id=5678"` fornecerá automaticamente quatro variáveis, que podem ser referenciadas nas regras de regravação. Neste exemplo, uma variável é chamada &quot;session&quot; e seu valor é &quot;1234&quot;, enquanto outra variável é chamada &quot;id&quot; e seu valor é &quot;5678&quot;. (As outras duas variáveis são `sp_a` e `sp_q`.) Você deve passar todas as variáveis necessárias como campos ocultos do formulário de pesquisa em sua página da Web. Neste exemplo, você deve passar os valores &quot;session&quot; e &quot;id&quot;, que identificam o usuário do site que está realizando a pesquisa. Para passar um campo oculto no formulário de pesquisa, use uma tag como `<input type=hidden name="session" value="1234">`.

Funções São funções do formato ${NAME_OF_FUNCTION:key}, onde NAME_OF_FUNCTION é:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* O URL de escape codifica todos os caracteres em *key*. Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados, os espaços são convertidos em &#39;+&#39; e todos os outros caracteres são transformados em seu equivalente codificado em URL %xx.
* unescape transforma &#39;+&#39; de volta ao espaço e todos os caracteres de codificação de URL %xx de volta em caracteres únicos.

**** CondPatternis é uma Expressão regular estendida padrão com algumas adições. A string de padrão pode ser prefixada com um &#39;!&#39; (ponto de exclamação) para especificar um padrão não correspondente. Em vez de sequências de expressão regulares reais, você pode usar uma das seguintes variantes especiais.

Você pode prefixar todos esses testes usando um ponto de exclamação (&#39;!&#39;) negar o seu significado.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sequência CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>É lexicamente menor. </p> <p> Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente menor que <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>É lexicamente maior. </p> <p> Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente maior que <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>É lexicamente igual. </p> <p> Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente igual a <i>CondPattern</i>. Ou seja, as duas strings são exatamente iguais (caractere por caractere). Se <i>CondPattern</i> for apenas "" (duas aspas), isso compara <i>TestString</i> à string vazia. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sinalizadores** (opcional)

Os sinalizadores estão entre colchetes `[]`e vários sinalizadores são separados por vírgulas:

&#39;nocase|NC&#39; (nenhum caso): Isso faz com que o teste não diferencie maiúsculas de minúsculas. Em outras palavras, não há diferença entre &#39;A-Z&#39; e &#39;a-z&#39; tanto no *TestString* expandido quanto no *CondPattern*.

&#39;ornext|OR&#39; (ou condição seguinte): Use-o para combinar condições de regras com um OU local em vez do E implícito. Sem esse sinalizador, você teria que escrever a segunda/regra várias vezes.

**Exemplo**

Algumas páginas da Web atribuem uma variável CGI &quot;sessionid&quot; na primeira vez que um cliente chega a um site. Essa variável é usada para identificar o cliente e, à medida que o cliente navega pelo site, a variável é transmitida. Como o robô de pesquisa se parece com um cliente do site, ele recebe um número &quot;sessionid&quot;. O robô de pesquisa mantém esse único valor &quot;sessionid&quot;, mesmo se uma segunda página do site tentar atribuir um novo valor. Para garantir isso, você precisa da seguinte regra de regravação:

```
RewriteCond  %{sessionid}  .+ 
RewriteRule  ^ 
<b>(.+)</b>sessionid=[^&#]+ 
<i>(.*)</i>$   
<b>$1</b>sessionid=%{sessionid} 
<i>$2</i>
```

O padrão RewriteRule contém duas referências anteriores: (.+) e (.*). A primeira referência posterior corresponde a todos os caracteres antes de &quot;sessionid=&quot;. A segunda referência retroativa corresponde a todos os caracteres após o término de &#39;&amp;&#39; ou &#39;#&#39; do sessionid.

O padrão de Substituição regrava o URL usando a primeira referência retroativa, seguida pela string &quot;sessionid=&quot;, seguida pelo valor da variável da ID da sessão, que foi transmitida como um parâmetro CGI no URL, seguido pela segunda referência retroativa. `($1sessionid=%{sessionid}$2)`.

O **RewriteCond** examina a variável sessionid `(%{sessionid})`. Se contiver pelo menos um caractere (.+), em seguida, a RewriteRule corresponde.

Assim, se o query de pesquisa for `"https://search.atomz.com/search/?sp_a=sp99999999&sp_q=word&sessionid=5678"`, todos os URLs de resultado de pesquisa serão regravados para que o valor &quot;sessionid&quot; seja &quot;5678&quot; em vez do valor &quot;sessionid&quot; encontrado pelo robô de pesquisa ao rastrear seu site e salvar os links.

**Reconhecimento**

O software do mecanismo de regravação foi desenvolvido originalmente pelo Apache Group para uso no projeto do servidor HTTP Apache (https://www.apache.org/).

## Adicionar regras de URL de pesquisa {#task_50C77D1B53804AEEB20896F74265BD6F}

Você pode adicionar regras de URL de pesquisa para especificar como os URLs nos resultados de pesquisa do site são exibidos. As regras operam em URLs completos. É possível manipular qualquer parte do URL, incluindo argumentos de query nos quais as informações de ID da sessão são mantidas com frequência.

<!-- 

t_adding_search_url_rules.xml

 -->

**Para adicionar regras de URL de pesquisa**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search URL Rules]**.
1. No campo [!DNL Search URL Rules], insira as regras desejadas.

   São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash).
1. (Opcional) Na página [!DNL Search URL Rules], no campo [!DNL Test Search URL Rules], digite um URL de teste cujas regras de rastreamento você deseja testar e clique em **Testar**.
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Search URL Rules], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre as Regras de Título de Pesquisa {#concept_C72D20F8DFF64EDE809AF4B72797E858}

As Regras de título de pesquisa especificam como os títulos em seus resultados de pesquisa do site são exibidos. Qualquer parte do título pode ser manipulada.

<!-- 

c_about_search_title_rules.xml

 -->

Uma regra de regravação pode ser usada para remover uma parte de um título, como um nome de organização, por exemplo. Por padrão, a pesquisa/comercialização do site não tem regras de título e não faz modificações de título.

As regras de título podem consistir em dois elementos principais: RewriteRule e RewriteCond opcionais. Pode ser especificado um número ilimitado de regras e condições. A ordem dessas regras é importante, pois o conjunto de regras é repetido por regra. Quando uma regra corresponde, o software executa o loop por qualquer condição de regravação (opcional) correspondente. As Regras de Título de Pesquisa são especificadas da seguinte maneira:

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Quando um título é encontrado, a pesquisa/comercialização do site tenta corresponder ao Padrão de cada regra de rastreamento. Se o padrão corresponder, o mecanismo de regravação procurará as diretivas RewriteCond correspondentes. Se nenhuma condição estiver presente, o título será substituído por um novo valor construído a partir da string Substituição e continuará com a próxima regra no conjunto de regras. Se houver condições, elas serão processadas na ordem em que estão listadas. O mecanismo de regravação tenta corresponder um padrão de condição (CondPattern) a uma string de teste (TestString). Se as duas corresponderem, a próxima condição será processada até que não haja mais condições disponíveis. Se todas as condições corresponderem, o URL será substituído pela Substituição especificada na regra. Se a condição não for atendida, o conjunto completo de condições e a regra correspondente falharão.

## Diretiva RewriteRule {#section_3BF2B0FF89F74A26AE79D68FA3184B9B}

Cada diretiva RewriteRule define uma regra de regravação. As regras são aplicadas na ordem em que estão listadas. Uma regra de regravação assume o seguinte formato:

```
RewriteRule Pattern Substitution [Flags]
```

**** PadrãoUma expressão regular POSIX, que é aplicada ao título atual. O &quot;título atual&quot; pode ser diferente do título original, pois as regras anteriores podem já ter correspondido e alterado.

Consulte [Expressões regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Você pode usar o caractere &quot;não&quot; (&#39;!&#39;) para prefixar o padrão. O caractere &quot;não&quot; permite negar um padrão. Ou seja, ser verdadeiro somente se o título atual NÃO corresponder ao padrão. O caractere &quot;não&quot; pode ser usado quando é melhor corresponder a um padrão negativo ou como uma regra padrão final. Observação: Não é possível usar o caractere &quot;não&quot; e curingas agrupadas em um padrão. Além disso, não é possível usar um padrão negado quando a string de substituição contém $N.

Você pode usar parênteses para criar uma referência retroativa, que pode ser referenciada pela Substituição e CondPattern.

**** SubstituiçãoO título é completamente substituído pela string de substituição, que pode conter o seguinte:

Texto sem formatação - texto que é transmitido sem alterações.

**** BackreferencesFornece acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Estes são dois tipos de referências retroativas:

* **RewriteRule** BackreferencesElas correspondem às referências anteriores no RewriteRule Pattern correspondente e assumem a forma $N (0  &lt;> Por exemplo, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* ** RewriteCond Backreferences** Essas referências retroativas correspondem na última RewriteCond Cond CondPattern correspondente e têm o formato %N (0 &lt;= N &lt;= 9).

**Variáveis** São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE pode ser uma string para o nome de uma variável definida. Consulte o sinalizador [E] para obter mais informações sobre como configurar variáveis de ambiente. As variáveis também podem ser definidas no formulário de pesquisa que gerou os resultados da pesquisa.

**** FunçõesEssas são funções do formulário ${NAME_OF_FUNCTION: key} onde NAME_OF_FUNCTION é:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.

Existe uma string de substituição especial: &quot;-&quot; significa &quot;substituição de NO&quot;. A sequência de caracteres &#39;-&#39; geralmente é útil em conjunto com o sinalizador C (cadeia), permitindo que você corresponda um título a vários padrões antes que ocorra uma substituição.

**Sinalizadores** (opcional)

Os sinalizadores estão entre colchetes `[]` e vários sinalizadores são separados por vírgulas:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p> Última regra. </p> <p> Pare o processo de regravação e não aplique regras adicionais de regravação. Use esse sinalizador para impedir qualquer processamento adicional no título atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Próxima rodada. </p> <p> Execute novamente o processo de regravação (começando pela primeira regra de regravação) usando o título da última regra de regravação (não o título original!). Tenha cuidado para não criar um ciclo sem saída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Encadeado com a próxima regra. </p> <p> Esse sinalizador encadea a regra atual à regra seguinte (que também pode ser encadeada à regra a seguir e assim por diante). Se uma regra corresponde, o processo de substituição continua como de costume. Se a regra não corresponder, todas as regras encadeadas subsequentes serão ignoradas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Nenhum caso. </p> <p> Este sinalizador faz com que o Padrão não diferencie maiúsculas de minúsculas. Ou seja, não há diferença entre 'A-Z' e 'a-z' quando o padrão é comparado ao título atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p> Ignorar a regra ou as regras seguintes. </p> <p> Se a regra atual corresponder, esse sinalizador forçará o mecanismo de regravação a ignorar as regras de próximo número no conjunto de regras. Use-o para criar construções pseudo if-then-else. A última regra da cláusula then torna-se um skip=N, onde N é o número de regras na cláusula else. (Não é o mesmo que o sinalizador 'chain|C'!) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Defina a variável ambiente. </p> <p> Este sinalizador cria uma variável ambiental "VAR" definida como valor VAL, onde VAL pode conter referências anteriores regulares do expressão, $N e %N, que serão expandidas. Você pode usar esse sinalizador mais de uma vez para definir várias variáveis. As variáveis podem ser referenciadas posteriormente em um padrão RewriteCond a seguir via %{VAR}. Use esse sinalizador para retirar e lembrar informações dos títulos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Diretiva RewriteCond (opcional) {#section_9D72B2AB454849A7B681BC39C506AAA3}

A diretiva RewriteCond define uma condição de regra. Quando um RewriteCond precede uma RewriteRule, a regra é usada somente se seu padrão corresponder ao título atual e se as condições adicionais se aplicarem.

As diretivas de condição de regravação assumem a seguinte forma:

```
RewriteCond TestString CondPattern [Flags]
```

**** TestStringis é uma string que pode conter as seguintes construções:

Texto sem formatação - texto que é transmitido sem alterações.

As referências retroativas fornecem acesso às partes agrupadas (entre parênteses) do Padrão ou CondPattern. Há dois tipos de referências retroativas:

* **RewriteRule** BackreferencesElas correspondem às referências anteriores no RewriteRule Pattern correspondente e assumem a forma $N (0  &lt;> Por exemplo, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RewriteCond** BackreferencesEssas backreferences correspondem no último RewriteCond Cond CondPattern correspondente e assumem o formato %N (0)  &lt;>

**Variáveis** São variáveis do formulário %{NAME_OF_VARIABLE} em que NAME_OF_VARIABLE pode ser uma string para o nome de uma variável definida. Consulte o sinalizador `[E]` para obter mais informações sobre como configurar variáveis de ambiente. As variáveis também podem ser definidas no formulário de pesquisa que gerou os resultados da pesquisa.

**** FunçõesEssas são funções do formulário ${NAME_OF_FUNCTION:key} onde NAME_OF_FUNCTION é:

* a opção torna todos os caracteres em *key* minúsculas.
* o toupper coloca todos os caracteres em *key* maiúsculo.
* O URL de escape codifica todos os caracteres em *key*.
* Os caracteres &#39;a&#39;.z&#39;, &#39;A&#39;..Z&#39;, &#39;0&#39;...9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; e &#39;_&#39; são deixados inalterados, os espaços são convertidos em &#39;+&#39; e todos os outros caracteres são transformados em seu equivalente codificado em URL %xx.
* unescape transforma &#39;+&#39; de volta ao espaço e todos os caracteres codificados por URL %xx de volta em caracteres únicos.

Existe uma string de substituição especial: &quot;-&quot; significa &quot;substituição de NO&quot;. A sequência de caracteres &#39;-&#39; geralmente é útil em conjunto com o sinalizador C (cadeia), permitindo que você corresponda um URL a vários padrões antes que ocorra uma substituição.

**** CondPatternUma Expressão regular estendida padrão com algumas adições. A string de padrão pode ser prefixada com um &#39;!&#39; (ponto de exclamação) para especificar um padrão não correspondente. Em vez de sequências de expressão regulares reais, você pode usar uma das seguintes variantes especiais.

Todos esses testes também podem ser prefixados por um ponto de exclamação (&#39;!&#39;) negar o seu significado.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sequência CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>É lexicamente menor. </p> <p> Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente menor que <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p> É lexicamente maior. </p> <p> Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente maior que <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>É lexicamente igual. </p> <p> Trata o <i>CondPattern</i> como uma cadeia de caracteres simples e o compara lexicamente a <i>TestString</i>. True se <i>TestString</i> for lexicamente igual a <i>CondPattern</i>. Ou seja, as duas strings são exatamente iguais (caractere por caractere). Se <i>CondPattern</i> for apenas "" (duas aspas), isso compara <i>TestString</i> à string vazia. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sinalizadores** (opcional)

Os sinalizadores estão entre colchetes`[]` e vários sinalizadores são separados por vírgulas:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sinalizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' (nenhum caso) </p> </td> 
   <td colname="col2"> <p>Torna o teste não sensível. Ou seja, não há diferença entre 'A-Z' e 'a-z' tanto no <i>TestString</i> expandido quanto no <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' (ou próxima condição) </p> </td> 
   <td colname="col2"> <p> Use-o para combinar condições de regras com um OU local em vez do E implícito. Sem esse sinalizador, você teria que escrever a segunda/regra várias vezes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section_E7454FFE169E459AABD9D033651939CB}

Suponha que você tenha um site corporativo com um formato de título padrão: &quot;Minha Empresa&quot; seguido por um hífen e, em seguida, uma descrição específica da página (&quot;Minha Empresa - Bem-vindo&quot; ou &quot;Minha Empresa - Notícias&quot;, por exemplo). Deseja retirar &quot;Minha Empresa -&quot; do título e converter o título inteiro em letras maiúsculas quando indexar o site.

A regra de regravação a seguir usa a função toupper para regravar somente a parte descritiva de um título para maiúsculas:

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>} 
```

O Padrão `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` da regra contém uma referência retroativa **`(.*)`** que corresponde ao conteúdo do título que segue &quot;Minha Empresa-&quot;. Lembre-se de que ao redor de uma parte de um padrão com parênteses ( ) cria uma referência retroativa que pode ser referenciada pela Substituição. Neste exemplo, a Substituição (${toupper:**$1**}) regrava aquela referência retroativa (**$1**) usando a função de toupper.

Assim, um título do formulário &quot;Minha Empresa - Bem-vindo&quot; é reescrito como &quot;BEM-VINDO&quot;.

**Reconhecimento**

O software do mecanismo de regravação foi desenvolvido originalmente pelo Apache Group para uso no projeto do servidor HTTP Apache (https://www.apache.org/).

## Adicionar regras de título de pesquisa {#task_155CECB74BE3444384EDBBD04F41515E}

Você pode adicionar regras de título de pesquisa para especificar como os títulos do site e os resultados de pesquisa são exibidos. É possível manipular qualquer parte do título.

<!-- 

t_adding_search_title_rules.xml

 -->

**Para adicionar regras de título de pesquisa**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search Title Rules]**.
1. No campo [!DNL Search Title Rules], insira as regras desejadas.

   São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash).
1. (Opcional) Na página [!DNL Search Title Rules], no campo [!DNL Test Search Title Rules], digite um título de teste e clique em **Teste**.
1. Clique em **Salvar alterações**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Search Title Rules], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

