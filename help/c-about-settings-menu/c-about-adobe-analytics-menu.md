---
description: Use o menu Adobe Analytics para configurar a autenticação das métricas do Adobe Analytics, gerenciar as métricas do Adobe Analytics de um Conjunto de relatórios ou usar o SAINT para aprimorar os relatórios do Adobe Analytics através da aceitação de dados tabulares de fontes externas.
seo-description: Use o menu Adobe Analytics para configurar a autenticação das métricas do Adobe Analytics, gerenciar as métricas do Adobe Analytics de um Conjunto de relatórios ou usar o SAINT para aprimorar os relatórios do Adobe Analytics através da aceitação de dados tabulares de fontes externas.
seo-title: Sobre o menu Adobe Analytics
solution: Target
subtopic: Adobe Analytics
title: Sobre o menu Adobe Analytics
topic: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '3448'
ht-degree: 1%

---


# Sobre o menu Adobe Analytics{#about-the-adobe-analytics-menu}

Use o menu Adobe Analytics para configurar a autenticação das métricas do Adobe Analytics, gerenciar as métricas do Adobe Analytics de um Conjunto de relatórios ou usar o SAINT para aprimorar os relatórios do Adobe Analytics através da aceitação de dados tabulares de fontes externas.

## Configuração da autenticação de métricas do Adobe Analytics {#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Para incorporar métricas da Adobe Analytics às classificações de pesquisa/comercialização do site, primeiro você deve obter um logon dos Serviços da Web da Adobe Analytics. Depois de obter as informações de logon, você pode usá-las para configurar a autenticação do Adobe Analytics na pesquisa/comercialização do site.

**Para configurar a autenticação das métricas do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Authentication]**.
1. Na página [!DNL Setup Adobe Analytics Metrics Authentication], especifique as informações solicitadas em cada campo.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Campo de texto </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome da Empresa Adobe Analytics </p> </td> 
      <td colname="col2"> <p>A mesma configuração de Nome de Empresa usada para fazer logon em sua conta Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome de usuário dos Serviços da Web </p> </td> 
      <td colname="col2"> <p>O nome de usuário dos Serviços Web associado à sua conta Adobe Analytics. </p> <p>Você pode obter essas informações no Adobe Analytics. Na barra de menus do Adobe Analytics, clique em <span class="uicontrol"> <b>Admin</b> </span> &gt; <span class="uicontrol"> <b>Admin Console</b> </span> &gt; <span class="uicontrol"> <b>Empresa</b> </span> &gt; <span class="uicontrol"> <b>Serviços da Web</b> </span>. As informações estão na tabela Informações de acesso à API. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Segredo Compartilhado dos Serviços Web </p> </td> 
      <td colname="col2"> <p>O Segredo Compartilhado dos Serviços Web que está associado à sua conta Adobe Analytics. </p> <p>Você pode obter essas informações no Adobe Analytics. Na barra de menus do Adobe Analytics, clique em <span class="uicontrol"> <b>Admin</b> </span> &gt; <span class="uicontrol"> <b>Admin Console</b> </span> &gt; <span class="uicontrol"> <b>Empresa</b> </span> &gt; <span class="uicontrol"> <b>Serviços da Web</b> </span>. As informações estão na tabela Informações de acesso à API. </p> </td> 
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

## Sobre os conjuntos de relatórios da Adobe Analytics {#concept_1A51AEC5D40E459B813E7891D64B1BAE}

Para usar os dados do Conjunto de relatórios da Adobe Analytics na pesquisa/comercialização do site, é necessário primeiro criar cópias dos dados da Adobe Analytics na sua conta de pesquisa/comercialização do site.

Você pode criar novas definições de Conjunto de relatórios da Adobe Analytics ou visualização ou modificar seus Conjuntos de relatórios da Adobe Analytics e métricas associadas existentes.

