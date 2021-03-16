---
description: Use o menu Opções de Conta para atualizar suas configurações de conta, definir preferências de comercialização ou remover seu próprio Search&amp, amp, Promote account.
solution: Target
subtopic: Account Options
title: Sobre o menu Opções de conta
topic: Configurações,Pesquisa e comercialização do site
uuid: 0f830033-de9e-4197-8d76-906c818662eb
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 2%

---


# Sobre o menu Opções de conta{#about-the-account-options-menu}

Use o menu Opções de conta para atualizar suas configurações de conta, definir preferências de merchandising ou remover sua própria conta do Search &amp; Promote.

## Definição das configurações da conta {#task_80A38D0C8E4F453395BD67B81E4B45D9}

Gerencie configurações da conta, como nome e endereço do site, fuso horário e muito mais. Ou exibir o número da sua conta.

**Para definir suas configurações de conta**

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
      <td colname="col2"> <p>Obrigatório. </p> <p>O endereço do URL do seu site. O endereço especificado aqui é usado como o ponto de entrada principal do site. </p> <p>Consulte também <a href="../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45" type="task" format="dita" scope="local"> Adicionando vários pontos de entrada de URL que você deseja indexar </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuso horário (para relatórios e agendamento) </p> </td> 
      <td colname="col2"> <p>O fuso horário usado para relatórios e operações de publicação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Validar atributos de tag do modelo ao salvar </p> </td> 
      <td colname="col2"> <p>Valida todos os atributos em <span class="codeph"> &lt;guided-*&gt; </span> e <span class="codeph"> &lt;search-*&gt; </span> quando você salva um modelo no Editor de modelo preparado. </p> <p>Consulte <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> Edição de uma apresentação ou de um modelo de transporte </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Validar referências de modelo para objetos GS ao salvar </p> </td> 
      <td colname="col2"> <p> Verifica a existência de objetos de Pesquisa guiada, como menus, facetas, navegação estrutural, vars personalizadas e modelos, que são mencionados nas tags <span class="codeph"> &lt;guided-*&gt; </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Impor verificação rigorosa da sintaxe do modelo </p> </td> 
      <td colname="col2"> <p>Torna o validador de modelo mais rígido e permite a verificação de itens, como aspas desequilibradas e símbolos &lt;&gt;. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número da conta </p> </td> 
      <td colname="col2"> <p>Não é possível editar o número da conta. É somente para fins de exibição. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.

## Configuração da integração com o Adobe CQ5 {#task_EA2FC2C24960498DAE01A1AB769D2F14}

Você pode configurar a integração de pesquisa/merchandising do site com o Adobe CQ5.

**Para configurar a integração com o Adobe CQ5**

1. Obtenha sua ID de membro e a ID de conta fazendo o seguinte:

   * Faça logon na conta de comercialização/pesquisa do site.
   * No caminho do URL, copie a ID do membro e a ID da conta.

      Por exemplo, se o caminho do URL para sua conta fosse `https://searchandpromote.mycompany.com/px/home/?sp_id=00123a4b-sp1234a5b6`, o ID do membro seria `00123a4b` e o ID da conta seria `sp1234a5b6`.

1. No Adobe CQ5, use a guia Cloud Services para criar a configuração de pesquisa/merchandising do site.

   Use a ID de membro e a ID de conta copiadas para as respectivas configurações.

## Configuração das preferências de comercialização {#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A}

Gerencie preferências de comercialização, como o construtor de regras padrão e o termo de pesquisa padrão.

