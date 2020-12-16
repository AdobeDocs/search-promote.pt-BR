---
description: As Visualizações de dados exibem os resultados da pesquisa com os campos meta. Cada coluna é um campo de meta e cada linha é resultado de um query de pesquisa. Personalize Visualizações de dados escolhendo e reorganizando colunas. As Visualizações de dados também podem ter títulos e descrições personalizados.
seo-description: As Visualizações de dados exibem os resultados da pesquisa com os campos meta. Cada coluna é um campo de meta e cada linha é resultado de um query de pesquisa. Personalize Visualizações de dados escolhendo e reorganizando colunas. As Visualizações de dados também podem ter títulos e descrições personalizados.
seo-title: Sobre Visualizações de dados
solution: Target
title: Sobre Visualizações de dados
topic: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
translation-type: tm+mt
source-git-commit: 7af85dd37f06fe506e5f57e28a25385ca7ab3db5
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 1%

---


# Sobre Visualizações de dados{#about-data-views}

As Visualizações de dados exibem os resultados da pesquisa com os campos meta. Cada coluna é um campo de meta e cada linha é resultado de um query de pesquisa. Personalize Visualizações de dados escolhendo e reorganizando colunas. As Visualizações de dados também podem ter títulos e descrições personalizados.

## Usando Visualizações de dados {#concept_DCA897D074464BC1861AA47B40CC86C3}

Cada conta tem a conveniência de criar várias visualizações de dados. Use a página Visualizações de dados para criar e editar essas visualizações de dados.

Depois de adicionar uma visualização de dados, é necessário editá-la para configurar e personalizar a visualização.

