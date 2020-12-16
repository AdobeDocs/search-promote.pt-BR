---
description: Sempre que seu site muda, você pode executar um script ou programa solicitando que o robô de pesquisa execute um índice usando o controle remoto.
seo-description: Sempre que seu site muda, você pode executar um script ou programa solicitando que o robô de pesquisa execute um índice usando o controle remoto.
seo-title: Sobre o controle remoto para indexação
solution: Target
title: Sobre o controle remoto para indexação
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 1%

---


# Sobre o controle remoto para indexação{#about-remote-control-for-indexing}

Sempre que seu site muda, você pode executar um script ou programa solicitando que o robô de pesquisa execute um índice usando o controle remoto.

## Usando o controle remoto para indexação {#concept_C79B322190E84106A434E5C6D4A4118F}

Normalmente, a solicitação de indexação do controle remoto provém de um script ou de um programa localizado no servidor.

O robô executa as mesmas etapas de indexação como se tivesse sido iniciado manualmente pelo menu [!DNL Index]. Para enviar uma solicitação de controle remoto, configure a senha e as sequências de caracteres de resposta necessárias.

## Como fazer uma solicitação de controle remoto {#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

Para fazer uma solicitação de controle remoto, use os seguintes exemplos de formato com base na localização do seu data center:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Localização do centro de dados </p> </th> 
   <th colname="col2" class="entry"> <p>Exemplo </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Londres </p> </td> 
   <td colname="col2"> <p> <code> https://center.lon5.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>América do Norte </p> </td> 
   <td colname="col2"> <p> <code> https://center.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Singapura </p> </td> 
   <td colname="col2"> <p> <code> https://center.sin2.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

ou

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>String e valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp9999999  </span> </p> </td> 
   <td colname="col2"> <p> O número da sua conta. </p> <p>Você pode encontrar seu número de conta em <span class="uicontrol"> <b>Settings</b> </span> &gt; <span class="uicontrol"> <b>Opções de Conta</b> </span> &gt; <span class="uicontrol"> <b>Configurações de Conta</b> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N  </span> </p> </td> 
   <td colname="col2"> <p>Permite verificar o status de um rastreamento de índice em execução. </p> <p> <span class="codeph">  N  </span> é um número inteiro positivo ou  <span class="codeph"> todos  </span>. Se esse for um valor numérico, as últimas linhas <span class="codeph"> N </span> do arquivo de log de índice correspondente serão incluídas na resposta JSON. </p> <p>Se o valor for <span class="codeph"> todos os </span>, o arquivo inteiro será retornado. </p> <p>Se o valor for <span class="codeph"> 0 </span>, nenhuma informação de log será retornada. Esse valor é o padrão para um query de status de índice em execução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op  </span> </p> </td> 
   <td colname="col2"> <p>Permite que você especifique uma das seguintes operações de indexação que deseja executar: </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index  </span> <p>O robô de pesquisa executa um índice completo do seu site. </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incremental_index  </span> <p>O robô de pesquisa executa um índice incremental usando a configuração definida em <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Índice Incremental</b> </span> &gt; <span class="uicontrol"> <b>Configuração</b></span>. </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index  </span> <p>O robô de pesquisa executa uma atualização vertical usando a configuração definida em <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Atualização vertical</b> </span> &gt; <span class="uicontrol"> <b>Configuração</b></span>. </p> <p>Consulte <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Sobre a Atualização Vertical</a>. </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index  </span> <p>O robô de pesquisa executa um índice incremental usando o arquivo de texto especificado em <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Índice Script</b> </span> &gt; <span class="uicontrol"> <b>Configuração</b></span>. </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index  </span> <p>O robô de pesquisa executa um índice completo de etapas do seu site. </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incremental_staged_index  </span> <p>O robô de pesquisa executa um índice escalonado incremental usando a configuração definida em <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Índice Incremental</b> </span> &gt; <span class="uicontrol"> <b>Configuração</b></span>. </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index  </span> <p>O robô de pesquisa executa uma atualização de etapas verticais usando a configuração definida em <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Atualização vertical</b> </span> &gt; <span class="uicontrol"> <b>Configuração</b></span>. </p> </li> 
     </ul> </p> <p>Observação:  Para usar as Atualizações verticais, talvez seja necessário ativá-las em sua conta pelo representante de conta do Adobe ou pelo Suporte ao Adobe. </p> <p>Consulte <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Sobre a atualização vertical </a>. </p> <p>Você pode anexar <span class="codeph"> _saved </span> a qualquer um dos valores <span class="codeph"> sp_operation </span> acima para que o robô de pesquisa tente usar o conteúdo salvo. Por exemplo, você pode especificar o seguinte: </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p>ou </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>Ou você pode anexar <span class="codeph"> _status </span> a qualquer um dos valores <span class="codeph"> sp_operation </span> acima para solicitar um relatório de status para a operação atual ou mais recente. Por exemplo, você pode especificar o seguinte: </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p>ou </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>e os resultados são retornados como um objeto JSON. Inclua <span class="codeph"> sp_lines=N </span> para incluir N linhas do arquivo de log associado. Se N for negativo, as últimas N linhas serão incluídas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= pushlive  </span> </p> </td> 
   <td colname="col2"> <p> Permite que você envie ao vivo remotamente um índice de preparo. </p> <p>Qualquer tentativa de anexar <span class="codeph"> _saved </span> à operação ativa de envio é ignorada. </p> <p>Quando você executa uma operação <span class="codeph"> pushlive </span>, uma string de texto de resposta OK, Priority ou Error é retornada ao servidor. Especifique essas sequências de caracteres de resposta na página <span class="wintitle"> Controle remoto </span>. </p> <p>Consulte <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> Configurando o controle remoto para indexação</a>. </p> <p>Se você mover ao vivo quando não houver um índice de preparo, nada acontecerá e a sequência de caracteres de resposta OK será retornada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxx  </span> </p> </td> 
   <td colname="col2"> <p>A senha do controle remoto. </p> </td> 
  </tr> 
 </tbody> 
