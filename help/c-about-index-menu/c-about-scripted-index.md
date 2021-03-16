---
description: Com o Índice de script, você pode gravar, atualizar e manter opções de indexação incremental sem precisar fazer logon. O robô de pesquisa lê as instruções de um arquivo de texto hospedado em seu servidor.
solution: Target
subtopic: Scripted Index
title: Sobre índice de script
topic: Índice,Pesquisa e comercialização do site
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1730'
ht-degree: 1%

---


# Sobre o Índice com script{#about-scripted-index}

Com o Índice de script, você pode gravar, atualizar e manter opções de indexação incremental sem precisar fazer logon. O robô de pesquisa lê as instruções de um arquivo de texto hospedado em seu servidor.

## Usando o índice de script {#concept_34F58D551BC04BFB8ADC294B9DA9199D}

## Sobre a configuração de indexação incremental com script {#section_161D254065E143F3A39F3FC09C400090}

Para usar o Índice com script, use a página Configuração de índice incremental com script para especificar o URL para um arquivo de script (um arquivo de texto simples) localizado em seu servidor. Por exemplo, `https://www.mysite.com/indexlist.txt`. Conforme seu site muda, você pode adicionar blocos de comando ao arquivo de texto manualmente ou automaticamente (com um script acionado pela chegada de informações de um feed de notícias, marcador de ações ou outro arquivo alterado).

Quando o índice incremental com script começa, o robô de pesquisa lê o arquivo de texto e executa os novos comandos encontrados nesse arquivo. Por padrão, o robô de pesquisa processa apenas os novos comandos, que são determinados pela data do arquivo. A menos que você marque **[!UICONTROL Clear Date]** no momento em que configura o Índice de scripts, o robô de pesquisa &quot;lembra&quot; o especificador de datas do bloco processado mais recentemente.

## Sobre o arquivo de script {#section_B312E40539F44C6583B4F9637D428E19}

O arquivo de script especificado no URL é um arquivo de texto simples localizado no servidor. Você pode usar retornos de carro, feeds de linha ou ambos para a sequência de fim de linha. Uma linha em branco contém zero ou mais caracteres de espaço em branco, seguidos por uma sequência de fim de linha. Todos os comandos não diferenciam maiúsculas de minúsculas.

O arquivo de texto é organizado em blocos que descrevem as informações que o robô de pesquisa usa ao executar um índice incremental com script.

Os blocos são ordenados por data, com os blocos mais antigos na parte superior do arquivo de texto e os blocos mais recentes na parte inferior. Cada bloco começa com um comando date-command de linha única e um comando date-specifier e termina com um separador de linha em branco, como no exemplo de bloco a seguir (entre eles, há vários comandos):

