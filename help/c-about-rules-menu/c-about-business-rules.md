---
description: Você pode usar as Regras de negócios para anunciar sua pesquisa.
solution: Target
title: Sobre regras de negócios
topic: Regras, Pesquisa e comercialização do site
uuid: f2186f54-7a39-4f46-bb29-5115d5a17f07
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '3120'
ht-degree: 1%

---


# Sobre as Regras de Negócios{#about-business-rules}

Você pode usar as Regras de negócios para anunciar sua pesquisa.

## Usando Regras de Negócios {#concept_2A93D76216754D3D8412CDEA00BD26BD}

Por exemplo, você pode configurar quando os banners são exibidos, ou quais resultados são exibidos e em que ordem. Você também pode configurar a posição de um item em sua faceta e qual modelo é usado para determinada pesquisa. As regras são executadas na ordem em que foram definidas; quanto mais alto o número do pedido de uma regra, mais tarde ele será executado no processo, superando as regras anteriores. Você pode arrastar e soltar as regras para alterar sua ordem ou reorganizá-las inserindo um novo número na caixa de texto da ordem das regras.

Cada regra de negócios é composta de acionadores e ações.

O acionador define quando a regra é executada. Por exemplo, quando o termo de consulta é &quot;masculino&quot; ou quando os resultados são em sua maioria chapéus. O acionador consiste em várias condições que devem ser todas ou todas verdadeiras para que o acionador geral seja verdadeiro. É possível especificar a precedência alterando o operador do acionador.

A ação define o que acontece quando a condição de disparo é atendida. Por exemplo, definir o banner para exibir ou mover um determinado resultado para a posição 1. A tabela de regras mostra informações de resumo sobre a regra. Você pode clicar em um nome de regra para abri-la e ver informações adicionais.

A tabela de regras mostra uma lista de todas as suas regras de negócios. Por padrão, a tabela mostra as últimas dez regras que foram adicionadas, em ordem decrescente. Você pode clicar nos cabeçalhos da coluna na tabela para classificar as regras em ordem crescente ou decrescente.

As regras de negócios podem ter um dos três estados: Aprovado, Suspenso ou WIP (Trabalho em Andamento)

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Estado da regra de negócios </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aprovado </p> </td> 
   <td colname="col2"> <p>Regras de negócios aprovadas são executadas no ambiente ativo e no ambiente de preparo. Você aprova uma regra de negócios no Construtor de regras avançado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Suspenso </p> </td> 
   <td colname="col2"> <p>Regras de negócios suspensas nunca são executadas em seu ambiente de preparo ou em seu ambiente ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>WIP </p> </td> 
   <td colname="col2"> <p>WIP (Trabalho em progresso) são regras de negócios que não são aprovadas nem suspensas. Ou seja, você ainda pode estar trabalhando neles ou pode testá-los primeiro antes de aprová-los. Regras de negócios em um estado de WIP são executadas somente no ambiente de preparo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você aprova regras de negócios e as envia ao vivo para que sejam executadas em seu ambiente ativo. Atualmente, você só pode colocar as regras *all* online. No entanto, você pode alterar o status de uma regra para ter controle sobre quais regras são executadas e não são executadas em seu ambiente ativo.

Por padrão, as regras são executadas sempre que os acionadores associados são atendidos. No entanto, você pode, opcionalmente, programar uma regra para ser executada para uma data e um intervalo de tempo específicos.

Além disso, por padrão, as regras são executadas sempre que os acionadores associados são atendidos para todas as lojas. Se desejar que a regra seja aplicada somente a determinados armazenamentos, é possível usar o painel Armazenamentos para selecionar um ou mais armazenamentos aos quais a regra é aplicada.

## Adicionar uma nova regra de negócios {#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7}

Você pode usar [!DNL Visual Rule Builder] ou [!DNL Advanced Rule Builder] para adicionar regras de negócios que ajustem a experiência de pesquisa do cliente.

**Para adicionar uma nova regra de negócios**

As etapas a seguir pressupõem que você esteja usando o Construtor visual de regras.

