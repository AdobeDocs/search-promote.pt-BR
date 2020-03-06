---
description: Você pode usar o Rollback para fazer backup e arquivar os índices de site que você gerou. Você também pode restaurar o backup de um índice a qualquer momento.
seo-description: Você pode usar o Rollback para fazer backup e arquivar os índices de site que você gerou. Você também pode restaurar o backup de um índice a qualquer momento.
seo-title: Sobre o Reverter para índices
solution: Target
subtopic: Rollback
title: Sobre o Reverter para índices
topic: Index,Site search and merchandising
uuid: abed878a-71b3-4122-9822-7410f4427a9a
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Sobre o Reverter para índices{#about-rollback-for-indexes}

Você pode usar [!DNL Rollback] para fazer backup e arquivar os índices de site que você gerou. Você também pode restaurar o backup de um índice a qualquer momento.

## Uso de Reversão para índices {#concept_0BC4BC975DB045A986C3607CF32705D8}

O arquivo contém quatro índices: o índice do site atual e três índices de site anteriores, que o robô de pesquisa arquiva automaticamente com base nas configurações de reversão. Cada vez que seu site é indexado, o arquivo é atualizado. Índices mais recentes substituem os índices arquivados existentes para que o arquivo sempre permaneça atual.

Cada índice arquivado é listado no arquivo com as seguintes informações:

* Data e hora em que o índice foi finalizado.
* Idade do índice.
* Número de documentos indexados.
* Tipo de operação de indexação (completo, incremental e assim por diante).
* Status do índice, como se o índice está ativo no momento e se ele será mantido ou removido após o índice seguinte.

Cada vez que seu site é indexado, o novo índice é adicionado ao arquivo e um índice arquivado existente é removido. Observe, no entanto, que o índice mais antigo não é necessariamente o que é removido. Quando um novo índice é adicionado ao arquivo, uma comparação de idade é feita de cada índice arquivado para as idades especificadas nas configurações de reversão. O índice mais afastado do agendamento desejado é removido. Por exemplo, suponha que a configuração seja 24,48,72 e que as idades dos índices salvos sejam 5, 23, 47 e 71. O índice mais recente (cinco horas de idade) é removido quando um novo índice é adicionado ao arquivo porque sua idade é mais distante das configurações. Para conveniência, o arquivo anota qual índice é removido quando o site é indexado novamente.

É possível navegar para outras áreas na interface do usuário enquanto um índice é ativado. Um indicador de status controla o progresso da ativação e está disponível quando você exibe a [!DNL Rollback] página. Se um índice arquivado for restaurado, os usuários serão notificados na parte superior das páginas Índice completo, Índice incremental, Índice com script e Regenerar. Nenhuma operação de indexação pode ocorrer enquanto um índice estiver sendo restaurado. Se uma operação de reversão entrar em conflito com um índice de site programado, a indexação programada será adiada até que a reversão seja concluída. Se um índice já estiver em andamento, ele será cancelado, desde que o usuário confirme que a prioridade de recebimento da reversão.

Para manter a integridade do arquivo, o robô de pesquisa não atualiza o arquivo de reversão se forem encontrados erros durante um rastreamento. Também não há atualização se um usuário cancelar uma operação de indexação. Se uma operação de indexação exceder o tempo máximo, bytes, páginas ou documentos, o crawler finaliza o índice e o adiciona ao arquivo. Além disso, se o número mínimo de páginas não for atendido durante uma operação de indexação, o crawler cancelará o índice e o índice anterior permanecerá ativo.

## Configurar a programação de arquivamento de rollback de índices {#task_CD403B9AE2244B13A6B3861B5F9B055C}

É possível usar [!DNL Configure] para determinar quais arquivos de índice você deseja armazenar no arquivo de rollback. O arquivo pode armazenar o índice atual e três índices de backup.

O **[!UICONTROL Schedule]** campo contém três valores separados por vírgulas que representam horas do presente. Por exemplo, os valores de programação 24,48,72 especificam 24 horas do presente ou do ontem, 48 horas do presente ou dois dias atrás e 72 horas do presente ou três dias atrás.

A pesquisa arquiva continuamente os índices do site mais próximos de um dia, dois dias e três dias. As horas e datas reais dos índices arquivados podem variar dependendo da programação de indexação do site.

**Para configurar a programação de arquivamento de rollback de índices**

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Configure]**.
1. Na [!DNL Rollback Configuration] página, no **[!UICONTROL Schedule]** campo, insira uma lista separada por comando de três páginas de índice, em horas. Os índices mais próximos a essas páginas são salvos.
1. Clique em **[!UICONTROL Save Changes]**.

## Ativar um índice arquivado {#task_5DCE3D660F6F4197993E92AA59227332}

Você pode usar Reverter para ativar um índice arquivado.

Quando você clica **[!UICONTROL Activate]** para reverter um índice, o índice ativo atual é movido para o arquivo.

Após a ativação do índice arquivado, você será redirecionado para a [!DNL Activate Index] página. As informações sobre a reversão de índice são exibidas. Além disso, a [!DNL Activate] coluna na [!DNL Available Indexes] tabela identifica o índice revertido com o status &quot;Índice ativo&quot;.

1. No menu do produto, clique em **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Rollback]**.
1. Na [!DNL Activate Index] página, na [!DNL Available Indexes] tabela, clique **[!UICONTROL Activate]** no tipo de índice arquivado associado que você deseja tornar ativo.

   Use as colunas Data, Idade, Páginas e Operação para ajudar a determinar qual índice será ativado.
1. Na [!DNL Verify Rollback] página, reveja as informações do índice para verificar se você selecionou o índice correto e clique em **[!UICONTROL Activate Now]**.

## Exibição do log de todas as reversões de índice {#task_D2D9AA7203F0465FB5AE0D49212AC41C}

Exibir a data e a hora de todas as operações relacionadas à reversão.

**Para exibir o log de todas as reversões de índice**

1. No menu do produto, execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Live Log]**.

   * Clique em **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Staged Log]**.

1. Na página de log, na parte superior ou inferior, execute um dos procedimentos a seguir:

   * Use as opções de navegação **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]****[!UICONTROL Last]** ou **[!UICONTROL Go to line]** para percorrer o log.

   * Use as opções de exibição **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** para refinar o que você vê.

