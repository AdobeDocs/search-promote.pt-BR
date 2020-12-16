---
description: Use as Regras de pré-pesquisa para analisar o query recebido e determinar qual modelo de apresentação usar. As Regras de pré-pesquisa são executadas em sequência para cada query. Para alterar a ordem de suas regras, é possível usar o recurso arrastar e soltar. A ordem real não é alterada até que você a salve.
seo-description: Use as Regras de pré-pesquisa para analisar o query recebido e determinar qual modelo de apresentação usar. As Regras de pré-pesquisa são executadas em sequência para cada query. Para alterar a ordem de suas regras, é possível usar o recurso arrastar e soltar. A ordem real não é alterada até que você a salve.
seo-title: Sobre as regras de pré-pesquisa
solution: Target
title: Sobre as regras de pré-pesquisa
topic: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d
workflow-type: tm+mt
source-wordcount: '1709'
ht-degree: 1%

---


# Sobre as regras de pré-pesquisa{#about-pre-search-rules}

Use as Regras de pré-pesquisa para analisar o query recebido e determinar qual modelo de apresentação usar. As Regras de pré-pesquisa são executadas em sequência para cada query. Para alterar a ordem de suas regras, é possível usar o recurso arrastar e soltar. A ordem real não é alterada até que você a salve.

## Usando regras de pré-pesquisa {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

Normalmente, as Regras de pré-pesquisa são usadas para selecionar qual modelo de apresentação exibe os resultados com base no query recebido. Recursos mais avançados podem ser usados para alterar o query usado para uma pesquisa que está sendo feita para um modelo de apresentação. Você pode adicionar, excluir ou alterar o valor dos parâmetros do query, conforme necessário. Para cada query recebido, um módulo de processamento de pré-pesquisa examina as regras de pré-pesquisa para determinar se o query foi modificado e qual modelo de apresentação é usado. Cada regra de pré-pesquisa consiste em dois elementos principais: as ações da regra e as condições opcionais. Você pode especificar um número ilimitado de regras e condições. A ordem dessas regras é importante, pois o conjunto de regras é repetido por regra. Quando as condições de uma regra são correspondidas, todas as ações associadas são executadas.

No módulo Processamento de pré-pesquisa, todos os modelos definidos e suas pesquisas nomeadas associadas são instanciadas, onde cada pesquisa recebe uma cópia local dos parâmetros cgi. Como resultado, você pode personalizar uma pesquisa adicionando, excluindo ou alterando um dos parâmetros cgi que a pesquisa usa sem alterar qualquer outra pesquisa nomeada que o modelo usa ou afetando qualquer outro modelo. Como resultado, se você tiver um modelo de apresentação que exibe mais de um conjunto de resultados, poderá personalizar cada pesquisa individualmente. Se você quiser realizar alterações nos parâmetros CGI globais antes que eles sejam copiados para cada pesquisa para cada modelo, use o módulo Limpeza de Query.

## Condições de regras de pré-pesquisa {#section_B5568ADEB28546A280720309498B045D}

As condições são opcionais. Se você optar por ter ações especificadas para cada query, as ações sempre serão executadas. É considerada a prática recomendada para a primeira regra ser executada para cada query, onde seleciona o modelo de apresentação padrão. Dessa forma, você pode ter certeza de que, independentemente do que for o query recebido, selecionou um modelo de apresentação de pior cenário para usar. As condições podem ser baseadas em qualquer parâmetro de query CGI, cookie ou variável personalizada que uma regra anterior tenha definido ou em uma variável do sistema.

## Ações de regras de pré-pesquisa {#section_3B8E19D287554C1C969F5B8D81226981}

Todas as ações dentro de uma Regra de pré-pesquisa que tem condições correspondentes são exercidas. Normalmente, as ações consistem em uma operação, nos dados para executar a operação e no valor a ser usado. A ação mais simples é especificar qual modelo de apresentação usar quando o query corresponder às condições da Regra de pré-pesquisa. Em seguida, defina o modelo direcionado com o nome do modelo de apresentação. Ações mais complicadas podem ser usadas para alterar a pesquisa que está sendo usada para um determinado modelo por meio da execução de uma operação no parâmetro de pesquisa de um modelo. Ao executar uma operação no parâmetro de pesquisa de um modelo, especifique um modelo de apresentação e uma pesquisa.