Na primeira vez que você acessa o Adobe Analytics a partir da pesquisa/comercialização do site, uma lista dos Report Suites disponíveis para empresa é baixada e armazenada em cache. Se os novos conjuntos de relatórios tiverem sido adicionados recentemente ou se os existentes tiverem sido removidos, você poderá atualizar a lista do conjunto de relatórios para baixar novamente a lista dos conjuntos de relatórios.

## Adicionar um conjunto de relatórios da Adobe Analytics {#task_6DE17305EA7146DA8C30FF8FDF68A3C0}

Você pode selecionar um Conjunto de relatórios da Adobe Analytics no qual basear as regras de classificação de pesquisa/comercialização do site.

A lista que você pode selecionar deve corresponder aos Report Suites que estão disponíveis em sua conta Adobe Analytics. O Conjunto de relatórios selecionado determina as métricas que estão disponíveis para uso nas Regras de classificação de pesquisa/comercialização do site.

Consulte [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Após adicionar um Conjunto de relatórios da Adobe Analytics, é possível editar suas métricas.

Consulte [Editar as métricas do Adobe Analytics de um Report Suite](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**Para adicionar um conjunto de relatórios da Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na página Report Suites da Adobe Analytics, clique em **[!UICONTROL Add Report Suite]**.
1. Na lista suspensa da linha de tabela recém-adicionada, selecione o Conjunto de relatórios desejado.
1. Edite as métricas do Adobe Analytics de um Conjunto de relatórios.

## Editar as métricas do Adobe Analytics de um Conjunto de relatórios {#task_360904CCBBB140238ADA036C3CC07664}

Para incorporar métricas do Adobe Analytics às Regras de classificação na pesquisa/comercialização do site, selecione uma ou mais métricas associadas ao Conjunto de relatórios escolhido. Em seguida, você configura as opções usadas para buscar dados de métrica por meio do Adobe Analytics Web Service.

Consulte [Adicionar um conjunto de relatórios da Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

Consulte [Configuração de opções avançadas do Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19).

**Para editar as métricas do Adobe Analytics de um conjunto de relatórios**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na página [!DNL Adobe Analytics Report Suites], na coluna **[!UICONTROL Actions]**, clique em **[!UICONTROL Edit]** para o Conjunto de relatórios cujas métricas você deseja configurar.
1. Na página [!DNL Edit Adobe Analytics Metrics], defina as métricas necessárias. As métricas que não têm um asterisco (*) ao lado do nome da métrica são opcionais.

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
      <td colname="col1"> <p>Nome da Visualização do conjunto de relatórios </p> </td> 
      <td colname="col2"> <p>Fornece um nome "alias" para o nome do Conjunto de relatórios da Adobe Analytics. Esse nome alternativo é útil se o mesmo Conjunto de relatórios for usado em mais de uma definição. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Selecionar Tipo de relatório </p> </td> 
      <td colname="col2"> <p>Especifica o valor Tipo de relatório a ser usado com o Conjunto de relatórios selecionado. O valor identifica a chave para cada linha de resultados retornada. </p> <p>O Tipo de relatório também é conhecido como Elemento Adobe Analytics. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do campo de referência cruzada </p> </td> 
      <td colname="col2"> <p>Especifica um campo de metadados cujos valores são usados como "chaves" de pesquisa nos dados do Conjunto de relatórios. </p> <p>Se nenhum valor for selecionado ("— Nenhum —"), os dados deste Conjunto de relatórios não estarão disponíveis para uso em cálculos de classificação ( <span class="uicontrol"> <b>Regras</b> </span> &gt; <span class="uicontrol"> <b>Regras de classificação</b> </span> &gt; <span class="uicontrol"> <b>Editar regras</b> &lt;a1 1/&gt;).</span> </p> <p>Quando você seleciona um valor, os valores desse campo são usados para fazer referência cruzada aos documentos de pesquisa/comercialização do site com os dados Adobe Analytics deste Conjunto de relatórios, usando o valor Tipo de relatório selecionado definido anteriormente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Relatório de termos de pesquisa </p> </td> 
      <td colname="col2"> <p>Fornece acesso para criar regras de negócios e simular termos de pesquisa na página <b>Pré-visualização de dados do Adobe Analytics de estágio</b>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Pré-visualização de Dados Adobe Analytics</a>. </p> <p>Um menu suspenso é exibido em cada linha que inclui duas opções: <b>Simular Termo de Pesquisa</b> e <b>Criar Nova Regra de Negócios</b>. </p> <p>Ambas as opções usam dados do Tipo de relatório como termos de pesquisa. Portanto, esse recurso só faz sentido se o Tipo de relatório representa termos de pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Métricas </p> </td> 
      <td colname="col2"> <p>Identifica os valores de métrica que você deseja baixar e usar nas Regras de classificação de pesquisa/comercialização do site. </p> <p>As métricas que você configura aqui aparecem como opções nas <span class="uicontrol"> <b>Regras</b> </span> &gt; <span class="uicontrol"> <b>Regras de classificação</b> </span> &gt; <span class="uicontrol"> <b>Editar regras</b> </span> páginas do centro membro, quando o Tipo de dados da regra está definido como <span class="uicontrol"> Métrica Adobe Analytics (Número) </span>. As opções mostram uma combinação dos nomes do Conjunto de relatórios ou dos Nomes de Visualização do Conjunto de relatórios, se especificado, e os nomes de métricas individuais. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor Mínimo da Métrica </p> </td> 
      <td colname="col2"> <p>Permite inserir um valor diferente de zero para especificar um valor mínimo para a métrica. </p> <p>Se estiver em branco, ou se for zero, todos os valores da métrica serão baixados; caso contrário, o download dessa métrica será interrompido quando o valor mínimo da métrica for transmitido. </p> <p>As métricas do Adobe Analytics são recuperadas em ordem decrescente. </p> <p>Clique em <span class="uicontrol"> <b>+</b> </span> para adicionar definições de métricas adicionais; clique em <span class="uicontrol"> <b>-</b> </span> para remover as definições de métricas que não são mais necessárias ou desejadas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Período de agregação de métrica do Adobe Analytics (Dias) </p> </td> 
      <td colname="col2"> <p> Controla o número de dias que as métricas do Adobe Analytics valem para buscar, contando a partir da data de ontem. Nenhuma tentativa é feita para buscar dados do dia atual. </p> <p>O padrão é 7. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frequência de Atualização de Download da Adobe Analytics (Dias) </p> </td> 
      <td colname="col2"> <p> Define o intervalo mínimo entre downloads de dados do Adobe Analytics usados em cálculos de classificação. </p> <p>Os downloads acionados por índice que ocorrem dentro do intervalo de frequência de atualização do download são ignorados. No entanto, os downloads manuais ignoram esse valor. </p> <p>Quando você define esse valor como padrão de 1, os dados da Adobe Analytics não baixam mais de uma vez em um período de 24 horas. Todos os índices de pesquisa que ocorrem dentro do intervalo de frequência de atualização de download usam o último conjunto de dados que foi baixado. </p> <p>Essa métrica é necessária. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Consulte também [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).
1. Clique em **[!UICONTROL Save Changes]**.

   Você é retornado para a página Preparado [!DNL Adobe Analytics Report Suites].
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo um conjunto de relatórios da Adobe Analytics {#task_0ACA172214D14654ABDB139F417B9F7D}

Você pode usar Excluir para remover um Conjunto de relatórios da página [!DNL Adobe Analytics Report Suites]. A exclusão de um conjunto de relatórios remove apenas a cópia dos dados dos servidores de pesquisa/comercialização do site; não afeta os dados nos sistemas Adobe Analytics.

**Para excluir um conjunto de relatórios da Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na página [!DNL Adobe Analytics Report Suites], na coluna **[!UICONTROL Actions]**, clique em **[!UICONTROL Delete]** para o Conjunto de relatórios que deseja remover.
1. Na página [!DNL Adobe Analytics Delete Report Suite], clique em **[!UICONTROL Delete]**.

## Visualização de dados do Adobe Analytics {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Você pode usar a Pré-visualização para visualização das métricas do Adobe Analytics carregadas mais recentemente.

A coluna Linha na tabela mostra o número de cada linha de dados de métrica, indicando a ordem original em que as métricas do Adobe Analytics foram carregadas.

A coluna Produto mostra o Elemento Adobe Analytics que está associado a cada linha de dados de métrica. Os valores nesta coluna são usados para associar as páginas de pesquisa/comercialização do site aos valores de métrica correspondentes, conforme configurado nas definições de classificação.

Consulte [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Consulte [Configurando a classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

As colunas restantes mostram os valores de métrica associados a cada entrada.

Se a tabela estiver vazia, isso significa que você ainda não carregou nenhum dado do Adobe Analytics. Você pode fechar a página [!DNL Adobe Analytics Data Preview] e carregar os dados do Adobe Analytics.

Consulte [Carregando dados do Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).
Se a tabela foi designada como um relatório de termo de pesquisa, um pequeno triângulo aparecerá em cada linha. Você pode clicar na lista suspensa e selecionar **Simular termo de pesquisa** ou **Criar nova regra de negócios**. A ação selecionada é aplicada ao termo de pesquisa dessa linha, os dados que residem na segunda coluna

**Para pré-visualização de dados do Adobe Analytics**

1. No menu do produto, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**. Na página [!DNL Adobe Analytics Report Suites], na coluna [!DNL Actions], clique em **[!UICONTROL Preview]** para o Conjunto de relatórios cujos dados baixados você deseja visualização.

   * Clique em **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. Na página [!DNL Adobe Analytics Terms Report], na coluna [!DNL Actions], clique em **[!UICONTROL Preview]** para o Conjunto de relatórios cujos dados baixados você deseja visualização.

1. Na página [!DNL Adobe Analytics Data Preview], use as opções de navegação e exibição na parte superior e inferior da página para visualização dos dados.

   Clique em qualquer cabeçalho de coluna na tabela para classificar os dados em ordem crescente ou decrescente.
1. Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Download to Desktop]** para baixar e salvar a tabela como um arquivo `.xlt`.

   * Feche a página quando terminar de visualizar os dados do Adobe Analytics e retorne à página visualizada anteriormente.

## Visualização do log a partir do carregamento de dados mais recente da Adobe Analytics {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Você pode usar o Log de Visualizações para examinar o arquivo de log de dados da Adobe Analytics do processo de download mais recente. Você também pode usar a visualização de log para monitorar um download em execução.

Consulte [Carregando dados do Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Para visualização do log a partir do carregamento de dados mais recente do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na página [!DNL Adobe Analytics Report Suites], clique em **[!UICONTROL View Log]**. página de registro,
1. Na página [!DNL Adobe Analytics Data Log], use as opções de navegação e exibição na parte superior e inferior da página para visualização das informações de log.
1. Quando terminar, feche a página para retornar à página [!DNL Adobe Analytics Report Suites].

## Carregando dados do Adobe Analytics {#task_2F3C55189B0A4049AB2113F2291CC181}

Você pode baixar os dados configurados do Conjunto de relatórios da Adobe Analytics na pesquisa/comercialização do site.

A página Carregamento de dados mostra o status da última operação de Carregamento de dados da Adobe Analytics com as seguintes informações:

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
1. Na página [!DNL Stage Adobe Analytics Report Suites], clique em **[!UICONTROL Load Adobe Analytics Data]**.
1. Na página **[!UICONTROL Adobe Analytics Data Load]**, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Start Load]** para start da operação de carregamento.

      Durante uma operação de carregamento de dados, a linha **Progress** fornece informações sobre seu progresso.

   * Clique em **[!UICONTROL Stop Load]** para interromper a operação de carregamento.

1. Clique em **[!UICONTROL Close]** para retornar à página [!DNL Stage Adobe Analytics Reports Suite].

## Atualização da lista do conjunto de relatórios {#task_EA6215D438CA4185B106657D9712ED34}

Na primeira vez que você acessa o Adobe Analytics na interface de usuário de pesquisa/comercialização do site, uma lista dos Conjuntos de relatórios do Adobe Analytics disponíveis para empresa é baixada e armazenada em cache. Se novos Conjuntos de relatórios tiverem sido adicionados recentemente ou se os existentes tiverem sido excluídos, você poderá usar Atualizar a Lista do Conjunto de relatórios para atualizar a lista atualmente exibida na pesquisa/comercialização do site.

Consulte [Adicionar um conjunto de relatórios da Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

Consulte [Excluindo um conjunto de relatórios da Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D).

**Para atualizar a lista do conjunto de relatórios**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Na página [!DNL Adobe Analytics Report Suites], clique em **[!UICONTROL Refresh Report Suite List]**.

## Configuração de opções avançadas do Adobe Analytics {#task_C0FF2D69F59D44D8943A7831ED7FEC19}

Você pode usar [!DNL Advanced Adobe Analytics Options] para controlar as configurações destinadas a ajudar a ajustar o comportamento do processo de download do Conjunto de relatórios da Adobe Analytics.

Consulte [Editar as métricas do Adobe Analytics de um Report Suite](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**Para configurar opções avançadas do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Advanced Options]**.
1. Na página [!DNL Advanced Adobe Analytics Options], defina as seguintes opções:

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

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre feeds de classificação de SAINT {#concept_C55609DA24914BBC92CD90ED0259199D}

Você pode usar o Adobe Analytics SAINT para aprimorar seus relatórios de análise através da aceitação de dados tabulares de fontes externas. Por exemplo, você pode usar a pesquisa/comercialização do site para recuperar os dados de seus próprios índices e exportar esses dados para a Adobe Analytics.

Para usar com êxito o recurso Adobe Analytics SAINT na pesquisa/comercialização do site, esteja ciente dos seguintes requisitos:

* É necessário ter uma empresa Adobe Analytics e um Conjunto de relatórios.

   Consulte [Sobre o menu Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411).
* A conta de usuário do Adobe Analytics deve ter privilégios para modificar o Conjunto de relatórios.

   Consulte [Configurar a autenticação de métricas do Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42).
* O usuário do Adobe Analytics deve pertencer ao grupo da API da Web para que possa usar a API da Web do Adobe Analytics.
* O índice de pesquisa deve ter dados que a Adobe Analytics pode usar, como dados no formato correto.

Antes de criar um feed, reveja as seguintes perguntas e informações para que você possa concluir o assistente de Feed de SAINT com êxito:

* Com qual conjunto de relatórios você vai trabalhar?
* Para qual conjunto de classificações, como produto, e-var e assim por diante, você fornecerá dados?
* Quais classificações existem nos relatórios? A resposta a essa pergunta é determinada pelo tipo de dados que está prontamente disponível na pesquisa/comercialização do site e pelo tipo de relatórios que a Adobe Analytics informa como desejável.
* O SAINT aceita os dados da pesquisa/comercialização do site como um tipo de texto. O formato desses dados afeta a apresentação dos relatórios da Adobe Analytics.

## Criação de um feed do Adobe Analytics SAINT {#task_914B5AB821E84627953D8EF9339A7DD0}

Você pode usar o Adobe Analytics SAINT para aprimorar relatórios do Adobe Analytics através da aceitação de dados tabulares de fontes externas.

Por exemplo, você pode usar a pesquisa/comercialização do site para recuperar dados de seus próprios índices e exportar esses dados para a Adobe Analytics.

**Para criar um feed do Adobe Analytics SAINT**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na página [!DNL SAINT Classification Feeds], clique em **[!UICONTROL Create SAINT Feed]**.
1. Na caixa de diálogo [!DNL Create Feed], no campo de texto **Nome do feed**, digite o novo nome do feed e clique em **[!UICONTROL Next]**.

   Nesse ponto, o feed é salvo e adicionado à página [!DNL SAINT Classification Feed]. Se você escolher, poderá sair e editar o feed mais tarde para concluir o assistente.
1. Na página [!DNL Authentication], especifique o nome da empresa do Adobe Analytics, o nome de usuário e o segredo da Web nos respectivos campos de texto e clique em **[!UICONTROL Next]**.

   Certifique-se de que esteja autorizado a usar a API da Web com a Adobe Analytics.
1. Na página **[!UICONTROL Report Suite]**, escolha um conjunto de relatórios e seu conjunto de dados de classificação e clique em **[!UICONTROL Next]**.
1. Na página [!DNL Field Maps], mapeie as classificações do Adobe Analytics com os campos de metadados de pesquisa/comercialização do site e clique em **[!UICONTROL Next]**.

   Para ajustar as classificações do Adobe Analytics, clique em **[!UICONTROL Edit]** Classificações do Adobe Analytics para fazer logon no Adobe Analytics. Quando terminar de fazer as alterações, clique em **[!UICONTROL Refresh Classifications]** para atualizar as opções de classificações.
1. Na página [!DNL Search Criteria], os dados da pesquisa/comercialização do site podem ser filtrados antes de serem enviados ao Adobe Analytics SAINT. Construa regras de filtro aqui usando a interface do construtor de regras e clique em **[!UICONTROL Next]**.
1. Na página [!DNL Configure FTP], selecione o servidor FTP. Especifique a frequência de carregamento dos dados e clique em **[!UICONTROL Next]**.

   Como prática recomendada, cada feed tem sua própria conta FTP para evitar a perda acidental de dados. Você pode criar uma nova conta FTP da Adobe Analytics aqui.
1. Na página [!DNL Verification], clique em **[!UICONTROL Show Data View]** para revisar a representação da visualização de dados da saída. Se houver algum arquivo de feed real, eles serão listados aqui e estarão disponíveis para download.
1. Clique em **[!UICONTROL Close]**.

## Edição de um feed do Adobe Analytics SAINT {#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

É possível editar todos os aspectos de um feed de SAINT existente que você criou.

**Para editar um feed de SAINT do Adobe Analytics**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na página [!DNL Saint Classification Feeds], na coluna **[!UICONTROL Name]**, na lista suspensa ao lado de um feed, clique em **[!UICONTROL Edit feed]**.
1. Na caixa de diálogo SAINT feed, no campo de texto **Nome do feed**, digite o novo nome do feed e clique em **[!UICONTROL Next]**.

   Nesse ponto, o feed é salvo e adicionado à página [!DNL SAINT Classification Feed]. Se você escolher, poderá sair e editar o feed mais tarde para concluir o assistente.
1. Na página [!DNL Authentication], especifique o nome da empresa do Adobe Analytics, o nome de usuário e o segredo da Web nos respectivos campos de texto e clique em **[!UICONTROL Next]**.

   Certifique-se de que esteja autorizado a usar a API da Web com a Adobe Analytics.
1. Na página **[!UICONTROL Report Suite]**, escolha um conjunto de relatórios e seu conjunto de dados de classificação e clique em **[!UICONTROL Next]**.
1. Na página [!DNL Field Maps], mapeie as classificações do Adobe Analytics com os campos de metadados de pesquisa/comercialização do site e clique em **[!UICONTROL Next]**.

   Para ajustar as classificações do Adobe Analytics, clique em **[!UICONTROL Edit]** Classificações do Adobe Analytics para fazer logon no Adobe Analytics. Quando terminar de fazer as alterações, clique em **[!UICONTROL Refresh Classifications]** para atualizar as opções de classificações.
1. Na página [!DNL Search Criteria], os dados da pesquisa/comercialização do site podem ser filtrados antes de serem enviados ao Adobe Analytics SAINT. Construa regras de filtro aqui usando a interface do construtor de regras e clique em **[!UICONTROL Next]**.
1. Na página [!DNL Configure FTP], selecione o servidor FTP. Especifique a frequência de carregamento dos dados e clique em **[!UICONTROL Next]**.

   Como prática recomendada, cada feed tem sua própria conta FTP para evitar a perda acidental de dados. Você pode criar uma nova conta FTP da Adobe Analytics aqui.
1. Na página [!DNL Verification], clique em **[!UICONTROL Show Data View]** para revisar a representação da visualização de dados da saída. Se houver algum arquivo de feed real, eles serão listados aqui e estarão disponíveis para download.
1. Clique em **[!UICONTROL Close]**.

## Excluindo um feed do Adobe Analytics SAINT {#task_5319B1F4CA1A406393CFD7AE97258CEB}

Você pode excluir um feed de SAINT existente do Adobe Analytics que não é mais necessário ou usado.

**Para excluir um feed do Adobe Analytics SAINT**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na página [!DNL Saint Classification Feeds], na coluna **[!UICONTROL Name]**, na lista suspensa ao lado de um feed que você deseja remover, clique em **[!UICONTROL Delete feed]**.
1. Na caixa de diálogo Excluir, clique em **Yes** para verificar a exclusão do feed.

## Visualizando um arquivo de feed do Adobe Analytics SAINT {#task_F0C8BADD25E14E5DB30BF31D1F879FDB}

Você pode abrir a página [!DNL Verification] de um feed de SAINT existente para revisar a representação da visualização de dados da saída.

Se houver algum arquivo de feed real, eles serão listados aqui e estarão disponíveis para download como um arquivo de texto.

**Para visualização de um arquivo de feed do Adobe Analytics SAINT**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na página [!DNL Saint Classification Feeds], na coluna **[!UICONTROL Name]**, na lista suspensa ao lado de um feed, clique em **[!UICONTROL View Feed Files]**.
1. (Opcional) Clique em **[!UICONTROL Download File]** para salvar o arquivo de feed como um arquivo de texto.
1. Clique em **[!UICONTROL Close]** para retornar à página [!DNL SAINT Classification Feeds].

## Testando um feed do Adobe Analytics SAINT {#task_9864D69BE3824FC29C10B36EE4855D25}

Você pode testar um feed Adobe Analytics SAINT sem upload de arquivo.

Consulte [Gerando e fazendo upload de um feed do Adobe Analytics SAINT](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A).

Consulte [Visualizando um arquivo de feed do Adobe Analytics SAINT](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB).

**Para testar um arquivo de feed do Adobe Analytics SAINT**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na página [!DNL Saint Classification Feeds], na coluna **[!UICONTROL Name]**, na lista suspensa ao lado de um feed, clique em **[!UICONTROL Test Feed (No file upload)]**.
1. Quando o feed terminar de processar, na lista suspensa do nome do feed, clique em **[!UICONTROL View Feed Files]**.
1. Na página [!DNL Verification], clique em **[!UICONTROL Download File]** para baixar o arquivo de feed.
1. Clique em **[!UICONTROL Close]** para retornar à página [!DNL SAINT Classification Feeds].

## Gerando e fazendo upload de um feed do Adobe Analytics SAINT {#task_47AED946AA964334A877FDC8D4F6F00A}

Você pode gerar e carregar arquivos de feed para um feed Adobe Analytics existente que você criou.

Consulte [Testando um feed de SAINT Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25).

Consulte [Visualizando um arquivo de feed do Adobe Analytics SAINT](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB).

**Para gerar e carregar um arquivo de feed do Adobe Analytics SAINT**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Na página [!DNL Saint Classification Feeds], na coluna **[!UICONTROL Name]**, na lista suspensa ao lado de um feed, clique em **[!UICONTROL Generate and Upload Feed]**.
1. Quando o feed terminar de processar, na lista suspensa do nome do feed, clique em **[!UICONTROL View Feed Files]**.
1. Na página [!DNL Verification], clique em **[!UICONTROL Download File]** para baixar o arquivo de feed.
1. Clique em **[!UICONTROL Close]** para retornar à página [!DNL SAINT Classification Feeds].
