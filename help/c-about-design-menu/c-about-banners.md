---
description: Você pode usar os Banners para gerenciar os anúncios em banners em seu site.
solution: Target
title: Sobre banners
topic-legacy: Design,Site search and merchandising
uuid: 653b567d-5cf3-41a0-a260-a6912d0fd20d
exl-id: 2c1de213-e6fc-425b-9971-43a09c07d07c
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '4796'
ht-degree: 1%

---

# Sobre banners {#about-banners}

Você pode usar os Banners para gerenciar os anúncios de banner que estão em seu site.

## Uso de banners {#concept_5BBE01FEC6134393B43CC917C8CC64DA}

<!-- 

c_about_banners.xml

 -->

Há dois métodos que você pode usar para adicionar anúncios de banner ao seu site.

O primeiro método é adicionar banners por meio do Target, Search &amp; Promote. Os banners são trechos de código HTML exibidos no momento em que um cliente pesquisa em seu site. Seu banner pode incluir texto ou uma imagem no formato GIF, JPEG ou PNG, ou uma combinação de ambos. Você pode selecionar dentre tamanhos predefinidos ou definir suas próprias dimensões personalizadas para caber em sua página. O código HTML usado para exibir o banner também pode especificar itens, como o estilo da fonte a ser usada e a borda. Esse método de adicionar um banner oferece funcionalidade básica e não requer software adicional.

O segundo método é usar o Adobe Dynamic Media Classic, um serviço de gerenciamento e publicação de mídia dinâmica. Uma conta válida do Adobe Dynamic Media Classic permite gerenciar e fornecer conteúdo de banner diretamente para o Target, Search &amp; Promote, usando o Dynamic Media Classic. Em pesquisa/merchandising no site, você configura o acesso à sua conta do Dynamic Media Classic. Em seguida, abra o navegador de mídia do Dynamic Media Classic e escolha um ativo de mídia dinâmica que deseja utilizar como banner.

>[!NOTE]
>
>Antes de usar ativos de mídia dinâmica como banners em pesquisa/merchandising do site, os ativos são carregados e preparados para publicação no Sistema de publicação do Scene7. Você pode fazer upload de ativos de dentro da pesquisa/comercialização do site e prepará-los automaticamente para publicação pelo Scene7 Publishing System. Ou você pode fazer upload e publicar ativos de todo o Scene7 Publishing System.

## Integração de banners com o Adobe Scene7 Publishing System {#section_D4D7ADEA6A6348E68EDA138E184FE579}

Você pode usar os tipos de ativos do Dynamic Media Classic como banners em pesquisa/merchandising do site, incluindo imagens, banners dinâmicos e modelos, como modelos de imagem ou modelos de Flash.

Os modelos são arquivos de imagem em camadas dinamicamente criados e endereçáveis, como arquivos em camadas em aplicativos de edição de imagens, como o Adobe Photoshop®. Diferentemente de um arquivo de imagem estática, um modelo pode incluir parâmetros. Por meio dos parâmetros, você pode personalizar as propriedades variáveis da imagem e o conteúdo da imagem.

>[!NOTE]
>
>Você também pode criar modelos a partir de designs baseados em layout usando a Publicação de modelo no Scene7 Publishing System e arquivos do Adobe Illustrator e Adobe InDesign.

