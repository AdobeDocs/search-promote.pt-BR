---
description: Use o menu Filtragem para usar scripts que alteram o conteúdo de um documento da Web antes de ele ser indexado.
solution: Target
subtopic: Filtering
title: Sobre o menu Filtragem
topic-legacy: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
exl-id: 1a1c7b86-a29b-4c17-8743-ff3c2c91b63a
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '4003'
ht-degree: 1%

---

# Sobre o menu Filtragem{#about-the-filtering-menu}

Use o menu Filtragem para usar scripts que alteram o conteúdo de um documento da Web antes de ele ser indexado.

## Sobre o script de filtragem {#concept_E56B73D625854AB2A899EF2D56CFCB47}

Você pode usar [!DNL Filtering Script] para alterar o conteúdo de um documento da Web antes que ele seja indexado.

Você pode inserir tags HTML, remover conteúdo irrelevante e até criar novos metadados HTML com base em URL de um documento, tipo MIME e conteúdo existente. O script de filtragem é um script Perl, que fornece manuseio poderoso de strings e flexibilidade de correspondência regular de expressões. Você usa o script de filtragem com um script de inicialização, script de terminação, script de máscaras de URL e URL de teste.

O script de filtragem é executado sempre que um documento é lido do site. O script é executado como um filtro padrão, em outras palavras, lê dados de STDIN, transforma esses dados de alguma forma e grava os resultados em STDOUT. Você pode usar o script de filtragem para imprimir mensagens de status do script de filtragem para o log de índice. Você pode imprimir as mensagens para STDERR ou por meio da sub-rotina `_search_debug_log()`.

Algumas opções de diferencial de GNU que podem ser usadas no modo **[!UICONTROL Expert (diff)]** na página Script de filtragem preparada incluem:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opção de diferencial GNU </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações na quantidade de espaço em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações que inserem ou excluem linhas em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando três linhas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Linhas -C  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando linhas (um número inteiro) de contexto ou três linhas se não forem fornecidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações em caso de; considere letras maiúsculas e minúsculas equivalentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Torna a saída semelhante a um script de ed, mas com alterações na ordem em que aparecem no arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> Gera diffs no formato RCS; como <span class="codeph"> -f </span> exceto que cada comando especifica o número de linhas afetadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída unificado, mostrando três linhas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Linhas -U  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída unificado, mostrando linhas (um inteiro) de contexto ou três se linhas não forem fornecidas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode usar variáveis locais, variáveis globais ou ambos nesses scripts. Todas as variáveis globais são precedidas pelo namespace &quot;main::&quot;. Quando o script de filtragem é iniciado, seu ambiente contém os seguintes identificadores de arquivos padrão:

* STDIN - nada (retorna imediatamente EOF quando lido)
* STDOUT - HTML de substituição (se os dados forem impressos em STDOUT, ele será usado no lugar do documento original)
* STDERR - os dados impressos em STDERR são impressos no Log de Índice como um erro

Além disso, você pode gravar mensagens personalizadas no log de índice usando a sub-rotina `_search_debug_log()`, como no exemplo a seguir:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Essas mensagens são exibidas com a palavra `DEBUG` como um prefácio e não são registradas como erros.

Veja a seguir um exemplo de filtragem. Os campos da página da Web `<title>` geralmente começam com o nome da empresa. Embora essas informações sejam úteis para fins de navegação no site, elas não são relevantes ao pesquisar. Se os títulos de todas as páginas da Web do MegaCorp começarem com uma string comum, como a seguinte:

```
<title>MegaCorp -- meaningful title 
here</title>
```

Você deve remover &quot; `MegaCorp --`&quot; do início de cada título de documento e contar cada documento processado com o script de filtragem. Para fazer isso, é possível usar o seguinte script:

```
# Make sure this is an HTML document. 
if ($main::ws_content_type =~ /^text\/html/) { 
    # Read the entire document into a local scalar variable. 
    my @docarray = <>; 
    my $doc = join("", @docarray); 
 
    # Remove "MegaCorp -- " from the title. 
    $doc =~ s/(<TITLE>)MegaCorp -- /$1/gis; 
 
    # Print the resulting document. 
    print $doc; 
 
    # Count that we've filtered one more document. 
    $main::doc_count++; 
}
```

