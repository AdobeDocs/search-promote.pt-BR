---
description: Você pode usar menus para personalizar a camada da apresentação.
seo-description: Você pode usar menus para personalizar a camada da apresentação.
seo-title: Sobre menus
solution: Target
subtopic: Navigation
title: Sobre menus
topic: Design,Site search and merchandising
uuid: 011050cd-21b6-4150-9503-18fa3f771626
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 1%

---


# Sobre menus{#about-menus}

Você pode usar menus para personalizar a camada da apresentação.

## Usando menus {#concept_68123CE5CF4447B59217B5D721424E32}

Adicione menus que mapeiam para configurações na sua pesquisa. Cada item dentro de um menu especifica o valor para a configuração do menu. Você também pode personalizar os rótulos dos menus.

No modelo de apresentação, é possível fazer referência aos menus definidos. Você pode colocá-los em qualquer componente HTML que desejar, como um controle de seleção. Essa combinação permite que os usuários personalizem seus resultados de pesquisa. Há suporte para três tipos de menu: classificar, contar e navegação.

## Adicionar um novo menu {#task_EE171532D3AE477FAFE8C2F4077A6D73}

Você pode adicionar menus que mapeiam para configurações nos resultados da pesquisa.

<!-- 

t_adding_a_new_menu.xml

 -->

>[!NOTE]
>
>Certifique-se de consultar o menu no modelo de apresentação para que fique visível no site.

**Para adicionar um novo menu**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. Na página [!DNL Menus], clique em **[!UICONTROL Add New Menu]**.
1. Na página [!DNL Add Menu], defina as opções desejadas.

   Essas configurações afetam o comportamento e a apresentação padrão de uma navegação estrutural. É possível substituir algumas dessas configurações por meio das configurações do modelo de apresentação.

   Consulte [Sobre menus](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

   <!-- 
   r_add_menu_options.xml
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
      <td colname="col1"> <p>Nome do menu </p> </td> 
      <td colname="col2"> <p>Nome do menu. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo de menu </p> </td> 
      <td colname="col2"> <p>Define um dos três tipos de menu a seguir: </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
      <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Classificar  </span> <p>Organiza sua pesquisa por qualquer um dos tipos de metadados definidos. </p> <p>Por exemplo, você pode definir um menu de classificação com os seguintes tipos de metadados: três pontos relevantes; um campo de metadados personalizado, como um código de disponibilidade; e preço. Os três itens podem receber os rótulos "Classificar por relevância", "Classificar por disponibilidade" e "Classificar por preço", respectivamente. Quando você incluir isso no modelo de apresentação, o cliente poderá usar esse controle para classificar os resultados da pesquisa. </p> </li> 
      <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Contagem </span> <p>Define o número de resultados da pesquisa a serem exibidos. Esse tipo de menu mapeia para o parâmetro cgi <span class="varname"> sp_c </span>. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> </li> 
      <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Navegação </span> <p>Especifica um conjunto de URLs estáticos associados aos itens de menu. Normalmente, um menu de navegação é usado para criar uma barra de navegação de nível superior na página de resultados da pesquisa. </p> <p>Por exemplo, você pode criar um menu que tenha mulheres, homens, meninos e meninas em que os itens de menu seriam algo como: 
      <code>
        /?q1=womens;x1=gender 
      </code>, 
      <code>
        /?q1=mens;x1=gender 
      </code> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comercialização </p> 
        <!--DONT' KNOW WHAT THIS DOES--> </td> 
      <td colname="col2"> <p>Essa opção só estará disponível se você escolher o tipo de menu <span class="uicontrol"> Classificar. </span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de itens no menu </p> </td> 
      <td colname="col2"> <p>Especifica o número de itens em um menu. Alterar essa configuração adiciona ou exclui campos do formulário. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Item padrão </p> </td> 
      <td colname="col2"> <p>Permite selecionar qual item de menu é exibido por padrão. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor do item </p> </td> 
      <td colname="col2"> <p>O valor do item depende do tipo de menu definido. </p> 
        <ul id="ul_2F14E6AA673640578A2D5161FD9D13EF"> 
        <li id="li_5017EC6E4ACB4B8E99E0AA61CBAAFFAE"> Tipo de menu Classificar <p>Identifica pelo que o item selecionado no menu deve ser classificado. Os itens selecionados são preenchidos com campos de metadados classificáveis. </p> <p>Para um único item, é possível classificar por três campos de metadados. A classificação é feita na ordem especificada. </p> </li> 
        <li id="li_CC6BAFBF969C4367A71B55F08E0758D1"> Tipo de menu Contagem <p>Permite que você especifique o número de resultados que deseja retornar quando o cliente selecionar esse item de menu. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rótulo do item </p> </td> 
      <td colname="col2"> <p>O rótulo do item depende do tipo de menu definido. </p> 
        <ul id="ul_957BF01235F84748B5EB7062D6AEAC41"> 
        <li id="li_03FB2E2C96134A2B8E08154F87F0CD55"> Tipo de menu Classificar <p>Identifica o rótulo personalizado que você deseja que seu cliente veja quando ele visualização este item no menu. </p> </li> 
        <li id="li_C9FE2BC46D9443FB85FEB837C7CA45E1"> Tipo de menu Contagem <p>Identifica o rótulo personalizado que você deseja que seja exibido para este item de menu. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Na página [!DNL Menus], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar um menu {#task_0770DBFD0C7046169097FB6F771B9114}

É possível editar as configurações de qualquer menu que você tenha adicionado.

<!-- 

t_editing_a_menu.xml

 -->

>[!NOTE]
>
>Certifique-se de consultar o menu no modelo de apresentação para que fique visível no site.

**Para editar um menu**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. Na página [!DNL Menus], clique em **[!UICONTROL Edit]** à direita do nome de um menu.
1. Na página [!DNL Edit Menu], defina as opções desejadas.

   Consulte a tabela de opções em [Adicionar um novo menu](../c-about-design-menu/c-about-menus.md#task_EE171532D3AE477FAFE8C2F4077A6D73).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Na página [!DNL Menus], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo um menu {#task_645E212311A045CD8D9D906878165F47}

Você pode excluir qualquer menu que tenha adicionado.

<!-- 

t_deleting_a_menu.xml

 -->

**Para excluir um menu**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**
1. Na página [!DNL Menus], clique em **[!UICONTROL Delete]** à direita do nome de um menu.
1. Na caixa de diálogo [!DNL Confirmation], clique em **[!UICONTROL OK]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

