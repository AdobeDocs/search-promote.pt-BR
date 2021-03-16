---
description: Search& amp; Notas de versão do Promote 15.3.1.
solution: Target
title: Search& amp; Notas de versão do Promote 15.3.1 (24/03/2015)
topic: Notas de versão, Pesquisa e comercialização do site
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Notas de versão do Search &amp; Promote 15.3.1 (24/03/2015){#search-promote-release-notes}

## Novos recursos e melhorias {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Pesquisando números de modelos de produtos - Adição de uma nova configuração de Linguística que permite dividir tokens em transições alfabéticas e numéricas. Essa funcionalidade permite correspondências de texto livre mais flexíveis em tokens de estilo de produto ou de peça.

   Consulte **[!UICONTROL Partial Alphanumeric Matching]** em [Configuração da correspondência dos termos de pesquisa com o conteúdo da Web...](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* Adição da capacidade de exportar resultados de visualização de dados.

   Consulte [Sobre visualizações de dados](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

* Intervalos gerados dinamicamente para recursos de divisão de valores de faceta automática de atributos variados.

   Atualmente, o Adobe Systems exige que você forneça conteúdo identificando valores de intervalo para fazer isso. Por exemplo, para um preço de 10, gere uma string de intervalo &quot;Entre $10 e $20&quot;). Ou, o Adobe Systems requer que você use a Filtragem por script. Adição de novos atributos a uma definição de campo de metadados, somente para campos `Type=Number`. As novas opções associam o campo numérico a um campo `Type=Text` e especificam as informações de configuração que descrevem como a descrição do intervalo é criada.

   Consulte [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Correções {#section_22D1AFC99F394D569898828A0D3C419D}

* A caixa de diálogo de edição do painel de facetas deve incluir aspectos preparados.
* Resultados de pesquisa principal vazios para o modo de pesquisa &quot;incorporado&quot;, para uma pesquisa contendo caracteres japoneses.
* A conversão Tika de arquivos .docx do Word agora preenche o atributo `title`.
* Correção de mensagens incorretas de &quot;banner duplicado&quot; no gerenciador **[!UICONTROL Banner]**.
* [!DNL Dynamic Media Classic] banners agora são independentes de protocolo.
* O atributo de campo **[!UICONTROL Table Name]** às vezes ficava oculto ao editar campos definidos pelo usuário na interface do usuário de Metadados, mesmo quando **[!UICONTROL Dynamic Facets]** estava habilitado para a conta.
* **[!UICONTROL Recent Searches]** O não codifica mais caracteres não ASCII que sejam codificados com vários caracteres.
* Os campos MDI podem ser preenchidos sem recurso à Filtragem com script.
* Codificação incorreta em sugestões.
* O acionador &quot;outra faceta selecionada&quot; agora funciona corretamente com regras comerciais complexas.

