---
description: Você pode definir Frases comuns usadas em seu site para que, quando um cliente entrar em uma query de pesquisa, não precise inserir aspas em qualquer uma das frases que você definiu.
solution: Target
title: Sobre frases comuns
topic: Linguistics,Site search and merchandising
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 1%

---


# Sobre frases comuns{#about-common-phrases}

Você pode definir Frases comuns usadas em seu site para que, quando um cliente entrar em uma query de pesquisa, não precise inserir aspas em qualquer uma das frases que você definiu.

## Uso de frases comuns {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>O recurso Frase comum não aparece na interface do usuário porque não está habilitado por padrão. Entre em contato com o Suporte Técnico para ativar esse recurso para uso.

Frases comuns são uma coleção de frases com várias palavras que são reconhecidas durante a pesquisa de um cliente. Ele trata as frases como um grupo combinado de palavras em vez de palavras individuais. Quando um cliente insere uma consulta de pesquisa em seu site, ele pode identificar frases ao redor dos termos com aspas duplas, como &quot;Oceano Pacífico&quot;. No entanto, quando você adiciona grupos de frases comuns, as etapas de aspas são executadas automaticamente para o cliente, à medida que ele encontra frases correspondentes na query de pesquisa.

Por exemplo, suponha que um cliente de seu site insira a seguinte consulta de pesquisa:

`hotels near the pacific ocean`

Sem a adição de aspas em `pacific ocean`, a pesquisa do cliente retorna os resultados para hotéis próximos a qualquer oceano no mundo, o que não é o que o cliente desejava.

No entanto, quando você adiciona a frase comum &quot;Oceano Pacífico&quot;, sua consulta de pesquisa é convertida automaticamente para o seguinte:

`hotels near the "pacific ocean"`

O uso de Frases comuns não impede que seus clientes usem aspas explicitamente em torno de frases de palavras. Em vez disso, simplesmente adiciona aspas, quando essas frases definidas são encontradas em sua consulta de pesquisa.

Essa expansão da consulta de pesquisa se aplica aos parâmetros CGI da pesquisa de backend `sp_q` e `sp_q_#`,