## Regras genéricas {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

Ao executar operações no parâmetro de pesquisa de um modelo, existem dois valores especiais: *direcionado e *principal para o modelo de apresentação e a pesquisa nomeada, respectivamente. Com esses valores, você pode criar regras com base na pesquisa principal do modelo direcionado atual. Essas construções permitem criar regras genéricas onde você não precisa se preocupar com o que o modelo direcionado atual ou a pesquisa primária são chamados. Obviamente, uma Regra de pré-pesquisa anterior define o modelo direcionado atual. Caso contrário, um modelo de apresentação inicial será selecionado para você, produzindo resultados indesejados.

## Exemplos {#section_EA153A151987454EA44A4A6862466DF6}

Defina o modelo padrão como guided.tmpl, quando o usuário passar em um parâmetro cgi chamado lang, definido como um idioma conhecido, use o modelo desse idioma.

```
    On condition: 
      Every Query 
    Perform the following actions: 
      Set targeted template to guided 
 
    On condition: 
      Query lang matches regular expression fr 
    Perform the following actions: 
      Set targeted template to guided_french 
 
    On condition: 
      Query lang matches regular expression de 
    Perform the following actions: 
      Set targeted template to guided_german
```

## Práticas recomendadas {#section_31EBAE5E54174DEE8986CBB636746A98}

* A primeira regra seleciona um modelo padrão para cada query.
* A extração de dados do query é feita dentro das regras de limpeza do query. É possível referenciá-los no processamento pré-pesquisa.
* Adicione quaisquer novas variáveis personalizadas que você introduziu nas Regras de pré-pesquisa a uma regra de pré-pesquisa que é executada para cada query antes que qualquer outra Regra de pré-pesquisa as referencie.

## Adicionando uma nova regra de pré-pesquisa {#task_182B95918462490D8BDA7F16A81CAC11}

Você pode usar [!DNL Pre-Search Rules] para selecionar qual modelo de apresentação é usado para exibir os resultados da pesquisa com base no query recebido.

