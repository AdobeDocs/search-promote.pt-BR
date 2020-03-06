---
description: Você pode usar Regras de pós-pesquisa para examinar os resultados de uma pesquisa e determinar como ela afeta o conteúdo exibido.
seo-description: Você pode usar Regras de pós-pesquisa para examinar os resultados de uma pesquisa e determinar como ela afeta o conteúdo exibido.
seo-title: Sobre as regras de pós-pesquisa
solution: Target
title: Sobre as regras de pós-pesquisa
topic: Rules,Site search and merchandising
uuid: 312d1e4a-f5b6-4629-8645-17e6f6c09fc4
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# Sobre as regras de pós-pesquisa{#about-post-search-rules}

Você pode usar Regras de pós-pesquisa para examinar os resultados de uma pesquisa e determinar como ela afeta o conteúdo exibido.

## Uso de regras de pós-pesquisa {#concept_AF6ADFCC0ADF4A788003964939917FDE}

Se uma pesquisa não tiver resultados, uma Regra de pós-pesquisa poderá executar uma pesquisa por um item semelhante. Ou pode exibir uma página da Web que recomenda outros itens aos clientes que pesquisam o item que não foi encontrado.

Cada Regra de pós-pesquisa consiste em dois elementos principais: as ações da regra e suas condições opcionais. Você pode especificar um número ilimitado de regras e condições. A ordem dessas regras é importante porque o conjunto de regras é repetido por regra. Quando as condições de uma regra correspondem, todas as ações associadas são executadas.

Você pode refinar o conjunto de resultados da pesquisa para um máximo de três rodadas de pesquisa. Depois disso, o que estiver disponível será usado. Esse limite impede loops infinitos e garante que o cliente receba uma resposta eficiente. Quanto mais vezes você refizer uma pesquisa, mais tempo levará para retornar os resultados da pesquisa. Se nenhuma das regras correspondentes alterar uma das buscas pelo modelo de apresentação usado no momento ou alternar o modelo, o conjunto de resultados da pesquisa será considerado finalizado e sairá da pesquisa.

O processamento pós-pesquisa baseia-se nos módulos de processamento anteriores Limpeza de consulta e processamento Pré-pesquisa. Portanto, quaisquer variáveis personalizadas definidas nesses módulos estão disponíveis para uso nas regras de processamento pós-pesquisa. Da mesma forma, o processamento pré-pesquisa instanciou todos os modelos nos quais cada pesquisa nomeada associada ao modelo de apresentação tem sua própria cópia local dos parâmetros CGI. Por sua vez, você pode personalizar cada pesquisa individualmente.

Consulte [Sobre regras](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C)de limpeza de consulta.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

## Sobre as condições da regra de pós-pesquisa {#section_C43EB77CC0AC43B8B9D38569264BF1B5}

As condições são opcionais. Se você especificar que as ações são especificadas para cada consulta, então as ações são sempre executadas. É possível basear as condições em qualquer parâmetro de consulta CGI, cookie, resultado de pesquisa ou variável personalizada que uma regra anterior tenha definido. Ou você pode baseá-lo em uma condição do sistema, como o modelo selecionado no momento ou se for a última pesquisa. Ao criar uma condição nos resultados de uma pesquisa ou de um parâmetro CGI, você especifica o modelo e o nome da pesquisa.

## Sobre as ações da Regra de pós-pesquisa {#section_0E15FE683A894ECAAA386267EEC7F7C5}

Todas as ações em uma Regra de pós-pesquisa que têm condições correspondentes são exercidas. Normalmente, as ações consistem em uma operação, nos dados para executar a operação e no valor a ser usado. A ação mais simples é alternar qual modelo de Apresentação usar com base nas condições da Regra de pós-pesquisa. Você pode usar ações mais avançadas para alterar os parâmetros de uma pesquisa que resulta na pesquisa sendo refeita. Ao executar uma operação no parâmetro de pesquisa de um modelo, especifique um modelo de Apresentação e uma pesquisa.

