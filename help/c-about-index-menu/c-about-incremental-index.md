---
description: Você pode usar o Índice incremental para indexar "partes" de seu site ativo ou temporário, como uma coleção de páginas alteradas com frequência.
solution: Target
subtopic: Incremental Index
title: Sobre índice incremental
topic: Índice,Pesquisa e comercialização do site
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 1%

---


# Sobre o Índice Incremental{#about-incremental-index}

Você pode usar o Índice incremental para indexar &quot;partes&quot; de seu site ativo ou temporário, como uma coleção de páginas alteradas com frequência.

## Usando o Índice Incremental {#concept_A7770F0552D14C47B3DDB65DB78FFFEE}

Um índice incremental demora apenas segundos para ser executado e é útil em sites de grande capacidade que podem levar muitas horas para ser indexados completamente.

Quando você gera um índice incremental, as informações de status são exibidas, como tempo de início, tempo decorrido e erros durante o processo de indexação. As informações sobre o status do último índice também são exibidas.

Você pode interromper ou reiniciar o processo de indexação incremental a qualquer momento.

Embora o novo índice incremental seja criado para seu site ativo, os clientes podem continuar a pesquisar seu site usando seu último índice incremental.

## Configurar um índice incremental de um site preparado {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

Você pode configurar quais páginas do site deseja incluir em seu índice incremental especificando URLs de site e máscaras de URL.

