---
description: Você pode usar Palavras excluídas para especificar frases usadas com frequência e palavras comuns, como "a" e "the", que você deseja excluir dos resultados da pesquisa.
seo-description: Você pode usar Palavras excluídas para especificar frases usadas com frequência e palavras comuns, como "a" e "the", que você deseja excluir dos resultados da pesquisa.
seo-title: Sobre palavras excluídas
solution: Target
title: Sobre palavras excluídas
topic: Linguistics,Site search and merchandising
uuid: 1c879462-1b19-44f6-a3b2-20aa786b3221
translation-type: tm+mt
source-git-commit: 46cdbdf94ba8f92dba7d03ce80b25a2ae73b228a

---


# Sobre palavras excluídas{#about-excluded-words}

Você pode usar Palavras excluídas para especificar frases usadas com frequência e palavras comuns, como &quot;a&quot; e &quot;the&quot;, que você deseja excluir dos resultados da pesquisa.

## Uso de palavras excluídas {#concept_9DB67BD2F0DC43AC88741003D9F39812}

See also [About Searches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

Sem palavras excluídas, as pesquisas que contêm essas palavras podem identificar numerosos resultados irrelevantes. Quando você exclui palavras e frases, os resultados da pesquisa são omitidos que correspondem apenas aos termos excluídos especificados. Se uma consulta de pesquisa contiver uma palavra excluída, somente as palavras não excluídas serão usadas para localizar documentos.

As palavras de pesquisa excluídas não são destacadas nos resultados da pesquisa. No entanto, a pontuação de relevância de cada resultado é influenciada pelas palavras excluídas. Em outras palavras, as palavras excluídas são ignoradas ao localizar documentos, mas ainda são usadas ao classificar os documentos na página de resultados da pesquisa. Antes de os efeitos das configurações de Palavras excluídas (ou alterações nessas configurações) estarem disponíveis para os clientes, verifique se você regenerou o índice do site.

Ao digitar palavras para excluir dos resultados da pesquisa, separe palavras ou frases umas das outras com vírgulas. É possível inserir uma ou mais palavras de exclusão por linha. A seguir está um exemplo de palavras excluídas em linhas separadas e divididas por vírgulas.

![](assets/excluded_words_1.jpg)

Usando a lista de exemplos de palavras excluídas acima, se o cliente pesquisar &quot;os estados unidos da América&quot;, as palavras &quot;o&quot; e &quot;de&quot; serão excluídas da pesquisa. Em vez disso, a pesquisa encontra todas as páginas que contêm as palavras &quot;unido&quot;, &quot;estados&quot; e &quot;américa&quot;. As páginas que contêm apenas a palavra &quot;de&quot; ou &quot;o&quot; não são exibidas.

Alguns sites contêm frases específicas na maioria ou em todas as páginas. Por exemplo, um site sobre turismo em Nova York poderia conter as palavras Nova York no título de cada página. Considere adicionar essa frase, e outras como ela, à lista de exclusões:

![](assets/excluded_words_2.jpg)

Quando uma frase é excluída, as palavras individuais que a compõem ainda são usadas como termos de pesquisa. Somente quando um visitante pesquisa as palavras exatas, na ordem exata de uma frase excluída, é a frase excluída dos resultados da pesquisa. Utilizando o exemplo acima, se um cliente procurar o &quot;balé de nova orla&quot;, são excluídas a palavra &quot;a&quot; e a expressão &quot;nova orla&quot;; somente as páginas que contêm a palavra &quot;balé&quot; são retornadas como resultado da pesquisa. Por outro lado, uma busca por &quot;novos edifícios&quot; ou &quot;duke of york&quot; ainda encontra páginas que contêm a palavra &quot;novo&quot; ou &quot;iork&quot;, respectivamente.

## Configuração de palavras excluídas {#task_60BF6BB7A66C48479D2BBB32C0F38CDE}

Você pode excluir frases usadas com frequência e palavras comuns dos resultados da pesquisa.

É possível inserir uma ou mais palavras por linha. Separe cada palavra por vírgulas como no exemplo a seguir:

![](assets/excluded_words_1.jpg)

Você pode optar por mostrar os resultados da pesquisa quando todas as palavras na pesquisa do cliente forem palavras excluídas. Por exemplo, se você excluiu a palavra &quot;o&quot; e um cliente optar por pesquisar apenas por &quot;o&quot;, os resultados da pesquisa mostrarão qualquer página que contenha a palavra &quot;o&quot;. Este resultado é verdadeiro, apesar de a palavra &quot;o&quot; estar excluída. Se você não marcar essa opção, o cliente não obterá resultados de pesquisa. Essa configuração não terá efeito se a pesquisa contiver pelo menos uma palavra não excluída.

**Para configurar palavras excluídas**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Excluded Words]**.
1. Na [!DNL Excluded Words] página, no campo de **[!UICONTROL Words and Phrases]** texto, digite as palavras que deseja excluir dos resultados da pesquisa.
1. (Opcional) Clique em **[!UICONTROL Show results when all words in the query are excluded words]**.

   Quando todas as palavras na pesquisa do cliente são palavras excluídas, todas as palavras são usadas juntas para executar a pesquisa.
1. Clique em **[!UICONTROL Save Changes]**.
1. Para visualizar os resultados de suas alterações, clique em **[!UICONTROL regenerate your staged site index]** para recriar o índice de site preparado.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Excluded Words]** e siga um destes procedimentos:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