**Para configurar preferências de Merchandising**

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
      <td colname="col1"> <p>Limite Dominante do Grupo de Acionadores </p> </td> 
      <td colname="col2"> <p> A porcentagem limite a ser aplicada a acionadores com base em resultados "dominantes por grupos" que especificam "usar padrão da conta". </p> <p>Alterar essa configuração pode afetar imediatamente as pesquisas em tempo real, portanto, use com cautela. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Definição de grupo </p> </td> 
      <td colname="col2"> <p>O número de resultados em um grupo para o console de comercialização. O máximo é 50.000. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Campo "ID do documento de merchandising" (MDI) </p> </td> 
      <td colname="col2"> <p> O campo especificado deve "unificar" os resultados da pesquisa que você deseja manipular por meio de acionadores e ações baseados em resultados de "resultado único". </p> <p>O uso do campo URL predefinido funciona em alguns casos, mas não é recomendado. Um meta campo definido pelo usuário com uma ID exclusiva para cada página (como SKU ou product_id, por exemplo) seria muito mais eficiente do que usar o campo URL. Especificar 'nenhum' desativa os acionadores e as ações baseados em resultados de 'único resultado' no gerenciador de regras. Alterar essa opção se aplica somente às regras que são salvas a partir de agora; as regras existentes continuam a usar a MDI com a qual foram originalmente salvas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Termo de pesquisa VRB padrão (Construtor visual de regras) </p> </td> 
      <td colname="col2"> <p> Permite personalizar o termo de pesquisa inicial usado no Construtor de regras visual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisa padrão VRB </p> </td> 
      <td colname="col2"> <p>Essa configuração permite que você defina qual pesquisa padrão é inicialmente selecionada no Construtor de regras visual. </p> <p> Essa configuração é relevante somente para implementação com várias pesquisas. O VRB permite que você selecione a pesquisa no acionador ou na ação à qual o grupo definido se aplica. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tempo Limite do VRB/Simulador </p> </td> 
      <td colname="col2"> <p>O VRB e o Simulador enviam pesquisas por meio de um servidor proxy que são mais lentas do que sua pesquisa de produção. Em determinadas circunstâncias, como ativos de carregamento lento, o VRB ou simulador pode atingir o tempo limite. Você pode aumentar ou diminuir o número de segundos que a interface do usuário deve aguardar antes de parar. Você raramente precisa aumentar essa configuração a partir do padrão de 60. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.

## Configuração do acesso à sua conta Adobe Dynamic Media Classic {#task_CEFF88C2033D41D0B2FE86C435EDAC6D}

Vincule sua conta de pesquisa/merchandising do site ao Adobe Dynamic Media Classic para adicionar facilmente anúncios de banner ao seu site usando ativos digitais carregados do Adobe Scene7.

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
      <td colname="col2"> <p>Obrigatório. Identifica a região do mundo em que sua conta do Dynamic Media Classic acessa os vários servidores do Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Empresa padrão </p> </td> 
      <td colname="col2"> <p>Identifica o nome da empresa associada à conta do Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Email </p> </td> 
      <td colname="col2"> <p>Obrigatório. Identifica o endereço de email usado para logon e comunicações do Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Senha </p> </td> 
      <td colname="col2"> <p>Obrigatório. Sua senha de logon do Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativado </p> </td> 
      <td colname="col2"> <p>Habilita todos os controles do Dynamic Media Classic em pesquisa/comercialização do site. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Teste </p> </td> 
      <td colname="col2"> <p>Verifica se o nome da região do Dynamic Media Classic, o endereço de email e os detalhes de senha estão corretos. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Clique em **[!UICONTROL Test]** para verificar se o nome da região do Dynamic Media Classic, o endereço de email e os detalhes da senha estão corretos.
1. Clique em **[!UICONTROL Save Changes]**.

## Configurar o redirecionador do Adobe Analytics {#task_2C9DE333FD7246E4A460FC0F55204160}

Se você usar [!DNL Adobe Analytics] para rastrear visitantes do site, poderá usar [!DNL Adobe Analytics Redirector] em pesquisa/merchandising do site para rastrear todos os redirecionamentos HTTP com [!DNL Adobe Analytics].