## Variáveis globais {#global-variables}

Você pode usar as seguintes variáveis em qualquer script de filtragem:

| Variável | Descrição |
|--- |--- |
| `$main::search_crawl_type` | O valor de `$main::search_crawl_type` indica o tipo de operação de índice em andamento.  Formulário obsoleto: `$main::ws_crawl_type` As operações de índice e os valores associados incluem o seguinte: <ul><li>Índice completo: Manual - `manual`</li><li>Índice completo: Agendado - `auto`</li><li>Índice completo: Controle remoto - `CGI`</li><li>Índice incremental: Manual - `manual-incremental`</li><li>Índice incremental: Agendado - `auto-incremental` </li><li>Índice incremental: Controle remoto - `CGI-incremental`</li><li>Índice com script: Manual - `manual-indexlist.txt` </li><li>Índice com script: Agendado - `auto-indexlist.txt`</li><li>Índice com script: Controle remoto - `CGI-indexlist.txt`</li><li>Regenerar - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | O valor indica se a opção de indexação &quot;Clear index cache&quot; foi solicitada para a operação de índice atual. Se &quot;Limpar cache de índice&quot; foi solicitado, o valor de `$main::search_clear_cache` é &quot; `1`&quot;.  Forma obsoleta: `$main::ws_clear_cache` |
| `$main::search_fields` | O valor contém uma lista separada por tabulações dos campos de metadados definidos na conta. Por padrão, o valor é:   `url title desc keys target body alt date charset language` Formulário obsoleto: `$main::ws_fields` |
| `$main::search_collections` | O valor contém uma lista separada por tabulações das Coleções definidas na conta.  Forma obsoleta: `$main::ws_collections` |
| `$main::search_url` | O valor é o URL totalmente qualificado do documento.  Forma obsoleta: `$main::ws_url` |
| `$main::search_content_type` | O valor é o tipo de conteúdo do documento, conforme buscado na meta tag http-equiv. Um valor típico é &quot;text/html; charset=iso-8859-1&quot;.  Forma obsoleta: `$main::ws_content_type` |
| `$main::search_content_class` | O valor é a classe de conteúdo do documento, conforme derivado do campo content-type .  Forma obsoleta: `$main::ws_content_class` |
| `$main::search_syntax_check` | O valor reflete o uso do botão &quot;Verificar sintaxe&quot;. Se clicado, o valor é 1 (um); caso contrário, seu valor será 0 (zero).  Forma obsoleta: `$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Se fornecido pelo servidor da Web, esse valor contém a representação de época (segundos desde 1° de janeiro de 1970) da data da última modificação do documento.  Você pode formatar esse valor usando a chamada da biblioteca Perl localtime() . |

### Dicas rápidas {#section_89A5C16911744AF98E232DF608C6A1F5}

* Todas as variáveis globais são precedidas pelo namespace &quot;main:&quot;:: `$main::doc_count = 0;`
* Todas as variáveis locais são declaradas com &quot;my&quot;: `my $i = 0;`
* As sub-rotinas são definidas no script de inicialização. Eles não precisam de um namespace &quot;main::&quot; explícito: `sub my_sub {` `...`

   `}`

* Teste o `$main::search_content_type` antes de fazer alterações em um arquivo. O teste pode ajudá-lo a evitar alterações descuidadas em arquivos binários, como arquivos SWF ou PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* O `$main::search_content_type` é o cabeçalho Content-Type completo fornecido pelo servidor. Às vezes, ele pode conter um tipo MIME simples, como &quot;text/html&quot;. Ou pode conter um tipo MIME seguido de outras informações, como a codificação do conjunto de caracteres do documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento não HTML, `$main::search_content_type` pode tomar vários valores. Testar cada valor no script torna-se complicado. Por exemplo, alguns documentos do Word têm valores de tipo de conteúdo de &quot;aplicativo/senha&quot;, &quot;application/vnd.ms-word&quot; ou &quot;aplicativo/x-msword&quot;. Nesses casos, `$main::search_content_class` pode ter os seguintes valores:

   * html
   * pdf
   * palavra
   * excel
   * powerpoint
   * mp3
   * text

* No exemplo, testar `$main::search_content_class` para &quot;palavra&quot; corresponderia a qualquer um dos três valores de tipo de conteúdo possíveis.
* Se nada for impresso para STDOUT a partir do script de filtragem, o documento será usado exatamente como foi baixado. Ou seja, se você não precisar alterar nada em um documento, não precisará copiar STDIN para STDOUT para esse documento.
* Se quiser remover todo o texto de um documento, imprima um arquivo válido STDOUT. Por exemplo, para remover completamente todo o texto de um documento HTML, faça o seguinte: `print "<html></html>";`

## Adicionar um script de filtragem {#task_0AB84FD1133F47F9AA069A79BEA13A22}

O script de filtragem é um script Perl que é executado para cada documento baixado do site.

Você usa o script de filtragem juntamente com um script de inicialização, script de terminação e script de máscaras de URL.

Certifique-se de recriar o índice do site para que os resultados do script de filtragem estejam visíveis para os clientes.

Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para adicionar um script de filtragem**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Filtering Script]**.
1. (Opcional) Na página [!DNL Filtering Script], no campo [!DNL Test URL], insira o URL de um documento em seu site.

   Clique em uma opção de teste para ver as alterações no texto HTML bruto.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Campo URL de teste </p> </td> 
      <td colname="col2"> <p>Permite que você insira o URL de um documento em seu site. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Teste </p> </td> 
      <td colname="col2"> <p>Testa o URL em relação aos scripts de filtragem e máscaras de URL. </p> <p>O documento de URL de teste é baixado, que é usado como a entrada STDIN para o script de filtragem. Os scripts de inicialização, filtragem e terminação são executados. Se houver alguma saída STDOUT do script de filtragem, essa saída será exibida em uma nova janela do navegador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Testar somente </p> </td> 
      <td colname="col2"> <p>Testa somente a operação do script. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Visualizar </p> </td> 
      <td colname="col2"> <p>Permite que você visualize a página. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Vídeo completo </p> </td> 
      <td colname="col2"> <p>Gera uma visualização completa da tabela antes e depois dos documentos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Visual Curto </p> </td> 
      <td colname="col2"> <p>Mostra apenas as diferenças entre as exibições antes e depois. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Especialista (diff) </p> </td> 
      <td colname="col2"> <p>Exibe a saída bruta do comando GNU diff usado para comparar os arquivos, usando as opções de linha de comando fornecidas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Script de filtragem </p> </td> 
      <td colname="col2"> <p>Permite colar o script de filtragem no campo fornecido. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Salvar alterações </p> </td> 
      <td colname="col2"> <p>Salva o script de filtragem. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verificar sintaxe </p> </td> 
      <td colname="col2"> <p>Permite que você faça uma verificação rápida da sintaxe do script executando os scripts de inicialização, filtragem e término. Ele não atualiza e salva o script. </p> <p>Todos os erros e avisos do compilador Perl e todas as saídas STDERR são impressos. </p> <p>Antes que os efeitos do script fiquem visíveis para os clientes, você deve reconstruir o índice do site. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opções de linha de comando do diferencial de GNU**

   Algumas opções de diferencial de GNU que podem ser usadas no modo **[!UICONTROL Expert (diff)]** na página Script de filtragem preparada incluem:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção de linha de comando diff GNU </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
      <td colname="col2"> <p> Ignora alterações na quantidade de espaço em branco. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
      <td colname="col2"> <p> Ignora alterações que inserem ou excluem linhas em branco. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
      <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando três linhas de contexto. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> Linhas -C  </span> </p> </td> 
      <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando linhas (um número inteiro) de contexto ou três linhas se não forem fornecidas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
      <td colname="col2"> <p> Ignora alterações em caso de; considere letras maiúsculas e minúsculas equivalentes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
      <td colname="col2"> <p> Torna a saída semelhante a um script de ed, mas com alterações na ordem em que aparecem no arquivo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
      <td colname="col2"> <p> Gera diffs no formato RCS; como <span class="codeph"> -f </span> exceto que cada comando especifica o número de linhas afetadas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> Usa o formato de saída unificado, mostrando três linhas de contexto. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> Linhas -U  </span> </p> </td> 
      <td colname="col2"> <p> Usa o formato de saída unificado, mostrando linhas (um inteiro) de contexto ou três se linhas não forem fornecidas. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Test]** para testar os scripts de filtragem e as máscaras de URL.

   Clicar em **[!UICONTROL Test]** não atualiza e salva o script de filtragem.
1. No campo [!DNL Filtering Script], cole o script.
1. (Opcional) Clique em **[!UICONTROL Check Syntax]** para executar uma verificação rápida da sintaxe do script, executando os scripts de filtragem, inicialização e término.

   **[!UICONTROL Check Syntax]** não atualiza e salva o script.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Filtering Script] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre o script de inicialização {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

Você pode usar [!DNL Initialization Script] para alterar o conteúdo de um documento da Web antes que ele seja indexado.

Você pode inserir tags HTML, remover conteúdo irrelevante e até criar novos metadados HTML com base em URL de um documento, tipo MIME e conteúdo existente. O script de inicialização é um script Perl, que fornece manuseio poderoso de strings e flexibilidade de correspondência regular de expressões. Use o script de inicialização com um script de filtragem, script de terminação, script de máscara de URL e URL de teste.

O script de inicialização é executado uma vez antes do início da indexação. Use esse script para inicializar qualquer variável e sub-rotinas globais usadas pelo seu script de filtragem. Você pode usar o script de inicialização para imprimir mensagens de status do script de filtragem para o log de índice. Você pode imprimir as mensagens para STDERR ou por meio da sub-rotina `_search_debug_log()`.

Algumas opções de diferencial de GNU que podem ser usadas no modo **[!UICONTROL Expert (diff)]** na página Script de Inicialização Preparada incluem:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opção de diferencial GNU </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações na quantidade de espaço em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações que inserem ou excluem linhas em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando três linhas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Linhas -C  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando linhas (um número inteiro) de contexto ou três linhas se não forem fornecidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações em caso de; considere letras maiúsculas e minúsculas equivalentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Torna a saída semelhante a um script de ed, mas com alterações na ordem em que aparecem no arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> Gera diffs no formato RCS; como <span class="codeph"> -f </span> exceto que cada comando especifica o número de linhas afetadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída unificado, mostrando três linhas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Linhas -U  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída unificado, mostrando linhas (um inteiro) de contexto ou três se linhas não forem fornecidas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode usar variáveis locais, variáveis globais ou ambos nesses scripts. Todas as variáveis globais são precedidas pelo namespace &quot;main::&quot;. Quando o script de inicialização é iniciado, seu ambiente contém os seguintes identificadores de arquivo padrão:

* STDIN - nada (retorna imediatamente EOF quando lido)
* STDOUT - nada (se os dados forem impressos em STDOUT, serão descartados)
* STDERR - os dados impressos em STDERR são impressos no Log de Índice como um erro

Além disso, você pode gravar mensagens personalizadas no log de índice usando a sub-rotina `_search_debug_log()`, como no exemplo a seguir:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Essas mensagens são exibidas com a palavra `DEBUG` como um prefácio e não são registradas como erros.

Um exemplo de script de inicialização é o seguinte:

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

Consulte [Variáveis Globais](#global-variables)

### Dicas rápidas {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* Todas as variáveis globais são precedidas pelo namespace &quot;main:&quot;:: `$main::doc_count = 0;`
* Todas as variáveis locais são declaradas com &quot;my&quot;: `my $i = 0;`
* As sub-rotinas são definidas no script de inicialização. Eles não precisam de um namespace &quot;main::&quot; explícito: `sub my_sub {` `...`

   `}`

* Teste o `$main::search_content_type` antes de fazer alterações em um arquivo. O teste pode ajudá-lo a evitar alterações descuidadas em arquivos binários, como arquivos SWF ou PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* O `$main::search_content_type` é o cabeçalho Content-Type completo fornecido pelo servidor. Às vezes, ele pode conter um tipo MIME simples, como &quot;text/html&quot;. Ou pode conter um tipo MIME seguido de outras informações, como a codificação do conjunto de caracteres do documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento não HTML, `$main::search_content_type` pode tomar vários valores. Testar cada valor no script torna-se complicado. Por exemplo, alguns documentos do Word têm valores de tipo de conteúdo de &quot;aplicativo/senha&quot;, &quot;application/vnd.ms-word&quot; ou &quot;aplicativo/x-msword&quot;. Nesses casos, `$main::search_content_class` pode ter os seguintes valores:

   * html
   * pdf
   * palavra
   * excel
   * powerpoint
   * mp3
   * texto

* No exemplo, testar `$main::search_content_class` para &quot;palavra&quot; corresponderia a qualquer um dos três valores de tipo de conteúdo possíveis.
* Se nada for impresso para STDOUT a partir do script de filtragem, o documento será usado exatamente como foi baixado. Ou seja, se você não precisar alterar nada em um documento, não precisará copiar STDIN para STDOUT para esse documento.
* Se quiser remover todo o texto de um documento, imprima um arquivo válido STDOUT. Por exemplo, para remover completamente todo o texto de um documento HTML, faça o seguinte: `print "<html></html>";`

## Adicionar um script de inicialização {#task_5A03B8D0C46E4674B7CE88203515803B}

O script de inicialização é um script Perl que é executado uma vez antes que qualquer documento seja indexado.

Você usa o script de inicialização juntamente com um script de filtragem, script de terminação e script de máscaras de URL.

Certifique-se de recriar o índice do site para que os resultados do script de inicialização fiquem visíveis para os clientes.

Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para adicionar um script de inicialização**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Initialization Script]**.
1. (Opcional) Na página [!DNL Initialization Script], no campo [!DNL Test URL], insira o URL de um documento em seu site.

   Clique em uma opção de teste para ver as alterações no texto HTML bruto.

   Consulte a tabela de opções de filtragem em **Adição de um script de filtragem**.

   Clique em **[!UICONTROL Test]** para testar os scripts de filtragem e as máscaras de URL.

   Clicar em **[!UICONTROL Test]** não atualiza e salva o script de inicialização.
1. No campo [!DNL Initialization Script], cole o script.
1. (Opcional) Clique em **[!UICONTROL Check Syntax]** para executar uma verificação rápida da sintaxe do script, executando os scripts de filtragem, inicialização e término.

   **[!UICONTROL Check Syntax]** não atualiza e salva o script.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Initialization Script] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre o script de terminação {#concept_AAD6B3B0E7124874AD0947096FC42F47}

Você pode usar [!DNL Termination Script] para alterar o conteúdo de um documento da Web antes que ele seja indexado.

Você pode inserir tags HTML, remover conteúdo irrelevante e até criar novos metadados HTML com base em URL de um documento, tipo MIME e conteúdo existente. O script de inicialização é um script Perl, que fornece manuseio poderoso de strings e flexibilidade de correspondência regular de expressões. Use o script de terminação com um script de inicialização, script de filtragem, script de terminação, script de máscaras de URL e URL de teste.

O script de finalização é executado uma vez depois que todos os documentos são indexados. Você pode usar o script de terminação para imprimir mensagens de status do script de filtragem para o log de índice. Você pode imprimir as mensagens para STDERR ou por meio da sub-rotina `_search_debug_log()`.

Algumas opções de linha de comando de diferencial de GNU que podem ser usadas no modo **[!UICONTROL Expert (diff)]** na página Script de Terminação Preparada incluem o seguinte:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opção de linha de comando diff GNU </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações na quantidade de espaço em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações que inserem ou excluem linhas em branco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando três linhas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Linhas -C  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída do contexto, mostrando linhas (um número inteiro) de contexto ou três linhas se não forem fornecidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> Ignora alterações em caso de; considere letras maiúsculas e minúsculas equivalentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Torna a saída semelhante a um script de ed, mas com alterações na ordem em que aparecem no arquivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> Gera diffs no formato RCS; como <span class="codeph"> -f </span> exceto que cada comando especifica o número de linhas afetadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída unificado, mostrando três linhas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Linhas -U  </span> </p> </td> 
   <td colname="col2"> <p> Usa o formato de saída unificado, mostrando linhas (um inteiro) de contexto ou três se linhas não forem fornecidas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode usar variáveis locais, variáveis globais ou ambos nesses scripts. Todas as variáveis globais são precedidas pelo namespace &quot;main::&quot;. Quando o script de terminação é iniciado, seu ambiente contém os seguintes identificadores de arquivo padrão:

* STDIN - nada (retorna imediatamente EOF quando lido)
* STDOUT - nada (se os dados forem impressos em STDOUT, serão descartados)
* STDERR - os dados impressos em STDERR são impressos no log de índice como um erro

Além disso, você pode gravar mensagens personalizadas no log de índice usando a sub-rotina `_search_debug_log()`, como no exemplo a seguir:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Essas mensagens são exibidas com a palavra `DEBUG` como um prefácio e não são registradas como erros.

Para exibir o número de documentos que foram processados pelo script de filtragem como uma linha de erro no log de índice, você pode usar o seguinte script de terminação:

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

Consulte [Variáveis Globais](#global-variables)

### Dicas rápidas {#section_5790EA7ACAC046CBA01F759F88E2460F}

* Todas as variáveis globais são precedidas pelo namespace &quot;main:&quot;:: `$main::doc_count = 0;`
* Todas as variáveis locais são declaradas com &quot;my&quot;: `my $i = 0;`
* As sub-rotinas são definidas no script de inicialização. Eles não precisam de um namespace &quot;main::&quot; explícito: `sub my_sub {` `...`

   `}`

* Teste o `$main::search_content_type` antes de fazer alterações em um arquivo. O teste pode ajudá-lo a evitar alterações descuidadas em arquivos binários, como arquivos SWF ou PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* O `$main::search_content_type` é o cabeçalho Content-Type completo fornecido pelo servidor. Às vezes, ele pode conter um tipo MIME simples, como &quot;text/html&quot;. Ou pode conter um tipo MIME seguido de outras informações, como a codificação do conjunto de caracteres do documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento não HTML, `$main::search_content_type` pode tomar vários valores. Testar cada valor no script torna-se complicado. Por exemplo, alguns documentos do Word têm valores de tipo de conteúdo de &quot;aplicativo/senha&quot;, &quot;application/vnd.ms-word&quot; ou &quot;aplicativo/x-msword&quot;. Nesses casos, `$main::search_content_class` pode ter os seguintes valores:

   * html
   * pdf
   * palavra
   * excel
   * powerpoint
   * mp3
   * texto

* No exemplo, testar `$main::search_content_class` para &quot;palavra&quot; corresponderia a qualquer um dos três valores de tipo de conteúdo possíveis.
* Se nada for impresso para STDOUT a partir do script de filtragem, o documento será usado exatamente como foi baixado. Ou seja, se você não precisar alterar nada em um documento, não precisará copiar STDIN para STDOUT para esse documento.
* Se quiser remover todo o texto de um documento, imprima um arquivo válido STDOUT. Por exemplo, para remover completamente todo o texto de um documento HTML, faça o seguinte: `print "<html></html>";`

## Adicionar um script de terminação {#task_F0CFB412871642CFBC88132889C5B6F9}

O script de terminação é um script Perl que é executado uma vez depois que todos os documentos são indexados.

Você usa o script de terminação juntamente com um script de filtragem, script de terminação e script de máscaras de URL.

Certifique-se de recriar o índice do site para que os resultados do script de inicialização fiquem visíveis para os clientes.

Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para adicionar um script de terminação**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Termination Script]**.
1. (Opcional) Na página [!DNL Termination Script], no campo [!DNL Test URL], insira o URL de um documento em seu site.

   Clique em uma opção de teste para ver as alterações no texto HTML bruto.

   Consulte a tabela de opções de filtragem em **Adição de um script de filtragem**.

   Clique em **[!UICONTROL Test]** para testar os scripts de filtragem e as máscaras de URL.

   Clicar em **[!UICONTROL Test]** não atualiza e salva seu script de terminação.
1. No campo [!DNL Termination Script], cole o script.
1. (Opcional) Clique em **[!UICONTROL Check Syntax]** para executar uma verificação rápida da sintaxe do script, executando os scripts de inicialização, filtragem e término.

   **[!UICONTROL Check Syntax]** não atualiza e salva o script.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Termination Script] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre o script de máscaras de URL {#concept_384F32EA18F84853A7BA99A04009330B}

Com a filtragem, você pode alterar o conteúdo de um documento da Web antes de ele ser indexado. Você pode inserir tags HTML, remover conteúdo irrelevante e até criar novos metadados HTML com base em URL de um documento, tipo MIME e conteúdo existente. O script de máscaras de URL é um script Perl que fornece manuseio poderoso de strings e flexibilidade de correspondência regular de expressões.

Para alterar o conteúdo dos documentos que existem apenas em uma porção específica do site, você pode especificar incluir máscaras de URL, excluir máscaras de URL, ou ambas, para definir as páginas apropriadas.

Se quiser alterar apenas os documentos em `"https://www.mysite.com/faqs/"`, poderá usar o seguinte conjunto de máscaras:

```
include https://www.mysite.com/faqs/ 
exclude *
```

Também é possível usar a expressão regular em um script de máscara de URL, como no exemplo a seguir:

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

Consulte [Expressões regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

As máscaras de URL com script são consideradas na ordem em que foram inseridas no campo [!DNL URL Masks]. Quando um URL de documento corresponde a uma máscara, esse documento é incluído ou excluído com base no tipo de máscara. Se o URL de um documento não corresponder a nenhuma máscara de URL, o documento será incluído somente se seu tipo MIME for &quot;text/html&quot;. Todos os outros tipos MIME são excluídos.

## Adicionar um script de máscara de URL {#task_D18F2A496C1C45C997B5DA650AAF5D59}

Especifique as máscaras de inclusão e de exclusão de URL para alterar o conteúdo dos documentos que existem apenas em uma porção específica do site.

Antes que os efeitos das configurações de Máscaras de URL fiquem visíveis para os visitantes, recrie o índice do site.

**Para adicionar um script de máscara de URL**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL URL Masks]**.
1. (Opcional) Na página [!DNL URL Masks] , no campo [!DNL Test URL] , insira um URL de um documento em seu site e clique em **[!UICONTROL Test]** para testar o URL em relação aos scripts e máscaras de filtragem.

   O documento de URL de teste é baixado, que é usado como a entrada STDIN para o script de filtragem. Em seguida, os scripts de filtragem, inicialização e terminação são executados. Se houver alguma saída STDOUT do script de filtragem que a saída é exibida em uma nova janela do navegador.

   Clicar em **[!UICONTROL Test]** não atualiza e salva o script.
1. No campo [!DNL URL Masks], insira uma máscara de URL por linha.
1. (Opcional) Clique em **[!UICONTROL Check Syntax]** para executar uma verificação rápida da sintaxe de suas máscaras de URL executando os scripts de filtragem, inicialização e término.

   **[!UICONTROL Check Syntax]** não atualiza e salva o script.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL URL Masks] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre os tipos de conteúdo na filtragem {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

Permite selecionar quais tipos de conteúdo você deseja filtrar para esta conta.

O texto encontrado nos tipos de conteúdo selecionados é convertido em HTML e, em seguida, processado usando o script especificado em Filtering Script.

Consulte [Sobre o script de filtragem](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

Os Tipos de conteúdo que você pode selecionar incluem:

* documentos PDF
* Documentos em texto
* Filmes sobre Flash Adobe
* Arquivos do Microsoft Word
* Arquivos do Microsoft Office (OpenXML)
* Arquivos do Microsoft Excel
* Arquivos do Microsoft Powerpoint
* Texto em arquivos de música MP3

Antes que os efeitos das configurações de Tipos de conteúdo ou alterações nas configurações sejam visíveis para os clientes, você deve recriar o índice do site.

## Selecionar os tipos de conteúdo que são filtrados {#task_C46081FA425A43EC8FDE6EA4A52A170A}

Selecione os tipos de conteúdo que você deseja passar para o script especificado em Filtering Script.

Consulte [Sobre o script de filtragem](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

**Para selecionar os tipos de conteúdo filtrados**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Content Types]**.
1. Na página [!DNL Content Types], verifique os tipos de conteúdo que deseja passar para o script de filtro.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Content Types] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
