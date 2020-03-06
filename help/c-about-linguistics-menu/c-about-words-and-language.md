---
description: Você pode usar Palavras e idiomas para determinar como os termos de pesquisa são correspondidos ao conteúdo de suas páginas da Web.
seo-description: Você pode usar Palavras e idiomas para determinar como os termos de pesquisa são correspondidos ao conteúdo de suas páginas da Web.
seo-title: Sobre Palavras e Idioma
solution: Target
title: Sobre Palavras e Idioma
topic: Linguistics,Site search and merchandising
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Sobre Palavras e Idioma{#about-words-language}

Você pode usar [!DNL Words & Language] para determinar como os termos de pesquisa são correspondidos ao conteúdo das páginas da Web.

## Uso de palavras e idiomas {#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

Antes de os efeitos das [!DNL Words & Language] configurações estarem disponíveis para os visitantes do site, incluindo quaisquer alterações feitas nessas configurações, você deve gerar novamente o índice do site. A regeneração, diferentemente da indexação, não envolve o rastreamento de páginas da Web e leva apenas alguns segundos.

## Configurar a correspondência entre os termos de pesquisa e o conteúdo da Web {#task_351A9144A51F4B41923BDBACDEF3B616}

Você pode usar Palavras e idiomas para determinar como a pesquisa/comercialização do site corresponde os termos de pesquisa ao conteúdo de suas páginas da Web.

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**Para configurar a correspondência dos termos de pesquisa com o conteúdo da Web**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**.
1. Na [!DNL Words & Languages] página, defina as opções desejadas.

   <!-- 
   
   r_words_and_languages_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Uso de maiúsculas e minúsculas </p> </td> 
      <td colname="col2"> <p>Não selecionado por padrão. </p> <p>Determina se letras maiúsculas são diferenciadas das letras minúsculas. Por exemplo, quando selecionado, "Êxito" é diferenciado de "bem-sucedido", e os resultados da pesquisa podem variar entre os dois. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sensibilidade diacrítica </p> </td> 
      <td colname="col2"> <p>Selecionado por padrão. </p> <p> Determina se as palavras que contêm caracteres diacríticos são distintas das palavras que não o fazem. Por exemplo, quando selecionada, a "pagina" é destacada do "início". Desmarque essa opção se você tiver um site que use idiomas diferentes do inglês. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Números </p> </td> 
      <td colname="col2"> <p>Selecionado por padrão. </p> <p>Determina se as palavras que contêm dígitos são indexadas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorar apóstrofos </p> </td> 
      <td colname="col2"> <p>Não selecionado por padrão. </p> <p>Os apóstrofos são removidos das consultas. Por exemplo, uma pesquisa por "Árvores" retornaria os mesmos resultados que uma pesquisa por "Árvores". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorar hífens </p> </td> 
      <td colname="col2"> <p>Não selecionado por padrão. </p> <p>Os hífens são removidos das consultas. Por exemplo, uma busca por "sinal azul" retornaria os mesmos resultados que uma busca por "bluebell". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Correspondência alfanumérica parcial </p> </td> 
      <td colname="col2"> <p>Não selecionado por padrão. </p> <p>Quando selecionada, essa opção permite dividir tokens em transições alfabéticas-numéricas para permitir correspondências de texto livre em tokens de parte ou de produto. </p> <p>Por exemplo, suponha que você tenha um identificador de produto de <span class="codeph"> 910XT </span> no conteúdo do corpo de uma ou mais páginas em um site. Quando essa opção <i>não</i> está selecionada, o <span class="keyword"> Adobe Search&amp;Promote </span> encontra correspondências para esse identificador de produto ao pesquisar por <span class="codeph"> 910XT </span>. Além disso, com <span class="uicontrol"> a opção Pesquisar Concat-Div-Enable </span> ativada, o <span class="keyword"> Adobe Search&amp;Promote </span> também encontraria <span class="codeph"> 910 XT </span>. No entanto, não encontraria casos de <span class="codeph"> 910 </span> ou <span class="codeph"> XT </span> exclusivamente. </p> <p>Quando você seleciona Correspondência alfanumérica <span class="uicontrol"> parcial </span>, o indexador divide esses tokens alfanuméricos mistos em vários tokens. Por exemplo, um identificador de produto como <span class="codeph"> XYZ123 </span> é indexado em três tokens: <span class="codeph"> XYZ123 </span>, <span class="codeph"> XYZ </span>, e <span class="codeph"> 123 </span>. Essa funcionalidade permite a correspondência de texto livre em tempo de pesquisa em qualquer uma dessas variantes. </p> <p>Em outro exemplo, suponha que você tenha o identificador de produto <span class="codeph"> AB910XT </span>. Se você selecionar Correspondência alfanumérica Parcial <span class="uicontrol"> e </span> a opção <i>Pesquisar Concat-Div-Enable</i> estiver ativada, o <span class="uicontrol"> Adobe Search&amp;Promote o </span> indexará como <span class="keyword"> AB910XT </span> <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span>,  AB, 910,  e XT. Em seguida, quando um usuário pesquisa por <span class="codeph"> 910XT </span>, por exemplo, a pesquisa é expandida para também localizar instâncias de <span class="codeph"> 910XT </span>, <span class="codeph"> 910 </span>ou <span class="codeph"> XT </span>. </p> <p> <p>Observação:  Por padrão, a opção <span class="uicontrol"> Pesquisar Concat-Div-Enable não </span> está ativada. Entre em contato com o suporte técnico para ativar o recurso para uso. </p> </p> <p> <p>Observação:  A Correspondência alfanumérica <span class="uicontrol"> parcial </span> é aplicada globalmente a todos os campos indexados. No entanto, afeta apenas a correspondência de texto livre; não afeta a correspondência exata nem a correspondência de intervalo. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Correspondência semelhante a som </p> </td> 
      <td colname="col2"> <p>Selecionado por padrão. </p> <p>Palavras que soam iguais são correspondidas como "saúde" e "saúde". Esse recurso permite que o cliente pesquise facilmente, apesar de uma palavra ter sido escrita incorretamente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formulários do Word Alternativo </p> </td> 
      <td colname="col2"> <p>O padrão é Formulários <b>do Word alternativos</b>padrão. </p> <p>É possível selecionar uma das seguintes opções na lista suspensa Formulários do Word alternativos: 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>None</b> <p>Nenhuma forma de texto de origem ou alternativa é aplicada durante a indexação. </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>Formulários do Word Alternativo Padrão</b> <p>A depuração é feita automaticamente durante a indexação. </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>Dicionário de domínio</b> <p>Qualquer dicionário de domínio definido como um dicionário de origem é usado como uma fonte de formulários de palavras alternativas. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> Sobre dicionários </a>. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> Configurar um dicionário como um dicionário de origem </a>. </p> </li> 
      </ul> </p> <p>Se a origem de frases estiver ativada no <span class="keyword"> Adobe Search&amp;Promote </span>, esteja ciente de que formulários de palavras alternativas também ocorrem dentro de frases. </p> <p>Consulte <a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Search&amp;Promote 8.15.0 Release Notes (19/6/2014) </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Idioma  </p> </td> 
      <td colname="col2"> <p>O padrão é <b>inglês (Estados Unidos)</b>. </p> <p>O idioma selecionado garante que os valores numéricos e de data sejam analisados de acordo com as convenções usadas na parte selecionada do mundo. </p> <p>Quando <span class="uicontrol"> Formulários do Word alternativos </span> estiver definido como <span class="uicontrol"> Padrão de formulários do Word alternativos </span> ou como <span class="uicontrol"> </span>Dicionário de domínio, os formulários do Word e as terminações do texto serão alterados de acordo com as regras linguísticas do idioma selecionado. </p> <p>Por padrão, a configuração Idioma não é usada para determinar o idioma das páginas lidas do site. O idioma de uma página de leitura é determinado a partir de seus cabeçalhos HTTP ou de métricas dentro da própria página. Seu site pode conter páginas em vários idiomas diferentes. Cada página é lida e indexada corretamente, independentemente do idioma selecionado aqui. </p> <p>Se você usar uma codificação de conjunto de caracteres Unicode, como UTF-8, para algumas páginas do seu site, certifique-se de que o idioma de cada uma dessas páginas esteja especificado corretamente. Se os cabeçalhos HTTP ou as métricas apropriadas não existirem para seus documentos Unicode, você poderá usar <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Injeções </span> para especificar o idioma apropriado. </p> <p>Marque <span class="uicontrol"> Aplicar a documentos sem idioma especificado? </span> para usar a configuração Idioma para páginas lidas de seu site que não têm configuração explícita. Use essa configuração quando apenas <i>alguns</i> documentos não tiverem configurações de idioma. Use <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Injeções </span> se <i>nenhum</i> dos seus documentos tiver configurações de idioma ou se o conjunto de documentos afetados for uma lista bem conhecida e gerenciável pequena. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> Sobre Injeções </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Usar Decompounder? </p> </td> 
      <td colname="col2"> <p> <p>Observação:  Este recurso é usado apenas para dinamarquês e alemão. Além disso, esse recurso não é ativado por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso. Depois de habilitado, o Decompounder <b>Usar?</b> só será exibida na interface do usuário se você selecionar <span class="uicontrol"> dinamarquês </span> ou <span class="uicontrol"> alemão </span> na lista suspensa <span class="uicontrol"> Idioma </span> descrita anteriormente nesta tabela. </p> </p> <p>Quando você seleciona <span class="uicontrol"> Usar decompounder? </span>, o serviço detalha as palavras compostas em dinamarquês ou alemão, que permitem a indexação de palavras do componente junto com as palavras compostas originais. </p> <p>Para ver como esse recurso funciona, insira palavras no campo de texto e clique em <span class="uicontrol"> Testar </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Settings]**.
1. Para visualizar os resultados de suas alterações, clique em **[!UICONTROL regenerate your staged site index]** para recriar o índice de site preparado.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

