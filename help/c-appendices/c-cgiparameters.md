---
description: Saiba mais sobre como usar vários parâmetros CGI.
solution: Target
title: Parâmetros CGI
topic-legacy: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
exl-id: 9f24aebf-5fa3-433e-b66d-4129bdd3f7f6
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1938'
ht-degree: 1%

---

# Parâmetros CGI{#cgi-parameters}

## Parâmetros CGI {#concept_F395999090FE4926B38BC73D5E612800}

## Pesquisar parâmetros CGI {#reference_DA27A8B0728246DA94994885E1353890}

O código do formulário de pesquisa é fornecido para que você possa copiar e colar no HTML do seu site ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**).

Consulte [Copiando o código HTML do formulário de pesquisa para o...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Também é possível definir os parâmetros listados no próprio formulário de pesquisa ou a partir de um script. Além dos parâmetros listados abaixo, você também pode usar os parâmetros de pesquisa de backend para controlar a pesquisa.

Consulte [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

As solicitações de pesquisa consistem em um URL básico. O URL base indica qual conta o cliente está pesquisando e um conjunto de parâmetros CGI (pares de valores chave) que indicam como retornar os resultados de pesquisa desejados para a conta associada.

O URL de base é associado a uma conta específica e a um ambiente temporário ou ao vivo. Você pode solicitar vários aliases para o URL básico de seu gerente de conta. Por exemplo, uma empresa chamada Megacorp pode ter dois URLs básicos associados à conta: `https://search.megacorp.com` e `https://stage.megacorp.com`. O URL anterior pesquisa seu índice ativo e o último URL pesquisa seu índice de preparo.

Há suporte para três formatos de Parâmetros CGI. Por padrão, sua conta é configurada para separar Parâmetros CGI com ponto-e-vírgula, como no exemplo a seguir:

`https://search.megacorp.com?q=shoes;page=2`

Se preferir, seu gerente de conta pode configurar sua conta para usar o &quot;E&quot; comercial para separar os parâmetros da CGI, como no exemplo a seguir:

`https://search.megacorp.com?q=shoes&page=2`

Um terceiro formato, chamado de formato SEO, também é suportado, onde uma barra `/` é usada no lugar do separador e sinal de igual como no exemplo a seguir:

`https://search.megacorp.com/q/shoes/page/2`

Sempre que o formato SEO for usado para enviar uma solicitação, todos os links de saída serão retornados no mesmo formato.

| Parâmetro de pesquisa guiada | Exemplo | Descrição |
|--- |--- |--- |
| q | `q=string` | Especifica a sequência de consulta para a pesquisa. Esse parâmetro mapeia para o parâmetro de pesquisa de backend `sp_q`.  Consulte [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| q# | `q#=string` | A faceta (pesquisa em um determinado campo) é feita por meio de parâmetros q e x numerados.  O parâmetro q define o termo que você está procurando na faceta, como denotado pelo parâmetro x numerado correspondente.<br>Por exemplo, se você tiver duas facetas nomeadas de tamanho e cor, poderá ter algo como q1=small;x1=size;q2=red;x2=color.  Esse parâmetro mapeia para os parâmetros de pesquisa de backend `sp_q_exact_#`.  <br>Consulte Parâmetros CGI  [da pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| x# | `q#=string` | A faceta (pesquisa em um determinado campo) é feita por meio de parâmetros q e x numerados.  O parâmetro q define o termo que você está procurando na faceta, como denotado pelo parâmetro x numerado correspondente. <br>Por exemplo, se você tiver duas facetas nomeadas de tamanho e cor, poderá ter algo como q1=small;x1=size;q2=red;x2=color.  Esse parâmetro mapeia para os parâmetros de pesquisa de backend `sp_x_#`.  <br>Consulte Parâmetros CGI  [da pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| coleção | `collection=string` | Especifica a coleção a ser usada para a pesquisa.  Esse parâmetro mapeia para o parâmetro de pesquisa de backend `sp_k`.  Consulte [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| count | `count=number` | Especifica a contagem total de resultados mostrados.  O padrão é definido em [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Esse parâmetro mapeia para o parâmetro de pesquisa de backend `sp_c`.  Consulte [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| página | `page=number` | Especifica a página de resultados que são retornados. |
| classificação | `rank=field` | Especifica o campo de classificação a ser usado para classificação estática.  O campo deve ser um campo do tipo Classificação com relevância maior que 0.  Esse parâmetro mapeia para o parâmetro de back-end `sp_sr`.  Consulte [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| sort | `sort=number` | Especifica a ordem de classificação.<br>&quot;0&quot; é o padrão e classifica por pontuação de relevância; &quot;1&quot; ordena por data; &quot;-1&quot; não classifica.  Os usuários podem especificar um nome de campo para o valor do parâmetro `sp_s` .  Por exemplo, `sp_s=title` classifica os resultados de acordo com os valores contidos no campo de título. Quando um nome de campo é usado para o valor de um parâmetro ` sp_s ` , os resultados são classificados por esse campo e depois subclassificados por relevância.  Para ativar este recurso, clique em [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. Na página Definições , clique em [!UICONTROL Add New Field ] ou em [!UICONTROL Edit ] para obter um nome de campo específico. Na lista suspensa [!UICONTROL Sorting ], selecione [!UICONTROL Ascending ] ou [!UICONTROL Descending ]. Esse parâmetro mapeia para o parâmetro de pesquisa de backend `sp_s`. <br>Consulte Parâmetros CGI  [da pesquisa de backend].(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## Parâmetros CGI de pesquisa de backend {#reference_582E85C3886740C98FE88CA9DF7918E8}

Normalmente, os clientes interagem com uma camada de apresentação chamada Pesquisa guiada. No entanto, é teoricamente possível ignorar a camada de Pesquisa guiada e interagir com a pesquisa principal de backend diretamente usando os parâmetros CGI descritos nesta página.

Você pode selecionar parâmetros CGI de pesquisa de backend na tabela a seguir:
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Suporte a query única </p> </th> 
   <th colname="col03" class="entry"> <p>Suporte a várias consultas </p> </th> 
   <th colname="col3" class="entry"> <p>Exemplos </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_a= string </code> </p> </td> 
   <td colname="col4"> <p>Especifica a string do número da conta. Esse parâmetro é necessário e deve ser uma string válida de número de conta. Você pode encontrar a string do número da conta em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Opções da conta </span> &gt; <span class="uicontrol"> Configurações da conta </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_advanced= 0 or 1 </code> </p> </td> 
   <td colname="col4"> <p>Se <code>sp_advanced=1 </code> for enviado com uma consulta, todo o código entre a tag <code>&lt;search-if-advanced&gt; </code> e a tag <code>&lt;/search-if-advanced&gt; </code> no modelo de pesquisa será usado para o formulário de pesquisa. Todos os códigos entre a tag <code>&lt;search-if-not-advanced&gt; </code> e a tag <code>&lt;/search-if-not-advanced&gt; </code> são ignorados. Se <code>sp_advanced=0 </code> (ou qualquer outro valor) for enviado, o bloco de modelo &lt;search-if-advanced&gt; será ignorado e o bloco de modelo &lt;search-if-not-advanced&gt; será usado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_c= number </code> </p> </td> 
   <td colname="col4"> <p>Especifica a contagem total de resultados a serem mostrados. O padrão é 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Coleta informações contextuais para o campo especificado. As informações coletadas são geradas nos resultados da pesquisa por meio da tag do modelo <code>&lt;search-context&gt; </code> . O valor padrão é <code>body </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_d= type </code> </p> </td> 
   <td colname="col4"> <p>Especifica o tipo de intervalo de datas que deve ser executado. Valores possíveis para o tipo são qualquer, o que significa que não executa pesquisa por intervalo de datas, personalizado, que indica que o valor de <code>sp_date_range </code> deve ser usado para determinar as datas para pesquisa, e específico, que indica que os valores em <code>sp_start_day </code>, <code>sp_start_month </code>, <code>sp_start_year </code>, <code>sp_end_day </code>, <code>sp_end_month </code> e <code>sp_end_year </code> são usados para determinar o intervalo de datas a ser pesquisado. <code>sp_d </code> só é necessário se o formulário de pesquisa contiver a opção de pesquisar por um intervalo personalizado (por meio de  <code>sp_date_range </code>) ou por um intervalo de datas inicial e final específico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <code>sp_d_#= type </code> </p> </td> 
   <td colname="col4"> <p>Especifica o tipo de pesquisa de intervalo de datas a ser executada para a consulta <code>sp_q_# </code> correspondente. O "#" é substituído por um número entre 1 e 16 (por exemplo, <code>sp_d_8 </code>, se aplica à consulta numerada <code>sp_q_8 </code>). </p> <p>Você pode definir <code>type </code> como qualquer, o que significa que não executa pesquisa por intervalo de datas, personalizado, o que indica que o valor de <code>sp_date_range_# </code> é usado para determinar as datas a serem pesquisadas, e específico, que indica que os valores em <code>sp_q_min_day_# </code>, <code>sp_q_min_month_# </code>, <code>sp_q_min_year_# </code>, <code>sp_q_max_day_# </code>, <code>sp_q_max_month_# </code> devem ser usados para determinar o intervalo de datas. <code>sp_q_max_year_# </code> O uso de <code>sp_d_# </code> só é necessário se o formulário de pesquisa contiver a opção para pesquisar por um intervalo personalizado (por meio de <code>sp_date_range_# </code>) ou por um intervalo de datas inicial e final específico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica um intervalo de datas predefinido a ser aplicado à pesquisa. Valores maiores ou iguais a zero especificam o número de dias para pesquisa antes de hoje — por exemplo, um valor "0" especifica "hoje", um valor "1" especifica "hoje e ontem", um valor "30" especifica "nos últimos 30 dias" e assim por diante. </p> <p>Os valores abaixo de zero especificam um intervalo personalizado da seguinte maneira: </p> <p>-1 = "Nenhum", o mesmo que especificar nenhum intervalo de datas. </p> <p>-2 = "Esta semana", que pesquisa de domingo a sábado da semana atual. </p> <p>-3 = "Última semana", que pesquisa de domingo a sábado da semana anterior à semana atual. </p> <p>-4 = "Este mês", que pesquisa datas dentro do mês atual. </p> <p>-5 = "Último mês", que pesquisa datas dentro do mês anterior ao mês atual. </p> <p>-6 = "Este ano", que pesquisa datas dentro do ano atual. </p> <p>-7 = "Ano passado", que pesquisa datas no ano anterior ao ano atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica um intervalo de datas predefinido a ser aplicado à consulta <code>sp_q_# </code> correspondente. O "#" é substituído por um número entre 1 e 16 (por exemplo, <code>sp_date_range_8 </code>, se aplica à consulta numerada <code>sp_q_8 </code>). </p> <p>Valores maiores ou iguais a zero especificam o número de dias para pesquisa antes de hoje. Por exemplo, um valor 0 especifica hoje; um valor de 1 especifica hoje e ontem; um valor de 30 especifica nos últimos 30 dias e assim por diante. </p> <p>Os valores abaixo de zero especificam um intervalo personalizado da seguinte maneira: </p> <p>-1 = "Nenhum", o mesmo que especificar nenhum intervalo de datas. </p> <p>-2 = "Esta semana", que pesquisa de domingo a sábado da semana atual. </p> <p>-3 = "Última semana", que pesquisa de domingo a sábado da semana anterior à semana atual. </p> <p>-4 = "Este mês", que pesquisa datas dentro do mês atual. </p> <p>-5 = "Último mês", que pesquisa datas dentro do mês anterior ao mês atual. </p> <p>-6 = "Este ano", que pesquisa datas dentro do ano atual. </p> <p>-7 = "Ano passado", que pesquisa datas no ano anterior ao ano atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica um único campo no qual os resultados da pesquisa serão deduplicados. Todos os resultados duplicados nesse campo são removidos dos resultados da pesquisa. Por exemplo, se para <code>sp_dedupe_field=title </code>, somente o resultado superior de um determinado título é exibido nos resultados da pesquisa (nenhum dos dois resultados terá conteúdo de campo de título idêntico). Para campos de tipo com vários valores (lista de permissões), todo o conteúdo do campo é usado para comparação. É possível especificar apenas um campo. Um "qualificador de tabela" não é permitido no nome do campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_e= number </code> </p> </td> 
   <td colname="col4"> <p>Especifica que a expansão automática de curinga deve ocorrer para qualquer palavra da string de consulta com mais de caracteres numéricos. Em outras palavras, <code>sp_e=5 </code> especifica que palavras com 5 ou mais caracteres, como "query" ou "número", devem ser expandidas com o caractere curinga '*', tornando a pesquisa equivalente a uma pesquisa por "query*" ou "número*". Palavras com menos caracteres não são expandidas, portanto, uma pesquisa por "palavra" não teria expansão automática de curinga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <code>sp_e_#= number </code> </p> </td> 
   <td colname="col4"> <p>Especifica que a expansão automática de curinga ocorre para qualquer palavra da sequência de consulta <code>sp_q_# </code> correspondente com mais de caracteres numéricos. Em outras palavras, <code>sp_e_2=5 </code> especifica que as palavras com cinco ou mais caracteres na sequência de consulta <code>sp_q_2 </code>, como "query" ou "número", devem ser expandidas com o caractere curinga ' <code>* </code>', tornando a pesquisa equivalente a uma pesquisa por "query*" ou "number*". Palavras com menos caracteres não são expandidas, portanto, uma pesquisa por "palavra" em <code>sp_q_2 </code> não teria expansão automática de curinga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Esse triplet de valores especifica o intervalo de datas final para a pesquisa e deve ser fornecido como um conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_f= string </code> </p> </td> 
   <td colname="col4"> <p>Especifica o conjunto de caracteres das sequências de parâmetro de consulta (como <code>sp_q </code>). Essa sequência sempre deve corresponder ao conjunto de caracteres da página que contém o formulário de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Define uma tabela de dados lógica que consiste em determinados campos. Por exemplo, uma tabela chamada "itens" que consiste nos campos "cor", "tamanho" e "preço" seria definida como a seguinte: </p> <p> <code>sp_field_table=items:color,size,price </code> </p> <p>As tabelas lógicas são mais úteis em conjunto com campos que têm "Listas de permissões" marcadas (em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>). Todos os parâmetros CGI e tags de modelo que assumem um nome de campo como valor podem especificar opcionalmente um nome de tabela seguido por um "." antes do nome do campo (por exemplo, <code>sp_x_1=tablename.fieldname </code>). </p> <p>Por exemplo, para realizar uma pesquisa por documentos que contenham um ou mais itens "vermelhos" de tamanho "grande" (onde os itens são representados como linhas paralelas de metadados), você pode usar o seguinte: </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p></td><td colname="col4"><p></p><p></p><p><code>sp_i=1 </code><code>sp_i=2 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_k= string </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_l= string </code></p></td><td colname="col4"><p><code>sp_q </code><code>string </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_literal= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_literal=1 </code></p><p><code>sp_literal=0 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_m= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_n= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_not_found_page= url </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p= any/all/phrase </code></p></td><td colname="col4"><p><code>any </code><code>all </code><code>phrase </code></p><p><code>phrase </code><code>all </code><code>sp_p </code></p><p></p><p></p><p><code>sp_p </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p_#= any/all/phrase </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>any </code><code>all </code><code>phrase </code></p><p><code>all </code><code>phrase </code><code>sp_p_# </code><code>any </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>exact </code><code>equivalent </code><code>compatible </code><code>sp_p </code><code>exact </code><code>sp_p </code><code>all </code><code>phrase </code><code>equivalent </code><code>sp_pt </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt_#= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>exact </code><code>equivalent </code><code>exact </code><code>compatible </code><code>sp_p_# </code><code>exact </code><code>sp_p_# </code><code>equivalent </code><code>sp_pt_# </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q= string </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_#= text </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_q_1 </code><code>sp_q_16 </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_day= integer value </code></p><p><code>sp_q_month= integer value </code></p><p><code>sp_q_year= integer value </code></p><p><code>sp_q_day_#= integer value </code></p><p><code>sp_q_month_#= integer value </code></p><p><code>sp_q_year_#= integer value </code></p></td><td colname="col4"><p><code>sp_q_day </code><code>sp_q_month </code><code>sp_q_year </code><code>sp_q </code></p><p><code># </code><code>sp_q_day_6 </code><code>sp_q_6 </code></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p><p><code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p></td><td colname="col4"><p><code>sp_q_location </code><code>sp_q_location_# </code><code># </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_max_relevant_distance= <i>value</i> </code></p><p><code> sp_q_max_relevant_distance_#= <i>value</i> </code></p></td><td colname="col4"><p><code>sp_q_max_relevant_distance </code><code>sp_q_max_relevant_distance_# </code><code># </code></p><p><code>sp_q_max_relevant_distance </code></p><p><code>sp_q_max_relevant_distance_# </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p><p></p></td><td colname="col03"><p></p><p></p></td><td colname="col3"><p><code> sp_q_min_day=<i>integer value</i> </code></p><p><code> sp_q_min_month=<i>integer value</i> </code></p><p><code> sp_q_min_year=<i>integer value</i> </code></p><p><code> sp_q_max_day=<i>integer value</i> </code></p><p><code> sp_q_max_month=<i>integer value</i> </code></p><p><code> sp_q_max_year=<i>integer value</i> </code></p><p><code> sp_q_min_day_#=<i>integer value</i> </code></p><p><code> sp_q_min_month_#=<i>integer value</i> </code></p><p><code> sp_q_min_year_#=<i>integer value</i> </code></p><p><code> sp_q_max_day_#=<i>integer value</i> </code></p><p><code> sp_q_max_month_#=<i>integer value</i> </code></p><p><code> sp_q_max_year_#=<i>integer value</i> </code></p></td><td colname="col4"><p><code>sp_q_min_day </code><code>sp_q_min_month </code><code>sp_q_min_year </code><code>sp_q_max_day </code><code>sp_q_max_month </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_day_6 </code><code>sp_q_6 </code></p><p></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_min= value </code></p><p><code>sp_q_max= value </code></p><p><code>sp_q_min_#= value </code></p><p><code>sp_q_max_#= value </code></p><p><code>sp_q_exact_#=value </code></p></td><td colname="col4"><p><code>sp_q_min </code><code>sp_q_max </code><code>sp_q_exact </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_8 </code><code>sp_q_8 </code></p><p><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code></p><p><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_nocp= 1 or 0 </code></p><p><code>sp_q_nocp_#= 1 or 0 </code></p></td><td colname="col4"><p><code>0 </code></p><p><code>1 </code></p><p><code>sp_q_nocp </code><code>sp_q </code><code># </code><code>sp_q_nocp_8 </code><code>sp_q_8 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_required= 1 or 0 or -1 </code></p><p><code>sp_q_required_#= 1 or 0 or -1 </code></p></td><td colname="col4"><p></p><p><code>sp_q_required </code><code>sp_q </code></p><p><code># </code><code>sp_q_required_8 </code><code>sp_q_8 </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_referrer= url </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>ro </code></p><p></p><p><code>sp_ro=body:10 </code></p><p></p><p><code>sp_ro=body:9|title:9 </code></p><p><p><code>sp_ro=title:10 </code><code>title </code><code>sp_ro </code><code>sp_ro </code></p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_s= number </code></p></td><td colname="col4"><p></p><p><code>sp_s </code><code>sp_s=title </code><code>sp_s </code></p><p></p><p><code>sp_s </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code></p><p><code>sp_field_table </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sr= field </code></p></td><td colname="col4"><p><code>sp_sr </code></p><p><code>sp_sr </code><code>&lt;input type="hidden" name="sp_sr" value=""&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sfvl_field= string </code></p></td><td colname="col4"><p><code>search-field-value-list</code></p><p><code>sp_sfvl_field </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>search-field-value-list </code></p><p><code>dynamic-facet-field-count </code><code>dynamic-facet-field-count </code></p><p><code>sp_sfvl_df_count </code><code>dynamic-facet-field-count </code><code>sp_sfvl_df_count </code><code>sp_sfvl_df_count </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p><p><code>sp_sfvl_df_count </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_count </code></p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_staged= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_staged=1 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_start_day= number </code></p><p><code>sp_start_month= number </code></p><p><code>sp_start_year= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_suggest_q= number </code></p></td><td colname="col4"><p><code>sp_suggest_q </code><code>sp_q[_#] </code></p><p><code>sp_suggest_q </code><code>sp_q </code></p><p><code>sp_suggest_q=1 </code><code>sp_q_1 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_t= string </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_trace= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_stage=1 </code></p><p></p><p><p></p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_w= <i>sound-alike-enable</i> </code></p><p><code> sp_w_control=<i>sound-alike-control</i> </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p><p></p><code>sp_w_control </code></p><p><code>sp_w_control=0 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control=1 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control </code><code>sp_w </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x= field </code></p></td><td colname="col4"><p><code>sp_q </code><code>sp_x </code></p><p></p><p><code>sp_x </code></p><p></p><p><code>sp_x=any </code><code>sp_x </code></p><p><code>sp_x </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x_#= field-name </code></p></td><td colname="col4"><p><code>sp_q_# </code><code> # </code><code>sp_x_8 </code></p><p><code>sp_x_# </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code></p><p><code>sp_x </code><code>sp_x_# </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code></p></td></tr></tbody></table>

## Um exemplo típico de uso de parâmetros CGI de pesquisa de backend {#section_260012BBC2514CC9A8E02E53DE8B41EE}

As seguintes consultas de link iniciam uma pesquisa usando &quot;Música&quot; como consulta de pesquisa e usam todos os parâmetros padrão. Observe que o URL é dividido entre duas linhas para facilitar a leitura. No seu HTML, esse link deve estar em uma linha.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

A mesma funcionalidade geralmente é definida com um formulário:

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

Normalmente, você deve usar parâmetros padrão ao iniciar uma pesquisa. Dessa forma, a primeira página é mostrada, classificada por relevância, e permite que o cliente escolha outras páginas e outras opções. Se o formulário de pesquisa do site incluir opções para coleções, passe o nome da coleção como parâmetro.

## Um exemplo detalhado do uso de parâmetros CGI de pesquisa de backend {#section_5FA3C620D5124FB2AB28857F8D8473F6}

As consultas de formulário a seguir exibem `25` resultados iniciando em result `10`. Os resumos não são mostrados, a ordem de classificação é por data e a coleção chamada `support` é usada. Somente os documentos datados dos últimos 30 dias são retornados.

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
<input type=hidden name=sp_n value=10> 
<input type=hidden name=sp_c value=25> 
<input type=hidden name=sp_m value=0> 
<input type=hidden name=sp_s value=1> 
<input type=hidden name=sp_k value="support"> 
<input type=hidden name=sp_date_range value=30> 
</form>
```
