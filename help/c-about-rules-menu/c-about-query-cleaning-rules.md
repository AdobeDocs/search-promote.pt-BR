---
description: Use Regras de limpeza de consulta para analisar e modificar a consulta recebida.
solution: Target
title: Sobre as regras de limpeza de query
topic-legacy: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
exl-id: 22ebca58-7687-4c8c-9ac1-bacb321065f3
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1596'
ht-degree: 1%

---

# Sobre as Regras de Limpeza de Consulta{#about-query-cleaning-rules}

Use Regras de limpeza de consulta para analisar e modificar a consulta recebida.

## Usando Regras de Limpeza de Consulta {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

Esse recurso é frequentemente usado quando você deseja modificar o comportamento de pesquisa/comercialização do site. Por exemplo, você pode alterar uma pesquisa em branco para uma palavra-chave popular em vez de uma pesquisa &quot;*&quot;, promovendo assim um produto popular. Também é possível usar as regras de limpeza de consultas para executar uma ocorrência direta, onde você redireciona para um URL. Isso pode ser particularmente útil quando você detectar que alguém está procurando por um SKU de produto e deseja ignorar a pesquisa e redirecionar para a página desse produto. A limpeza de consulta também pode realizar a mina da consulta e definir variáveis personalizadas que podem ser usadas em etapas de fluxo de processamento posterior. As regras de limpeza de query são executadas em sequência para cada query. Para alterar a ordem de suas regras, você pode usar o recurso de arrastar e soltar. A ordem real não é alterada até que você a salve.

As regras de limpeza de consulta em um módulo de limpeza de consulta são examinadas para determinar se qualquer um dos parâmetros de consulta deve ser modificado ou se alguma variável personalizada deve ser definida. Cada regra de limpeza de consulta consiste em dois elementos principais: as ações da regra e as condições opcionais. É possível especificar um número ilimitado de regras e condições. A ordem dessas regras é importante, já que a pesquisa/comercialização do site é loops por regra do conjunto de regras. Quando as condições de uma regra correspondem, todas as ações associadas são executadas.

Depois que a limpeza de query for concluída, os parâmetros CGI resultantes serão usados a partir de agora. Todas as variáveis personalizadas que foram definidas estão disponíveis para uso em estágios posteriores no fluxo de processamento. Por padrão, o sistema remove automaticamente o espaço em branco à esquerda e à direita do termo de consulta.

## Sobre as Condições de Limpeza de Consulta {#section_BF6F25F94FED4DDEA8600D921EA43A66}

As condições são opcionais. Se decidir que as ações são especificadas para cada query, as ações são sempre executadas. As condições podem ser baseadas em qualquer parâmetro de consulta CGI, cookie existente ou variável personalizada que uma regra anterior tenha definido. É considerada a &quot;prática recomendada&quot; para a primeira regra de limpeza de consulta ser executada para cada query, onde ela define e inicializa todas as variáveis personalizadas que você planeja usar.

## Sobre as ações de limpeza de consulta {#section_78F74A9B48DE484191CDA95F5B4E7154}

Todas as ações em uma regra de limpeza de consulta que tem condições correspondentes são exercidas. As ações normalmente consistem em uma operação, os dados nos quais executar a operação e o valor a ser usado.

