---
description: Use o menu do Adobe Analytics para configurar a autenticação das métricas do Adobe Analytics, gerenciar as métricas do Adobe Analytics de um conjunto de relatórios ou usar o SAINT para aprimorar os relatórios do Adobe Analytics por meio da aceitação de dados tabulares de fontes externas.
seo-description: Use o menu do Adobe Analytics para configurar a autenticação das métricas do Adobe Analytics, gerenciar as métricas do Adobe Analytics de um conjunto de relatórios ou usar o SAINT para aprimorar os relatórios do Adobe Analytics por meio da aceitação de dados tabulares de fontes externas.
seo-title: Sobre o menu do Adobe Analytics
solution: Target
subtopic: Adobe Analytics
title: Sobre o menu do Adobe Analytics
topic: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Sobre o menu do Adobe Analytics{#about-the-adobe-analytics-menu}

Use o menu do Adobe Analytics para configurar a autenticação das métricas do Adobe Analytics, gerenciar as métricas do Adobe Analytics de um conjunto de relatórios ou usar o SAINT para aprimorar os relatórios do Adobe Analytics por meio da aceitação de dados tabulares de fontes externas.

## Configuração da autenticação de métricas do Adobe Analytics {#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Para incorporar métricas do Adobe Analytics às classificações de pesquisa/comercialização do site, primeiro você deve obter um logon dos Serviços da Web do Adobe Analytics. Depois de obter as informações de logon, você pode usá-las para configurar a autenticação do Adobe Analytics na pesquisa/comercialização do site.

**Para configurar a autenticação das métricas do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Authentication]**.
1. Na [!DNL Setup Adobe Analytics Metrics Authentication] página, especifique as informações solicitadas em cada campo.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Campo de texto </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome da empresa do Adobe Analytics </p> </td> 
      <td colname="col2"> <p>A mesma configuração de Nome da empresa usada para fazer logon em sua conta do Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome de usuário dos Serviços da Web </p> </td> 
      <td colname="col2"> <p>O nome de usuário dos serviços da Web associado à sua conta do Adobe Analytics. </p> <p>Você pode obter essas informações no Adobe Analytics. Na barra de menus do Adobe Analytics, clique em <span class="uicontrol"> Admin <b>&gt;</b> Console </span> de <span class="uicontrol"> administração <b>&gt;</b> Empresa &gt; </span> <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> <b></b> </span>Serviços Web. As informações estão na tabela Informações de acesso à API. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Segredo Compartilhado dos Serviços Web </p> </td> 
      <td colname="col2"> <p>O segredo compartilhado dos serviços da Web que está associado à sua conta do Adobe Analytics. </p> <p>Você pode obter essas informações no Adobe Analytics. Na barra de menus do Adobe Analytics, clique em <span class="uicontrol"> Admin <b>&gt;</b> Console </span> de <span class="uicontrol"> administração <b>&gt;</b> Empresa &gt; </span> <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> <b></b> </span>Serviços Web. As informações estão na tabela Informações de acesso à API. </p> </td> 
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

## Sobre os conjuntos de relatórios do Adobe Analytics {#concept_1A51AEC5D40E459B813E7891D64B1BAE}

Para usar os dados do Conjunto de relatórios do Adobe Analytics na pesquisa/comercialização do site, é necessário primeiro criar cópias dos dados do Adobe Analytics na sua conta de pesquisa/comercialização do site.

Você pode criar novas definições do Conjunto de relatórios do Adobe Analytics ou exibir ou modificar os Conjuntos de relatórios do Adobe Analytics e as métricas associadas existentes.

Na primeira vez que você acessa o Adobe Analytics a partir da pesquisa/comercialização do site, uma lista dos Report Suites disponíveis da sua empresa é baixada e armazenada em cache. Se os novos conjuntos de relatórios tiverem sido adicionados recentemente ou se os existentes tiverem sido removidos, você poderá atualizar a lista de conjuntos de relatórios para baixar novamente a lista de conjuntos de relatórios.

## Adicionar um conjunto de relatórios do Adobe Analytics {#task_6DE17305EA7146DA8C30FF8FDF68A3C0}

Você pode selecionar um Conjunto de relatórios do Adobe Analytics no qual basear as regras de classificação de comercialização/pesquisa do site.

