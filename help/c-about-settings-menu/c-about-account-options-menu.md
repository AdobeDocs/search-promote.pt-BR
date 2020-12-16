---
description: Use o menu Opções de conta para atualizar suas configurações de conta, definir preferências de comercialização ou remover seu próprio Search&amp;Promover conta.
seo-description: Use o menu Opções de conta para atualizar suas configurações de conta, definir preferências de comercialização ou remover seu próprio Search&amp;Promover conta.
seo-title: Sobre o menu Opções da conta
solution: Target
subtopic: Account Options
title: Sobre o menu Opções da conta
topic: Settings,Site search and merchandising
uuid: 0f830033-de9e-4197-8d76-906c818662eb
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 2%

---


# Sobre o menu Opções de conta{#about-the-account-options-menu}

Use o menu Opções de conta para atualizar suas configurações de conta, definir preferências de comercialização ou remover sua própria conta de Search &amp; Promote.

## Definição das configurações da sua conta {#task_80A38D0C8E4F453395BD67B81E4B45D9}

Gerencie configurações de conta, como nome e endereço do site, fuso horário e muito mais. Ou, visualização o número da sua conta.

**Para configurar suas configurações de conta**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Account Settings]**.
1. Na página [!DNL Account Settings], defina as opções desejadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome do site </p> </td> 
      <td colname="col2"> <p>Obrigatório. </p> <p>Um nome curto que é usado para descrever seu site/conta. Essa opção é útil se você tiver vários sites. </p> <p> <p>Observação:  Você deve entrar em contato com o Suporte Técnico para selecionar um ou mais nomes que deseja usar. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Endereço do site </p> </td> 
      <td colname="col2"> <p>Obrigatório. </p> <p>O endereço URL do seu site. O endereço especificado aqui é usado como o ponto de entrada principal do site. </p> <p>Consulte também <a href="../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45" type="task" format="dita" scope="local"> Adicionar vários pontos de entrada de URL que você deseja indexar </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuso horário (para relatórios e agendamento) </p> </td> 
      <td colname="col2"> <p>O fuso horário usado para relatórios e operações de publicação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Validar atributos de tag do modelo ao salvar </p> </td> 
      <td colname="col2"> <p>Valida todos os atributos em <span class="codeph"> &lt;guided-*&gt; </span> e <span class="codeph"> &lt;search-*&gt; </span> quando você salva um modelo no Editor de modelos preparados. </p> <p>Consulte <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> Editando uma apresentação ou um modelo de transporte </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Validar referências de modelo para objetos GS ao salvar </p> </td> 
      <td colname="col2"> <p> Verifica a existência de objetos de Pesquisa guiada, como menus, facetas, navegações estruturais, vars personalizadas e modelos, que são referenciados nas tags <span class="codeph"> &lt;guided-*&gt; </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Impor verificação rigorosa da sintaxe do modelo </p> </td> 
      <td colname="col2"> <p>Torna o validador de modelo mais restrito e permite a verificação de itens como aspas desbalanceadas e símbolos &lt;&gt;. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número da conta </p> </td> 
      <td colname="col2"> <p>Não é possível editar o número da conta. É apenas para fins de exibição. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.

## Configurando a integração com o Adobe CQ5 {#task_EA2FC2C24960498DAE01A1AB769D2F14}

Você pode configurar a integração da pesquisa/comercialização do site com o Adobe CQ5.

**Para configurar a integração com o Adobe CQ5**

1. Obtenha a ID do membro e a ID da conta, fazendo o seguinte:

   * Faça logon na sua conta de pesquisa/comercialização do site.
   * No caminho do URL, copie a ID do membro e a ID da conta.

      Por exemplo, se o caminho do URL para sua conta fosse `https://searchandpromote.mycompany.com/px/home/?sp_id=00123a4b-sp1234a5b6`, a ID do membro seria `00123a4b` e a ID da conta seria `sp1234a5b6`.