**Para configurar um índice incremental de um site preparado**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Configuration]**.
1. Na página **[!UICONTROL Incremental Index Configuration]** , use os vários campos para especificar quais páginas deseja indexar.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Campo </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Adicionar ou atualizar URLs </p> </td> 
      <td colname="col2"> <p>Especifique URLs. </p> <p>O robô de pesquisa indexa apenas os documentos especificados que foram alterados desde a última vez que você indexou. </p> <p>Além disso, o robô de pesquisa segue os links contidos nos documentos especificados e indexa apenas os documentos que foram alterados. </p> <p>Este campo deve conter somente URLs de documento e não máscaras, como no exemplo a seguir: </p> <p> 
        <code>
          https://www.mydomain.com/products/new.html 
        </code> </p> <p>Você pode usar as seguintes palavras-chave com o URL: </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <code>
            noindex 
          </code> <p>Se você não quiser indexar o texto na página que corresponde a um URL especificado, mas quiser seguir os links da página, adicione 
            <code>
              noindex 
            </code> após o URL, como no exemplo a seguir: </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html noindex 
            </code> </p> <p>Certifique-se de separar 
            <code>
              noindex 
            </code> do URL com um espaço; uma vírgula não é um separador válido. </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <code>
            nofollow 
          </code> <p>Se você deseja indexar o texto na página que corresponde ao URL especificado, mas não deseja seguir os links da página, adicione 
            <code>
              nofollow 
            </code> após o URL, como no exemplo a seguir: </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html nofollow 
            </code> </p> <p> Certifique-se de separar 
            <code>
              nofollow 
            </code> do URL com um espaço; uma vírgula não é um separador válido. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Localizar e atualizar máscaras de URL </p> </td> 
      <td colname="col2"> <p>Especifique máscaras de URL simples: caminho completo, caminho parcial ou caminhos que usam curingas ou expressões regulares. </p> <p>O robô de pesquisa encontra todos os documentos e índices correspondentes apenas os que foram alterados desde a última vez que você indexou. </p> <p>Além disso, o robô de pesquisa segue os links contidos nos documentos correspondentes e indexa apenas as páginas que foram alteradas. Por exemplo: </p> <p> 
      <code>
        https://www.mydomain.com/products/household/*.html 
      </code> </p> <p>Também é possível usar expressões regulares como no exemplo a seguir: </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/household/.*\.html$ 
      </code> </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares</a>. </p> <p>Também é possível usar as palavras-chave 
      <code>
        nofollow 
      </code> e 
      <code>
        noindex 
      </code> conforme descrito em <span class="uicontrol"> Adicionar ou atualizar URLs </span> acima. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir e excluir máscaras de URL </p> </td> 
      <td colname="col2"> <p>Especifique máscaras simples de inclusão ou exclusão de URL: caminho completo, caminho parcial ou caminhos que usam curingas ou expressões regulares. </p> <p>O robô de pesquisa encontra e indexa ("include") ou ignora ("exclude") documentos com base no tipo de máscara especificada. </p> <p> Ao indexar um site, as instruções são seguidas na ordem de aparência. Por exemplo, a seguinte lista de máscaras: </p> <p> 
      <code>
        include https://www.mydomain.com/products/household/lightbulbs*.html 
      </code> </p> <p> 
      <code>
        exclude https://www.mydomain.com/products/ 
      </code> </p> <p>indexa as páginas 
      <code>
        lightbulbs1.html 
      </code> e 
      <code>
        lightbulbs2.html 
      </code>. No entanto, ele não indexa nenhuma outra página que esteja listada no diretório de produtos. </p> <p>Uma máscara de URL que aparece primeiro sempre tem precedência sobre uma que aparece mais tarde na lista. Além disso, se o robô de pesquisa encontrar um documento que corresponda a uma máscara de inclusão e uma máscara de exclusão, a máscara listada primeiro terá prioridade. </p> <p>Também é possível usar as palavras-chave 
      <code>
        nofollow 
      </code> e 
      <code>
        noindex 
      </code> conforme descrito em <span class="uicontrol"> Adicionar ou atualizar URLs </span> acima. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> Sobre máscaras de URL</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir e excluir máscaras de data </p> </td> 
      <td colname="col2"> <p>Especifique máscaras de data simples de inclusão ou exclusão: caminho completo, caminho parcial ou caminhos que usam curingas ou expressões regulares. </p> <p>O robô de pesquisa encontra e indexa ("include") ou ignora ("exclude") documentos com base no URL e na data dos documentos. </p> <p>Você pode usar os seguintes tipos de máscaras de data: </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <code>
        include-days NNN 
      </code> <p>O robô de pesquisa indexa todos os documentos que correspondem à máscara de URL especificada e são NNN dias ou mais antigos. </p> <p>Você pode seguir a máscara de URL com uma ou mais das seguintes palavras-chave: 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">nofollow </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">data do servidor </li> 
        </ul> </p> <p>Por exemplo, a seguinte máscara inclui todos os documentos na pasta /archive/support que tenham 0 dias ou mais: </p> <p> 
        <code>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </code> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <code>
        include-date YYYY-MM-DD 
      </code> <p>O robô de pesquisa indexa todos os documentos que correspondem à máscara de URL especificada e são tão antigos ou mais antigos que a data AAAA-MM-DD. </p> <p>Você pode seguir a máscara de URL com uma ou mais das seguintes palavras-chave: </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">nofollow </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> data do servidor </li> 
        </ul> </p> <p>O exemplo de máscara a seguir inclui todos os documentos na pasta /archive/ com data de 25 de julho de 2011 ou anterior: </p> <p> 
        <code>
          include-date 2011-07-25 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <code>
        exclude-days NNN 
      </code> <p>Desative a indexação de todos os documentos que correspondem à máscara de URL especificada e são NNN dias ou mais antigos. </p> <p>Como opção, você pode seguir a máscara de URL pela palavra-chave 
        <code>
          server-date 
        </code>. </p> <p>O exemplo de máscara a seguir exclui todos os arquivos PDF com 90 dias ou mais de seu índice: </p> <p> 
        <code>
          exclude-days 90 *.pdf 
        </code> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <code>
        exclude-date YYYY-MM-DD 
      </code> <p>Desative a indexação de todos os documentos que correspondem à máscara de URL especificada e que são tão antigos ou mais antigos que a data AAAA-MM-DD. </p> <p>Como opção, você pode seguir a máscara de URL pela palavra-chave 
        <code>
          server-date 
        </code>. </p> <p>O exemplo de máscara a seguir exclui todos os documentos na pasta /archive/ datada de ou antes de 23 de abril de 2004: </p> <p> 
        <code>
          exclude-date 2004-04-23 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      </ul> </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local"> Sobre máscaras de data</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Excluir URLs </p> </td> 
      <td colname="col2"> <p>Especifique URLs. </p> <p>O robô de pesquisa encontra e exclui os documentos especificados do seu índice de pesquisa. Se uma página especificada já estiver no índice de pesquisa, o robô a excluirá antes de adicionar ou atualizar quaisquer outras páginas. </p> <p>Este campo deve conter somente URLs de documento, e não máscaras. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Localizar e excluir máscaras de URL </p> </td> 
      <td colname="col2"> <p>Especifique máscaras de URL simples: caminho completo, caminho parcial ou que usam curingas ou expressões regulares. </p> <p>Se a máscara de URL especificada corresponder às páginas no seu índice de pesquisa, o robô de pesquisa excluirá as páginas antes de adicionar ou atualizar quaisquer outras páginas. Por exemplo: </p> <p> 
      <code>
        https://www.mydomain.com/products/1998/household/* 
      </code> </p> <p>Também é possível usar expressões regulares como no exemplo a seguir: </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/199[567]/.*$ 
      </code> </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares</a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurar o agendamento de índice incremental para um site ativo {#task_2A46BA189ECC4317A9D5C6E99A336F33}

Você pode selecionar a frequência do Índice incremental e o tempo base usado para rastrear e atualizar seu índice incremental.

O horário selecionado é local de acordo com o fuso horário configurado nas Configurações da conta.

Consulte [Definição das configurações da sua conta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Os servidores da Web geralmente são agendados para serem mantidos no meio da noite. Se o servidor estiver inativo durante um tempo de índice agendado, o processo de indexação falhará. Certifique-se de selecionar uma hora do dia em que o servidor da Web está disponível.

O agendamento de índice se aplica somente ao seu índice ativo; não é possível agendar índices preparados.

**Para definir o agendamento de índice incremental para um site ativo**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Schedule]**.
1. Na página **[!UICONTROL Incremental Index Schedule]** , na lista suspensa **[!UICONTROL Incrementally Index]**, selecione a frequência de indexação em horas ou minutos.
1. Na lista suspensa **[!UICONTROL Base Time]**, selecione a hora inicial em que deseja gerar novamente um novo índice incremental.
1. Clique em **[!UICONTROL Save Changes]**.

## Executando um índice incremental de um site ativo ou temporário {#task_9BFB6157F3884B2FAECB7E0E9CA318CB}

Você pode usar o Índice incremental para indexar &quot;partes&quot; de seu site ativo ou temporário, como uma coleção de páginas alteradas com frequência.

**Para executar um índice incremental de um site ativo ou temporário**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Index]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Index]**.

1. Clique em **[!UICONTROL Incremental Index Now]**.
1. (Opcional) Se ocorreram erros de indexação, clique em **[!UICONTROL View Errors]** para visualizar o log associado.

## Visualização do log de índice incremental de um site ativo ou temporário {#task_E668E1F1240C476DAA1CA783DC728232}

Quando um índice incremental ao vivo ou um índice incremental por etapas é concluído, você pode exibir seu log associado para solucionar problemas que ocorreram.


Não é possível exportar logs nem salvá-los. O log permanece disponível para exibição até que o novo índice ocorra.

**Para exibir o log de índice incremental de um site ativo ou temporário**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Log]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Log]**.

1. Na página de log, na parte superior ou inferior, execute um dos seguintes procedimentos:

   * Use as opções de navegação **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** para percorrer o log.

   * Use as opções de exibição **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** para refinar o que você vê.

