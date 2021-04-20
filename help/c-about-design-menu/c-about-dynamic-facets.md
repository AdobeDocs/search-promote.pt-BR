---
description: Use Aspectos dinâmicos para criar novas seleções de intervalo automaticamente no momento da pesquisa. Como opção, você pode associar cada campo de aspecto dinâmico a até um nome de tabela no Adobe Search&amp;Promote account. Você aplica esses relacionamentos de tabela no tempo de pesquisa para qualquer campo de aspecto dinâmico envolvido na pesquisa.
solution: Target
subtopic: Navigation
title: Sobre aspectos dinâmicos
topic: Design,Site search and merchandising
uuid: 1ea91c22-dcc2-4173-aa50-ce618ad0a99c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---


# Sobre aspectos dinâmicos{#about-dynamic-facets}

Use Aspectos dinâmicos para criar novas seleções de intervalo automaticamente no momento da pesquisa. Como opção, você pode associar cada campo de aspecto dinâmico a até um nome de tabela em sua conta de Adobe Search &amp; Promote. Você aplica esses relacionamentos de tabela no tempo de pesquisa para qualquer campo de aspecto dinâmico envolvido na pesquisa.

## Uso de aspectos dinâmicos {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

>[!NOTE]
>
>Por padrão, esse recurso não está ativado em [!DNL Adobe Search&Promote]. Entre em contato com o Suporte Técnico para ativar o recurso para uso.

Sem o uso de Aspectos dinâmicos, era necessário mesclar atributos relacionados em &quot;slots&quot; e exibir apenas os espaços homogêneos para uma determinada pesquisa. Ou seja, eles só poderiam conter os valores de um atributo lógico, como &quot;tamanho do sapato&quot; ou &quot;tamanho do anel&quot;. Esse método forneceu desempenho adequado em tempo de pesquisa com um grande conjunto de atributos únicos.

No entanto, quando o Dynamic Faceting é usado, ele não coloca um limite no número de aspectos que a pesquisa principal pode rastrear com eficiência. Você pode definir centenas de aspectos dinâmicos, a partir dos quais a pesquisa principal pode retornar os &quot;principais `N` aspectos dinâmicos&quot; para uma determinada pesquisa, onde `N` normalmente é um valor mais modesto de 10 a 20 ou menos. Esse método elimina a necessidade de ajustar os atributos. Agora você pode criar uma faceta dinâmica exclusiva para atributos em seu site.

## Quais facetas você deveria tornar dinâmicas? {#section_254EE034BCAD4250A5D09FBF6158C4A5}

Facetas que são escassamente preenchidas em todo o seu site e aparecem somente para um subconjunto de pesquisas são bons candidatos a tornarem-se dinâmicas. Por exemplo, uma faceta chamada &quot;largura da frente&quot; só pode ser preenchida ao procurar sapatos ou botas. Enquanto outra faceta chamada &quot;Estilo numérico da face&quot;, com possíveis valores de &quot;Romano&quot; e &quot;Árabe&quot;, só pode aparecer ao procurar relógios ou relógios.

Se sua conta tiver um grande número dessas facetas, ele aprimora o desempenho da pesquisa para usar facetas dinâmicas, em vez de sempre selecionar todo o conjunto de facetas possíveis para cada pesquisa. Facetas genéricas como &quot;SKU&quot; ou &quot;marca&quot;, que normalmente são apropriadas para exibir com os resultados de cada pesquisa, normalmente não são apropriadas como facetas dinâmicas.

## Relação de aspectos para campos de meta tag {#section_2869E5FCDA8B431A87BC6E5573F2B0A0}

Os aspectos são criados sobre os campos da meta tag. Um campo de meta tag é um recurso de camada de pesquisa principal de baixo nível de [!DNL Adobe Search&Promote]. Facetas, por outro lado, são parte da GS (Pesquisa guiada), a camada de apresentação de alto nível da Search &amp; Promote de Adobe. No entanto, os campos de metatag próprios da faceta não sabem nada sobre aspectos. Ao configurar aspectos dinâmicos, você primeiro adiciona facetas e, em seguida, adiciona campos de metatag com a opção Faceta dinâmica selecionada para definir a faceta identificada como dinâmica.

>[!NOTE]
>
>Não há nenhuma configuração de &quot;Aspecto dinâmico&quot; em **[!UICONTROL Design > Navigation > Facets]**. O que torna uma faceta &quot;dinâmica&quot; é que seu &quot;campo da meta tag&quot; subjacente é dinâmico, conforme definido em **[!UICONTROL Settings > Metadata > Definitions]**.

## Exemplos de aspectos dinâmicos na ação {#section_BC699A05E2E742EF94D41679163ACE84}

Exemplo de aspectos dinâmicos que são exibidos após uma pesquisa por &quot;inicializações&quot;:

![](assets/dynamicfacets_boots.png)

