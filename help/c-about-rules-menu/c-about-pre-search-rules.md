---
description: Use Regras de pré-pesquisa para analisar a consulta recebida e determinar qual modelo de apresentação usar. As Regras de pré-pesquisa são executadas em sequência para cada consulta. Para alterar a ordem de suas regras, você pode usar o recurso de arrastar e soltar. A ordem real não é alterada até que você a salve.
solution: Target
title: Sobre as regras de pré-pesquisa
topic-legacy: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
exl-id: 23e7feda-956a-48ce-8c61-fe0498c1bbda
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1661'
ht-degree: 1%

---

# Sobre as regras de pré-pesquisa{#about-pre-search-rules}

Use Regras de pré-pesquisa para analisar a consulta recebida e determinar qual modelo de apresentação usar. As Regras de pré-pesquisa são executadas em sequência para cada consulta. Para alterar a ordem de suas regras, você pode usar o recurso de arrastar e soltar. A ordem real não é alterada até que você a salve.

## Uso das regras de pré-pesquisa {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

Normalmente, as Regras pré-pesquisa são usadas para selecionar qual modelo de apresentação exibe os resultados com base na consulta recebida. Recursos mais avançados podem ser usados para alterar a consulta usada para uma pesquisa que está sendo feita para um modelo de apresentação. Você pode adicionar, excluir ou alterar o valor dos parâmetros de consulta, conforme necessário. Para cada query recebida, um módulo de pré-pesquisa examina as regras de pré-pesquisa para determinar se a query é modificada e qual template de apresentação é usado. Cada Regra de pré-pesquisa consiste em dois elementos principais: as ações da regra e as condições opcionais. Você pode especificar um número ilimitado de regras e condições. A ordem dessas regras é importante, pois o conjunto de regras é loopado por regra. Quando as condições de uma regra são satisfeitas, todas as ações associadas são executadas.

No módulo de Processamento de Pré-pesquisa , todos os modelos definidos e suas pesquisas nomeadas associadas são instanciadas, onde cada pesquisa recebe uma cópia local dos parâmetros da cgi. Como resultado, você pode personalizar uma pesquisa adicionando, excluindo ou alterando um dos parâmetros de cgi que a pesquisa usa sem alterar qualquer outra pesquisa nomeada que o modelo usa ou afetando qualquer um dos outros modelos. Como resultado, se você tiver um modelo de apresentação que exibe mais de um conjunto de resultados, poderá personalizar cada pesquisa individualmente. Se você quiser executar alterações nos parâmetros CGI globais antes que sejam copiados para cada pesquisa de cada modelo, use o módulo Limpeza de Consulta.

## Condições da regra de pré-pesquisa {#section_B5568ADEB28546A280720309498B045D}

As condições são opcionais. Se você optar por ter ações especificadas para cada query, as ações serão sempre executadas. É considerada prática recomendada para a primeira regra ser executada para cada query, onde seleciona o modelo de apresentação padrão. Dessa forma, você pode ter certeza de que, independentemente do que é o query de entrada, selecionou um modelo de apresentação do pior cenário para usar. As condições podem ser baseadas em qualquer parâmetro de consulta CGI, cookie ou variável personalizada que uma regra anterior tenha definido ou em uma variável do sistema.

## Ações da regra de pré-pesquisa {#section_3B8E19D287554C1C969F5B8D81226981}

Todas as ações em uma Regra de pré-pesquisa que têm condições correspondentes são exercidas. As ações normalmente consistem em uma operação, os dados para executar a operação e o valor a ser usado. A ação mais simples é especificar qual modelo de apresentação usar quando a consulta corresponder às condições da Regra de pré-pesquisa. Em seguida, defina o template de target para o nome do template de apresentação. Ações mais complicadas podem ser usadas para alterar a pesquisa usada para um determinado modelo por meio da execução de uma operação no parâmetro de pesquisa de um modelo. Ao executar uma operação no parâmetro de pesquisa de um modelo, especifique um modelo de apresentação e uma pesquisa.

## Regras genéricas {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

Ao executar operações no parâmetro de pesquisa de um modelo, existem dois valores especiais: *direcionado e *principal para o modelo de apresentação e a pesquisa nomeada, respectivamente. Com esses valores, você pode criar regras baseadas na pesquisa principal do modelo direcionado atual. Essas construções permitem a criação de regras genéricas, onde não é necessário se preocupar com o nome do modelo direcionado ou da pesquisa primária atual. Obviamente, uma Regra pré-pesquisa anterior define o modelo direcionado atual. Caso contrário, um modelo de apresentação inicial será selecionado para você, o que produzirá resultados indesejados.

## Exemplos {#section_EA153A151987454EA44A4A6862466DF6}

Defina o modelo padrão como guided.tmpl, quando o usuário passa um parâmetro de cgi chamado lang, definido como um idioma conhecido, use o modelo desse idioma.

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
* A extração de dados da consulta é feita dentro das regras de limpeza de consulta. Você pode referenciá-los no processamento anterior à pesquisa.
* Adicione novas variáveis personalizadas que você introduziu nas Regras de pré-pesquisa a uma regra de pré-pesquisa que é executada para cada consulta antes que outras Regras de pré-pesquisa as referenciem.

## Adicionar uma nova regra de pré-pesquisa {#task_182B95918462490D8BDA7F16A81CAC11}

Você pode usar [!DNL Pre-Search Rules] para selecionar qual modelo de apresentação é usado para exibir os resultados da pesquisa com base na query recebida.