## Regras gerais {#section_AEE923988CC748FF9DEF2233FBF333B5}

Ao executar operações no parâmetro de pesquisa de um modelo, existem dois valores especiais, *direcionados e *primários para o modelo de Apresentação e a pesquisa nomeada respectivamente. Use esses valores para criar regras baseadas na pesquisa principal do modelo direcionado atual. Essas construções permitem criar regras genéricas onde você não precisa se preocupar com o que o modelo direcionado atual ou a pesquisa primária são chamados. Se essa passagem for a primeira através do processamento pós-pesquisa, o modelo direcionado será qualquer processamento pré-pesquisa definido.

## Redirecionamentos {#section_E5669A2F13C240F2968E31C75591CD6A}

Ocorrências diretas e redirecionamentos na Limpeza de consulta permitem redirecionar para um URL com base nos termos de pesquisa recebidos. Os redirecionamentos dentro das regras de pós-pesquisa estendem essa ideia, exceto que permitem que você verifique quantos resultados a pesquisa retornou antes de decidir se deseja que um redirecionamento ocorra. Com Regras de pós-pesquisa, você pode redirecionar para um URL, onde pode substituir variáveis personalizadas ou parâmetros de consulta. Ou você pode redirecionar para um campo dentro do primeiro resultado. Quando você redireciona para o campo de um resultado, define o campo no modelo de Transporte e ele deve conter um URL válido e explícito; caso contrário, o redirecionamento é ignorado.

Quando você usa o mecanismo de redirecionamento nas Regras de pós-pesquisa, é possível detectar quando uma pesquisa retorna um único resultado. Em vez de retornar tal resultado, você pode redirecionar para a página da Web associada ao resultado.

Consulte o exemplo de redirecionamento abaixo para obter um exemplo de uso de redirecionamentos com Regras de pós-pesquisa.

## Última regra {#section_FC1E0050C9324278B171038E98F6C335}

Quando as condições são atendidas para uma regra que tem a opção **[!UICONTROL Last Rule]** definida, o módulo de processamento de pesquisa posterior não executa quaisquer regras adicionais após a ação da regra correspondente. Essa situação é útil quando você define ações que fazem com que uma regra posterior corresponda, mas deseja que o processamento pare. E, para que essa regra mais tarde corresponda potencialmente depois da próxima rodada de pesquisa.

## Exemplos {#section_DDB98383690941F9B44AD00FBA55BB56}

No exemplo a seguir, suponha que você tenha dois modelos de apresentação. Um modelo é usado para exibir muitos resultados de pesquisa e o outro modelo é usado para exibir um único resultado e uma pesquisa adicional por acessórios relacionados à pesquisa principal. Você deseja detectar quando tiver um único resultado e alternar para o outro modelo de apresentação. Para realizar essa tarefa, você pode usar as seguintes regras:

```
On condition: 
  targeted template is default 
  targeted template primary results equal 1 
  not last search 
Perform the following actions: 
  Set targeted template to product_spotlight
```

A MegaElectronic é uma grande loja de eletrônicos. Após analisar os dados de pesquisa, a MegaElectronic nota que muitos de seus clientes fazem uma pesquisa de produto usando o número de peça de um produto. Nesses casos, a MegaElectronic deseja redirecionar para a página da Web que está associada ao produto, se o cliente pesquisou diretamente e somente um único produto foi encontrado.

Para obter esse resultado, é possível usar uma única regra com três condições. A primeira condição verifica se a pesquisa retornada tem apenas um único resultado. A segunda condição garante que o termo de consulta corresponda ao formato de número de peça da MegaElectronic aos resultados que eles desejam causar o redirecionamento. A terceira condição garante que o cliente não tenha usado quaisquer aspectos para detalhar para um resultado, visto que o número da peça pode ser um número de peça parcial e retornar mais de um resultado. A ação redireciona para um campo dentro do resultado.

