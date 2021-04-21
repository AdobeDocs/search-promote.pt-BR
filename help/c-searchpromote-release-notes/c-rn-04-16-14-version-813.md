---
description: Search& amp; Notas de versão do Promote 8.13.0.
solution: Target
title: Search& amp; Notas de versão do Promote 8.13.0 (16/04/2014)
topic-legacy: Release Notes,Site search and merchandising
uuid: b3524992-ff00-4a7c-a404-078242456734
exl-id: cba582ad-d388-4317-af06-b8b12b300f02
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 57%

---

# Notas de versão do Search &amp; Promote 8.13.0 (16/04/2014){#search-promote-release-notes}

| Novo recurso e aprimoramento | Descrição |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aspectos dinâmicos com suporte total à tabela correspondente | Alguns clientes tinham muitos atributos de &quot;nível SKU&quot; que queriam selecionar e exibir por meio de Aspectos dinâmicos. Sendo assim, agora existe a opção de associar cada campo de aspecto dinâmico com até um nome de tabela em uma configuração de conta estática. Essas relações entre tabelas podem então ser aplicadas em uma pesquisa para qualquer campo de aspecto dinâmico envolvido na pesquisa. Consulte [Sobre Fatos Dinâmicos](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899). |

**Correções**

* Alteração do campo de descrição da exibição de dados para usar a tag `<search-display-field>` em vez de `<search-description>`.
* Adição de um recurso dentro do Conector de índice para tornar a Chave primeira o encadeamento de dois ou mais campos.
* Alteração do script AttributeLoader-Regen-Enabled `attributeloader-regen.pl`. Não possui mais valores codificados em HTML.
* Tempo de índice e tempo de busca de caractere invisível agora são correspondentes para consultas de pesquisa de variedades.
* A adição de uma regra empresarial poderia resultar em um erro quando os Aspectos dinâmicos estavam habilitados.

   Consulte [Sobre as Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Um erro de Javascript impedia adicionar ou editar uma definição em **Settings** > **SPIN** > **IndexConnector**.
* Depois que uma Regra de negócios era salva, parecia que, quando a hora era selecionada durante a criação da Regra de negócios, ela usava o fuso horário GMT como padrão. Após a regra ser salva, o fuso horário da conta aparecia corretamente.

   Consulte [Sobre as Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* A classificação das regras empresariais não estava funcionando corretamente.

   Consulte [Sobre as Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* O relatório de desempenho de pesquisa for aprimorado e agora é possível agendar relatórios para entregas de emails.
* A programação fixa de regras empresariais estava mudando automaticamente para o horário de verão.

   Consulte [Sobre as Regras de Negócios](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Se um grande número de campos de faceta dinâmicos foi definido, os usuários experimentaram tempos de resposta de pesquisa de núcleo lento.
* Falsos erros de índice de intervalo estavam ocorrendo.
* O acesso ao Dynamic Media Classic em data centers não norte-americanos estava interrompido.
* A função de validação SPIN XPath exibia um erro falso-positivo.

* O usuário era redirecionado para a página de logon de membros após habilitar/desabilitar o SPIN.
