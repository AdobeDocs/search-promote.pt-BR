---
description: Você pode configurar várias áreas da opção Completar automaticamente para controlar a geração do formulário de pesquisa ativado para preenchimento automático e do arquivo autocomplete_data.js, que é incluído como parte do formulário de pesquisa ativado para preenchimento automático.
seo-description: Você pode configurar várias áreas da opção Completar automaticamente para controlar a geração do formulário de pesquisa ativado para preenchimento automático e do arquivo autocomplete_data.js, que é incluído como parte do formulário de pesquisa ativado para preenchimento automático.
seo-title: Sobre a conclusão automática
solution: Target
subtopic: Auto-Complete
title: Sobre a conclusão automática
topic: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
translation-type: tm+mt
source-git-commit: 439100ab96f4b597c55b1c1ae38a5778c208e896

---


# Sobre a conclusão automática{#about-auto-complete}

Você pode configurar várias áreas da opção Completar automaticamente para controlar a geração do formulário de pesquisa ativado para preenchimento automático e do arquivo autocomplete_data.js, que é incluído como parte do formulário de pesquisa ativado para preenchimento automático.

## Sobre a conclusão automática {#concept_093A9CD754864BA79B456FE4BEB64578}

O arquivo [!DNL autocomplete_data.js] é gerado novamente e publicado na rede de conteúdo de pesquisa sempre que houver alterações salvas na página de Configuração de Completar automaticamente.

## Configuração da conclusão automática {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

Você pode configurar e configurar as opções que controlam a geração do formulário de pesquisa ativado de preenchimento automático e o arquivo.

<!-- 

t_configuring_auto-complete.xml

 -->

Depois de configurar o preenchimento automático, você pode exibir a fonte HTML resultante para revisão. A fonte HTML é o que você copia e cola nas páginas do seu site.