Consulte a tabela de opções em [Adicionar uma regra de limpeza de consulta](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

## Sobre redirecionamentos {#section_597481E6194440C0A7B9E6FC901A81C0}

A interface Direct-Hits permite definir um conjunto de redirecionamentos com base no termo de query de entrada. Redirecionamentos dentro da Limpeza de consulta estende essa ideia. No entanto, os redirecionamentos oferecem mais granularidade ao determinar quando um redirecionamento ocorre por meio da especificação de condições e permite redirecionar para um URL dinâmico, em vez de estático. Ao selecionar a ação de redirecionamento, a linha é atualizada para ter uma caixa de texto onde você especifica o URL para o qual deseja redirecionar. No URL, você pode especificar variáveis ou parâmetros que deseja substituir por meio da inclusão delas entre colchetes duplos. As variáveis personalizadas têm precedência maior que os parâmetros CGI na substituição.

## Exemplos {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Suponha que você tenha uma loja de varejo de roupas com um site. Se o usuário clicar em Pesquisar sem nenhum termo de pesquisa, você deseja retornar uma pesquisa contra jeans, pois é para isso que você é internacionalmente conhecido. Você também deseja analisar o termo de consulta de um gênero para criar uma regra de pré-pesquisa posteriormente, com base na variável personalizada que usa um modelo de apresentação diferente para cada gênero.

```
On condition: 
  query q equal 
Perform the following actions: 
  Set query parameter q to value jeans 
 
On condition: 
  Query q matches regular expression wom[e|a]n[s]|girl[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value female 
 
On condition: 
  Query q matches regular expression men[s]|boy[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value male
```

A MegaElectronic é uma grande loja de eletrônica. Analisando seus dados de pesquisa, a MegaElectronic tem notado que muitos de seus clientes experientes geralmente procuram um produto usando o SKU do produto, em vez de retornar um resultado de pesquisa para o produto único, a MegaElectronic gostaria de redirecionar para a página da Web associada a esse SKU.

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## Adicionar uma regra de limpeza de consulta {#task_47F43988D3D9485F8AE1DFDA7E00BF54}

Você pode definir regras que limpam ou editam o query de pesquisa de entrada de um cliente.

Você só pode selecionar modelos que existem no momento. Se não tiver templates, primeiro defina-os.

Consulte [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para adicionar uma regra de limpeza de consulta**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na página [!DNL Query Cleaning Rules], clique em **[!UICONTROL Add New Rule]**.
1. No campo [!DNL Name], digite o nome da nova regra de limpeza de consulta.
1. Na página [!DNL Add Query Cleaning Rule] , use as listas suspensas e os campos de texto para criar sua query.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Cookie </p> </td> 
      <td colname="col2"> <p>Um cookie HTTP. Você pode definir condições com base em cookies associados ao seu domínio. Ou você pode definir um cookie gravado com resultados de pesquisa de saída. O nome e os valores dos cookies devem ser codificados com o Identificador de recurso uniforme. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável personalizada </p> </td> 
      <td colname="col2"> <p>Uma variável definida pelo usuário. Adicione, exclua ou defina uma quantidade ilimitada de variáveis definidas pelo usuário. Você pode fazer referência a qualquer variável definida pelo usuário aqui nas Regras de pré-pesquisa e Regras pós-pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável de sistema </p> </td> 
      <td colname="col2"> <p>Variáveis somente leitura definidas pelo sistema interno que você pode verificar. As seguintes variáveis de sistema são compatíveis: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname  </span> <p>O nome do host do servidor. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>O URI solicitado sem a cadeia de caracteres de consulta. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>A string de consulta inteira. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> ambiente </span> <p>"Stage" ou "live" dependendo se a consulta recebida foi enviada para o seu ambiente temporário ou ativo. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>O URL de onde o cliente veio. </p> </li> 
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> agente do usuário  </span> <p>A string "agente-usuário" do navegador do cliente. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de consulta </p> </td> 
      <td colname="col2"> <p>Parâmetros CGI passados para a query. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de backend </p> </td> 
      <td colname="col2"> <p>Os parâmetros de consulta de entrada eventualmente são traduzidos em parâmetros de backend usados para executar a pesquisa. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> <p>Os parâmetros de backend não são exibidos nos elementos de navegação. Como resultado, você pode ocultar quaisquer parâmetros adicionais que deseja aplicar a uma pesquisa dos seus clientes. As ações nos parâmetros de back-end são vinculação tardia; ou seja, elas são aplicadas antes do envio da pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Faceta </p> </td> 
      <td colname="col2"> <p>Parâmetros CGI especiais associados a uma determinada faceta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação </p> </td> 
      <td colname="col2"> <p>Permite que você especifique a regra de classificação a ser usada na pesquisa. Essa opção só aparece quando você tem alguns campos de classificação e regras de classificação definidas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Loja </p> </td> 
      <td colname="col2"> <p>O mecanismo de pesquisa detecta automaticamente em qual armazenamento o usuário está, com base no nome do host ou no parâmetro de consulta <span class="codeph"> gs_store </span>, com a última prioridade. Você pode criar condições fora da loja. Apenas na limpeza de consultas, também é possível usar uma ação para substituir a loja atual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última Regra </p> </td> 
      <td colname="col2"> <p>Quando as condições são atendidas para uma regra que tem o último conjunto de regras, o módulo de processamento de limpeza de consulta não executa regras adicionais após a ação da regra correspondente. Isso é útil quando você definiu ações que farão com que uma regra posterior seja correspondente, mas não deseja que a regra posterior seja acionada. Observe que, se a ação de uma regra for executar um redirecionamento, o redirecionamento ocorrerá imediatamente, de modo que essencialmente atua como se a última regra tivesse sido definida. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suspender </p> </td> 
      <td colname="col2"> <p>Desativa a execução da regra, mas não a exclui. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma regra de limpeza de consulta {#task_FA2FF1A7E2634350AD703485CBC27CB3}

É possível editar as regras de limpeza de consulta existentes que você adicionou à página Regras de limpeza de consulta .

**Para editar uma regra de limpeza de consulta**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na página [!DNL Query Cleaning Rules] , na coluna **[!UICONTROL Actions]** da tabela, clique em **[!UICONTROL Edit]** para a regra associada que deseja editar.
1. Na página [!DNL Edit Query Cleaning Rule] , use as listas suspensas e os campos de texto para criar sua query.

   Consulte a tabela de opções em [Adicionar uma regra de limpeza de consulta](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma regra de limpeza de consulta {#task_C52D17226B824590B087CAB6970CBB01}

Você pode excluir as regras de limpeza de consulta que não são mais necessárias ou usadas.

Quando você exclui uma regra, a ordem em que as regras restantes são executadas é ajustada automaticamente para contabilizar a exclusão.

**Para excluir uma regra de limpeza de consulta**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na página [!DNL Query Cleaning Rules] , na coluna **[!UICONTROL Actions]** da tabela, clique em **[!UICONTROL Delete]** para a regra associada que deseja excluir.
1. Na caixa de diálogo [!DNL Confirmation], clique em **[!UICONTROL OK]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Alteração da ordem em que as regras de limpeza de consulta são executadas {#task_C24012C45A4445468A7FD998017388CA}

Você pode reordenar as regras de limpeza de consulta para alterar a ordem em que são executadas nos modelos de apresentação.

As regras de limpeza de query são executadas na ordem em que foram definidas. Quanto maior for o número do pedido de uma regra, mais tarde ela será executada no processo, superando as regras anteriores. Você reorganiza as regras inserindo um novo número na coluna Ordem da tabela na página [!DNL Query Cleaning Rules]. Também é possível usar as regras de arrastar e soltar para alterar a ordem de execução.

**Para alterar a ordem de execução das regras de limpeza de consulta**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na página [!DNL Query Cleaning Rules], execute um dos seguintes procedimentos:

   * Clique no cabeçalho da coluna [!DNL Order] para classificar as regras em ordem crescente ou decrescente.
   * Na coluna [!DNL Order], no campo de texto à esquerda do nome de uma regra de limpeza de consulta, digite o número do pedido que deseja que a regra seja executada.
   * Arraste e solte uma linha de tabela na posição em que deseja que a regra seja executada. Todos os números de pedido são atualizados para refletir a nova ordem em que as regras são executadas.

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
