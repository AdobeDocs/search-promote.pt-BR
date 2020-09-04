---
description: Use o menu Pesquisa para definir palavras, coleções, restrições, pré-visualização e quadros excluídos.
seo-description: Use o menu Pesquisa para definir palavras, coleções, restrições, pré-visualização e quadros excluídos.
seo-title: Sobre o menu Pesquisar
solution: Target
subtopic: Searching
title: Sobre o menu Pesquisar
topic: Settings,Site search and merchandising
uuid: 072111fc-a32b-4acb-8337-cb21bcdb5542
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '11182'
ht-degree: 1%

---


# Sobre o menu Pesquisar{#about-the-searching-menu}

Use o menu Pesquisa para definir palavras, coleções, restrições, pré-visualização e quadros excluídos.

## Sobre pesquisas {#concept_207105CF26B1448F8A3D223787C56AB8}

Você pode usar Pesquisas para definir e personalizar as pesquisas nomeadas que seus modelos de apresentação podem referenciar.

<!-- 

c_about_searches.xml

 -->

No modelo de apresentação, é possível fazer referência a qualquer pesquisa nomeada definida no módulo Pesquisas. Por sua vez, isso permite que você personalize facilmente o tipo de pesquisa que é feita para um determinado conjunto de modelos.

Para excluir frases usadas com frequência e palavras comuns dos resultados da pesquisa, consulte [Configuração de palavras](../c-about-linguistics-menu/c-about-excluded-words.md#task_60BF6BB7A66C48479D2BBB32C0F38CDE)excluídas.

Para definir áreas específicas e pesquisáveis do seu site, consulte [Adicionar coleções](../c-about-settings-menu/c-about-searching-menu.md#task_07732D0F00104E59AD421297A704B2F6).

Para especificar um quadro de público alvo para links de resultados de pesquisa, consulte [Uso de quadros com formulários](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Para restringir pesquisas com base na quem indicou HTTP, endereço IP ou esquema de solicitação (HTTP ou HTTPS), consulte [Configuração de valores na Pré-visualização](../c-about-settings-menu/c-about-searching-menu.md#task_CE267A0FF621474E80AB43B67B1C28D7).

## Dicas de pesquisa {#section_22F0E2BCF259459FA5F49FBCC0F09A7C}

Para obter resultados de pesquisa mais específicos, você pode usar as seguintes dicas de pesquisa.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Dica de pesquisa </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verificar ortografia </p> </td> 
   <td colname="col2"> <p>Certifique-se de que seus termos de pesquisa estejam escritos corretamente. Se a Correspondência com <span class="uicontrol"> som semelhante </span> estiver ativada em <span class="uicontrol"> Linguística </span> &gt; <span class="uicontrol"> Palavras e idiomas </span>, o mecanismo de pesquisa tentará encontrar palavras que soem semelhantes aos seus termos de pesquisa. No entanto, é sempre melhor tentar soletrar os termos de pesquisa corretamente. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Sobre Palavras e Idioma </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar várias palavras </p> </td> 
   <td colname="col2"> <p>Exemplo: 
     <code>
       our free product 
     </code> </p> <p>Query de várias palavras retornam resultados mais refinados do que query de uma única palavra. </p> <p>Por exemplo, <code>
       our free product 
     </code> retorna resultados mais relevantes do que apenas <code>
       product 
     </code>. </p> <p>Lembre-se de que os resultados relevantes são retornados mesmo que não contenham todos os termos de query. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar palavras semelhantes </p> </td> 
   <td colname="col2"> <p>Exemplo: 
     <code>
       safe secure privacy security 
     </code> </p> <p>Quanto mais palavras semelhantes forem usadas em um query de pesquisa, mais relevantes serão os resultados da pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar capitalização apropriada </p> </td> 
   <td colname="col2"> <p>Exemplo: 
     <code>
       Search Template Reference 
     </code> </p> <p>Coloque os substantivos corretos em maiúsculas. Se você usar uma palavra em minúsculas, o mecanismo de pesquisa corresponderá a qualquer caso da palavra. </p> <p>Por exemplo, se você digitar <code>
       search 
     </code>, o mecanismo de pesquisa retornará todos os documentos que contêm as palavras "pesquisa", "Pesquisa" e "PESQUISA". No entanto, se você digitar <code>
       Search 
     </code>, o mecanismo de pesquisa retornará documentos que contenham apenas a palavra em maiúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar aspas </p> </td> 
   <td colname="col2"> <p>Exemplo: 
     <code>
       "our pledge to you" 
     </code> </p> <p>Use aspas para localizar palavras que devem aparecer adjacentes, como "nossa promessa para você". Sem as citações adjacentes, os resultados da pesquisa incluem as palavras "nosso", "compromisso", "para" e "você", mas não necessariamente nessa ordem. Em vez disso, as palavras podem aparecer em qualquer lugar, e em qualquer ordem, dentro do documento. </p> <p> se você estiver usando o Formulário de pesquisa avançada com botões de opção para <span class="uicontrol"> qualquer </span>, <span class="uicontrol"> todos </span>e <span class="uicontrol"> frase </span>, você só poderá usar aspas quando <span class="uicontrol"> houver alguma </span> selecionada. As aspas são ignoradas se <span class="uicontrol"> toda </span> a frase ou a <span class="uicontrol"> frase </span> estiver selecionada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar + (mais) ou - (menos) </p> </td> 
   <td colname="col2"> <p>Exemplo: 
     <code>
       +"template language" 
     </code> </p> <p>Use + para indicar que um termo de pesquisa ou frase deve aparecer nos resultados da pesquisa. </p> <p>Usar - para indicar que um termo de pesquisa ou frase deve estar ausente dos resultados da pesquisa. </p> <p>Você deve conter uma frase entre aspas. Não deixe espaços entre o sinal de mais ou menos e o termo de pesquisa, como no exemplo acima. </p> <p> se você estiver usando o Formulário de pesquisa avançada com botões de opção para <span class="uicontrol"> qualquer </span>, <span class="uicontrol"> todos </span>e <span class="uicontrol"> frase </span>, você só poderá usar aspas quando <span class="uicontrol"> houver alguma </span> selecionada. Os modificadores de mais e menos serão ignorados se <span class="uicontrol"> toda a </span> frase ou <span class="uicontrol"> frase </span> for selecionada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar pesquisas de campo </p> </td> 
   <td colname="col2"> <p>Exemplos: </p> <p> 
     <ul id="ul_F7CFF7652894402E8D19D6BA49792530"> 
      <li id="li_27492EF933C5437CB2C499746EC8CF39"> 
       <code>
         title:about 
       </code> </li> 
      <li id="li_BD21505122104FD0B16A4DAD777811DA"> 
       <code>
         desc:"Our Team" 
       </code> </li> 
      <li id="li_8264630F8B3D46BF872EFEB1D69DB6BE"> 
       <code>
         keys:login 
       </code> </li> 
      <li id="li_EBB81CBFC6DA45E99A524890DCD56E9F"> 
       <code>
         body:security 
       </code> </li> 
      <li id="li_6A852E35D6984A2C94144AB6C6D2DFA0"> 
       <code>
         alt:"join now" 
       </code> </li> 
      <li id="li_F4C5699360484D12ACD62BBFB84A7904"> 
       <code>
         url:help 
       </code> </li> 
      <li id="li_B2DBBA2239E74D98868D92B3EDEF5B51"> 
       <code>
         target:Adobe 
       </code> </li> 
     </ul> </p> <p>Pesquisas de campo permitem criar pesquisas específicas para palavras que aparecem em uma parte específica de um documento. </p> <p>Você pode realizar uma pesquisa de campo em texto de corpo (corpo:), texto do título (título:), texto alternativo (alt:), descrição meta (desc:), palavras-chave meta (chaves:), URL (url:) ou palavras-chave de público alvo meta (público alvo:). Use minúsculas para o nome do campo e imediatamente seguidas por dois pontos. Não há espaços entre o dois pontos e o termo de pesquisa. </p> <p>As pesquisas de campo são seguidas apenas por uma palavra ou frase. As frases devem estar entre aspas. </p> <p>se você estiver usando o Formulário de pesquisa avançada com uma caixa de lista para o nome do campo, você só poderá inserir nomes de campo antes de uma palavra ou frase quando <span class="uicontrol"> alguma </span> estiver selecionada. Nomes de campos específicos serão ignorados se qualquer outro campo do Formulário de pesquisa avançada estiver selecionado na caixa lista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar curingas </p> </td> 
   <td colname="col2"> <p>Exemplos: </p> <p> 
     <ul id="ul_D8E3867EB15641B0A6E55AD546CCB4DD"> 
      <li id="li_CB8B8FC15EB14B13BB33BB69F5206303"> 
       <code>
         wh* 
       </code> </li> 
      <li id="li_5350A934648C4C81BD6C0875061B426B"> 
       <code>
         "wh* are" 
       </code> </li> 
      <li id="li_7965A2F7186F40039D2F0736299D11B1"> 
       <code>
         415-*-* 
       </code> </li> 
     </ul> </p> <p>Pesquisas curingas expandem o número de correspondências para uma solicitação específica. O caractere * é usado como caractere curinga. </p> <p>Por exemplo, procurar por <code>
       wh* 
     </code> encontra as palavras "o que", "porquê", "quando", "se" e qualquer outra palavra que se start com "o". Procurando por *her* encontra as palavras "aqui", "se", "junto", "juntando" e qualquer outra palavra que contenha "ela" em qualquer lugar dentro da palavra. </p> <p>É possível combinar curingas com modificadores + e -, aspas para frases, bem como os especificadores de pesquisa de campo. </p> <p>A pesquisa <code>
       +wh* -se*ch 
     </code> localiza todas as páginas que têm uma palavra que se start com "wh" e não contém uma palavra que se start com "se" e termina com "ch". </p> <p>A pesquisa <code>
       "wh* are" 
     </code> encontra as frases "onde estão", "o que estão", "por que estão", e assim por diante. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adicionar uma nova definição de pesquisa {#task_98D3A168AB5D4F30A1ADB6E0D48AB648}

Você pode usar o [!DNL GS Add Search] painel para configurar e adicionar uma nova definição de pesquisa para seus componentes de Pesquisa guiada, como facetas, navegações estruturais, navegação de página, menus e pesquisas recentes, na camada de apresentação.

<!-- 

t_adding_a_new_definition.xml

 -->

Depois de adicionar a nova definição de pesquisa, certifique-se de referenciá-la no modelo de apresentação para que seja exibida.

Consulte [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para adicionar uma nova definição de pesquisa**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. Na [!DNL Searches] página, clique em **[!UICONTROL Add New Search]**.
1. Na **[!UICONTROL GS Add Search]** página, defina as opções desejadas.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   Observe que as regras de processamento que selecionam o modelo de apresentação podem substituir algumas dessas opções.

   Consulte [Adicionar uma nova definição](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) de pesquisa ou [Editar uma definição](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)de pesquisa.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome da pesquisa </p> </td> 
      <td colname="col2"> <p>Identifica o nome da pesquisa definida. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fonte </p> </td> 
      <td colname="col2"> <p>Permite que você selecione a pesquisa de back-end que deseja usar. Você pode selecionar entre <span class="wintitle"> SiteSearch </span> ou <span class="wintitle"> Merchandising </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Conta </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Permite que você selecione a conta de pesquisa/comercialização do site que deseja pesquisar. Geralmente, uma pesquisa pesquisa na conta que você está usando no momento. Entretanto, o modelo de apresentação pode usar uma pesquisa de back-end para qualquer uma de suas outras contas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do servidor/IP </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Merchandising </span> como sua fonte. </p> <p>Especifica o nome completo do <span class="wintitle"> servidor de comercialização </span> que a <span class="wintitle"> pesquisa de comercialização </span> deve acessar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Porta do servidor </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Merchandising </span> como sua fonte. </p> <p>Especifica o número da porta do <span class="wintitle"> Merchandising </span> Server. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pirâmide </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Merchandising </span> como sua fonte. </p> <p>Especifica a pirâmide dentro do <span class="wintitle"> servidor de comercialização </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de resultados </p> </td> 
      <td colname="col2"> <p>Especifica o número de resultados de pesquisa que você deseja que sejam retornados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de resultados da primeira página (se for diferente) </p> </td> 
      <td colname="col2"> <p>Especifica o número de resultados que são retornados na primeira página. Use essa opção se precisar diferenciá-la das outras páginas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de colunas </p> </td> 
      <td colname="col2"> <p>Especifica o número de colunas nas quais os resultados da pesquisa são divididos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo De Pesquisa </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Permite selecionar entre os três tipos de pesquisa a seguir. </p> <p> 
        <ul id="ul_2F6FA9EFD8DB49EEAB866C3D070E2644"> 
          <li id="li_ECFEBEDD86FF4DE2BB768423B3B91B5E"> <span class="uicontrol"> todas </span> <p>Procura documentos que contenham todas as palavras na string do query. </p> <p>O uso de "+" e "-" antes das palavras de pesquisa serem desativadas e esses caracteres forem ignorados. </p> </li> 
          <li id="li_62EB215BDDE74DF0BF76B3BD5B96776F"> <span class="uicontrol"> qualquer </span> <p>O uso de prefixos de palavras "+" e "-" é permitido. </p> </li> 
          <li id="li_3D71982C0BBA41AFA353069AF3F2F6D8"> <span class="uicontrol"> frase </span> <p>A string de query é tratada como se fosse uma frase entre aspas, e todas as aspas digitadas pelo usuário são ignoradas. </p> <p>O uso de "+" e "-" antes das palavras de pesquisa serem desativadas e esses caracteres forem ignorados. </p> </li> 
        </ul> </p> <p> Se você quiser que cada palavra em um query selecione potencialmente um valor de faceta, então sua pesquisa principal sempre deve usar <span class="uicontrol"> tudo </span>. </p> <p>Você pode revisar dicas de pesquisa relacionadas ao uso dos modificadores + e - em um query de pesquisa. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Sobre pesquisadores </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Coleção </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Identifica a coleção dentro do índice que você deseja pesquisar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Permite usar uma seleção aleatória dos resultados da pesquisa, dependendo do <span class="uicontrol"> Número de resultados </span> que você especificou. </p> <p>A busca promocional é um conceito legado. Dessa forma, recomendamos que você use o novo sistema de gerenciamento de banner dentro da pesquisa/comercialização do site. </p> <p>Consulte <a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">Sobre banners </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aplicar parâmetros de aspecto </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte e selecionar <span class="uicontrol"> Pesquisa promocional </span>. </p> <p>Especifica que uma pesquisa promocional use as facetas selecionadas para restringir as promoções. A maioria das contas promosearch não usam essa opção. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fornecer promoção padrão se nenhuma promoção correspondente </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte e selecionar <span class="uicontrol"> Pesquisa promocional </span>. </p> <p>Especifica que outra pesquisa por uma promoção ocorre se a pesquisa inicial por uma promoção não encontrar nada. A segunda pesquisa por uma promoção ignora a palavra-chave. Em vez disso, ele procura qualquer promoção em que um campo de metadados "is_default" esteja definido como "yes". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Realçar pesquisa </p> </td> 
      <td colname="col2"> <p>Puxa um número selecionado de resultados da pesquisa principal que você deseja destacar em uma "zona-herói". </p> <p>Normalmente, as pesquisas de realce têm critérios de pesquisa semelhantes à pesquisa principal, mas com um mecanismo de classificação diferente para realçar determinados resultados. O software remove os duplicados da pesquisa principal. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisa básica </p> </td> 
      <td colname="col2"> <p>Esta opção só está disponível se você selecionou <span class="uicontrol"> Realçar pesquisa </span>. </p> <p>Permite selecionar a pesquisa que tem os resultados dos quais você está destacando. Duplicados são removidos desta pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prioridade DeDupe </p> </td> 
      <td colname="col2"> <p>Esta opção só está disponível se você selecionou <span class="uicontrol"> Realçar pesquisa </span>. </p> <p>Permite que você tenha várias pesquisas de realce. </p> <p>Quando você tem várias pesquisas de realce, é necessário especificar a prioridade da eliminação da duplicação, onde "1" é a prioridade mais alta. </p> <p>Por exemplo, suponha que você tenha duas pesquisas de realce: best-sellers e novos produtos. Teoricamente. é possível que um best-seller seja também um novo produto. Nesse caso, você deseja que o duplicado seja removido dos novos produtos e da pesquisa principal. Portanto, você define a prioridade dos best-sellers como 1 e a prioridade dos novos produtos como 2. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro </p> </td> 
      <td colname="col2"> <p>Permite adicionar parâmetros CGI à pesquisa. </p> <p>Consulte <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> Parâmetros CGI de pesquisa de backend </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Na [!DNL Searches] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma definição de pesquisa {#task_AF1FFB1AEF874C13AB359C28F74BF461}

Você pode usar o [!DNL Staged GS Edit Search] painel para reconfigurar uma definição de pesquisa existente para a camada de apresentação da Pesquisa guiada.

<!-- 

t_editing_a_search_definition.xml

 -->

Depois de editar a definição de pesquisa, certifique-se de tê-la referenciado no modelo de apresentação para que seja exibido.

Consulte [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para editar uma definição de pesquisa**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. Na [!DNL Searches] página, na tabela, clique **[!UICONTROL Edit]** na linha da definição que deseja alterar.
1. Na **[!UICONTROL GS Edit Search]** página, defina as opções desejadas.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   Observe que as regras de processamento que selecionam o modelo de apresentação podem substituir algumas dessas opções.

   Consulte [Adicionar uma nova definição](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) de pesquisa ou [Editar uma definição](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)de pesquisa.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome da pesquisa </p> </td> 
      <td colname="col2"> <p>Identifica o nome da pesquisa definida. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fonte </p> </td> 
      <td colname="col2"> <p>Permite que você selecione a pesquisa de back-end que deseja usar. Você pode selecionar entre <span class="wintitle"> SiteSearch </span> ou <span class="wintitle"> Merchandising </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Conta </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Permite que você selecione a conta de pesquisa/comercialização do site que deseja pesquisar. Geralmente, uma pesquisa pesquisa na conta que você está usando no momento. No entanto, o modelo de apresentação pode usar uma pesquisa de back-end para qualquer uma de suas outras contas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do servidor/IP </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Merchandising </span> como sua fonte. </p> <p>Especifica o nome completo do <span class="wintitle"> servidor de comercialização </span> que a <span class="wintitle"> pesquisa de comercialização </span> deve acessar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Porta do servidor </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Merchandising </span> como sua fonte. </p> <p>Especifica o número da porta do <span class="wintitle"> Merchandising </span> Server. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pirâmide </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Merchandising </span> como sua fonte. </p> <p>Especifica a pirâmide dentro do <span class="wintitle"> servidor de comercialização </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de resultados </p> </td> 
      <td colname="col2"> <p>Especifica o número de resultados de pesquisa que você deseja que sejam retornados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de resultados da primeira página (se for diferente) </p> </td> 
      <td colname="col2"> <p>Especifica o número de resultados que são retornados na primeira página. Use essa opção se precisar diferenciá-la das outras páginas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de colunas </p> </td> 
      <td colname="col2"> <p>Especifica o número de colunas nas quais os resultados da pesquisa são divididos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo De Pesquisa </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Permite selecionar entre os três tipos de pesquisa a seguir. </p> <p> 
        <ul id="ul_E1D8B3DE9DB24DE4813D53F6298A03A6"> 
          <li id="li_C3DD7AA7699B477A9EE0731CFC012630"> <span class="uicontrol"> todas </span> <p>Procura documentos que contenham todas as palavras na string do query. </p> <p>O uso de "+" e "-" antes das palavras de pesquisa serem desativadas e esses caracteres forem ignorados. </p> </li> 
          <li id="li_4C66B9EFEFA042908A4D3730F9F54EB0"> <span class="uicontrol"> qualquer </span> <p>O uso de prefixos de palavras "+" e "-" é permitido. </p> </li> 
          <li id="li_37E9AD42A61C4E31A0816DFB8E71118D"> <span class="uicontrol"> frase </span> <p>A string de query é tratada como se fosse uma frase entre aspas, e todas as aspas digitadas pelo usuário são ignoradas. </p> <p>O uso de "+" e "-" antes das palavras de pesquisa serem desativadas e esses caracteres forem ignorados. </p> </li> 
        </ul> </p> <p> Se você quiser que cada palavra em um query selecione potencialmente um valor de faceta, então sua pesquisa principal sempre deve usar <span class="uicontrol"> tudo </span>. </p> <p>Você pode revisar dicas de pesquisa relacionadas ao uso dos modificadores + e - em um query de pesquisa. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Sobre pesquisadores </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Coleção </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Identifica a coleção dentro do índice que você deseja pesquisar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte. </p> <p>Permite usar uma seleção aleatória dos resultados da pesquisa, dependendo do <span class="uicontrol"> Número de resultados </span> que você especificou. </p> <p>A busca promocional é um conceito legado. Dessa forma, recomendamos que você use o novo sistema de gerenciamento de banner dentro da pesquisa/comercialização do site. </p> <p>Consulte <a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">Sobre banners </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aplicar parâmetros de aspecto </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte e selecionar <span class="uicontrol"> Pesquisa promocional </span>. </p> <p>Especifica que uma pesquisa promocional use as facetas selecionadas para restringir as promoções. A maioria das contas promosearch não usam essa opção. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fornecer promoção padrão se nenhuma promoção correspondente </p> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher <span class="uicontrol"> Search &amp; Promote </span> como sua fonte e selecionar <span class="uicontrol"> Pesquisa promocional </span>. </p> <p>Especifica que outra pesquisa por uma promoção ocorre se a pesquisa inicial por uma promoção não encontrar nada. A segunda pesquisa por uma promoção ignora a palavra-chave. Em vez disso, ele procura qualquer promoção em que um campo de metadados "is_default" esteja definido como "yes". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Realçar pesquisa </p> </td> 
      <td colname="col2"> <p>Puxa um número selecionado de resultados da pesquisa principal que você deseja destacar em uma "zona-herói". </p> <p>Normalmente, as pesquisas de realce têm critérios de pesquisa semelhantes à pesquisa principal, mas com um mecanismo de classificação diferente para realçar determinados resultados. O software remove os duplicados da pesquisa principal. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisa básica </p> </td> 
      <td colname="col2"> <p>Esta opção só está disponível se você selecionou <span class="uicontrol"> Realçar pesquisa </span>. </p> <p>Permite selecionar a pesquisa que tem os resultados dos quais você está destacando. Duplicados são removidos desta pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prioridade DeDupe </p> </td> 
      <td colname="col2"> <p>Esta opção só está disponível se você selecionou <span class="uicontrol"> Realçar pesquisa </span>. </p> <p>Permite que você tenha várias pesquisas de realce. </p> <p>Quando você tem várias pesquisas de realce, é necessário especificar a prioridade da eliminação da duplicação, onde "1" é a prioridade mais alta. </p> <p>Por exemplo, suponha que você tenha duas pesquisas de realce: best-sellers e novos produtos. Teoricamente. é possível que um best-seller seja também um novo produto. Nesse caso, você deseja que o duplicado seja removido dos novos produtos e da pesquisa principal. Portanto, você define a prioridade dos best-sellers como 1 e a prioridade dos novos produtos como 2. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro </p> </td> 
      <td colname="col2"> <p>Permite adicionar parâmetros CGI à pesquisa. </p> <p>Consulte <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> Parâmetros CGI de pesquisa de backend </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Na [!DNL Searches] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma definição de pesquisa {#task_1D8E991E4C4146B7A7311FAE5DAA3742}

Você pode excluir uma definição de pesquisa de guia que não é mais necessária ou não é mais usada.

<!-- 

t_deleting_a_search_definition.xml

 -->

Consulte [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para excluir uma definição de pesquisa**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. Na [!DNL Searches] página, na tabela, clique **[!UICONTROL Delete]** na linha da definição que deseja remover.
1. Na caixa de [!DNL Confirmation] diálogo, clique em **[!UICONTROL OK]**.
1. (Opcional) Na [!DNL Searches] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre o Gerenciador de Palavras-Chave de Resultados Fixos {#concept_0C5F152C029C485D8872C6795CBCD7C7}

É possível prender manualmente os resultados da pesquisa em um local específico. Esses resultados fixados estão associados a um query de pesquisa ou palavras-chave específicos. Você pode usar [!DNL Pinned Result Keyword Manager] para gerenciar todas as palavras-chave com resultados fixados.

<!-- 

c_about_pinned_results_keyword_manager.xml

 -->

## Regras de pesquisa de palavra-chave a serem seguidas {#section_ED67A24BE884468286F34FA5DFF826D7}

O query de pesquisa inserido no painel tem as seguintes regras:

* Os espaços à esquerda e à direita são excluídos do query.
* Nenhum caractere de pesquisa especial é permitido, como o seguinte:

   * Correspondência curinga com asteriscos (*).
   * Nenhum must-have ou must-not-have está usando mais ou menos (+ ou -).
   * Nenhum especificador de campo com o caractere de dois pontos (:).
   * Sem vírgulas ou aspas de duplo (, ou &quot;).

* Vários termos ou palavras separadas por espaços no query são permitidos.
* Letras maiúsculas são convertidas em letras minúsculas.

Os termos de pesquisa são memorizados exatamente como estão; você deve usar os mesmos termos de pesquisa novamente para obter os mesmos resultados exatos.

Os resultados fixados não suportam distinção entre maiúsculas e minúsculas. Todas as palavras-chave têm letras maiúsculas convertidas em letras minúsculas.

## Reordenação dos resultados da pesquisa {#section_46FBE5279C7740A09D6DC9F54FE104AA}

Quando você pesquisa uma palavra-chave no [!DNL Stage Add New Keyword] painel ou no [!DNL Staged Edit Keyword] painel, os resultados da pesquisa refletem o que pode acontecer após a próxima operação de índice. Você pode reordenar os resultados da pesquisa na tabela usando um dos três métodos diferentes.

O primeiro método é usar a **[!UICONTROL Pinned]** caixa de seleção. A caixa de seleção é usada para fixar um resultado a uma posição específica. Quando você seleciona a caixa de seleção, todos os resultados da pesquisa acima da caixa de seleção também são fixados. Essa funcionalidade garante que todos os resultados acima dessa caixa de seleção sejam exibidos nessa ordem específica. Desvincular um resultado de pesquisa faz com que ele caia abaixo de todos os resultados atualmente fixados.

O segundo método é usar o recurso arrastar e soltar na tabela. É possível mover um resultado para uma nova posição com o recurso arrastar e soltar. Depois de arrastar um resultado para um novo local, todos os resultados acima do novo local são fixados. Esse pinning automático garante que o restante dos resultados aparecerão acima do resultado arrastado recentemente.

O terceiro método é definir a ordem dos resultados fixados digitando uma posição específica na coluna &quot;#&quot;. Ao contrário do recurso arrastar e soltar, a ordem dos resultados da pesquisa simulada só será óbvia na próxima vez que você abrir o [!DNL Staged Edit Keyword] painel. A definição do número do pedido para uma linha atualmente não fixada garante que pelo menos muitos itens sejam fixados. A definição do número do pedido para uma linha atualmente fixada define a ordem desse item dentro dos itens atualmente fixados. No entanto, não aumenta o número de itens fixados.

Ao salvar os resultados da pesquisa, você pode visualização os resultados novamente inserindo exatamente o mesmo query no campo Palavra-chave.

## Sobre os resultados de pesquisa fixados {#section_46780B7812F249F3B45503161C4FBDEE}

Os resultados da pesquisa são geralmente ordenados pela pontuação de relevância. No entanto, um resultado de pesquisa fixado ignora a pontuação de relevância e tenta substituir a ordem natural pela posição predeterminada. Ao garantir que o resultado permaneça relativamente onde está, outros resultados de pesquisa conhecidos acima dele precisam ser fixados.

Os resultados da pesquisa exibidos no painel simulam o que aparece depois do próximo índice. No entanto, as alterações do documento original ou determinadas alterações de configuração no Centro-Membro podem produzir resultados com discrepâncias. Por exemplo, a alteração do conteúdo de um documento não é conhecida até depois do índice.

Os resultados fixados aparecem em uma ordem semelhante ou igual após o índice, pois ignoram a relevância. Os resultados não fixados regressam à sua posição natural após um índice; a ordem dos resultados não fixados não é garantida.

## Adding a new keyword {#task_8CED128DADD34D0DAD2C64B64D0D6B06}

É possível adicionar novas palavras-chave e seus resultados fixados.

<!-- 

t_adding_a_new_keyword.xml

 -->

No momento em que você adiciona uma nova palavra-chave, é possível reordenar os resultados da pesquisa e fixá-los em uma posição específica.

**Para adicionar uma nova palavra-chave**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. Na [!DNL Pinned Keyword Results Manager] página, clique em **[!UICONTROL Add New Keyword]**.
1. Na [!DNL Add New Keyword] página, no **[!UICONTROL Keyword]** campo, digite um query de pesquisa e clique em **[!UICONTROL Search Keyword]**.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   Você pode usar o botão Editar tabela para ajustar como visualização a tabela de resultados de pesquisa. Por exemplo, você pode usar a lista de colunas para revelar ou ocultar colunas específicas. Também é possível reorganizar a ordem das colunas usando o recurso arrastar e soltar.

   A tabela a seguir descreve as propriedades da coluna que estão no editor de tabela.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Coluna </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p>Especifica a ordem numérica da aparência das colunas. Você pode arrastar e soltar as colunas para atualizar automaticamente a ordem. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do campo </p> </td> 
      <td colname="col2"> <p>Identifica o nome do cabeçalho da coluna que aparece na <span class="wintitle"> tabela Resultados de pesquisa </span> simulada do <span class="wintitle"> painel Adicionar nova palavra-chave </span> encenada <span class="wintitle"> e do painel Editar palavra-chave </span> encenada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir </p> </td> 
      <td colname="col2"> <p>A coluna será exibida na Tabela de resultados fixados se a caixa estiver marcada. Se a caixa estiver vazia ou desmarcada, a coluna desaparecerá da tabela. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Exibir URL como imagem </p> </td> 
      <td colname="col2"> <p>Se o campo meta atribuído a essa coluna tiver URLs para gráficos ou imagens, marcar essa caixa coloca tags de imagem HTML ao seu redor e a imagem é exibida. As imagens ausentes ou os links inválidos estão vazios. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Extensão do campo </p> </td> 
      <td colname="col2"> <p>Permite que você insira o comprimento máximo do texto para exibição antes que ele seja truncado com elipses (...). Se a coluna estiver definida para exibir URLs como imagens, esse campo não terá efeito. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Execute um dos procedimentos a seguir:

   * Reordene os resultados da pesquisa.
   * Clique **[!UICONTROL Edit Table]** para ajustar a visualização da [!DNL Simulated Search Results] tabela. Quando terminar, clique em **[!UICONTROL Save Changes]** para retornar ao [!DNL Add New Keyword] painel.

1. Clique em **[!UICONTROL Save Search Results]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)de preparo.
1. (Opcional) Na [!DNL Pinned Results Keyword Manager] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma palavra-chave {#task_30C550A7350B4394B5B43536368A84B1}

É possível editar palavras-chave existentes e seus resultados fixados.

<!-- 

t_editing_a_keyword.xml

 -->

Ao editar uma palavra-chave, você pode reordenar os resultados da pesquisa e fixá-los em uma posição específica.

**Para editar uma palavra-chave**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. Na [!DNL Pinned Keyword Results Manager] página, na tabela, clique **[!UICONTROL Edit]** na linha da palavra-chave que você deseja alterar.
1. Na [!DNL Edit Keyword] página, no **[!UICONTROL Keyword]** campo, digite um query de pesquisa e clique em **[!UICONTROL Search Keyword]**.

   Certifique-se de seguir as regras para a pesquisa de palavra-chave.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   Você pode usar o botão Editar tabela para ajustar como visualização a tabela de resultados de pesquisa. Por exemplo, você pode usar a lista de colunas para revelar ou ocultar colunas específicas. Também é possível reorganizar a ordem das colunas usando o recurso arrastar e soltar.

   A tabela a seguir descreve as propriedades da coluna que estão no editor de tabela.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Coluna </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p>Especifica a ordem numérica da aparência das colunas. Você pode arrastar e soltar as colunas para atualizar automaticamente a ordem. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do campo </p> </td> 
      <td colname="col2"> <p>Identifica o nome do cabeçalho da coluna que aparece na <span class="wintitle"> tabela Resultados de pesquisa </span> simulada do <span class="wintitle"> painel Adicionar nova palavra-chave </span> encenada <span class="wintitle"> e do painel Editar palavra-chave </span> encenada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir </p> </td> 
      <td colname="col2"> <p>A coluna será exibida na Tabela de resultados fixados se a caixa estiver marcada. Se a caixa estiver vazia ou desmarcada, a coluna desaparecerá da tabela. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Exibir URL como imagem </p> </td> 
      <td colname="col2"> <p>Se o campo meta atribuído a essa coluna tiver URLs para gráficos ou imagens, marcar essa caixa coloca tags de imagem HTML ao seu redor e a imagem é exibida. As imagens ausentes ou os links inválidos estão vazios. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Extensão do campo </p> </td> 
      <td colname="col2"> <p>Permite que você insira o comprimento máximo do texto para exibição antes que ele seja truncado com elipses (...). Se a coluna estiver definida para exibir URLs como imagens, esse campo não terá efeito. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Execute um dos procedimentos a seguir:

   * Reordene os resultados da pesquisa.
   * Clique **[!UICONTROL Edit Table]** para ajustar a visualização da [!DNL Simulated Search Results] tabela.

      Consulte [Adicionar uma nova palavra-chave](../c-about-settings-menu/c-about-searching-menu.md#task_8CED128DADD34D0DAD2C64B64D0D6B06).

      Quando terminar, clique em **[!UICONTROL Save Changes]** para retornar ao [!DNL Add New Keyword] painel.

1. Clique em **[!UICONTROL Save Search Results]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)de preparo.
1. (Opcional) Na [!DNL Pinned Results Keyword Manager] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma palavra-chave {#task_F17D6357D6DD416495E6D4117899D81D}

É possível excluir palavras-chave que não são mais necessárias ou não são usadas.

<!-- 

t_deleting_a_keyword.xml

 -->

No momento em que você adiciona uma nova palavra-chave, é possível reordenar os resultados da pesquisa e fixá-los em uma posição específica.

**Para excluir uma palavra-chave**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. Na [!DNL Pinned Keyword Results Manager] página, na tabela, clique **[!UICONTROL Delete]** na linha da palavra-chave que deseja remover.
1. Na [!DNL Delete Keyword] página, clique em **[!UICONTROL Delete]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)de preparo.
1. (Opcional) Na [!DNL Pinned Results Keyword Manager] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre coleções {#concept_62E42ACE53D54EEE9273433B86259127}

Você pode usar Coleções para permitir que os clientes pesquisem áreas específicas de um site para que possam encontrar rapidamente o que estão procurando.

<!-- 

c_about_collections.xml

 -->

Consulte [Sobre pesquisadores](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

Consulte [Uso de coleções em formulários](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de pesquisa.

Por exemplo, os clientes podem pesquisar uma coleção de URLs relacionados às vendas de produtos ou aos serviços de suporte. Antes que os clientes possam usar as coleções especificadas, atualize o formulário de pesquisa no menu Formulário de pesquisa.

Antes que os efeitos das configurações de Coleções fiquem visíveis para os clientes, recrie o índice do site.

Você pode testar suas coleções digitando um dos URLs do site no campo opcional **[!UICONTROL Test Collections]** e clicando em **[!UICONTROL Test]**. A coleção à qual a página especificada pertence é retornada.

Cada coleção é especificada em uma única linha com um nome e uma máscara de URL. Uma máscara de URL pode consistir no seguinte:

* um caminho completo, como `https://www.mydomain.com/products.html`
* um caminho parcial, como `https://www.mydomain.com/products`
* uma expressão regular

   Para tornar uma máscara uma expressão regular, insira a palavra-chave `regexp` entre o nome da coleção e a máscara do URL.

   Consulte Expressões [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Cada linha no campo Coleções pode conter apenas uma máscara de URL. No entanto, você pode especificar várias máscaras de URL para o mesmo nome de coleção em linhas diferentes. O exemplo a seguir contém quatro nomes de coleção diferentes e cinco máscaras de URL:

```
Company Info https://www.yoursite.com/company 
Products https://www.yoursite.com/products 
FAQs regexp ^.*/faqs 
Support https://www.yoursite.com/email_support/ 
Support https://www.yoursite.com/phone_support/
```

Neste exemplo, depois de atualizar o formulário de pesquisa para incluir essas coleções, os clientes podem selecionar e pesquisar cada coleção definida individualmente. A `Support` coleção inclui arquivos que correspondem às máscaras de URL, para que os arquivos em ambos `www.yoursite.com/email_support/` e `www.yoursite.com/phone_support` sejam pesquisados quando essa coleção for selecionada.

## Adicionar coleções {#task_07732D0F00104E59AD421297A704B2F6}

Você pode adicionar coleções para permitir que os clientes pesquisem áreas específicas do site para que possam encontrar rapidamente o que estão procurando.

<!-- 

t_adding_collections.xml

 -->

Certifique-se de recriar o índice do site para que os resultados das máscaras de URL fiquem visíveis aos clientes.

Consulte [Configurar um índice incremental de um site](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)de preparo.

**Para adicionar coleções**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Collections]**.
1. No [!DNL Collections] campo, insira um nome de coleção e um endereço de máscara de URL, um por linha.
1. (Opcional) Na [!DNL Collections] página, no **[!UICONTROL Test Collections]** campo, insira uma máscara de URL de teste em seu site e clique em **[!UICONTROL Test]**.

   Uma janela de saída da coleção de teste é exibida mostrando o URL e o nome da coleção.
1. Quando terminar de adicionar coleções, clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)de preparo.
1. (Opcional) Na [!DNL Collections] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre restrições {#concept_B5B527E04EBF4E9AB5956EEF881DDBF1}

Antes de uma pesquisa ser realizada, o URL de referência e o endereço IP são examinados para determinar se uma pesquisa é possível a partir desse local. O que você especificou [!DNL Restrictions] determina se a pesquisa é permitida. Se uma pesquisa não for permitida, uma página de erro genérica será retornada ao solicitante.

<!-- 

c_about_restrictions.xml

 -->

Você pode especificar configurações de restrição como máscaras de URL de quem indicou ou máscaras de endereço IP. Ambos os tipos de restrições usam máscaras para permitir pesquisas e excluir máscaras para negá-las.

Uma pesquisa é permitida se ela passar pelo URL da quem indicou e pelos critérios de restrição de endereço IP. Se uma das configurações não permitir a pesquisa, a pesquisa falhará, independentemente de outras restrições que a permitam.

Por exemplo, se o campo &quot;quem indicou HTTP&quot; de uma solicitação de pesquisa corresponder a uma máscara de URL de quem indicou &quot;excluído&quot;, a pesquisa falhará, mesmo se o endereço IP solicitante corresponder a uma máscara de endereço IP &quot;incluir&quot;. Se nenhuma máscara corresponder ao URL ou endereço IP da quem indicou, o local será incluído por padrão.

Insira cada máscara de inclusão ou exclua em uma única linha.

## Adicionando máscara de URL de quem indicou ou restrições de máscara de endereço IP {#task_E6FF2DD83E8D4B00A0E2809DC13A56C9}

Você pode especificar configurações de restrição como &quot;Máscaras de URL de Quem indicou&quot; ou &quot;Máscaras de endereço IP&quot;. Ambos os tipos de restrições usam máscaras para permitir pesquisas e excluir máscaras para negá-las. Uma pesquisa é permitida se ela passar pelo URL da quem indicou e pelos critérios de restrição de endereço IP.

<!-- 

t_adding_url_mask_or_jp_address_restrictions.xml

 -->

**Para adicionar máscara de URL de quem indicou ou restrições de máscara de endereço IP**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**.
1. Na [!DNL Restrictions] página, defina as opções de restrição desejadas. Insira endereços de máscara de URL de quem indicou, endereços de máscara de endereço IP ou, opcionalmente, um endereço de URL de uma página da Web personalizada que é exibida para clientes que não têm permissão para pesquisar no site.

   <!-- 
   
   r_restriction_options.xml
   
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
      <td colname="col1"> <p>Máscaras de URL de quem indicou </p> </td> 
      <td colname="col2"> <p>O URL da quem indicou do cabeçalho da quem indicou HTTP é lido. A primeira máscara que corresponde ao URL da quem indicou determina se a pesquisa deve ser permitida, se a máscara for uma máscara de inclusão. Ou, determina se a pesquisa deve ser desabilitada, se a máscara for uma máscara excluída. Se nenhuma máscara corresponder ao URL da quem indicou, esse URL será incluído e a pesquisa será permitida. </p> <p> Se o modelo de pesquisa contiver um novo formulário de pesquisa ou se o modelo de pesquisa puder conter links como "Próximo 10", "Anterior 10" ou "Ocultar Resumos", você lista o modelo de resultados de pesquisa como uma máscara "incluir". A maneira mais fácil de fazer isso é com a expressão normal, como no exemplo a seguir: </p> <p> <span class="codeph"> incluir regexp ^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ </span> </p> <p>O exemplo a seguir contém cinco máscaras de URL de quem indicou diferentes: </p> <p> <code> include&nbsp;https://www.mydomain.com/search/ 
          include&nbsp;https://search.mydomain.com/ 
          include&nbsp;regexp&nbsp;^https://www.mydomain.com/help/.*/search/ 
          include&nbsp;regexp&nbsp;^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ 
          exclude&nbsp;* </code> </p> <p>Se as máscaras de URL de quem indicou forem as seguintes: </p> <p> <code> https://www.mydomain.com/search/searchpage.html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://search.mydomain.com/advanced/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/search/advanced/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          https://www.anotherdomain.com/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          blank&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscaras de endereço IP </p> </td> 
      <td colname="col2"> <p>A primeira máscara que corresponde ao endereço IP determina se a pesquisa deve ser permitida, se a máscara for uma máscara de inclusão. Ou, determina se a pesquisa deve ser permitida ou não se deve ser permitida se a máscara for uma máscara excluída. Se nenhuma máscara corresponder ao endereço IP solicitante, esse endereço IP será incluído e a pesquisa será permitida. </p> <p>O exemplo a seguir mostra quatro máscaras de endereço IP diferentes. </p> <p> <code> include&nbsp;64.128.192.* 
          include&nbsp;192.168. 
          include&nbsp;regexp&nbsp;^209\.42\.97\.[1-5]+ 
          exclude&nbsp;* </code> </p> <p>Se as máscaras de endereço IP de referência forem as seguintes: </p> <p> <code> 64.128.192.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          192.168.10.127&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          209.42.97.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          64.128.193.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          192.169.10.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          209.42.97.68&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Permitir somente pesquisas que usam HTTPS </p> </td> 
      <td colname="col2"> <p>Restrinja pesquisas para HTTPS. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL para o qual as solicitações não permitidas devem ser enviadas </p> </td> 
      <td colname="col2"> <p> Os usuários restritos são redirecionados para o URL inserido aqui. Esta opção fornece uma forma de criar sua própria página de erro personalizada para ser exibida aos clientes que não têm permissão para pesquisar no site. </p> <p>Se você não especificar um URL, uma página de erro genérica será retornada quando um usuário restrito tentar pesquisar em seu site. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre Pré-visualizações {#concept_DF293FD3B02C467F8842C8C21D62F294}

A sequência de caracteres e os parâmetros do query definidos [!DNL Preview] são usados sempre que um formulário de pesquisa é testado ou visualizado no software.

<!-- 

c_about_preview.xml

 -->

See also [About Searches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

## Configuração de valores na Pré-visualização {#task_CE267A0FF621474E80AB43B67B1C28D7}

Os valores de pré-visualização definidos são usados sempre que um formulário de pesquisa é testado ou visualizado no software.

<!-- 

t_setting_values_in_preview.xml

 -->

**Definição de valores na Pré-visualização**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Preview]**.
1. Na [!DNL Preview] página, defina as opções desejadas.

   <!-- 
   
   r_preview_options.xml
   
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
      <td colname="col1"> <p>Consulta </p> </td> 
      <td colname="col2"> <p>Por padrão, a string de query é definida como <span class="codeph"> * </span>, o que geralmente retorna os resultados. No entanto, você pode especificar um query mais específico para o conteúdo do seu site. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetros </p> </td> 
      <td colname="col2"> <p>Os parâmetros são definidos com um nome e um valor. Você pode especificar quantos parâmetros adicionais forem necessários. Por exemplo, você pode especificar critérios de pesquisa adicionais com <span class="codeph"> parâmetros sp_q_1 </span> e <span class="codeph"> sp_x_1 </span> . O valor do parâmetro <span class="codeph"> sp_q_1=windows&amp;sp_x_1=platform </span> cria uma pesquisa de pré-visualização que procura o valor "windows" na tag meta "platform" das páginas pesquisadas, além do query principal. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Host </p> </td> 
      <td colname="col2"> <p>Se o site usar a rotulagem de domínio privado, defina o nome do host apropriado para pré-visualização precisa dos resultados da pesquisa. </p> <p>Para obter informações sobre a rotulagem de domínio privado, entre em contato com o Suporte ao cliente. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre feeds {#concept_FEBFEE51A3AB49F88CBA0D16E2AD6916}

O índice de pesquisa é visto como um grande banco de dados do seu site. Com informações suficientes das meta tags corretas, as informações são coletadas e organizadas ou sindicadas nos feeds de dados. Você pode enviar esses feeds de dados para outro serviço, como um recipient de terceiros.

<!-- 

c_about_feeds.xml

 -->

Depois que seu site é rastreado e indexado, você pode gerar feeds automáticos e enviá-los para mecanismos de pesquisa orgânicos e mecanismos de compras de terceiros. Você pode criar os seguintes feeds de fluxo:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tipo de feed </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Recommendations </p> </td> 
   <td colname="col2"> <p>Recomendações os feeds fornecem recursos de sindicalização de dados com a Adobe Recommendations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feed genérico </p> </td> 
   <td colname="col2"> <p>É possível implementar vários feeds com o tipo Feed Genérico. Um query de pesquisa personalizado é feito em relação ao índice do seu site. Os dados são retornados por meio de modelos de pesquisa personalizados usando a mesma linguagem de modelo para exibir resultados de pesquisa. Esse tipo de flexibilidade significa que você pode enviar feeds para muitos outros fornecedores, não apenas para tipos específicos de feed. </p> <p>Você pode adicionar o modelo de transporte (pesquisa) usando as instruções no seguinte tópico da Ajuda: </p> <p>Consulte <a href="../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012" type="task" format="dita" scope="local"> Adicionando uma nova apresentação ou arquivo de modelo de transporte </a>. </p> <p> Depois de adicionar o modelo, edite-o usando tags de modelo de pesquisa para definir quais campos de metadados de pesquisa você deseja incluir, juntamente com seu formato. </p> <p>Consulte <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> Editar uma apresentação ou um modelo de transporte </a>. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Pesquisar marcas de modelo </a>. </p> <p>Lembre-se do nome do arquivo de modelo de transporte. Use o nome para vincular o feed genérico ao modelo ao especificar os critérios do feed. </p> <p>Se você tiver trabalhado anteriormente com outros feeds, lembre-se de mapear os campos de feed para os campos de metadados de pesquisa. Feeds genéricos não têm essa etapa específica no <span class="uicontrol"> assistente Criar feed </span> . Em vez disso, o modelo especifica os metadados e a formatação dos metadados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Google Merchant </p> </td> 
   <td colname="col2"> <p>O Google Merchant Center permite que as pessoas vendam produtos por meio de vários serviços do Google. Ele tem um componente de sindicalização de dados no qual você pode enviar uma lista de produtos disponíveis para venda periodicamente. </p> <p>Assim como com qualquer fornecedor de feed de terceiros, o Google Merchant Center tem padrões específicos que você atende antes que eles considerem o feed legítimo. Para obter mais informações, entre em contato com seu representante de cliente e visite a documentação do Google Merchant. Este é um resumo rápido do que o Google Merchant Center considera ao validar um feed: </p> 
    <ul id="ul_3D84D4A6A4BF4C08860F86403F8F9CD6"> 
     <li id="li_5B6516CC7BC7493B8B8E8AFB454E573F">Cada produto tem uma página de produto; um URL dedicado. </li> 
     <li id="li_5A6D5AD5E1B54A94B224D19E888B5443"> Cada variante de produto tem uma entrada separada no feed. </li> 
     <li id="li_89748D3241B34A4493576DAC38681988"> Cada produto tem um URL de imagem, de preferência originário do seu servidor. As variantes do produto têm imagens específicas que mostram suas variações reais. Em outras palavras, diferentes cores do sapato não devem compartilhar a mesma imagem. </li> 
     <li id="li_A594AD19480F41EAA72181355F28447B"> Cada produto tem informações específicas, como disponibilidade, condição, descrição, categoria e preço. </li> 
     <li id="li_0955B3A6ED2746D2B7CB42DC8AB27D3A">Em geral, cada produto tem um identificador exclusivo, como ISBN, UPC, JAN ou EAN e assim por diante. </li> 
     <li id="li_2C371653F1C5471FA638F3A3818ABC17">Em geral, cada produto é classificado com a taxonomia de produto do Google. </li> 
     <li id="li_6EB392A5A0BE490FAED5BC5E83228E32"> Os produtos de vestuário têm campos obrigatórios extras, como gênero, faixa etária, cor e tamanho. </li> 
     <li id="li_44B91FA9A95F4172A2F03F8206E9081E"> O imposto e o frete são especificados como uma configuração de conta no Google Merchant Center ou em relação ao produto, dentro deste feed. </li> 
     <li id="li_71A63E9905B840C0A04F6CDAA23C9AB0"> Produtos feitos por medida e certos produtos de vestuário podem ser isentos de algumas das regras, mas você deve entrar em contato com o Google para obter permissão e detalhes sobre essas isenções. </li> 
    </ul> <p>Há muitos detalhes que governam a validação do feed. Consulte a documentação do Google Merchant para obter informações sobre o gerenciamento de feed. O Google frequentemente altera as especificações, portanto, consulte a documentação com frequência. </p> <p>O feed associado ao Google Merchant Center é geralmente chamado de feed do Google Product Search. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Google Sitemaps </p> </td> 
   <td colname="col2"> <p>O Google Sitemaps fornece uma maneira de influenciar como o Google rastreia seu site. Um feed de dados sindicalizado, um mapa do site nesse caso, é submetido periodicamente ao Google Sitemaps. O mapa do site contém URLs acessíveis pela Internet e informações específicas, como a data da última modificação ou a prioridade da página, podem ser associadas a cada URL. Fornecer tais informações ao Google pode aumentar a frequência e a chance de uma página específica ser rastreada e indexada. Em alguns casos, um mapa do site é usado para anunciar uma lista de links que não podem ser acessados pelo rastreador em circunstâncias normais. </p> <p>Se você estiver interessado em criar um mapa do Google Sitemap com nosso recurso de feed, entre em contato com o representante do cliente. O Google disponibilizou seu serviço Google Sitemap ao público em geral e eles fornecem documentação em sua página do Google Webmaster Tools. </p> <p> <b>Requisitos para a criação de um feed do Google Sitemap</b> </p> <p>Para criar um feed do Google Sitemap, verifique se você já possui uma conta do Google Webmaster Tools com o mapa do Google Sitemap configurado. Consulte a documentação de ferramentas do Google Webmaster para configurar o Google Sitemap. </p> <p>Você também precisa determinar como os arquivos do mapa do site são entregues. Em geral, os arquivos de mapa do site vêm do seu domínio e, especificamente, da raiz do site. O modelo simples é ter os arquivos entregues por FTP para seus servidores. A outra solução é redirecionar a solicitação dos arquivos do mapa do site para a pesquisa/comercialização do site Content Network. Entre em contato com seu representante de consultoria sobre como coordenar e configurar o delivery de feeds de mapa do site. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se você estiver interessado em feeds automáticos, entre em contato com os serviços profissionais para obter assistência. Cada feed tem requisitos rigorosos no que diz respeito à qualidade dos dados e à transmissão dos arquivos.

O tipo de feed selecionado afeta as opções que aparecem ao construir um campo usando o **[!UICONTROL Create Feed]** assistente. Cada tipo de feed tem diferentes formatos de dados. Certifique-se de seguir o formato de dados correto para evitar a rejeição de um feed por um recipient de feed ou a publicação de dados inadequados para seus clientes. Além do formato de dados, os fornecedores geralmente têm uma ou mais formas preferenciais de receber os dados. Consulte a documentação do fornecedor sobre seus feeds.

Um desafio na criação de um feed é corresponder os dados entre a pesquisa/comercialização do site e o feed. Normalmente, os dados recuperados do rastreamento de índice estão no formato incorreto ou estão ausentes. A seguir está uma lista de perguntas que podem ajudá-lo a se concentrar no que procurar ao criar um feed.

* Que tipo de relacionamento comercial você tem com o recipient de feed?
* Você precisa se registrar e criar uma conta no recipient de feed?
* Quem vai monitorar e cuidar dos problemas que surgem com o feed em relação ao vendedor? Em geral, é sua responsabilidade gerenciar a conta do fornecedor. Por exemplo, o Google Sitemap requer uma conta WebMaster e alguém para monitorar a integridade do mapa do site.
* Qual é o formato de dados do feed?
* Seu índice corresponde à codificação de caracteres do feed? Os formatos de dados delimitados por tabulação e por vírgulas tornam-se um problema quando os dados têm tabulações ou vírgulas.
* O que você faz quando tem guias ou vírgulas em seus dados?
* Há alguma página no índice com dados vazios?
* O recipient de feed pode aceitar dados vazios? Você pode resolver dados vazios editando os critérios de como os dados são recuperados pelo software.
* O formato de dados é semelhante ao que o recipient de feed deseja? Por exemplo, alguns recipient de feed são específicos sobre como os preços e a moeda são exibidos.
* O fornecedor tem um número máximo de itens que ele pode aceitar? Você pode resolver esse problema potencial limitando os resultados com os critérios de pesquisa.
* Como o fornecedor deseja receber o feed? Os envios FTP e a hospedagem HTTP são suportados.

## Criação de um feed {#task_63179C1FC359497483CD6CE13FD1C250}

Você pode criar um ou mais feeds de dados.

<!-- 

t_creating_a_feed.xml

 -->

**Para criar um feed**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Na [!DNL Feeds] página, selecione um tipo de feed na lista **[!UICONTROL Create Feed]** suspensa.
1. Dependendo do tipo de feed selecionado, na caixa de [!DNL Create Feed] diálogo, defina as opções como identificadas em cada painel do assistente.

   <!-- 
   
   r_feed_options.xml
   
   -->

   Dependendo do tipo de feed que você está criando ou editando, as opções disponíveis diferem ligeiramente.

   **Adobe Recommendations**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Painel </p> </th> 
      <th colname="col2" class="entry"> <p>Nome do painel Assistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nome do feed </p> </td> 
      <td colname="col3"> <p>Especifica o nome do feed. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Mapas de campo </p> </td> 
      <td colname="col3"> <p>Permite mapear campos de feed específicos do fornecedor para campos de metadados de pesquisa/comercialização do site. Essa etapa de mapeamento no assistente é importante porque permite que os Feeds correlacionem as informações entre os campos no índice e os campos nos dados do feed. Na maioria dos casos, exceto Feeds <span class="wintitle"> genéricos </span>, as correlações são salvas em um modelo de pesquisa gerado dinamicamente. </p> <p>Cada linha na tabela <span class="wintitle"> Mapas de campo </span> representa um mapeamento de campo. Na coluna Adicionar/Remover da tabela, clique em <span class="uicontrol"> + </span> para adicionar uma nova linha de mapeamento de campo; clique em <span class="uicontrol"> - </span> para excluir a linha de mapeamento de campo atualmente selecionada da tabela. Para associar um campo de feed a um campo de metadados de pesquisa/comercialização do site, use as respectivas listas suspensas para escolher os campos desejados. </p> <p> <b>Mapeamentos de campo para Adobe Recommendations</b> </p> <p>O feed de dados do Recommendations é um arquivo CSV, colunas de dados separadas por vírgulas. A ordem de aparência de cada mapeamento na tabela Mapas de campo é importante, pois determina a ordem das colunas no arquivo de feed CSV. Crie as linhas de mapeamentos na seguinte ordem — cada linha é obrigatória: </p> <p> 
        <ol id="ol_49C739D04DD340168DC6C1F794544C35"> 
          <li id="li_A95D9C5A353746A3A0D38F200AC2EEA2"> id </li> 
          <li id="li_044763D4C7054CEB948C94590735D74F"> name </li> 
          <li id="li_832F07CA0E3F4E10A4AE30171F3E8541"> categoryId </li> 
          <li id="li_2A33FB42F7E942ED881BA1F478542C4D"> message </li> 
          <li id="li_A76E66B2366845B0B63ED5C200531ADD"> thumbnailURL </li> 
          <li id="li_518CCD5E7E404521AB8199981BA86F76"> value </li> 
          <li id="li_14A0A8FCC2B34B758E1FBB98E3F2DFB2"> pageURL </li> 
          <li id="li_36D22F1603394AF89E0C7ADB18AAAAB7"> inventory </li> 
          <li id="li_ABDB9C762BBC4F27B82FEA4425A8DDC4"> margin </li> 
        </ol> </p> <p> <b>Uso avançado</b> </p> <p>Depois de mapear os nove primeiros campos obrigatórios do feed, conforme descrito acima, você pode criar seus próprios campos personalizados. Na lista <span class="wintitle"> suspensa Campos de feed, clique em </span> Personalizado <span class="uicontrol"> </span>. No campo de texto associado, insira um nome de tag personalizado para esse campo. Essa opção personalizada será útil se um feed precisar de campos específicos do fornecedor. </p> <p> <p>Observação:  Embora as especificações do feed de recomendação indiquem que cada nome de campo deve ter o prefixo "entity", isso não é necessário neste caso. </p> </p> <p>Também é possível criar um campo de metadados personalizado. Na lista suspensa Campos de <span class="wintitle"> metadados </span> , clique em <span class="uicontrol"> Personalizado </span>. No campo de texto associado, insira um valor de campo de metadados personalizado. O valor é inserido no modelo pré-gerado e também pode ser usado para inserir tags de modelo de pesquisa personalizadas. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Pesquisar marcas de modelo </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Critérios de busca </p> </td> 
      <td colname="col3"> <p>Quando os arquivos de feed são gerados, um query de pesquisa é usado para filtrar os dados. Você define os filtros usados para o query de pesquisa neste painel. </p> 
        <ul id="ul_799ECF61C03A44878C7182F8B88CC3AD"> 
        <li id="li_0763F600A4FB4650ACC28BF337EB50AF"> <span class="uicontrol"> Campo Meta </span> <p>Define em qual campo de metadados você deseja filtrar. </p> <p> <b>Uso avançado</b> </p> <p>Como o sistema de filtragem é um query de pesquisa padrão, você pode selecionar Formulário <span class="uicontrol"> Livre </span> na lista suspensa para inserir os parâmetros de pesquisa CGI e seus valores. É necessário escape de URL. O argumento de pesquisa <span class="codeph"> sp_q </span> é ignorado. É possível criar várias linhas de caixas de texto de Formulário gratuito. Entre cada linha, os argumentos são delimitados automaticamente com o &amp;'s. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Pesquisar parâmetros CGI </a>. </p> </li> 
        <li id="li_756B776902AE4A0E95524442D663343E"> <span class="uicontrol"> Critérios </span> <p>Define a operação de filtro. A operação de filtro selecionada na lista suspensa aplica o valor constante inserido na terceira coluna. </p> </li> 
        <li id="li_7ADEDB8747B241D78AC50F1AC75AE695"> <span class="uicontrol"> Valor </span> <p>O valor constante. </p> </li> 
        <li id="li_4039A9BC2F74460B83BFF662B58DAA1B"> <span class="uicontrol"> Ação </span> <p>Adiciona uma nova linha de mapeamento de campo ou exclui a linha realçada no momento. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envio de arquivo </p> </td> 
      <td colname="col3"> <p>Permite configurar o agendamento para enviar os arquivos de feed e definir o método que deseja usar para fazer upload dos arquivos. </p> 
        <ul id="ul_55E253F83BDA46BAABF2BE38F0918E80"> 
        <li id="li_877A376B5B30422FAC816E31D50EA508"> <span class="uicontrol"> Agendar </span> <p>Define a frequência máxima de envio de um feed. Selecionar <span class="uicontrol"> Nunca </span> desliga o feed. Outros valores definem o período que o feed aguarda antes de enviar novamente. A decisão de submeter o feed é feita em cada índice. Em outras palavras, no final do índice, um feed é verificado para ver se expirou e precisa ser atualizado e enviado pelo fornecedor. Além disso, é usado como um método para impedir que uma conta envie em excesso para um fornecedor. Alguns fornecedores têm políticas contra fontes de feed de dados que carregam com frequência. Verifique a política do fornecedor do feed de dados sobre a frequência de envios. 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--ick <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_760F5068D3ED46C582AE41392A2CA342"> <span class="uicontrol"> Método de upload </span> <p>A maioria dos feeds tem duas formas de distribuir os arquivos: FTP e Rede de conteúdo hospedado. </p> 
          <ul id="ul_666759EDDD034537AA7C0ED936A2F315"> 
          <li id="li_B4AD5CEEBB7B41C0B8DC291B95DC5F83"> <span class="uicontrol"> FTP </span> <p>Os servidores de pesquisa/comercialização do site usam FTP passivo. </p> <p>O FTP é a única maneira de enviar um arquivo para outro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> - Especifica o nome do servidor FTP. Não inclua o protocolo ou o anterior "ftp://". </p> <p> <span class="uicontrol"> Nome de usuário FTP </span> - Especifica o nome da conta FTP. </p> <p> <span class="uicontrol"> Senha FTP </span> - Especifica a senha da conta FTP. </p> <p> <span class="uicontrol"> Nome do arquivo FTP </span> - Especifica o nome do arquivo a ser transmitido. Esse nome é um modelo se o feed gerar vários arquivos, normalmente incrementando um número no final do nome, mas antes da extensão. Por exemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Diretório FTP </span> - se um caminho de diretório específico for necessário, insira-o aqui. Não inclua o nome de arquivo no caminho. </p> </li> 
          <li id="li_C082D3993C6C469B9067F207703BE619"> <span class="uicontrol"> Rede de conteúdo hospedado </span> <p>A Rede de Conteúdo é a forma de servir arquivos dos servidores da Web de pesquisa/comercialização de sites. O recipient do feed o extrai dos servidores da Web usando uma solicitação HTTP. A única informação a ser configurada é o Nome do Arquivo de Rede <span class="uicontrol"> de Conteúdo </span>. O nome do arquivo é o nome base do arquivo que é disponibilizado. Use apenas nomes de arquivo com uma extensão de nome de arquivo. Dependendo do feed, o nome do arquivo é um modelo para vários arquivos em que o feed pode gerar vários arquivos no seguinte formato: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. </p> <p>Depois que o nome de arquivo base é inserido e o feed é salvo com êxito, o URL do arquivo de Rede de conteúdo é exibido no painel Verificação do assistente. O URL torna-se ativo depois que o feed é processado com êxito. O fornecedor pode obter os dados do feed deste URL. Vários arquivos usam o mesmo caminho de URL. No entanto, substitua ou altere o nome do arquivo de acordo com o esquema de lista discriminada. </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Verificação </p> </td> 
      <td colname="col3"> <p>Quando você chega ao <span class="wintitle"> painel </span> Verificação, seu feed é salvo nesse ponto. No entanto, os arquivos de feed reais não são salvos até mais tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_0C6EFB38E06F401696084863D85CBD0D"> 
        <li id="li_07FC9F04C7F640048546F9DC5D91DA1D"> <span class="uicontrol"> Data View </span> <p>Permite que você clique no link para verificar a saída do feed por meio de uma visualização de dados exibida em forma de tabela. A visualização de dados também pode ajudá-lo a solucionar problemas, mostrando quais campos meta foram escolhidos e como qualquer critério de pesquisa especificado no painel Critérios de <span class="wintitle"> pesquisa </span> do assistente afeta a saída do feed. A visualização de dados é gerada dinamicamente, de modo que esteja disponível o tempo todo. </p> </li> 
        <li id="li_67046A56D08C48298E5A3E1F9C4A8AF3"> <span class="uicontrol"> Arquivos de feed </span> <p>Depois que os servidores de pesquisa/comercialização do site gerarem os arquivos de feed, você poderá usar a lista suspensa <span class="uicontrol"> Feed Files </span> para visualização os arquivos dos servidores. Uma nova guia do navegador ou nova janela do navegador é exibida com o conteúdo do feed. Esse método é útil para ajudar a solucionar problemas de feeds com problemas de formatação. Observe que você não visualização os arquivos do destino final ou dos próprios fornecedores. </p> <p> Se o feed for novo, a lista suspensa fica vazia até que você gere os arquivos de feed. </p> </li> 
        <li id="li_99D66C7AD87A475CB3D831D514DB78A0"> <span class="uicontrol"> Link de rede de conteúdo </span> <p>Se você escolher <span class="uicontrol"> Rede de conteúdo hospedado </span> como método de upload no painel <span class="wintitle"> Envio de arquivo </span> do assistente, o URL será exibido aqui. Se você ainda não tiver gerado nenhum arquivo de feed, o URL não será válido até que o feed seja gerado com êxito. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Feed genérico**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Painel </p> </th> 
      <th colname="col2" class="entry"> <p>Nome do painel Assistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nome do feed </p> </td> 
      <td colname="col3"> <p>Especifica o nome do feed. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Critérios de busca </p> </td> 
      <td colname="col3"> <p>Quando os arquivos de feed são gerados, um query de pesquisa é usado para filtrar os dados. Você define os filtros usados para o query de pesquisa neste painel. </p> 
        <ul id="ul_C750687E69A647D0A4440FF1B6CC7E05"> 
        <li id="li_B5C3B8523D71472E9508A04E23AC0211"> <span class="uicontrol"> Campo Meta </span> <p>Define em qual campo de metadados você deseja filtrar. </p> <p> <b>Uso avançado</b> </p> <p>Como o sistema de filtragem é um query de pesquisa padrão, você pode selecionar Formulário <span class="uicontrol"> Livre </span> na lista suspensa para inserir os parâmetros de pesquisa CGI e seus valores. É necessário escape de URL. O argumento de pesquisa <span class="codeph"> sp_q </span> é ignorado. É possível criar várias linhas de caixas de texto de Formulário gratuito. Entre cada linha, os argumentos são delimitados automaticamente com o &amp;'s. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Pesquisar parâmetros CGI </a>. </p> </li> 
        <li id="li_D1E49834BBEA42CC8C49AE7D72037C53"> <span class="uicontrol"> Critérios </span> <p>Define a operação de filtro. A operação de filtro selecionada na lista suspensa aplica o valor constante inserido na terceira coluna. </p> </li> 
        <li id="li_D5F0651B834F4EACAD15A2D154A0737B"> <span class="uicontrol"> Valor </span> <p>O valor constante. </p> </li> 
        <li id="li_FC8F382BD20C4518BC2230D4B4954591"> <span class="uicontrol"> Ação </span> <p>Adiciona uma nova linha de mapeamento de campo ou exclui a linha realçada no momento. </p> </li> 
        </ul> <p>Os feeds genéricos precisam de um parâmetro CGI especial especificado. Para vincular o modelo especial associado a esse feed, defina o parâmetro <span class="codeph"> sp_t </span> . Defina o valor de <span class="codeph"> sp_t </span> para o nome do arquivo de modelo de transporte. Por exemplo, se você adicionou um arquivo de modelo de transporte chamado <span class="codeph"> super_feed.tpl </span>, crie um parâmetro de pesquisa CGI personalizado como <span class="codeph"> sp_t=super_feed </span>. A caixa de texto para inserir o <span class="codeph"> sp_t </span> não é exibida até que você selecione <span class="uicontrol"> Formulário gratuito </span> na lista suspensa <span class="wintitle"> Campo </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Envio de arquivo </p> </td> 
      <td colname="col3"> <p>Permite configurar o agendamento para enviar os arquivos de feed e definir o método que deseja usar para fazer upload dos arquivos. </p> 
        <ul id="ul_30E830C41F6A4526822AF1FD3083075A"> 
        <li id="li_79EAFDBD2B9F411EA985CAEC1BAF3926"> <span class="uicontrol"> Agendar </span> <p>Define a frequência máxima de envio de um feed. Selecionar <span class="uicontrol"> Nunca </span> desliga o feed. Outros valores definem o período que o feed aguarda antes de enviar novamente. A decisão de submeter o feed é feita em cada índice. Em outras palavras, no final do índice, um feed é verificado para ver se expirou e precisa ser atualizado e enviado pelo fornecedor. Além disso, é usado como um método para impedir que uma conta envie em excesso para um fornecedor. Alguns fornecedores têm políticas contra fontes de feed de dados que carregam com frequência. Verifique a política do fornecedor do feed sobre a frequência dos envios. 
          <!--he time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--<uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_20BF70A19E7E45BA91CD972E2FCE0EA4"> <span class="uicontrol"> Método de upload </span> <p>A maioria dos feeds tem duas formas de distribuir os arquivos: FTP e Rede de conteúdo hospedado. </p> 
          <ul id="ul_5888C2E9097645CE89938EE09F8CB4F1"> 
          <li id="li_EA9ED19F3BEA4BEAB1A9F2C2FAFF85F7"> <span class="uicontrol"> FTP </span> <p>Os servidores de pesquisa/comercialização do site usam FTP passivo. </p> <p>O FTP é a única maneira de enviar um arquivo para outro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> - Especifica o nome do servidor FTP. Não inclua o protocolo ou o anterior "ftp://". </p> <p> <span class="uicontrol"> Nome de usuário FTP </span> - Especifica o nome da conta FTP. </p> <p> <span class="uicontrol"> Senha FTP </span> - Especifica a senha da conta FTP. </p> <p> <span class="uicontrol"> Nome do arquivo FTP </span> - Especifica o nome do arquivo a ser transmitido. Esse nome é um modelo se o feed gerar vários arquivos, normalmente incrementando um número no final do nome, mas antes da extensão. Por exemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Diretório FTP </span> - se um caminho de diretório específico for necessário, insira-o aqui. Não inclua o nome de arquivo no caminho. </p> </li> 
          <li id="li_181268A7EE40456CA1DB768E8C66EEB9"> <span class="uicontrol"> Rede de conteúdo hospedado </span> <p>A Rede de Conteúdo Hospedado é a forma de servir arquivos dos servidores da Web de pesquisa/comercialização do site. O recipient do feed o extrai dos servidores da Web usando uma solicitação HTTP. A única informação a ser configurada é o Nome do Arquivo de Rede <span class="uicontrol"> de Conteúdo </span>. O nome do arquivo é o nome base do arquivo que é disponibilizado. Use apenas nomes de arquivo com uma extensão de nome de arquivo. 
            <!--Depending on the feed, the file name is a template for multiple files where the feed might generate multiple files in the following format: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. --> </p> <p>Depois que o nome de arquivo base é inserido e o feed é salvo com êxito, o URL do arquivo de Rede de conteúdo é exibido no painel Verificação do assistente. O URL torna-se ativo depois que o feed é processado com êxito. O fornecedor pode obter os dados do feed deste URL. </p> </li> 
          </ul> </li> 
        <li id="li_4DF56FA607A7479296CDA042A63C5A2C"> <p> <b>Preservar guias?</b> </p> <p>Manter caracteres de guia no feed. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Verificação </p> </td> 
      <td colname="col3"> <p>Quando você chega ao <span class="wintitle"> painel </span> Verificação, seu feed é salvo nesse ponto. No entanto, os arquivos de feed reais não são salvos até mais tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_7420C415987448A796DD979CF5FA2EB6"> 
        <li id="li_AF02E8609B7B4F20A01AF4E010308E15"> <span class="uicontrol"> Data View </span> <p>Permite que você clique no link para verificar a saída do feed por meio de uma visualização de dados exibida em forma de tabela. A visualização de dados também pode ajudá-lo a solucionar problemas, mostrando quais campos meta foram escolhidos e como qualquer critério de pesquisa especificado no painel Critérios de <span class="wintitle"> pesquisa </span> do assistente afeta a saída do feed. A visualização de dados é gerada dinamicamente, de modo que esteja disponível o tempo todo. </p> </li> 
        <li id="li_32CEB8885C184354BFA1773BA66DB7A7"> <span class="uicontrol"> Arquivos de feed </span> <p>Depois que os servidores de pesquisa/comercialização do site gerarem os arquivos de feed, você poderá usar a lista suspensa <span class="uicontrol"> Feed Files </span> para visualização os arquivos dos servidores. Uma nova guia do navegador ou nova janela do navegador é exibida com o conteúdo do feed. Esse método é útil para ajudar a solucionar problemas de feeds com problemas de formatação. Observe que você não visualização os arquivos do destino final ou dos próprios fornecedores. </p> <p> Se o feed for novo, a lista suspensa fica vazia até que você gere os arquivos de feed. </p> </li> 
        <li id="li_8D1B876B0EC2455C8654EC573EC53FA9"> <span class="uicontrol"> Link de rede de conteúdo </span> <p>Se você escolher <span class="uicontrol"> Rede de conteúdo hospedado </span> como método de upload no painel <span class="wintitle"> Envio de arquivo </span> do assistente, o URL será exibido aqui. Se você ainda não tiver gerado nenhum arquivo de feed, o URL não será válido até que o feed seja gerado com êxito. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Google Merchant Center**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Painel </p> </th> 
      <th colname="col2" class="entry"> <p>Nome do painel Assistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nome do feed </p> </td> 
      <td colname="col3"> <p>Especifica o nome do feed. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Mapas de campo </p> </td> 
      <td colname="col3"> <p>Permite mapear campos de feed específicos do fornecedor para campos de metadados de pesquisa/comercialização do site. Essa etapa de mapeamento no assistente é importante porque permite que os Feeds correlacionem as informações entre os campos no índice e os campos nos dados do feed. Na maioria dos casos, exceto Feeds <span class="wintitle"> genéricos </span>, as correlações são salvas em um modelo de pesquisa gerado dinamicamente. </p> <p>Cada linha na tabela Mapas de campo representa um mapeamento de campo. Na coluna <span class="wintitle"> Adicionar/Remover </span> da tabela, clique em <span class="uicontrol"> + </span> para adicionar uma nova linha de mapeamento de campo; clique em <span class="uicontrol"> - </span> para excluir a linha de mapeamento de campo atualmente selecionada da tabela. Para associar um campo de feed a um campo de metadados de pesquisa/comercialização do site, use as respectivas listas suspensas para escolher os campos desejados. </p> <p> <b>Uso avançado</b> </p> <p>Você pode criar seus próprios campos personalizados. Na lista <span class="wintitle"> suspensa Campos de feed, clique em </span> Personalizado <span class="uicontrol"> </span>. No campo de texto associado, insira um nome de tag personalizado para esse campo. Essa opção personalizada será útil se um feed precisar de campos específicos do fornecedor. </p> <p>Também é possível criar um campo de metadados personalizado. Na lista suspensa Campos de <span class="wintitle"> metadados </span> , clique em <span class="uicontrol"> Personalizado </span>. No campo de texto associado, insira um valor de campo de metadados personalizado. O valor é inserido no modelo pré-gerado e também pode ser usado para inserir tags de modelo de pesquisa personalizadas. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Pesquisar marcas de modelo </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Critérios de busca </p> </td> 
      <td colname="col3"> <p>Quando os arquivos de feed são gerados, um query de pesquisa é usado para filtrar os dados. Você define os filtros usados para o query de pesquisa neste painel. </p> 
        <ul id="ul_8179321A58BB4C72B0CDB2B2BEC58FE4"> 
        <li id="li_9F8008A2398A4667B106BC49C94E5E3E"> <span class="uicontrol"> Campo Meta </span> <p>Define em qual campo de metadados você deseja filtrar. </p> <p> <b>Uso avançado</b> </p> <p>Como o sistema de filtragem é um query de pesquisa padrão, você pode selecionar Formulário <span class="uicontrol"> Livre </span> na lista suspensa para inserir os parâmetros de pesquisa CGI e seus valores. É necessário escape de URL. O argumento de pesquisa <span class="codeph"> sp_q </span> é ignorado. É possível criar várias linhas de caixas de texto de Formulário gratuito. Entre cada linha, os argumentos são delimitados automaticamente com o &amp;'s. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Pesquisar parâmetros CGI </a>. </p> </li> 
        <li id="li_50C9CE59E9E5418895F8C1A070560063"> <span class="uicontrol"> Critérios </span> <p>Define a operação de filtro. A operação de filtro selecionada na lista suspensa aplica o valor constante inserido na terceira coluna. </p> </li> 
        <li id="li_9F86D0F5010046A4A9F93DBA5FB158B3"> <span class="uicontrol"> Valor </span> <p>O valor constante. </p> </li> 
        <li id="li_1051AFD5AEA447D0AF5FAB305E1D1E64"> <span class="uicontrol"> Ação </span> <p>Adiciona uma nova linha de mapeamento de campo ou exclui a linha realçada no momento. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envio de arquivo </p> </td> 
      <td colname="col3"> <p>Permite configurar o agendamento para enviar os arquivos de feed e definir o método que deseja usar para fazer upload dos arquivos. </p> 
        <ul id="ul_A6A3C333AADD4438B835BF3E16E2AEFF"> 
        <li id="li_FCC4DAF198E149278B5CFB870CB6218C"> <span class="uicontrol"> Agendar </span> <p>Define a frequência máxima de envio de um feed. Selecionar <span class="uicontrol"> Nunca </span> desliga o feed. Outros valores definem o período que o feed aguarda antes de enviar novamente. A decisão de submeter o feed é feita em cada índice. Em outras palavras, no final do índice, um feed é verificado para ver se expirou e precisa ser atualizado e enviado pelo fornecedor. Além disso, é usado como um método para impedir que uma conta envie em excesso para um fornecedor. Alguns fornecedores têm políticas contra fontes de feed de dados que carregam com frequência. Verifique a política do fornecedor do feed sobre a frequência dos envios. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_2D9ECAFB8E8544D39B486F7BC3DCE589"> <span class="uicontrol"> Método de upload </span> <p>A maioria dos feeds tem duas formas de distribuir os arquivos: FTP e Rede de conteúdo hospedado. </p> <p>O método de upload recomendado para enviar o feed de dados é <span class="uicontrol"> FTP </span>. O Google Merchant Center hospeda um servidor FTP para esse fim. Consulte a Ajuda do Google Merchant Center sobre como configurar uma conta FTP separada do Google para este feed do Google Product Search. </p> 
          <ul id="ul_BC0D8B541068407883CAC948496DBD0A"> 
          <li id="li_DB28CA23C94A4AF09E1A0EB06DF8F40C"> <span class="uicontrol"> FTP </span> <p>Os servidores de pesquisa/comercialização do site usam FTP passivo. </p> <p>O FTP é a única maneira de enviar um arquivo para outro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> - Especifica o nome do servidor FTP. Neste caso, é <code>
              uploads.google.com 
            </code>. Não inclua o protocolo ou o anterior "ftp://". </p> <p> <span class="uicontrol"> Nome de usuário FTP </span> - Especifica o nome da conta FTP. </p> <p> <span class="uicontrol"> Senha FTP </span> - Especifica a senha da conta FTP. </p> <p> <span class="uicontrol"> Nome do arquivo FTP </span> - Especifica o nome do arquivo a ser transmitido. Esse nome é um modelo se o feed gerar vários arquivos, normalmente incrementando um número no final do nome, mas antes da extensão. Por exemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Diretório FTP </span> - se um caminho de diretório específico for necessário, insira-o aqui. Não inclua o nome de arquivo no caminho. </p> </li> 
          <li id="li_5990927146434DAF89273F4636D21437"> <span class="uicontrol"> Rede de conteúdo hospedado </span> <p>A Rede de Conteúdo é a forma de servir arquivos dos servidores da Web de pesquisa/comercialização de sites. O recipient do feed o extrai dos servidores da Web usando uma solicitação HTTP. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Verificação </p> </td> 
      <td colname="col3"> <p>Quando você chega ao <span class="wintitle"> painel </span> Verificação, seu feed é salvo nesse ponto. No entanto, os arquivos de feed reais não são salvos até mais tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_4A94355A8DF840A3BAF6BD5E9F11C27F"> 
        <li id="li_825697CB36B34C4AB5959B15EDDB55F1"> <span class="uicontrol"> Data View </span> <p>Permite que você clique no link para verificar a saída do feed por meio de uma visualização de dados exibida em forma de tabela. A visualização de dados também pode ajudá-lo a solucionar problemas, mostrando quais campos meta foram escolhidos e como qualquer critério de pesquisa especificado no painel Critérios de <span class="wintitle"> pesquisa </span> do assistente afeta a saída do feed. A visualização de dados é gerada dinamicamente, de modo que esteja disponível o tempo todo. </p> </li> 
        <li id="li_91B8B5F5F9DE4A13863CD62F74AA6206"> <span class="uicontrol"> Arquivos de feed </span> <p>Depois que os servidores de pesquisa/comercialização do site gerarem os arquivos de feed, você poderá usar a lista suspensa <span class="uicontrol"> Feed Files </span> para visualização os arquivos dos servidores. Uma nova guia do navegador ou nova janela do navegador é exibida com o conteúdo do feed. Esse método é útil para ajudar a solucionar problemas de feeds com problemas de formatação. Observe que você não visualização os arquivos do destino final ou dos próprios fornecedores. </p> <p> Se o feed for novo, a lista suspensa fica vazia até que você gere os arquivos de feed. </p> </li> 
        <li id="li_4A5EC089628E43029A38F8919888FF0A"> <span class="uicontrol"> Link de rede de conteúdo </span> <p>Se você escolher <span class="uicontrol"> Rede de conteúdo hospedado </span> como método de upload no painel <span class="wintitle"> Envio de arquivo </span> do assistente, o URL será exibido aqui. Se você ainda não tiver gerado nenhum arquivo de feed, o URL não será válido até que o feed seja gerado com êxito. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Google Sitemaps**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Painel </p> </th> 
      <th colname="col2" class="entry"> <p>Nome do painel Assistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nome do feed </p> </td> 
      <td colname="col3"> <p>Especifica o nome do feed. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Mapas de campo </p> </td> 
      <td colname="col3"> <p>Permite mapear campos de feed específicos do fornecedor para campos de metadados de pesquisa/comercialização do site. Essa etapa de mapeamento no assistente é importante porque permite que os Feeds correlacionem as informações entre os campos no índice e os campos nos dados do feed. Na maioria dos casos, exceto Feeds <span class="wintitle"> genéricos </span>, as correlações são salvas em um modelo de pesquisa gerado dinamicamente. </p> <p>Cada linha na tabela Mapas de campo representa um mapeamento de campo. Na coluna Adicionar/Remover da tabela, clique em <span class="uicontrol"> + </span> para adicionar uma nova linha de mapeamento de campo; clique em <span class="uicontrol"> - </span> para excluir a linha de mapeamento de campo atualmente selecionada da tabela. Para associar um campo de feed a um campo de metadados, use as respectivas listas suspensas para escolher os campos desejados. </p> <p> <b>Uso avançado</b> </p> <p>Você pode criar seus próprios campos personalizados. Na lista <span class="wintitle"> suspensa Campos de feed, clique em </span> Personalizado <span class="uicontrol"> </span>. No campo de texto associado, insira um nome de tag personalizado para esse campo. Essa opção personalizada será útil se um feed precisar de campos específicos do fornecedor. </p> <p>Também é possível criar um campo de metadados personalizado. Na lista suspensa Campos de <span class="wintitle"> metadados </span> , clique em <span class="uicontrol"> Personalizado </span>. No campo de texto associado, insira um valor de campo de metadados personalizado. O valor é inserido no modelo pré-gerado e também pode ser usado para inserir tags de modelo de pesquisa personalizadas. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Pesquisar marcas de modelo </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Critérios de busca </p> </td> 
      <td colname="col3"> <p>Quando os arquivos de feed são gerados, um query de pesquisa é usado para filtrar os dados. Você define os filtros usados para o query de pesquisa neste painel. </p> 
        <ul id="ul_994585E89A044BD3A89A99D30F277432"> 
        <li id="li_61FA9246B9824E3C8124958C8EBFF0DA"> <span class="uicontrol"> Campo Meta </span> <p>Define em qual campo de metadados você deseja filtrar. </p> <p> <b>Uso avançado</b> </p> <p>Como o sistema de filtragem é um query de pesquisa padrão, você pode selecionar Formulário <span class="uicontrol"> Livre </span> na lista suspensa para inserir os parâmetros de pesquisa CGI e seus valores. É necessário escape de URL. O argumento de pesquisa <span class="codeph"> sp_q </span> é ignorado. É possível criar várias linhas de caixas de texto de Formulário gratuito. Entre cada linha, os argumentos são delimitados automaticamente com o &amp;'s. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Pesquisar parâmetros CGI </a>. </p> </li> 
        <li id="li_A5D00883738845C8B8F612A7521F160F"> <span class="uicontrol"> Critérios </span> <p>Define a operação de filtro. A operação de filtro selecionada na lista suspensa aplica o valor constante inserido na terceira coluna. </p> </li> 
        <li id="li_5A312C2984454C2CB518CA453AD9F6D2"> <span class="uicontrol"> Valor </span> <p>O valor constante. </p> </li> 
        <li id="li_666AAE1BC7A2432E91953B08EC7394DC"> <span class="uicontrol"> Ação </span> <p>Adiciona uma nova linha de mapeamento de campo ou exclui a linha realçada no momento. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envio de arquivo </p> </td> 
      <td colname="col3"> <p>Permite configurar o agendamento para enviar os arquivos de feed e definir o método que deseja usar para fazer upload dos arquivos. </p> 
        <ul id="ul_49B3255BE669424B925BBAEE4C9B385F"> 
        <li id="li_939828C774D440EBB0769F6D5B0BBA23"> <span class="uicontrol"> Agendar </span> <p>Define a frequência máxima de envio de um feed. Selecionar <span class="uicontrol"> Nunca </span> desliga o feed. Outros valores definem o período que o feed aguarda antes de enviar novamente. A decisão de submeter o feed é feita em cada índice. Em outras palavras, no final do índice, um feed é verificado para ver se expirou e precisa ser atualizado e enviado pelo fornecedor. Além disso, é usado como um método para impedir que uma conta envie em excesso para um fornecedor. Alguns fornecedores têm políticas contra fontes de feed de dados que carregam com frequência. Verifique a política do fornecedor do feed sobre a frequência dos envios. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_07B5BCF7936241A7915C4898B231184B"> <span class="uicontrol"> Método de upload </span> <p>A maioria dos feeds tem duas formas de distribuir os arquivos: FTP e Rede de conteúdo hospedado. </p> 
          <ul id="ul_74FA98A82754469BA5FADCC63FC364F7"> 
          <li id="li_02940B712D6444A8B65C0A51834187E6"> <span class="uicontrol"> FTP </span> <p>Os servidores de pesquisa/comercialização do site usam FTP passivo. </p> <p>O FTP é a única maneira de enviar um arquivo para outro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> - Especifica o nome do servidor FTP. Não inclua o protocolo ou o anterior "ftp://". </p> <p> <span class="uicontrol"> Nome de usuário FTP </span> - Especifica o nome da conta FTP. </p> <p> <span class="uicontrol"> Senha FTP </span> - Especifica a senha da conta FTP. </p> <p> <span class="uicontrol"> Nome do arquivo FTP </span> - Especifica o nome do arquivo a ser transmitido. Esse nome é um modelo se o feed gerar vários arquivos, normalmente incrementando um número no final do nome, mas antes da extensão. Por exemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Diretório FTP </span> - se um caminho de diretório específico for necessário, insira-o aqui. Não inclua o nome de arquivo no caminho. </p> </li> 
          <li id="li_EAE504436CD84452BA04BE51855A2BEF"> <span class="uicontrol"> Rede de conteúdo hospedado </span> <p>A Rede de Conteúdo é a maneira de disponibilizar arquivos dos servidores da Web de pesquisa/comercialização de sites. O recipient do feed o extrai dos servidores da Web usando uma solicitação HTTP. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> <p>Observe que qualquer um dos métodos de upload requer que você especifique o URL que o Google usa para recuperar o mapa do site, no campo URL do mapa do site <span class="wintitle"> principal </span> . O nome do arquivo do mapa do site também é determinado aqui. Se o mapa do site for grande, poderão existir vários arquivos e a convenção de nomenclatura será anexar um número de índice ao final do arquivo, começando com o número 1. O primeiro arquivo ou arquivo de índice não tem índice, como em <span class="codeph"> sitemap.xml </span>, <span class="codeph"> sitemap1.xml </span>, <span class="codeph"> sitemap2.xml </span> ... <span class="codeph"> sitemap12.xml </span>. </p> <p>Se você escolher <span class="uicontrol"> Rede de conteúdo hospedado </span> como método de upload, o URL dos arquivos terá os mesmos nomes de arquivo, mas o URL terá o caminho e o nome do host do serviço de hospedagem. Portanto, você redireciona as solicitações do mapa do site para a Rede de conteúdo hospedado. Você também deve conseguir extrair os arquivos do mesmo local. </p> <p>Depois que os arquivos de feed são criados e enviados para o destino intermediário, o Google é pingado e informa que o feed do mapa do site está pronto. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Verificação </p> </td> 
      <td colname="col3"> <p>Quando você chega ao <span class="wintitle"> painel </span> Verificação, seu feed é salvo nesse ponto. No entanto, os arquivos de feed reais não são salvos até mais tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_A1D889A84972419599FC83F39EA2676A"> 
        <li id="li_C8ED077B6DD1461E85A4914C1CFDBE88"> <span class="uicontrol"> Data View </span> <p>Permite que você clique no link para verificar a saída do feed por meio de uma visualização de dados exibida em forma de tabela. A visualização de dados também pode ajudá-lo a solucionar problemas, mostrando quais campos meta foram escolhidos e como qualquer critério de pesquisa especificado no painel Critérios de <span class="wintitle"> pesquisa </span> do assistente afeta a saída do feed. A visualização de dados é gerada dinamicamente, de modo que esteja disponível o tempo todo. </p> </li> 
        <li id="li_DACEE40703AF40EFBCD90D43825CE9C1"> <span class="uicontrol"> Arquivos de feed </span> <p>Depois que os arquivos de feed forem gerados, você poderá usar a lista suspensa <span class="uicontrol"> Arquivos de feed </span> para visualização dos arquivos dos servidores. Uma nova guia do navegador ou nova janela do navegador é exibida com o conteúdo do feed. Esse método é útil para ajudar a solucionar problemas de feeds com problemas de formatação. Observe que você não visualização os arquivos do destino final ou dos próprios fornecedores. </p> <p> Se o feed for novo, a lista suspensa fica vazia até que você gere os arquivos de feed. </p> </li> 
        <li id="li_1C530354B4F34EC79D92CEFEB5B39ED7"> <span class="uicontrol"> Link de rede de conteúdo </span> <p>Se você escolher <span class="uicontrol"> Rede de conteúdo hospedado </span> como método de upload no painel <span class="wintitle"> Envio de arquivo </span> do assistente, o URL será exibido aqui. Se você ainda não tiver gerado nenhum arquivo de feed, o URL não será válido até que o feed seja gerado com êxito. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Quando você concluir as etapas do assistente, clique em **[!UICONTROL Close]**.

## Editar um feed {#task_B855D28CD99B4FA58E2D4D4FD6DC9CEB}

É possível editar a configuração de um feed existente.

<!-- 

t_editing_a_feed.xml

 -->

>[!NOTE]
>
>Ao editar um feed, não é possível alterar o tipo de feed. Se precisar alterar o tipo de feed, exclua o feed existente e adicione um novo feed com o tipo desejado.

Consulte [Excluindo um feed](../c-about-settings-menu/c-about-searching-menu.md#task_7E39A140E69D43C6B61FB42E81051269).

**Para editar um feed**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Faça uma das seguintes opções:

* Na [!DNL Feeds] página, na [!DNL Name] coluna da tabela, clique na lista suspensa ao lado do nome de um feed e clique em **[!UICONTROL Edit feed]**.

* Na [!DNL Feeds] página, na [!DNL Name] coluna, clique no nome de um feed que você deseja alterar.

1. No assistente do feed, defina as opções desejadas para cada painel no assistente.

   Consulte as tabelas de opções em **Adicionar um feed**.
1. No final do assistente, no [!DNL Verification] painel, clique em **[!UICONTROL Close]**.

## Excluindo um feed {#task_7E39A140E69D43C6B61FB42E81051269}

Você pode excluir um feed que não precisa mais ou que não usa.

<!-- 

t_deleting_a_feed.xml

 -->

**Para excluir um feed**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Na [!DNL Feeds Menu] tela, na [!DNL Actions] coluna, clique **[!UICONTROL Delete]** no nome do feed que você deseja remover.
1. Na caixa de [!DNL Delete feed] diálogo, clique **[!UICONTROL Yes]** para confirmar a exclusão.

## Exibição de arquivos de feed {#task_1E413C7650DE466EA68925F72E086884}

Você pode acessar o último painel do assistente de feed para conceder acesso rápido para visualizar a visualização de dados do feed ou para baixar quaisquer arquivos de feed atuais do servidor. Essa funcionalidade é útil se você deseja verificar e examinar a saída do feed.

<!-- 

t_viewing_feed_files.xml

 -->

**Para visualização de arquivos de feed**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Na [!DNL Feeds] página, na [!DNL Name] coluna da tabela, clique na lista suspensa ao lado do nome de um feed e clique em **[!UICONTROL View Feed Files]**.
1. No [!DNL Verification] painel do assistente do feed, clique em **[!UICONTROL Show Data View]**.
1. Clique em **[!UICONTROL Close]**.

## Testando um feed sem upload de arquivo {#task_F1F390F72E0A4886B6CD4CD86EDB4C8C}

Você pode testar um feed sem fazer upload de arquivos para o destino final.

<!-- 

t_testing_a_feed_with_no_file_upload.xml

 -->

**Para testar um feed sem upload de arquivo**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Na [!DNL Feeds] página, na [!DNL Name] coluna da tabela, clique na lista suspensa ao lado do nome de um feed e clique em **[!UICONTROL Test Feed (No file upload)]**.
1. Na [!DNL Feeds] página, a [!DNL Feed Status] coluna é atualizada durante e após o teste.

## Geração e upload de um feed {#task_C9A57827C7674035B62A22D310DDAA0C}

Você pode gerar e enviar arquivos de feed manualmente para o destino final, independentemente da programação definida no [!DNL File Submission] painel do assistente de feed.

<!-- 

t_generating_and_uploading_a_feed.xml

 -->

Consulte também [Criação de um feed](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250).

**Para gerar e carregar um feed**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Na [!DNL Feeds] página, na [!DNL Name] coluna da tabela, clique na lista suspensa ao lado do nome de um feed e clique em **[!UICONTROL Generate and Upload Feed]**.
1. Na [!DNL Feeds] página, a [!DNL Feed Status] coluna é atualizada durante e após a geração e o upload do feed de dados.