Consulte as linhas da tabela 25, 26 e 32 em [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Adicionar um grupo de frases comum {#task_35C84FABCD9042C5B48C5C788B752871}

Você pode adicionar Grupos de frases comuns para garantir que as consultas de pesquisa retornem com precisão as páginas da Web que tenham todas as palavras, na ordem e proximidade exatas, que um cliente digitou.

À medida que você adiciona Grupos de frases comuns, pode usar o recurso Localizar na página principal do Grupo de frases comuns. O recurso Localizar permite que você pesquise uma frase existente e descubra em qual grupo ela reside.

Consulte [Localização de grupos que contêm palavras específicas em uma frase](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E).

**Para adicionar um grupo Frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na página [!DNL Common Phrases Groups], clique em **Adicionar grupo de frases**.
1. Na página [!DNL Add Common Phrase Group] , defina as opções desejadas e adicione todas as frases que compõem o grupo.

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
      <td colname="col2"> <p>Obrigatório. </p> <p>O nome exclusivo do Grupo de Frases Comuns. </p> <p>Se você editar um Grupo de frases comuns posteriormente, observe que não pode alterar o Nome do grupo. Para alterar o Nome do grupo, use o recurso <span class="uicontrol"> Renomear</span>. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> Renomeando um Grupo de Frases Comum</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Notas </p> </td> 
      <td colname="col2"> <p>Opcional. </p> <p>Adicione informações que pertencem ao Grupo de frases comuns. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frases </p> </td> 
      <td colname="col2"> <p>Obrigatório. </p> <p>Permite que você especifique uma frase até um máximo de cinco palavras. Para ajustar a configuração máxima de palavras, entre em contato com o Suporte técnico. </p> <p>Cada frase inserida deve ser exclusiva em qualquer Grupo de frases comuns. </p> <p>Use os ícones de mais (+) e menos (-) na coluna Ação para adicionar a frase inserida ou excluir uma frase. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Clique em **Adicionar**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Teste de uma frase comum {#task_A0C344E051CA45A9A0588242F9DA675D}

Se você selecionou campos de metadados para associar a um grupo de frases, é possível testar a expansão de uma frase específica.

Ao testar a expansão de uma frase, você pesquisa uma frase exata em relação aos campos de metadados associados ao grupo de frases. A frase é pesquisada como se tivesse aspas em torno dela. Todos os outros campos de metadados pesquisam apenas as palavras dentro da frase, sem as aspas. Por exemplo, suponha que você tenha testado a frase `audi TT`. Os resultados retornados podem aparecer da seguinte maneira:

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**Para testar uma frase comum**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na página [!DNL Common Phrases Groups], no campo de texto **Frase de teste que contém**, digite a frase cuja expansão de metadados você deseja testar.
1. Clique em **[!UICONTROL Test]**.

   Os resultados da expansão são exibidos na caixa de texto.
1. (Opcional) Arraste o canto inferior direito da caixa de texto para expandir a região de exibição.

## Encontrar grupos que contêm palavras específicas em uma frase {#task_20714969274740A7BB4DC71E705EA15E}

Você pode usar [!DNL Find] para pesquisar por palavras específicas em uma frase entre todos os grupos existentes que você adicionou.

Ao usar Localizar, ele localiza o seguinte:

* Onde a mesma frase é encontrada entre todos os grupos.
* Qualquer uma das palavras na frase entre todos os grupos, independentemente da palavra ordem e proximidade na frase.

Consulte também [Editar um Grupo de Frases Comuns](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61).

**Para encontrar grupos que contenham palavras específicas em uma frase**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na página [!DNL Common Phrases Groups], no campo de texto **[!UICONTROL Find groups with phrases that contain]**, digite uma frase.
1. Clique em **[!UICONTROL Find]**.

   Os resultados são exibidos na caixa de texto.
1. (Opcional) Siga um ou mais destes procedimentos:

   * Arraste o canto inferior direito da caixa de texto para expandir a região de exibição.
   * Na janela de resultados, clique em uma frase com hiperlink para abrir a página Editar Grupo de Frases Comuns do grupo associado.

## Editar um grupo de frases comum {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

É possível editar os Campos, Notas e Frases existentes de um grupo de frases comum que você adicionou. No entanto, para editar o Nome do grupo, você deve usar o recurso [!DNL Rename].

Consulte também [Renomeando um grupo de frases comum](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB).

**Para editar um grupo de Frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na página [!DNL Common Phrases Groups] , clique em **[!UICONTROL Edit]** à direita de um nome de grupo.
1. Na página [!DNL Edit Common Phrase Group], defina as opções desejadas.

   Consulte a tabela de opções em [Adicionar um grupo de frases comum](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871).
1. Clique em **Salvar alterações**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Renomear um grupo de frases comum {#task_168E07C59C0F40989D43E7010EFF22EB}

Você pode alterar o nome de um Grupo de Frases Comuns existente. No entanto, se você quiser alterar os Campos, Notas e Frases existentes de um grupo de frases comum, deverá usar o recurso [!DNL Edit].

Consulte [Editar um grupo de frases comum](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61) .

**Para renomear um grupo de Frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na página [!DNL Common Phrases Groups] , clique em **[!UICONTROL Rename]** à direita de um nome de grupo.
1. Na página [!DNL Rename Common Phrase Group], no campo de texto **[!UICONTROL Group Name]**, digite o novo nome do grupo.
1. Clique em **Renomear**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo um Grupo de Frases Comuns {#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

É possível excluir qualquer Grupo de frases comuns adicionado. Se você excluir um grupo por engano, é possível usar [!DNL History] para restaurar o grupo.

Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

**Para excluir um grupo de Frases comuns**

1. No menu do produto, clique em **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Na página [!DNL Common Phrases Groups] , clique em **[!UICONTROL Delete]** à direita de um nome de grupo.
1. Na página [!DNL Delete Common Phrase Group], clique em **[!UICONTROL Delete]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

