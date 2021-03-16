---
description: Você pode usar o Índice de regeneração para atualizar o índice do seu site sem precisar rastrear novamente seu site.
solution: Target
subtopic: Regenerate Index
title: Sobre o Índice de Regeneração
topic: Índice,Pesquisa e comercialização do site
uuid: 9d1f1d88-0453-4422-a625-a348febbf224
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# Sobre Regenerar Índice{#about-regenerate-index}

Você pode usar [!DNL Regenerate Index] para atualizar o índice do site sem precisar rastrear novamente seu site.

## Usando o Índice Regenerado {#concept_6CBE6B8D18EF47D293091CBA542245FA}

Você pode usar essa opção sempre que fizer uma alteração nas seguintes opções de conta:

* Palavras e idiomas
* Palavras excluídas
* Sinônimos
* Configurações de metadados, como ao excluir um campo de metadados, alterar um nome de campo, tipo de dados, formatos de data, ordem de classificação, valor de classificação mínimo ou máximo, valor de classificação padrão, tipo de lista ou separador de lista.

As informações da opção de conta atualizada são usadas para gerar um novo índice de site. Regenerate permite que você faça alterações no índice do site de forma rápida e eficiente.

Por padrão, qualquer conteúdo novo ou alterado do site não é incluído no índice. Para incluir esse conteúdo, execute um índice completo ou incremental.

Consulte também [Executar um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte também [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Regeneração do índice de um site em tempo real ou temporário {#task_B28DE40C0E9A475ABCBCBC4FF993AACD}

Você pode usar [!DNL Regenerate Index] para atualizar o índice do site sem precisar rastrear novamente o site.

**Para gerar novamente o índice de um site ao vivo ou preparado**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Regenerate]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Regenerate]**.

1. Na página [!DNL Regenerate], clique em **[!UICONTROL Regenerate Index Now]**.
1. (Opcional) Siga um destes procedimentos:

   * Se você optou por executar **[!UICONTROL Live Regenerate]**, clique em **[!UICONTROL View Last Crawl]** para revisar as estatísticas de desempenho da última regeneração de índice ao vivo que foi executada.

   * Enquanto o índice estiver sendo gerado novamente, clique em **[!UICONTROL Stop Regenerate Now]** para interromper o processo de regeneração do índice.
   * Enquanto o índice estiver sendo regenerado, clique em **[!UICONTROL Restart Regenerate Now]** para reiniciar o processo de regeneração de índice a partir do início.
   * Se ocorreram erros de indexação após uma regeneração preparada, clique em **[!UICONTROL View Errors]** para exibir o log associado.

## Visualização do log de índice gerado novamente de um site ativo ou preparado {#task_61CE8F9E7BF84BA89A8D482B2106BB15}

Quando uma regeneração de índice ao vivo ou de um índice de preparo estiver concluída, você poderá exibir seu log associado para solucionar qualquer erro que tenha ocorrido.

Não é possível exportar logs nem salvá-los. No entanto, o log permanece disponível para exibição até que o novo índice ocorra.

**Para exibir o log de índice gerado de um site ativo ou em preparo**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Log]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Log]**.

1. Na página de log, na parte superior ou inferior, execute um dos seguintes procedimentos:

   * Use as opções de navegação **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** para percorrer o log.

   * Use as opções de exibição **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** para refinar o que você vê.