```
On condition: 
  targeted template's primary results equal 1 
  query q matches regular expression ^\D\D\D-\d+ 
  no facet selected ^\D\D\D-\d+ 
Perform the following actions: 
  redirect to result field "loc" in template *targeted for search *primary
```

## Práticas recomendadas {#section_1BF7DE1BD5664B3BAEC26AA829FDB0BA}

* Qualquer conjunto de regras que aciona uma nova rodada de pesquisa deve sempre ter uma cláusula condicional para verificar se essa não é a última passagem pelo módulo. Se você já tiver realizado o número máximo de pesquisas, não será possível refazer nenhuma pesquisa.
* Se você estiver na última passagem pelo módulo e os resultados ainda estiverem insatisfeitos, poderá alternar para um modelo &quot;sem resultados&quot;.
* Você deve basear a alteração de um modelo de apresentação no resultado de uma pesquisa que potencialmente tenha outros parâmetros. Se você quiser selecionar um modelo que seja baseado apenas na consulta recebida, uma regra de pré-pesquisa será mais eficiente.
* A extração de dados da consulta é feita no módulo Limpeza de consulta. É possível referenciar as variáveis personalizadas no processamento pós-pesquisa.
* Quando você redireciona, sempre verifique se o cliente não selecionou nenhum aspecto. O motivo é porque é inconveniente quando um cliente detalha uma faceta e é subitamente tirado dos resultados da pesquisa. O cliente pode querer desmarcar a faceta quando perceber que o único resultado não é que ele estava procurando.

## Adicionar uma nova regra pós-pesquisa {#task_52F6F9AAD65B45B5ACA1FF245DFFADD9}

Você pode usar [!DNL Post-Search Rules] para selecionar qual modelo de apresentação é usado para exibir os resultados da pesquisa com base na consulta recebida.

**Para adicionar uma nova regra pós-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Na [!DNL Post-Search Rules] página, clique em **[!UICONTROL Add New Rule]**.
1. No [!DNL Name] campo, digite o nome da nova regra de limpeza de consulta.
1. Na [!DNL Add Post-Search Rule] página, use as listas suspensas e os campos de texto para desenvolver sua consulta.

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
      <td colname="col2"> <p>Um cookie HTTP. Nomes e valores de cookies devem ser codificados como Identificador de recurso uniforme. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável personalizada </p> </td> 
      <td colname="col2"> <p>Uma variável definida pelo usuário. Você pode adicionar, excluir ou definir um número ilimitado de variáveis personalizadas. </p> <p>É possível fazer referência a quaisquer variáveis personalizadas que você definiu nos módulos Limpeza de consulta e Regras de pré-pesquisa, nas Regras de pós-pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável do sistema </p> </td> 
      <td colname="col2"> <p>Variáveis somente leitura definidas pelo sistema interno que você pode verificar. As seguintes variáveis do sistema são suportadas: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> nome do host </span> <p>O nome do host do servidor. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>O Identificador de Recurso Uniforme solicitado sem a string de consulta. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args </span> <p>A string de consulta inteira. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> ambiente </span> <p>"Stage" ou "live", dependendo se a consulta recebida foi enviada para o ambiente preparado ou para o ambiente ativo. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>O Uniform Resource Locator de onde o cliente veio. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável do sistema </p> </td> 
      <td colname="col2"> <p>Variáveis somente leitura que podem ser usadas em condições para determinar o estado atual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aspecto de pesquisa do modelo </p> </td> 
      <td colname="col2"> <p>Uma faceta local para uma pesquisa nomeada associada a um modelo de apresentação. Uma faceta é essencialmente parâmetros CGI especiais usados para indicar qual valor em uma faceta um cliente selecionou. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de pesquisa do modelo </p> </td> 
      <td colname="col2"> <p>Um parâmetro CGI que é local para uma pesquisa nomeada associada a um modelo de apresentação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de backend do modelo </p> </td> 
      <td colname="col2"> <p>Os parâmetros de consulta de entrada eventualmente são convertidos em parâmetros de backend usados para executar a pesquisa. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> <p>Os parâmetros de backend não são exibidos nos elementos de navegação. Como resultado, você pode ocultar quaisquer parâmetros adicionais que você deseja aplicar a uma pesquisa de seus clientes. </p> <p>O parâmetro é local para uma pesquisa específica em um modelo de apresentação. As ações nos parâmetros de backend são vinculação tardia; ou seja, eles são aplicados logo antes da pesquisa ser enviada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Modelo direcionado </p> </td> 
      <td colname="col2"> <p>Uma instância especial de uma variável personalizada definida pelo sistema que não pode ser excluída. Essa variável contém o modelo de apresentação direcionado atual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação </p> </td> 
      <td colname="col2"> <p>Permite que você especifique qual regra de classificação usar na pesquisa. Essa opção só aparece quando você definiu campos de classificação e regras de classificação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última regra </p> </td> 
      <td colname="col2"> <p>Quando marcado, o módulo de processamento pós-pesquisa não executa nenhuma regra adicional após a ação da regra correspondente. Essa ação é útil para quando você define ações que fazem com que uma regra posterior corresponda, mas não quer que a regra posterior seja executada. </p> </td> 
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

