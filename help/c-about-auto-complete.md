---
description: É possível configurar várias áreas de Preenchimento automático para controlar a geração do formulário de pesquisa ativado de preenchimento automático e o arquivo autocomplete_data.js, que é incluído como parte do formulário de pesquisa ativado de preenchimento automático.
solution: Target
subtopic: Auto-Complete
title: Sobre a Conclusão Automática
topic-legacy: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
exl-id: a1d08c0a-6c68-4da2-88d2-fe953d333536
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 1%

---

# Sobre a Conclusão Automática{#about-auto-complete}

É possível configurar várias áreas de Preenchimento automático para controlar a geração do formulário de pesquisa ativado de preenchimento automático e o arquivo autocomplete_data.js, que é incluído como parte do formulário de pesquisa ativado de preenchimento automático.

## Sobre a Conclusão automática {#concept_093A9CD754864BA79B456FE4BEB64578}

O arquivo [!DNL autocomplete_data.js] é gerado novamente e publicado na rede de conteúdo de pesquisa sempre que há alterações que a página Configuração de Completar Automaticamente foi salva.

## Configuração da Conclusão Automática {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

Você pode configurar e configurar as opções que controlam a geração do formulário de pesquisa ativado de preenchimento automático e o arquivo.

<!-- 

t_configuring_auto-complete.xml

 -->

Depois de configurar o preenchimento automático, você pode exibir a fonte HTML resultante para revisão. A fonte HTML é o que você copia e cola nas páginas do seu site.

