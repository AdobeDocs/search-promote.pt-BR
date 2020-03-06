---
description: 'null'
seo-description: 'null'
seo-title: Perguntas frequentes
solution: Target
title: Perguntas frequentes
topic: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
translation-type: tm+mt
source-git-commit: 4270ea66ba645ad0f71c9c8b5c2a1fcc6eb02ad2

---


# Perguntas frequentes{#frequently-asked-questions}

## Adobe Flash {#reference_4A25BBDE32214AF5A1A454F38FD51243}

Uma página de perguntas frequentes que discute o suporte à indexação e pesquisa de arquivos SWF em um site.

Veja a seguir perguntas comuns sobre arquivos SWF:

* [Quando um arquivo SWF é rastreado e indexado?](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [O que tenho que fazer para indexar um SWF...](#section_0A6A52CC70D4495BBE14D91906318F95)
* [Como os arquivos SWF são reconhecidos?](#section_B36C0536AB544F509601DC6A11A8E656)
* [Como os arquivos SWF são indexados?](#section_36856058A4B54FA5ABF921344F50410C)
* [Um arquivo SWF conta como uma página?](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [Como impedir a indexação de arquivos SWF individuais...](#section_E38AD37989EF410B97AF5125057BFD22)
* [Como impedir que arquivos SWF sejam indexados em...](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [Por que não posso pesquisar os arquivos SWF chineses, japoneses ou coreanos no meu site?](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## Quando um arquivo SWF é rastreado e indexado? {#section_01BB5259140D4D5FB04CCB7A1A63DE99}

Um arquivo SWF será rastreado e indexado se estiver contido em uma tag embed ou object em uma página HTML, como no exemplo a seguir:

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

Um arquivo SWF também é reconhecido se você listar o URL do arquivo como um ponto de entrada.

Consulte [Adicionar vários pontos de entrada de URL que você deseja indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## O que devo fazer para indexar um arquivo SWF? {#section_0A6A52CC70D4495BBE14D91906318F95}

Para rastrear e indexar arquivos SWF, selecione o tipo de conteúdo **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Desde que seu arquivo Flash seja referenciado de uma `<embed>` tag ou de uma `<object>` tag em um documento HTML, o texto será indexado e todos os URLs listados no arquivo serão rastreados.

Se o arquivo não for referenciado por uma `<embed>` tag ou por uma `<object>` tag, você poderá listar o arquivo SWF em uma `<a href=...>` tag em um documento HTML ou como um ponto de entrada de URL.

Consulte [Adicionar vários pontos de entrada de URL que você deseja indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Como os arquivos SWF são reconhecidos? {#section_B36C0536AB544F509601DC6A11A8E656}

Os arquivos SWF são identificados pelo seguinte tipo MIME:

`application/x-shockwave-flash`

Os arquivos SWF também são reconhecidos com os tipos `application/octet-stream`&quot; ou `text/plain` MIME, desde que a extensão do arquivo seja .swf.

Um servidor configurado incorretamente pode usar um tipo MIME diferente para arquivos SWF. Verifique a configuração do servidor se tiver problemas ao rastrear e indexar arquivos SWF.

## Como os arquivos SWF são indexados? {#section_36856058A4B54FA5ABF921344F50410C}

O texto contido em um arquivo SWF é indexado como se fosse `<body>` texto na página HTML anexada. Se um resultado de pesquisa encontrar o texto contido em um arquivo SWF incorporado, o resultado na verdade será vinculado à página HTML circundante e não ao arquivo SWF. Dessa forma, o arquivo SWF é exibido no contexto correto.

Se um arquivo SWF contiver um URL como uma ação &quot;Carregar filme&quot;, o texto no arquivo SWF referenciado será indexado como parte da página HTML circundante.

Se um arquivo SWF contiver um URL como uma ação &quot;Obter URL&quot;, o URL será rastreado e indexado posteriormente, exatamente como uma referência HTML é rastreada e indexada posteriormente. `<a href=...>`

Se um arquivo SWF estiver listado como um ponto de entrada de URL, o texto do arquivo SWF será indexado como uma única página. Um resultado de pesquisa que encontra texto de um SWF de ponto de entrada vincula diretamente ao filme, não a uma página HTML de inclusão.

Consulte [Adicionar vários pontos de entrada de URL que você deseja indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Um arquivo SWF conta como uma página? {#section_0158D6DE70BC40D78E2374787B9F58AB}

Não. Um arquivo SWF é considerado parte de sua página HTML de inclusão. Todos os URLs &quot;Carregar filme&quot; contidos em arquivos SWF também são considerados parte da página HTML de inclusão. Portanto, os arquivos SWF referenciados em uma página HTML não contam como uma &quot;página&quot; para o total de páginas da conta.

Se um arquivo SWF estiver listado como um ponto de entrada de URL, esse arquivo SWF e todos os URLs &quot;Carregar filme&quot; listados nesse arquivo SWF serão contados como uma &quot;página&quot; para o total de páginas da conta.

## Como impedir a indexação de arquivos SWF individuais? {#section_E38AD37989EF410B97AF5125057BFD22}

Para impedir a indexação de um arquivo SWF, é possível adicionar uma tag meta ( `<meta name="ROBOTS" content="NOINDEX">`) ou uma `<noindex>` tag do robô ao documento HTML circundante. Ou seja, o documento que contém a tag `<embed>` ou `<object>` .

Você também pode usar a meta tag ( `<meta name="ROBOTS" content="NOFOLLOW">`) dos robôs para impedir os seguintes URLs contidos no arquivo SWF. Se o documento HTML anexado tiver sido desabilitado, os URLs listados como ações &quot;Obter URL&quot; no arquivo SWF não serão seguidos.

## Como impedir que arquivos SWF sejam indexados no meu site? {#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

Para desativar a indexação SWF, desmarque o tipo de conteúdo **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Você também pode optar por usar [!DNL URL Masks] para desativar a indexação de arquivos SWF.

Consulte [Adicionar máscaras de URL para indexar ou não indexar partes de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Para desativar a indexação SWF, insira uma das seguintes máscaras de URL:

* `exclude *.swf` (se você não estiver usando expressões regulares)
* `exclude regexp ^.*\.swf$` (se você estiver usando expressões regulares)

Consulte Expressões [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Por que não posso pesquisar os arquivos SWF chineses, japoneses ou coreanos no meu site? {#section_EE1A3A705AE74148BD195A0CE513A5C4}

A pesquisa/comercialização do site obtém UTF-8 de arquivos SWF criados com o Adobe Flash. O UTF-8 não contém nenhuma indicação de idioma. Se você selecionou o tipo de conteúdo **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o idioma usado pelo arquivo SWF.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

Arquivos SWF antigos também não especificam um conjunto de caracteres. Se você selecionou o tipo de conteúdo SWF **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o conjunto de caracteres usado no arquivo SWF.

## Pesquisa geral {#reference_E2C675162789452A9B99C6633B12CBEF}

Uma página de perguntas frequentes que discute como a pesquisa/comercialização do site ajuda os clientes que visitam seu site a encontrar o que estão procurando.

Veja a seguir perguntas comuns sobre a pesquisa geral:

* [Preciso instalar qualquer software para usar o site...](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [O que acontece quando meu site excede o limite de página?](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [Como faço para alterar o endereço de e-mail onde a mensagem semanal..](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [Qual é a segurança das informações do meu cliente na pesquisa/comercialização do site?](#section_5484CB954167412BB7F0480CB0C504B8)
* [E quanto à privacidade das informações do meu cliente?](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [Posso mostrar meus próprios anúncios de banner na busca...](#section_611EB8B32C16418386CB7DC7FB6954B8)

Veja a seguir algumas perguntas comuns sobre os recursos de pesquisa:

* [Posso personalizar os resultados da pesquisa para o meu site?](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [Posso ver o que os clientes estão procurando no meu...](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [Como posso controlar quais tipos de conteúdo (PDF, texto, Flash, MP3 e Microsoft Office) são indexados e pesquisados?](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [As páginas da Web geradas dinamicamente por meio de conteúdo baseado em ASP, JSP, PHP, CFM ou Perl são suportadas?](#section_E279F004F1C542A2B9773B832E7B013F)
* [Como posso usar sinônimos para melhorar os resultados da pesquisa...](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [Tenho controle sobre a ordem dos resultados da pesquisa...](#section_C6361048502745779D9749A842C4C370)
* [Posso alterar o idioma da página de resultados da pesquisa...](#section_6EE41DA8241247D48BBEB061A50599C5)
* [Posso ter mais de um site em meu Adobe...](#section_AFA8825182094660A71EEC84B8329D6D)
* [Posso pesquisar mais de um domínio?](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [Posso subdividir meu site em seções separadas para que...](#section_52153A9DE9F9493B967A70583848B2A4)
* [Como eu excluo partes do meu site de ser...](#section_D452EDE153654EF398F4A87780C6D43B)
* [Quais conjuntos de caracteres são suportados?](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [E se eu alterar ou atualizar meu site?](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [Meu site pode ser indexado automaticamente?](#section_9C7D41636238488691ECDFEE4D4E5103)
* [Eu uso senhas em meu site. Ainda posso usar a pesquisa/comercialização do site?](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [Você suporta o rastreamento e a indexação de https ou...](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [A pesquisa/comercialização do site honra o arquivo robots.txt do meu site?](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [Certas partes do meu site devem ser atualizadas com frequência para que...](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [Posso usar scripts ou programas para iniciar um incremento...](#section_0B6BB039557A42AA876D35D748E17DD0)

## Preciso instalar algum software para usar a pesquisa/comercialização do site? {#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

Não. Essa é a principal vantagem da pesquisa/comercialização do site. O mecanismo é um aplicativo profissional hospedado e mantido inteiramente em nossos servidores de alto desempenho. Isso torna o software mais fácil de usar do que outras soluções de pesquisa. A única coisa que você precisa fazer é adicionar uma pequena quantidade de código HTML às suas páginas para que os clientes do seu site possam inserir pesquisas. A pesquisa/comercialização do site cuida de todo o resto.

## O que acontece quando meu site excede o limite de página? {#section_ECA5FA01032D4322BABA4E2C7FE498C1}

Continuamos servindo suas pesquisas para que seus visitantes possam pesquisar em seu site sem interrupção. Para ver se o site excede o limite de página, reveja o status do Índice Completo ou do Log ao Vivo.

Consulte [Sobre o Índice](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3)Completo.

Consulte [Visualizando o log de índice completo de um ativo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

## Como faço para alterar o endereço de email para o qual os relatórios semanais são enviados? {#section_AE27F63DD13F425B940C8E7D9ED5C614}

Relatórios semanais são enviados ao proprietário de cada conta ativa. Você pode alterar o endereço de email clicando em **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**. Se você tiver mais de uma conta de pesquisa ativa, todos os boletins serão enviados para o novo endereço.

Consulte [Configuração das informações](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)pessoais do usuário.

## Qual é a segurança das informações do meu cliente na pesquisa/comercialização do site? {#section_5484CB954167412BB7F0480CB0C504B8}

A pesquisa/comercialização do site é segura, rápida, estável e fácil de usar. Você não é forçado a usar cookies (embora possa usá-los se desejar) para usar nossos produtos, e as informações confidenciais, como senhas, nunca são colocadas em qualquer link de URL que possa ser recuperado posteriormente do seu navegador.

## E quanto à privacidade das informações do meu cliente? {#section_8FB493F15E51454BA92A0C83E14C0CC7}

A Adobe está comprometida em honrar a privacidade de seus clientes e visitantes. Consulte o Centro [de](https://www.adobe.com/privacy.html)privacidade da Adobe.

## Posso mostrar meus próprios anúncios de banner nas páginas de resultados da pesquisa? {#section_611EB8B32C16418386CB7DC7FB6954B8}

Sim. Você controla a aparência e o conteúdo dos resultados da pesquisa. No modelo de resultados da pesquisa para seu site, você pode criar links para sua própria rede de troca de banners, como LinkExchange ou SmartClicks. Todas as ocorrências feitas pelos seus visitantes são creditadas corretamente na sua conta de troca de banner.

## Posso personalizar os resultados da pesquisa para o meu site? {#section_A64B3A621B794DF78D35ED06D9C43D0B}

Sim. Este é um recurso exclusivo de pesquisa/comercialização do site. Com nossa avançada tecnologia de modelo e um pouco de conhecimento em HTML, você pode controlar exatamente como os resultados da pesquisa aparecem.

Consulte [Pesquisar marcas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modelo.

A transição entre seus próprios servidores e os servidores de pesquisa/comercialização do site é totalmente ininterrupta e invisível para seus clientes. Se você não souber HTML ou se não tiver tempo para criar um modelo personalizado, poderá escolher entre uma variedade de modelos atraentes e prontos para uso criados pela equipe interna de desenvolvedores da Web profissionais da Adobe.

## Posso ver o que os clientes estão procurando no meu site? {#section_73709E1B0E82478DA7B4D15B6C845F33}

Sim. Mantemos estatísticas de pesquisa para pesquisas feitas por visitantes em seu site nos últimos dois meses. Você pode revisar essas estatísticas a qualquer momento em Relatórios no menu do produto. Os relatórios de pesquisa fornecem informações vitais sobre exatamente o que os visitantes estão procurando em seu site. Você pode usar essas informações para melhorar o design ou para ajustar o mecanismo de pesquisa/comercialização do site para melhor servir aos seus visitantes.

## Como posso controlar quais tipos de conteúdo (PDF, texto, Flash, MP3 e Microsoft Office) são indexados e pesquisados? {#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

Você pode configurar facilmente contas para ativar ou desativar a indexação e a pesquisa de texto encontrado em documentos PDF, documentos de texto simples, filmes Flash, arquivos MP3 ou documentos do Microsoft Office.

Essas configurações são controladas na [!DNL Staged Content Types] página.

Consulte [Sobre tipos](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de conteúdo.

## As páginas da Web geradas dinamicamente por meio de conteúdo baseado em ASP, JSP, PHP, CFM ou Perl são suportadas? {#section_E279F004F1C542A2B9773B832E7B013F}

As páginas da Web HTML estáticas ou geradas dinamicamente são indexadas, incluindo páginas criadas a partir de bancos de dados ou qualquer outro processo back-end. Como o código HTML que um navegador vê é indexado, você pode usar a pesquisa/comercialização do site em sites, desde que essas arquiteturas de back-end resultem em páginas HTML.

O robô de pesquisa rastreia seu site começando pela primeira página no endereço do site especificado em [!DNL Account Settings]e segue links de página para página.

Consulte [Definição das configurações](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)da sua conta.

Quando o robô de pesquisa rastreia e indexa todas as páginas do site, você pode usar o mecanismo de pesquisa para pesquisar no site. Em outras palavras, se documentos gerados dinamicamente forem inseridos em seu site com links de outras páginas, o robô de pesquisa ainda poderá rastrear e indexar o conteúdo dinâmico.

Depois que o conteúdo do site é rastreado e indexado, os clientes do site podem pesquisar informações dentro do conteúdo indexado.

## Como posso usar sinônimos para melhorar os resultados da pesquisa do meu site? {#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

Você pode usar sinônimos quando quiser que os visitantes localizem páginas relacionadas à consulta de pesquisa deles.

Por exemplo, suponha que você tenha uma página que contenha uma lista de preços de produtos para venda em seu site. No entanto, após examinar os relatórios de pesquisa fornecidos pela pesquisa/comercialização do site, você verá que os clientes estão procurando a palavra &quot;custo&quot;, &quot;despesa&quot;, &quot;encargo&quot; ou &quot;taxa&quot; em suas pesquisas. Essas palavras não exibem sua página de lista de preços nos resultados da pesquisa. Com o [!DNL Add Synonyms] recurso em [!DNL Dictionaries], você pode especificar que essas palavras sejam sinônimos, e seu cliente pode encontrar sua lista de preços, independentemente do termo de pesquisa que usarem.

Consulte [Sobre dicionários](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034).

## Tenho controle sobre a ordenação dos resultados da pesquisa? {#section_C6361048502745779D9749A842C4C370}

Sim. Usando a interface de relevância avançada, você pode controlar quais páginas são retornadas para uma consulta de pesquisa específica. Esse recurso é útil se você quiser ter certeza de que os clientes verão uma página específica ao consultar determinadas palavras.

Consulte [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.

## Posso alterar o idioma da página de resultados da pesquisa? {#section_6EE41DA8241247D48BBEB061A50599C5}

Sim. O modelo de pesquisa/comercialização do site é flexível quando se trata de permitir que você construa uma página de resultados que usa o idioma de sua escolha e corresponde à aparência do site.

O modelo consiste em uma combinação de texto, tags HTML padrão e tags especiais definidas para exibir os resultados da pesquisa. Quando um cliente realiza uma pesquisa, o robô de pesquisa lê o modelo, gera o texto usando tags HTML padrão e insere os links de resultados com base nas tags de modelo especiais.

Consulte [Pesquisar marcas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modelo.

Se quiser alterar o idioma dos resultados, edite o texto em inglês que aparece no modelo.

Consulte [Editar uma apresentação ou um modelo](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.

## É possível ter mais de um site no logon de cliente da Adobe? {#section_AFA8825182094660A71EEC84B8329D6D}

Sim. Com um único logon de cliente da Adobe, você pode gerenciar um mecanismo de pesquisa diferente para vários sites diferentes. Selecione e gerencie contas em &quot;Contas&quot;.

Consulte [Seleção de uma conta diferente para usar](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26).

## Posso pesquisar mais de um domínio? {#section_BFBB0E9861D942F095B56CF0A8F16596}

Sim. Você pode configurar o acesso para mais de um domínio usando [!DNL URL Entrypoints]. Forneça pontos de entrada de URL para domínios adicionais que você possui. Lembre-se de que você deve ter permissão para indexar domínios que você não possui.

Consulte [Sobre pontos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## Posso subdividir meu site em seções separadas para que os clientes possam pesquisar qualquer uma dessas áreas individualmente ou em todo o site? {#section_52153A9DE9F9493B967A70583848B2A4}

Sim. Um recurso &quot;Coleções&quot; está incluído e permite que os clientes pesquisem áreas específicas do seu site para encontrar rapidamente o que estão procurando.

Consulte [Sobre coleções](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127).

Por exemplo, os clientes podem pesquisar uma coleção de URLs relacionados a informações de vendas de produtos ou uma coleção de URLs relacionados a serviços de suporte. Você pode configurar coleções para que seus clientes vejam uma lista suspensa de coleções ou um grupo de caixas de seleção.

## Como excluir partes do meu site de serem pesquisadas? {#section_D452EDE153654EF398F4A87780C6D43B}

Sim. Especifique as máscaras de URL para determinar quais páginas do site você deseja incluir ou excluir da indexação. As máscaras de URL determinam se as páginas do site aparecem nos resultados da pesquisa.

Consulte [Sobre máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)de URL.

Consulte [Sobre o script](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)de máscaras de URL.

Para impedir que partes de páginas da Web individuais sejam pesquisadas, é possível excluir partes de uma página da indexação. Envolva o texto com `<noindex>` e `</noindex>` tags. Esse método é útil se você deseja excluir o texto de navegação das pesquisas.

## Quais conjuntos de caracteres são suportados? {#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

Geralmente, as páginas da Web especificam o conjunto de caracteres com uma tag meta semelhante ao seguinte:

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

O mecanismo de pesquisa/comercialização do site indexa corretamente as páginas da Web usando todos os conjuntos de caracteres comuns em uso na Internet hoje. Alguns dos conjuntos de caracteres suportados incluem o seguinte:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Árabe (ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>Chinês (Tradicional; Big5) </p> </td> 
   <td colname="col3"> <p>Japonês (Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Árabe (Windows-1256) </p> </td> 
   <td colname="col2"> <p>Chinês (Tradicional; EUC-TW) </p> </td> 
   <td colname="col3"> <p>Russo (KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Báltico (ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>Cirílico (ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>Sul da Europa (ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Báltico (Windows-1257) </p> </td> 
   <td colname="col2"> <p>Cirílico (Windows-1251) </p> </td> 
   <td colname="col3"> <p>Turco (ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa Central (ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>Grego (ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>Turco (Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa Central (Windows-1250) </p> </td> 
   <td colname="col2"> <p>Grego (Windows-1253) </p> </td> 
   <td colname="col3"> <p>Unicode (UTF-8) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (ISO-2022-CN) </p> </td> 
   <td colname="col2"> <p>Hebraico (ISO-8859-8) </p> </td> 
   <td colname="col3"> <p>US-ASCII (us-ascii) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (ISO-2022-CN-EXT) </p> </td> 
   <td colname="col2"> <p>Hebraico (Windows-1255) </p> </td> 
   <td colname="col3"> <p>Europeu Ocidental (ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (Simplificado; EUC-CN) </p> </td> 
   <td colname="col2"> <p>Japonês (EUC-JP) </p> </td> 
   <td colname="col3"> <p>Europeu Ocidental (ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (Simplificado; (GB2312) </p> </td> 
   <td colname="col2"> <p>Japonês (ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>Europeu Ocidental (Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (Simplificado; GBK) </p> </td> 
   <td colname="col2"> <p>Japonês (ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>Europeu Ocidental (x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinês (Simplificado; HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>Japonês (ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Entre em contato com o suporte técnico para saber mais sobre os conjuntos de caracteres que não estão listados acima.

## E se eu alterar ou atualizar meu site? {#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

Depois de alterar o conteúdo do seu site, você pode executar um índice completo ou incremental. A pesquisa/comercialização do site baixa e indexa qualquer conteúdo alterado do site. Depois que a indexação for concluída, seus clientes poderão pesquisar o novo conteúdo. Você também pode agendar uma indexação automática do site em um determinado momento e em um dia específico.

Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Consulte [Configuração do agendamento de índice completo para um site](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)ao vivo.

Consulte [Configurar o agendamento de índice incremental para um site](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)ao vivo.

## Meu site pode ser indexado automaticamente? {#section_9C7D41636238488691ECDFEE4D4E5103}

Sim. Você pode agendar um índice automático do site todos os dias.

Além da indexação automática diária, você pode optar por ter partes do site alteradas com frequência e indexadas incrementalmente. Nos dias em que você tem um índice automático programado, é possível controlar a hora do dia em que o índice ocorre. Além disso, você sempre pode iniciar manualmente um índice de site sempre que desejar.

Consulte [Configuração do agendamento de índice completo para um site](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)ao vivo.

Consulte [Configurar o agendamento de índice incremental para um site](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)ao vivo.

## Eu uso senhas em meu site. Ainda posso usar a pesquisa/comercialização do site? {#section_4618EB5B66704640B5502D1B5CB4B32E}

Se você usar a Autenticação Básica HTTP para proteger por senha determinadas partes do seu site, poderá especificar realms e senhas que a pesquisa/comercialização do site pode usar para indexar seu site.

Consulte [Adicionando senhas para acessar áreas de seu site que exigem...](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).

## Você suporta o rastreamento e a indexação de https ou conteúdo protegido do servidor? {#section_D5BB8B8FBEA4405583E86B4AEC37151B}

Sim. Você pode rastrear e indexar conteúdo em servidores protegidos (https).

## A pesquisa/comercialização do site honra o arquivo robots.txt do meu site? {#section_73BBF6FE93C64C109F45CBC2FA394DB2}

Sim. O Robots Exclusion Protocol está em conformidade. O robô de pesquisa examina o arquivo robots.txt se ele estiver presente em seu site. Se o arquivo robots.txt excluir todos os robôs de rastrear seu site, o robô de pesquisa/comercialização do site também será excluído. Para permitir que somente o robô de pesquisa/comercialização do site rastreie seu site, defina o conteúdo do arquivo robots.txt para o seguinte:

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

Você pode saber mais sobre robôs web e o protocolo de exclusão de robôs no seguinte endereço:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## Determinadas partes do meu site devem ser atualizadas com frequência para que meus clientes obtenham os resultados de pesquisa mais precisos. A indexação incremental ajuda com esse problema? {#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

Sim. Esse cenário é o que o recurso de indexação incremental foi criado para facilitar a pesquisa/comercialização do site. O principal benefício da indexação incremental é que ela permite que as empresas indexem com frequência partes dinâmicas do site que mudam. Essa funcionalidade garante que você esteja exibindo os resultados da pesquisa com precisão de &quot;até um minuto&quot;.

Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Consulte [Configurar o agendamento de índice incremental para um site](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)ao vivo.

## As páginas da Web geradas dinamicamente são suportadas por um banco de dados back-end, como catálogos de produtos ou sistemas de gerenciamento de inventário? {#section_26896C556483457E879785E751583B16}

Páginas da Web HTML estáticas ou geradas dinamicamente, incluindo páginas criadas a partir de bancos de dados ou qualquer outro processo de back-end são indexadas. Como o código HTML, conforme exibido por um navegador, é indexado, você pode usar a pesquisa/comercialização do site em sites, desde que as informações do banco de dados de back-end resultem em páginas HTML.

O robô de pesquisa rastreia seu site começando pela primeira página no endereço do site especificado em [!DNL Account Settings]e segue links de página para página.

Consulte [Definição das configurações](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)da sua conta.

Quando o robô de pesquisa rastreia e indexa todas as páginas do site, você pode usar o mecanismo de pesquisa para pesquisar no site. Em outras palavras, se documentos gerados dinamicamente forem inseridos em seu site com links de outras páginas, o robô de pesquisa ainda poderá rastrear e indexar o conteúdo do banco de dados dinâmico.

Depois que o conteúdo do site é rastreado e indexado, os clientes do site podem pesquisar informações dentro do conteúdo indexado.

Você pode facilmente habilitar a pesquisa de conteúdo completo ou uma pesquisa com base em tópicos mais restrita, restrita a informações no título, à meta-descrição ou às tags de documento de meta-palavras, ou todas as três. Usando definições de metadados, também é possível criar campos de exibição personalizados, como uma imagem de produto, nos resultados da pesquisa real.

Consulte [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.

## Posso usar scripts ou programas para iniciar um índice incremental do meu site? {#section_0B6BB039557A42AA876D35D748E17DD0}

Sim. Você pode usar scripts ou programas para iniciar um índice incremental do seu site, bem como fazer ping nos servidores para indexar o site sempre que o conteúdo for alterado ou atualizado.

Consulte [Sobre o índice](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)de script.

## Implementações de recursos {#reference_2D0C4A80B8D64051BA9694D562DCE663}

Uma página de perguntas frequentes que discute várias implementações de recursos em [!DNL Search&Promote].

Veja a seguir perguntas comuns sobre implementações de recursos em um [!DNL Search&Promote] site:

* [Por que minhas regras de negócios não estão funcionando?](#section_7FEB60383D8A4B11A60DFF9067274699)
* [Por que há problemas ao agendar a indexação, erros ao iniciar a indexação e problemas ao iniciar a indexação em etapas?](#section_E05758193DF5436784B0145839989F75)
* [Meu limite de tamanho de índice excede meu limite permitido. Por que isso está acontecendo e como faço para consertá-lo?](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## Por que minhas regras de negócios não estão funcionando? {#section_7FEB60383D8A4B11A60DFF9067274699}

Configure as regras de negócios quando os banners forem exibidos ou para ajudar a decidir quais resultados serão exibidos e em que ordem. Você também pode configurar a posição de um item em sua faceta e qual modelo é usado para uma determinada pesquisa.
Reorganize as regras de negócios para alterar a ordem em que são executadas nos modelos de apresentação. As regras de negócio são aplicadas na ordem em que foram definidas; ou seja, quanto maior for o número do pedido de uma regra, mais tarde ela será executada no processo, superando as regras anteriores. Você reorganiza as regras digitando um novo número na coluna Ordem da tabela na página Regras de Negócios.

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Por que há problemas ao agendar a indexação, erros ao iniciar a indexação e problemas ao iniciar a indexação em etapas? {#section_E05758193DF5436784B0145839989F75}

Quando você gera um índice, seja ele completo ou incremental, as informações de status de rastreamento de índice são exibidas em tempo real. Por exemplo, você pode exibir a hora de início, o tempo decorrido e quaisquer erros que ocorreram durante o processo de indexação. As informações sobre o status do último índice também são exibidas. Use essas informações para solucionar erros de indexação encontrados.

Para agendar um índice, consulte [Configuração do agendamento de índice completo para um site](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0) ao vivo e [Definição do agendamento de índice incremental para um site](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)ao vivo.

Para iniciar um índice de preparo, consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D) ou [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Meu limite de tamanho de índice excede meu limite permitido. Por que isso está acontecendo e como faço para consertá-lo? {#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

Um site pode ter tendência a crescer e ao longo do tempo o Search&amp;Promote &quot;descobre&quot; mais documentos e páginas da Web que foram adicionados. Eventualmente, sua conta poderá exceder seu limite de tamanho de indexação, em tais casos, você poderá considerar o uso **[!UICONTROL URL Mask]**. Este recurso oculta documentos e páginas da Web do rastreamento de índice que você não deseja ou não precisa que sejam indexados, reduzindo o tamanho do índice. Outra opção pode ser entrar em contato com o suporte técnico para que o limite de tamanho de indexação seja definido como maior na sua conta.

Consulte [Sobre máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)de URL.

Se não tiver certeza do que fazer, entre em contato com o Suporte Técnico. Pode haver muitas outras variáveis afetando o tamanho do índice que, se ajustadas, também podem afetar o faturamento da sua conta.

## Internacional {#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

Uma página de perguntas frequentes que discute o suporte à indexação e pesquisa de mais de 19 idiomas, incluindo idiomas asiáticos multibyte, como chinês (simplificado e tradicional), japonês e coreano.

Veja a seguir perguntas comuns sobre idiomas e conjuntos de caracteres:

* [O que controla a codificação do conjunto de caracteres da consulta de pesquisa...](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [São apenas páginas pesquisadas cuja codificação corresponde à codificação de...](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [Qual codificação é usada para a página de resultados da pesquisa?](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [Posso usar a pesquisa/comercialização do site em páginas codificadas em Unicode, UTF-8?](#section_130997CB08934A13A5261D85CF88040C)
* [Por que não posso pesquisar os arquivos PDF chineses, japoneses ou coreanos no meu site?](#section_539AFF482F814D28B5929F683D2F2175)
* [Por que não posso pesquisar os arquivos SWF chineses, japoneses ou coreanos no meu site?](#section_9C0849528AFF4C10AA97A2C912992638)
* [Por que não posso pesquisar os arquivos do Microsoft Office em chinês, japonês ou coreano no meu site?](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [Por que não posso pesquisar os arquivos MP3 chineses, japoneses ou coreanos no meu site?](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [Preciso fazer algo especial para conseguir...](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [Como as fontes chinesas, japonesas ou coreanas aparecem nos resultados da pesquisa no Netscape 4.7 e anterior?](#section_DF42567063304F918D406AC76529DFB7)

## O que controla a codificação do conjunto de caracteres da consulta de pesquisa? {#section_DF2E8570AFC2480FA199FD26C941A22F}

A seção &quot;Formulários Web&quot; da sua conta de pesquisa contém formulários de pesquisa de amostra que você usa para adicionar a funcionalidade de pesquisa ao seu site. Se você observar esse código de pesquisa de formulários, poderá encontrar uma linha semelhante à seguinte:

`<input type=hidden name="sp_f" value="iso-8859-1">`

Essa linha de código informa ao mecanismo de pesquisa que a consulta recebida está codificada em iso-8859-1, uma codificação comum para idiomas da Europa Ocidental. Você pode alterar essa configuração indo para o menu do produto e clicando em **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**. Na [!DNL Personal Information] página, na lista **[!UICONTROL Character Encoding]** suspensa, selecione uma nova codificação.

Consulte [Configuração das informações](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)pessoais do usuário.

Também é possível alterar manualmente o valor de codificação em suas páginas da Web editando a `sp_f` linha do formulário de pesquisa. Lembre-se de que o `sp_f` valor do formulário de pesquisa deve corresponder à codificação do conjunto de caracteres da página em que ele aparece.

## Somente as páginas pesquisadas cuja codificação corresponde à codificação da consulta de pesquisa? {#section_9E544F3DB7DE41618DC1BC8224B32C5A}

Por padrão, não. Desde que as páginas do site identifiquem corretamente a codificação do conjunto de caracteres, as conversões necessárias são feitas entre a codificação da consulta de pesquisa e a das páginas, mesmo quando as páginas usam várias codificações.

## Qual codificação é usada para a página de resultados da pesquisa? {#section_DA68670F35D54EAABF7DBB010F4409BF}

A codificação do conjunto de caracteres da sua conta determina a codificação padrão para o modelo de resultados.

Consulte [Configuração das informações](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)pessoais do usuário.

Você pode saber mais sobre como especificar um conjunto de caracteres em um modelo HTML.

Consulte [Pesquisar marcas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modelo.

## Posso usar a pesquisa/comercialização do site em páginas codificadas em Unicode, UTF-8? {#section_130997CB08934A13A5261D85CF88040C}

Sim. No entanto, os conjuntos de caracteres Unicode, como o UTF-8, não fornecem informações suficientes para determinar o idioma no qual as páginas estão gravadas. Para pesquisar corretamente essas páginas, é necessário especificar o idioma. Para determinar o idioma do documento, as informações são processadas na seguinte ordem:

* Cabeçalho HTTP de linguagem de conteúdo fornecido para o documento pelo seu servidor.
* Elementos META (por exemplo, `META HTTP-EQUIV="Content-Language" Content="ja_JP"`) na seção `<HEAD>` do documento.

* Atributo LANG da `<HTML>` tag (por exemplo, `<HTML LANG="ja_JP">`).

Se o servidor não estiver configurado para fornecer o cabeçalho HTTP de linguagem de conteúdo e os documentos não contiverem o elemento META de idioma nem o atributo de idioma para a `<HTML>` tag , você poderá usar injeções de metadados para especificar o idioma apropriado.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

## Por que não posso pesquisar os arquivos PDF chineses, japoneses ou coreanos no meu site? {#section_539AFF482F814D28B5929F683D2F2175}

A pesquisa/comercialização do site obtém UTF-8 de arquivos Adobe PDF sem indicação de idioma. Se você selecionou **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o idioma usado no arquivo PDF.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

## Por que não posso pesquisar os arquivos SWF chineses, japoneses ou coreanos no meu site? {#section_9C0849528AFF4C10AA97A2C912992638}

A pesquisa/comercialização do site obtém UTF-8 de arquivos de filme Adobe Flash que foram criados com o Adobe Flash sem indicação de idioma. Se você selecionou o tipo de conteúdo **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o idioma usado no arquivo SWF.

Para Flash versão 4 ou versões anteriores de arquivos SWF, o conjunto de caracteres dos caracteres no arquivo não é especificado. Se você selecionou o tipo de conteúdo **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o conjunto de caracteres usado no arquivo SWF.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

## Por que não posso pesquisar os arquivos do Microsoft Office em chinês, japonês ou coreano no meu site? {#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

A pesquisa/comercialização do site obtém UTF-8 de arquivos do Microsoft Office (Microsoft Word, Microsoft Excel e Microsoft PowerPoint) sem indicação de idioma. Se você selecionou o tipo de conteúdo **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o idioma usado nos arquivos do Microsoft Office.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

## Por que não posso pesquisar os arquivos MP3 chineses, japoneses ou coreanos no meu site? {#section_DB6D60CF46F94125BF4E54AF3036DBFC}

Se você selecionar o tipo de conteúdo **[!UICONTROL Text in MP3 Music Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), deverá usar injeções de metadados para especificar o conjunto de caracteres usado para codificar os arquivos MP3.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

## Preciso fazer algo especial para que os arquivos .txt no meu site sejam indexados corretamente? {#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

Se você selecionou o tipo de conteúdo **[!UICONTROL Text Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o conjunto de caracteres usado para codificar os arquivos .txt.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

## Como as fontes chinesas, japonesas ou coreanas aparecem nos resultados da pesquisa no Netscape 4.7 e anterior? {#section_DF42567063304F918D406AC76529DFB7}

Se sua conta usar o modelo padrão, um dos modelos prontos para uso ou um modelo baseado em qualquer um desses modelos, ele pode conter tags de fonte que especificam Arial ou Helvetica como faces de fonte. Por exemplo, `<font face="arial, helvetica" size="+1">`. O Netscape 4.7 e anterior não exibe caracteres chineses, japoneses ou coreanos quando a face de fonte Arial ou Helvetica é usada. Remova o `face` atributo ou substitua a face da fonte por uma mais apropriada para chinês, japonês ou coreano.

## Contagem de página baixa {#reference_4344E3E3CB2948939860F8C078BD7773}

Uma página de perguntas frequentes que discute problemas comuns associados a uma baixa contagem de páginas de indexação.

Veja a seguir algumas perguntas comuns relacionadas às contagens baixas de páginas de indexação:

* [Você examinou seu registro de índice?](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [Você tem erros de digitação no URL?](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [A página da Web do ponto de entrada tem links para outras páginas...](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [São links para outras páginas do site incorporadas em...](#section_EE34A67D60A844EBB0921C03544FF63E)
* [As tags HTML na sua página da Web estão em um...](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [Você formou tags de comentário HTML incorretamente em seu...](#section_D1C39D79341845CB9C38579AABDF3A24)
* [Sua página da Web contém links para páginas em outra?..](#section_F8082759184049AAA8FA6342C1F84389)
* [Você está usando um serviço de domínio virtual para seu URL...](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [Sua página da Web usa uma tag meta-refresh?](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [Sua página da Web usa uma tag meta-robôs?](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [Seu site usa um arquivo de exclusão de robôs?](#section_BF7B663347814F58AD736066C86B7D25)

## Você examinou seu registro de índice? {#section_D6626536DC3D40DDA4A1224F1CB276BF}

O log de índice contém informações detalhadas que o robô de pesquisa/comercialização do site coleta ao indexar seu site. O log inclui uma lista de links rastreados e erros encontrados. Examinar o log de índice é o melhor local para começar a determinar por que todas as páginas do site não estão indexadas.

Consulte [Visualizando o log de índice completo de um ativo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Consulte [Visualizando o log de índice incremental de um ativo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

## Você tem erros de digitação no URL? {#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

Quando você digita URLs longos em formulários HTML, ele pode inserir um ou mais erros tipográficos. Lembre-se de que os URLs não devem conter espaços. Além disso, lembre-se de que alguns servidores da Web lidam com URLs que fazem distinção entre maiúsculas e minúsculas.

No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Na [!DNL Staged URL Entrypoints] página, verifique o seguinte:

* Você não tem nenhum erro tipográfico em seus URLs.
* Os caracteres nos URLs estão usando a caixa correta.
* Não há caracteres de espaço nos URLs.

Para testar seus pontos de entrada de URL, copie e cole um URL em um navegador da Web para ver se seu site é exibido. Se não for exibido, verifique novamente para garantir que você não cometeu nenhum erro no caminho do URL.

Consulte [Sobre pontos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## A página da Web do ponto de entrada tem links para outras páginas do seu site? {#section_1C2D6ED54E7249268B555D9DC33352B3}

O robô de pesquisa/comercialização do site rastreia seu site da mesma forma que seu cliente faz; seguindo os links de página para página. Os links devem estar presentes na página da Web do ponto de entrada antes que o robô de pesquisa possa localizar e indexar outras páginas em seu site.

Consulte [Adicionar vários pontos de entrada de URL que você deseja indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Os links para outras páginas do seu site estão incorporados ao JavaScript? {#section_EE34A67D60A844EBB0921C03544FF63E}

Você pode usar técnicas de navegação sofisticadas em seu site, como ações de roll-over e menus, que usam JavaScript para criar links para outras páginas. Entretanto, o robô de pesquisa/comercialização do site não pode seguir os links incorporados ao JavaScript.

Uma solução que você pode usar para resolver esse problema é colocar links ocultos para outras páginas no HTML que contém o JavaScript. Embora os clientes do seu site não vejam esses links, o robô de pesquisa ainda os encontra e os rastreia. Você pode colocar tags ocultas na parte inferior da página antes da `</body>` tag . Eles podem se parecer com o seguinte:

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

Outra solução é listar os URLs das páginas adicionais em seu site como pontos de entrada para rastrear e indexar. Inicie os URLs com a `https://` seguinte maneira:

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

Consulte [Adicionar vários pontos de entrada de URL que você deseja indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## As tags HTML na sua página da Web estão em uma sequência inválida? {#section_F31A2F5D2C284AC084158A5BD763DC5D}

A especificação HTML exige que as tags `<html>`, `<head>`e `<body>` sigam uma sequência específica em um documento HTML. As tags em todas as suas páginas da Web devem ter a seguinte sequência:

```
<html> 
<head> 
...  
<i>head tags go here</i> ... 
</head> 
<body> 
...  
<i>body tags go here</i> ... 
</body> 
</html>
```

Se as tags HTML não estiverem na ordem correta, o robô de pesquisa/comercialização do site não poderá analisar e indexar corretamente sua página da Web. A seguir está um exemplo de tags que não estão na sequência correta:

```
<body> 
<head> 
...  
<i>head tags are here</i> ... 
</head> 
...  
<i>body tags are here</i> ... 
</body>
```

Nesse caso, coloque as tags `<html>`, `<head>`e `<body>` na sequência correta na sua página da Web.

## Você formou tags de comentário HTML incorretamente na sua página da Web? {#section_D1C39D79341845CB9C38579AABDF3A24}

Certifique-se de revisar e corrigir cuidadosamente todos os comentários HTML inválidos em suas páginas da Web.

A especificação HTML exige que um comentário HTML comece com os caracteres `<!--` e termine com os caracteres `-->`. É fácil ignorar comentários formatados incorretamente que fazem com que o robô de pesquisa/comercialização do site analise incorretamente as tags em sua página da Web. Um comentário formado incorretamente pode fazer com que o robô de pesquisa/comercialização do site perca outras tags importantes que precisam ser analisadas. Lembre-se dos comentários logo antes da `<body>` tag na sua página da Web.

A seguir está um exemplo de um comentário corretamente formado:

`<!-- This HTML comment is OK. -->`

Este é um exemplo de comentários formados incorretamente:

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## Sua página da Web contém links para páginas em outro domínio? {#section_F8082759184049AAA8FA6342C1F84389}

Geralmente, um site pode consistir em páginas que realmente existem em um servidor da Web com um endereço de domínio diferente. Por exemplo, se o endereço do site principal for o seguinte:

`https://www.mydomain.com/`

Seu site também pode ter páginas em outro domínio, como:

`https://www.otherdomain.com/`

Por padrão, o robô de pesquisa/comercialização do site não segue links em um domínio diferente do principal. No entanto, ao configurar pontos de entrada adicionais para sua conta de pesquisa, você pode indexar facilmente vários domínios.

No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Adicione o URL do &quot;ponto de entrada principal do site&quot; de seu site. Em seguida, adicione outros pontos de entrada de URL a qualquer outro domínio que contenha páginas do site. Por exemplo, você definiria seu ponto de entrada principal de URL como:

`https://www.mydomain.com/`

e adicione o seguinte ponto de entrada adicional do URL do site:

`https://www.otherdomain.com/`

## Você está usando um serviço de domínio virtual para seu URL? {#section_2861F09EA21A45E6B7E15F032739CDF3}

Você pode estar usando um serviço de domínio virtual (às vezes chamado de &quot;serviço de redirecionamento de domínio&quot;) para fornecer um URL melhor para os clientes acessarem seu site. Por exemplo, suponha que o endereço real do seu site seja o seguinte:

`https://www.myispdomain.com/~myname/mywebpages/`

No entanto, você usa um serviço de domínio virtual para que os clientes possam acessar seu site nos seguintes endereços:

`https://myname.adomain.com/`

ou

`https://adomain.com/myname/`

Por padrão, o robô de pesquisa/comercialização do site não segue links em um domínio diferente do principal. No entanto, ao configurar pontos de entrada adicionais para sua conta de pesquisa, você pode indexar facilmente vários domínios.

No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Adicione o &quot;ponto de entrada principal do URL do site&quot; ao nome de domínio virtual do site. Em seguida, adicione outros pontos de entrada ao domínio onde seu site realmente vive.

Por exemplo, você definiria seu ponto de entrada principal do URL como o seguinte:

`https://myname.adomain.com/`

E adicione o seguinte ponto de entrada adicional do URL do site:

`https://www.myispdomain.com/~myname/mywebpages/`

## Sua página da Web usa uma tag meta-refresh? {#section_5A2F544C237C49B8B1A7FE0C45371C0D}

Muitos sites têm uma página inicial que inclui uma tag meta-refresh entre as `<head>...</head>` tags semelhantes às seguintes:

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

Em determinadas circunstâncias, o robô de pesquisa/comercialização do site não consegue seguir o URL de atualização meta para indexar o conteúdo do site. Esse problema é fácil de resolver ao configurar pontos de entrada adicionais.

No menu do produto, clique em **[!UICONTROL Settings]** > Rastreamento > **[!UICONTROL URL Entrypoints]**. Adicione outro ponto de entrada ao URL da tag meta-refresh.

## Sua página da Web usa uma tag meta-robôs? {#section_36275A33DDFE4620BABA948F8A63DBD2}

Às vezes, as páginas da Web usam tags meta-robôs para controlar robôs da Web que periodicamente tentam rastrear um site. As tags de meta-robôs são exibidas entre as `<head>...</head>` tags de uma página da Web e parecem semelhantes à seguinte tag:

`<meta name="robots" content="noindex, nofollow">`

Como o robô de pesquisa/comercialização do site é um robô web, ele segue os rumos da tag meta-robôs. Ao excluir outros robôs dessa forma, você também exclui o robô de pesquisa/comercialização do site.

Você pode saber mais sobre robôs web e o protocolo de exclusão de robôs no seguinte endereço:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Remova ou modifique a tag meta-robôs nas páginas da Web que você deseja indexar em seu site.

## Seu site usa um arquivo de exclusão de robôs? {#section_BF7B663347814F58AD736066C86B7D25}

Às vezes um site tem uma página chamada robots.txt que exclui todos ou alguns robôs de rastreá-lo. Para ver se o site tem um arquivo robots.txt, procure-o logo abaixo do domínio de nível superior, como mostrado no seguinte:

`https://www.yourdomain.com/robots.txt`

O conteúdo do arquivo robots.txt é semelhante ao seguinte texto:

```
User-agent: * 
Disallow: /
```

Como o robô de pesquisa/comercialização do site é um robô web, ele segue as direções no arquivo robots.txt — exclui o robô de pesquisa/comercialização do site. Para contornar esse problema, edite o arquivo de exclusão de robôs (robots.txt) para permitir que o robô de pesquisa/comercialização do site rastreie e indexe seu site da seguinte maneira:

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

Uma página de perguntas frequentes que discute o suporte à indexação e pesquisa de arquivos do Microsoft® Office em um site.

Veja a seguir perguntas comuns sobre arquivos do Microsoft Office:

* [O que é indexado em um arquivo do Microsoft Office?](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [O que não é indexado em um arquivo do Microsoft Office...](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [Como os arquivos do Microsoft Office são indexados de forma diferente das páginas HTML...](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Como impedir que os arquivos do Microsoft Office sejam indexados...](#section_FEBA71274CD14CB99731ADF982087F4C)

## O que é indexado em um arquivo do Microsoft Office? {#section_8681DADFCFE24B7787B1FC08D431EE28}

O conteúdo completo dos arquivos do Microsoft Word, do Microsoft Excel e do Microsoft PowerPoint é indexado.

As seguintes partes de um arquivo do Microsoft Word estão indexadas:

* Título
* Palavras-chave
* Assunto (Descrição)
* Conteúdo baseado em texto
* Hiperlinks para outros documentos

As seguintes partes de um arquivo do Microsoft Excel estão indexadas:

* Título
* Palavras-chave
* Assunto (Descrição)
* Texto em células
* Valores de fórmulas numéricas em células

As seguintes partes de um arquivo do Microsoft PowerPoint estão indexadas:

* Título
* Palavras-chave
* Assunto (Descrição)
* Texto em cada slide

## O que não é indexado em um arquivo do Microsoft Office? {#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

Os gráficos contidos em arquivos do Microsoft Office ou qualquer texto que faça parte de um gráfico contido não são indexados. As definições de propriedade personalizada não são indexadas como metadados. Alguns textos em campos especiais, como cabeçalhos e rodapés em um arquivo PowerPoint, também não são indexados.

## Como os arquivos do Microsoft Office são indexados de forma diferente das páginas HTML? {#section_C104B44684F340549A6B9EB8F39EDDBB}

A diferença entre a forma como o robô de pesquisa indexa arquivos do Microsoft Office e arquivos HTML é que cada arquivo HTML é uma página individual e um único arquivo do Microsoft Office pode representar centenas de páginas. Por isso, cada página é contada em um arquivo do Microsoft Office como uma página separada na sua conta de pesquisa.

## Como impedir que os arquivos do Microsoft Office sejam indexados no meu site? {#section_FEBA71274CD14CB99731ADF982087F4C}

Se você não quiser que o robô de pesquisa rastreie e indexe arquivos do Microsoft Office, desmarque o tipo de conteúdo **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Você também pode usar [!DNL URL Masks] para desativar a indexação de arquivos do Microsoft Office.

Digite as seguintes máscaras de URL:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Se você não estiver usando expressões regulares </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">exclude *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">excluir *.xls </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">excluir *.ppt </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Se você estiver usando expressões regulares </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">exclua regexp ^.*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">exclua regexp ^.*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">exclua regexp ^.*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Consulte [Adicionar máscaras de URL para indexar ou não indexar partes de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Consulte Expressões [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

Uma página de perguntas frequentes que discute o suporte à indexação e pesquisa de arquivos de música MP3 em um site.

Veja a seguir perguntas comuns sobre arquivos MP3.

* [Quando um arquivo MP3 é rastreado e indexado?](#section_538EA1682C9C47E3A62640BB25D84C36)
* [O que tenho que fazer para rastrear e indexar...](#section_3CD794446E3545379C14E9F222118665)
* [Como um arquivo MP3 é reconhecido?](#section_230E7336965A424F96C5CCF1D3C2D103)
* [O que é indexado em um arquivo MP3?](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [Um arquivo MP3 conta como uma página?](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [Como impedir a indexação de arquivos MP3 individuais...](#section_C989DC1D3D3841B38F683A462195DC05)
* [Como impedir que arquivos MP3 sejam indexados?](#section_305D2B28D1124776B6DC0C62A17827C6)
* [Por que não consigo pesquisar os arquivos MP3 chineses, japoneses ou coreanos no meu site?](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## Quando um arquivo MP3 é rastreado e indexado? {#section_538EA1682C9C47E3A62640BB25D84C36}

Arquivos MP3 são rastreados e indexados de uma das duas maneiras. A maneira mais comum é a partir de uma tag href de âncora em um arquivo HTML:

`<a href="MP3-file-URL"></a>`

Uma segunda maneira é inserir o URL do arquivo MP3 como um ponto de entrada de URL.

Consulte [Sobre pontos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## O que devo fazer para rastrear e indexar os arquivos MP3 no meu site? {#section_3CD794446E3545379C14E9F222118665}

Para ativar o rastreamento e a indexação MP3 para sua conta, no menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Na [!DNL Staged Content Types] página, selecione **[!UICONTROL Text in MP3 Music Files]**.

Consulte [Sobre tipos](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de conteúdo.

## Como um arquivo MP3 é reconhecido? {#section_230E7336965A424F96C5CCF1D3C2D103}

Um arquivo MP3 é reconhecido pelo tipo MIME que é &quot;audio/mpeg&quot;.

## O que é indexado em um arquivo MP3? {#section_E99D252B27CA4946AED3FCD3ABD8779D}

Como opção, os arquivos MP3 armazenam uma pequena quantidade de informações textuais. Essas informações podem incluir o nome do álbum, o nome do artista, o título da música, o gênero da música, o ano de lançamento e um comentário. Estas informações são armazenadas no final do ficheiro no que é chamado TAG. Os arquivos MP3 que contêm informações TAG são indexados da seguinte maneira:

* O título da música é tratado como o título de uma página HTML.
* O comentário é tratado como uma descrição definida para uma página HTML.
* O gênero é tratado como uma palavra-chave definida para uma página HTML.
* O nome do artista, o nome do álbum e o ano de lançamento são tratados como o corpo de um documento HTML.

## Um arquivo MP3 conta como uma página? {#section_9910BEB6617D4D2090558CDF6C65D16B}

Sim, cada arquivo MP3 rastreado e indexado em seu site é contado como uma página.

## Como impedir a indexação de arquivos MP3 individuais? {#section_C989DC1D3D3841B38F683A462195DC05}

Coloque as tags de âncora que se vinculam aos arquivos MP3 com `<nofollow>` e `</nofollow>` tags. O robô de pesquisa não segue os links entre essas tags.

Outro método é adicionar os URLs dos arquivos MP3 como máscaras de exclusão.

Consulte [Sobre máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)de URL.

Consulte [Sobre o script](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)de máscaras de URL.

## Como impedir que arquivos MP3 sejam indexados? {#section_305D2B28D1124776B6DC0C62A17827C6}

A maneira mais fácil de controlar a indexação MP3 para sua conta é desmarcando **[!UICONTROL Text in MP3 Music Files]** a página [!DNL Staged Content Types] .

Consulte [Seleção de tipos de conteúdo para rastrear e indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

Você também pode usar o recurso Máscaras de URL para desativar a indexação MP3 por extensão de arquivo. Para fazer isso, no menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Digite uma das seguintes máscaras:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Se sua conta... </p> </th> 
   <th colname="col2" class="entry"> <p>Insira a seguinte máscara de URL </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Não usa expressões regulares </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclude *.mp3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usa expressões regulares </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclua regexp ^.*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte Expressões [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Por que não consigo pesquisar os arquivos MP3 chineses, japoneses ou coreanos no meu site? {#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

Para pesquisar arquivos MP3 chineses, japoneses ou coreanos, no menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** > **[!UICONTROL Text in MP3 Music Files]**. Em seguida, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]** e especifique o conjunto de caracteres usado para codificar os arquivos MP3.

Consulte [Seleção de tipos de conteúdo para rastrear e indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

Consulte [Sobre Injeções](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

Uma página de perguntas frequentes discute o suporte à indexação e pesquisa de arquivos PDF em um site.

Veja a seguir perguntas comuns sobre arquivos PDF:

* [O que é indexado em um arquivo PDF?](#section_62BFCD7158B44F2BB3B1864224B50174)
* [O que não é indexado em um arquivo PDF?](#section_A14B353AE503408896BACBBF3F748FA0)
* [Como os arquivos PDF indexados são contados?](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [Os resultados da pesquisa podem exibir um ícone PDF?](#section_829CE82CC3544502A13D27C4DB820189)
* [Os resultados da pesquisa podem se vincular a uma página específica em...](#section_A06E7F7017E6441E98209D288EE57BF6)
* [Como impedir que arquivos PDF sejam indexados em...](#section_96671419A822486AAC654D8DAD819940)
* [Por que não posso pesquisar os arquivos PDF chineses, japoneses ou coreanos no meu site?](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## O que é indexado em um arquivo PDF? {#section_62BFCD7158B44F2BB3B1864224B50174}

O conteúdo completo dos arquivos PDF é indexado. As seguintes partes de um arquivo PDF são indexadas:

* Título
* Palavras-chave
* Assunto (Descrição)
* Conteúdo baseado em texto

## O que não é indexado em um arquivo PDF? {#section_A14B353AE503408896BACBBF3F748FA0}

O sumário do PDF, qualquer gráfico do arquivo ou qualquer texto que faça parte de um gráfico contido não são indexados.

## Como os arquivos PDF indexados são contados? {#section_C35DE36A65D649BD8FF314E9EFD990A6}

Cada arquivo PDF é contado, incluindo PDFs que contêm várias páginas, como um único documento.

## Os resultados da pesquisa podem exibir um ícone PDF? {#section_829CE82CC3544502A13D27C4DB820189}

Sim. Use a `<search-if-link-extension>` tag do modelo para incluir um ícone PDF ou outros gráficos ou texto nos resultados da pesquisa:

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

Os ícones de PDF ajudam seus clientes a saber que o resultado da pesquisa é vinculado a um arquivo PDF que pode ser muito grande. O tamanho do arquivo pode ser importante para os clientes que estão acessando seu site por um modem ou em um dispositivo móvel.

## Os resultados da pesquisa podem se vincular a uma página específica em um arquivo PDF? {#section_A06E7F7017E6441E98209D288EE57BF6}

Sim. Usando a tag do modelo de links inteligentes ( `<search-smart-link>...</search-smart-link>`), os clientes podem clicar para abrir a primeira página do PDF que contém o resultado da pesquisa.

Para usar links inteligentes, substitua as `<search-link>...</search-link>` tags na seção de resultados da pesquisa do modelo por `<search-smart-link>...</search-smart-link>` tags. Quando um cliente clica em um link gerado pelas tags de link inteligente, ele vai para a primeira página PDF relevante para a consulta de pesquisa.

>[!NOTE]
>
>Para usar esse recurso, o cliente deve usar uma versão recente do Adobe Acrobat ou do Adobe Acrobat Reader, que deve incluir o plug-in de realce e o plug-in External Window Handler (EWH). Além disso, o navegador da Web deles deve usar o plug-in do Adobe Acrobat para o Netscape Navigator (você pode usar qualquer navegador que aceite esse plug-in do Netscape Navigator) ou o controle do Acrobat AtiveX para o Internet Explorer 4.0 e posterior.

Consulte [Pesquisar marcas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modelo.

## Como impedir que arquivos PDF sejam indexados no meu site? {#section_96671419A822486AAC654D8DAD819940}

Se você não quiser que o robô de pesquisa rastreie e indexe arquivos PDF, desmarque o tipo de conteúdo **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Você também pode optar por usar [!DNL URL Masks] para desativar a indexação de PDF.

Consulte [Adicionar máscaras de URL para indexar ou não indexar partes de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Para desativar a indexação de PDF, insira uma das seguintes máscaras de URL:

* `exclude *.pdf` (se você não estiver usando expressões regulares)
* `exclude regexp ^.*\.pdf$` (se você estiver usando expressões regulares)

Consulte Expressões [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Por que não posso pesquisar os arquivos PDF chineses, japoneses ou coreanos no meu site? {#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

A pesquisa/comercialização do site obtém UTF-8 de arquivos PDF sem indicação de idioma. Se você selecionou o tipo de conteúdo **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), é necessário usar injeções de metadados para especificar o idioma usado no arquivo PDF.

Consulte [Adicionar definições](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de injeção de campo.

## Muitas páginas {#reference_48A748BC1ED14844ACAC2735C8388E8A}

Uma página de perguntas frequentes que explica algumas das razões pelas quais o indexador contou mais páginas do que você realmente conta, e qual é a solução em cada caso.

Se você tiver certeza de que seu site está abaixo do limite de sua página, mas o indexador estiver informando que o limite foi atingido, você deverá revisar essas perguntas e respostas comuns para encontrar possíveis soluções.

* [Você examinou seus vários registros de índice?](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [Os programas CGI estão sendo indexados em seu site?](#section_86ED8A641B3841EC80153B4F107548FD)
* [Seu servidor tem a navegação de diretório ativada?](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [Há fóruns ou grupos de notícias em seu site?](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [Há arquivos PDF ou do Microsoft Office no seu site...](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [Você tem vários pontos de entrada de URL?](#section_8C54AFD7DF56472A9364D516482B534C)
* [Você excedeu os bytes internos ou os limites de tempo de...](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## Você examinou seus vários registros de índice? {#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

O log de índice contém informações detalhadas coletadas pelo robô de pesquisa/comercialização do site, à medida que indexa seu site. O log inclui uma lista de todos os links rastreados e encontrou erros. Examinar o log de índice é o melhor local para iniciar quando você está tentando determinar quais páginas estão sendo indexadas.

Consulte [Visualizando o log de índice completo de um ativo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Consulte [Visualizando o log de índice incremental de um ativo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

Consulte [Visualizando o log de índice incremental com script de um live ou...](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).

Consulte [Visualizando o log de índice gerado novamente de um ativo ou preparado...](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).

Consulte [Visualizar o log de índice reclassificado de um site](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D)ao vivo ou preparado.

## Os programas CGI estão sendo indexados em seu site? {#section_86ED8A641B3841EC80153B4F107548FD}

Os programas CGI usam parâmetros de URL que às vezes fazem com que o indexador rastreie vários URLs &quot;falsos&quot;. Se a pesquisa/comercialização do site estiver lendo seus programas CGI e seguindo URLs com parâmetros CGI neles, provavelmente existem vários múltiplos de páginas sendo rastreadas e indexadas que não são úteis para seu índice de pesquisa. Parâmetros CGI típicos são exibidos em URLs com `?` ou `&` caracteres.

Você pode impedir que os programas CGI sejam indexados usando o recurso Máscaras de URL. Você pode mascarar um prefixo de URL ou usar expressões regulares para mascarar seus scripts CGI.

Consulte [Sobre máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)de URL.

Consulte [Sobre o script](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)de máscaras de URL.

Consulte Expressões [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Seu servidor tem a navegação de diretório ativada? {#section_073C88EEE74F4CA0AD2C7145D4810B22}

Quando um servidor da Web tem a navegação de diretório ativada e não há um arquivo index.html presente em um determinado diretório, uma visita a esse diretório pode mostrar a lista de arquivos nesse diretório. Normalmente, há links na parte superior da página para permitir que você classifique a lista de maneiras diferentes apenas clicando **[!UICONTROL Name]**, **[!UICONTROL Last modified]**, **[!UICONTROL Size]** etc. Normalmente, eles aparecem no log de índice de pesquisa/comercialização do site como URLs com caracteres, como `?M=A` no final. O indexador de pesquisa/comercialização do site os segue como links, e isso pode levar à indexação de vários URLs &quot;falsos&quot;.

Normalmente, um site bem projetado tem arquivos de índice localizados em cada diretório ou tem a navegação de diretório desativada para esses diretórios sem arquivos de índice. Felizmente, há uma maneira fácil de mascarar esses URLs &quot;falsos&quot; se você não conseguir alterar suas páginas ou desativar as listas de diretórios no lado do servidor.

Para realizar essa tarefa, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Adicione uma máscara para mascarar qualquer URL que contenha o caractere `?`. É possível realizar essa tarefa inserindo a seguinte máscara de expressão regular:

`exclude regexp ^.*\?.*$`

Depois de criar a máscara, certifique-se de reindexar seu site.

Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Há fóruns ou grupos de notícias em seu site? {#section_8DCB94F0850A41B9B2EA885F779E2F84}

Se fóruns ou grupos de notícias estiverem sendo pesquisados em seu site, ele pode estar seguindo URLs para opções de exibição diferentes ou opções de classificação. Esse comportamento significa que a mesma página é indexada várias vezes.

Geralmente, fóruns ou grupos de notícias vêm com seus próprios mecanismos de pesquisa. Nesse caso, você pode usar [!DNL URL Masks] para mascarar os fóruns da pesquisa/comercialização do site.

No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Na [!DNL Staged URL Masks] página, mascare seus fóruns inserindo seus URLs como máscaras de URL excluídas.

Consulte [Adicionar máscaras de URL para indexar ou não indexar partes de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Depois de criar as máscaras, certifique-se de indexar novamente seu site.

Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Há arquivos PDF ou do Microsoft Office em seu site? {#section_455FC5438DF74E68AB9A31D359EAD4D9}

Se você tiver arquivos PDF ou [!DNL Microsoft Office] arquivos PDF em seu site, talvez observe que o tamanho de índice de apenas alguns arquivos conta muitas páginas. O motivo pelo qual há mais páginas sendo indexadas do que documentos que você tem é porque cada página em um arquivo PDF ou do Microsoft Office é contada como uma página separada.

No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**. Na [!DNL Full Index] página, selecione **[!UICONTROL Count All Pages]** e clique **[!UICONTROL Full Index Now]** para ver uma contagem total de páginas. Se não quiser que arquivos PDF ou arquivos do Microsoft Office sejam indexados, desative esse tipo de conteúdo em **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.

Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Sobre tipos](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de conteúdo.

## Você tem vários pontos de entrada de URL? {#section_8C54AFD7DF56472A9364D516482B534C}

O robô de pesquisa/comercialização do site começa a rastrear em pontos de entrada de URL especificados e segue todos os links encontrados para todo o conteúdo desse domínio específico. Se você tiver especificado muitos pontos de entrada de URL, um número significativo de páginas poderá ser rastreado.

Use a `nofollow` tag do protocolo de exclusão de robôs nos cabeçalhos dos documentos de ponto de entrada nos domínios adicionais da seguinte maneira:

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

O código acima diz ao robô de pesquisa/comercialização do site para indexar o conteúdo da página, mas não para seguir os links para páginas adicionais.

Você pode saber mais sobre robôs web e o protocolo de exclusão de robôs no seguinte endereço:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Se você não tiver acesso à origem das páginas em domínios adicionais, poderá remover os vários pontos de entrada do URL. Isso ajuda a limitar a atividade de indexação somente aos domínios cujo conteúdo você deseja que os clientes possam pesquisar.

Consulte [Sobre pontos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## Você excedeu os bytes internos ou os limites de tempo de pesquisa/comercialização do site? {#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

Verifique se sua conta atingiu seu limite na tela &quot;Status completo do índice&quot;. Se o status reportar que seu índice é maior do que o permitido ou que levou mais tempo do que o permitido, seu site não será completamente indexado. Você pode corrigir esse erro para obter a cobertura correta e a contagem de páginas do site.

Para proteger os servidores de pesquisa/comercialização do site, há limites internos em bytes e tempo. Somente quando os arquivos rastreados são muito grandes, ou quando o servidor que a pesquisa/comercialização do site está tentando acessar está lento esses limites são atingidos.

Se você atingir um limite de tempo, verifique se o servidor está online e tente o índice novamente mais tarde. Se você atingir um limite de bytes, verifique os arquivos rastreados exibindo seu log de índice. Elas são excepcionalmente grandes? Entre em contato com o suporte técnico se você encontrar uma dessas mensagens.
