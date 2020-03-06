---
description: Você pode configurar a opção Você quis dizer para que os clientes recebam sugestões para termos de pesquisa válidos quando tentarem pesquisas que falharam. As sugestões são formadas procurando por correções de ortografia e digitação nos termos de pesquisa que resultam em uma pesquisa válida.
seo-description: Você pode configurar a opção Você quis dizer para que os clientes recebam sugestões para termos de pesquisa válidos quando tentarem pesquisas que falharam. As sugestões são formadas procurando por correções de ortografia e digitação nos termos de pesquisa que resultam em uma pesquisa válida.
seo-title: Sobre você quis dizer
solution: Target
title: Sobre você quis dizer
topic: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# About Did You Mean{#about-did-you-mean}

Você pode configurar a opção Você quis dizer para que os clientes recebam sugestões para termos de pesquisa válidos quando tentarem pesquisas que falharam. As sugestões são formadas procurando por correções de ortografia e digitação nos termos de pesquisa que resultam em uma pesquisa válida.

## A Configuração Você quis dizer {#task_B539D6A0043547EFB1CA19B67E762371}

Você pode adaptar como [!DNL site search/merchandising] faz sugestões de pesquisa quando a consulta de um cliente retorna resultados de pesquisa não ou mínimos.

<!-- 

t_configuring_did_you_mean.xml

 -->

**Para configurar Você quis dizer**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**.
1. Na [!DNL Did You Mean] página, no campo de texto **Remover essas palavras de sugestões** , digite palavras separadas por linha ou espaço para filtrar sugestões indesejadas.

   Essas são palavras no índice de pesquisa que não aparecem como termos de pesquisa alternativos recomendados. É possível excluir qualquer palavra que corresponda a um padrão por meio do uso de expressões regulares. Caso contrário, apenas a palavra exata será removida.

1. Defina as opções **Você quis dizer** .

   <!-- 
   
   r_did_you_mean_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Algoritmo de sugestão </p> </td> 
      <td colname="col2"> <p>Ajusta até onde o software vai para encontrar sugestões. Se um usuário cometer um erro de uma letra, todos os algoritmos apresentam as mesmas sugestões. O motivo é que basta apenas uma edição para chegar a uma sugestão funcional e todos os algoritmos encontram palavras próximas ao original. Mas quando os termos de pesquisa originais não são semelhantes aos termos existentes no índice, os Algoritmos de Sugestão <b>Deep</b> e <b>Bad Spellers</b> continuam a procurar possíveis sugestões. Esse cenário é útil se um cliente tentar um nome adequado, difícil de digitar, e exibir os nomes. No entanto, se você quiser que sugestões semelhantes sejam exibidas, poderá escolher o algoritmo <b>Rápido</b> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Contagem padrão de sugestões para mostrar </p> </td> 
      <td colname="col2"> <p>Especifica o número de sugestões de termos Você quis dizer (0-20) que você deseja mostrar quando a pesquisa de um cliente não retorna resultados. O padrão é 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comprimento mínimo da palavra de sugestão </p> </td> 
      <td colname="col2"> <p>Prunes Você quis dizer termos especificando o número mínimo de letras de uma palavra sugerida. </p> <p>Por exemplo, se você definir o valor como 4, o software não sugerirá uma palavra com 1, 2 ou 3 caracteres. Se você especificar um valor de 0, nenhuma palavra curta será removida das sugestões de termos. Se você especificar um valor alto, isso geralmente não resulta em sugestões de termos. O valor padrão é 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frequência mínima do índice </p> </td> 
      <td colname="col2"> <p> Especifica o número mínimo de vezes que uma palavra deve aparecer no índice antes de ser incluída no dicionário Você quis dizer. </p> <p>Não é possível especificar um número negativo no campo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisar termo de sugestão se não houver resultados </p> </td> 
      <td colname="col2"> <p>Pesquisa automaticamente o primeiro termo sugerido quando a pesquisa de um cliente não produz resultados e há pelo menos uma sugestão de termos Você quis dizer. </p> <p>Você pode usar as seguintes tags no modelo de apresentação para indicar que a pesquisa/comercialização do site está automaticamente procurando por um termo diferente: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>Você também pode mostrar outras sugestões aqui. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fazer sugestões devido aos baixos resultados </p> </td> 
      <td colname="col2"> <p>Se um cliente pesquisar por um termo que produza menos de dez resultados, o mecanismo de pesquisa verificará se ele tem uma sugestão que pode gerar mais de 100 resultados. Se isso ocorrer, você poderá usar as seguintes tags para indicar ao usuário que, embora ele tenha resultados, ele pode ter desejado procurar algo diferente: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> No cenário acima, o número de sugestões é controlado pelo valor especificado na contagem Padrão de sugestões a serem exibidas <span class="uicontrol"></span>. Os limites baixo e alto são configuráveis pelas opções abaixo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fazer sugestões quando os resultados iniciais forem menores que </p> </td> 
      <td colname="col2"> <p>Controla o número de resultados quando o sistema começa a oferecer sugestões. </p> <p>Essa opção aparece somente quando você marca <span class="uicontrol"> Fazer sugestões devido a baixos resultados</span>. </p> <p>O padrão é 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Uma sugestão deve gerar pelo menos tantos resultados </p> </td> 
      <td colname="col2"> <p>Filtra as sugestões que são feitas devido aos baixos resultados na pesquisa primária pela contagem de resultados. </p> <p>Essa opção aparece somente quando você marca <span class="uicontrol"> Fazer sugestões devido a baixos resultados</span>. </p> <p>O padrão é 100. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **Salvar alterações**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