Consulte [Visualizar o formulário de pesquisa como ele apareceria em seu...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Consulte [Configurando a Lista de Palavras de Conclusão Automática](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

Consulte [Configuração do CSS de Conclusão Automática](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Para configurar a Conclusão automática**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. Na página [!DNL Auto-Complete Setup], defina as opções desejadas.

   Consulte também [Visualizar o formulário de pesquisa como ele apareceria em seu...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

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
      <td colname="col1"> <p>Caracteres de entrada mínimos </p> </td> 
      <td colname="col2"> <p>Especifica o número de caracteres que um cliente deve digitar no formulário de pesquisa de preenchimento automático antes de exibir sugestões. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máximo de entradas de cache </p> </td> 
      <td colname="col2"> <p>Especifica o número máximo de sugestões de preenchimento automático solicitadas anteriormente a serem armazenadas em cache no navegador do cliente. Geralmente, você deve deixar essa configuração no padrão de 1000. </p> <p>Embora você possa desativar completamente o armazenamento em cache do navegador definindo essa opção como 0, isso não é recomendado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do formulário </p> </td> 
      <td colname="col2"> <p>Especifica o atributo "name" da tag "form" do formulário de pesquisa habilitado para preenchimento automático. Por exemplo, </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>onde <span class="filepath"> SiteSearch </span> é o atributo name da tag form. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID da tag Div </p> </td> 
      <td colname="col2"> <p>Especifica o atributo ID da tag "div" do formulário de pesquisa habilitado para preenchimento automático. Por exemplo, </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>onde <span class="filepath"> preencher automaticamente </span> é o atributo da tag div. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID da tag de entrada </p> </td> 
      <td colname="col2"> <p>Especifica o atributo de ID da tag de "entrada" do formulário de pesquisa habilitado para preenchimento automático. Por exemplo, </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>onde <span class="filepath"> q </span> é o atributo id da tag de entrada. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Exibir sombra </p> </td>
      <td colname="col2"> <p>Adiciona uma sombra suspensa superficial à lista de sugestões de preenchimento automático. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Corresponder somente no início da frase </p> </td>
      <td colname="col2"> <p>Sugerir apenas resultados que correspondam ao início do texto de entrada. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Suporte para conjunto de caracteres UTF-8 </p> </td>
      <td colname="col2"> <p>Trata corretamente caracteres não ASCII em termos. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurando a Lista de Palavras de Conclusão Automática {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Configure a lista de palavras e frases que a opção Completar automaticamente exibe para um cliente como sugestões.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Consulte [Configuração da Conclusão Automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuração do CSS de Conclusão Automática](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Para configurar a Lista de Palavras de Completar Automaticamente**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. Na página [!DNL Auto-Complete Word List], defina as opções desejadas.

   Consulte [Visualizar o formulário de pesquisa como ele apareceria em seu...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

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
      <td colname="col2"> <p>Controla o número máximo de palavras e frases pesquisadas que serão incluídas na lista de palavras de preenchimento automático. As principais palavras e frases, que também são as mais populares, são incluídas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do campo </p> </td> 
      <td colname="col2"> <p>Cada nome de campo define o nome de um campo para o qual incluir valores indexados. Use + e - para adicionar ou remover nomes de campos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Contagem de Valores Máximos </p> </td> 
      <td colname="col2"> <p>Define a contagem máxima de valores de campo permitidos para o nome do campo selecionado. Os valores principais, que também são os mais referenciados, são incluídos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adicione estas palavras e frases </p> </td> 
      <td colname="col2"> <p> A lista de palavras de preenchimento automático é preenchida com as palavras e frases listadas nessa área. </p> <p> Clique em <span class="uicontrol"> Editar </span> para ver a lista ou para adicionar palavras e frases à lista. Quando terminar, clique em <span class="uicontrol"> Salvar alterações </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover estas palavras e frases </p> </td> 
      <td colname="col2"> <p> As entradas nessa área não são exibidas na lista de palavras de preenchimento automático. </p> <p> Clique em <span class="uicontrol"> Editar </span> para ver a lista ou para adicionar palavras e frases à lista. Quando terminar, clique em <span class="uicontrol"> Salvar alterações </span>. </p> <p> Expressões regulares são permitidas nesta lista. Para especificar uma expressão regular nessa lista, inicie a linha com <code>regexp</code> seguida por um único espaço, seguido pela expressão regular. Todas as linhas da lista de palavras que correspondem à expressão regular são removidas. </p> <p> <b>Importante</b>: Você só deve usar expressões regulares se tiver trabalhado com elas anteriormente em outros aplicativos. </p> <p>Consulte <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorar maiúsculas e minúsculas </p> </td> 
      <td colname="col2"> <p>São removidas entradas duplicadas na lista de palavras de preenchimento automático que diferem apenas por letras maiúsculas/minúsculas alfabéticas; todas as entradas da lista de palavras são forçadas a minúsculas. </p> <p>Se desejar que as sugestões de Preenchimento automático apareçam "primeira letra maiúscula" ou "todas maiúsculas", adicione a 
        <code>
          text-transform : capitalize; 
        </code> ou 
        <code>
          text-transform : uppercase; 
        </code> Propriedades de texto CSS para o conteúdo CSS de Completar automaticamente, em "/* estilos para o item de resultado */". </p> <p>Consulte <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> Configurando o CSS de Conclusão Automática </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Atualizar no reindexação </p> </td> 
      <td colname="col2"> <p>A lista de palavras de preenchimento automático é regenerada automaticamente após cada reindexação de conta bem-sucedida. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.
   * Clique em **[!UICONTROL Preview Word List]** para salvar as alterações feitas e abra a página [!DNL Auto-Complete Word List Preview], onde poderá revisar a lista de sugestões de preenchimento automático. Use as opções de navegação perto da parte superior da página para revisar e refinar a lista exibida. Quando terminar, clique em **[!UICONTROL Close]** para retornar à página [!DNL Auto-Complete Word List].

      Consulte [Usando a opção Histórico](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuração do CSS de Conclusão Automática {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Use o CSS de Completar Automaticamente para configurar a folha de estilos em cascata de preenchimento automático que deseja usar.

<!-- 

t_configuring_auto-complete_css.xml

 -->

O CSS de Completar automaticamente controla o conteúdo de [!DNL autocomplete_styles.css], que é incluído como parte do formulário de pesquisa ativado de preenchimento automático. O CSS especificado aqui controla a apresentação visual da lista de sugestão de preenchimento automático. Para obter um exemplo das ideias de apresentação visual possíveis, consulte o seguinte:

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[Configurando a Lista de Palavras de Preenchimento Automático](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

[Configuração da Conclusão Automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Quando você terminar de configurar o CSS de Completar Automaticamente, poderá visualizar o formulário de pesquisa para ver se o CSS especificado é aceitável na aparência e no layout.

Consulte [Visualizar o formulário de pesquisa como ele apareceria em seu...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Importante**: Para aplicar seu CSS personalizado de preenchimento automático, é necessário remover as tags de comentário da segunda linha que aparece no código HTML. Em seguida, mova a mesma linha para dentro da seção de cabeçalho da página que contém o formulário de pesquisa.

Consulte [Copiando o código HTML do formulário de pesquisa para o...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Para configurar o CSS de Conclusão Automática**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. No campo de texto [!DNL Auto-Complete CSS], cole ou digite as informações da folha de estilos em cascata que deseja associar à lista de sugestão de preenchimento automático.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualizar o formulário de pesquisa como ele apareceria em seu site {#task_437B35EFA5424603A08AF8E79E6B4714}

Com base na sua configuração de CSS de Preenchimento Automático e de Preenchimento Automático, você pode visualizar como o formulário de pesquisa será exibido se quiser adicionar o código HTML ao seu site.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Consulte [Configuração da Conclusão Automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuração do CSS de Conclusão Automática](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Consulte [Copiando o código HTML do formulário de pesquisa para o...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de coleções em formulários de pesquisa](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Consulte [Uso de quadros com formulários](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Amostra de formulário de pesquisa avançada](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Consulte [Código HTML do formulário de pesquisa avançada](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Consulte [Código do modelo de formulário de pesquisa avançada](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**Para visualizar o formulário de pesquisa como ele apareceria em seu site**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Opcional) Clique em **[!UICONTROL HTML code]** para ver o HTML que você copia e cola nas páginas do seu site.

## Copiando o código HTML do formulário de pesquisa nas páginas do seu site {#task_A3A01EA800F24C0AA33902387E0362C7}

Com base na sua configuração de CSS de Preenchimento Automático e de Preenchimento Automático, você pode visualizar como o formulário de pesquisa será exibido se quiser adicionar o código HTML ao seu site.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Consulte [Configuração da Conclusão Automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuração do CSS de Conclusão Automática](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Consulte [Copiando o código HTML do formulário de pesquisa para o...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de coleções em formulários de pesquisa](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Consulte [Uso de quadros com formulários](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Amostra de formulário de pesquisa avançada](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Consulte [Código HTML do formulário de pesquisa avançada](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Consulte [Código do modelo de formulário de pesquisa avançada](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**Para copiar o código HTML do formulário de pesquisa nas páginas do seu site**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >Não altere o valor `form name=` na origem do formulário.

1. (Opcional) Siga um destes procedimentos:

   * Se você tiver configurado o CSS de preenchimento automático e quiser que os estilos sejam aplicados ao formulário de pesquisa, remova as tags de comentário da segunda linha exibida no código HTML. Em seguida, mova a mesma linha para dentro da seção de cabeçalho da página que contém o formulário de pesquisa.
   * Para obter o máximo desempenho, mova as tags listadas na parte inferior do código HTML e coloque-as na parte inferior da seção de corpo de cada página que contém o formulário de pesquisa.

1. Copie o código e cole-o nas páginas da Web do seu site, onde deseja que o formulário de pesquisa apareça.
