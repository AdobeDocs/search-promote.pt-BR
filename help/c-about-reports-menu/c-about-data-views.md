---
description: Exibições de dados exibe os resultados da pesquisa com os campos meta. Cada coluna é um campo meta e cada linha é resultado de uma consulta de pesquisa. Personalize as Exibições de dados escolhendo e reorganizando colunas. As Exibições de dados também podem ter títulos e descrições personalizados.
seo-description: Exibições de dados exibe os resultados da pesquisa com os campos meta. Cada coluna é um campo meta e cada linha é resultado de uma consulta de pesquisa. Personalize as Exibições de dados escolhendo e reorganizando colunas. As Exibições de dados também podem ter títulos e descrições personalizados.
seo-title: Sobre exibições de dados
solution: Target
title: Sobre exibições de dados
topic: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
translation-type: tm+mt
source-git-commit: 7af85dd37f06fe506e5f57e28a25385ca7ab3db5

---


# Sobre exibições de dados{#about-data-views}

Exibições de dados exibe os resultados da pesquisa com os campos meta. Cada coluna é um campo meta e cada linha é resultado de uma consulta de pesquisa. Personalize as Exibições de dados escolhendo e reorganizando colunas. As Exibições de dados também podem ter títulos e descrições personalizados.

## Uso de exibições de dados {#concept_DCA897D074464BC1861AA47B40CC86C3}

Cada conta tem a conveniência de criar várias exibições de dados. Use a página Exibições de dados para criar e editar essas exibições de dados.

Depois de adicionar uma exibição de dados, você deve editá-la para configurar e personalizar a exibição.

Consulte [Edição de uma exibição](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de dados.

É possível copiar uma exibição de dados existente para usar como a base para a criação de uma nova exibição de dados.

Consulte [Copiando uma exibição](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF)de dados.

## Adicionar uma exibição de dados {#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

Você pode adicionar uma exibição de dados à [!DNL Data Views] página para exibir os valores de cada campo meta com uma consulta de pesquisa.

Depois de adicionar uma exibição de dados, você deve editá-la para configurar e personalizar a exibição.

Consulte [Edição de uma exibição](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de dados.

**Para adicionar uma exibição de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na [!DNL Data Views] página, clique em **[!UICONTROL Add New Data View]**.
1. Na caixa de [!DNL Add New Data View] diálogo, no [!DNL Title] campo, digite o nome da exibição de dados que deseja criar.
1. Clique em **[!UICONTROL Add]**.

## Edição de uma exibição de dados {#task_258A367896C24DD498C755925EA8F516}

Ao adicionar uma exibição de dados à [!DNL Data Views] página, use Editar para alterar o nome e a descrição da exibição de dados ou para mover, revelar ou ocultar a exibição de cada campo de metadados.

Você também pode bloquear ou desbloquear uma exibição de dados selecionada.

Consulte [Adicionar uma exibição](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D)de dados.

**Para editar uma exibição de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na [!DNL Data Views] página, na [!DNL Actions] coluna da tabela, clique **[!UICONTROL Edit]** na linha com a exibição de dados que você deseja alterar.
1. Na [!DNL Data Views Editor] página, defina as opções desejadas.

   O Editor de visualização de dados tem todos os controles para ocultar, mostrar e mover colunas de campo na página Exibição de dados.

   Quando você exibe uma exibição de dados, a tabela resultante também mostra os seguintes campos de coluna adicionais que não são editáveis: Classificação, relevância e pontuação (geral). Esses três campos especiais representam as pontuações de relevância, as pontuações de classificação e as pontuações gerais para cada resultado.

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
      <td colname="col2"> <p>O nome da exibição de dados. O nome é exibido na parte superior direita quando você exibe a exibição de dados. </p> <p>Consulte <a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local"> Visualização de uma visualização</a>de dados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Descrição </p> </td> 
      <td colname="col2"> <p>(Opcional) Contém uma descrição da exibição de dados. A descrição é exibida entre o nome do título da exibição de dados e o campo de texto <span class="wintitle"> Nova pesquisa</span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetros de pesquisa </p> </td> 
      <td colname="col2"> <p>Permite que você especifique parâmetros de pesquisa padrão. Quando a exibição de dados é exibida pela primeira vez, esses parâmetros CGI são anexados automaticamente. </p> <p>Não altere nem exclua <span class="codeph"> sp_cs</span> ou <span class="codeph"> sp_f</span>. Esses parâmetros são essenciais para a Exibição de dados independentemente do conjunto de caracteres preferencial da conta. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros</a>CGI de pesquisa de backend. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bloquear status </p> </td> 
      <td colname="col2"> <p>Permite bloquear ou desbloquear a visualização de dados. </p> <p>É possível exibir uma exibição de dados bloqueados somente com uma senha e um nome de usuário. O usuário deve ser um membro atual da conta. </p> <p>Uma exibição de dados desbloqueada é acessada sem uma senha ou conta de usuário. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p> Permite alterar a ordem das colunas editando o número na caixa de texto <span class="wintitle"> Pedido</span> . Também é possível arrastar e soltar uma linha para alterar a ordem da coluna. </p> </td> 
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
      <td colname="col2"> <p>Define o número de caracteres exibidos como resultado na exibição de dados. </p> <p>O padrão é 100 caracteres. </p> <p>Alguns campos, como a pontuação de classificação e o campo de data, não têm tamanhos de campo ajustáveis. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cópia de uma exibição de dados {#task_78D4C2799BC84677843ED4CA1CD205AF}

É possível copiar uma exibição de dados existente na [!DNL Data Views] página para usar como a base para a criação de uma nova exibição de dados.

Depois de copiar uma exibição de dados, você pode personalizá-la ainda mais editando a exibição.

Consulte [Edição de uma exibição](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de dados.

**Para copiar uma exibição de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na [!DNL Data Views] página, na [!DNL Actions] coluna da tabela, clique **[!UICONTROL Copy]** na linha com a exibição de dados que deseja copiar.
1. Na [!DNL Copy Data View] página, no campo de [!DNL New Title] texto, digite o novo nome que você deseja atribuir à exibição de dados.
1. Clique em **[!UICONTROL Copy]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma exibição de dados {#task_61C32F8F00A549A5A3E7EDDA6F537098}

É possível excluir uma exibição de dados na [!DNL Data Views] página que não é mais necessária ou não é mais usada.

**Para excluir uma exibição de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Na [!DNL Data Views] página, na [!DNL Actions] coluna da tabela, clique **[!UICONTROL Delete]** na linha com a exibição de dados que deseja remover.
1. Na [!DNL Delete Data View] página, clique em **Excluir**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Exibição de uma exibição de dados {#task_FD0D2CE53DF84CBD9220AD7CA920011F}

Você pode usar [!DNL View] na [!DNL Data Views] página para exibir uma exibição de dados selecionada.

A exibição de dados selecionada é aberta em uma janela separada do navegador.

**Para exibir uma exibição de dados**

1. No menu do produto, clique em **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Execute um dos procedimentos a seguir:

   * Na [!DNL Data Views] página, na [!DNL Title] coluna da tabela, clique no nome de uma exibição de dados que deseja abrir.

   * Na [!DNL Data Views] página, na [!DNL Actions] coluna da tabela, clique **[!UICONTROL View]** na linha com a exibição de dados que deseja abrir.

