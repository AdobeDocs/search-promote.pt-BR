---
description: O armazenamento temporário permite testar e visualizar alterações em suas configurações e configurações sem afetar seu índice dinâmico.
solution: Target
title: Sobre preparo
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# Sobre o armazenamento temporário{#about-staging}

O armazenamento temporário permite testar e visualizar alterações em suas configurações e configurações sem afetar seu índice dinâmico.

## Sobre o armazenamento temporário {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

O armazenamento temporário permite testar e visualizar alterações em suas configurações e configurações sem afetar seu índice dinâmico.

Consulte também [ID do elemento :context_A5783D07C72042EC886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Qualquer página que tenha as opções de armazenamento temporário **[!UICONTROL Push All Live]** ou **[!UICONTROL View Live Settings]** significa que todas as configurações dessa página podem ser preparadas. As exceções são as páginas da Web no Índice. As páginas nessa área são explicitamente para o índice de preparo ou o índice live para permitir controlar diretamente os dois índices de forma independente.

Você pode preparar quase tudo, incluindo seu índice. Algumas exceções incluem configurações específicas da conta que afetam o ambiente temporário e ativo simultaneamente e a programação de operações de indexação. Por padrão, ao salvar as alterações em uma configuração que pode ser preparada, ela é automaticamente preparada.

Quando as opções **[!UICONTROL Push All Live]** ou **[!UICONTROL View Lives Settings]** não estão ativadas (esmaecidas), significa que as configurações preparadas nessa página são as mesmas que as configurações ativas.

Para um item que é preparado, observe que a versão ao vivo das configurações é somente leitura; ele só pode ser manipulado ao colocar as configurações de preparo ativas.

## Sobre o Histórico nas Páginas Preparadas {#section_5BE780AFF26A450A9EFF4000DE53531B}

A maioria das configurações preparadas tem uma opção [!DNL History] na área superior direita da página. Ao clicar em **[!UICONTROL History]**, é possível reverter as alterações feitas recentemente na página de preparo específica que você abriu.

Você também pode exibir o Log de alterações para uma exibição alternativa do Histórico. Toda vez que uma alteração é aplicada, uma versão de backup do arquivo de dados subjacente é criada. O Log de alterações mostra cada revisão, mostrando o número da versão, o endereço de email do usuário que executou as alterações e a data em que o backup foi feito. A entrada com um valor de versão em negrito representa a versão atual.

Consulte [Exibindo o Log de alterações](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## A página Gerenciar configurações do Stage-Live {#section_E72B8CAF516345A5B6B6783CF6E512EE}

Além de oferecer as opções **[!UICONTROL Push All Live]** e **[!UICONTROL View Live Settings]** diretamente de uma determinada página, você também pode usar a página **[!UICONTROL Manage Stage-Live Settings]** para fazer a mesma coisa. A página **[!UICONTROL Manage Stage-Live Settings]**, disponível no menu principal do produto, é um local central que mostra todas as configurações em sua conta que estão preparadas no momento. Você pode colocar todas as configurações em tempo real, enviar somente as configurações selecionadas em tempo real ou excluir as configurações. Como prática recomendada, no entanto, sempre coloque todos os itens preparados online para evitar problemas de interdependência.

As configurações na página são agrupadas em categorias. Você pode expandir cada categoria para mostrar quais configurações de página são preparadas. Atualmente, as dependências não são rastreadas no gerenciador de palco. Portanto, é recomendável colocar tudo ao vivo de uma só vez, exceto pelo índice.

Você pode enviar um índice por etapas ao vivo. Certifique-se de verificar primeiro se o índice preparado não está obsoleto ou corrompido. Se você cometer um erro e colocar o índice em funcionamento, é possível reverter um índice em tempo real antigo. O envio de um índice temporário em tempo real geralmente leva menos de 30 segundos.

## Teste de uma configuração ou índice preparados {#section_6800E52D20854A779946EAB600801F12}

Em páginas que oferecem suporte a um controle de teste, você pode testar as configurações em tempo real ou temporário. Quando você exibe as configurações de preparo, a configuração de preparo é usada para o teste. Da mesma forma, quando você está visualizando a configuração ao vivo, o teste usa as configurações ao vivo. Na seção templates , todos os testes são feitos em relação à versão preparada do índice. Para pesquisar um índice preparado, defina o parâmetro CGI `sp_staged` igual a 1. Por sua vez, isso indica que você deseja usar o índice de preparo. Se um índice preparado não existir, seu índice ativo será pesquisado e quaisquer configurações de tempo de pesquisa preparados serão aplicadas conforme apropriado.

Consulte também [Parâmetros CGI de pesquisa de backend](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Exibir configurações ativas {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

Você pode revisar a versão ao vivo das configurações de qualquer página preparada.

<!-- 

t_viewing_live_settings.xml

 -->

Se a opção **[!UICONTROL View Live Settings]** não estiver ativada (esmaecida), significa que as configurações de palco dessa página e as configurações ativas já estão sincronizadas.

**Para exibir as configurações ao vivo**

1. Em qualquer página que tenha configurações de preparo, clique em **[!UICONTROL View Live Settings]** para ver a versão ao vivo das configurações.
1. Como opção, execute um dos seguintes procedimentos:

   * Clique em **[!UICONTROL View]** para ver as opções atuais selecionadas para a configuração preparada.
   * Clique em **[!UICONTROL View Stage Settings]** para retornar à configuração preparada, onde é possível editar ou excluir a configuração.

## Envio das configurações do estágio em tempo real {#task_44306783B4C0408AAA58B471DAF2D9A4}

Você pode enviar as configurações ao vivo de qualquer visualização de página preparada ou da página central **[!UICONTROL Manage Stage-Live Settings]** .

<!-- 

t_pushing_live_settings_live.xml

 -->

Quando a opção **[!UICONTROL Push Live]** está ativada (não esmaecida) em uma página, significa que há uma configuração que é preparada. Ou significa que uma configuração tem edições e, quando você salva, a configuração é preparada. Ao clicar nessa opção, todas as edições não salvas são salvas na área de preparo. Se não houver edições pendentes, as configurações da página serão colocadas online imediatamente.

**Para colocar as configurações de preparo ao vivo**

1. Faça uma das seguintes opções:

   * Em qualquer página que tenha &quot;Preparado&quot; selecionado como a Exibição, clique em **[!UICONTROL Push Live]**.
   * No menu do produto, clique em **[!UICONTROL Staging]**. Na página **[!UICONTROL Manage Stage-Live Settings]**, execute um dos seguintes procedimentos:

   * Use a árvore de configurações para verificar apenas as configurações que deseja enviar ao vivo e clique em **[!UICONTROL Push Selected Live]**.
   * Clique em **[!UICONTROL Push All Live]**.

## Excluindo configurações do stage-live de um local central {#task_B72BEA9269704B1399600A9CA273369B}

Se você tiver muitas configurações para excluir, poderá usar a página **[!UICONTROL Manage Stage-Live Settings]** para excluir configurações de um local central.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Aviso**: Ao clicar em  **[!UICONTROL Delete Selected]**, todas as configurações marcadas são excluídas imediatamente; não há caixa de diálogo de confirmação para verificar se você realmente deseja excluir as configurações selecionadas. Além disso, não há nenhum recurso Histórico associado à página. Portanto, não é possível desfazer a exclusão.

**Para excluir configurações de estágio-ativo de um local central**

1. No menu do produto, clique em **[!UICONTROL Staging]**.
1. Na página **[!UICONTROL Manage Stage-Live Settings]**, use a árvore de configurações para verificar apenas as configurações que deseja excluir.
1. Clique em **[!UICONTROL Delete Selected]**.