**Para adicionar uma nova regra de pré-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules], clique em **[!UICONTROL Add New Rule]**.
1. No campo [!DNL Name], digite o nome da nova regra de limpeza de consulta.
1. Na página [!DNL Add Pre-Search Rule] , use as listas suspensas e os campos de texto para criar sua query.

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
      <td colname="col2"> <p>Um cookie HTTP. O nome e os valores dos cookies devem ser codificados com o Identificador de recurso uniforme. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variável personalizada </p> </td> 
      <td colname="col2"> <p>Uma variável definida pelo usuário. Adicione, exclua ou defina uma quantidade ilimitada de variáveis definidas pelo usuário. </p> <p>Você pode fazer referência a qualquer variável definida no módulo Limpeza de Consulta nas Regras Pré-Pesquisa. </p> </td> 
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
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Faceta </p> </td> 
      <td colname="col2"> <p>Parâmetros CGI especiais na coleção global que estão associados a uma faceta específica. Todos os parâmetros CGI são copiados para cada pesquisa nomeada dentro de um modelo após a Limpeza de consulta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de consulta </p> </td> 
      <td colname="col2"> <p>Parâmetro CGI na coleção global. Esses parâmetros são copiados para cada pesquisa nomeada dentro de um modelo após a Limpeza de consulta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de pesquisa do modelo </p> </td> 
      <td colname="col2"> <p>Um parâmetro CGI local para uma pesquisa nomeada associada a um modelo de apresentação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetro de backend do modelo </p> </td> 
      <td colname="col2"> <p>Os parâmetros de consulta de entrada eventualmente são traduzidos em parâmetros de backend usados para executar a pesquisa. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> <p>Os parâmetros de backend não são exibidos nos elementos de navegação. Como resultado, você pode ocultar quaisquer parâmetros adicionais que deseja aplicar a uma pesquisa dos seus clientes. O parâmetro é local para uma pesquisa específica em um modelo de apresentação. As ações nos parâmetros de back-end são vinculação tardia; ou seja, elas são aplicadas antes do envio da pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Modelo direcionado </p> </td> 
      <td colname="col2"> <p>Uma instância especial de uma variável personalizada definida pelo sistema que não pode ser excluída. Essa variável contém o template de apresentação direcionado atual. Você pode ler ou definir essa variável especificando a variável personalizada "targeted_template". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação </p> </td> 
      <td colname="col2"> <p>Permite que você especifique a regra de classificação a ser usada na pesquisa. Essa opção só aparece quando você definiu campos de classificação e regras de classificação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Loja </p> </td> 
      <td colname="col2"> <p>O mecanismo de pesquisa detecta automaticamente em qual armazenamento o cliente está, com base no nome do host ou no parâmetro de consulta <span class="codeph"> gs_store </span>, com a última prioridade. Você pode criar condições fora da loja. Apenas na limpeza de consultas, também é possível usar uma ação para substituir a loja atual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última Regra </p> </td> 
      <td colname="col2"> <p>Quando marcado, o módulo de processamento de pré-pesquisa não executa regras adicionais após a ação da regra correspondente. Essa ação é útil para quando você define ações que fazem com que uma regra posterior seja correspondente, mas não deseja que a regra posterior seja executada. </p> </td> 
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

## Editar uma regra de pré-pesquisa {#task_25F77050C5DA42B29DFD1C9718FB8C64}

É possível editar as regras de pré-pesquisa existentes que você adicionou à página [!DNL Pre-Search Rules].

**Para editar uma regra de pré-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules] , na coluna **[!UICONTROL Actions]** da tabela, clique em **[!UICONTROL Edit]** para a regra associada que deseja editar.
1. Na página [!DNL Edit Pre-Search Rule] , use as listas suspensas e os campos de texto para criar sua query.

   Consulte a tabela de opções em [Adicionar uma nova regra pré-pesquisa](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma regra de pré-pesquisa {#task_128B6A79CA6C451C991AEDAD58F51743}

É possível excluir regras de pré-pesquisa que não são mais necessárias ou usadas.

Quando você exclui uma regra, a ordem em que as regras restantes são executadas é ajustada automaticamente para contabilizar a exclusão.

**Para excluir uma regra de pré-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules] , na coluna **[!UICONTROL Actions]** da tabela, clique em **[!UICONTROL Delete]** para a regra associada que deseja excluir.
1. Na caixa de diálogo [!DNL Confirmation], clique em **[!UICONTROL OK]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Alteração da ordem em que as regras de pré-pesquisa são executadas {#task_C18817276A3C459089C97448076365D1}

Você pode reordenar as regras de pré-pesquisa para alterar a ordem em que são executadas nos modelos de apresentação.

As regras de pré-pesquisa são executadas na ordem em que foram definidas. Quanto maior for o número do pedido de uma regra, mais tarde ela será executada no processo, superando as regras anteriores. Você reorganiza as regras inserindo um novo número na coluna Ordem da tabela na página [!DNL Pre-Search Rules]. Também é possível usar as regras de arrastar e soltar para alterar a ordem de execução.

**Para alterar a ordem de execução das regras de pré-pesquisa**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Na página [!DNL Pre-Search Rules], execute um dos seguintes procedimentos:

   * Clique no cabeçalho da coluna **[!UICONTROL Order]** para classificar as regras em ordem crescente ou decrescente.
   * Na coluna **[!UICONTROL Order]** , no campo de texto à esquerda de um nome de regra de pré-pesquisa, digite o número do pedido que deseja que a regra seja executada.
   * Arraste e solte uma linha de tabela na posição em que deseja que a regra seja executada. Todos os números de pedido são atualizados para refletir a nova ordem em que as regras são executadas.

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
