---
description: Use Aspectos dinâmicos para criar novas seleções de intervalo automaticamente no momento da pesquisa. Como opção, você pode associar cada campo de aspecto dinâmico a até um nome de tabela na sua conta do Adobe Search&amp;Promote. Você aplica essas relações de tabela em tempo de pesquisa para quaisquer campos de aspecto dinâmico envolvidos na pesquisa.
seo-description: Use Aspectos dinâmicos para criar novas seleções de intervalo automaticamente no momento da pesquisa. Como opção, você pode associar cada campo de aspecto dinâmico a até um nome de tabela na sua conta do Adobe Search&amp;Promote. Você aplica essas relações de tabela em tempo de pesquisa para quaisquer campos de aspecto dinâmico envolvidos na pesquisa.
seo-title: Sobre aspectos dinâmicos
solution: Target
subtopic: Navigation
title: Sobre aspectos dinâmicos
topic: Design,Site search and merchandising
uuid: 1ea91c22-dcc2-4173-aa50-ce618ad0a99c
translation-type: tm+mt
source-git-commit: 4270ea66ba645ad0f71c9c8b5c2a1fcc6eb02ad2

---


# Sobre aspectos dinâmicos{#about-dynamic-facets}

Use Aspectos dinâmicos para criar novas seleções de intervalo automaticamente no momento da pesquisa. Como opção, você pode associar cada campo de aspecto dinâmico a até um nome de tabela na sua conta do Adobe Search&amp;Promote. Você aplica essas relações de tabela em tempo de pesquisa para quaisquer campos de aspecto dinâmico envolvidos na pesquisa.

## Usando aspectos dinâmicos {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

>[!NOTE]
>
>Por padrão, esse recurso não está ativado em [!DNL Adobe Search&Promote]. Entre em contato com o suporte técnico para ativar o recurso para uso.

Sem o uso de Aspectos dinâmicos, era necessário unir atributos relacionados em &quot;slots&quot; e exibir apenas os slots homogêneos para uma determinada pesquisa. Ou seja, eles poderiam conter apenas os valores de um atributo lógico, como &quot;tamanho do sapato&quot; ou &quot;tamanho do anel&quot;. Este método proporcionou um desempenho adequado em tempo de pesquisa com um grande conjunto de atributos exclusivos.

No entanto, quando o Dynamic Faceting é usado, ele não coloca um limite no número de aspectos que a pesquisa principal pode rastrear com eficiência. Você pode definir centenas de aspectos dinâmicos, a partir dos quais a pesquisa principal pode retornar as &quot;principais facetas `N` dinâmicas&quot; para uma determinada pesquisa, onde normalmente `N` é um valor mais modesto de 10 a 20 ou menos. Esse método elimina a necessidade de alocar os atributos - agora você pode criar uma faceta dinâmica exclusiva para atributos em seu site.

## Que facetas você deveria fazer dinâmicas? {#section_254EE034BCAD4250A5D09FBF6158C4A5}

As facetas que são escassamente preenchidas em seu site e que aparecem somente para um subconjunto de pesquisas são bons candidatos para tornar dinâmicas. Por exemplo, uma faceta chamada &quot;largura da frente&quot; só pode ser preenchida quando se procura sapatos ou botas. Enquanto outra faceta chamada &quot;Estilo numérico da face&quot;, com possíveis valores de &quot;Romano&quot; e &quot;Árabe&quot;, só pode aparecer ao procurar relógios ou relógios.

Se sua conta tiver um grande número dessas facetas, isso aprimora o desempenho da pesquisa para usar facetas dinâmicas em vez de sempre selecionar o conjunto completo de possíveis aspectos para cada pesquisa. Aspectos genéricos, como &quot;SKU&quot; ou &quot;marca&quot;, que normalmente são apropriados para exibição com os resultados de cada pesquisa, normalmente não são apropriados como aspectos dinâmicos.

## Relação entre aspectos e campos de meta tag {#section_2869E5FCDA8B431A87BC6E5573F2B0A0}