Consulte [Publicação de modelo](https://help.adobe.com/en_US/scene7/using/WSFBFBAD30-2694-4b18-B7CE-894F9FC5CDDF.html) no Guia do usuário do Dynamic Media Classic (Scene7).

Um modelo pode conter qualquer número de camadas de imagem e camadas de texto. Você pode converter um arquivo estático contendo camadas, como um arquivo PSD em camadas, em um modelo ou criar modelos no Dynamic Media Classic. Você pode criar camadas de texto em modelos usando fontes que foram carregadas no Scene7 Publishing System. Após adicionar texto a um modelo, é possível formatá-lo alterando sua justificação, fontes, tamanho da fonte e cor.

Usando a tela Parâmetros no Dynamic Media Classic, você pode converter qualquer aspecto de um modelo em um parâmetro endereçável. Ao fazer isso, você pode alterar a imagem em camadas a ser usada ou o valor do texto a ser usado no modelo. Os parâmetros são passados com a string do URL, permitindo alterar qualquer parâmetro para personalizar dinamicamente a imagem de resposta gerada do servidor de imagem.

Você pode aprender mais sobre como usar o Dynamic Media Classic para criar modelos e parametrizar as propriedades nas camadas para usá-las em banners.

Consulte [Fundamentos do modelo](https://help.adobe.com/en_US/scene7/using/WS60B68844-9054-4099-BF69-3DC998A04D3C.html) no Guia do usuário do Dynamic Media Classic (Scene7).

**Upload e publicação de ativos**

Você deve fazer upload e publicar ativos no Dynamic Media Classic antes de usá-los para banners em pesquisa/merchandising de site. Esse pré-requisito também inclui todos os ativos que um modelo de imagem ou um modelo de Flash usam. Use sua conta do Dynamic Media Classic para fazer upload e publicar ativos digitais. Ou você pode usar a pesquisa/comercialização do site para fazer upload de um ativo digital e, em seguida, fazer com que o Dynamic Media Classic o publique automaticamente para você, com base nas configurações de upload. Se você tentar escolher um ativo que ainda não foi carregado e publicado, você será notificado na interface do usuário e terá a opção de fazer upload dele antes de continuar.

Saiba mais sobre como fazer upload e publicar ativos digitais usando o Scene7 Publishing System.

Consulte [Fazer upload e publicar ativos](https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html) no Guia do usuário do Dynamic Media Classic (Scene7).

>[!NOTE]
>
>Para usar a funcionalidade de upload no visualizador de ativos do Dynamic Media Classic, verifique se a conta do Dynamic Media Classic usada tem a função de &quot;Administrador da empresa do SPS&quot; já definida.

Consulte [Configuração de administração](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) no Guia do Usuário do Dynamic Media Classic (Scene7).

**Alteração dos parâmetros do modelo do Dynamic Media Classic em um banner usando regras de negócios**

Se você tiver adicionado um ativo do Dynamic Media Classic como banner, poderá usar [!DNL Visual Rule Builder] em [!DNL Business Rules] para adicioná-lo a qualquer área de banner no seu site. Por exemplo, você adiciona o banner às suas páginas de resultados da pesquisa, assim como faria com qualquer outro banner. Você também pode substituir os valores dos parâmetros padrão nos modelos do Dynamic Media Classic, personalizando-os de acordo com suas necessidades específicas. Esse tipo de funcionalidade permite personalizar modelos do Dynamic Media Classic com diferentes mensagens de marketing e hiperlinks para diferentes pontos de extremidade.

Consulte também [Adicionar uma nova regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).

Consulte também [Editar uma regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

## Adicionar um banner {#task_549D02B5F73B4158B105A94E39D937B7}

Você pode usar [!DNL Banners] para gerenciar os anúncios de banner e onde eles são colocados em seu site. Ao adicionar um banner, você está fazendo referência externa à imagem por meio de trechos de código HTML exibidos no momento da pesquisa.

<!-- 

t_adding_a_new_banner.xml

 -->

Se você tiver uma conta válida do Adobe Dynamic Media Classic, poderá adicionar anúncios de banner por meio do Scene7 Publishing System.

Consulte [Adicionar um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

Consulte [Configuração do acesso à sua conta Adobe Dynamic Media Classic](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D).

**Para adicionar um banner**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Na página [!DNL Banners], na lista suspensa **[!UICONTROL Add Banner]**, selecione **[!UICONTROL HTML code]**.
1. Na caixa de diálogo [!DNL Add Banner], defina as opções desejadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome </p> </td> 
      <td colname="col2"> <p>Obrigatório. Identifica o nome do banner. O nome é usado para fazer referência ao banner quando você o adiciona no Construtor de regras visuais em Regras comerciais. O nome não aparece no próprio banner. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" type="task" format="dita" scope="local"> Adicionando uma nova regra de negócios.</a> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>HTML do banner </p> </td> 
      <td colname="col2"> <p> Permite colar o código HTML associado ao banner. </p> <p>Qualquer código HTML é aceitável, incluindo código CSS rodeado por 
        <code>
          &lt;style&gt; 
        </code> tags ou código JavaScript rodeado por 
        <code>
          &lt;script&gt; 
        </code> tags. Por exemplo, o seguinte bloco de código é para um banner de texto do tipo Horizontal top : <code> &lt;div&nbsp;style="width:&nbsp;684px;&nbsp;background-image:&nbsp;url('https://www.brough.com/blackb.gif');&nbsp; 
          padding-top:&nbsp;10px;&nbsp;padding-bottom:&nbsp;10px;&nbsp;color:&nbsp;white;&nbsp;font-family:&nbsp;verdana;&nbsp; 
          text-align:&nbsp;center;&nbsp;font-size:&nbsp;20px;"&gt;&nbsp;Sound&nbsp;Study&nbsp;ships&nbsp;free!&nbsp;&lt;/div&gt; </code>No exemplo a seguir, o bloco de código é para uma imagem de abertura completa: <code> &lt;img&amp;nbsp;src='https://geometrixx.com/images/GEOAds/geometrixx-beauty-home-01.jpg'&amp;nbsp;border="0"&amp;nbsp;/&gt; </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo </p> </td> 
      <td colname="col2"> <p>Especifica os seguintes tipos de banners: 
        <ul id="ul_6423AEDB9E664049989EB529D63C4A62"> 
          <li id="li_BF6CD60B3ED748D49CFFB9C5D607661C"> <span class="uicontrol"> [novo tipo]  </span> <p>Permite especificar o tipo de banner desejado, incluindo as dimensões e o nome. </p> </li> 
          <li id="li_1A29AB22AD644E60A12298187B5E898E"> <span class="uicontrol"> Splash completo  </span> <p>A dimensão definida desse tipo de banner é de 680 pixels de largura e 650 pixels de altura. Como opção, você pode especificar o nome do tipo ou aceitar o nome padrão que é o nome do próprio tipo de banner. </p> </li> 
          <li id="li_2BE06D013CB54DDE851051BFC038BB57"> <span class="uicontrol"> Parte superior horizontal  </span> <p> O banner é posicionado na área superior do site. Esse tipo é útil se você pretende adicionar hiperlinks à esquerda ou à direita do banner. A dimensão definida desse tipo de banner tem 468 pixels de largura e 60 pixels de altura. Como opção, você pode especificar o nome do tipo ou aceitar o nome padrão que é o nome do próprio tipo de banner. </p> </li> 
          <li id="li_EC35AB92234749F08AA8A9BD26D0EA8D"> <span class="uicontrol"> Parte superior horizontal - Largura completa  </span> <p>Esse tipo é o padrão quando você adiciona um novo banner. O banner é posicionado na área superior do site e ocupa a largura total da página. A dimensão definida desse tipo de banner é de 670 pixels de largura e 150 pixels de altura. Como opção, você pode especificar o nome do tipo ou aceitar o nome padrão que é o nome do próprio tipo de banner. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tags </p> </td> 
      <td colname="col2"> <p>Adiciona tags ou "palavras-chave" que você deseja associar ao banner. Se você usar muitos banners, a adição de tags pode ajudá-lo a refinar sua pesquisa de banner para que você possa localizar rapidamente o banner correto para suas necessidades. Também é possível excluir quaisquer tags adicionadas. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar um banner {#task_D4081083BE7B40F5A003D1A2F1435AEA}

Use [!DNL Edit Banner] para alterar coisas como o nome do banner, o HTML do banner, o tipo de banner e quaisquer tags associadas.

<!-- 

t_editing_a_banner.xml

 -->

Se você tiver adicionado um banner usando pesquisa/merchandising do site, também poderá editar o banner usando o Adobe Dynamic Media Classic.

Consulte também [Edição de um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

**Para editar um banner**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Na página [!DNL Banners], clique em ![](assets/icon_edit_16.gif).

   acima de uma miniatura do banner que você deseja editar.
1. Na página [!DNL Edit Banner], defina as opções desejadas.

   Consulte a tabela de opções em [Adicionar um banner](../c-about-design-menu/c-about-banners.md#task_549D02B5F73B4158B105A94E39D937B7).
1. Quando terminar de editar o banner, clique em **[!UICONTROL Save]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Adicionar um banner usando o Adobe Dynamic Media Classic {#task_AD1E0C00A9E04B1FA819EB93288786B3}

Você pode usar [!DNL Banners] para gerenciar os anúncios de banner em seu site. Ao adicionar um banner usando o Adobe Dynamic Media Classic, você pode escolher qualquer ativo digital que tenha carregado no Scene7 Publishing System.

<!-- 

t_adding_a_banner_using_adobe_scene7.xml

 -->

Para adicionar um banner usando o Adobe Dynamic Media Classic, verifique se você configurou o acesso à sua conta válida do Dynamic Media Classic.

Consulte [Configuração do acesso à sua conta Adobe Dynamic Media Classic](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D).

**Para adicionar um banner usando o Adobe Dynamic Media Classic**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Banners.]**
1. Na página [!DNL Banners] , na lista suspensa **[!UICONTROL Add Banner]**, clique em **[!UICONTROL Adobe Scene7]**.
1. Na caixa de diálogo [!DNL Pick an Asset], no painel esquerdo, use as opções de navegação na interface do usuário para localizar a pasta que contém o ativo digital que deseja usar em um banner.

   Com exceção das opções de navegação de ativos, todas as outras opções dependem do ativo digital selecionado para adição ou edição.

   Use as opções de navegação de ativos para localizar um ativo que deseja usar para um novo banner na pesquisa/comercialização do site. As opções de navegação se aplicam a todos os tipos de ativos digitais selecionados.

   >[!NOTE]
   >
   >As opções de navegação do ativo não são exibidas ao editar o banner na caixa de diálogo [!DNL Change Parameters].

   Consulte [Editar um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   **Opções de navegação de ativos**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção de navegação </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/S7_folders.png"> </p> </td> 
      <td colname="col2"> <p>Permite selecionar a conta do Dynamic Media Classic para sua empresa específica na lista suspensa e também navegar pelas pastas de ativos digitais dentro dessa conta. </p> <p>Ao selecionar uma pasta, o painel direito da caixa de diálogo <span class="wintitle"> Selecionar um ativo </span> mostra todos os ativos digitais disponíveis que estão contidos nessa pasta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_folderhistory.png"> </p> </td> 
      <td colname="col2"> <p>Permite avançar ou retroceder pelo histórico de navegação de pastas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_reloadfolder.png"> </p> </td> 
      <td colname="col2"> <p>Atualiza a lista de ativos digitais que são exibidos para uma pasta selecionada. </p> <p>Talvez seja necessário clicar nesse controle ao mover, excluir ou renomear um ativo selecionado usando a lista suspensa <span class="uicontrol"> Ações </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_list_or_grid.png"> </p> </td> 
      <td colname="col2"> <p>Exibe ativos digitais em uma exibição em lista. A lista exibe o ícone associado de cada ativo ou a imagem em miniatura, o nome do arquivo, o tipo de ativo digital, as dimensões (quando aplicável) e a data em que foi editado pela última vez. </p> <p>A exibição em grade exibe ativos digitais na pasta selecionada como ícones, miniaturas ou ambos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_actionsdropdown.png"> </p> </td> 
      <td colname="col2"> <p>Na exibição de lista, é possível mover, excluir ou renomear um ativo digital selecionado. </p> <p>Na exibição em grade, é possível mover ou excluir um ou mais ativos digitais selecionados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_upload.png"> </p> </td> 
      <td colname="col2"> <p>Abre a caixa de diálogo <span class="wintitle"> Fazer upload </span> onde é possível fazer upload de um ativo digital selecionado do desktop ou de um servidor externo para usá-lo como um banner. </p> <p>Após fazer upload do ativo, um trabalho de publicação é automaticamente agendado para você no Scene7 Publishing System. </p> <p>Consulte a tabela de opções em <a href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita" scope="local"> Adicionar um banner usando o Adobe Dynamic Media Classic </a>. </p> <p>Saiba mais sobre como fazer upload e publicar ativos digitais usando o Scene7 Publishing System. </p> <p>Consulte <a href="https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html" scope="external" format="html"> Fazer upload e publicar ativos </a> no Guia do usuário do sistema de publicação do Scene7. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_searchfield.png"> </p> </td> 
      <td colname="col2"> <p>Permite pesquisar um ativo digital por palavra-chave ou pesquisar por local de arquivo dentro da pasta selecionada e suas subpastas associadas. </p> <p>Ao clicar no campo de pesquisa, ele adiciona automaticamente um campo de filtro opcional para você. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Adiciona outro filtro de ativo para que você possa refinar a lista de ativos digitais exibidos por tipo ou por uma data específica. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_Kindfilter.png"> </p> </td> 
      <td colname="col2"> <p>Refine a lista de ativos digitais exibidos para mostrar apenas aqueles de um determinado tipo, como Flash, Imagem, Modelo ou Qualquer. </p> <p>Clique em <img src="assets/s7_deletefilter.png"> para excluir o filtro da pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_datefilter.png"> </p> </td> 
      <td colname="col2"> <p>Refine a lista de ativos digitais exibidos para mostrar apenas aqueles criados ou editados antes de uma determinada data ou após uma determinada data. </p> <p>Clique em <img src="assets/s7_deletefilter.png" /> para excluir o filtro da pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_assetzoom.png"> </p> </td> 
      <td colname="col2"> <p>Permite arrastar o controle deslizante para a esquerda ou para a direita para reduzir ou ampliar toda a exibição do painel de ativos digitais, respectivamente. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opções de propriedades**

   As opções Propriedades são exibidas se você escolher um modelo de Flash, um modelo de imagem ou uma imagem. Dependendo do ativo digital escolhido, nem todas as opções estão disponíveis.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção Propriedades </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome </p> </td> 
      <td colname="col2"> <p>O nome descritivo do modelo ou imagem, sem espaços em branco. Como opção, você pode incluir a especificação do tamanho da imagem no nome para ajudar os usuários a identificar ainda mais o ativo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato </p> </td> 
      <td colname="col2"> <p>Identifica o formato da imagem ou do modelo de imagem. </p> <p>Você pode escolher entre os seguintes formatos: </p> 
        <ul id="ul_9A19421BCC424CF585645049DCB87F10"> 
        <li id="li_A4913D783BD547F9AFA1A259C56EC2B3">jpeg </li> 
        <li id="li_66237D7BE8754FB0B0088CE5A02C0214">png </li> 
        <li id="li_4EDDFD7C8AB04677BEC20EFC9AEBBF1F">png-alfa </li> 
        <li id="li_4FCB03C29AE647ACBAF5105016DF7579">gif </li> 
        <li id="li_B884BD7DFF1845FAA9C58EF09B888A77">gif-alfa </li> 
        </ul> <p>Essa opção não se aplica aos modelos de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Qualidade </p> </td> 
      <td colname="col2"> <p>Controla o nível de compactação de imagens em formato JPEG ou GIF. Essa configuração afeta o tamanho do arquivo e a qualidade da imagem. A escala de qualidade é de 1 a 100. </p> <p>Quando você arrasta o controle deslizante para a esquerda ou para a direita, a imagem na janela de visualização é atualizada para refletir a alteração na qualidade. </p> <p>Essa opção não se aplica aos modelos de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Largura </p> </td> 
      <td colname="col2"> <p>Especifica a largura do ativo digital, em pixels. Essa dimensão é a largura em que o ativo é visualizado por clientes que visitam seu site. </p> <p>Essa opção não se aplica aos modelos de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Altura </p> </td> 
      <td colname="col2"> <p>Especifica a altura do ativo digital, em pixels. Essa dimensão é a altura em que o ativo é visualizado por clientes que visitam seu site. </p> <p>Essa opção não se aplica aos modelos de Flash. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opções de link do banner**

   As opções de Link do banner são exibidas somente se você escolher uma imagem ou um modelo de imagem para seu banner.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção Link do banner </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>URL de link </p> </td> 
      <td colname="col2"> <p>Especifica o endereço de URL ao qual você deseja que o banner seja vinculado quando um cliente clicar na imagem. </p> <p>Se você não quiser que o banner se vincule a nada, deixe o campo Link URL em branco. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Target </p> </td> 
      <td colname="col2"> <p>Especifica onde abrir o banner vinculado, como uma nova janela do navegador ou uma nova guia. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opção Modificar links**

   A opção Modificar links só será exibida se você escolher um modelo de Flash para seu banner.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção Modificar links </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img placement="inline" id="image_EBB8159690C74D4692B5DF945B045E0B" src="assets/icon_edit_16.gif" /> </p> </td> 
      <td colname="col2"> <p>Permite editar o campo de link URL usado no modelo de Flash. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opções de Substituir texto**

   As opções Substituir texto são exibidas somente se você escolher um modelo de Flash para seu banner que tenha camadas de texto editáveis.

   Todas as alterações feitas no texto no modelo de Flash são refletidas na janela Visualização.

   >[!NOTE]
   >
   >Se você adicionar um comando search and replace para substituir &quot;vaca&quot; por &quot;maçã&quot; e, em seguida, criar um segundo comando para substituir &quot;maçã&quot; por &quot;laranja&quot;, o segundo comando não terá efeito.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção Substituir texto </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Adiciona um campo de pesquisa e substituição. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_deletefilter.png"> </p> </td> 
      <td colname="col2"> <p>Exclui um campo Pesquisar e substituir e restaura o texto usado anteriormente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisa  </p> </td> 
      <td colname="col2"> <p>Permite inserir um termo de pesquisa para texto não vinculado nas camadas do modelo de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Substituir </p> </td> 
      <td colname="col2"> <p>Permite que você especifique o texto a ser inserido no lugar do texto que está procurando. </p> <p>Ao pressionar <span class="uicontrol"> Enter </span> neste campo, a janela de pré-visualização é atualizada com o texto de substituição. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opções de parâmetros**

   As opções de parâmetros aparecem somente se você escolher um modelo de imagem ou um modelo de Flash para o seu banner. As opções de parâmetros reais variam de acordo com a forma como o modelo foi criado e parametrizado no Sistema de Publicação Scene7. Por exemplo, seu modelo pode parametrizar campos que permitem alterar itens como texto, estilo de fonte, preço, códigos especiais usados para envio gratuito, o tamanho da imagem dentro do banner ou até mesmo procurar uma imagem diferente para usar.

   >[!NOTE]
   >
   >Esteja ciente de que qualquer alteração feita nos parâmetros pode ser substituída por regras de negócios. Os parâmetros só servem como padrões quando nenhuma regra comercial é criada e, de outra forma, alteraria os parâmetros.

   Consulte [Adicionar uma nova regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).

   Consulte [Editar uma regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

   **Alternar as opções de visibilidade da camada**

   A opção Alternar visibilidade da camada se aplica somente se você escolher um modelo de Flash para o banner.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção Alternar visibilidade da camada </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_togglelayervisibility.png"> </p> </td> 
      <td colname="col2"> <p>Permite ativar ou desativar a visibilidade das várias camadas que compõem o arquivo de modelo de Flash. </p> <p>Cada vez que você ativa ou desativa a visibilidade de uma camada, a janela de visualização é atualizada para atualizar a exibição. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   (Opcional) Se o ativo digital que você deseja usar para um banner não estiver disponível na pasta selecionada, talvez seja necessário carregá-lo. Clique em **[!UICONTROL Upload]** e selecione o arquivo e as opções desejadas. O arquivo é carregado na pasta selecionada.

   >[!NOTE]
   >
   >Se você quiser usar a funcionalidade de upload no visualizador de ativos do Scene7, verifique se a conta do Scene7 usada tem a função de &quot;Administrador da empresa do SPS&quot; já definida.

   Consulte [Configuração de administração](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) no Guia do Usuário do Sistema de Publicação do Scene7.

   **Opções básicas**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Navegar </p> </td> 
      <td colname="col2"> <p> Permite navegar até o arquivo que deseja fazer upload, publicar e selecionar para uso como banner. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Substituir </p> </td> 
      <td colname="col2"> <p>Os arquivos carregados substituem os arquivos existentes pelo mesmo nome de arquivo, na pasta selecionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Preferência de email </p> </td> 
      <td colname="col2"> <p> Permite escolher qual notificação por email você obtém para o upload, ou você pode optar por não ser notificado para nada relacionado ao trabalho de upload. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opções avançadas**

   Ao carregar arquivos de imagem PostScript (EPS) ou Illustrator (AI), você pode formatá-los de várias maneiras. Você pode rasterizar os arquivos, convertê-los em FXG para publicação de modelos, manter o plano de fundo transparente, escolher uma resolução e escolher um espaço de cores.

   Os PSD (arquivos de documento do Photoshop) são usados com mais frequência no Dynamic Media Classic para criar modelos. Ao carregar um arquivo PSD, você pode criar um modelo do Dynamic Media Classic automaticamente a partir do arquivo (selecione a opção **[!UICONTROL Create Template]** ).

   O Scene7 Publishing System cria várias imagens de um arquivo PSD com camadas se você usar o arquivo para criar um modelo; ele cria uma imagem para cada camada.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Nome do grupo de opções </p> </th> 
      <th colname="col02" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Opções de perfil de cores </p> </td> 
      <td colname="col02"> <p>Perfil de cores </p> </td> 
      <td colname="col2"> <p> Permite escolher entre as seguintes opções: </p> 
        <ul id="ul_6927BC08CA2647EDB2C85DAD2B82AE31"> 
        <li id="li_CA3F44FF9C0F4CE987DCB0AF9303C2E4"> <span class="uicontrol"> Converter em SRGB  </span> <p>Converte em SRGB (Azul Verde Vermelho Padrão). SRGB é o espaço de cores recomendado para exibir imagens nas páginas da Web. </p> </li> 
        <li id="li_FCCEE6B14CCD4246ADA152932010ABF1"> <span class="uicontrol"> Manter espaço de cor original  </span> <p>Mantém o espaço de cores original. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções de edição de imagem </p> </td> 
      <td colname="col02"> <p>Criar máscara a partir do caminho de recorte </p> </td> 
      <td colname="col2"> <p>Crie uma máscara para a imagem com base em suas informações de traçado de recorte. Essa opção se aplica a imagens criadas com aplicativos de edição de imagens nas quais um traçado de recorte foi criado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções de PostScript </p> <p>Opções do Illustrator </p> </td> 
      <td colname="col02"> <p>Processando </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> A  </span> opção Rasterizar converte gráficos vetoriais no formato de arquivo em bitmap. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opções de postscript </p> <p>Opções do Illustrator </p> </td> 
      <td colname="col02"> <p> Resolução </p> </td> 
      <td colname="col2"> <p> Determina a configuração de resolução. Essa configuração determina quantos pixels são exibidos por polegada no arquivo. O padrão é 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opções de PostScript </p> <p>Opções do Illustrator </p> </td> 
      <td colname="col02"> <p> Espaço da cor </p> </td> 
      <td colname="col2"> <p>Permite escolher um espaço de cores para o arquivo Illustrator. O espaço de cores RGB é preferível para visualização online. </p> <p>Você pode escolher entre as seguintes opções de espaço de cores: </p> 
        <ul id="ul_0E83E2762A574480B243F963A7FB2ACD"> 
        <li id="li_B9FEC7D220D04CCABACD30839051DAE4"> <span class="uicontrol"> Detectar automaticamente  </span> <p> Mantém o espaço de cores do arquivo PDF. </p> </li> 
        <li id="li_ED0EB3B12BCF41C7AFC435447010B6FF"> <span class="uicontrol"> Forçar como RGB  </span> <p> Converte para o espaço de cores RGB. </p> </li> 
        <li id="li_3FB5DD8887C540BC97148A4D63B38F72"> <span class="uicontrol"> Forçar como CMYK  </span> <p> Converte para o espaço de cores CMYK. </p> </li> 
        <li id="li_6C018D3A4B254880AD41896E9F4AF3D9"> <span class="uicontrol"> Forçar como Escala de Cinza  </span> <p> Converte para o espaço de cor Escala de Cinza. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opções de PostScript </p> <p>Opções do Illustrator </p> </td> 
      <td colname="col02"> <p> Manter plano de fundo transparente </p> </td> 
      <td colname="col2"> <p>Mantém a transparência em segundo plano do arquivo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções do Photoshop </p> </td> 
      <td colname="col02"> <p> Manter camadas </p> </td> 
      <td colname="col2"> <p>Remove as camadas na PSD, se houver, em ativos individuais. As camadas de ativo permanecem associadas ao PSD. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opções do Photoshop </p> </td> 
      <td colname="col02"> <p>Criar modelo </p> </td> 
      <td colname="col2"> <p> Cria um modelo a partir das camadas no arquivo PSD. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opções do Photoshop </p> </td> 
      <td colname="col02"> <p> Extrair texto </p> </td> 
      <td colname="col2"> <p> Extrai o texto para que os clientes possam pesquisar por palavras-chave dentro de um banner. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções do Photoshop </p> </td> 
      <td colname="col02"> <p> Estender camadas </p> </td> 
      <td colname="col2"> <p>Estende o tamanho das camadas de imagem cortadas até o tamanho da camada de plano de fundo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções do Photoshop </p> </td> 
      <td colname="col02"> <p> Nomenclatura de camada </p> </td> 
      <td colname="col2"> <p>As camadas no arquivo PSD são carregadas como imagens separadas. Você pode selecionar entre as seguintes opções para decidir como deseja nomear essas imagens no Sistema de Publicação do Scene7: </p> 
        <ul id="ul_C2A25177A07740CA90B32C638304D39F"> 
        <li id="li_477D5BFF7238454BBF0E04B22DE378F7"> <span class="uicontrol"> Usar nome de camada do arquivo PSD  </span> <p>Nomes das imagens após os nomes das camadas no arquivo PSD. Por exemplo, uma camada chamada <span class="codeph"> Tag de preço </span> no arquivo PSD original se torna uma imagem chamada <span class="codeph"> Tag de preço </span>. No entanto, se os nomes de camada no arquivo PSD forem nomes de camada padrão do Photoshop (Plano de fundo, Camada 1, Camada 2 e assim por diante), as imagens serão nomeadas após seus números de camada no arquivo PSD, não seus nomes de camada padrão. </p> </li> 
        <li id="li_EB4173B884FC41328CFBDE27DA6D43AA"> <span class="uicontrol"> Usar o nome do arquivo PSD e o número do anexo  </span> <p>Nomes das imagens depois de seus números de camada no arquivo PSD, ignorando os nomes da camada original. As imagens são nomeadas com o nome do arquivo Photoshop e um número de camada anexado. Por exemplo, a segunda camada de um arquivo chamado <span class="codeph"> Spring Ad.psd </span> é chamada de <span class="codeph"> Spring Ad_2 </span> mesmo que tenha um nome não padrão no Photoshop. </p> </li> 
        <li id="li_10B2D2DE2FD24BD08DB56D1D95ABA53D"> <span class="uicontrol"> Usar o nome de arquivo PSD e o nome ou número da camada  </span> <p>Nomes das imagens após o arquivo PSD seguido do nome da camada ou do número da camada. O número da camada é usado se os nomes da camada no arquivo PSD forem nomes padrão da camada do Photoshop. Por exemplo, uma camada chamada <span class="codeph"> Tag de preço </span> em um arquivo PSD chamado <span class="codeph"> SpringAd </span> é chamada <span class="codeph"> Tag Ad_Price de primavera </span>. Uma camada com o nome padrão <span class="codeph"> Camada 2 </span> é chamada <span class="codeph"> Primavera Ad_2 </span>. </p> </li> 
        <li id="li_5E57AC0719D4484B9C9BD14DB42B4455"> <span class="uicontrol"> Criar pasta com base no nome de arquivo PSD  </span> <p>Cria uma pasta para as imagens da camada usando o nome do arquivo do PSD. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções do Photoshop </p> </td> 
      <td colname="col02"> <p>Âncora </p> </td> 
      <td colname="col2"> <p>Especifique como as imagens são ancoradas em modelos que são gerados a partir da composição em camadas produzida a partir do arquivo PSD. </p> <p>Por padrão, a âncora é o centro. Uma âncora central permite que imagens de substituição preencham melhor o mesmo espaço, independentemente da proporção da imagem de substituição. Imagens com um aspecto diferente que substituem essa imagem, ao referenciar o modelo e usar substituição de parâmetro, ocupam efetivamente o mesmo espaço. Altere para uma configuração diferente se o aplicativo exigir as imagens de substituição para preencher o espaço alocado no modelo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções de PDF </p> </td> 
      <td colname="col02"> <p>Processando </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> A  </span> opção Rasterizar remove as páginas do arquivo PDF e converte gráficos vetoriais em imagens bitmap.  
        <!--Choose this option to create an eCatalog. (This option is thedefault.)--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções de PDF </p> </td> 
      <td colname="col02"> <p> Resolução </p> </td> 
      <td colname="col2"> <p>Determina a configuração de resolução. Essa configuração determina quantos pixels são exibidos por polegada no arquivo PDF. O padrão é 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções de PDF </p> </td> 
      <td colname="col02"> <p> Espaço da cor </p> </td> 
      <td colname="col2"> <p>Permite escolher um espaço de cores para o arquivo PDF. A maioria dos arquivos PDF tem imagens coloridas RGB e CMYK. O espaço de cores RGB é preferível para visualização online. </p> <p>Você pode escolher entre as seguintes opções de espaço de cores: </p> 
        <ul id="ul_44A8C39DEB21473F9375E3962F14D3C6"> 
        <li id="li_1046FA0017934C5EB7C0100F8F78507D"> <span class="uicontrol"> Detectar automaticamente  </span> <p> Mantém o espaço de cores do arquivo PDF. </p> </li> 
        <li id="li_561CCF705EDD451993D2DA2EB33F05F7"> <span class="uicontrol"> Forçar como RGB  </span> <p> Converte para o espaço de cores RGB. </p> </li> 
        <li id="li_D9E8CF61C40140979484EDEF7DAD2C44"> <span class="uicontrol"> Forçar como CMYK  </span> <p> Converte para o espaço de cores CMYK. </p> </li> 
        <li id="li_F3606B45C0F84BA594263EA12243F67A"> <span class="uicontrol"> Forçar como Escala de Cinza  </span> <p> Converte para o espaço de cor Escala de Cinza. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opções de PDF </p> </td> 
      <td colname="col02"> <p>Gerar automaticamente o catálogo eletrônico a partir de PDF de várias páginas </p> </td> 
      <td colname="col2"> <p> Cria automaticamente um eCatalog a partir do arquivo PDF. O eCatalog é nomeado após o arquivo PDF que você carregou. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opções de PDF </p> </td> 
      <td colname="col02"> <p>Extrair palavras-chave </p> </td> 
      <td colname="col2"> <p>Extrai palavras do arquivo PDF para que ele possa ser pesquisado por palavras-chave. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. No painel direito, clique na imagem, modelo ou arquivo de Flash desejado.

   A janela pop-up [!DNL Pick An Asset] é exibida.
1. (Opcional) Na janela pop-up [!DNL Pick An Asset], na lista suspensa [!DNL Actions], execute um dos seguintes procedimentos:

   * Clique em **[!UICONTROL Move]**. Na caixa de diálogo [!DNL Select a folder to move to], selecione a pasta onde deseja mover o ativo digital. Clique em **[!UICONTROL Move]**.

      Você também pode selecionar vários ativos digitais que deseja mover para outra pasta.

   * Clique em **[!UICONTROL Delete]**. Na caixa de diálogo [!DNL Delete Selected Assets], clique em **[!UICONTROL Delete]**.

      Você também pode selecionar vários ativos digitais que deseja excluir da pasta.

   * Clique em **[!UICONTROL Rename]**. Na caixa de diálogo [!DNL Enter a new name for], no campo de texto, digite um novo nome para o ativo digital. Clique em **[!UICONTROL Rename]**.

1. (Opcional) Dependendo do ativo digital selecionado, no painel esquerdo da janela pop-up [!DNL Pick an Asset], defina as opções desejadas.
1. Clique no ativo para selecioná-lo para uso como banner.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edição de um banner usando o Adobe Dynamic Media Classic {#task_C3E782477FBF428ABEA220751781ACA9}

Use [!DNL Edit Banner] para alterar as propriedades e os parâmetros de um banner que você adicionou usando o Adobe Dynamic Media Classic.

<!-- 

t_editing_a_banner_using_adobe_scene7.xml

 -->

Se você tiver adicionado um banner adicionando código HTML, edite o banner usando pesquisa/merchandising de site.

Consulte também [Edição de um banner](../c-about-design-menu/c-about-banners.md#task_D4081083BE7B40F5A003D1A2F1435AEA).

**Para editar um banner usando o Adobe Dynamic Media Classic**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Na página [!DNL Banners] , clique em ![](assets/icon_edit_16.gif) acima de uma miniatura de banner que tenha um ícone S7 no canto inferior esquerdo da janela do banner.
1. Na página [!DNL Change Parameter], defina as opções desejadas.
1. Quando terminar de editar o banner, clique em **[!UICONTROL Save]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo banners {#task_32F3BADC481E4E8984B2AA04B96052EB}

Você pode excluir os banners preparados que não são mais necessários ou que deseja usar um de cada vez ou como um grupo.

<!-- 

t_deleting_banners.xml

 -->

**Para excluir banners**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Opcional) Siga um ou mais destes procedimentos:

   * Na página [!DNL Banners] , selecione o tipo de banner que deseja localizar na lista suspensa **[!UICONTROL Find banner of type]**. Se desejar, especifique um nome de tag no campo de texto **[!UICONTROL with tag]** ou um nome de tipo de banner no campo de texto **[!UICONTROL with name]**. Clique em **[!UICONTROL Find.]**

   * Na lista suspensa **[!UICONTROL Sort]**, selecione como deseja que a lista de banners seja ordenada.
   * Na lista suspensa **[!UICONTROL Show]**, selecione o número de banners que deseja carregar na página atual que você está visualizando.

1. Faça uma das seguintes opções:

   * No canto superior esquerdo de qualquer caixa de banner, clique na caixa de seleção de cada banner que deseja excluir.
   * Na barra superior da página [!DNL Banners], marque **[!UICONTROL Select all]** para selecionar cada banner carregado na página exibida no momento.

1. Na lista suspensa **[!UICONTROL Bulk Actions]**, clique em **[!UICONTROL Delete]**.
1. Na caixa de diálogo [!DNL Confirmation Action], clique em **[!UICONTROL OK]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualização de banners {#task_6AB1F81A984A4DC2ACACD1FE030545E2}

Você pode navegar pelos banners adicionados à página [!DNL Banners] para visualizar o tamanho completo. Nenhum CSS no modelo que afete o banner é exibido.

<!-- 

t_previewing_banners.xml

 -->

**Para visualizar banners**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Opcional) Siga um ou mais destes procedimentos:

   * Na página [!DNL Banners] , selecione o tipo de banner que deseja localizar na lista suspensa **[!UICONTROL Find banner of type]**. Se desejar, especifique um nome de tag no campo de texto **[!UICONTROL with tag]** ou um nome de tipo de banner no campo de texto **[!UICONTROL with name]**. Clique em **[!UICONTROL Find.]**

   * Na lista suspensa **[!UICONTROL Sort]**, selecione como deseja que a lista de banners seja ordenada.
   * Na lista suspensa **[!UICONTROL Show]**, selecione o número de banners que deseja carregar na página atual que você está visualizando.

1. Na página [!DNL Banners] , clique em uma miniatura do banner para exibir seu tamanho completo.
1. Faça uma das seguintes opções:

   * Na caixa de diálogo Visualização do banner, clique na seta da esquerda ou da direita para navegar e exibir os banners de tamanho inteiro adicionados.
   * Clique no botão Fechar para fechar a caixa de diálogo Visualização do banner e retorne à página [!DNL Banners].

## Movendo banners ao vivo {#task_161F4FEC8362474296A566E64BF05B97}

Você pode enviar um ou mais banners selecionados ao vivo para seu site.

<!-- 

t_pushing_banners_live.xml

 -->

Ou, se preferir, você pode mover ao vivo todas as alterações para qualquer banner, usando a opção **[!UICONTROL Push Live]** próxima à parte inferior da página [!DNL Banners].

Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

**Para enviar banners ao vivo**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Opcional) Siga um ou mais destes procedimentos:

   * Na página [!DNL Banners] , selecione o tipo de banner que deseja localizar na lista suspensa **[!UICONTROL Find banner of type]**. Se desejar, especifique um nome de tag no campo de texto **[!UICONTROL with tag]** ou um nome de tipo de banner no campo de texto **[!UICONTROL with name]**. Clique em **[!UICONTROL Find]**.

   * Na lista suspensa **[!UICONTROL Sort]**, selecione como deseja que a lista de banners seja ordenada.
   * Na lista suspensa **[!UICONTROL Show]**, selecione o número de banners que deseja carregar na página atual que você está visualizando.

1. Faça uma das seguintes opções:

   * No canto superior esquerdo de qualquer caixa de banner, clique na caixa de seleção de cada banner que deseja excluir.
   * Na barra superior da página [!DNL Banner], marque **[!UICONTROL Select all]** para selecionar cada banner carregado na página exibida no momento.

1. Na lista suspensa **[!UICONTROL Bulk Actions]**, clique em **[!UICONTROL Push live]**.
1. Na caixa de diálogo [!DNL Confirmation Action], clique em **[!UICONTROL OK]**.
1. (Opcional) Na página [!DNL Banners] , clique em **[!UICONTROL History]** para reverter as alterações feitas.

   Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).