1. No Adobe CQ5, use a guia Cloud Services para criar a configuração de pesquisa/comercialização do site.

   Use a ID do membro e a ID da conta copiadas para as respectivas configurações.

## Configuração das preferências de comercialização {#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A}

Gerencie preferências de comercialização, como o construtor de regras padrão e o termo de pesquisa padrão.

**Para configurar preferências de comercialização**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Merchandising Preferences]**.
1. Na página [!DNL Merchandising Preferences], defina as opções desejadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Limite dominante do grupo de acionadores </p> </td> 
      <td colname="col2"> <p> A porcentagem limite a ser aplicada a acionadores baseados em resultados "dominantes de grupo" que especificam "usar padrão de conta". </p> <p>A alteração dessa configuração pode afetar imediatamente as pesquisas ao vivo, portanto, use com cautela. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Definição de grupo </p> </td> 
      <td colname="col2"> <p>O número de resultados em um grupo para o console de comercialização. O máximo é 50.000. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Campo 'ID do Documento de comercialização' (MDI) </p> </td> 
      <td colname="col2"> <p> O campo que você especificar deve "unificar" os resultados da pesquisa que você deseja manipular por meio de acionadores e ações baseados em resultados com "único resultado". </p> <p>O uso do campo URL predefinido funciona em alguns casos, mas não é recomendado. Um campo meta definido pelo usuário com uma ID exclusiva para cada página (como SKU ou product_id, por exemplo) seria muito mais eficiente do que usar o campo URL. A especificação de 'nenhum' desativa os acionadores e as ações baseados em resultados de 'único resultado' no gerenciador de regras. A alteração dessa opção se aplica somente às regras que são salvas posteriormente; as regras existentes continuam a usar a MDI com a qual foram originalmente salvas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Termo de pesquisa VRB padrão (Visual Rule Builder) </p> </td> 
      <td colname="col2"> <p> Permite personalizar o termo de pesquisa inicial usado no Construtor de regras visual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisa padrão VRB </p> </td> 
      <td colname="col2"> <p>Essa configuração permite definir qual pesquisa padrão foi inicialmente selecionada no Construtor de regras visual. </p> <p> Essa configuração só é relevante para implementação com várias pesquisas. O VRB permite selecionar a que pesquisa o acionador ou a ação o grupo definido se aplica. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tempo limite do VRB/Simulador </p> </td> 
      <td colname="col2"> <p>O VRB e o Simulator enviam pesquisas por meio de um servidor proxy que são mais lentas do que a pesquisa de produção. Em determinadas circunstâncias, como ativos de carregamento lento, o VRB ou simulador pode atingir o tempo limite. Você pode aumentar ou diminuir o número de segundos que a interface do usuário deve esperar antes de parar. Você raramente precisa aumentar essa configuração a partir do padrão de 60. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.

## Configurar acesso à sua conta Adobe Dynamic Media Classic {#task_CEFF88C2033D41D0B2FE86C435EDAC6D}

Vincule sua conta de pesquisa/comercialização do site ao Adobe Dynamic Media Classic para que você possa adicionar facilmente anúncios de banner ao seu site usando ativos digitais carregados da Adobe Scene7.

Consulte [Sobre banners](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA).

Consulte [Adicionar um banner usando o Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

**Para configurar o acesso à sua conta Adobe Dynamic Media Classic**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Scene7 Configuration]**.
1. Na página [!DNL Scene7 Configuration], defina as opções desejadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Região </p> </td> 
      <td colname="col2"> <p>Obrigatório. Identifica a região do mundo onde sua conta do Dynamic Media Classic acessa os vários servidores Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Empresa padrão </p> </td> 
      <td colname="col2"> <p>Identifica o nome da empresa associada à sua conta do Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Email </p> </td> 
      <td colname="col2"> <p>Obrigatório. Identifica seu endereço de email usado para logon e comunicações do Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Senha </p> </td> 
      <td colname="col2"> <p>Obrigatório. Sua senha de logon do Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativado </p> </td> 
      <td colname="col2"> <p>Habilita todos os controles do Dynamic Media Classic na pesquisa/comercialização do site. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Teste </p> </td> 
      <td colname="col2"> <p>Verifica se o nome da região do Dynamic Media Classic, o endereço de email e os detalhes da senha estão corretos. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Clique em **[!UICONTROL Test]** para verificar se o nome da região do Dynamic Media Classic, o endereço de email e os detalhes da senha estão corretos.