A lista que você pode selecionar deve corresponder aos Report Suites que estão disponíveis na sua conta do Adobe Analytics. O Conjunto de relatórios selecionado determina as métricas que estão disponíveis para uso nas Regras de classificação de pesquisa/comercialização do site.

Consulte [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Depois de adicionar um Conjunto de relatórios do Adobe Analytics, é possível editar suas métricas.

Consulte [Editar as métricas do Adobe Analytics de um Conjunto](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)de relatórios.

**Para adicionar um conjunto de relatórios do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na página Report Suites do Adobe Analytics, clique em **[!UICONTROL Add Report Suite]**.
1. Na lista suspensa da linha de tabela recém-adicionada, selecione o Conjunto de relatórios desejado.
1. Edite as métricas do Adobe Analytics de um Conjunto de relatórios.

## Editar as métricas do Adobe Analytics de um conjunto de relatórios {#task_360904CCBBB140238ADA036C3CC07664}

Para incorporar métricas do Adobe Analytics às Regras de classificação na pesquisa/comercialização do site, selecione uma ou mais métricas associadas ao Conjunto de relatórios escolhido. Em seguida, você configura as opções usadas para buscar dados de métrica por meio do Adobe Analytics Web Service.

Consulte [Adicionar um conjunto](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)de relatórios do Adobe Analytics.

Consulte [Configuração de opções](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19)avançadas do Adobe Analytics.

**Para editar as métricas do Adobe Analytics de um conjunto de relatórios**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na [!DNL Adobe Analytics Report Suites] página, na **[!UICONTROL Actions]** coluna, clique **[!UICONTROL Edit]** no Conjunto de relatórios cujas métricas você deseja configurar.
1. Na [!DNL Edit Adobe Analytics Metrics] página, defina as métricas necessárias. As métricas que não têm um asterisco (*) ao lado do nome da métrica são opcionais.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Conjunto de relatórios </p> </td> 
      <td colname="col2"> <p>Exibe o nome do conjunto de relatórios que você adicionou no momento. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome de exibição do conjunto de relatórios </p> </td> 
      <td colname="col2"> <p>Fornece um nome de "alias" para o nome do Conjunto de relatórios do Adobe Analytics. Esse nome alternativo é útil se o mesmo Conjunto de relatórios for usado em mais de uma definição. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Selecionar Tipo de relatório </p> </td> 
      <td colname="col2"> <p>Especifica o valor Tipo de relatório a ser usado com o Conjunto de relatórios selecionado. O valor identifica a chave para cada linha de resultados retornada. </p> <p>O Tipo de relatório também é conhecido como o Elemento do Adobe Analytics. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do campo de referência cruzada </p> </td> 
      <td colname="col2"> <p>Especifica um campo de metadados cujos valores são usados como "chaves" de pesquisa nos dados do Conjunto de relatórios. </p> <p>Se nenhum valor for selecionado ("— Nenhum —"), os dados deste Conjunto de relatórios não estarão disponíveis para uso em cálculos de classificação ( <span class="uicontrol"> Regras <b></b> &gt; Regras </span> de <span class="uicontrol"> classificação <b>&gt;</b> </span> <span class="uicontrol"> <b></b> </span>Editar regras). </p> <p>Quando você seleciona um valor, os valores desse campo são usados para fazer referência cruzada aos documentos de pesquisa/comercialização do site com os dados do Adobe Analytics desse conjunto de relatórios, usando o valor do Tipo de relatório selecionado definido anteriormente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Relatório de termos de pesquisa </p> </td> 
      <td colname="col2"> <p>Fornece acesso para criar regras de negócios e simular termos de pesquisa na página Visualização <b>de dados do</b> Stage Adobe Analytics. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Visualização de dados</a>do Adobe Analytics. </p> <p>Um menu suspenso é exibido em cada linha que inclui duas opções: <b>Simular o termo</b> de pesquisa e <b>Criar nova regra</b>de negócios. </p> <p>Ambas as opções usam dados do Tipo de relatório como termos de pesquisa. Portanto, esse recurso só faz sentido se o Tipo de relatório representa termos de pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Métricas </p> </td> 
      <td colname="col2"> <p>Identifica os valores de métrica que você deseja baixar e usar nas Regras de classificação de pesquisa/comercialização do site. </p> <p>As métricas que você configura aqui aparecem como opções nas páginas do centro de membros <span class="uicontrol"> Regras <b></b> &gt; Regras </span> de <span class="uicontrol"> classificação <b>&gt;</b> </span> <span class="uicontrol"> <b></b> </span> <span class="uicontrol"> </span>Editar regras, quando o Tipo de dados da regra é definido como Métrica do Adobe Analytics (Número) de participantes. As opções mostram uma combinação dos nomes do Conjunto de relatórios ou dos Nomes de exibição do Conjunto de relatórios, se especificados, e os nomes de métricas individuais. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor Mínimo da Métrica </p> </td> 
      <td colname="col2"> <p>Permite inserir um valor diferente de zero para especificar um valor mínimo para a métrica. </p> <p>Se estiver em branco, ou se for zero, todos os valores da métrica serão baixados; caso contrário, o download dessa métrica será interrompido quando o valor mínimo da métrica for transmitido. </p> <p>As métricas do Adobe Analytics são recuperadas em ordem decrescente. </p> <p>Clique em <span class="uicontrol"> <b>+</b> </span> para adicionar outras definições de métricas. clique <span class="uicontrol"> - <b></b> </span> para remover as definições de métricas que não são mais necessárias ou desejadas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Período de agregação de métrica do Adobe Analytics (Dias) </p> </td> 
      <td colname="col2"> <p> Controla o número de dias que as métricas do Adobe Analytics devem recuperar, contando a partir da data de ontem. Nenhuma tentativa é feita para buscar dados do dia atual. </p> <p>O padrão é 7. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frequência de atualização de download do Adobe Analytics (dias) </p> </td> 
      <td colname="col2"> <p> Define o intervalo mínimo entre downloads de dados do Adobe Analytics usados em cálculos de classificação. </p> <p>Os downloads acionados por índice que ocorrem dentro do intervalo de frequência de atualização do download são ignorados. No entanto, os downloads manuais ignoram esse valor. </p> <p>Quando você define esse valor como padrão de 1, os dados do Adobe Analytics não baixam mais de uma vez em um período de 24 horas. Todos os índices de pesquisa que ocorrem dentro do intervalo de frequência de atualização de download usam o último conjunto de dados que foi baixado. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   See also [About Ranking Rules](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).
1. Clique em **[!UICONTROL Save Changes]**.

   Você é retornado para a [!DNL Adobe Analytics Report Suites] página Preparado.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo um conjunto de relatórios do Adobe Analytics {#task_0ACA172214D14654ABDB139F417B9F7D}

Você pode usar Excluir para remover um Report Suite da [!DNL Adobe Analytics Report Suites] página. A exclusão de um conjunto de relatórios remove apenas a cópia dos dados dos servidores de pesquisa/comercialização do site; não afeta os dados nos sistemas do Adobe Analytics.

**Para excluir um conjunto de relatórios do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na [!DNL Adobe Analytics Report Suites] página, na **[!UICONTROL Actions]** coluna, clique **[!UICONTROL Delete]** no Conjunto de relatórios que deseja remover.
1. Na [!DNL Adobe Analytics Delete Report Suite] página, clique em **[!UICONTROL Delete]**.

## Visualização de dados do Adobe Analytics {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Você pode usar Visualizar para exibir as métricas carregadas mais recentemente do Adobe Analytics.

A coluna Linha na tabela mostra o número de cada linha de dados de métrica, indicando a ordem original em que as métricas do Adobe Analytics foram carregadas.

A coluna Produto mostra o Elemento do Adobe Analytics associado a cada linha de dados de métrica. Os valores nesta coluna são usados para associar as páginas de pesquisa/comercialização do site aos valores de métrica correspondentes, conforme configurado nas definições de classificação.

Consulte [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

As colunas restantes mostram os valores de métrica associados a cada entrada.

Se a tabela estiver vazia, isso significa que você ainda não carregou nenhum dado do Adobe Analytics. Você pode fechar a [!DNL Adobe Analytics Data Preview] página e carregar os dados do Adobe Analytics.

Consulte [Carregamento de dados](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)do Adobe Analytics.
Se a tabela foi designada como um relatório de termo de pesquisa, um pequeno triângulo aparecerá em cada linha. Você pode clicar na lista suspensa e selecionar **Simular termo** de pesquisa ou **Criar nova regra** comercial. A ação selecionada é aplicada ao termo de pesquisa dessa linha, os dados que residem na segunda coluna

**Para visualizar os dados do Adobe Analytics**

1. No menu do produto, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**. Na [!DNL Adobe Analytics Report Suites] página, na [!DNL Actions] coluna, clique **[!UICONTROL Preview]** no Conjunto de relatórios cujos dados baixados você deseja visualizar.

   * Clique em **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. Na [!DNL Adobe Analytics Terms Report] página, na [!DNL Actions] coluna, clique **[!UICONTROL Preview]** no Conjunto de relatórios cujos dados baixados você deseja visualizar.

1. Na [!DNL Adobe Analytics Data Preview] página, use as opções de navegação e exibição na parte superior e inferior da página para exibir os dados.

   Clique em qualquer cabeçalho de coluna na tabela para classificar os dados em ordem crescente ou decrescente.
1. Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL Download to Desktop]** para baixar e salvar a tabela como um `.xlt` arquivo.

   * Feche a página quando terminar de visualizar os dados do Adobe Analytics e retornar à página visualizada anteriormente.

## Como visualizar o log a partir do carregamento de dados mais recente do Adobe Analytics {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Você pode usar Exibir log para examinar o arquivo de log de dados do Adobe Analytics do processo de download mais recente. Você também pode usar a exibição de log para monitorar um download em execução.

Consulte [Carregamento de dados](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)do Adobe Analytics.

**Para exibir o log a partir do carregamento de dados mais recente do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na [!DNL Adobe Analytics Report Suites] página, clique em **[!UICONTROL View Log]**. página de registro,
1. Na [!DNL Adobe Analytics Data Log] página, use as opções de navegação e exibição na parte superior e inferior da página para exibir as informações do log.
1. Quando terminar, feche a página para retornar à [!DNL Adobe Analytics Report Suites] página.

## Carregamento de dados do Adobe Analytics {#task_2F3C55189B0A4049AB2113F2291CC181}

Você pode baixar os dados configurados do Conjunto de relatórios do Adobe Analytics na pesquisa/comercialização do site.

A página Carregamento de dados mostra o status da última operação de Carregamento de dados do Adobe Analytics com as seguintes informações:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Campo Status </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> <p>Indica o sucesso ou a falha da última tentativa de carregamento de dados. Ou exibe o status de uma operação de carregamento de dados que já está em andamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Resultados </p> </td> 
   <td colname="col2"> <p>Exibe o número de linhas de dados de métrica que foram baixadas durante a última tentativa de carregamento de dados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora inicial </p> </td> 
   <td colname="col2"> <p>Exibe a data e a hora em que a última operação de carregamento de dados foi iniciada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora de Parada </p> </td> 
   <td colname="col2"> <p>Exibe a data e a hora de conclusão da última operação de carregamento de dados. Ou indica que a operação de carregamento de dados atual ainda está em andamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Para carregar dados do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na [!DNL Stage Adobe Analytics Report Suites] página, clique em **[!UICONTROL Load Adobe Analytics Data]**.
1. Na **[!UICONTROL Adobe Analytics Data Load]** página, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Start Load]** para iniciar a operação de carregamento.

      Durante uma operação de carregamento de dados, a linha **Andamento** fornece informações sobre seu progresso.

   * Clique em **[!UICONTROL Stop Load]** para interromper a operação de carregamento.

1. Clique em **[!UICONTROL Close]** para retornar à [!DNL Stage Adobe Analytics Reports Suite] página.

## Atualização da lista de Report Suites {#task_EA6215D438CA4185B106657D9712ED34}

Na primeira vez que você acessa o Adobe Analytics na interface de usuário de pesquisa/comercialização do site, uma lista dos Conjuntos de relatórios disponíveis do Adobe Analytics da sua empresa é baixada e armazenada em cache. Se os novos Conjuntos de relatórios foram adicionados recentemente ou os existentes foram excluídos, você pode usar Atualizar a Lista de conjuntos de relatórios para atualizar a lista exibida no momento na pesquisa/comercialização do site.

Consulte [Adicionar um conjunto](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0)de relatórios do Adobe Analytics.

Consulte [Excluindo um conjunto](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D)de relatórios do Adobe Analytics.

**Para atualizar a lista de Report Suites**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na [!DNL Adobe Analytics Report Suites] página, clique em **[!UICONTROL Refresh Report Suite List]**.

## Configuração de opções avançadas do Adobe Analytics {#task_C0FF2D69F59D44D8943A7831ED7FEC19}

Você pode usar [!DNL Advanced Adobe Analytics Options] para controlar as configurações destinadas a ajudar a ajustar o comportamento do processo de download do Conjunto de relatórios do Adobe Analytics.

Consulte [Editar as métricas do Adobe Analytics de um Conjunto](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)de relatórios.

**Para configurar opções avançadas do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Advanced Options]**.
1. Na [!DNL Advanced Adobe Analytics Options] página, defina as seguintes opções:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Linhas máximas, qualquer métrica </p> </td> 
      <td colname="col2"> <p>Uma configuração de otimização que impede o download de muitos dados do Adobe Analytics. </p> <p>Se você definir essa opção para um valor diferente de zero, a busca de dados do Adobe Analytics será interrompida quando o número total de linhas buscadas para cada métrica exceder o valor especificado. </p> <p>O valor padrão é 0; nenhum valor máximo aplicado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tamanho da busca repetida da métrica (linhas) </p> </td> 
      <td colname="col2"> <p> Controla o número de valores de métrica do Adobe Analytics a serem obtidos por vez. As linhas de dados de métrica são repetidamente buscadas até que todos os dados sejam recuperados ou até que o limite máximo de linhas seja atingido. </p> <p>Normalmente, não é necessário alterar essa configuração. No entanto, você pode achar útil otimizar a fase de download da métrica de um reíndice completo do seu site. </p> <p>O valor padrão é 5000. </p> </td> 
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

