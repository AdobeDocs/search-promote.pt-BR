---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Notas de versão do Promote 15.3.1 (24/03/2015)
solution: Target
title: Search&amp;Notas de versão do Promote 15.3.1 (24/03/2015)
topic: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 15.3.1 Release Notes (03/24/2015){#search-promote-release-notes}

## New features and enhancements {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Pesquisando números de modelo de produto - Adicionada uma nova configuração de Linguística que permite, opcionalmente, dividir tokens em transições alfabéticas-numéricas. Essa funcionalidade permite correspondências de texto livre mais flexíveis em tokens de estilo de peça ou de produto.

   Consulte **[!UICONTROL Partial Alphanumeric Matching]** Configurando como os termos de pesquisa são [correspondentes ao seu conteúdo da Web...](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* Foi adicionada a capacidade de exportar resultados de exibição de dados.

   Consulte [Sobre exibições](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)de dados.

* Intervalos gerados dinamicamente para os atributos variados que têm os recursos de segmentação de valores de faceta automática.

   A Adobe Systems atualmente exige que você forneça conteúdo identificando valores de intervalo para fazer isso. Por exemplo, para um preço de 10, gere uma string de intervalo &quot;Entre $10 e $20&quot;). Ou a Adobe Systems exige que você use a Filtragem por script. Adicionados novos atributos a uma definição de campo de metadados, somente para `Type=Number` campos. As novas opções associam o campo numérico a um `Type=Text` campo e especificam informações de configuração que descrevem como a descrição do intervalo é criada.

   Consulte [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.

## Correções {#section_22D1AFC99F394D569898828A0D3C419D}

* A caixa de diálogo de edição do painel de facetas deve incluir facetas preparadas.
* Resultados de pesquisa principais vazios para o modo de pesquisa &quot;incorporado&quot;, para uma pesquisa contendo caracteres japoneses.
* A conversão tika dos arquivos .docx do Word agora preenche o `title` atributo.
* Correção de mensagens erradas de &quot;banner duplicado&quot; no **[!UICONTROL Banner]** gerenciador.
* Os banners do Dynamic Media Classic agora são agnósticos de protocolo.
* O atributo de **[!UICONTROL Table Name]** campo às vezes era oculto ao editar campos definidos pelo usuário na interface do usuário de Metadados, mesmo quando **[!UICONTROL Dynamic Facets]** era ativado para a conta.
* **[!UICONTROL Recent Searches]** não codifica mais caracteres que não sejam ASCII.
* Os campos MDI podem ser preenchidos sem precisar usar a Filtragem por script.
* Codificação incorreta em sugestões.
* O acionador &quot;outra faceta selecionada&quot; agora funciona corretamente com regras comerciais complexas.

