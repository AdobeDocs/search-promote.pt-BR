---
description: Você pode configurar a opção Você quis dizer para que os clientes recebam sugestões para termos de pesquisa válidos quando tentarem pesquisas que falharam. As sugestões são formadas procurando por ortografia e digitando correções nos termos de pesquisa que resultam em uma pesquisa válida.
solution: Target
title: Sobre Você quis dizer
topic: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 2%

---


# Sobre você quis dizer{#about-did-you-mean}

Você pode configurar a opção Você quis dizer para que os clientes recebam sugestões para termos de pesquisa válidos quando tentarem pesquisas que falharam. As sugestões são formadas procurando por ortografia e digitando correções nos termos de pesquisa que resultam em uma pesquisa válida.

## Configurar Você quis dizer {#task_B539D6A0043547EFB1CA19B67E762371}

Você pode adaptar como [!DNL site search/merchandising] faz sugestões de pesquisa quando um query de cliente retorna nenhum ou mínimo resultados de pesquisa.

<!-- 

t_configuring_did_you_mean.xml

 -->

**Para configurar, você quis dizer**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**.
1. Na página [!DNL Did You Mean], no campo de texto **Remover essas palavras de sugestões**, insira espaço ou palavras separadas por linha para filtrar sugestões indesejáveis.

   Essas são palavras no seu índice de pesquisa que não aparecem como termos de pesquisa alternativos recomendados. É possível excluir qualquer palavra que corresponda a um padrão por meio do uso de expressões regulares. Caso contrário, apenas a palavra exata será removida.

1. Defina as opções **Você quis dizer** que deseja.

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
      <td colname="col2"> <p>Ajusta o alcance do software para encontrar sugestões. Se um usuário cometer um erro de uma letra, todos os algoritmos receberão as mesmas sugestões. O motivo é que basta uma edição para chegar a uma sugestão funcional e todos os algoritmos encontram palavras próximas ao original. Mas quando os termos de pesquisa originais não são semelhantes aos termos existentes no índice, os <b>Deep</b> e <b>Ortografia inválida</b> Algoritmos de Sugestão continuam a procurar possíveis sugestões. Esse cenário é útil se um cliente tentar um nome próprio difícil de digitar e exibir os nomes. No entanto, se você quiser que apenas sugestões semelhantes sejam exibidas, poderá escolher o algoritmo <b>Quick</b>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Contagem padrão de sugestões a serem mostradas </p> </td> 
      <td colname="col2"> <p>Especifica o número de sugestões de termos Você quis dizer (0-20) que deseja mostrar quando a pesquisa de um cliente não retorna resultados. O padrão é 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comprimento mínimo da palavra de sugestão </p> </td> 
      <td colname="col2"> <p>Prunes quis dizer termos especificando o número mínimo de letras de uma palavra sugerida. </p> <p>Por exemplo, se você definir o valor como 4, o software não sugerirá uma palavra com 1, 2 ou 3 caracteres. Se você especificar um valor de 0, nenhuma palavra curta será removida das sugestões de termo. Se você especificar um valor alto, isso geralmente não resulta em sugestões de termos. O valor padrão é 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frequência mínima do índice </p> </td> 
      <td colname="col2"> <p> Especifica o número mínimo de vezes que uma palavra deve aparecer no índice antes de ser incluída no dicionário Você quis dizer. </p> <p>Não é possível especificar um número negativo no campo . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisar termo de sugestão se não houver resultados </p> </td> 
      <td colname="col2"> <p>Pesquisa automaticamente pelo primeiro termo sugerido quando a pesquisa de um cliente não produz resultados e há pelo menos uma sugestão de termo Você quis dizer. </p> <p>Você pode usar as seguintes tags no modelo de apresentação para indicar que a pesquisa/comercialização do site está procurando automaticamente por um termo diferente: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>Você também pode mostrar outras sugestões aqui. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fazer sugestões devido aos baixos resultados </p> </td> 
      <td colname="col2"> <p>Se um cliente pesquisar por um termo que produza menos de dez resultados, o mecanismo de pesquisa verificará se ele tem uma sugestão que pode produzir mais de 100 resultados. Se isso acontecer, você poderá usar as seguintes tags para indicar ao usuário que, embora tenha resultados, ele pode ter desejado procurar outra coisa: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> No cenário acima, o número de sugestões é controlado pelo valor especificado em <span class="uicontrol"> Contagem padrão de sugestões para mostrar</span>. Os limites baixo e alto são configuráveis pelas opções abaixo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fazer sugestões quando os resultados iniciais forem menores que </p> </td> 
      <td colname="col2"> <p>Controla o número de resultados quando o sistema começa a oferecer sugestões. </p> <p>Essa opção aparece somente quando você marca <span class="uicontrol"> Fazer sugestões devido a baixos resultados</span>. </p> <p>O padrão é 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Uma sugestão deve gerar pelo menos tantos resultados </p> </td> 
      <td colname="col2"> <p>Filtra as sugestões feitas devido aos baixos resultados na pesquisa principal por sua contagem de resultados. </p> <p>Essa opção aparece somente quando você marca <span class="uicontrol"> Fazer sugestões devido a baixos resultados</span>. </p> <p>O padrão é 100. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **Salvar alterações**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

