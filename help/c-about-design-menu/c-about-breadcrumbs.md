---
description: Trilhas são um controle de navegação que você pode adicionar ao seu site. A trilha de navegação fornece aos clientes feedback sobre onde eles estão em um conjunto de resultados de pesquisa. Isso também os ajuda a retornar rapidamente a uma etapa anterior.
seo-description: Trilhas são um controle de navegação que você pode adicionar ao seu site. A trilha de navegação fornece aos clientes feedback sobre onde eles estão em um conjunto de resultados de pesquisa. Isso também os ajuda a retornar rapidamente a uma etapa anterior.
seo-title: Sobre a navegação estrutural
solution: Target
subtopic: Navigation
title: Sobre a navegação estrutural
topic: Design,Site search and merchandising
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
translation-type: tm+mt
source-git-commit: 7f1b5d94e8002992d62ec1e3dce11f9c5605fde8

---


# Sobre a navegação estrutural{#about-breadcrumbs}

Trilhas são um controle de navegação que você pode adicionar ao seu site. A trilha de navegação fornece aos clientes feedback sobre onde eles estão em um conjunto de resultados de pesquisa. Isso também os ajuda a retornar rapidamente a uma etapa anterior.

## Uso da navegação estrutural {#concept_FB8A943C594A4A1593B118141DA61F03}

As navegações estruturais rastreiam o termo pesquisado e as facetas subsequentes que foram selecionadas para restringir o conjunto de resultados.

Use as configurações de navegação estrutural para personalizar o controle de navegação estrutural da sua camada de apresentação de pesquisa. Se a sua camada de apresentação tiver mais de um conjunto de resultados de pesquisa, o controle de navegação estrutural atuará na pesquisa principal na página.

É possível editar uma navegação estrutural para alterar o comportamento padrão, a largura máxima do valor e a extensão do valor, e selecionar se o termo de consulta deve ser incluído.

## Adding a new breadcrumb {#task_2FFA94F82AE74F10BDDE7367CDCEAE8B}

É possível adicionar uma barra de navegação estrutural para que o cliente possa rastrear onde está em seu site.

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>Certifique-se de fazer referência à navegação estrutural no modelo de apresentação para que ela fique visível no site.

**Para adicionar uma nova navegação estrutural**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Na [!DNL Breadcrumbs] página, clique em **[!UICONTROL Add Breadcrumb]**.
1. Na [!DNL Add Breadcrumb] página, defina as opções desejadas.

   Essas configurações afetam o comportamento e a apresentação padrão de uma navegação estrutural. É possível substituir algumas dessas configurações por meio das configurações do modelo de apresentação.

   <!-- 
   
   r_breadcrumb_options.xml
    
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
      <td colname="col1"> <p>Nome da navegação estrutural </p> </td> 
      <td colname="col2"> <p>O nome da trilha de navegação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comportamento </p> </td> 
      <td colname="col2"> <p>Define um dos três comportamentos de navegação estrutural a seguir: </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Ir para </span> <p>Ir para remove todas as navegações estruturais após aquela clicada e inicia uma nova pesquisa nesse ponto. </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Remover </span> <p>Remova as exclusões do caminho da navegação estrutural em que o cliente clicou e, em seguida, inicie uma nova pesquisa. Esse comportamento é útil quando você deseja permitir que o cliente desfaça as etapas da busca. </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Soltar </span> <p>Soltar remove todas as navegações estruturais. </p> </li> 
      </ul> </p> <p> Por exemplo, suponha que você tenha uma trilha de navegação de 1 &gt; 2 &gt; 3 &gt; 4. Quando um cliente clica em "2", ele tem os seguintes resultados, com base no comportamento escolhido: </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">Ir para - 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">Remover - 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> Drop - Toda a trilha de navegação é solta, levando o cliente de volta ao ponto antes de ele começar a fazer drill-down. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Largura máxima do valor </p> </td> 
      <td colname="col2"> <p>Especifica o comprimento de cada valor na trilha de navegação estrutural. Especifique a configuração como um número de caracteres. </p> <p>Por exemplo, uma configuração de 6 significa que a trilha de navegação pode ter até 6 caracteres, incluindo espaços. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Extensão de valor </p> </td> 
      <td colname="col2"> <p>Especifica as elipses a serem usadas quando uma navegação estrutural estiver truncada. </p> <p>Por padrão, um "..." (elipses). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir termo de consulta </p> </td> 
      <td colname="col2"> <p>Controla a presença do termo de consulta em uma trilha de navegação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativar migalhas definidas pelo usuário </p> </td> 
      <td colname="col2"> <p>Marque para permitir que você use os itens Definidos pelo usuário na navegação estrutural usando os parâmetros <span class="codeph"> uX=[name]&amp;[name]=[value] </span> no URL. Você pode usar as regras de processamento para manipular esses parâmetros da maneira que desejar. </p> <p>Por exemplo, se esse recurso estiver ativado e você tiver o URL, <code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code> caso você tenha facetas <span class="codeph"> de categoria <span class="varname"> </span> e </span> tipo <span class="codeph"> , sua trilha de navegação parecerá <span class="varname"> </span> </span><span class="codeph"> </span>Roupas &gt; Masculino &gt; Sweater . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nomes De Crumb Definidos Pelo Usuário </p> </td> 
      <td colname="col2"> <p>Uma lista separada por vírgulas de todos os nomes possíveis de itens de navegação estrutural definidos pelo usuário. </p> <p>Essa opção só estará disponível se você marcar <span class="uicontrol"> Ativar migalhas definidas pelo usuário </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Na [!DNL Breadcrumbs] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edição de uma navegação estrutural {#task_583481D9A23E4E0F97AEB18E72CBE13F}

É possível editar as configurações de qualquer trilha de navegação adicionada.

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>Certifique-se de fazer referência à navegação estrutural no modelo de apresentação para que ela fique visível no site.

**Para editar uma navegação estrutural**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Na [!DNL Breadcrumbs] página, clique **[!UICONTROL Edit]** na extremidade direita do nome da trilha de navegação.
1. Na [!DNL Edit Breadcrumb] página, defina as opções desejadas.

   Consulte a tabela de opções em [Adicionar uma nova navegação estrutural](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Na **[!UICONTROL Breadcrumb]** página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma navegação estrutural {#task_401C6E481A744284906E15A29E04F757}

É possível excluir qualquer navegação estrutural adicionada.

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**Para excluir uma navegação estrutural**

1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Na [!DNL Breadcrumbs] página, clique **[!UICONTROL Delete]** na extremidade direita do nome da trilha de navegação.
1. Na caixa de [!DNL Confirmation] diálogo, clique em **[!UICONTROL OK]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

