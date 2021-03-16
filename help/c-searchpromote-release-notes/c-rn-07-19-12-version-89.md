---
description: Search& amp; Notas de versão do Promote 8.9.
solution: Target
title: Search& amp; Notas de versão do Promote 8.9 (19/07/2012)
topic: Notas de versão, Pesquisa e comercialização do site
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 65%

---


# Notas de versão do Search &amp; Promote 8.9 (19/07/2012){#search-promote-release-notes}

**Novos recursos**

* Aprimoramentos no gerenciamento de metadados – Definição dinâmica de metadados a pratir de feeds de cliente

   Criar um esquema para reconfigurar dinamicamente sua conta do Search&amp;Promote com base nas defininções de metadados fornecidas pelo cliente.
* Aprimoramento ao desempenho da indexação – Carregador de índice

   O Carregador de índice é uma nova maneira de importar conteúdo XML diretamente para um índice do Search&amp;Promote. Trata-se de um subconjunto da funcionalidade Conector de índice existente, projetado para importar rapidamente nossos arquivos de feed XML padrão.

**Correções e aprimoramentos**

* Adição de suporte para alteração da opção de classificação por uma regra comercial.
* No sistema de Ajuda, a tag `<search-description>` mostra o corpo em vez disso, quando a meta tag da descrição tem conteúdo vazio.
* Adição da capacidade de rastrear as ocorrências da tabela aplicada de resultados adicionados por meio de ações baseadas em resultados.
* Adição de suporte para envio de parâmetros de consulta via POST
* Durante o rastreamento, uma operação final mirror_account pode ser ignorada em alguns casos.
* Os URLs do Adobe Analytics não incluem argumentos CGI e o código Search &amp; Promote que faz as pesquisas do Adobe Analytics necessárias para retirar de forma semelhante os argumentos CGI das chaves de URL.
* As regras de regravação desaparecem intermitentemente da interface de usuário depois de terem sido encaminhadas para ativação.
* As contas do Search &amp; Promote com as configurações Você quis dizer que foram definidas para fazer sugestões devido a resultados baixos podem ter resultados intermitentes.
* A saída de teste da regra de regravação não tinha quebras de linha.
* As páginas Regras de URL de pesquisa e Regras de URL de armazenamento da lista de rastreamento apontavam para a página de Histórico incorreta.
* Clicar em Editar em algums banners não exibia a página Editar.
* Às vezes, a reclassificação do código de atualização podia ser extraordinariamente lenta.
* Remover ou enviar um item de faceta não funcionava se o nome da faceta usasse uma mistura de letras maiúsculas e minúsculas.