1. Faça uma das seguintes opções:

   * No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**. Na página [!DNL Business Rules], clique em **[!UICONTROL Add New Rule]**.

   * No menu do produto, clique em **[!UICONTROL Simulator]**. Na página **[!UICONTROL Simulator for Today]** , clique em **[!UICONTROL Add New Rule]** à direita do menu suspenso **[!UICONTROL Options]**.

      Se a opção **[!UICONTROL Add New Rule]** não estiver visível na página, no menu suspenso **[!UICONTROL Options]**, clique em **[!UICONTROL Simulate Staged]**.

      ![](assets/Simulator.png)

1. No campo de texto **[!UICONTROL Name]**, digite o novo nome da regra de negócios.

   Ainda não clique em **[!UICONTROL Save Rule]**.
1. (Opcional) Se você gerenciar um grande número de regras de negócios, é possível marcar regras de negócios com rótulos específicos. No campo **[!UICONTROL Tags]** , insira um ou mais rótulos de tag, Use a vírgula, a Guia ou Enter como delimitador.

   Na página [!DNL Business Rules] , use o recurso **[!UICONTROL Filter by tag]** para filtrar regras que correspondam a um determinado rótulo. 1. Na página [!DNL Business Rule Builder], defina os acionadores e as ações que deseja usar.

   **Opções de acionador**

   Os acionadores são as condições que devem ser atendidas para que uma regra de negócios seja executada. Quando uma regra comercial tiver vários acionadores, você poderá configurar como os acionadores responderão usando um dos três métodos a seguir:

   * Uma resposta em que todos os acionadores devem ser verdadeiros (a configuração padrão), como no exemplo a seguir:

      `if a AND b AND c then ...`

   * Uma resposta em que qualquer um dos acionadores deve ser verdadeiro como no exemplo a seguir:

      `if a OR b OR c then ...`

   * Uma resposta em que uma combinação personalizada de acionadores é especificada. Ou seja, você combina acionadores individuais ou &quot;condições&quot; com operadores `AND` e operadores `OR`.

      Também é possível alterar a precedência da avaliação adicionando combinações de parênteses esquerdo e direito como no exemplo a seguir:

      `if (a OR b) AND c then ...`

      >[!NOTE]
      >
      >Se você combinar operadores `AND` com operadores `OR` em um conjunto de regras de negócios personalizado, certifique-se de especificar parênteses apropriadamente para garantir que os acionadores sejam avaliados na ordem correta.

      Esse recurso específico de personalizar uma combinação de acionadores não é habilitado por padrão. Entre em contato com o Suporte Técnico para ativar esse recurso para uso.
   <table> 
      <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção Triggers </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Correspondências de palavras-chave </p> </td> 
      <td colname="col2"> <p>O acionador é verdadeiro quando o termo de pesquisa corresponde a determinada palavra-chave que diferencia maiúsculas e minúsculas. O acionador é verdadeiro para a palavra-chave e todos os seus sinônimos, conforme definido no dicionário Linguística. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Correspondências de Consulta </p> </td> 
      <td colname="col2"> <p> O acionador é verdadeiro quando todos os parâmetros de pesquisa correspondem. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> O Grupo de Resultados é Dominante </p> </td> 
      <td colname="col2"> <p> O acionador é verdadeiro quando o grupo de resultados definido pela pesquisa fornecida domina o conjunto de resultados. </p> <p>Por padrão, a posição dominante é definida como 50%. Essa configuração é uma preferência de merchandising que pode ser definida. </p> <p> 
        <!--See <xref href="t_Configuring_Merchandising_preferences.xml#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A" type="task" format="dita" scope="local">Configuring Merchandising preferences</xref>. --> </p> <p>O grupo inteiro deve estar presente no conjunto de resultados para que esse acionador seja verdadeiro. O grupo de resultados é dinâmico. Elas podem ser alteradas após operações de índice, dependendo de quais resultados correspondem aos critérios de pesquisa originais. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>O Grupo de Resultados está presente </p> </td> 
      <td colname="col2"> <p> O acionador é verdadeiro quando o grupo de resultados definido pela pesquisa fornecida está presente no conjunto de resultados. O grupo inteiro deve estar presente no conjunto de resultados para que esse acionador seja atendido (os resultados podem estar presentes em qualquer página). O grupo de resultados é dinâmico e pode ser alterado após operações de índice dependentes de quais resultados correspondem aos critérios de pesquisa originais. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Resultado presente </p> </td> 
      <td colname="col2"> <p> O acionador é verdadeiro quando o resultado individual é encontrado dentro do conjunto de resultados. O resultado pode estar em qualquer lugar no conjunto de resultados, não precisa estar na página que o usuário está visualizando no momento. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opções de ação**

   Quando os acionadores de uma regra de negócios são atendidos, as ações associadas à regra são executadas. Embora o Construtor de regras visual permita que você crie as seguintes ações, você pode usar o Construtor de regras avançado para criar tipos adicionais de ações.

   As ações Remover item de faceta, Revelar item de faceta, Revelar faceta, Remover faceta, Empurrar item de faceta na tabela a seguir exigem uma faceta. A interface para escolher uma faceta depende de como sua conta está configurada. Por exemplo, uma conta normal usa uma lista suspensa para escolher aspectos. No entanto, se sua conta tiver facetas ajustadas, uma caixa de texto de preenchimento automático será exibida, onde você poderá inserir o nome de qualquer faceta. O preenchimento automático sugere aspectos em uma lista suspensa à medida que você digita o nome da faceta. As sugestões incluem aspectos definidos no momento. Se sua conta tiver um mapa de slot, também sugerirá facetas com slot.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção Ações </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Grupo de push </p> </td> 
      <td colname="col2"> <p> Força o grupo de resultados de pesquisa conforme definido pelos critérios de pesquisa especificados para uma posição específica. </p> <p>Mover um grupo de resultados de pesquisa não adiciona implicitamente o grupo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adicionar grupo </p> </td> 
      <td colname="col2"> <p> Adicione o grupo de resultados de pesquisa conforme definido pelos critérios de pesquisa especificados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover grupo </p> </td> 
      <td colname="col2"> <p> Remova o grupo de resultados de pesquisa definido pelos critérios de pesquisa especificados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Empurrar único </p> </td> 
      <td colname="col2"> <p> Força o resultado da pesquisa individual para a posição selecionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adicionar um único </p> </td> 
      <td colname="col2"> <p> Adiciona um resultado de pesquisa individual à posição selecionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover único </p> </td> 
      <td colname="col2"> <p> Remove um resultado de pesquisa individual do conjunto de resultados de pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover Todos os Resultados </p> </td> 
      <td colname="col2"> <p>Remove todos os resultados do conjunto de resultados da pesquisa. </p> <p> 
        <!-- Bug #3331637 The option is meant to be used in conjunction with other rule actions in order to create "canned landing pages" where we want to create a page's content solely by rule actions, and need to completely discard the "natural" results of the search. Given that the other options don't have any kind of "here's how/why you might use this", I don't see much point in breaking that precedent here.--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Selecionar banner diferente </p> </td> 
      <td colname="col2"> <p> Altera o banner na área do banner selecionado. </p> <p>Essa opção está disponível ao clicar com o botão direito do mouse em um banner na área de visualização da página da Web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adicionar comandos de banner </p> </td> 
      <td colname="col2"> <p>Aplica-se somente a modelos Adobe Dynamic Media Classic. </p> <p>Permite alterar os parâmetros padrão usados no modelo de banner. </p> <p>Consulte a tabela de opções em <a scope="local" href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita"> Adicionar um banner usando o Adobe Dynamic Media Classic </a>. </p> <p>Consulte também <a href="../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9" type="task" format="dita" scope="local"> Edição de um banner usando o Adobe Dynamic Media Classic </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover banner </p> </td> 
      <td colname="col2"> <p> Remove o banner da área selecionada do banner; nenhum banner é exibido, a menos que outra regra que defina um banner substitua essa regra. </p> <p>Essa opção está disponível ao clicar com o botão direito do mouse em um banner na área de visualização da página da Web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Enviar item de faceta </p> </td> 
      <td colname="col2"> <p> Força um item dentro de uma faceta para a posição selecionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover Zona </p> </td> 
      <td colname="col2"> <p> Remove uma zona da página de resultados da pesquisa. </p> <p>Consulte também a ação Remover face abaixo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zona de Revisão </p> </td> 
      <td colname="col2"> <p> Revela uma zona na página de resultados da pesquisa. </p> <p>Consulte também a ação Revelar Faceta abaixo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover item de faceta </p> </td> 
      <td colname="col2"> <p> Remove um item de faceta de uma faceta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ação de item de revelação de faceta </p> </td> 
      <td colname="col2"> <p> Revela um item de faceta específico. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Revelar Aspecto </p> </td> 
      <td colname="col2"> <p> Revela uma faceta específica. Essa ação é preferível à ação Zona de revelação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remover Faceta </p> </td> 
      <td colname="col2"> <p> Remove uma faceta específica. Essa ação é preferível à ação Remover zona. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Dependendo do painel do construtor de regras que está ativo (desdobrado), você também pode fazer o seguinte para definir acionadores e ações.

   * Quando o painel **[!UICONTROL Triggers]** for desdobrado - Na área de modelo de apresentação da página Construtor de regras de negócios, clique com o botão direito do mouse em qualquer resultado de pesquisa ou aspecto de pesquisa e depois clique em **[!UICONTROL Add "result present" trigger]**.

      No painel Triggers, clique no &quot;X&quot; à esquerda de um acionador para removê-lo da lista de acionadores.

   * Quando o painel **[!UICONTROL Actions]** for desdobrado - Na área de modelo de apresentação da página Construtor de regras de negócios , clique com o botão direito do mouse em um resultado de pesquisa. Clique em **[!UICONTROL Add Result]**, **[!UICONTROL Remove Result]**, **[!UICONTROL Push to bottom]** ou **[!UICONTROL Push to #`<n>`]** (onde `<n>` é um número).


1. (Opcional) Em qualquer painel Construtor de regras de negócios ( [!DNL Triggers], [!DNL Actions] ou [!DNL Schedule]), execute um dos seguintes procedimentos:

   * Na área de modelo de apresentação da página Construtor de regras de negócios , clique com o botão direito do mouse em um banner e depois clique em **[!UICONTROL Select different banner]**. Na página **[!UICONTROL Pick Banner]** , clique em **[!UICONTROL Pick this banner]** abaixo da miniatura do banner para adicioná-la ao modelo de apresentação. Somente banners que correspondem ao tamanho e à área do banner original no modelo de apresentação estão disponíveis para seleção.

      A ação adicionar banner é adicionada ao painel [!DNL Actions].

   * Na área de modelo de apresentação da página [!DNL Business Rule Builder], clique com o botão direito do mouse em um banner de modelo do Adobe Dynamic Media Classic cujos parâmetros você deseja alterar e clique em **[!UICONTROL Add banner commands]**. Na caixa de diálogo [!DNL Change Parameters], defina as opções de parâmetro desejadas.

      Consulte a tabela de opções em [Adicionar um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Clique em **[!UICONTROL Save]**.

      As alterações de parâmetro são adicionadas ao painel [!DNL Actions].

      Consulte também [Edição de um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * Na área de modelo de apresentação da página Construtor de regras de negócios , clique com o botão direito do mouse em um banner que deseja excluir da página e depois clique em **[!UICONTROL Remove banner]**. A ação remover banner é adicionada ao painel Ações.

1. (Opcional) No painel **[!UICONTROL Schedule]**, siga um destes procedimentos:

   * Clique em **[!UICONTROL Run Indefinitely]** para que a regra seja executada sempre que seus acionadores associados forem atendidos. Essa é a opção padrão.
   * Clique em **[!UICONTROL Fixed Schedule]** e especifique a data e a hora de início e a data e hora de término para que a regra seja executada sempre que seu acionador associado for atingido.

1. Clique em **[!UICONTROL Save Rule]**.
1. (Opcional) Na página [!DNL Business Rules] , execute um dos seguintes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma regra de negócios {#task_375CFA75D1D94D9E92A35DE1228E5087}

Você pode usar o Construtor de regras visual ou o Construtor de regras avançado para editar regras de negócios que você adicionou.

**Para editar uma nova regra de negócios**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Na página [!DNL Business Rules], execute um dos seguintes procedimentos:

   * Na coluna [!DNL Name] , clique no nome de uma regra de negócios que deseja alterar.

      A regra de negócios é aberta na interface padrão especificada em **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL My Preferences]**.

   * Na lista suspensa, ao lado do nome de uma regra comercial que você deseja editar, clique em **[!UICONTROL Edit in advanced mode]** ou **[!UICONTROL Edit in visual mode]**.

1. No campo de texto [!DNL Name], digite o novo nome da regra de negócios.

   Ainda não clique em **[!UICONTROL Save Rule]**. 1. Na página [!DNL Business Rule Builder], defina os acionadores e as ações que deseja usar.

   Consulte a tabela de opções em [Adicionar uma nova regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).
1. (Opcional) Em qualquer painel **[!UICONTROL Business Rule Builder]** ( [!DNL Triggers], [!DNL Actions] ou [!DNL Schedule], execute um dos seguintes procedimentos:

   * Na área de modelo da apresentação da página [!DNL Business Rule Builder], clique com o botão direito do mouse em um banner e depois clique em **[!UICONTROL Select different banner]**. No [!DNL Pick Banner page], clique em **[!UICONTROL Pick this banner]** abaixo da miniatura do banner para adicioná-la ao modelo de apresentação. Somente banners que correspondem ao tamanho e à área do banner original no modelo de apresentação estão disponíveis para seleção.

      A ação adicionar banner é adicionada ao painel [!DNL Actions].

   * Na área de modelo de apresentação da página [!DNL Business Rule Builder], clique com o botão direito do mouse em um banner de modelo do Adobe Dynamic Media Classic cujos parâmetros você deseja alterar e clique em **[!UICONTROL Add banner commands]**. Na caixa de diálogo [!DNL Change Parameters], defina as opções de parâmetro desejadas.

      Consulte a tabela de opções em [Adicionar um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Clique em **[!UICONTROL Save]**.

      As alterações de parâmetro são adicionadas ao painel [!DNL Actions].

      Consulte também [Edição de um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * Na área de modelo da apresentação da página [!DNL Business Rule Builder], clique com o botão direito do mouse em um banner que deseja excluir da página e depois clique em **[!UICONTROL Remove banner]**. A ação de remover banner é adicionada ao painel [!DNL Actions].

1. (Opcional) No painel [!DNL Schedule], siga um destes procedimentos:

   * Clique em **[!UICONTROL Run Indefinitely]** para que a regra seja executada sempre que seus acionadores associados forem atendidos. Essa é a opção padrão.
   * Clique em **[!UICONTROL Fixed Schedule]** e especifique a data e a hora de início e a data e hora de término para que a regra seja executada sempre que seu acionador associado for atendido.

1. Clique em **[!UICONTROL Save Rule]**.

   A página [!DNL Business Rule Builder] é fechada e você é retornado à página **[!UICONTROL Business Rule]**. Suas regras aparecem na tabela. Clique no cabeçalho da coluna **[!UICONTROL Modified]** para classificar as regras por data de edição. 1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copiando uma regra de negócios {#task_89F1879C71A54EE9B7454439302C03EC}

Você pode copiar uma regra de negócios existente para usar como base para uma nova regra de negócios que deseja criar.

**Para copiar uma regra de negócios**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Na página **[!UICONTROL Business Rules]** , na lista suspensa ao lado do nome de uma regra de negócios que você deseja copiar, clique em **[!UICONTROL Copy rule]**.
1. Edite a regra comercial copiada como de costume.

   Consulte [Editar uma regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

## Aprovar regras de negócios {#task_BD569D18BF664272B8692294C162E2C1}

Você pode ativar regras de negócios que tenham status WIP (Trabalho em progresso) ou suspenso.

**Para aprovar regras de negócios**

1. No menu do produto, clique em **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Na página [!DNL Business Rules] , usando o cabeçalho da coluna de status na coluna [!DNL Status] da tabela de regras de negócios, classifique as regras que têm um status de **[!UICONTROL WIP]** ou **[!UICONTROL suspended]**.

   Use o cabeçalho da coluna da caixa de seleção no lado esquerdo da tabela para verificar todas as regras exibidas atualmente na página ou verificar apenas aquelas que têm status **[!UICONTROL WIP]** ou **[!UICONTROL suspended]**. 1. Na barra de menu próxima à parte superior da página, clique em **[!UICONTROL Approve]**.
1. Na caixa de diálogo **[!UICONTROL Confirm Action]**, clique em **[!UICONTROL OK]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suspender regras de negócios {#task_364E1FFB905141C08E306C8F1794A20E}

Você pode suspender as regras de negócios que têm status WIP (Trabalho em progresso) ou aprovado.

Quando você suspende uma regra que está indicando na interface do usuário que a tornou temporariamente inativa e está adiando qualquer trabalho nela por outro tempo. No entanto, ainda é possível editar uma regra suspensa.

**Para suspender as regras de negócios**

1. No menu do produto, clique em **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Na página [!DNL Business Rules], usando o status na coluna Status da tabela de regras de negócios, na coluna à esquerda da tabela, verifique as regras que têm um status **[!UICONTROL WIP]** ou **[!UICONTROL approved]**.
1. Na barra de menu próxima à parte superior da página, clique em **[!UICONTROL Suspend]**.
1. Na caixa de diálogo **[!UICONTROL Confirm Action]**, clique em **[!UICONTROL OK]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Retomar regras de negócios {#task_E67D678C765B436EA2A3D6ADD7A49ABA}

Você pode retomar as regras de negócios para reativar uma regra suspensa. Após retomar a regra de negócios, seu status é definido como WIP (Trabalho em progresso).

**Para retomar as regras de negócios**

1. No menu do produto, clique em **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Na página [!DNL Business Rules] , usando o status na coluna Status da tabela de regras de negócios, na coluna à esquerda da tabela, verifique as regras que têm um status **[!UICONTROL suspended]**.
1. Na barra de menu próxima à parte superior da página, clique em **[!UICONTROL Resume]**.
1. Na caixa de diálogo [!DNL Confirm Action], clique em **[!UICONTROL OK]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Alteração da ordem em que as regras de negócios são executadas {#task_FE3B1C17307F49B49050C2EC5A063991}

Você pode reordenar as regras de negócios para alterar a ordem em que são executadas nos modelos de apresentação.

As regras de negócios são executadas na ordem em que foram definidas; quanto mais alto o número do pedido de uma regra, mais tarde ele será executado no processo, superando as regras anteriores. Você reorganiza as regras inserindo um novo número na coluna Ordem da tabela na página [!DNL Business Rules]. Também é possível usar as regras de arrastar e soltar para alterar a ordem de execução.

**Para alterar a ordem de execução das regras de negócios**

1. No menu do produto, clique em **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Na página [!DNL Business Rules] , na tabela, execute um dos seguintes procedimentos:

   * Clique no cabeçalho da coluna **[!UICONTROL Order]** para classificar as regras em ordem crescente ou decrescente.
   * Na coluna **[!UICONTROL Order]** , no campo de texto à esquerda do nome de uma regra de negócios, digite o número do pedido que deseja que a regra seja executada.
   * Arraste e solte uma linha de tabela na posição em que deseja que a regra seja executada. Todos os números de pedido são atualizados para refletir a nova ordem em que as regras são executadas.

1. Clique em **[!UICONTROL Save Changes]**.

   Suas regras de negócios serão executadas na ordem especificada. A exceção é se houver uma regra de negócios de redirecionamento especificada. Se e quando a regra de negócios de redirecionamento for acionada ou atingida, o processamento de regras de negócios para de permitir o redirecionamento.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo regras de negócios {#task_AE37B42412044541BCC6D46CF8793DFF}

Você pode excluir regras comerciais cujo status é WIP, suspenso ou aprovado, usando o menu suspenso Ações em massa .

**Para excluir regras de negócios**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Na página [!DNL Business Rules], execute um dos seguintes procedimentos:

   * Use o cabeçalho da coluna da caixa de seleção para verificar todas as regras exibidas atualmente na página.
   * Verifique somente as regras de negócios que deseja excluir, com base no status na coluna Status da tabela.

1. Na lista suspensa [!DNL Bulk Actions], clique em **[!UICONTROL Delete]**.
1. Na caixa de diálogo [!DNL Confirm Action], clique em **[!UICONTROL OK]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