## Sobre feeds de classificação SAINT {#concept_C55609DA24914BBC92CD90ED0259199D}

Você pode usar o Adobe Analytics SAINT para aprimorar seus relatórios de análise por meio da aceitação de dados tabulares de fontes externas. Por exemplo, você pode usar a pesquisa/comercialização do site para recuperar os dados de seus próprios índices e exportar esses dados para o Adobe Analytics.

Para usar com êxito o recurso SAINT do Adobe Analytics na pesquisa/comercialização do site, esteja ciente dos seguintes requisitos:

* Você deve ter uma empresa do Adobe Analytics e um Conjunto de relatórios.

   Consulte [Sobre o menu](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411)do Adobe Analytics.
* A conta de usuário do Adobe Analytics deve ter privilégios para modificar o Conjunto de relatórios.

   Consulte [Configuração da autenticação](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42)de métricas do Adobe Analytics.
* O usuário do Adobe Analytics deve pertencer ao grupo da API da Web para que possa usar a API da Web do Adobe Analytics.
* O índice de pesquisa deve ter dados que o Adobe Analytics pode usar, como dados no formato correto.

Antes de criar um feed, reveja as seguintes perguntas e informações para que você possa concluir o assistente de feed SAINT com êxito:

* Com qual conjunto de relatórios você vai trabalhar?
* Para qual conjunto de classificações, como produto, e-var e assim por diante, você fornecerá dados?
* Quais classificações existem nos relatórios? A resposta a essa pergunta é determinada pelo tipo de dados que está prontamente disponível na pesquisa/comercialização do site e pelo tipo de relatórios que o Adobe Analytics relata como desejáveis.
* O SAINT aceita os dados de pesquisa/comercialização do site como um tipo de texto. O formato desses dados afeta a apresentação dos relatórios do Adobe Analytics.

