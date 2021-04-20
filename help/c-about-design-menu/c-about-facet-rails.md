---
description: Use o Facet Rail para reorganizar grupos de facetas em uma página da Web.
solution: Target
subtopic: Navigation
title: Sobre o Facet Rail
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 1%

---


# Sobre o Facet Rail{#about-facet-rail}

Use o Facet Rail para reorganizar grupos de facetas em uma página da Web.

## Uso do Facet Rail {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

Uma faceta é uma propriedade ou característica, é uma maneira de categorizar os resultados da pesquisa. Por exemplo, fabricante, preço e cor podem ser considerados um grupo de facetas. Cada faceta pode ter várias restrições ou valores. Por exemplo, se você tivesse cor como uma faceta, os &quot;valores da faceta&quot; poderiam ser vermelhos, laranja, amarelo, verde, azul, índio e violeta.

Consulte [Sobre facetas](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Você usa o Facet Rail para reordenar esses grupos de facetas em uma página da Web. Por exemplo, suponha que você tenha uma seção de resultados de pesquisa no lado esquerdo de uma página da Web. A seção listada, de cima para baixo, uma faceta Categoria, uma faceta Marca, uma faceta Preço e uma faceta Mais Popular. Usando um painel de facetas, você pode, por exemplo, ter a faceta Mais popular exibida acima ou abaixo da faceta Categoria.

O grupo de facetas que você deseja reorganizar pertencem a uma tag do painel de facetas. Uma faceta só pode pertencer a um painel de facetas. O painel de facetas é uma tag do modelo de Apresentação e engloba uma única representação de uma faceta. Todas as facetas que pertencem a esse painel compartilham essa única representação de faceta.

Consulte [Sobre modelos](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) e Faceta em [Tags de modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

## Configurar um painel de facetas {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

Você pode adicionar um painel de facetas para personalizar a camada de apresentação. Os painéis de facetas fornecem aos clientes uma Pesquisa guiada que permite que eles detalhem os resultados da pesquisa com base na ordem dos aspectos na sua página da Web.

<!-- 

t_configuring_facet_rail.xml

-->

Todas as alterações feitas nos painéis de faceta podem ser revertidas usando o recurso Histórico .

**Para configurar um painel de facetas**

1. Antes de configurar um painel de facetas, verifique se já adicionou uma faceta e, como parte dessa tarefa, especificou um nome de painel de faceta.

   Consulte [Adicionar uma nova faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. No menu do produto, clique em **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. Na página [!DNL Facet Rail], selecione as facetas que deseja incluir no painel de facetas e defina a opção **[!UICONTROL Sort Facets Method]** na lista suspensa.

   <!-- 
   r_facet_rail_options.xml
   -->

   | Recurso/Opção | Descrição |
   |--- |--- |
   | Facet Rail Nome | Identifica o nome do painel de facetas.  Você cria o nome do painel de facetas no momento em que adiciona a faceta.  Consulte [Adicionar uma nova faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | Aspectos incluídos | Uma lista de possíveis aspectos que você pode selecionar para adicionar ao painel de facetas.  Se você optar por classificar facetas usando `Custom`, a ordem em que você seleciona facetas aqui determina a ordem em que elas aparecem na caixa de texto `Custom Facet Order`. |
   | Método Classificar Aspectos | Escolha uma das três opções a seguir na lista suspensa:<ul><li>`Alpha` As facetas são classificadas em ordem alfabética em relação a seus nomes, incluindo caracteres de pontuação.</li><li>`Alpha (not case sensitive)` As facetas são classificadas em ordem alfabética em relação aos nomes, ignorando o caso de caracteres alfabéticos e incluindo caracteres de pontuação. </li><li>`Alpha (alphanumeric only)` As facetas são classificadas em ordem alfabética em relação a seus nomes, ignorando caracteres de pontuação. </li><li>`Alpha (not case sensitive, alphanumeric only)` As facetas são classificadas em ordem alfabética em relação a seus nomes, ignorando o caso de caracteres alfabéticos e ignorando caracteres de pontuação. </li><li>`Count` As facetas são classificadas com base na contagem. </li><li>`Custom` Abre a caixa de  `Custom Facet Order` texto que permite definir a ordem das facetas, inserindo o nome exato de cada faceta. Quaisquer rótulos de faceta deixados de fora são removidos da lista `Custom Facet Order`.</li></ul> |
   | Ordem de Faceta Personalizada | Essa opção só estará disponível se você tiver selecionado `Custom` na lista suspensa `Sort Facets Method`.  Permite listar nomes de facetas, um por linha ou todos em uma linha e separados por vírgulas. Se os rótulos de faceta forem definidos, eles serão mostrados na lista `Facets Included`, entre parênteses.  Não inclua rótulos de aspecto na caixa de texto `Custom Facet Order`.  Ao selecionar ou desmarcar aspectos na lista `Facets Included`, a caixa de texto `Custom Facet Order` é atualizada automaticamente. |

1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Na página [!DNL Facet Rail] , execute um dos seguintes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Edite o modelo de Apresentação fazendo o seguinte:

   * Crie um &quot;modelo de faceta&quot; no modelo de apresentação.
   * Marque o &quot;modelo de faceta&quot; com as tags `<guided-facet-rail>`.

      Consulte Facetas em [Tags do modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

      Exemplo:

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      Essas tags fazem uma seção do modelo de apresentação para se tornarem um padrão repetível para cada faceta no painel de facetas. Cada faceta que pertence ao painel de facetas usa essa seção gravada para avaliar seu resultado. Somente uma tag `<guided-facet-rail>` pode aparecer no modelo de apresentação final.

      As tags a seguir não precisam do atributo `gsname` dentro de `<guided-facet-rail>` porque o valor é determinado dinamicamente no tempo de pesquisa e é substituído corretamente:

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * Salve o template de apresentação e coloque-o online.

      Consulte [Edição de uma apresentação ou de um modelo de transporte](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).