As facetas são criadas sobre os campos da meta tag. Um campo de tag meta é um recurso de camada de pesquisa principal de baixo nível [!DNL Adobe Search&Promote]. As facetas, por outro lado, fazem parte do GS (Pesquisa guiada), a camada de apresentação de alto nível do Adobe Search&amp;Promote. No entanto, os próprios campos de meta tag do Facebook não conhecem nada sobre aspectos. Ao configurar aspectos dinâmicos, você primeiro adiciona aspectos e, em seguida, adiciona campos de tag meta com a opção Aspecto dinâmico selecionada para definir a faceta identificada como dinâmica.

>[!NOTE]
>
>Não há configuração &quot;Aspecto dinâmico&quot; em **[!UICONTROL Design > Navigation > Facets]**. O que torna uma faceta &quot;dinâmica&quot; é que seu &quot;campo de tag meta&quot; subjacente é dinâmico conforme definido em **[!UICONTROL Settings > Metadata > Definitions]**.

## Exemplos de aspectos dinâmicos em ação {#section_BC699A05E2E742EF94D41679163ACE84}

Exemplo de aspectos dinâmicos que são exibidos após uma pesquisa por &quot;inicializações&quot;:

![](assets/dynamicfacets_boots.png)

Outro exemplo de aspectos dinâmicos que são exibidos após uma pesquisa por &quot;relógios&quot;:

![](assets/dynamicfacets_watches.png)

Consulte também