Consulte [Visualizar o formulário de pesquisa como ele apareceria em...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Consulte [Configuração da lista](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)de palavras de preenchimento automático.

Consulte [Configuração do CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de Completar automaticamente.

**Para configurar a conclusão automática**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. Na [!DNL Auto-Complete Setup] página, defina as opções desejadas.

   Consulte também [Visualizar o formulário de pesquisa como ele apareceria em...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Máximo de sugestões </p> </td> 
      <td colname="col2"> <p>Especifica o número máximo de itens a serem exibidos na lista de sugestões de preenchimento automático. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caracteres mínimos de entrada </p> </td> 
      <td colname="col2"> <p>Especifica o número de caracteres que um cliente deve digitar no formulário de pesquisa de preenchimento automático antes de exibir sugestões. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máximo de entradas de cache </p> </td> 
      <td colname="col2"> <p>Especifica o número máximo de sugestões de preenchimento automático solicitadas anteriormente para armazenar em cache no navegador do cliente. Geralmente, você deve deixar essa configuração no padrão 1000. </p> <p>Embora você possa desativar completamente o cache do navegador ao definir essa opção para 0, isso não é recomendado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do formulário </p> </td> 
      <td colname="col2"> <p>Especifica o atributo "name" da tag "form" do formulário de pesquisa ativado para preenchimento automático. Por exemplo, </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>onde <span class="filepath"> SiteSearch </span> é o atributo name da tag de formulário. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID da tag Div </p> </td> 
      <td colname="col2"> <p>Especifica o atributo ID da tag "div" do formulário de pesquisa ativado para preenchimento automático. Por exemplo, </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>em que <span class="filepath"> preenchimento automático </span> é o atributo da tag div. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID da tag de entrada </p> </td> 
      <td colname="col2"> <p>Especifica o atributo ID da tag "input" do formulário de pesquisa ativado para preenchimento automático. Por exemplo, </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>onde <span class="filepath"> q </span> é o atributo id da tag de entrada. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Exibir sombra </p> </td>
      <td colname="col2"> <p>Adiciona uma sombra projetada superficial à lista de sugestões de preenchimento automático. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Corresponder somente no início da frase </p> </td>
      <td colname="col2"> <p>Sugerir somente resultados que correspondam ao início do texto de entrada. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Suporte a conjunto de caracteres UTF-8 </p> </td>
      <td colname="col2"> <p>Tratar corretamente caracteres não ASCII em termos. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuração da lista de palavras de preenchimento automático {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Configure a lista de palavras e frases que a opção Completar automaticamente é exibida para um cliente como sugestões.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Consulte [Configuração da conclusão automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuração do CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de Completar automaticamente.

**Para configurar a Lista de palavras de preenchimento automático**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. Na [!DNL Auto-Complete Word List] página, defina as opções desejadas.

   Consulte [Visualizar o formulário de pesquisa como ele apareceria em...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Período de pesquisa popular </p> </td> 
      <td colname="col2"> <p> Controla o período de tempo para a inclusão de palavras e frases de pesquisas recentes de um cliente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Contagem máxima de pesquisa </p> </td> 
      <td colname="col2"> <p>Controla o número máximo de palavras e frases pesquisadas a serem incluídas na lista de palavras de preenchimento automático. As palavras e frases principais, que também são as mais populares, estão incluídas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do campo </p> </td> 
      <td colname="col2"> <p>Cada nome de campo define o nome de um campo para o qual incluir valores indexados. Use + e - para adicionar ou remover nomes de campos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Contagem de valores máximos </p> </td> 
      <td colname="col2"> <p>Define a contagem máxima de valores de campo que são permitidos para o nome do campo selecionado. Os valores principais, que também são os mais referenciados, são incluídos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adicionar estas palavras e frases </p> </td> 
      <td colname="col2"> <p> A lista de palavras de preenchimento automático é preenchida com as palavras e frases listadas nessa área. </p> <p> Clique em <span class="uicontrol"> Editar </span> para ver a lista ou para adicionar palavras e frases à lista. Quando terminar, clique em <span class="uicontrol"> Salvar alterações </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover essas palavras e frases </p> </td> 
      <td colname="col2"> <p> As entradas nesta área não são exibidas na lista de palavras de preenchimento automático. </p> <p> Clique em <span class="uicontrol"> Editar </span> para ver a lista ou para adicionar palavras e frases à lista. Quando terminar, clique em <span class="uicontrol"> Salvar alterações </span>. </p> <p> Expressões regulares são permitidas nesta lista. Para especificar uma expressão regular nesta lista, inicie a linha com 
        <userinput>
          regexp 
        </userinput> seguido por um único espaço, seguido pela expressão regular. Todas as linhas na lista de palavras que correspondem à expressão regular são removidas. </p> <p> <b>Importante</b>: Você só deve usar expressões regulares se tiver trabalhado com elas anteriormente em outros aplicativos. </p> <p>Consulte <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorar Maiúsculas e Minúsculas </p> </td> 
      <td colname="col2"> <p>São removidas entradas duplicadas na lista de palavras de preenchimento automático que diferem apenas por letras maiúsculas/minúsculas alfabéticas; todas as entradas da lista de palavras são forçadas a minúsculas. </p> <p>Se desejar que as sugestões de Completar automaticamente apareçam "primeira letra maiúscula" ou "todas maiúsculas", adicione o 
        <userinput>
          text-transform : capitalizar; 
        </userinput> ou 
        <userinput>
          text-transform : maiúsculo; 
        </userinput> Propriedades de texto CSS para o conteúdo de CSS de Completar automaticamente, em "/* estilos para o item de resultado */". </p> <p>Consulte <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> Configurando o CSS de Completar automaticamente </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Atualização ao reindexar </p> </td> 
      <td colname="col2"> <p>A lista de palavras de preenchimento automático é automaticamente regenerada após cada reindexação de conta bem-sucedida. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.
   * Clique **[!UICONTROL Preview Word List]** para salvar quaisquer alterações feitas e abra a [!DNL Auto-Complete Word List Preview] página onde você pode revisar a lista de sugestões de preenchimento automático. Use as opções de navegação próximas à parte superior da página para revisar e refinar a lista exibida. Quando terminar, clique em **[!UICONTROL Close]** para retornar à [!DNL Auto-Complete Word List] página.

      Consulte [Uso da opção](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurando o CSS de Completar Automaticamente {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Use a opção Completar automaticamente o CSS para configurar a folha de estilos em cascata de preenchimento automático que você deseja usar.

<!-- 

t_configuring_auto-complete_css.xml

 -->

A opção Completar automaticamente o CSS controla o conteúdo do [!DNL autocomplete_styles.css], que é incluído como parte do formulário de pesquisa ativado para preenchimento automático. O CSS especificado aqui controla a apresentação visual da lista de sugestão de preenchimento automático. Para obter um exemplo das ideias de apresentação visual possíveis, consulte o seguinte:

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[Configuração da lista](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)de palavras de preenchimento automático.

[Configuração da Completar](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)Automaticamente.

Quando terminar de configurar o CSS de Completar automaticamente, você poderá visualizar o formulário de pesquisa para ver se o CSS especificado é aceitável na aparência e no layout.

Consulte [Visualizar o formulário de pesquisa como ele apareceria em...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Importante**: Para aplicar seu CSS de preenchimento automático personalizado, é necessário remover as tags de comentário da segunda linha que aparece no código HTML. Em seguida, mova a mesma linha para dentro da seção de cabeçalho da página que contém o formulário de pesquisa.

Consulte [Copiando o código HTML do formulário de pesquisa no...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Para configurar o CSS de Completar automaticamente**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. No campo de [!DNL Auto-Complete CSS] texto, cole ou digite as informações da folha de estilos em cascata que você deseja associar à lista de sugestão de preenchimento automático.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualizar o formulário de pesquisa como ele apareceria em seu site {#task_437B35EFA5424603A08AF8E79E6B4714}

Com base na configuração de Completar automaticamente e Completar automaticamente o CSS, você pode visualizar como o formulário de pesquisa será exibido se você quiser adicionar o código HTML ao seu site.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Consulte [Configuração da conclusão automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuração do CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de Completar automaticamente.

Consulte [Copiando o código HTML do formulário de pesquisa no...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de coleções em formulários](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de pesquisa.

Consulte [Uso de quadros com formulários](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Amostra de formulário](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de pesquisa avançada.

Consulte Código [HTML do formulário de pesquisa](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)avançada.

Consulte Código [do modelo de formulário de pesquisa](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)avançada.

**Para visualizar o formulário de pesquisa como ele apareceria em seu site**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Opcional) Clique em **[!UICONTROL HTML code]** para ver o HTML que você copia e cola nas páginas do seu site.

## Copiar o código HTML do formulário de pesquisa para as páginas do site {#task_A3A01EA800F24C0AA33902387E0362C7}

Com base na configuração de Completar automaticamente e Completar automaticamente o CSS, você pode visualizar como o formulário de pesquisa será exibido se você quiser adicionar o código HTML ao seu site.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Consulte [Configuração da conclusão automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuração do CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de Completar automaticamente.

Consulte [Copiando o código HTML do formulário de pesquisa no...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de coleções em formulários](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de pesquisa.

Consulte [Uso de quadros com formulários](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Amostra de formulário](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de pesquisa avançada.

Consulte Código [HTML do formulário de pesquisa](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)avançada.

Consulte Código [do modelo de formulário de pesquisa](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)avançada.

**Para copiar o código HTML do formulário de pesquisa nas páginas do site**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >Não altere o `form name=` valor na fonte do formulário.

1. (Opcional) Execute um dos procedimentos a seguir:

   * Se você configurou o CSS de preenchimento automático e deseja que os estilos sejam aplicados ao formulário de pesquisa, remova as marcas de comentário da segunda linha que aparece no código HTML. Em seguida, mova a mesma linha para dentro da seção de cabeçalho da página que contém o formulário de pesquisa.
   * Para obter o desempenho máximo, mova as tags listadas na parte inferior do código HTML e coloque-as na parte inferior da seção body de cada página que contém o formulário de pesquisa.

1. Copie o código e cole-o nas páginas da Web do site onde deseja que o formulário de pesquisa apareça.