## Criação de um feed SAINT do Adobe Analytics {#task_914B5AB821E84627953D8EF9339A7DD0}

Você pode usar o Adobe Analytics SAINT para aprimorar os relatórios do Adobe Analytics por meio da aceitação de dados tabulares de fontes externas.

Por exemplo, você pode usar a pesquisa/comercialização do site para recuperar dados de seus próprios índices e exportar esses dados para o Adobe Analytics.

**Para criar um feed SAINT do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na [!DNL SAINT Classification Feeds] página, clique em **[!UICONTROL Create SAINT Feed]**.
1. Na caixa de diálogo [!DNL Create Feed] , no campo de texto Nome **do** feed, digite o novo nome do feed e clique em **[!UICONTROL Next]**.

   Nesse ponto, o feed é salvo e adicionado à [!DNL SAINT Classification Feed] página. Se você escolher, poderá sair e editar o feed mais tarde para concluir o assistente.
1. Na [!DNL Authentication] página, especifique o nome da empresa, o nome de usuário e o segredo da Web do Adobe Analytics nos respectivos campos de texto e clique em **[!UICONTROL Next]**.

   Certifique-se de que esteja autorizado a usar a API da Web com o Adobe Analytics.
1. Na **[!UICONTROL Report Suite]** página, escolha um conjunto de relatórios e seu conjunto de dados de classificação e clique em **[!UICONTROL Next]**.
1. Na [!DNL Field Maps] página, mapeie as classificações do Adobe Analytics com os campos de metadados de pesquisa/comercialização do site e clique em **[!UICONTROL Next]**.

   Para ajustar as classificações do Adobe Analytics, clique em Classificações **[!UICONTROL Edit]** do Adobe Analytics para fazer logon no Adobe Analytics. Quando terminar de fazer as alterações, clique em **[!UICONTROL Refresh Classifications]** para atualizar as opções de classificações.