</table>

A pesquisa retorna dados na forma de uma resposta HTTP adequada. A resposta completa é composta de um status HTTP, cabeçalhos de resposta HTTP, uma linha em branco e a string de resposta.

Por exemplo, suponha que você execute a seguinte solicitação de controle remoto:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

A seguir está a resposta do servidor:

```
Status: 200 OK 
Content-type: text/plain 
OK
```

Ou suponha que você execute a seguinte solicitação de status de controle remoto:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status
```

A resposta do servidor pode ser semelhante ao seguinte:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:58:58-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "status": 1, 
    "message": "ok" 
}
```

Para obter as primeiras dez linhas da listagem de log associadas à operação de índice, juntamente com seu status, o seguinte query é usado:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=10
```

A resposta do servidor:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:59:30-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "offset": 672, 
    "lines": [ 
        "07/25 16:40:07 PST   ======== Starting manual crawl of account sp99999999. ========", 
        "07/25 16:40:08 PST   Loading existing data", 
        "07/25 16:40:08 PST   Downloading entrypoint https://www.atomz.com/", 
        "07/25 16:40:08 PST   Robots.txt exclude mask: https://www.atomz.com/snap", 
        "07/25 16:40:08 PST   Exclude mask: regexp ^https://www.atomz.com/$", 
        "07/25 16:40:08 PST   Include mask: https://www.atomz.com/", 
        "07/25 16:40:08 PST   Downloading https://www.atomz.com/style.css", 
        "07/25 16:40:09 PST   Ignoring https://www.atomz.com/style.css, document type 'text/css'.", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/privacy.html", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/terms.html" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Observe o valor `offset`. Esse valor identifica a posição de deslocamento do arquivo no arquivo de log, onde a leitura ficou desativada. Para ler as dez linhas *ao lado* no arquivo, inclua, neste exemplo, `&sp_offset=672` na solicitação enviada para o servidor.

Usando `sp_offset`, você pode navegar efetivamente por um arquivo de log.

Para obter as *last* dez linhas do log, juntamente com o status, especifique a contagem como um número negativo. Por exemplo, especifique `sp_lines=` com um valor de `-10` como no seguinte:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=-10
```

A resposta do servidor:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T11:01:14-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "lines": [ 
        "07/25 16:40:20 PST   End Time: 07/25/2017 16:40:20 PST", 
        "07/25 16:40:20 PST   Elapsed Time: 13 seconds", 
        "07/25 16:40:20 PST   Pages Crawled: 3 pages", 
        "07/25 16:40:20 PST   Pages Indexed: 3 pages", 
        "07/25 16:40:20 PST   Words/Bytes Indexed: 2373 words/ 20618 bytes", 
        "07/25 16:40:20 PST   Errors: 0", 
        "07/25 16:40:20 PST   *** Index Summary ***", 
        "07/25 16:40:20 PST   Total Pages: 3", 
        "07/25 16:40:20 PST   --------------------------------------------------------------------", 
        "07/25 16:40:20 PST   ======== Finish manual crawl of account sp99999999: Done. ========" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Observe que não há valor `offset` retornado aqui, pois essa operação terminou no final do arquivo e não há mais linhas para ler.

## Configurando o controle remoto para indexação {#task_57C296258404448DA7A5ADC9B7232391}

Sempre que seu site muda, você pode usar o Controle remoto para executar um script ou programa do servidor, solicitando que o robô de pesquisa execute um índice.

**Configuração do controle remoto para indexação**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Remote Control]**.
1. Na página [!DNL Remote Control], defina cada opção de campo de configuração para poder enviar uma solicitação de indexação do servidor automaticamente para indexar seu site.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Opção </p> </th> 
    <th colname="col2" class="entry"> <p>Descrição </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Senha do controle remoto </p> </td> 
    <td colname="col2"> <p>Especifique a senha do controle remoto. </p> <p> As senhas diferenciam maiúsculas de minúsculas, têm pelo menos seis caracteres e devem incluir pelo menos uma letra. É recomendável incluir pelo menos um número. </p> <p>Não use a senha de logon de pesquisa/comercialização do site. </p> <p>Sua senha é usada em cada solicitação de controle remoto. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Sequência de Resposta OK </p> </td> 
    <td colname="col2"> <p>Permite que você especifique uma string de texto de resposta OK se a operação de índice solicitada começar com êxito. Nesses casos, o robô de pesquisa retorna a sequência de caracteres de resposta OK ao servidor. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>String de resposta de prioridade </p> </td> 
    <td colname="col2"> <p>Se outra operação de indexação estiver em andamento quando a solicitação remota for feita, o robô de pesquisa não poderá executar o índice solicitado. Nesses casos, sua sequência de texto de resposta Prioridade é retornada ao servidor. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>String de resposta de erro </p> </td> 
    <td colname="col2"> <p>Permite que você especifique uma sequência de texto de resposta de erro Se a senha estiver incorreta ou se ocorrer outro erro. Nesses casos, o robô de pesquisa retorna a sequência de caracteres de resposta Erro ao servidor. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