Um zero à esquerda é necessário para todas as datas ordinais inferiores ao décimo ao usar o estilo HTTP 1.1. Por exemplo, 6 de novembro é 6 de novembro, não 6 de novembro.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Comando </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>date-command </p> </td> 
   <td colname="col2"> <p>A primeira linha de cada bloco começa com um de dois comandos de data: </p> <p> 
     <ul id="ul_9C1B229B7F1846C490B853FC34989E77"> 
      <li id="li_31FEF1A7163842BDBB0ABE779D07045A"> <span class="codeph"> data  </span> <p>Use o comando "date" para indicar que o especificador de data consistirá em um dia, data, hora e fuso horário. </p> </li> 
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> segundos </span> <p>Use <span class="codeph"> segundos </span> para indicar que o especificador de data consistirá em um tempo em segundos de época (por exemplo, 78411777). Ao usar <span class="codeph"> segundos </span>, verifique se o número de segundos aumenta entre os blocos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>especificador de data </p> </td> 
   <td colname="col2"> <p>O comando <span class="codeph"> date-specifier </span> normalmente registra a data e a hora ordinais (comando de data) ou o tempo em segundos de época (comando segundos) em que as informações do bloco foram adicionadas ao arquivo. Por exemplo: </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>Um zero à esquerda é necessário para todas as datas ordinais inferiores ao décimo ao usar o estilo HTTP 1.1. Por exemplo, 6 de novembro é 6 de novembro, não 6 de novembro. </p> <p>O robô de pesquisa "lembra" o especificador de datas do bloco processado mais recentemente e indexa apenas as informações que considera como "mais recentes". (Tempo real não importa para o robô de pesquisa. Em vez disso, o tempo em relação a outros tempos processados anteriormente é o que importa.) </p> <p>Depois que o robô de pesquisa ler um bloco com um especificador de data de 10:00 p.m., por exemplo, ele não lê nenhum bloco que registre horários antes das 22:00, independentemente de quando a operação de índice é executada. Em um pior cenário, você pode inserir erroneamente o ano "2040" em vez de "2004" no seu especificador de datas. Nesse caso, o robô de pesquisa indexa o bloco 2040 durante a próxima operação de indexação e depois recusa ler qualquer outro bloco de informações (a menos que um post-dates 2040). Se isso acontecer, remova todos os blocos processados anteriormente do arquivo de texto, clique em <span class="uicontrol"> Limpar Data </span> e coloque-o online. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>linha de comentário </p> </td> 
   <td colname="col2"> <p>Comece as linhas de comentário com o caractere "#". </p> <p>Cada linha de comentário deve ser uma linha própria; não é possível digitar comentários de fim de linha. </p> <p>Uma linha de comentário não é considerada uma linha em branco. Ele também pode aparecer em qualquer lugar em um bloco, mesmo antes de um comando date ou seconds, como no exemplo a seguir: </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;#Added&nbsp;by&nbsp;Cathy&nbsp;Read&nbsp;after&nbsp;the&nbsp;Y2K&nbsp;seminar 
      &nbsp;&nbsp;&nbsp;&nbsp;date&nbsp;Mon,&nbsp;29&nbsp;Dec&nbsp;1999&nbsp;09:32:20&nbsp;GMT&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>action-command </p> </td> 
   <td colname="col2"> <p>Cada bloco de texto pode conter quantos comandos de ação desejar. As seguintes opções de comando de ação correspondem às opções para indexação incremental padrão: </p> <p> 
     <ul id="ul_8E1435350A0F416BB8F7826CD3886E74"> 
      <li id="li_22181666628C48A28A6A0BA1F7CA8E77"> 
       <code>
         add 
       </code> <p>Use com URL. O robô de pesquisa indexa apenas os URLs especificados que foram alterados desde a última operação de indexação. Além disso, o robô de pesquisa segue os links contidos em documentos especificados e indexa apenas os documentos que foram alterados. </p> <p>Você pode seguir o URL com 
        <code>
          nofollow 
        </code> ou 
        Palavras-chave <code>
          noindex 
        </code> como no exemplo a seguir: </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <code>
         update 
       </code> <p>Use com máscara de URL. O robô de pesquisa encontra e atualiza todos os documentos que correspondem à máscara de URL especificada. </p> <p>Você pode seguir o URL com 
        <code>
          nofollow 
        </code> ou 
        Palavras-chave <code>
          noindex 
        </code> como no exemplo a seguir: </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
      <li id="li_B3EC8B1670D54F66A1D8411A694EF7E4"> 
       <code>
         include 
       </code> ou 
       <code>
         exclude 
       </code> <p>Use com máscara de URL. O robô de pesquisa encontra e indexa ("include") ou ignora ("exclude") documentos com base no tipo de máscara especificada. </p> <p>Por exemplo, </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/products/household/lightbulbs*.html </code> </p> <p>ou </p> <p> <code> exclude&amp;nbsp;https://www.mydomain.com/archive/ </code> </p> </li> 
      <li id="li_050B54B735F0475E93806455FA6DC6A5"> 
       <code>
         include-date 
       </code> ou 
       <code>
         exclude-date 
       </code> <p>Use com máscara de URL. O robô de pesquisa encontra e indexa ("include") ou ignora ("exclude") documentos com base no URL e na data dos documentos. Os seguintes tipos de máscaras estão disponíveis: </p> <p> 
        <ul id="ul_23A15CB492214B86BE84D8E6EA1820AE"> 
         <li id="li_0C7051AC3B5A4C57A3E477F7B6246611"> 
          <code>
            include-days NNN 
          </code> <p>O robô de pesquisa indexa todos os documentos que correspondem à máscara de URL especificada e são NNN dias ou mais antigos. </p> <p>Você pode seguir a máscara de URL com as palavras-chave 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code>, e/ou 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <code>
            include-date YYYY-MM-DD 
          </code> <p> O robô de pesquisa indexa todos os documentos que correspondem à máscara de URL especificada e são tão antigos ou mais antigos que a data AAAA-MM-DD, onde "AAAA" é o ano de 4 dígitos, "MM" é o mês de um ou dois dígitos (1-12) e "DD" é o dia de um ou dois dígitos (1-31). </p> <p>Você pode seguir a máscara de URL com as palavras-chave 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code>, e/ou 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <code>
            exclude-days NNN 
          </code> <p> Desativa a indexação de todos os documentos que correspondem à máscara de URL especificada e são NNN dias ou mais antigos. </p> <p>Você pode seguir a máscara de URL com a palavra-chave 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <code>
            exclude-date YYYY-MM-DD 
          </code> <p>Desativa a indexação de todos os documentos que correspondem à máscara de URL especificada e são tão antigos ou mais antigos que a data AAAA-MM-DD. </p> <p>Você pode seguir a máscara de URL com a palavra-chave 
           <code>
             server-date 
           </code>. </p> </li> 
        </ul> </p> </li> 
      <li id="li_AA78F22B60FE4535BE73BA87A8992C08"> 
       <code>
         delete 
       </code> <p>Especifique URLs. O robô de pesquisa remove documentos do índice que são identificados pelo URL. </p> </li> 
      <li id="li_9C63061568AA4D57A4FEBCF6DB9194EC"> 
       <code>
         deletemask 
       </code> <p>O robô de pesquisa remove documentos do índice que correspondem à máscara de URL especificada. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte também [Sobre máscaras de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

## Exemplo de arquivo de script {#section_9F580F20E7214751B157A28B392BD64E}

No exemplo de arquivo de script a seguir, o robô de pesquisa processa os blocos, desde que os especificadores de data postem o especificador de data do bloco processado mais recentemente. Se esse for o caso, as seguintes operações de indexação ocorrem:

* Exclui `y2k-problems.html` do índice.
* Adiciona `no-y2k-problems.html` ao índice de pesquisa e não segue nenhum dos links para `no-y2k-problems.html`.

* Ao rastrear, exclua URLs que correspondam a `housewares.htm` e `lightfixtures.htm`l do índice de pesquisa.

* Inclua todos os outros diretórios e documentos em `www.mydomain.com`.
* Atualize todos os documentos nos diretórios `products` e `information`, rastreando e indexando todos os links subsidiários que foram alterados desde a última operação de indexação.

* Durante o rastreamento, exclua URLs na seção `archive` do site se elas tiverem data de 1 de janeiro de 1999 ou anterior a elas.
* Exclua URLs que correspondam a `housewares.html` e `lightfixtures.html` do índice de pesquisa.

* Arquivos de índice no diretório `help`, mas não rastreiam nem indexam nenhum link desses arquivos.
* Rastreie e indexe quaisquer outros arquivos encontrados para `www.mydomain.com`.

```
# Start of file. 
# Added by John Smith 
date Sat, 01 Jan 2004 16:05:53 PST 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/ 
delete https://www.mydomain.com/y2k-problems.html 
add https://www.mydomain.com/no-y2k-problems.html nofollow 
 
date Sun, 02 Jan 2004 20:19:08 PST 
# Added by the wire service updater 
exclude-date 1999-01-01 https://www.mydomain.com/archive server-date 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/help/ nofollow 
include https://www.mydomain.com/ 
# no add files, just update existing files 
# update all files in the "products" directory 
update https://www.mydomain.com/products/ 
# update all files in the "information" directory 
update regexp ^https://www\.mydomain\.com/information/.*$ 
# End of file.
```

## Configurar um índice incremental com script {#task_05AE040FE75E40FFAA5E10B6B6D4D255}

Você pode especificar um script criado que grava, atualiza e mantém um índice incremental, sem a necessidade de fazer logon. O robô de pesquisa lê as instruções do arquivo de texto hospedado no servidor para executar o índice incremental.

**Para configurar um índice incremental com script**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Configuration]**.
1. Na página **[!UICONTROL Scripted Incremental Index Configuration]**, em **[!UICONTROL Script File URL]**, digite o URL para o script do arquivo de texto que está localizado em seu servidor.

   Consulte [Sobre o Índice com script](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D).
