---
description: Use Regras de limpeza de consulta para analisar e modificar a consulta recebida.
seo-description: Use Regras de limpeza de consulta para analisar e modificar a consulta recebida.
seo-title: Sobre Regras de Limpeza de Consulta
solution: Target
title: Sobre Regras de Limpeza de Consulta
topic: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# Sobre Regras de Limpeza de Consulta{#about-query-cleaning-rules}

Use Regras de limpeza de consulta para analisar e modificar a consulta recebida.

## Usando Regras de Limpeza de Consulta {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

Esse recurso é usado com frequência quando você deseja modificar o comportamento de pesquisa/comercialização do site. Por exemplo, você pode alterar uma pesquisa em branco para uma palavra-chave popular em vez de uma pesquisa &quot;*&quot;, promovendo assim um produto popular. Você também pode usar regras de limpeza de consulta para executar uma ocorrência direta, onde você redireciona para um URL. Isso pode ser particularmente útil quando você detecta que alguém está procurando por um SKU de produto e deseja ignorar a pesquisa e redirecionar para a página do produto. A Limpeza de consulta também pode realizar mineração na consulta e definir variáveis personalizadas que podem ser usadas em etapas posteriores do fluxo de processamento. As regras de limpeza de consulta são executadas em sequência para cada consulta. Para alterar a ordem de suas regras, é possível usar o recurso arrastar e soltar. A ordem real não é alterada até que você a salve.

As regras de limpeza de consulta em um módulo de limpeza de consulta são examinadas para determinar se qualquer um dos parâmetros de consulta deve ser modificado ou se qualquer variável personalizada deve ser definida. Cada regra de limpeza de consulta consiste em dois elementos principais: as ações da regra e as condições opcionais. É possível especificar um número ilimitado de regras e condições. A ordem dessas regras é importante, à medida que a pesquisa/comercialização do site é repetida pela regra de conjunto de regras por regra. Quando as condições de uma regra correspondem, todas as ações associadas são executadas.

Depois que a limpeza de consulta é concluída, os parâmetros CGI resultantes são usados para frente. Todas as variáveis personalizadas que foram definidas estão disponíveis para uso por etapas posteriores no fluxo de processamento. Por padrão, o sistema remove automaticamente o espaço em branco à esquerda e à direita do termo de consulta.

## Sobre as condições de limpeza de consulta {#section_BF6F25F94FED4DDEA8600D921EA43A66}

As condições são opcionais. Se você decidir que as ações são especificadas para cada consulta, as ações são sempre executadas. As condições podem ser baseadas em qualquer parâmetro de consulta CGI, cookie existente ou variável personalizada que uma regra anterior tenha definido. É considerada a &quot;prática recomendada&quot; para a primeira regra de limpeza de consulta ser executada para cada consulta, na qual ela define e inicializa todas as variáveis personalizadas que você planeja usar.

## Sobre ações de limpeza de consulta {#section_78F74A9B48DE484191CDA95F5B4E7154}

Todas as ações dentro de uma regra de limpeza de consulta que tem condições correspondentes são exercidas. As ações normalmente consistem em uma operação, os dados nos quais realizar a operação e o valor a ser usado.

Consulte a tabela de opções em [Adicionar uma regra](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)de limpeza de consulta.

## Sobre redirecionamentos {#section_597481E6194440C0A7B9E6FC901A81C0}

A interface de Ocorrências diretas permite definir um conjunto de redirecionamentos com base no termo de consulta recebido. Redirecionamentos dentro da Limpeza de consulta ampliam essa ideia. No entanto, os redirecionamentos fornecem uma granularidade mais fina sobre quando um redirecionamento ocorre por meio de condições específicas e permite redirecionar para um URL dinâmico em vez de um URL estático. Quando você seleciona a ação de redirecionamento, a linha é atualizada para ter uma caixa de texto na qual você especifica o URL para o qual deseja redirecionar. No URL, é possível especificar variáveis ou parâmetros que você gostaria de substituir ao incluí-los entre chaves duplas. As variáveis personalizadas têm precedência maior que os parâmetros CGI na substituição.

## Exemplos {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Suponha que você tenha uma loja de roupas com um site. Se o usuário clicar em Pesquisar sem nenhum termo de pesquisa, você deseja retornar uma pesquisa contra jeans, pois é para isso que você é conhecido internacionalmente. Você também deseja analisar o termo de consulta para um gênero, para que possa criar uma regra de pré-pesquisa posteriormente, com base na variável personalizada que usa um modelo de apresentação diferente para cada gênero.

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

A MegaElectronic é uma grande loja de eletrônicos. Ao analisar seus dados de pesquisa, a MegaElectronic percebeu que muitos clientes experientes geralmente procuram um produto usando o SKU do produto, em vez de retornar um resultado de pesquisa para o único produto, a MegaElectronic gostaria de redirecionar para a página da Web associada ao SKU.

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## Adicionando uma regra de limpeza de consulta {#task_47F43988D3D9485F8AE1DFDA7E00BF54}

Você pode definir regras que limpam ou editam a consulta de pesquisa recebida de um cliente.

Você só pode selecionar modelos que existem atualmente. Se você não tiver modelos, primeiro defina-os.