1. Na [!DNL Search Criteria] página, os dados da pesquisa/comercialização do site podem ser filtrados antes de serem enviados ao SAINT do Adobe Analytics. Construa regras de filtro aqui usando a interface do construtor de regras e clique em **[!UICONTROL Next]**.
1. Na [!DNL Configure FTP] página, selecione o servidor FTP. Especifique a frequência de carregamento dos dados e clique em **[!UICONTROL Next]**.

   Como prática recomendada, cada feed tem sua própria conta FTP para evitar a perda acidental de dados. Você pode criar uma nova conta FTP do Adobe Analytics aqui.
1. Na [!DNL Verification] página, clique **[!UICONTROL Show Data View]** para revisar a representação da exibição de dados da saída. Se houver algum arquivo de feed real, eles serão listados aqui e estarão disponíveis para download.
1. Clique em **[!UICONTROL Close]**.

## Editar um feed SAINT do Adobe Analytics {#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

Você pode editar todos os aspectos de um feed SAINT existente que você tenha criado.

**Para editar um feed SAINT do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na [!DNL Saint Classification Feeds] página, na **[!UICONTROL Name]** coluna, na lista suspensa ao lado de um feed, clique em **[!UICONTROL Edit feed]**.
1. Na caixa de diálogo do feed SAINT, no campo de texto Nome **do** feed, digite o novo nome do feed e clique em **[!UICONTROL Next]**.

   Nesse ponto, o feed é salvo e adicionado à [!DNL SAINT Classification Feed] página. Se você escolher, poderá sair e editar o feed mais tarde para concluir o assistente.