**Para configurar o Redirecionador Adobe Analytics**

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
      <td colname="col1"> <p>Ativar o recurso Redirecionador Adobe Analytics </p> </td> 
      <td colname="col2"> <p>Ativa o rastreamento de redirecionamentos HTTP com o Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Servidor de rastreamento </p> </td> 
      <td colname="col2"> <p> Identifica o nome do servidor de rastreamento do Adobe Analytics. </p> <p>Para descobrir o nome do servidor de rastreamento, </p> <p> 
      <ol id="ol_D17B77E81F8D40D0948415CD60839BE3"> 
      <li id="li_BE58DBA104D44F0DB6C64AD3F12CEA97"> No Adobe Analytics, clique em <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Gerenciador de código </span>. </li> 
      <li id="li_67A93D17C3A14874928C6DC4FF2D4784"> Na caixa de grupo <span class="wintitle"> Opções </span> , selecione um conjunto de relatórios na respectiva lista suspensa. </li> 
      <li id="li_5AAB004AC58441DBB0F813BDE30EFFD4"> Clique em <span class="uicontrol">Gerar código </span>. </li> 
      <li id="li_E80368993F4D4DD69E37509FF4348B36"> Na página <span class="wintitle"> Gerenciador de código </span> , clique na guia <span class="uicontrol"> Arquivo Javascript principal </span>. </li> 
      <li id="li_991BDCDDA41A445F85CEEAAE9A46A304"> Na <span class="wintitle"> Seção de configuração </span>, encontre a linha que se parece com a seguinte: <p> <code> s.trackingServer="yourcompany.122.2o7.net" </code> </p> <p>O nome do servidor de rastreamento, neste caso, é <span class="codeph"> "yourcompany.122.2o7.net" </span> </p> </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID do conjunto de relatórios </p> </td> 
      <td colname="col2"> <p> Identifica a ID do conjunto de relatórios. </p> <p>Para descobrir sua ID do conjunto de relatórios, </p> <p> 
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
      <td colname="col1"> <p>Defina as letras maiúsculas e minúsculas de todos os valores personalizados como </p> </td> 
      <td colname="col2"> <p>Permite padronizar a formatação usada para qualquer valor de parâmetro personalizado especificado acima. O Adobe Analytics diferencia maiúsculas de minúsculas, portanto, há um motivo para unificar as letras maiúsculas e minúsculas dos valores. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Adobe Analytics Redirector] , siga um destes procedimentos:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configurar arquivos raiz {#task_5F175C8743FB49A2A003813CBF7C56BF}

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
      <td colname="col2"> <p>Permite ou não permite que bots acessem determinadas partes do site. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>sitemap.xml </p> </td> 
      <td colname="col2"> <p>O arquivo XML com uma lista de todas as páginas disponíveis no site. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>crossdomain.xml </p> </td> 
      <td colname="col2"> <p>Permite ou não permite que o Flash Player acesse arquivos entre domínios. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Root Files] , siga um destes procedimentos:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Transferindo a propriedade da conta para outro usuário da conta {#task_47E3C66CC6374274830DA10171E0CF17}

Como proprietário de conta, se você pretende cancelar seu logon, primeiro deve transferir a propriedade para outro usuário ativo da conta. Você pode usar [!DNL Transfer Ownership] para realizar essa tarefa.

Você pode transferir a propriedade para qualquer usuário existente da conta de pesquisa/comercialização do site.

Quando a transferência de propriedade estiver concluída, o novo proprietário da conta receberá uma notificação por e-mail, e o antigo proprietário será aliviado das restrições e responsabilidades dessa posição.

Só pode haver um proprietário por conta. Se transferir sua propriedade para outro usuário, você não terá mais privilégios de propriedade.

Consulte [Cancelar seu logon](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Consulte [Remover uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Consulte [Removendo-se de uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

**Para transferir a propriedade da conta para outra conta**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Transfer Ownership]**.
1. Na página [!DNL Transfer Ownership] , clique no usuário que você deseja que assuma a propriedade de sua conta.
1. Clique em **[!UICONTROL Transfer]**.

## Remover uma conta {#task_975178D5B9444BF8B52D72B897A49C32}

Você pode remover uma conta totalmente da pesquisa/comercialização do site. Ao fazer isso, você e outros usuários da sua conta não terão mais acesso a ela.

Ao remover sua conta, ela não pode mais ser usada para indexar ou pesquisar seu site ativo. Além disso,

Para permitir que outros usuários continuem usando essa conta, você pode transferir a propriedade para um usuário diferente e, em seguida, remover a si mesmo como um usuário da conta.

Consulte [Transferindo a propriedade da conta para outro usuário da conta](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

Se tiver outras contas, depois de remover a conta atual, você será levado à primeira conta listada no logon.

Consulte [Removendo-se de uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

Consulte [Cancelar seu logon](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

**Para remover uma conta**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Account]**.
1. (Opcional) No campo [!DNL Reason for Removal] , insira um motivo para a remoção da conta.
1. Clique em **[!UICONTROL Remove Account]**.

## Removendo-se de uma conta {#task_C56F5AB87B664BAAAC2FD2F15003E73F}

Você pode se remover de uma conta de pesquisa/merchandising do site.

Ao remover a si mesmo de uma conta, não é mais possível acessá-la e não é possível editar as configurações da conta ou indexar seu site com ela.

Para recuperar o acesso à conta, peça a um usuário da conta atual para reinstalá-lo.

Consulte [Cancelar seu logon](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Consulte [Remover uma conta](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Consulte [Transferindo a propriedade da conta para outro usuário da conta](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

**Para remover você de uma conta**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Yourself]**.
1. Clique em **[!UICONTROL Remove Yourself]**.