**Para adicionar uma nova regra de pré-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules], clique em **[!UICONTROL Add New Rule]**.
1. No campo [!DNL Name], digite o nome da nova regra de limpeza de query.
1. Na página [!DNL Add Pre-Search Rule], use as listas suspensas e os campos de texto para desenvolver seu query.

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
      <td colname="col2"> <p>Um cookie HTTP. O nome e os valores dos cookies devem estar codificados no Identificador de recurso uniforme. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável personalizada </p> </td> 
      <td colname="col2"> <p>Uma variável definida pelo usuário. Adicione, exclua ou defina uma quantidade ilimitada de variáveis definidas pelo usuário. </p> <p>É possível fazer referência a quaisquer variáveis que você definiu no módulo Limpeza de Query dentro das Regras de pré-pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável do sistema </p> </td> 
      <td colname="col2"> <p>Variáveis somente leitura definidas pelo sistema interno que você pode verificar. As seguintes variáveis do sistema são suportadas: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> nome do host  </span> <p>O nome do host do servidor. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>O URI solicitado sem a string de query. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>A string inteira do query. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> ambiente </span> <p>"Palco" ou "ao vivo", dependendo se o query recebido foi enviado para o ambiente preparado ou ao vivo. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>O URL de onde o cliente veio. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aspecto </p> </td> 
      <td colname="col2"> <p>Parâmetros CGI especiais na coleção global que estão associados a uma faceta específica. Todos os parâmetros CGI são copiados para cada pesquisa nomeada dentro de um modelo após a Limpeza de Query. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de consulta </p> </td> 
      <td colname="col2"> <p>Parâmetro CGI na coleção global. Esses parâmetros são copiados para cada pesquisa nomeada dentro de um modelo após a Limpeza de Query. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de pesquisa do modelo </p> </td> 
      <td colname="col2"> <p>Um parâmetro CGI que é local para uma pesquisa nomeada associada a um modelo de apresentação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de backend do modelo </p> </td> 
      <td colname="col2"> <p>Os parâmetros de query de entrada acabam sendo convertidos em parâmetros de backend usados para executar a pesquisa. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> <p>Os parâmetros de backend não são exibidos nos elementos de navegação. Como resultado, você pode ocultar quaisquer parâmetros adicionais que você deseja aplicar a uma pesquisa de seus clientes. O parâmetro é local para uma pesquisa específica em um modelo de apresentação. As ações nos parâmetros de backend são vinculação tardia; ou seja, eles são aplicados logo antes da pesquisa ser enviada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Modelo direcionado </p> </td> 
      <td colname="col2"> <p>Uma instância especial de uma variável personalizada definida pelo sistema que não pode ser excluída. Essa variável contém o modelo de apresentação direcionado atual. Você pode ler ou definir essa variável especificando a variável personalizada "target_template". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação </p> </td> 
      <td colname="col2"> <p>Permite que você especifique qual regra de classificação usar na pesquisa. Essa opção só aparece quando você definiu campos de classificação e regras de classificação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Loja </p> </td> 
      <td colname="col2"> <p>O mecanismo de pesquisa detecta automaticamente em qual loja o cliente está com base no nome do host ou no parâmetro de query <span class="codeph"> gs_store </span>, tendo o último precedência. Você pode criar condições fora da loja. Somente na limpeza de query, também é possível usar uma ação para substituir a loja atual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última regra </p> </td> 
      <td colname="col2"> <p>Quando marcado, o módulo de processamento de pré-pesquisa não executa nenhuma regra adicional após a ação da regra de correspondência. Essa ação é útil para quando você define ações que fazem com que uma regra posterior corresponda, mas não quer que a regra posterior seja executada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suspender </p> </td> 
      <td colname="col2"> <p>Desativa a execução da regra, mas não a exclui. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editando uma regra de pré-pesquisa {#task_25F77050C5DA42B29DFD1C9718FB8C64}

Você pode editar as regras de pré-pesquisa existentes que você adicionou à página [!DNL Pre-Search Rules].

**Para editar uma regra de pré-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules], na coluna **[!UICONTROL Actions]** da tabela, clique em **[!UICONTROL Edit]** para obter a regra associada que você deseja editar.
1. Na página [!DNL Edit Pre-Search Rule], use as listas suspensas e os campos de texto para desenvolver seu query.

   Consulte a tabela de opções em [Adicionar uma nova regra de pré-pesquisa](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma regra de pré-pesquisa {#task_128B6A79CA6C451C991AEDAD58F51743}

É possível excluir regras de pré-pesquisa que não são mais necessárias ou não são mais usadas.

Quando você exclui uma regra, a ordem em que as regras restantes são executadas é ajustada automaticamente para contabilizar a exclusão.

**Para excluir uma regra de pré-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules], na coluna **[!UICONTROL Actions]** da tabela, clique em **[!UICONTROL Delete]** para obter a regra associada que você deseja excluir.
1. Na caixa de diálogo [!DNL Confirmation], clique em **[!UICONTROL OK]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Alteração da ordem em que as regras de pré-pesquisa são executadas {#task_C18817276A3C459089C97448076365D1}

É possível reordenar as regras de pré-pesquisa para alterar a ordem em que são executadas nos modelos de apresentação.

As regras de pré-pesquisa são executadas na ordem em que foram definidas. Quanto maior for o número do pedido de uma regra, mais tarde ela será executada no processo, superando as regras anteriores. Você reorganiza as regras digitando um novo número na coluna Ordem da tabela na página [!DNL Pre-Search Rules]. Também é possível usar as regras de arrastar e soltar para alterar a ordem de execução.

**Alteração da ordem em que as regras de pré-pesquisa são executadas**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules], execute um dos procedimentos a seguir:

   * Clique no cabeçalho da coluna **[!UICONTROL Order]** para classificar as regras em ordem crescente ou decrescente.
   * Na coluna **[!UICONTROL Order]**, no campo de texto à esquerda de um nome de regra de pré-pesquisa, digite o número do pedido que deseja que a regra execute.
   * Arraste e solte uma linha de tabela na posição em que deseja que a regra seja executada. Todos os números de pedido são atualizados para refletir a nova ordem em que as regras são executadas.

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

