---
description: Você pode usar o Rollback para fazer backup e arquivar índices de sites da Web que você gerou. Você também pode restaurar o backup de um índice a qualquer momento.
solution: Target
subtopic: Rollback
title: Sobre a reversão para índices
topic: Índice,Pesquisa e comercialização do site
uuid: abed878a-71b3-4122-9822-7410f4427a9a
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---


# Sobre a reversão para índices{#about-rollback-for-indexes}

Você pode usar [!DNL Rollback] para fazer backup e arquivar os índices de sites que gerou. Você também pode restaurar o backup de um índice a qualquer momento.

## Uso de reversão para índices {#concept_0BC4BC975DB045A986C3607CF32705D8}

O arquivo contém quatro índices: o índice de site atual e três índices de site anteriores, que o robô de pesquisa arquiva automaticamente com base nas configurações de configuração de rollback. Cada vez que seu site é indexado, o arquivo é atualizado. Os índices mais recentes substituem os índices arquivados existentes para que o arquivo sempre permaneça atual.

Cada índice arquivado é listado no arquivo com as seguintes informações:

* Data e hora em que o índice foi finalizado.
* Idade do índice.
* Número de documentos indexados.
* Tipo de operação de indexação (completo, incremental e assim por diante).
* Status do índice, como se o índice está ativo no momento e se ele será mantido ou removido após o próximo índice.

Cada vez que seu site é indexado, o novo índice é adicionado ao arquivo e um índice arquivado existente é removido. Observe, no entanto, que o índice mais antigo não é necessariamente o que foi removido. Quando um novo índice é adicionado ao arquivo, uma comparação de idade é feita de cada índice arquivado às idades especificadas nas configurações de rollback. O índice mais distante do agendamento desejado é removido. Por exemplo, suponha que a configuração seja 24,48,72 e as idades dos índices salvos sejam 5, 23, 47 e 71. O índice mais recente (cinco horas) é removido quando um novo índice é adicionado ao arquivo porque sua idade é mais distante das configurações. Para maior comodidade, o arquivo anota qual índice é removido quando o site é indexado novamente.

É possível navegar para outras áreas na interface do usuário enquanto um índice é ativado. Um indicador de status acompanha o progresso da ativação e está disponível ao visualizar a página [!DNL Rollback]. Se um índice arquivado for restaurado, os usuários serão notificados na parte superior das páginas Índice completo, Índice incremental, Índice com script e Regenerar. Nenhuma operação de indexação pode ocorrer enquanto um índice está sendo restaurado. Se uma operação de reversão entrar estiver em conflito com um índice de site programado, a indexação programada será adiada até que a reversão seja concluída. Se um índice já estiver em andamento, ele será cancelado, desde que o usuário confirme que a reversão recebe prioridade.

Para manter a integridade do arquivo, o robô de pesquisa não atualiza o arquivo de reversão se forem encontrados erros durante um rastreamento. Também não há atualização se um usuário cancelar uma operação de indexação. Se uma operação de indexação exceder o tempo máximo, bytes, páginas ou documentos, o crawler finaliza o índice e o adiciona ao arquivo. Além disso, se o número mínimo de páginas não for atendido durante uma operação de indexação, o crawler cancelará o índice e o índice anterior permanecerá ativo.

## Configurar o agendamento de arquivamento de rollback de índices {#task_CD403B9AE2244B13A6B3861B5F9B055C}

Você pode usar [!DNL Configure] para determinar quais arquivos de índice você deseja armazenar no arquivo de rollback. O arquivo pode armazenar o índice atual e três índices de backup.

O campo **[!UICONTROL Schedule]** contém três valores separados por vírgulas que representam horas a partir do presente. Por exemplo, os valores de programação de 24,48,72 especificam 24 horas desde o presente ou ontem, 48 horas desde o presente ou dois dias atrás e 72 horas desde o presente ou três dias atrás.

A pesquisa arquiva continuamente os índices do site mais próximos de um dia, dois dias e três dias. Os horários e datas reais dos índices arquivados podem variar dependendo da programação de indexação do site.

**Para configurar a programação de arquivamento de rollback de índices**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Configure]**.
1. Na página [!DNL Rollback Configuration], no campo **[!UICONTROL Schedule]**, insira uma lista separada por comandos de três idades de índice, em horas. Os índices mais próximos a essas páginas são salvos.
1. Clique em **[!UICONTROL Save Changes]**.

## Ativando um índice arquivado {#task_5DCE3D660F6F4197993E92AA59227332}

Você pode usar o Rollback para ativar um índice arquivado.

Quando você clica em **[!UICONTROL Activate]** para reverter um índice, o índice atualmente ativo é movido para o arquivo.

Após a ativação do índice arquivado, você é retornado à página [!DNL Activate Index]. As informações sobre a reversão de índice são exibidas. Além disso, a coluna [!DNL Activate] na tabela [!DNL Available Indexes] identifica o índice revertido com o status &quot;Índice ativo&quot;.

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Rollback]**.
1. Na página [!DNL Activate Index] , na tabela [!DNL Available Indexes], clique em **[!UICONTROL Activate]** para o tipo de índice arquivado associado que você deseja tornar ativo.

   Use as colunas Data, Idade, Páginas e Operação para ajudar a determinar qual índice ativar.
1. Na página [!DNL Verify Rollback] , revise as informações de índice para verificar se você selecionou o índice correto e clique em **[!UICONTROL Activate Now]**.

## Exibindo o log de todas as reversões de índice {#task_D2D9AA7203F0465FB5AE0D49212AC41C}

Exibir a data e a hora de todas as operações relacionadas à reversão.

**Para exibir o log de todas as reversões de índice**

1. No menu do produto, siga um destes procedimentos:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Live Log]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Staged Log]**.

1. Na página de log, na parte superior ou inferior, execute um dos seguintes procedimentos:

   * Use as opções de navegação **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** para percorrer o log.

   * Use as opções de exibição **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** para refinar o que você vê.

