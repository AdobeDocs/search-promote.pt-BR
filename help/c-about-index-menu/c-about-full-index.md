---
description: Você pode usar o Índice completo para indexar todas as páginas do seu site temporário ou ao vivo. A indexação ajuda seus clientes a encontrar mais facilmente o que estão procurando ou o que precisam ao realizar uma pesquisa.
seo-description: Você pode usar o Índice completo para indexar todas as páginas do seu site temporário ou ao vivo. A indexação ajuda seus clientes a encontrar mais facilmente o que estão procurando ou o que precisam ao realizar uma pesquisa.
seo-title: Sobre o Índice Completo
solution: Target
subtopic: Full Index
title: Sobre o Índice Completo
topic: Index,Site search and merchandising
uuid: dce1eafd-5aea-4945-8305-8f9e7dc392df
translation-type: tm+mt
source-git-commit: 7af85dd37f06fe506e5f57e28a25385ca7ab3db5

---


# Sobre o Índice Completo{#about-full-index}

Você pode usar o Índice completo para indexar todas as páginas do seu site temporário ou ao vivo. A indexação ajuda seus clientes a encontrar mais facilmente o que estão procurando ou o que precisam ao realizar uma pesquisa.

## Usando índice completo {#concept_C69BD21863FD4856B49326F35DB570D3}

Quando você gera um índice completo, as informações de status são exibidas, como hora de início, tempo decorrido e erros durante o processo de indexação. As informações sobre o status do último índice também são exibidas.

Se você tiver alterado uma configuração de conta que exija uma regeneração de índice, o status poderá ser &quot;Regenerando&quot;. Durante a regeneração, as configurações da conta são aplicadas para criar um índice de site atualizado.

Você pode interromper ou reiniciar o processo de indexação a qualquer momento.

Enquanto o novo índice é criado para um site ao vivo, os clientes podem continuar a pesquisar seu site usando seu último índice. As informações sobre o status do último índice também são exibidas.

## Configurar o agendamento de índice completo para um site ao vivo {#task_6760F3256D004A228B38968DF15421F0}

Você pode especificar a hora e os dias em que deseja rastrear seu site e atualizar o índice.

A hora selecionada é local de acordo com o fuso horário configurado nas Configurações da conta.

Consulte [Definição das configurações](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)da sua conta.

Os servidores da Web normalmente ficam inativos para manutenção no meio da noite. Se o servidor estiver inativo durante um tempo de índice programado, o processo de indexação falhará. Certifique-se de selecionar uma hora do dia em que o servidor Web está disponível.

A programação de índice se aplica somente ao seu índice ativo; não é possível agendar índices preparados.

**Para definir o agendamento de índice completo para um site ativo**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Schedule]**.
1. Na lista **[!UICONTROL Time]** suspensa, selecione a hora em que deseja que a indexação completa seja iniciada.
1. Selecione um ou mais dias para que a indexação completa seja executada.
1. Clique em **[!UICONTROL Save Changes]**.

## Execução de um índice completo de um site ao vivo ou preparado {#task_F7FE04D8A1654A7787FCCA31B45EB42D}

Você pode usar o Índice completo para indexar todas as páginas do seu site temporário ou ao vivo. A indexação ajuda seus clientes a encontrar mais facilmente o que estão procurando ou o que precisam ao realizar uma pesquisa.

**Para executar um índice completo de um site ao vivo ou preparado**

1. No menu do produto, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Index]**.

1. Defina as opções de indexação desejadas.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Opção </p> </th> 
    <th colname="col2" class="entry"> <p>Descrição </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Limpar cache de índice </p> </td> 
    <td colname="col2"> <p>Remove todos os documentos do cache de índice. </p> <p>Quando selecionada, cada página do site é baixada do servidor. Se essa configuração estiver marcada e desativada, sua conta será definida para limpar o cache toda vez que um índice completo for executado. Ou, algumas configurações de conta alteradas anteriormente agora exigem um índice completo. </p> <p>Quando desmarcada, todas as páginas indexadas permanecem no índice até que o servidor da Web diga que a página não existe mais. Essa situação é verdadeira mesmo se os links para essa página forem removidos. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Regenerar pendente </p> </td> 
    <td colname="col2"> <p>Selecione Se você fez alterações nas configurações da sua conta que alteraram substancialmente o conteúdo do índice. Alterações substanciais incluem fazer alterações em qualquer uma das seguintes situações: 
    <ul id="ul_4EB8FF692FEB47BBB9A64D61299380D1"> 
    <li id="li_7CF8D286512F4210BEA3DB9F0EFA097A">Sinônimos </li> 
    <li id="li_8178ABC342BB4365B3927E20433756E3">Coleções </li> 
    <li id="li_57C8BD06BFA64AFAA2C9EF2CC59520EF">Metadados </li> 
    <li id="li_C4B6A7DA023B4A43991D03EC592170C9">Palavras excluídas </li> 
    <li id="li_9E0AD4B6DDC24A5A8FB5C2C1CCD5348A">Idioma da conta </li> 
    <li id="li_338F107547DF48AAA0EF90F4AD8664A5">Classificação </li> 
    <li id="li_7F49B86D94974E79AAD381A64A1400F2">Alternar pesquisa que diferencia maiúsculas de minúsculas </li> 
    <li id="li_E8FE6EE240A840AC826ADF4294AAC6F6">Alternar o suporte diacrítico </li> 
    <li id="li_51763D482DCB4ED0972966F492B8C0F2">Alternando a indexação de números </li> 
    </ul> </p> <p>Antes que outro rastreamento ocorra, uma passagem rápida é feita por todos os dados de índice para torná-lo compatível com as novas configurações de conta. </p> <p>Essa opção só estará disponível se você estiver fazendo um índice completo de um site preparado. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Contar todas as páginas </p> </td> 
    <td colname="col2"> <p>Permite que o rastreamento de páginas do site continue mesmo depois que você atingir o limite de sua página de conta. </p> <p>As páginas adicionais não são adicionadas ao índice, mas você pode determinar o número total de documentos no site. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Clique em **[!UICONTROL Full Index Now]**.
1. (Opcional) Se ocorreram erros de indexação, clique em **[!UICONTROL View Errors]** para exibir o log associado.

## Visualizando o log de índice completo de um site ao vivo ou preparado {#task_02E5E944C56B4EB19CC1FF321F3221B8}

Quando um índice completo em tempo real ou um índice completo preparado estiver concluído, você poderá exibir seu log associado para solucionar quaisquer erros que ocorreram.

Não é possível exportar registros nem salvá-los. O log permanece disponível para exibição até que o novo índice ocorra.

**Para exibir o log de índice completo de um site ao vivo ou preparado**

1. No menu do produto, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Log]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Log]**.

1. Na página de log, na parte superior ou inferior, execute um dos procedimentos a seguir:

   * Use as opções de navegação **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]****[!UICONTROL Last]** ou **[!UICONTROL Go to line]** para percorrer o log.

   * Use as opções de exibição **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** para refinar o que você vê.