## Editar uma regra de pós-pesquisa {#task_ECB00334C0A74C87AF857DB3EB372119}

É possível editar as regras de pós-pesquisa existentes que você adicionou à [!DNL Post-Search Rules] página.

**Para editar uma regra de pós-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na [!DNL Post-Search Rules] página, na **[!UICONTROL Actions]** coluna da tabela, clique **[!UICONTROL Edit]** para a regra associada que você deseja editar.
1. Na [!DNL Edit Post-Search Rule] página, use as listas suspensas e os campos de texto para desenvolver sua consulta.

   Consulte a tabela de opções em [Adicionar uma nova regra](../c-about-rules-menu/c-about-post-search-rules.md#task_52F6F9AAD65B45B5ACA1FF245DFFADD9)de pós-pesquisa.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma regra pós-pesquisa {#task_0F4653AB20D54B769A4FA8D1491AB4CF}

É possível excluir regras de pós-pesquisa que não são mais necessárias ou não são mais usadas.

Quando você exclui uma regra, a ordem em que as regras restantes são executadas é ajustada automaticamente para contabilizar a exclusão.

**Para excluir uma regra pós-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Na [!DNL Post-Search Rules] página, na **[!UICONTROL Actions]** coluna da tabela, clique **[!UICONTROL Delete]** para a regra associada que deseja excluir.
1. Na caixa de [!DNL Confirmation] diálogo, clique em **[!UICONTROL OK]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Alteração da ordem em que as regras de pós-pesquisa são executadas {#task_40542FCD32234BBF881A81BF5477F78F}

É possível reordenar as regras de pós-pesquisa para alterar a ordem em que são executadas nos modelos de apresentação.

As regras de pós-pesquisa são executadas na ordem em que foram definidas. Quanto maior for o número do pedido de uma regra, mais tarde ela será executada no processo, superando as regras anteriores. Você reorganiza as regras digitando um novo número na coluna Ordem da tabela na [!DNL Post-Search Rules] página. Também é possível usar as regras de arrastar e soltar para alterar a ordem de execução.

**Alteração da ordem em que as regras de pós-pesquisa são executadas**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Na [!DNL Post-Search Rules] página, execute um dos procedimentos a seguir:

   * Clique no cabeçalho da **[!UICONTROL Order]** coluna para classificar as regras em ordem crescente ou decrescente.
   * Na [!DNL Order] coluna, no campo de texto à esquerda de um nome de regra de pré-pesquisa, digite o número do pedido que deseja que a regra execute.
   * Arraste e solte uma linha de tabela na posição em que deseja que a regra seja executada. Todos os números de pedido são atualizados para refletir a nova ordem em que as regras são executadas.

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
