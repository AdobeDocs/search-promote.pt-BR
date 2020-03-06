---
description: O armazenamento temporário permite que você teste e visualize alterações nas configurações e configurações sem afetar o índice ativo.
seo-description: O armazenamento temporário permite que você teste e visualize alterações nas configurações e configurações sem afetar o índice ativo.
seo-title: Sobre o armazenamento temporário
solution: Target
title: Sobre o armazenamento temporário
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Sobre o armazenamento temporário{#about-staging}

O armazenamento temporário permite que você teste e visualize alterações nas configurações e configurações sem afetar o índice ativo.

## Sobre o armazenamento temporário {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

O armazenamento temporário permite que você teste e visualize alterações nas configurações e configurações sem afetar o índice ativo.

Consulte também ID do [elemento : context_A5783D07C72042EC8886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Qualquer página que tenha as opções de preparo **[!UICONTROL Push All Live]** ou que **[!UICONTROL View Live Settings]** signifique que todas as configurações dessa página possam ser preparadas. As exceções são as páginas da Web no Índice. As páginas nesta área são explicitamente para o índice de preparo ou o índice ao vivo para permitir que você controle diretamente os dois índices de forma independente.

Você pode preparar quase tudo, incluindo seu índice. Algumas exceções incluem configurações específicas de conta que afetam o ambiente em estágio e em tempo real simultaneamente e a programação de operações de indexação. Por padrão, quando você salva qualquer alteração em uma configuração que pode ser preparada, ela é automaticamente preparada.

Quando as opções **[!UICONTROL Push All Live]** ou as **[!UICONTROL View Lives Settings]** opções não estão ativadas (esmaecidas), isso significa que as configurações preparadas nessa página são as mesmas que as configurações ativas.

Para um item que é preparado, observe que a versão em tempo real das configurações é somente leitura; ela só pode ser manipulada ao colocar as configurações preparadas ao vivo.

## Sobre o histórico em páginas preparadas {#section_5BE780AFF26A450A9EFF4000DE53531B}

A maioria das configurações preparadas tem uma [!DNL History] opção na área superior direita da página. Quando você clica **[!UICONTROL History]**, permite reverter quaisquer alterações feitas recentemente na página de preparo específica que você abriu.

Você também pode exibir o Log de alterações para uma exibição alternativa do Histórico. Sempre que uma alteração é aplicada, uma versão de backup do arquivo de dados subjacente é criada. O Log de alterações mostra cada revisão, mostrando o número da versão, o endereço de email do usuário que realizou as alterações e a data em que o backup foi feito. A entrada com um valor de versão em negrito representa a versão atual.

See [Viewing the Change Log](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## A página Gerenciar configurações do Stage-Live {#section_E72B8CAF516345A5B6B6783CF6E512EE}

Além de oferecer as opções **[!UICONTROL Push All Live]** e **[!UICONTROL View Live Settings]** diretamente de dentro de uma determinada página, você também pode usar a **[!UICONTROL Manage Stage-Live Settings]** página para fazer a mesma coisa. A **[!UICONTROL Manage Stage-Live Settings]** página, disponível no menu principal do produto, é um local central que mostra todas as configurações na sua conta que estão preparadas no momento. Você pode colocar todas as configurações ao vivo, colocar somente as configurações selecionadas ao vivo ou excluir as configurações. No entanto, como prática recomendada, sempre coloque todos os itens preparados online para evitar problemas de interdependência.

As configurações na página são agrupadas em categorias. Você pode expandir cada categoria para mostrar quais configurações de página são preparadas. Atualmente, as dependências não são rastreadas no gerenciador de palco. Portanto, é recomendável que você coloque tudo ao vivo de uma vez, exceto pelo índice.

Você pode colocar um índice preparado ao vivo. Certifique-se de verificar primeiro se o índice preparado não está obsoleto ou corrompido. Se você cometer um erro e colocar o índice em andamento, poderá reverter um índice em tempo real antigo. O envio de um índice em funcionamento normalmente leva menos de 30 segundos.

## Teste de uma configuração ou índice em etapas {#section_6800E52D20854A779946EAB600801F12}

Nas páginas que suportam um controle de teste, você pode testar em relação às configurações preparadas ou ativas. Quando você exibe as configurações de preparo, a configuração de preparo é usada para o teste. Da mesma forma, quando você estiver visualizando a configuração ao vivo, o teste usará as configurações ao vivo. Na seção modelos, todos os testes são feitos em relação à versão de teste do índice. Para pesquisar um índice preparado, defina o parâmetro `sp_staged` CGI igual a 1. Por sua vez, isso indica que você deseja usar o índice de preparo. Se não existir um índice preparado, o índice ativo será pesquisado e quaisquer configurações de tempo de pesquisa preparadas serão aplicadas conforme apropriado.

Consulte também Parâmetros [CGI de pesquisa de](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)backend.

## Exibir configurações ao vivo {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

Você pode revisar a versão ao vivo das configurações de qualquer página de preparo.

<!-- 

t_viewing_live_settings.xml

 -->

Se a **[!UICONTROL View Live Settings]** opção não estiver ativada (esmaecida), isso significa que as configurações de palco para essa página e as configurações ativas já estão sincronizadas.

**Para exibir configurações ao vivo**

1. Em qualquer página que tenha configurações preparadas, clique em **[!UICONTROL View Live Settings]** para ver a versão ativa das configurações.
1. Opcionalmente, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL View]** para ver as opções atuais selecionadas para a configuração de preparo.
   * Clique em **[!UICONTROL View Stage Settings]** para retornar à configuração de preparo onde você pode editar ou excluir a configuração.

## Colocando configurações de estágio em execução {#task_44306783B4C0408AAA58B471DAF2D9A4}

Você pode colocar as configurações ao vivo de qualquer exibição de página preparada ou da página central **[!UICONTROL Manage Stage-Live Settings]** .

<!-- 

t_pushing_live_settings_live.xml

 -->

Quando a **[!UICONTROL Push Live]** opção está ativada (não esmaecida) em uma página, isso significa que há uma configuração que é preparada. Ou, significa que uma configuração possui edições e, quando você salva, a configuração é encenada. Quando você clica nessa opção, qualquer edição não salva é salva na área de preparo. Se não houver edições pendentes, as configurações da página serão imediatamente colocadas online.

**Para colocar as configurações preparadas ao vivo**

1. Faça uma das seguintes opções:

   * Em qualquer página que tenha &quot;Preparado&quot; selecionado como Exibição, clique em **[!UICONTROL Push Live]**.
   * No menu do produto, clique em **[!UICONTROL Staging]**. Na **[!UICONTROL Manage Stage-Live Settings]** página, execute um dos procedimentos a seguir:

   * Use a árvore de configurações para verificar apenas as configurações que deseja colocar ao vivo e clique em **[!UICONTROL Push Selected Live]**.
   * Clique em **[!UICONTROL Push All Live]**.

## Excluindo configurações de stage-live de um local central {#task_B72BEA9269704B1399600A9CA273369B}

Se você tiver muitas configurações para excluir, poderá usar a **[!UICONTROL Manage Stage-Live Settings]** página para excluir configurações de um local central.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Aviso**: Quando você clica **[!UICONTROL Delete Selected]**, todas as configurações marcadas são excluídas imediatamente; não há caixa de diálogo de confirmação para verificar se você realmente deseja excluir as configurações selecionadas. Além disso, não há nenhum recurso Histórico associado à página. Portanto, não é possível desfazer a exclusão.

**Para excluir configurações de ativação de estágio de um local central**

1. No menu do produto, clique em **[!UICONTROL Staging]**.
1. Na **[!UICONTROL Manage Stage-Live Settings]** página, use a árvore de configurações para verificar apenas as configurações que deseja excluir.
1. Clique em **[!UICONTROL Delete Selected]**.
