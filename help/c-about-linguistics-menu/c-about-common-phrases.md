---
description: Você pode definir Frases comuns usadas em seu site para que, quando um cliente entrar em uma consulta de pesquisa, não precise digitar aspas em torno de nenhuma das frases que você definiu.
seo-description: Você pode definir Frases comuns usadas em seu site para que, quando um cliente entrar em uma consulta de pesquisa, não precise digitar aspas em torno de nenhuma das frases que você definiu.
seo-title: Sobre frases comuns
solution: Target
title: Sobre frases comuns
topic: Linguistics,Site search and merchandising
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: 8efa90ac2927b263b7d48ccbf25d4b0e917dac79

---


# Sobre frases comuns{#about-common-phrases}

Você pode definir Frases comuns usadas em seu site para que, quando um cliente entrar em uma consulta de pesquisa, não precise digitar aspas em torno de nenhuma das frases que você definiu.

## Uso de frases comuns {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>O recurso Frase comum não aparece na interface do usuário porque não está ativado por padrão. Entre em contato com o suporte técnico para ativar este recurso para uso.

Frases comuns são uma coleção de frases com várias palavras que são reconhecidas durante a pesquisa de um cliente. Ele trata as frases como um grupo combinado de palavras em vez de palavras individuais. Quando um cliente entra em uma consulta de pesquisa em seu site, ele pode identificar frases ao redor dos termos com aspas duplas, como &quot;Oceano Pacífico&quot;. No entanto, quando você adiciona grupos de frases comuns, as etapas de cotação são executadas automaticamente para o cliente, pois ele encontra frases correspondentes na consulta de pesquisa.

Por exemplo, suponha que um cliente do seu site insira a seguinte consulta de pesquisa:

`hotels near the pacific ocean`

Sem a adição de aspas por aí `pacific ocean`, a pesquisa do cliente retorna os resultados para hotéis próximos a qualquer oceano do mundo, o que não é o que o cliente pretendia.

No entanto, quando você adiciona a frase comum &quot;Oceano Pacífico&quot;, sua consulta de pesquisa é automaticamente convertida no seguinte:

`hotels near the "pacific ocean"`

O uso de frases comuns não impede que seus clientes usem aspas explicitamente em torno de frases de palavras. Em vez disso, ele simplesmente adiciona aspas, quando essas frases definidas são encontradas em suas consultas de pesquisa.

Esta expansão da consulta de pesquisa aplica-se aos parâmetros CGI de pesquisa de backend `sp_q` e `sp_q_#`,

Consulte as linhas da tabela 25, 26 e 32 nos parâmetros [CGI de pesquisa](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)de backend.

## Adicionando um grupo de frases comuns {#task_35C84FABCD9042C5B48C5C788B752871}

Você pode adicionar Grupos de frases comuns para garantir que as consultas de pesquisa retornem com precisão as páginas da Web que tenham todas as palavras, na ordem e proximidade exatas, digitadas por um cliente.

À medida que você adiciona Grupos de frases comuns, você pode usar o recurso Localizar na página principal do Grupo de frases comuns. O recurso Localizar permite que você pesquise por uma frase existente e descubra em qual grupo ela reside.

Consulte [Encontrar grupos que contêm palavras específicas em uma frase](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E).