Consulte [Sobre Modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para adicionar uma regra de limpeza de consulta**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na [!DNL Query Cleaning Rules] página, clique em **[!UICONTROL Add New Rule]**.
1. No [!DNL Name] campo, digite o nome da nova regra de limpeza de consulta.
1. Na [!DNL Add Query Cleaning Rule] página, use as listas suspensas e os campos de texto para desenvolver sua consulta.

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
      <td colname="col2"> <p>Um cookie HTTP. Você pode definir condições com base em cookies associados ao seu domínio. Ou você pode definir um cookie que é escrito com resultados de pesquisa enviados. O nome e os valores dos cookies devem estar codificados no Identificador de recurso uniforme. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável personalizada </p> </td> 
      <td colname="col2"> <p>Uma variável definida pelo usuário. Adicione, exclua ou defina uma quantidade ilimitada de variáveis definidas pelo usuário. Você pode fazer referência a quaisquer variáveis definidas pelo usuário em Regras de pré-pesquisa e Regras de pós-pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável do sistema </p> </td> 
      <td colname="col2"> <p>Variáveis somente leitura definidas pelo sistema interno que você pode verificar. As seguintes variáveis do sistema são suportadas: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> nome do host </span> <p>O nome do host do servidor. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>O URI solicitado sem a string de consulta. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args </span> <p>A string de consulta inteira. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> ambiente </span> <p>"Stage" ou "live", dependendo se a consulta recebida foi enviada para o seu ambiente ativo ou temporário. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>O URL de onde o cliente veio. </p> </li> 
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> agente do usuário </span> <p>A string "user-agent" do navegador do cliente. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de consulta </p> </td> 
      <td colname="col2"> <p>Parâmetros CGI passados para a consulta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de backend </p> </td> 
      <td colname="col2"> <p>Os parâmetros de consulta de entrada eventualmente são convertidos em parâmetros de backend usados para executar a pesquisa. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> <p>Os parâmetros de backend não são exibidos nos elementos de navegação. Como resultado, você pode ocultar quaisquer parâmetros adicionais que você deseja aplicar a uma pesquisa de seus clientes. As ações nos parâmetros de backend são vinculação tardia; ou seja, eles são aplicados logo antes da pesquisa ser enviada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aspecto </p> </td> 
      <td colname="col2"> <p>Parâmetros CGI especiais associados a uma determinada faceta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação </p> </td> 
      <td colname="col2"> <p>Permite que você especifique qual regra de classificação usar na pesquisa. Essa opção só aparece quando você tem alguns campos de classificação e regras de classificação definidos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Loja </p> </td> 
      <td colname="col2"> <p>O mecanismo de pesquisa detecta automaticamente em qual armazenamento o usuário está com base no nome do host ou no parâmetro de <span class="codeph"> consulta </span> gs_store, com a última prioridade. Você pode criar condições fora da loja. Somente na limpeza de consulta, você também pode usar uma ação para substituir a loja atual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última regra </p> </td> 
      <td colname="col2"> <p>Quando as condições são atendidas para uma regra que tem o último conjunto de regras, o módulo de processamento de limpeza de consulta não executa quaisquer regras adicionais após a ação da regra correspondente. Isso é útil quando você define ações que farão com que uma regra posterior seja correspondente, mas você não deseja que a regra posterior seja acionada. Observe que, se a ação de uma regra for executar um redirecionamento, o redirecionamento ocorrerá imediatamente, de modo que ele atua essencialmente como se a última regra tivesse sido definida. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suspender </p> </td> 
      <td colname="col2"> <p>Desativa a execução da regra, mas não a exclui. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma regra de limpeza de consulta {#task_FA2FF1A7E2634350AD703485CBC27CB3}

É possível editar as regras de limpeza de consulta existentes que você adicionou à página Regras de limpeza de consulta.

**Para editar uma regra de limpeza de consulta**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na [!DNL Query Cleaning Rules] página, na **[!UICONTROL Actions]** coluna da tabela, clique **[!UICONTROL Edit]** para a regra associada que você deseja editar.
1. Na [!DNL Edit Query Cleaning Rule] página, use as listas suspensas e os campos de texto para desenvolver sua consulta.

   Consulte a tabela de opções em [Adicionar uma regra](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)de limpeza de consulta.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma regra de limpeza de consulta {#task_C52D17226B824590B087CAB6970CBB01}

É possível excluir regras de limpeza de consulta que não são mais necessárias ou não são usadas.

Quando você exclui uma regra, a ordem em que as regras restantes são executadas é ajustada automaticamente para contabilizar a exclusão.

**Para excluir uma regra de limpeza de consulta**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na [!DNL Query Cleaning Rules] página, na **[!UICONTROL Actions]** coluna da tabela, clique **[!UICONTROL Delete]** para a regra associada que deseja excluir.
1. Na caixa de [!DNL Confirmation] diálogo, clique em **[!UICONTROL OK]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Alteração da ordem em que as regras de limpeza de consulta são executadas {#task_C24012C45A4445468A7FD998017388CA}

É possível reordenar as regras de limpeza de consulta para alterar a ordem em que são executadas nos modelos de apresentação.

As regras de limpeza de consulta são executadas na ordem em que foram definidas. Quanto maior for o número do pedido de uma regra, mais tarde ela será executada no processo, superando as regras anteriores. Você reorganiza as regras digitando um novo número na coluna Ordem da tabela na [!DNL Query Cleaning Rules] página. Também é possível usar as regras de arrastar e soltar para alterar a ordem de execução.

**Para alterar a ordem em que as regras de limpeza de consulta são executadas**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Na [!DNL Query Cleaning Rules] página, execute um dos procedimentos a seguir:

   * Clique no cabeçalho da [!DNL Order] coluna para classificar as regras em ordem crescente ou decrescente.
   * Na [!DNL Order] coluna, no campo de texto à esquerda de um nome de regra de limpeza de consulta, digite o número do pedido que deseja que a regra execute.
   * Arraste e solte uma linha de tabela na posição em que deseja que a regra seja executada. Todos os números de pedido são atualizados para refletir a nova ordem em que as regras são executadas.

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

