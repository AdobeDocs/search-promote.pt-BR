---
description: Use o Facet Rail para reordenar grupos de facetas em uma página da Web.
seo-description: Use o Facet Rail para reordenar grupos de facetas em uma página da Web.
seo-title: Sobre o Facet Rail
solution: Target
subtopic: Navigation
title: Sobre o Facet Rail
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: 6b3aa733b0dfaace956f0ffc25f433fefd21e15f

---


# Sobre o Facet Rail{#about-facet-rail}

Use o Facet Rail para reordenar grupos de facetas em uma página da Web.

## Uso do Facet Rail {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

Uma faceta é uma propriedade ou uma característica, É uma maneira de geralmente classificar os resultados da pesquisa. Por exemplo, o fabricante, o preço e a cor podem ser considerados um grupo de aspectos. Cada aspecto pode ter várias restrições ou valores. Por exemplo, se você tivesse cor como uma faceta, os &quot;valores da faceta&quot; poderiam ser vermelhos, laranja, amarelo, verde, azul, índigo e violeta.

Consulte [Sobre aspectos](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Use o Facet Rail para reordenar esses grupos de facetas em uma página da Web. Por exemplo, suponha que você tenha uma seção de resultados de pesquisa no lado esquerdo de uma página da Web. A seção listada, de cima para baixo, uma faceta de Categoria, uma faceta de Marca, uma faceta de Preço e uma faceta Mais Popular. Usando um painel de facetas, você pode, por exemplo, fazer com que a faceta Mais popular apareça acima ou abaixo da faceta Categoria.

O grupo de aspectos que você deseja reorganizar juntos pertence a uma tag do painel de facetas. Uma faceta só pode pertencer a um painel de facetas. O painel de facetas é uma tag de modelo de Apresentação e inclui uma única representação de uma faceta. Todas as facetas que pertencem a este trilho compartilham essa única representação de facetas.

Consulte [Sobre modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) e facetas nas tags [do modelo](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)Apresentação.

## Configurar um painel de facetas {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

Você pode adicionar um painel de facetas para personalizar a camada de apresentação. Os trilhos de face fornecem aos clientes uma Pesquisa guiada que permite que eles detalhem os resultados da pesquisa com base na ordem dos aspectos em sua página da Web.

<!-- 

t_configuring_facet_rail.xml

-->

Qualquer alteração feita nos trilhos de faceta pode ser revertida usando o recurso Histórico.

**Para configurar um painel de facetas**

1. Antes de configurar um painel de facetas, verifique se você já adicionou uma faceta e, como parte dessa tarefa, especificou um nome de painel de facetas.

   Consulte [Adicionar uma nova faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. Na [!DNL Facet Rail] página, selecione as facetas que deseja incluir no painel de facetas e, em seguida, defina a **[!UICONTROL Sort Facets Method]** opção na lista suspensa.

   <!-- 
   r_facet_rail_options.xml
   -->

   | Recurso/Opção | Descrição |
   |--- |--- |
   | Facet Rail Nome | Identifica o nome do painel de facetas.  Você cria o nome do painel de facetas no momento em que adiciona a faceta.  Consulte [Adicionar uma nova faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | Aspectos incluídos | Uma lista de possíveis aspectos que você pode selecionar para adicionar ao painel de facetas.  Se você optar por classificar facetas usando `Custom`, a ordem selecionada aqui determinará a ordem em que elas aparecem na caixa de `Custom Facet Order` texto. |
   | Método Classificar aspectos | Escolha uma das três opções a seguir na lista suspensa:<ul><li>`Alpha` Os aspectos são classificados em ordem alfabética em relação aos seus nomes, incluindo caracteres de pontuação.</li><li>`Alpha (not case sensitive)` Os aspectos são classificados em ordem alfabética em relação aos seus nomes, ignorando as letras maiúsculas e minúsculas dos caracteres alfabéticos e incluindo os caracteres de pontuação. </li><li>`Alpha (alphanumeric only)` As facetas são classificadas em ordem alfabética em relação aos seus nomes, ignorando os caracteres de pontuação. </li><li>`Alpha (not case sensitive, alphanumeric only)` As facetas são classificadas em ordem alfabética em relação aos seus nomes, ignorando as letras maiúsculas e minúsculas dos caracteres alfabéticos e ignorando os caracteres de pontuação. </li><li>`Count` As facetas são classificadas com base na contagem. </li><li>`Custom` Abre a caixa de `Custom Facet Order` texto que permite definir a ordem das facetas digitando o nome exato de cada faceta. Quaisquer rótulos de facetas deixados de fora são removidos da `Custom Facet Order` lista.</li></ul> |
   | Ordem de face personalizada | Essa opção só estará disponível se você tiver selecionado `Custom` na lista `Sort Facets Method` suspensa.  Permite listar os nomes de facetas, um por linha ou todos em uma linha e separados por vírgulas. Se os rótulos de aspecto forem definidos, eles serão mostrados na `Facets Included` lista, entre parênteses.  Não inclua rótulos de facetas na caixa de `Custom Facet Order` texto.  Quando você seleciona ou cancela a seleção de aspectos na `Facets Included` lista, a caixa de `Custom Facet Order` texto é atualizada automaticamente. |

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Na [!DNL Facet Rail] página, execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Edite o modelo de Apresentação fazendo o seguinte:

   * Crie um &quot;modelo de faceta&quot; no modelo de apresentação.
   * Envolva o &quot;modelo de faceta&quot; com as `<guided-facet-rail>` tags.

      Consulte Aspectos nas tags [do modelo de](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)Apresentação.

      Exemplo:

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      Essas tags criam uma seção do modelo de apresentação para se tornarem um padrão repetível para cada faceta no painel de facetas. Cada aspecto que pertence ao painel de facetas usa essa seção gravada para avaliar sua saída. Somente uma `<guided-facet-rail>` tag pode aparecer no modelo de apresentação final.

      As tags a seguir não precisam do `gsname` atributo dentro `<guided-facet-rail>` porque o valor é determinado dinamicamente no tempo de pesquisa e é substituído corretamente:

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * Salve o modelo de apresentação e coloque-o ao vivo.

      Consulte [Editar uma apresentação ou um modelo](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.