Consulte [Editar uma visualização de dados](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

É possível copiar uma visualização de dados existente para usar como a base para a criação de uma nova visualização de dados.

Consulte [Copiando uma visualização de dados](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF).

## Adicionando uma visualização de dados {#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

Você pode adicionar uma visualização de dados à página [!DNL Data Views] para exibir os valores de cada campo meta com um query de pesquisa.

Depois de adicionar uma visualização de dados, é necessário editá-la para configurar e personalizar a visualização.

Consulte [Editar uma visualização de dados](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

**Para adicionar uma visualização de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na página [!DNL Data Views], clique em **[!UICONTROL Add New Data View]**.
1. Na caixa de diálogo [!DNL Add New Data View], no campo [!DNL Title], digite o nome da visualização de dados que deseja criar.
1. Clique em **[!UICONTROL Add]**.

## Edição de uma visualização de dados {#task_258A367896C24DD498C755925EA8F516}

Ao adicionar uma visualização de dados à página [!DNL Data Views], use Editar para alterar o nome e a descrição da visualização de dados ou para mover, revelar ou ocultar a exibição de cada campo meta.

Você também pode bloquear ou desbloquear uma visualização de dados selecionada.

Consulte [Adicionar uma visualização de dados](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D).

**Para editar uma visualização de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na página [!DNL Data Views], na coluna [!DNL Actions] da tabela, clique em **[!UICONTROL Edit]** na linha com a visualização de dados que deseja alterar.
1. Na página [!DNL Data Views Editor], defina as opções desejadas.

   O Editor de Visualização de dados tem todos os controles para ocultar, mostrar e mover colunas de campo na página Visualização de dados.

   Quando você visualização uma visualização de dados, a tabela resultante também mostra os seguintes campos de coluna adicionais que não são editáveis: Classificação, relevância e pontuação (geral). Esses três campos especiais representam as pontuações de relevância, as pontuações de classificação e as pontuações gerais para cada resultado.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Título </p> </td> 
      <td colname="col2"> <p>O nome da visualização de dados. O nome é exibido na parte superior direita quando você visualização a visualização de dados. </p> <p>Consulte <a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local"> Visualizando uma visualização de dados</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Descrição </p> </td> 
      <td colname="col2"> <p>(Opcional) Contém uma descrição da visualização de dados. A descrição é exibida entre o nome do título da visualização de dados e o campo de texto <span class="wintitle"> Nova pesquisa</span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetros de pesquisa </p> </td> 
      <td colname="col2"> <p>Permite que você especifique parâmetros de pesquisa padrão. Quando a visualização de dados é exibida pela primeira vez, esses parâmetros CGI são anexados automaticamente. </p> <p>Não altere nem exclua <span class="codeph"> sp_cs</span> ou <span class="codeph"> sp_f</span>. Esses parâmetros são essenciais para a Visualização de dados, independentemente do conjunto de caracteres preferencial da conta. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bloquear status </p> </td> 
      <td colname="col2"> <p>Permite bloquear ou desbloquear a visualização de dados. </p> <p>Você pode visualização uma visualização de dados bloqueada somente com uma senha e um nome de usuário. O usuário deve ser um membro atual da conta. </p> <p>Uma visualização de dados desbloqueada é acessada sem uma senha ou conta de usuário. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p> Permite alterar a ordem da coluna editando o número na caixa de texto <span class="wintitle"> Order</span>. Também é possível arrastar e soltar uma linha para alterar a ordem da coluna. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir </p> </td> 
      <td colname="col2"> <p> Permite ativar ou desativar a exibição da coluna. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Exibir URL como imagem </p> </td> 
      <td colname="col2"> <p>Exiba miniaturas e imagens nesta coluna se o resultado da pesquisa para esta coluna retornar um URL. </p> <p>O URL é removido do nome do esquema ou protocolo antes de se tornar um valor do atributo <span class="codeph"> src</span> de uma tag de imagem. </p> <p>Se o resultado da pesquisa de retorno não se parecer com um URL para uma imagem, então um é exibido. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Extensão do campo </p> </td> 
      <td colname="col2"> <p>Define o número de caracteres exibidos como resultado da visualização de dados. </p> <p>O padrão é 100 caracteres. </p> <p>Alguns campos, como a pontuação de classificação e o campo de data, não têm tamanhos de campo ajustáveis. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copiando uma visualização de dados {#task_78D4C2799BC84677843ED4CA1CD205AF}

Você pode copiar uma visualização de dados existente na página [!DNL Data Views] para usar como a base para a criação de uma nova visualização de dados.

Depois de copiar uma visualização de dados, você pode personalizá-la ainda mais editando a visualização.

Consulte [Editar uma visualização de dados](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

**Para copiar uma visualização de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na página [!DNL Data Views], na coluna [!DNL Actions] da tabela, clique em **[!UICONTROL Copy]** na linha com a visualização de dados que deseja copiar.
1. Na página [!DNL Copy Data View], no campo de texto [!DNL New Title], digite o novo nome que você deseja atribuir à visualização de dados.
1. Clique em **[!UICONTROL Copy]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma visualização de dados {#task_61C32F8F00A549A5A3E7EDDA6F537098}

Você pode excluir uma visualização de dados na página [!DNL Data Views] que não é mais necessária ou não é mais usada.

**Para excluir uma visualização de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na página [!DNL Data Views], na coluna [!DNL Actions] da tabela, clique em **[!UICONTROL Delete]** na linha com a visualização de dados que deseja remover.
1. Na página [!DNL Delete Data View], clique em **Excluir**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Exibindo uma visualização de dados {#task_FD0D2CE53DF84CBD9220AD7CA920011F}

Você pode usar [!DNL View] na página [!DNL Data Views] para exibir uma visualização de dados selecionada.

A visualização de dados selecionada é aberta em uma janela separada do navegador.

**Para visualização de uma visualização de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Execute um dos procedimentos a seguir:

   * Na página [!DNL Data Views], na coluna [!DNL Title] da tabela, clique no nome de uma visualização de dados que deseja abrir.

   * Na página [!DNL Data Views], na coluna [!DNL Actions] da tabela, clique em **[!UICONTROL View]** na linha com a visualização de dados que deseja abrir.