Outro exemplo de aspectos dinâmicos que são exibidos após uma pesquisa por &quot;relógios&quot;:

![](assets/dynamicfacets_watches.png)

Consulte também

* [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Tags de modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Tags de modelo de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

## Configuração de aspectos dinâmicos {#task_D17F484130E448258100BAC1EEC53F39}

Configurando Aspectos Dinâmicos no Search&amp;Promote.

<!-- 

t_configuring_dynamic_facets.xml

 -->

>[!NOTE]
>
>Por padrão, esse recurso não está habilitado no Adobe Search &amp; Promote. Entre em contato com o Suporte Técnico para ativar o recurso para uso.

Antes que os efeitos dos seus aspectos dinâmicos estejam visíveis para os clientes, você deve reconstruir o índice do site.

Consulte também

* [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Tags de modelo de apresentação](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Tags de modelo de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**Para configurar aspectos dinâmicos**

1. Verifique se você já adicionou facetas.

   Consulte [Adicionar uma nova faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Após a adição dos seus aspectos, certifique-se de ter adicionado os aspectos aos novos campos de meta tag definidos pelo usuário.

   Consulte [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions.]**
1. Na página [!DNL Definitions], na tabela [!DNL User-defined fields], na coluna [!DNL Actions], clique no ícone de lápis (Editar) na linha do nome do campo da meta tag associado à faceta que você deseja tornar dinâmica.
1. Na página [!DNL Edit Field], marque **[!UICONTROL Dynamic Facet]**.

   Consulte a tabela de opções em [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Clique em **[!UICONTROL Save Changes]**.
1. Clique em **regenerar o índice de site preparado** na caixa azul para reconstruir rapidamente o índice de site preparado.

   Consulte também [Regenerando o índice de um site ativo ou temporário](../c-about-index-menu/c-about-regenerate-index.md#task_B28DE40C0E9A475ABCBCBC4FF993AACD).
1. Determine o número de aspectos dinâmicos a serem selecionados para uma determinada pesquisa. Você executa essa tarefa seguindo um destes procedimentos:

   * Crie uma regra de limpeza de consulta com as condições desejadas, que execute a ação `set`, `backend parameter`, `sp_sfvl_df_count` para o valor `X`, onde `X` é o número desejado de aspectos dinâmicos a serem solicitados no momento da pesquisa, e clique em **[!UICONTROL Add]**.

   ![](assets/querycleaningrule_dynamicfacets.png)

   Consulte [Adicionar uma regra de limpeza de consulta](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

   Consulte também [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8), linha 40 na tabela para obter mais explicações de `sp_sfvl_df_count`.

   * Adicione uma pesquisa e defina o parâmetro &quot;personalizado&quot; `sp_sfvl_df_count` para o valor desejado e clique em **[!UICONTROL Add]**.

   ![](assets/gs_addsearch_dynamic_facets.png)

   Consulte [Adicionar uma nova definição de pesquisa](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648).

   Consulte também [Parâmetros CGI de pesquisa de backend](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8), linha 40 na tabela para obter mais explicações de `sp_sfvl_df_count`.

1. Edite o modelo de transporte apropriado para exibir os aspectos dinâmicos que a pesquisa principal retorna.

   Consulte [Edição de uma apresentação ou de um modelo de transporte](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

   Por exemplo, suponha que seu modelo de transporte tenha o nome `guided.tpl`. Nesse caso, no menu do produto, clique em **[!UICONTROL Design > Templates]**. Na página [!DNL Templates] , localize `guided.tpl` na tabela. e clique em **[!UICONTROL Edit]** à direita do nome. Na página Edição , adicione o seguinte bloco de código ao final de `</facets>`: Saída JSON:

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

   Consulte [Edição de uma apresentação ou de um modelo de transporte](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

   Por exemplo, suponha que você tenha um modelo chamado `sim.tmpl` usado para produzir conteúdo no Simulador. Para editar esse modelo, no menu do produto, clique em **[!UICONTROL Design > Templates]**. Na página [!DNL Templates] , localize `sim.tmpl` na tabela. e clique em **[!UICONTROL Edit]** à direita do nome. Na página Edição , adicione o seguinte na área de exibição de faceta do modelo:

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

   Você também faria uma modificação semelhante a outros templates de Apresentação, conforme necessário, como `json.tmpl`.

   Certifique-se de especificar `__dynamic_facets` para `gsname` na tag `guided-facet-rail`. Essa tag é um painel de facetas predefinido reservado para a saída de quaisquer facetas dinâmicas que são retornadas para uma determinada pesquisa.

   Opcionalmente, também é possível editar esse painel de facetas especial por meio de **[!UICONTROL Rules > Business Rules]** e usando o **[!UICONTROL Advanced Rule Builder]**, como mostrado abaixo.

   ![](assets/dynamicfacetrail_businessrule.png)

   Consulte também [Adicionar uma nova regra de negócios](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)
