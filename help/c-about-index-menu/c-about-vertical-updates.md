---
description: Você pode usar a Atualização vertical para atualizar rapidamente partes do índice sem precisar processar grandes quantidades de dados.
solution: Target
subtopic: Vertical Update
title: Sobre atualização vertical
topic-legacy: Index,Site search and merchandising
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
exl-id: 8d6a48c0-377d-4a15-bddc-c67e28037bfc
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Sobre a atualização vertical{#about-vertical-update}

Você pode usar a Atualização vertical para atualizar rapidamente partes do índice sem precisar processar grandes quantidades de dados.

## Usando a Atualização Vertical {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

Um índice vertical demora apenas alguns segundos para ser executado e é útil em sites de comércio eletrônico de grande capacidade que podem levar muitas horas para índice completo ou incremental.

Ao gerar um índice vertical, as informações de status são exibidas, como tempo de início, tempo decorrido e erros durante o processo de indexação.

Você pode interromper ou reiniciar o processo de indexação vertical a qualquer momento.

Embora o novo índice vertical atualize seu site ativo, os clientes podem continuar a pesquisar seu site usando seu índice atual.

>[!NOTE]
>
>Por padrão, esse recurso não está ativado em [!DNL Adobe Search&Promote]. Entre em contato com o Suporte Técnico para ativar o recurso para uso.

As Atualizações verticais devem ser usadas especificamente em contas [!DNL Adobe Search&Promote] no estilo de comércio eletrônico que usam IndexConnector para fornecer o conteúdo do índice de pesquisa. O caso de uso típico é aquele em que o índice [!DNL Adobe Search&Promote] representa um catálogo de produtos pesquisável e a necessidade existe para poder atualizar rapidamente os valores que mudam com frequência, como inventário em estoque, disponibilidade e/ou preço. Uma Atualização Vertical é semelhante a um Índice Incremental, exceto que atualiza apenas partes de cada documento, enquanto um Índice Incremental substitui documentos inteiros por novas versões.

O termo &quot;Atualização vertical&quot; refere-se à noção de que um índice [!DNL Adobe Search&Promote] pode ser visualizado como uma tabela em colunas, com cada coluna correspondente a uma definição de campo de Metadados [!DNL Adobe Search&Promote] e cada linha correspondente a um documento. O processo de Atualização vertical substitui uma ou mais colunas sem a necessidade de alterar qualquer conteúdo das outras colunas.

Sempre que a fonte principal de conteúdo, um feed IndexConnector, contiver todos os elementos de dados necessários para criar o índice, o feed de Atualização Vertical será um subconjunto do feed principal, um que usa o mesmo &quot;schema&quot; IndexConnector para definir os elementos de dados, mas que contém *only* os itens de dados que precisam ser atualizados.

No mínimo, o feed de Atualização vertical precisa conter o elemento &quot;chave primária&quot; (conforme identificado com a caixa de seleção **Chave primária** na configuração IndexConnector) e pelo menos um elemento de dados a ser atualizado.

Por exemplo, um feed IndexConnector principal pode ser semelhante ao seguinte (mas geralmente com muitos mais itens de dados):

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <title><![CDATA[Title for product 123]]></title>
  <description><![CDATA[Description for product 123.]]></description>
  <price>3.99</price>
  <link><![CDATA[https://www.somewhere.com/products/123]]></link>
  <image><![CDATA[https://www.somewher.com/images/products/123.jpg]]></image>
  <label><![CDATA[PROD123]]></label>
  <inventory>100</inventory>
  <brand><![CDATA[brand123]]></brand>
  ...
</product>
<product>
...
</product>
</products>
```

Um requisito é poder atualizar rapidamente apenas os valores `<price>` e `<inventory>`, pois esses valores podem mudar rapidamente no site do cliente. Um feed de atualização vertical pode ser semelhante ao seguinte:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <price>3.50</price>
  <inventory>90</inventory>
</product>
<product>
...
</product>
</products>
```

Normalmente, essas informações são armazenadas em um arquivo separado no servidor do cliente e a configuração &quot;Caminho de arquivo vertical&quot; do IndexConnector aponta para esse arquivo. O processo de Atualização Vertical lê esse novo conteúdo e atualiza o índice [!DNL Adobe Search&Promote] existente, atualizando apenas os valores para `<price>` e `<inventory>`, neste caso. Pesquisas subsequentes retornam o conteúdo recém-atualizado.

>[!NOTE]
Neste exemplo, os campos `<price>` e `<inventory>` Metadados precisarão ter sido definidos com a opção **Campo de atualização vertical** marcada.

Consulte também [Sobre o controle remoto para indexação](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F) e [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Configurar uma atualização vertical de um site preparado {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

Você pode configurar quais fontes do Conector de índice deseja incluir na atualização vertical especificando URLs.

**Para configurar uma Atualização vertical de um site preparado**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Configuration]**.
1. Na página **[!UICONTROL Vertical Update Configuration]** , no campo Atualizar URLs , especifique os URLs das páginas que deseja indexar.

   O robô de pesquisa atualiza apenas os documentos identificados nas fontes especificadas do Conector de Índice.

   Este campo deve conter URLs do Conector de índice somente como no exemplo a seguir:

   `index:product_catalog`.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Exibindo o log de Atualização Vertical de um site ativo ou temporário {#task_E668E1F1240C476DAA1CA783DC728232}

Quando uma Atualização Vertical ao Vivo ou uma Atualização Vertical Preparada estiver concluída, você poderá exibir seu log associado para solucionar quaisquer erros que possam ter ocorrido.

Não é possível exportar arquivos de log de Atualização Vertical, nem salvá-los. O arquivo de log permanece disponível para exibição até que o próximo índice ocorra.

**Para exibir o log de Atualização Vertical de um site ativo ou temporário**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Live Log]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Staged Log]**.

1. Na página de log, na parte superior ou inferior, execute um dos seguintes procedimentos:

   * Use as opções de navegação **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** para percorrer o log.

   * Use as opções de exibição **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** para refinar o que você vê.