1. Na [!DNL Authentication] página, especifique o nome da empresa, o nome de usuário e o segredo da Web do Adobe Analytics nos respectivos campos de texto e clique em **[!UICONTROL Next]**.

   Certifique-se de que esteja autorizado a usar a API da Web com o Adobe Analytics.
1. Na **[!UICONTROL Report Suite]** página, escolha um conjunto de relatórios e seu conjunto de dados de classificação e clique em **[!UICONTROL Next]**.
1. Na [!DNL Field Maps] página, mapeie as classificações do Adobe Analytics com os campos de metadados de pesquisa/comercialização do site e clique em **[!UICONTROL Next]**.

   Para ajustar as classificações do Adobe Analytics, clique em Classificações **[!UICONTROL Edit]** do Adobe Analytics para fazer logon no Adobe Analytics. Quando terminar de fazer as alterações, clique em **[!UICONTROL Refresh Classifications]** para atualizar as opções de classificações.
1. Na [!DNL Search Criteria] página, os dados da pesquisa/comercialização do site podem ser filtrados antes de serem enviados ao SAINT do Adobe Analytics. Construa regras de filtro aqui usando a interface do construtor de regras e clique em **[!UICONTROL Next]**.
1. Na [!DNL Configure FTP] página, selecione o servidor FTP. Especifique a frequência de carregamento dos dados e clique em **[!UICONTROL Next]**.

   Como prática recomendada, cada feed tem sua própria conta FTP para evitar a perda acidental de dados. Você pode criar uma nova conta FTP do Adobe Analytics aqui.
