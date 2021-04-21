---
description: Search& amp; Notas de versão do Promote 8.14.0.
solution: Target
title: Search& amp; Notas de versão do Promote 8.14.0 (22/05/2014)
topic-legacy: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
exl-id: fcc00d85-128e-4015-aa82-7d31606cb076
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 67%

---

# Notas de versão do Search &amp; Promote 8.14.0 (22/05/2014){#search-promote-release-notes}

**Correções**

* Em caso de falha em [!DNL sqlite_open], o antigo arquivo de banco de dados sqlite é movido e um novo é criado do zero.
* Os principais resultados de pesquisa foram inconsistentes quando a mesma pesquisa foi repetida.
* Melhoria de desempenho do processamento de modelo quando há vários campos por resultado de pesquisa.
* Notas adicionadas a **[!UICONTROL Business Rule History]**.
* O desempenho dos acionadores com base em resultados e na fase de regeneração de índice com visualização de ações durante as operações de indexação, degradadas lentamente com o tempo.
* Alterada a opção **[!UICONTROL Reset SPIN cache]** de não booleano/próxima execução para três estados: não/sempre/próxima execução.