1. Clique em **[!UICONTROL Save Changes]**.

## Configuração do Adobe Analytics Redirecionador {#task_2C9DE333FD7246E4A460FC0F55204160}

Se você usar [!DNL Adobe Analytics] para rastrear visitantes do site, poderá usar [!DNL Adobe Analytics Redirector] na pesquisa/comercialização do site para rastrear todos os redirecionamentos HTTP com [!DNL Adobe Analytics].

**Para configurar o Adobe Analytics Redirecionador**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Adobe Analytics Redirector]**.
1. Na página [!DNL Adobe Analytics Redirector], defina as opções desejadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Ativar o recurso Adobe Analytics Redirecionador </p> </td> 
      <td colname="col2"> <p>Ativa o rastreamento de redirecionamentos HTTP com o Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Servidor de rastreamento </p> </td> 
      <td colname="col2"> <p> Identifica o nome do servidor de rastreamento do Adobe Analytics. </p> <p>Para descobrir o nome do servidor de rastreamento, </p> <p> 
      <ol id="ol_D17B77E81F8D40D0948415CD60839BE3"> 
      <li id="li_BE58DBA104D44F0DB6C64AD3F12CEA97"> No Adobe Analytics, clique em <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Gerenciador de código </span>. </li> 
      <li id="li_67A93D17C3A14874928C6DC4FF2D4784"> Na caixa de grupo <span class="wintitle"> Opções </span>, selecione um conjunto de relatórios na respectiva lista suspensa. </li> 
      <li id="li_5AAB004AC58441DBB0F813BDE30EFFD4"> Clique em <span class="uicontrol">Gerar código </span>. </li> 
      <li id="li_E80368993F4D4DD69E37509FF4348B36"> Na página <span class="wintitle"> Gerenciador de código </span>, clique na guia <span class="uicontrol"> Arquivo Javascript principal </span>. </li> 
      <li id="li_991BDCDDA41A445F85CEEAAE9A46A304"> Em <span class="wintitle"> Config Section </span>, localize a linha com a seguinte aparência: <p> <code> s.trackingServer="yourcompany.122.2o7.net" </code> </p> <p>O nome do servidor de rastreamento, neste caso, é <span class="codeph"> "yourcompany.122.2o7.net" </span> </p> </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID do conjunto de relatórios </p> </td> 
      <td colname="col2"> <p> Identifica a ID do conjunto de relatórios. </p> <p>Para descobrir a ID do conjunto de relatórios, </p> <p> 
      <ol id="ol_4FD7B2459358486DBDB130426131D16A"> 
      <li id="li_9AF624CEB128453C808892EEE385D5D1"> No Adobe Analytics, clique em <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Report Suites </span>. </li> 
      <li id="li_AAC47EAA04144A67BDCB5C7B8D8098E9"> Examine a coluna <span class="wintitle"> ID do conjunto de relatórios </span> na tabela para localizar a ID. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parâmetros personalizados </p> </td> 
      <td colname="col2"> <p>Permite adicionar parâmetros personalizados ao URL de redirecionamento do Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Defina a caixa de todos os valores personalizados como </p> </td> 
      <td colname="col2"> <p>Permite padronizar a caixa usada para quaisquer valores de parâmetro personalizados especificados acima. A Adobe Analytics faz distinção entre maiúsculas e minúsculas, portanto, há um motivo para unificar as letras maiúsculas e minúsculas dos valores. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Adobe Analytics Redirector], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurando arquivos raiz {#task_5F175C8743FB49A2A003813CBF7C56BF}

Gerencie arquivos raiz na pasta raiz do seu site.

**Para configurar arquivos raiz**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Root Files]**.
1. Na página [!DNL Root Files], navegue até os arquivos raiz que deseja carregar.

   <table> 
    <thead> 
    <tr> 
      <th colname="col1" class="entry"> <p>Arquivo raiz </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
      <td colname="col1"> <p>favicon.ico </p> </td> 
      <td colname="col2"> <p> O ícone do site. Normalmente, é exibido na barra de endereços do navegador do cliente. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>robots.txt </p> </td> 
      <td colname="col2"> <p>Permite ou despermite que bots acessem determinadas partes do site. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>sitemap.xml </p> </td> 
      <td colname="col2"> <p>O arquivo XML com uma lista de todas as páginas disponíveis no site. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>crossdomain.xml </p> </td> 
      <td colname="col2"> <p>Permite ou despermite que o Flash Player acesse arquivos em domínios. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar pré-visualização nos resultados.

   Consulte [Configurar um índice incremental de um site preparado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Root Files], execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Transferindo a propriedade da conta para outro usuário da conta {#task_47E3C66CC6374274830DA10171E0CF17}

Como proprietário da conta, se você pretende cancelar seu logon, primeiro é necessário transferir a propriedade para outro usuário ativo da conta. Você pode usar [!DNL Transfer Ownership] para realizar essa tarefa.

Você pode transferir a propriedade para qualquer usuário existente da conta de pesquisa/comercialização do site.

Quando a transferência de propriedade é concluída, o novo proprietário da conta recebe uma notificação por email, e o antigo proprietário é aliviado das restrições e responsabilidades dessa posição.

Só pode haver um proprietário por conta. Se transferir sua propriedade para outro usuário, você não terá mais privilégios de propriedade.

Consulte [Cancelando seu logon](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Consulte [Remoção de uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Consulte [Remover-se de uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

**Para transferir a propriedade da conta para outra conta**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Transfer Ownership]**.
1. Na página [!DNL Transfer Ownership], clique no usuário que você deseja que assuma a propriedade de sua conta.
1. Clique em **[!UICONTROL Transfer]**.

## Removendo uma conta {#task_975178D5B9444BF8B52D72B897A49C32}

Você pode remover uma conta totalmente da pesquisa/comercialização do site. Ao fazê-lo, você e outros usuários da sua conta não terão mais acesso a ela.

Quando você remove sua conta, ela não pode mais ser usada para indexar ou pesquisar seu site ativo. Além disso,

Para permitir que outros usuários continuem usando essa conta, você pode transferir a propriedade para um usuário diferente e, em seguida, removê-lo como um usuário da conta.

Consulte [Transferindo a propriedade da conta para outro usuário da conta](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

Se tiver outras contas, depois de remover a conta atual, você será levado para a primeira conta listada no logon.

Consulte [Remover-se de uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

Consulte [Cancelando seu logon](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

**Para remover uma conta**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Account]**.
1. (Opcional) No campo [!DNL Reason for Removal], informe um motivo para a remoção da conta.
1. Clique em **[!UICONTROL Remove Account]**.

## A remover-se de uma conta {#task_C56F5AB87B664BAAAC2FD2F15003E73F}

Você pode se remover de uma conta de pesquisa/comercialização do site.

Quando você se remove de uma conta, não pode mais acessá-la e não pode editar configurações de conta nem indexar seu site com ela.

Para recuperar o acesso à conta, peça a um usuário da conta atual para reinstalá-lo.

Consulte [Cancelando seu logon](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Consulte [Remoção de uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Consulte [Transferindo a propriedade da conta para outro usuário da conta](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

**Para se remover de uma conta**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Yourself]**.
1. Clique em **[!UICONTROL Remove Yourself]**.
