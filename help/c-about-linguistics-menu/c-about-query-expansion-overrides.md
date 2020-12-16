---
description: Você pode substituir a expansão dos resultados do query de pesquisa.
seo-description: Você pode substituir a expansão dos resultados do query de pesquisa.
seo-title: Sobre substituições de expansão de Query
solution: Target
title: Sobre substituições de expansão de Query
topic: Linguistics,Site search and merchandising
uuid: dfe18004-b8fd-4889-b01c-72a3b0c82b9c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---


# Sobre substituições de expansão de Query{#about-query-expansion-overrides}

Você pode substituir a expansão dos resultados do query de pesquisa.

## Usando substituições de expansão de Query {#concept_6895B469B0E044299E93361BFA06B554}

Quando você configura uma substituição de expansão de query, cria um conjunto de &quot;regras&quot;. Cada regra diz, essencialmente, &quot;Não expanda `<this>` para `<that>` no momento da pesquisa&quot;, onde `<this>` é uma palavra ou frase de texto simples e `<that>` é uma palavra ou frase de texto, ou uma classificação.

>[!NOTE]
>
>Por padrão, esse recurso não está ativado no Search &amp; Promote. Entre em contato com o suporte técnico para ativar o recurso para uso. Depois que o recurso Substituições de expansão de Query for ativado, você deverá &quot;ativá-lo&quot; na interface do usuário.

**Como funciona uma Substituição de Expansão de Query**

Quando um valor de Texto e Termo é especificado na página Adicionar substituições de expansão de Query, o código atua no emparelhamento específico. Quando um tipo de classificação é especificado como um Termo, como Dicionários ou Forms do Word Alternativo, o valor Não Expandir não é convertido em nenhum formulário criado pela classificação indicada.

Por exemplo, suponha que você tenha a seguinte definição:

`Do Not Expand = "dog"`

`Type = Text`

`Term = "dogs"`

Um query de busca por &quot;cachorro&quot;, que se expande para incluir &quot;cães&quot; e &quot;cães&quot; por meio do Alternate Word Forms, não incluiria &quot;cães&quot;.

No entanto, se a definição for a seguinte:

`Do Not Expand = "dog"`

`Type = Alternate Word Forms`

O query não inclui &quot;cães&quot; ou &quot;cães&quot; (o Forms alternativo disponível para &quot;cães&quot;).

É possível especificar vários termos, várias classificações ou ambos. No entanto, se você selecionar Todos como o Tipo, qualquer lista de vários termos será recolhida para apenas uma única entrada &quot;Todos&quot;.

Se as entradas de Texto e classificação estiverem misturadas em qualquer regra, elas serão reorganizadas na interface do usuário para mostrar os valores de texto primeiro. Mas isso não implica nem afeta a ordem de avaliação no momento da busca.

Os termos de texto são validados para remover referências sem significado. Ou seja, compara o termo com o valor Não expandir e remove o termo se houver uma correspondência. Além disso, os valores de Termo do duplicado, seja texto ou classificação, são removidos.

Se você adicionar uma nova regra com um valor Não Expandir replicando uma definição anterior, os Termos da nova definição serão adicionados ao original.

## Configurando substituições de expansão de Query {#task_A087354A509D4997BA275186C224160E}

Definir e adicionar uma Substituição de Expansão de Query no Search &amp; Promote.

<!-- 

t_configuring_query_expansion_overrides.xml

 -->

>[!NOTE]
Por padrão, esse recurso não está ativado no Search &amp; Promote. Entre em contato com o suporte técnico para ativar o recurso para uso. Depois que o recurso Substituições de expansão de Query for ativado, você deverá &quot;ativá-lo&quot; na interface do usuário. Os primeiros passos abaixo descrevem como fazer isso.

**Para configurar substituições de expansão de Query**

1. No Search &amp; Promote, clique em **Configurações** > **Usuário** > **Funções de Visualização**.
1. Na página Funções de Visualização, na coluna Ações da tabela, clique em **Editar** à direita da função que você deseja conceder acesso às Substituições de Expansão de Query no menu Linguística.
1. Na página Editar função, expanda a árvore Linguística.
1. Marque **Substituições de expansão de Query** e clique em **Salvar alterações**.
1. Clique em **Linguística** > **Substituições de expansão de Query**.
1. Clique em **Adicionar substituições de expansão de Query**.
1. Na página Adicionar substituições de expansão de Query, defina as opções desejadas.

   <!-- 
   
   r_query_expansion_override_definitions.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Não Expandir </p> </td> 
      <td colname="col2"> <p>Especifica a palavra ou frase que você não deseja expandir. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo </p> </td> 
      <td colname="col2"> <p>Selecione <b>Texto</b> para especificar um emparelhamento de palavras ou frases específico. Ou selecione uma classificação para especificar que a palavra ou frase Não expandir não é convertida por meio da classificação selecionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Termo </p> </td> 
      <td colname="col2"> <p>Disponível somente se você selecionou <b>Texto</b> como o Tipo. Especifica a palavra ou frase a ser excluída da expansão de pesquisa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ação </p> </td> 
      <td colname="col2"> <p> Clique em <b>+</b> ou <b>-</b> para adicionar ou excluir Termos, respectivamente, à definição. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Quando terminar, clique em **Adicionar**.

   Na página Definições de substituições de expansão de Query, é possível editar ou excluir as definições adicionadas.
1. Para pré-visualização dos resultados de suas adições, clique em **regenerar o índice do site preparado** na caixa azul para recriar rapidamente o índice do site preparado.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **Live**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)

   * Clique em **Empurrar ao vivo**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