1. Na [!DNL Verification] página, clique **[!UICONTROL Show Data View]** para revisar a representação da exibição de dados da saída. Se houver algum arquivo de feed real, eles serão listados aqui e estarão disponíveis para download.
1. Clique em **[!UICONTROL Close]**.

## Excluindo um feed SAINT do Adobe Analytics {#task_5319B1F4CA1A406393CFD7AE97258CEB}

Você pode excluir um feed SAINT existente do Adobe Analytics que não é mais necessário ou usado.

**Para excluir um feed SAINT do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na [!DNL Saint Classification Feeds] página, na **[!UICONTROL Name]** coluna, na lista suspensa ao lado de um feed que você deseja remover, clique em **[!UICONTROL Delete feed]**.
1. Na caixa de diálogo Excluir, clique em **Sim** para verificar a exclusão do feed.

## Exibição de um arquivo de feed SAINT do Adobe Analytics {#task_F0C8BADD25E14E5DB30BF31D1F879FDB}

Você pode abrir a [!DNL Verification] página de um feed SAINT existente para revisar a representação da exibição de dados da saída.

Se houver algum arquivo de feed real, eles serão listados aqui e estarão disponíveis para download como um arquivo de texto.

**Para exibir um arquivo de feed SAINT do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na [!DNL Saint Classification Feeds] página, na **[!UICONTROL Name]** coluna, na lista suspensa ao lado de um feed, clique em **[!UICONTROL View Feed Files]**.
1. (Opcional) Clique em **[!UICONTROL Download File]** para salvar o arquivo de feed como um arquivo de texto.
1. Clique em **[!UICONTROL Close]** para retornar à [!DNL SAINT Classification Feeds] página.

## Teste de um feed SAINT do Adobe Analytics {#task_9864D69BE3824FC29C10B36EE4855D25}

Você pode testar um feed SAINT do Adobe Analytics existente sem upload de arquivo.

Consulte [Geração e upload de um feed](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A)SAINT do Adobe Analytics.

Consulte [Visualização de um arquivo](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)de feed SAINT do Adobe Analytics.

**Para testar um arquivo de feed SAINT do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na [!DNL Saint Classification Feeds] página, na **[!UICONTROL Name]** coluna, na lista suspensa ao lado de um feed, clique em **[!UICONTROL Test Feed (No file upload)]**.
1. Quando o feed terminar de processar, na lista suspensa do nome do feed, clique em **[!UICONTROL View Feed Files]**.
1. Na [!DNL Verification] página, clique **[!UICONTROL Download File]** para baixar o arquivo de feed.
1. Clique em **[!UICONTROL Close]** para retornar à [!DNL SAINT Classification Feeds] página.

## Geração e upload de um feed SAINT do Adobe Analytics {#task_47AED946AA964334A877FDC8D4F6F00A}

Você pode gerar e carregar arquivos de feed para um feed existente do Adobe Analytics que você criou.

Consulte [Testando um feed](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25)SAINT do Adobe Analytics.

Consulte [Visualização de um arquivo](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB)de feed SAINT do Adobe Analytics.

**Para gerar e carregar um arquivo de feed SAINT do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na [!DNL Saint Classification Feeds] página, na **[!UICONTROL Name]** coluna, na lista suspensa ao lado de um feed, clique em **[!UICONTROL Generate and Upload Feed]**.
1. Quando o feed terminar de processar, na lista suspensa do nome do feed, clique em **[!UICONTROL View Feed Files]**.
1. Na [!DNL Verification] página, clique **[!UICONTROL Download File]** para baixar o arquivo de feed.
1. Clique em **[!UICONTROL Close]** para retornar à [!DNL SAINT Classification Feeds] página.
