---
description: 'null'
seo-description: 'null'
seo-title: Parâmetros CGI
solution: Target
title: Parâmetros CGI
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '5490'
ht-degree: 1%

---


# Parâmetros CGI{#cgi-parameters}

## Parâmetros CGI {#concept_F395999090FE4926B38BC73D5E612800}

## Pesquisar parâmetros CGI {#reference_DA27A8B0728246DA94994885E1353890}

O código do formulário de pesquisa é fornecido para que você possa copiar e colar no HTML do seu site ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**).

Consulte [Copiando o código HTML do formulário de pesquisa no...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Também é possível definir os parâmetros listados no próprio formulário de pesquisa ou em um script. Além dos parâmetros listados abaixo, também é possível usar os parâmetros de pesquisa de backend para controlar a pesquisa.

Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend.

As solicitações de pesquisa consistem em um URL base. O URL básico indica que conta o cliente está pesquisando e um conjunto de parâmetros CGI (pares de valores chave) que indicam como retornar os resultados de pesquisa desejados para a conta associada.

O URL de base está associado a uma conta específica e a um ambiente em tempo real ou temporário. Você pode solicitar vários aliases para o URL básico do seu gerente de conta. Por exemplo, uma empresa chamada Megacorp pode ter dois URLs básicos associados à conta: `https://search.megacorp.com` e `https://stage.megacorp.com`. O URL anterior pesquisa seu índice ativo e o último URL pesquisa seu índice de preparo.

Há suporte para três formatos de Parâmetros CGI. Por padrão, sua conta é configurada para separar Parâmetros CGI com ponto-e-vírgula, como no exemplo a seguir:

`https://search.megacorp.com?q=shoes;page=2`

Se preferir, você pode fazer com que seu gerente de conta configure sua conta para usar e comercial para separar os parâmetros CGI, como no exemplo a seguir:

`https://search.megacorp.com?q=shoes&page=2`

Um terceiro formato, chamado de formato SEO, também é suportado quando uma barra `/` é usada no lugar do separador e sinal de igual como no exemplo a seguir:

`https://search.megacorp.com/q/shoes/page/2`

Sempre que o formato SEO for usado para enviar uma solicitação, todos os links de saída serão retornados no mesmo formato.

| Parâmetro Pesquisa guiada | Exemplo | Descrição |
|--- |--- |--- |
| q | `q=string` | Especifica a string de query para a pesquisa. Esse parâmetro mapeia para o parâmetro de pesquisa de `sp_q` backend.  Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend. |
| q# | `q#=string` | A facetagem (pesquisa em um determinado campo) é feita por meio de parâmetros q e x numerados.  O parâmetro q define o termo que você está procurando na faceta, como denotado pelo parâmetro x numerado correspondente.<br>Por exemplo, se você tiver duas facetas nomeadas tamanho e cor, poderá ter algo como q1=small;x1=size;q2=red;x2=color.  Esse parâmetro mapeia para os parâmetros de pesquisa de `sp_q_exact_#` backend.  <br>Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend. |
| x# | `q#=string` | A facetagem (pesquisa em um determinado campo) é feita por meio de parâmetros q e x numerados.  O parâmetro q define o termo que você está procurando na faceta, como denotado pelo parâmetro x numerado correspondente. <br>Por exemplo, se você tiver duas facetas nomeadas tamanho e cor, poderá ter algo como q1=small;x1=size;q2=red;x2=color.  Esse parâmetro mapeia para os parâmetros de pesquisa de `sp_x_#` backend.  <br>Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend. |
| coleção | `collection=string` | Especifica a coleção a ser usada para a pesquisa.  Esse parâmetro mapeia para o parâmetro de pesquisa de `sp_k` backend.  Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend. |
| count | `count=number` | Especifica a contagem total de resultados que são mostrados.  O padrão é definido em [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Esse parâmetro mapeia para o parâmetro de pesquisa de `sp_c` backend.  Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend. |
| página | `page=number` | Especifica a página de resultados que são retornados. |
| classificação | `rank=field` | Especifica o campo de classificação a ser usado para classificação estática.  O campo deve ser do tipo Classificação com relevância maior que 0.  Esse parâmetro mapeia para o parâmetro `sp_sr` backend.  Consulte Parâmetros [CGI de pesquisa de](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend. |
| espécie | `sort=number` | Especifica a ordem de classificação.<br>&quot;0&quot; é o padrão e classifica por pontuação de relevância; &quot;1&quot; ordena por data; &quot;-1&quot; não classifica.  Os usuários podem especificar um nome de campo para o valor do `sp_s` parâmetro.  Por exemplo, `sp_s=title` classifica os resultados de acordo com os valores contidos no campo de título. Quando um nome de campo é usado para o valor de um ` sp_s ` parâmetro, os resultados são classificados por esse campo e, em seguida, subclassificados por relevância.  To enable this feature, click [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. Na página Definições, clique [!UICONTROL Add New Field ] ou clique [!UICONTROL Edit ] para obter um nome de campo específico. Na lista [!UICONTROL Sorting ] suspensa, selecione [!UICONTROL Ascending ] ou [!UICONTROL Descending ]. Esse parâmetro mapeia para o parâmetro de pesquisa de `sp_s` backend. <br>Consulte Parâmetros [CGI de pesquisa de]backend.(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## Parâmetros CGI de pesquisa de backend {#reference_582E85C3886740C98FE88CA9DF7918E8}

Normalmente, os clientes interagem com uma camada de apresentação chamada Pesquisa guiada. No entanto, é teoricamente possível ignorar a camada de Pesquisa guiada e interagir com a pesquisa principal de backend diretamente usando os parâmetros CGI descritos nesta página.

Você pode selecionar parâmetros CGI de pesquisa de backend na seguinte tabela:
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Suporte a query único </p> </th> 
   <th colname="col03" class="entry"> <p>Suporte a vários query </p> </th> 
   <th colname="col3" class="entry"> <p>Exemplos </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_a= string </span> </p> </td> 
   <td colname="col4"> <p>Especifica a string do número da conta. Esse parâmetro é obrigatório e deve ser uma string válida de número de conta. Você pode encontrar sua string de número de conta em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Opções de conta </span> &gt; <span class="uicontrol"> Configurações da conta </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p>Se <span class="codeph"> sp_advanced=1 </span> for enviado com um query, então todos os códigos entre a tag <span class="codeph"> &lt;search-if-advanced&gt; </span> e a tag <span class="codeph"> &lt;/search-if-advanced&gt; </span> no modelo de pesquisa serão usados para o formulário de pesquisa. Todo o código entre a tag <span class="codeph"> &lt;search-if-not-advanced&gt; </span> e a tag <span class="codeph"> &lt;/search-if-not-advanced&gt; </span> é ignorado. Se <span class="codeph"> sp_advanced=0 </span> (ou qualquer outro valor) for submetido, o bloco de modelo &lt;search-if-advanced&gt; será ignorado e o bloco de modelo &lt;search-if-not-advanced&gt; será usado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica a contagem total de resultados a serem exibidos. O padrão é 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Coleta informações contextuais para o campo em questão. As informações coletadas são geradas nos resultados da pesquisa por meio da tag de modelo <span class="codeph"> &lt;search-context&gt; </span> . O valor padrão é <span class="codeph">body </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d= tipo </span> </p> </td> 
   <td colname="col4"> <p>Especifica o tipo de pesquisa do intervalo de datas a ser executado. Os valores possíveis para o tipo são quaisquer, o que significa que não realiza a pesquisa por intervalo de datas, personalizado, que indica que o valor de <span class="codeph"> sp_date_range </span> deve ser usado para determinar as datas de pesquisa, e específico, que indica que os valores em <span class="codeph"> sp_start_day </span>, <span class="codeph"> sp_start_month, </span>_start_year <span class="codeph"> , </span>sp_end_day <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> __end é usado para determinar o intervalo de datas a ser pesquisado. <span class="codeph"> sp_d </span> é necessário somente se o formulário de pesquisa contiver a opção de pesquisar por um intervalo personalizado (por meio de <span class="codeph"> sp_date_range </span>) ou por um start específico e um intervalo de datas final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#= type </span> </p> </td> 
   <td colname="col4"> <p>Especifica o tipo de pesquisa do intervalo de datas a ser executado para o query <span class="codeph"> sp_q_# </span> correspondente. O "#" é substituído por um número entre 1 e 16 (por exemplo, <span class="codeph"> sp_d_8 </span>, se aplica ao query numerado <span class="codeph"> sp_q_8 </span>). </p> <p>Você pode definir o <span class="codeph"> tipo </span> como qualquer um, o que significa não executar pesquisa no intervalo de datas, personalizado, que indica que o valor de <span class="codeph"> _date_range_# </span> é usado para determinar as datas de pesquisa, e específico, que indica que os valores em <span class="codeph"> sp_q_min_day_# </span>, <span class="codeph"> _q_month_# </span>, <span class="codeph"> _q_year_# </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> , sp_q_max_day_# , sp_q_max_month_#, e sp_q_max_year_# devem ser usadas para determinar o intervalo de datas. O uso de <span class="codeph"> sp_d_# </span> só é necessário se o formulário de pesquisa contiver a opção de pesquisar por um intervalo personalizado (por meio de <span class="codeph"> sp_date_range_# </span>) ou por um start específico e um intervalo de datas final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica um intervalo de datas predefinido a ser aplicado à pesquisa. Valores maiores ou iguais a zero especificam o número de dias para pesquisar antes de hoje — por exemplo, um valor de "0" especifica "hoje", um valor de "1" especifica "hoje e ontem", um valor de "30" especifica "nos últimos 30 dias" e assim por diante. </p> <p>Valores abaixo de zero especificam um intervalo personalizado da seguinte maneira: </p> <p>-1 = "Nenhum", o mesmo que não especificar um intervalo de datas. </p> <p>-2 = "Esta semana", que pesquisa de domingo a sábado da semana atual. </p> <p>-3 = "Última semana", que pesquisa de domingo a sábado da semana anterior à semana atual. </p> <p>-4 = "Este mês", que pesquisa datas dentro do mês atual. </p> <p>-5 = "Último mês", que pesquisa datas dentro do mês anterior ao mês atual. </p> <p>-6 = "Este ano", que pesquisa datas dentro do ano atual. </p> <p>-7 = "Ano passado", que pesquisa datas no ano anterior ao ano atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica um intervalo de datas predefinido a ser aplicado ao query <span class="codeph"> sp_q_# </span> correspondente. O "#" é substituído por um número entre 1 e 16 (por exemplo, <span class="codeph"> sp_date_range_8 </span>, se aplica ao query numerado <span class="codeph"> sp_q_8 </span>). </p> <p>Valores maiores ou iguais a zero especificam o número de dias para pesquisar antes de hoje. Por exemplo, um valor de 0 especifica hoje; um valor de 1 especifica hoje e ontem; um valor de 30 especifica nos últimos 30 dias e assim por diante. </p> <p>Valores abaixo de zero especificam um intervalo personalizado da seguinte maneira: </p> <p>-1 = "Nenhum", o mesmo que não especificar um intervalo de datas. </p> <p>-2 = "Esta semana", que pesquisa de domingo a sábado da semana atual. </p> <p>-3 = "Última semana", que pesquisa de domingo a sábado da semana anterior à semana atual. </p> <p>-4 = "Este mês", que pesquisa datas dentro do mês atual. </p> <p>-5 = "Último mês", que pesquisa datas dentro do mês anterior ao mês atual. </p> <p>-6 = "Este ano", que pesquisa datas dentro do ano atual. </p> <p>-7 = "Ano passado", que pesquisa datas no ano anterior ao ano atual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica um único campo no qual os resultados da pesquisa serão removidos. Todos os resultados do duplicado nesse campo são removidos dos resultados da pesquisa. Por exemplo, se para <span class="codeph"> sp_dedupe_field=title </span>, somente o resultado superior de um determinado título é exibido nos resultados da pesquisa (nenhum dos dois resultados terá conteúdo de campo de título idêntico). Para campos do tipo de vários valores (lista de permissões), todo o conteúdo do campo é usado para comparação. Somente um campo pode ser especificado. Um "qualificador de tabela" não é permitido no nome do campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica que a expansão automática de caracteres curinga deve ocorrer para qualquer palavra da string de query com mais de caracteres numéricos. Em outras palavras, <span class="codeph"> sp_e=5 </span> especifica que palavras com 5 ou mais caracteres, como "query" ou "número", devem ser expandidas com o caractere curinga '*', tornando a pesquisa equivalente a uma pesquisa por "query*" ou "número*". Palavras com menos caracteres não são expandidas, portanto, uma pesquisa por "palavra" não teria expansão automática de caracteres curinga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica que a expansão automática de caracteres curinga ocorre para qualquer palavra da string de query <span class="codeph"> </span> sp_q_# com mais de caracteres numéricos. Em outras palavras, <span class="codeph"> sp_e_2=5 </span> especifica que palavras com cinco ou mais caracteres na sequência de caracteres do <span class="codeph"> query </span> sp_q_2, como "query" ou "número", devem ser expandidas com o caractere curinga ' <span class="codeph"> * </span>', tornando a pesquisa equivalente a uma pesquisa por "query*" ou "número*". Palavras com menos caracteres não são expandidas, portanto, uma pesquisa por "palavra" em <span class="codeph"> sp_q_2 não </span> teria expansão automática de caracteres curinga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Esse triplo de valores especifica o intervalo de datas final para a pesquisa e deve ser fornecido como um conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_f= string </span> </p> </td> 
   <td colname="col4"> <p>Especifica o conjunto de caracteres das strings de parâmetro de query (como <span class="codeph"> sp_q </span>). Essa string deve sempre corresponder ao conjunto de caracteres da página que contém o formulário de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Define uma tabela de dados lógica que consiste nos campos especificados. Por exemplo, uma tabela chamada "itens" que consiste nos campos "cor", "tamanho" e "preço" seria definida como: </p> <p> <span class="codeph"> sp_field_table=items:color,size,price </span> </p> <p>Tabelas lógicas são mais úteis em conjunto com campos que têm "Lista de permissões" marcado (em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>). Todos os parâmetros CGI e tags de modelo que usam um nome de campo como um valor podem, opcionalmente, especificar um nome de tabela seguido por um "". antes do nome do campo (por exemplo, <span class="codeph"> sp_x_1=tablename.fieldname </span>). </p> <p>Por exemplo, para realizar uma pesquisa por documentos que contenham um ou mais itens "vermelhos" de tamanho "grande" (onde os itens são representados como linhas paralelas de metadados), você pode usar o seguinte: </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> valor </span> </span> </p> </td> 
   <td colname="col4"> <p>Ignora a pesquisa quando você gera relatórios. </p> <p>Use esse query para mascarar determinadas pesquisas de backend, como pesquisas que Você quis dizer geram, ou pesquisas que um Administrador gera no centro membro. Como um usuário final não gera esses tipos de pesquisa, eles não são exibidos em vários relatórios de Search &amp; Promote de Adobe. </p> <p>Os valores válidos são <span class="codeph"> sp_i=1 </span> e <span class="codeph"> sp_i=2 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k= string </span> </p> </td> 
   <td colname="col4"> <p> Especifica a coleção a ser usada para a pesquisa. O padrão é nenhuma coleção, o que significa que a pesquisa deve incluir o site inteiro. </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> Uso de coleções em formulários de pesquisa </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l= string </span> </p> </td> 
   <td colname="col4"> <p>Especifica o idioma das strings de parâmetro do query (como <span class="codeph"> sp_q </span>). A <i> sequência de caracteres <span class="codeph"> </span></i> deve ser uma ID de localidade padrão contendo um código de idioma ISO-639 seguido opcionalmente por um código de país ISO-3166. Por exemplo, "en" ou "en_US" para inglês ou "ja" ou "ja_JP" para japonês. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_literal </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p> A configuração <span class="codeph"> sp_literal=1 desativa </span> temporariamente todos os recursos que podem interpretar as palavras no query. Com esse parâmetro, somente as palavras literais do query correspondem a documentos, independentemente de sinônimos, formas de palavras alternativas e correspondência de som. </p> <p>Observe que <span class="codeph"> sp_literal=0 não </span> tem significado e é ignorado se for usado. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> Sobre dicionários </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m= número </span> </p> </td> 
   <td colname="col4"> <p> Especifica se os resumos são exibidos. 1 é sim, 0 é não. O padrão é 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>20 </p> </td> 
   <td colname="col2"> <p>sp_n </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_n= número </span> </p> </td> 
   <td colname="col4"> <p> Especifica o número do resultado que start os resultados da pesquisa. O padrão é 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 </p> </td> 
   <td colname="col2"> <p>sp_not_found_page </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_not_found_page= url </span> </p> </td> 
   <td colname="col4"> <p> Especifica se é necessário redirecionar para o URL especificado se não houver resultados de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 </p> </td> 
   <td colname="col2"> <p>sp_p </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p= any/all/frase </span> </p> </td> 
   <td colname="col4"> <p> Especifica o tipo padrão de pesquisa a ser executado. O uso de <span class="codeph"> qualquer meio </span> significa pesquisar documentos que contenham qualquer palavra da string do query. O uso de <span class="codeph"> todos </span> significa pesquisar documentos que contenham todas as palavras na string do query. O uso de <span class="codeph"> frase </span> significa que a string de query é tratada como se fosse uma frase citada e todas as aspas digitadas pelo usuário são ignoradas. </p> <p>Para <span class="codeph"> frase </span> e <span class="codeph"> todos </span>, a especificação de "+" e "-" antes das palavras de pesquisa é desativada e esses caracteres são ignorados. Se <span class="codeph"> sp_p </span> não estiver presente, ou se estiver definida como uma string vazia ou qualquer outra, os prefixos de palavras "+" e "-" padrão são permitidos. </p> <p>Consulte a descrição das Dicas de pesquisa para obter mais informações sobre como usar mais ("+") e menos ("-") em pesquisas. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Sobre pesquisadores </a>. </p> <p>Consulte o formulário de pesquisa avançada de exemplo para obter exemplos sobre como usar o parâmetro <span class="codeph"> sp_p </span> . </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Amostra de formulário de pesquisa avançada </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#= any/all/frase </span> </p> </td> 
   <td colname="col4"> <p>Especifica o tipo padrão de pesquisa a ser realizada com o query <span class="codeph"> sp_q_# </span> correspondente. O "#" é substituído por um número entre 1 e 16 (por exemplo, <span class="codeph"> sp_p_8 </span> se aplica ao query numerado <span class="codeph"> sp_q_8 </span>). O uso de <span class="codeph"> qualquer meio </span> retorna documentos que contenham qualquer palavra da string do query. O uso de <span class="codeph"> todos </span> significa documentos de retorno que contêm todas as palavras na string do query. O uso de <span class="codeph"> frase </span> significa tratar a string do query como se fosse uma frase completa (e todas as aspas digitadas pelo usuário são ignoradas). </p> <p>Se você especificar <span class="codeph"> todas as palavras </span> ou <span class="codeph"> frases </span>, todos os sinais de mais e menos antes das palavras de pesquisa serão ignorados. Se <span class="codeph"> sp_p_# </span> for omitido, ou se estiver definido como uma string vazia ou <span class="codeph"> qualquer prefixo </span>, são permitidos os prefixos "+" e "-" padrão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> Especifica o tipo de correspondência de público alvo a ser aplicado. O uso do <span class="codeph"> exato </span> significa que o público alvo de rendimento corresponde somente a documentos que correspondem exatamente à sequência do query no conteúdo do público alvo. O uso do <span class="codeph"> equivalente </span> é exatamente igual, exceto que a ordem das palavras não é importante. O uso de <span class="codeph"> compatível define </span> automaticamente o tipo de correspondência de público alvo com base no valor do parâmetro <span class="codeph"> sp_p </span> . O uso de <span class="codeph"> exato </span> é usado se <span class="codeph"> sp_p </span> for tudo <span class="codeph"> ou </span> frase <span class="codeph"> , caso contrário </span>é usado o equivalente <span class="codeph"> </span> . O valor padrão de <span class="codeph"> sp_pt </span> é <span class="codeph"> compatível </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica o tipo de correspondência de público alvo a ser aplicado com o query <span class="codeph"> sp_q_# </span> correspondente. O "#" é substituído por um número entre 1 e 16 (por exemplo, <span class="codeph"> sp_p_8 </span> se aplica ao query numerado <span class="codeph"> sp_q_8 </span>). O uso do <span class="codeph"> exato </span> significa que o público alvo de rendimento corresponde somente a documentos que correspondem exatamente à sequência do query no conteúdo do público alvo. O uso do <span class="codeph"> equivalente </span> é como <span class="codeph"> exato </span>, exceto que a ordem das palavras não é importante. O uso de <span class="codeph"> compatível define </span> automaticamente o tipo de correspondência de público alvo com base no valor do parâmetro <span class="codeph"> sp_p_# </span> correspondente: <span class="codeph"> o exato </span> é usado se <span class="codeph"> sp_p_# </span> for tudo ou frase, caso contrário, é <span class="codeph"> usado o equivalente </span> . O valor padrão de <span class="codeph"> sp_pt_# </span> é <span class="codeph"> compatível </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>26 </p> </td> 
   <td colname="col2"> <p>sp_q </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q= string </span> </p> </td> 
   <td colname="col4"> <p> Especifica a string de query para a pesquisa. Uma string vazia leva a que nenhum resultado seja exibido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>27 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_q_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_#= texto </span> </p> </td> 
   <td colname="col4"> <p>Esse parâmetro permite a criação de vários query em formulários de pesquisa. O parâmetro <span class="codeph"> sp_q_# </span> contém a string de query a ser usada no query numerado especificado. Uma solicitação de pesquisa pode fazer referência a até 16 query numerados diferentes ( <span class="codeph"> sp_q_1 </span> a <span class="codeph"> sp_q_16 </span>). </p> <p>Por exemplo, o envio do formulário a seguir retorna todos os documentos que contêm as palavras "ótimo" e "livros". </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day, sp_q_month, sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q _day_#, sp_q _month_#, sp_q _year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day= valor inteiro </span> </p> <p> <span class="codeph"> sp_q_month= valor inteiro </span> </p> <p> <span class="codeph"> sp_q_year= valor inteiro </span> </p> <p> <span class="codeph"> sp_q_day_#= valor inteiro </span> </p> <p> <span class="codeph"> sp_q_month_#= valor inteiro </span> </p> <p> <span class="codeph"> sp_q_year_#= valor inteiro </span> </p> </td> 
   <td colname="col4"> <p>Esses parâmetros são usados para especificar uma data exata para um query específico. Os parâmetros <span class="codeph"> sp_q_day </span>, <span class="codeph"> sp_q_month </span>e <span class="codeph"> sp_q_year </span> se aplicam ao query principal ( <span class="codeph"> sp_q </span>). </p> <p>O <span class="codeph"> # </span>parâmetro é substituído por um número entre 1 e 16 (por exemplo, <span class="codeph"> sp_q_day_6 </span>, que se aplica ao query numerado <span class="codeph"> sp_q_6 </span>). Por padrão, todas as datas são pesquisadas em relação ao Tempo médio de Greenwich. </p> <p>A seguinte seção do código permite que um usuário procure a palavra "laranja" em documentos com data de "Jan. 1º, 2000" em um campo definido pelo usuário chamado <span class="codeph"> PublicarData </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>Esses parâmetros associam um local ao query principal ou numerado. O uso de <span class="codeph"> sp_q_location </span> afeta o query principal, <span class="codeph"> sp_q_location_# </span> (onde <span class="codeph"> # </span> é substituído por um número de 1 a 16), afeta o query numerado especificado. Esses parâmetros são usados para realizar pesquisas de proximidade de distância mínima e/ou máxima em relação aos dados de localização indexados para cada página do site. O formato do valor determina sua interpretação. </p> <p>Um valor na forma DDD (três dígitos) é interpretado como uma área telefônica dos EUA; um valor na forma DDDDD ou DDDDD-DDDD é interpretado como um código postal dos EUA; e um valor na forma ±DD.DDDD±DDD.DDDD é interpretado como um par de latitude/longitude. Os sinais são necessários para cada valor. Por exemplo, +38.6317+120.5509 especifica latitude 38.6317, longitude 120.5509. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Sobre pesquisa de proximidade </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_relevant_distance </p> </td> 
   <td colname="col03"> <p>sp_q_max _relevant _distance _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>Esses parâmetros controlam o cálculo de relevância aplicado às pesquisas de proximidade. O uso de <span class="codeph"> sp_q_max_relevant_distance </span> afeta o query principal, <span class="codeph"> sp_q_max_relevant_distance_# </span> (onde o <span class="codeph"> # </span> é substituído por um número de 1 a 16), afeta o query numerado especificado. </p> <p>O valor padrão de <span class="codeph"> sp_q_max_relevant_distance </span> é 100. </p> <p>Uma pontuação de relevância perfeita para o componente de proximidade representaria uma distância de 0. Uma pontuação de relevância mínima para o componente de proximidade representaria uma distância bem acima do valor <span class="codeph"> </span> sp_q_max_relevant_distance_# especificado. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Sobre pesquisa de proximidade </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day, sp_q_min_month, sp_q_min_year </p> <p>sp_q_max_day, sp_q_max_month, sp_q_max_year </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#, sp_q_min_month_#, sp_q_min_year_# </p> <p> sp_q_max_day_#, sp_q_max_month_#, sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>Esses parâmetros são usados para definir intervalos de datas mínimos e máximos para um determinado query. Os parâmetros <span class="codeph"> sp_q_min_day </span>, <span class="codeph"> sp_q_min_month </span>, <span class="codeph"> sp_q_min_year </span>, <span class="codeph"> sp_q_max_day </span>, <span class="codeph"> sp_q_max_month </span><i></i> <span class="codeph"> </span>e sp_q_max_yearaplicam-se ao query principal ( _q). </p> <p>O <span class="codeph"> # </span>no nome do parâmetro é substituído por um número entre 1 e 16 (por exemplo, <span class="codeph"> sp_q_min_day_6 </span> se aplica ao query numerado <span class="codeph"> sp_q_6 </span>). </p> <p>É legal especificar apenas uma data mínima, apenas uma data máxima ou ambas as datas mínima e máxima. No entanto, para um determinado conjunto mínimo ou máximo, todos os três parâmetros de data devem ser especificados (dia, mês e ano). Por padrão, todas as datas são pesquisadas em relação ao Tempo médio de Greenwich. </p> <p>A seguinte seção do código permite que um usuário pesquise a palavra "laranja" em documentos com uma data entre 1º de janeiro de 2000 e 31 de dezembro de 2000 em um campo definido pelo usuário chamado <span class="codeph"> Data de publicação </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>32 </p> </td> 
   <td colname="col2"> <p>sp_q_min, sp_q_max </p> </td> 
   <td colname="col03"> <p>sp_q _min_#, sp_q _max_#, sp_q _exato_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_min= valor </span> </p> <p> <span class="codeph"> sp_q_max= valor </span> </p> <p> <span class="codeph"> sp_q_min_#= valor </span> </p> <p> <span class="codeph"> sp_q_max_#= valor </span> </p> <p> <span class="codeph"> sp_q_exato_#=value </span> </p> </td> 
   <td colname="col4"> <p>Esses parâmetros especificam um valor mínimo (e/ou máximo) a ser aplicado ao query principal ou numerado. O uso de <span class="codeph"> sp_q_min </span>, <span class="codeph"> sp_q_max </span>e <span class="codeph"> sp_q_exato </span> afeta o query principal ( <span class="codeph"> sp_q </span>). </p> <p>Substitua <span class="codeph"> # </span>no nome do parâmetro por um número entre 1 e 16 (por exemplo, <span class="codeph"> sp_q_min_8 </span> se aplica ao query numerado <span class="codeph"> sp_q_8 </span>). </p> <p>O uso de <span class="codeph"> sp_q_exato_# </span> é abreviado para especificar <span class="codeph"> sp_q_min_# </span> e <span class="codeph"> sp_q_max_# </span> com o mesmo valor. Se <span class="codeph"> sp_q_exato_# </span> for especificado, quaisquer parâmetros <span class="codeph"> sp_q_min_# </span> ou <span class="codeph"> sp_q_max_# </span> correspondentes serão ignorados. </p> <p>Os parâmetros <span class="codeph"> sp_q_min_# </span>, <span class="codeph"> sp_q_max_# </span> e <span class="codeph"> sp_q_exato_# </span> podem, opcionalmente, especificar vários valores separados "|". Por exemplo, para procurar documentos que contenham o valor verde ou vermelho no campo "color": <span class="codeph"> ...&amp;sp_q_exatas_1=green|red&amp;sp_x_1=color </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q_nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1 ou 0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1 ou 0 </span> </p> </td> 
   <td colname="col4"> <p>O valor padrão do parâmetro é <span class="codeph"> 0, </span> o que significa que as expansões de Frase Comum são executadas. </p> <p>Quando definido como <span class="codeph"> 1 </span> para o query de pesquisa correspondente, as expansões de Frases comuns não são executadas. </p> <p>O uso de <span class="codeph"> sp_q_nocp </span> afeta o parâmetro principal do query de pesquisa <span class="codeph"> sp_q </span>. Para aplicar esse parâmetro a um query de pesquisa numerado, substitua <span class="codeph"> # </span> no nome do parâmetro pelo número correspondente. Por exemplo, <span class="codeph"> sp_q_nocp_8 </span> se aplica ao query de pesquisa numerado <span class="codeph"> sp_q_8 </span>. </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q _obrigatório _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1 ou 0 ou -1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1 ou 0 ou -1 </span> </p> </td> 
   <td colname="col4"> <p>Esse parâmetro determina se uma correspondência deve (1), pode (0) ou não deve ocorrer (-1) no query correspondente para que um documento seja retornado na página de resultados. </p> <p>O uso de <span class="codeph"> sp_q_required </span> afeta o query principal ( <span class="codeph"> sp_q </span>). </p> <p>Para aplicar a um query numerado, substitua o <span class="codeph"> # </span> no nome do parâmetro pelo número correspondente (por exemplo, <span class="codeph"> sp_q_required_8 </span> se aplica ao query numerado <span class="codeph"> sp_q_8 </span>). O valor padrão do parâmetro é 1 (deve corresponder). </p> <p>Para pesquisar documentos que contenham a palavra "calc", mas NÃO contenham "mac", "win" ou "all" no campo "platform" definido pelo usuário, o formulário de pesquisa HTML pode conter as seguintes linhas: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>35 </p> </td> 
   <td colname="col2"> <p>sp_redirect_ if_one_result </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica se é necessário redirecionar para o URL do resultado da pesquisa se houver apenas um resultado da pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>36 </p> </td> 
   <td colname="col2"> <p>sp_quem indicou </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_quem indicou= url </span> </p> </td> 
   <td colname="col4"> <p>Especifica o URL de quem indicou para a pesquisa. Útil para regras de regravação de pesquisa nas quais os resultados da pesquisa são vinculados de volta ao mesmo site que o formulário de pesquisa. </p> <p>O valor padrão é o valor padrão CGI HTTP_QUEM INDICOU fornecido pelo navegador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro= <span class="varname"> campo </span>: <span class="varname"> relevância </span> </span> </p> </td> 
   <td colname="col4"> <p>Permite tempo de pesquisa opcional, por nome de campo, controle de relevância. O <span class="codeph"> ou </span> no nome do parâmetro significa "substituição de relevância". O parâmetro aceita um ou mais nomes de campo, seguidos por um caractere de dois pontos, seguido por um valor de relevância de 0 a 10. </p> <p>Por exemplo, para definir o valor de relevância para o nome de campo "body" como 10, no momento em que um cliente realiza uma pesquisa, o parâmetro aparece da seguinte forma: </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>Ou, para especificar várias substituições de relevância de campo na string do parâmetro, é possível usar um delimitador de barra vertical. Por exemplo, para definir o valor de relevância para os nomes de campo "body" e "title" como 9, no momento em que um cliente realiza uma pesquisa, o parâmetro aparecerá da seguinte forma: </p> <p> <span class="codeph"> sp_ro=body:9|title:9 </span> </p> <p> <p>Observação:  A especificação de um campo que não esteja envolvido na pesquisa associada não tem efeito. Por exemplo, se você definir <span class="codeph"> sp_ro=title:10 </span>, mas o nome do <span class="codeph"> título do </span> campo não for pesquisado, o parâmetro <span class="codeph"> sp_ro </span> não terá efeito. Em outras palavras, a especificação de um nome de campo usando o parâmetro <span class="codeph"> sp_ro </span> não pesquisa automaticamente esse campo; em vez disso, ele apenas substitui a configuração de relevância associada a esse campo. </p> </p> <p>Consulte <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> Edição de campos de meta tag predefinidos ou definidos pelo usuário </a>. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> Sobre regras de limpeza de Query </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica a ordem de classificação. Zero (0) é o padrão e o meio para classificar por pontuação de relevância. Um (1) significa classificar por data e -1 significa não classificar. </p> <p>Você pode especificar um nome de campo para o valor do parâmetro <span class="codeph"> sp_s </span> . Por exemplo, <span class="codeph"> sp_s=title </span> classifica os resultados de acordo com os valores contidos no campo de título. Quando um nome de campo é usado para o valor de um parâmetro <span class="codeph"> sp_s </span> , os resultados são classificados por esse campo e, em seguida, subclassificados por relevância. </p> <p>Defina Classificação para o campo referenciado como <span class="uicontrol"> Crescente </span> ou <span class="uicontrol"> Decrescente </span> em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span> para ativar esse recurso. </p> <p>Também é possível atribuir vários campos de classificação a um único query definindo o parâmetro <span class="codeph"> sp_s </span> várias vezes no formulário de pesquisa. As linhas de modelo a seguir definem os resultados da pesquisa a serem classificados primeiro por nome de artista, depois por nome de álbum e, em seguida, por nome de rastreamento. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>Também é possível classificar na tabela dados de campo correspondentes especificando um qualificador de nome de tabela antes do nome do campo, por exemplo, items.price. Consulte o parâmetro <span class="codeph"> sp_field_table </span> para obter mais informações sobre a correspondência de tabelas. </p> <p>Se você pesquisar por proximidade, poderá classificar os resultados de acordo com a proximidade especificando um "campo de saída de proximidade". </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Sobre pesquisa de proximidade </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr= campo </span> </p> </td> 
   <td colname="col4"> <p>Especifica o campo de classificação a ser usado para classificação estática. O campo deve ser do tipo Classificação com relevância maior que 0. Se nenhum parâmetro <span class="codeph"> sp_sr </span> for fornecido para o query, um campo do tipo Classificação será selecionado automaticamente. </p> <p>Para desativar a classificação estática de um determinado query, inclua um valor NULL para <span class="codeph"> sp_sr </span> (por exemplo, <span class="codeph"> &lt;input type="hidden" name="sp_sr" value=""&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field= string </span> </p> </td> 
   <td colname="col4"> <p>Especifica o nome de um campo a ser usado juntamente com a tag <span class="codeph"> &lt;search-field-value-lista&gt; </span> no modelo de pesquisa. </p> <p>Você pode especificar vários <span class="codeph"> parâmetros sp_sfvl_field </span> . </p> </td> 
  </tr> 
  <tr>
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;valor_inteiro&gt; </span> </span> </p> </td> 
   <td colname="col4"> <p> Solicita até <span class="codeph"> &lt;integer_value&gt; <span class="varname"> campos </span> de campo de </span> pesquisa-valor-lista de facetas <span class="codeph"> </span> dinâmicas para esta pesquisa. </p> <p>O valor padrão é 0. O valor máximo permitido é o número atual de campos de aspecto dinâmico, contagem de campos de aspecto dinâmico definida para um determinado índice. Valores inteiros abaixo de 0 são tratados como 0. Os valores inteiros especificados acima de <span class="codeph"> dynamic-facet-field-count </span> são limitados a <span class="codeph"> dynamic-facet-field-count </span>. Valores que não sejam inteiros são ignorados; são tratados como valor padrão. </p> <p>Uma determinada pesquisa de fatia é limitada com um valor máximo permitido <span class="codeph"> sp_sfvl_df_count </span> do valor <span class="codeph"> dynamic-facet-field-count dessa fatia </span> . Ao mesclar os resultados da fatia, o valor máximo efetivo de <span class="codeph"> sp_sfvl_df_count </span> é o valor máximo real <span class="codeph"> sp_sfvl_df_count </span> em todas as fatias. </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuração de aspectos dinâmicos </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclude </p> </td> 
   <td colname="col03"> <p> </p> </td>
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclude= &lt; <span class="varname"> nome_do_campo </span>&gt;[|&lt; <span class="varname"> nome_do_campo </span> </span>&gt;|... </p> </td> 
   <td colname="col4"> <p> Especifica uma lista de campos de facetas dinâmicas específicos a serem excluídos da consideração dessa pesquisa. </p> <p>Por padrão, todos os campos de aspecto dinâmico são considerados. </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuração de aspectos dinâmicos </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> nome_do_campo </span>&gt;[|&lt; <span class="varname"> nome_do_campo </span> </span>&gt;|... </p> </td> 
   <td colname="col4"> <p> Especifica uma lista de campos de aspecto dinâmico específicos a serem incluídos nos resultados da pesquisa. </p> <p> <p>Observação:  O parâmetro <span class="codeph"> sp_sfvl_df_count </span> determina o número total de campos de aspecto dinâmicos a serem retornados, incluindo qualquer especificado por meio de <span class="codeph"> sp_sfvl_df_include </span>. Ou seja, usar <span class="codeph"> sp_sfvl_df_include </span> não permite que a contagem total de campos de facetas dinâmicas retornados exceda <span class="codeph"> sp_sfvl_df_count </span>. </p> </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuração de aspectos dinâmicos </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_staged </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p>Se <span class="codeph"> sp_staged=1 </span> for enviado com um query, o query executado será uma pesquisa por etapas. </p> <p>Uma pesquisa por etapas usa todos os componentes que estão preparados no momento, incluindo o índice e os modelos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_start_day, sp_start_month, sp_start_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_start_day= número </span> </p> <p> <span class="codeph"> sp_start_month= número </span> </p> <p> <span class="codeph"> sp_start_year= número </span> </p> </td> 
   <td colname="col4"> <p>Esse triplo de valores especifica o intervalo de datas inicial da pesquisa e você o fornece como um conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_ sugere _q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_Sudan_q= número </span> </p> </td> 
   <td colname="col4"> <p>O parâmetro <span class="codeph"> sp_sugestivo_q </span> determina qual parâmetro <span class="codeph"> sp_q[_#] </span> deve ser usado com o serviço Sugestão. </p> <p>O valor padrão de <span class="codeph"> sp_sugestivo_q </span> é 0, o que significa que o mecanismo de pesquisa usa o valor de <span class="codeph"> sp_q </span> para determinar as sugestões. </p> <p>Defina <span class="codeph"> sp_sugestivo_q=1 </span> para usar o valor de <span class="codeph"> sp_q_1 </span> para determinar as sugestões e assim por diante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t= string </span> </p> </td> 
   <td colname="col4"> <p>Especifica o modelo de transporte a ser usado. </p> <p>Esse parâmetro é útil se você deseja controlar a aparência dos principais resultados de pesquisa em seu site usando diferentes modelos de transporte de pesquisa para cada área na sua conta de pesquisa. </p> <p>O modelo de transporte padrão é "pesquisar". </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> Gerenciamento de vários modelos de transporte para seu site </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p>Quando definido como <span class="codeph"> sp_stage=1, </span>ativa o recurso principal de rastreamento de pesquisa no Simulator. </p> <p>Consulte <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> Sobre o Simulador </a>. </p> <p> <p>Observação:  Se esse parâmetro não for especificado, a pesquisa principal não coletará as informações de rastreamento e as tags do modelo de pesquisa principal relacionadas não terão saída. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w, sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica que a correspondência de som semelhante deve ser ativada ou desativada para este query em particular. </p> <p>O sp_w_control para "Exato" é Ignorado. A correspondência de som é Desativada. </p><p>O sp_w_control para "Alike" é Ignorado. A correspondência de som semelhante está ativada</p><p>O sp_w_control para qualquer outra opção é 1. A correspondência de som é Desativada. </p><p>O sp_w_control para qualquer outra coisa é qualquer outra. A correspondência de som é Ativada. </p>O <span class="codeph"> parâmetro </span> sp_w_control permite criar uma caixa de seleção com palavras negativas ou positivas para o controle do usuário final de correspondência de som. </p> <p>Se <span class="codeph"> sp_w_control=0 </span> for usado, uma caixa de seleção com palavras negativas é usada para definir o parâmetro <span class="codeph"> sp_w </span> como no exemplo a seguir: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>Se <span class="codeph"> sp_w_control=1 </span> for usado, uma caixa de seleção com uma palavra positiva será usada para definir o parâmetro <span class="codeph"> sp_w </span> como a seguir: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>Consulte o formulário de pesquisa avançada de amostra para obter mais exemplos sobre o uso de <span class="codeph"> parâmetros sp_w_control </span> e <span class="codeph"> sp_w </span> . </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Amostra de formulário de pesquisa avançada </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50  </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x= field </span> </p> </td> 
   <td colname="col4"> <p>Especifica os campos a serem pesquisados pela string do query. qualquer meio de pesquisa em todos os campos. título significa pesquisar somente campos de título. desc significa pesquisar somente campos de descrição do documento. teclas significa pesquisar somente palavras-chave do documento. body significa pesquisar somente texto do corpo. alt significa pesquisar somente texto alternativo. url significa pesquisar somente os valores de URL. público alvo significa pesquisar somente palavras-chave do público alvo. Em qualquer um desses casos, as especificações do usuário dos prefixos de campo "text:", "desc:", "keys:", "body:", "alt:", "url:" e "público alvo:" dentro do parâmetro <span class="codeph"> sp_q </span> correspondente são ignoradas. Se <span class="codeph"> sp_x não </span> estiver presente ou se estiver definida como uma string vazia ou qualquer outra, os prefixos de campo do usuário padrão serão permitidos. Consulte a descrição Dicas de pesquisa para obter mais informações sobre os prefixos de campo. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Sobre pesquisadores </a>. </p> <p>Consulte a descrição do formulário de pesquisa avançada de exemplo para obter exemplos usando o parâmetro <span class="codeph"> sp_x </span> . </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Amostra de formulário de pesquisa avançada </a>. </p> <p>Você pode criar query que pesquisam todos os campos definidos como <span class="uicontrol"> Pesquisar por padrão </span> em Opções <span class="uicontrol"> &gt; </span> Metadados <span class="uicontrol"> &gt; </span> Definições <span class="uicontrol"> definindo </span> sp_x=any <span class="codeph"> </span>. Os campos predefinidos e definidos pelo usuário podem ser usados como o valor do parâmetro <span class="codeph"> sp_x </span> . </p> <p>Você também pode atribuir vários campos a um único query definindo o parâmetro <span class="codeph"> sp_x </span> várias vezes. As linhas de modelo a seguir permitem que os usuários query os campos "título" e "autor" para "Grandes Livros". </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#= nome do campo </span> </p> </td> 
   <td colname="col4"> <p>Esse parâmetro especifica qual campo pesquisar no query <span class="codeph"> sp_q_# correspondente </span> . O <span class="codeph"> # <span class="codeph"> </span> é substituído por um número entre 1 e 16 (por exemplo, </span> sp_x_8 <span class="codeph"> </span>). O nome do campo é qualquer campo predefinido ou definido pelo usuário. </p> <p>Se nenhum parâmetro <span class="codeph"> sp_x_# </span> for fornecido para um determinado query numerado, todos os campos definidos como <span class="uicontrol"> Pesquisar por padrão </span> , conforme definido em <span class="uicontrol"> Configuração </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições, </span> serão pesquisados por esse query. </p> <p>Por exemplo, o envio do formulário a seguir retorna todos os documentos que contêm a palavra "ótimo" que também contêm a palavra "Fitzgerald" no campo "autor": </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>É possível associar vários nomes de campo a um query ou query numerado específico, fornecendo mais de uma instância do mesmo parâmetro <span class="codeph"> sp_x </span> ou <span class="codeph"> sp_x_# </span> em uma única solicitação de pesquisa. </p> <p>Por exemplo, para pesquisar a palavra "flor" nos campos "corpo" e "chaves", é possível criar um formulário de pesquisa com as seguintes informações: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Um exemplo típico do uso de parâmetros CGI de pesquisa de backend {#section_260012BBC2514CC9A8E02E53DE8B41EE}

O link a seguir start uma pesquisa usando &quot;Música&quot; como query de pesquisa e usa todos os parâmetros padrão. Observe que o URL é dividido em duas linhas para facilitar a leitura. Em seu HTML, esse link deve estar em uma linha.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

A mesma funcionalidade é mais tipicamente definida com um formulário:

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

Normalmente, você deve usar parâmetros padrão ao iniciar uma pesquisa. Dessa forma, a primeira página é mostrada, classificada por relevância, e permite que o cliente escolha outras páginas e outras opções. Se o formulário de pesquisa em seu site incluir opções para coleções, passe o nome da coleção como um parâmetro.

## Um exemplo detalhado do uso de parâmetros CGI de pesquisa de backend {#section_5FA3C620D5124FB2AB28857F8D8473F6}

Os query de formulário a seguir exibem `25` resultados que começam com o resultado `10`. Resumos não são exibidos, a ordem de classificação é por data e a coleção nomeada `support` é usada. Somente documentos com data dos últimos 30 dias são retornados.

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