**Para adicionar um grupo de frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na [!DNL Common Phrases Groups] página, clique em **Adicionar grupo** de frases.
1. Na [!DNL Add Common Phrase Group] página, defina as opções desejadas e adicione todas as frases que compõem o grupo.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome do grupo </p> </td> 
      <td colname="col2"> <p>Obrigatório. </p> <p>O nome exclusivo do Grupo de frases comuns. </p> <p>Se você editar um Grupo de frases comuns mais tarde, observe que não é possível alterar o Nome do grupo. Para alterar o Nome do grupo, use o recurso <span class="uicontrol"> Renomear</span> . </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> Renomeando um grupo</a>de frases comuns. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Notas </p> </td> 
      <td colname="col2"> <p>Opcional. </p> <p>Adicione informações relacionadas ao Grupo de frases comuns. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frases </p> </td> 
      <td colname="col2"> <p>Obrigatório. </p> <p>Permite que você especifique uma frase até um máximo de cinco palavras. Para ajustar a configuração máxima de palavras, entre em contato com o suporte técnico. </p> <p>Cada frase inserida deve ser exclusiva em qualquer Grupo de frases comuns. </p> <p>Use os ícones de mais (+) e menos (-) na coluna Ação para adicionar a frase inserida ou excluir uma frase. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **Adicionar**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Teste de uma frase comum {#task_A0C344E051CA45A9A0588242F9DA675D}

Se você selecionou campos de metadados para associar a um grupo de frases, é possível testar a expansão de uma frase específica.

Ao testar a expansão de uma frase, você pesquisa uma frase exata em relação aos campos de metadados associados ao grupo de frases. A frase é pesquisada como se tivesse aspas ao seu redor. Todos os outros campos de metadados pesquisam apenas as palavras dentro da frase, sem as aspas. Por exemplo, suponha que você testou a frase `audi TT`. Os resultados retornados podem ser exibidos da seguinte maneira:

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**Para testar uma frase comum**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na [!DNL Common Phrases Groups] página, na frase de **teste que contém** o campo de texto, digite a frase cuja expansão de metadados você deseja testar.
1. Clique em **[!UICONTROL Test]**.

   Os resultados da expansão são exibidos na caixa de texto.
1. (Opcional) Arraste o canto inferior direito da caixa de texto para expandir a região de exibição.

## Encontrar grupos que contêm palavras específicas em uma frase {#task_20714969274740A7BB4DC71E705EA15E}

Você pode usar [!DNL Find] para pesquisar palavras específicas em uma frase entre todos os grupos existentes que você adicionou.

Quando você usa Localizar, ele localiza o seguinte:

* Onde a mesma frase é encontrada entre todos os grupos.
* Qualquer uma das palavras na frase entre todos os grupos, independentemente da palavra ordem e proximidade na frase.

Consulte também [Editando um Grupo](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61)de frases comuns.

**Para localizar grupos que contêm palavras específicas em uma frase**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na [!DNL Common Phrases Groups] página, no campo de **[!UICONTROL Find groups with phrases that contain]** texto, digite uma frase.
1. Clique em **[!UICONTROL Find]**.

   Os resultados são exibidos na caixa de texto.
1. (Opcional) Execute um ou mais dos procedimentos a seguir:

   * Arraste o canto inferior direito da caixa de texto para expandir a região de exibição.
   * Na janela de resultados, clique em uma frase hipervinculada para abrir a página Editar grupo de frases comuns do grupo associado.

## Edição de um grupo de frases comuns {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

É possível editar os campos, as observações e as frases existentes de um grupo de frases comum que você adicionou. Entretanto, para editar o Nome do grupo, é necessário usar o [!DNL Rename] recurso.

Consulte também [Renomeando um Grupo](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB)de frases comuns.

**Para editar um grupo de frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na [!DNL Common Phrases Groups] página, clique **[!UICONTROL Edit]** na extremidade direita do nome de um grupo.
1. Na [!DNL Edit Common Phrase Group] página, defina as opções desejadas.

   Consulte a tabela de opções em [Adicionar um grupo](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871)de frases comuns.
1. Clique em **Salvar alterações**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Renomeando um Grupo de Frases Comuns {#task_168E07C59C0F40989D43E7010EFF22EB}

Você pode alterar o nome de um Grupo de frases comuns existente. No entanto, se você quiser alterar os campos, notas e frases existentes de um grupo de frases comum, use o [!DNL Edit] recurso.

Consulte [Editando um grupo](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61) de frases comuns.

**Para renomear um grupo de frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na [!DNL Common Phrases Groups] página, clique **[!UICONTROL Rename]** na extremidade direita do nome de um grupo.
1. Na [!DNL Rename Common Phrase Group] página, no campo de **[!UICONTROL Group Name]** texto, digite o novo nome do grupo.
1. Clique em **Renomear**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo um Grupo de Frases Comuns {#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

Você pode excluir qualquer Grupo de frases comuns que tenha adicionado. Se você excluir um grupo por engano, poderá usar [!DNL History] para restaurar o grupo.

Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

**Para excluir um grupo de frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na [!DNL Common Phrases Groups] página, clique **[!UICONTROL Delete]** na extremidade direita do nome de um grupo.
1. Na [!DNL Delete Common Phrase Group] página, clique em **[!UICONTROL Delete]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