* [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Tags de modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Tags de modelo de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

## Configuração de aspectos dinâmicos {#task_D17F484130E448258100BAC1EEC53F39}

Configuração de Aspectos Dinâmicos no Search&amp;Promotoe.

<!-- 

t_configuring_dynamic_facets.xml

 -->

>[!NOTE]
>
>Esse recurso não está ativado no Adobe Search&amp;Promote, por padrão. Entre em contato com o suporte técnico para ativar o recurso para uso.

Antes que os efeitos de seus aspectos dinâmicos sejam visíveis para os clientes, você deve recriar o índice do site.

Consulte também

* [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Tags de modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Tags de modelo de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**Para configurar aspectos dinâmicos**

1. Verifique se você já adicionou aspectos.

   Consulte [Adicionar uma nova faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Depois que seus aspectos forem adicionados, verifique se você adicionou os aspectos aos novos campos de meta tag definidos pelo usuário.

   Consulte [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.
1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions.]**
1. Na [!DNL Definitions] página, na [!DNL User-defined fields] tabela, na [!DNL Actions] coluna, clique no ícone de lápis (Editar) na linha do nome do campo da tag meta associada à faceta que você deseja tornar dinâmica.
1. Na [!DNL Edit Field] página, marque **[!UICONTROL Dynamic Facet]**.

   Consulte a tabela de opções em [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.
1. Clique em **[!UICONTROL Save Changes]**.
1. Clique em **regenerar o índice** de site preparado na caixa azul para recriar rapidamente o índice de site preparado.

   Consulte também [Regenerando o índice de um site](../c-about-index-menu/c-about-regenerate-index.md#task_B28DE40C0E9A475ABCBCBC4FF993AACD)ao vivo ou em etapas.
1. Determine o número de aspectos dinâmicos a serem selecionados para uma determinada pesquisa. Você realiza essa tarefa executando um dos seguintes procedimentos:

   * Crie uma regra de limpeza de consulta com quaisquer condições desejadas, que execute a ação `set`, `backend parameter`, `sp_sfvl_df_count` para valorizar `X`, onde `X` é o número desejado de aspectos dinâmicos a serem solicitados no momento da pesquisa e clique em **[!UICONTROL Add]**.
   ![](assets/querycleaningrule_dynamicfacets.png)

   Consulte [Adicionar uma regra](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54)de limpeza de consulta.

   Consulte também Parâmetros [CGI de pesquisa](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)de backend, linha 40 na tabela para obter mais explicações sobre `sp_sfvl_df_count`.

   * Adicione uma pesquisa e defina o parâmetro &quot;personalizado&quot; `sp_sfvl_df_count` para o valor desejado e clique em **[!UICONTROL Add]**.
   ![](assets/gs_addsearch_dynamic_facets.png)

   Consulte [Adicionar uma nova definição](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648)de pesquisa.

   Consulte também Parâmetros [CGI de pesquisa](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)de backend, linha 40 na tabela para obter mais explicações sobre `sp_sfvl_df_count`.

1. Edite o modelo de transporte apropriado para exibir os aspectos dinâmicos que a pesquisa principal retorna.

   Consulte [Editar uma apresentação ou um modelo](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.

   Por exemplo, suponha que seu modelo de transporte tenha o nome `guided.tpl`. Nesse caso, no menu do produto, clique em **[!UICONTROL Design > Templates]**. Na [!DNL Templates] página, localize `guided.tpl` a tabela. e clique **[!UICONTROL Edit]** na extremidade direita do nome. Na página Edição, adicione o seguinte bloco de código ao final de `</facets>`: Saída JSON:

   ```
   ... 
   }<search-dynamic-facet-fields>, 
           { 
               "name" : "<search-dynamic-facet-field-name>", 
               "dynamic-facet" : 1, 
               "values" : [<search-field-value-list quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
               "counts" : [<search-field-value-list quotes="yes" commas="yes" data="results" sortby="values" />] 
   
           }</search-dynamic-facet-fields> 
   ...
   ```

1. Edite o modelo ou modelos de apresentação apropriados para exibir as facetas dinâmicas.

   Consulte [Editar uma apresentação ou um modelo](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.

   Por exemplo, suponha que você tenha um modelo chamado `sim.tmpl` que seja usado para produzir conteúdo no Simulador. Para editar esse modelo, no menu do produto, clique em **[!UICONTROL Design > Templates]**. Na [!DNL Templates] página, localize `sim.tmpl` a tabela. e clique **[!UICONTROL Edit]** na extremidade direita do nome. Na página Edição, adicione o seguinte dentro da área de exibição da faceta do modelo:

   ```
   <h6>DF RAIL</h6> 
   <guided-facet-rail gsname="__dynamic_facets"> 
               <guided-facet ><!-- behavior=Normal --> 
               <div class="facet-block" id="facet"> 
               <p><b><guided-facet-display-name /></b></p> 
               <ul> 
                   <guided-facet-values> 
                       <guided-if-facet-value-equals-length-threshold> 
               </ul> 
               <ul id="brand" style="display:none"> 
                       </guided-if-facet-value-equals-length-threshold> 
                       <guided-if-facet-value-selected> 
                           <li><guided-facet-value> [<guided-lt>a href="<guided-facet-value-undo-path />"<guided-gt>X</a>]</li> 
                       <guided-else-facet-value-selected> 
                           <li><guided-facet-link><guided-facet-value></guided-facet-link> (<guided-facet-count>) </li> 
                       </guided-if-facet-value-selected> 
                   </guided-facet-values> 
               </ul> 
               <guided-if-facet-long> 
                 <br /><guided-lt />a href="#" onclick="moreless(this,'brand');return false;" <guided-gt /><button style="font-size:10px;">VIEW MORE</button></a> 
               </guided-if-facet-long> 
               </div> 
               </guided-facet> 
   </guided-facet-rail> 
   <h6>/DF RAIL</h6>
   ```

   Você também faria uma modificação semelhante a outros modelos de Apresentação, conforme necessário, como `json.tmpl`.

   Certifique-se de especificar `__dynamic_facets` para o `gsname` na `guided-facet-rail` tag . Esta tag é um painel de facetas predefinido reservado para a saída de quaisquer facetas dinâmicas que são retornadas para uma determinada pesquisa.

   Você também pode, opcionalmente, editar esse painel de facetas especial por meio de Regras > Regras de negócios e usando o Construtor de regras avançado, conforme mostrado abaixo.

   ![](assets/dynamicfacetrail_businessrule.png)

   Consulte também [Adicionar uma nova regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)