1. (Opcional) Marque **[!UICONTROL Clear Date]** se não quiser que o robô de pesquisa &quot;lembre-se&quot; do especificador de datas do bloco processado mais recentemente.

   Por padrão, o robô de pesquisa processa apenas novos blocos de comandos encontrados no arquivo de texto, que é determinado pela data do arquivo. Se não quiser o padrão, marque **[!UICONTROL Clear Date]**.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuração do agendamento de índice incremental com script para um site ativo {#task_B3A87AC4AC784507859C23B9062BA11C}

Você pode agendar a indexação incremental por script para que ocorra em intervalos regulares ao longo do dia.

A hora base selecionada é local de acordo com o fuso horário configurado nas Configurações da conta.

Consulte [Definição das configurações da sua conta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Os servidores da Web geralmente são agendados para serem mantidos no meio da noite. Se o servidor estiver inativo durante um tempo de índice agendado, o processo de indexação falhará. Certifique-se de selecionar uma hora do dia em que o servidor da Web está disponível.

O agendamento de índice se aplica somente ao seu índice ativo; não é possível agendar índices incrementais preparados.

**Para definir o agendamento de índice incremental com script para um site ativo**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Schedule]**.
1. Na página **[!UICONTROL Scripted Incremental Index Schedule]**, na lista suspensa **[!UICONTROL Read the Scripted Incrementally Indexing File]**, selecione a frequência com que deseja que o arquivo de texto de índice incremental com script seja executado, em horas ou minutos.
1. Na lista suspensa **[!UICONTROL Base Time]**, selecione a hora inicial em que deseja gerar novamente um novo índice incremental por script.
1. Clique em **[!UICONTROL Save Changes]**.

## Executando um índice incremental com script de um site ativo ou temporário {#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}

Você pode usar o Índice incremental com script para indexar &quot;partes&quot; de seu site ativo ou temporário, como uma coleção de páginas alteradas com frequência, tudo sem precisar fazer logon.

Para usar esse recurso, certifique-se de configurar um arquivo de texto de índice incremental com script.

Consulte [Configuração de um índice incremental com script](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255).

**Para executar um índice incremental com script de um site ativo ou temporário**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Index]**.
   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Index]**.

1. Clique em **[!UICONTROL Scripted Index Now]**.
1. (Opcional) Se ocorreram erros de indexação, clique em **[!UICONTROL View Errors]** para visualizar o log associado.

## Visualização do log de índice incremental com script de um site ativo ou preparado {#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}

Quando um índice de script completo em tempo real ou um índice de script completo preparado estiver concluído, você poderá exibir seu log associado para solucionar todos os erros que ocorreram.

Não é possível exportar logs nem salvá-los. No entanto, o log permanece disponível para exibição até que o novo índice ocorra.

**Para exibir o log de índice incremental de um site ativo ou temporário**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Log]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Log]**.

1. Na página de log, na parte superior ou inferior, execute um dos seguintes procedimentos:

   * Use as opções de navegação **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** para percorrer o log.

   * Use as opções de exibição **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** para refinar o que você vê.

