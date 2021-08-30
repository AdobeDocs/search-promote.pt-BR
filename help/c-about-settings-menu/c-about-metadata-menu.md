---
description: Use o menu Metadados para personalizar as Definições de pesquisa e as injeções de índice.
solution: Target
subtopic: Metadata
title: Sobre o menu Metadados
topic-legacy: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
exl-id: 53d62da9-c5bd-4c4a-bb89-743704f66f7f
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '8028'
ht-degree: 1%

---

# Sobre o menu Metadados{#about-the-metadata-menu}

Use o menu Metadados para personalizar as Definições de pesquisa e as injeções de índice.

## Sobre definições {#concept_AE48035C210145169BE067D396975620}

Você pode usar [!DNL Definitions] para personalizar o conteúdo e a relevância dos campos HTML e metadados que são considerados quando um cliente envia uma consulta de pesquisa.

É possível editar os campos que já estão predefinidos. Ou também é possível criar novos campos definidos pelo usuário com base no conteúdo da tag de metadados. Cada definição é exibida em uma única linha na página [!DNL Staged Definitions].

Consulte também [Sobre visualizações de dados](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

## Adição de um novo campo de meta tag {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

Você pode definir e adicionar seus próprios campos de tag de metadados.

Antes que os efeitos da nova definição de meta tag sejam visíveis para os clientes, você deve reconstruir o índice do site.

**Para adicionar um novo campo de meta tag**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Na página [!DNL Definitions], clique em **[!UICONTROL Add New Field]**.
1. Na página [!DNL Add Field], defina as opções desejadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome do campo </p> </td> 
      <td colname="col2"> <p>Especifica um nome que é usado para fazer referência ao campo. </p> <p>O nome do campo deve seguir as seguintes regras: </p> <p> 
      <ul id="ul_D39D09CD7E7D41A59ECB6C5A6F4F263D"> 
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> O nome deve conter somente caracteres alfanuméricos. </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> Os traços são permitidos no nome, mas nenhum espaço. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> É possível inserir um nome com até 20 caracteres. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> O nome não diferencia maiúsculas de minúsculas, mas é exibido e armazenado exatamente como você digita. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> Não é possível usar os nomes que existem nos campos predefinidos conforme vistos na tabela na página <span class="wintitle"> Definições Preparadas </span> . </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> Não é possível usar a palavra "any" como o valor de um nome de campo definido pelo usuário. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> Não é possível editar os nomes dos campos predefinidos. </li> 
      </ul> </p> <p> Exemplos de nome de campo: </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> autor </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> PublicarData </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> algo selvagem </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome(s) da Meta Tag </p> </td> 
      <td colname="col2"> <p>Determina o conteúdo associado ao campo definido. </p> <p>A lista de nomes pode ter até 255 caracteres. E o nome pode conter qualquer caractere permitido no atributo name de uma meta tag HTML. </p> <p>Você pode especificar várias metatags em uma única definição de campo. </p> <p>Vários valores devem ser separados por vírgulas, e o nome da meta tag mais à esquerda encontrado em qualquer página da Web tem prioridade. </p> <p>Por exemplo, suponha que você tenha definido um campo chamado "auth". O nome do campo tem as metatags associadas "author, dc.author". Nesse caso, o conteúdo da meta tag "author" é indexado e pesquisado sobre o do "dc.author" se ambas as meta tags forem exibidas em uma página da Web. </p> <p>Os campos definidos pelo usuário devem ter pelo menos um nome de meta tag em sua definição. Campos predefinidos não precisam ter uma meta tag associada. No entanto, se uma ou mais meta tags forem especificadas, o conteúdo das meta tags substituirá a fonte de dados atual para cada tag. </p> <p>Por exemplo, se a meta tag "dc.title" estiver associada ao campo "title" predefinido, o conteúdo da meta tag "dc.title" será indexado sobre o conteúdo da tag "dc.title" 
      <code>
        &lt;title&gt; 
      </code> para qualquer documento específico. </p> <p>Exemplos incluem: </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> descrição </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> marca própria </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo de dados </p> </td> 
      <td colname="col2"> <p>Cada campo tem um tipo de dados associado, como texto, número, data, versão, classificação ou local. Esse tipo de dados determina como o conteúdo do campo é indexado, pesquisado e, opcionalmente, classificado. </p> <p>Não é possível alterar o tipo de dados depois de criar a definição do campo. </p> <p>Use as informações a seguir para ajudar a selecionar o tipo de dados relevante para as informações que o campo contém. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> Os campos do tipo  </span> de dados de texto são tratados como cadeias de caracteres. </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> Os campos do tipo  </span> de dados Number são tratados como valores numéricos inteiros ou de ponto flutuante. </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> Os campos do tipo  </span> de dados de data são tratados como especificadores de data/hora. Você pode personalizar os formatos de data/hora permitidos ao adicionar ou editar o novo campo. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> Os campos do tipo  </span> de dados da versão são tratados como dados numéricos de forma livre. Por exemplo, 1.2.3 classifica antes de 1.2.2. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> Os campos de tipo de  </span> dados de classificação são tratados da mesma forma que os campos de tipo "Número", exceto que eles também influenciam os cálculos de classificação/relevância nos resultados da pesquisa. <p>Consulte <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">Sobre regras de classificação </a>. </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> Os campos do tipo de  </span> dados de localização são tratados como um local físico em qualquer lugar do mundo. Os formatos de localização permitidos incluem: <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> Códigos postais de 5 ou 9 dígitos, na forma de DDDD ou DDDDD, em que cada "D" é de 0 a 9 dígitos. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> Códigos de área de três dígitos na forma de DDD. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> Pares de latitude/longitude na forma ±DD.DDDD±DDD.DDDD, onde o primeiro número especifica a latitude e o segundo número especifica a longitude. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>lista de permissões </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Texto </span> ou <span class="uicontrol"> Número </span> estiver selecionado. </p> <p>Indexar valores separados no conteúdo de metadados desse campo. </p> <p>Por exemplo, o conteúdo "Vermelho, Amarelo, Verde, Azul" é tratado como quatro valores separados em vez de um quando "Listas de permissões" é selecionado. Esse tratamento é mais útil com pesquisa de intervalo (usando 
      <code>
        sp_q_min 
      </code>, 
      <code>
        sp_q_max 
      </code>, ou 
      <code>
        sp_q_exact 
      </code>) e com o 
      <code>
        &lt;search-field-value-list&gt; 
      </code>, 
      <code>
        &lt;search-field-values&gt; 
      </code>, e 
      <code>
        &lt;search-display-field-values&gt; 
      </code>. </p> <p>Não disponível se o tipo de dados Versão estiver selecionado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Aspecto dinâmico </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>Observação: Esse recurso não é habilitado por padrão. Entre em contato com o Suporte Técnico para ativá-lo para uso. Depois de ativada, ela é exibida na interface do usuário do . </p> </p> <p>Define a faceta identificada como dinâmica. </p> <p>Os aspectos são criados sobre os campos da meta tag. Um campo de meta tag é uma camada de pesquisa principal de baixo nível do Search &amp; Promote de Adobe. Facetas, por outro lado, são parte da GS (Pesquisa guiada), a camada de apresentação de alto nível da Search &amp; Promote de Adobe. No entanto, os campos de metatag próprios da faceta não sabem nada sobre aspectos. </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Sobre Aspectos Dinâmicos </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Permitir Dedução </p> </td> 
      <td colname="col2"> <p>Marque essa opção para ativar a desduplicação desse campo. Ou seja, permita que esse campo seja especificado no tempo de pesquisa por meio da variável 
        <code>
          sp_dedupe_field 
        </code> Parâmetro CGI de pesquisa. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Pesquisar parâmetros CGI </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome da tabela </p> </td> 
      <td colname="col2"> <p>Associa permanentemente o determinado campo ao nome de tabela fornecido. </p> <p>Sempre que esse campo for mencionado em um parâmetro CGI de pesquisa principal ou em uma tag de modelo, o nome da tabela será fornecido automaticamente. Esse recurso permite a seleção de aspectos dinâmicos por meio de correspondências de tabela, mas você também pode usá-la em campos de faceta não dinâmicos, se desejar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Delimitadores de lista </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Listas de permissões </span> estiverem selecionadas. </p> <p>Especifica quais caracteres separam valores de lista individuais. É possível especificar vários caracteres, cada um dos quais é tratado como um separador de valor. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesquisar por padrão </p> </td> 
      <td colname="col2"> <p>Quando selecionado, o conteúdo do campo é pesquisado mesmo quando o campo não é explicitamente especificado em uma determinada query de pesquisa. Se você desmarcar essa opção, o campo será pesquisado somente quando solicitado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Campo de atualização vertical </p> </td> 
      <td colname="col2"> <p> <p>Observação: Esse recurso não é habilitado por padrão. Entre em contato com o Suporte Técnico para ativá-lo para uso. Depois de ativada, ela é exibida na interface do usuário do . </p> </p> <p>Define o campo identificado como sendo um campo de Atualização vertical. </p> <p>Os campos de Atualização Vertical são candidatos a serem atualizados por meio do processo de Atualização Vertical ( <span class="uicontrol"> Índice </span> &gt; <span class="uicontrol"> Atualização Vertical </span>.) Devido à forma como as Atualizações Verticais são feitas, o conteúdo desses campos não pode ser pesquisado em pesquisas de texto livre. Marcar essa opção faz com que o conteúdo desse campo não seja adicionado ao índice "word" durante qualquer tipo de operação de índice. Ela também permite a atualização desse campo durante uma operação de Atualização Vertical. </p> <p>Para saber mais sobre Atualizações Verticais, consulte <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Sobre Atualização Vertical </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Relevância </p> </td> 
      <td colname="col2"> <p>É possível editar a relevância dos campos predefinidos e definidos pelo usuário. </p> <p>A relevância é especificada na escala 1-10. Uma configuração de 1 significa que é a menos relevante e 10 é a mais relevante. Esses valores são considerados quando o software considera que a consulta corresponde em cada campo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação </p> </td> 
      <td colname="col2"> <p>Especifica quando os resultados são classificados pelo campo nomeado, por meio do 
        <code>
          sp_s 
        </code> Parâmetro CGI de pesquisa. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Pesquisar parâmetros CGI </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Idioma  </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Classificação </span>, <span class="uicontrol"> Número </span> ou <span class="uicontrol"> Data </span> estiver selecionado. </p> <p>Controla as convenções de idioma e local que são aplicadas ao indexar a data, o número e os valores de classificação para este campo. </p> <p>Você pode optar por aplicar o idioma da conta (Linguística &gt; Palavras e idiomas). Ou você pode aplicar o idioma associado ao documento que contém cada número ou valor de data ou um idioma específico. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato(s) de data </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Date </span> estiver selecionado. </p> <p>Controla os formatos de data reconhecidos ao indexar valores de data para esse campo. </p> <p>Uma lista padrão de cadeias de caracteres de formato de data é fornecida para cada campo de data. Você pode adicionar à lista ou editar a lista para atender às necessidades de seu próprio site. </p> <p>Consulte <a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> Formatos de data </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formatos de data do teste </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Data </span> estiver selecionado como o Tipo de dados. </p> <p>Permite que você visualize os formatos de data especificados para garantir que eles estejam formatados corretamente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuso Horário </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Data </span> estiver selecionado como o Tipo de dados. </p> <p>Controla o fuso horário assumido que é aplicado ao indexar valores de data para esse campo que não especificam um fuso horário. </p> <p>Por exemplo, se o fuso horário da sua conta estiver definido como "América/Los Angeles" e você selecionar <span class="uicontrol"> Usar Fuso Horário da Conta </span>, o seguinte valor de meta data, que não tem um fuso horário especificado, será tratado como se fosse Horário do Pacífico, contabilizando o horário de verão: </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor de Classificação Menos Importante </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Classificação </span> estiver selecionado como o Tipo de dados. </p> <p>Controla o valor de classificação que representa a classificação mínima de qualquer documento. </p> <p>Se as classificações do documento variam de 0 para a classificação mais baixa a 10 para a classificação mais alta, você definirá esse valor como 0. </p> <p>Se as classificações do documento variam de 1 para a classificação mais alta a 10 para a classificação mais baixa, você definirá esse valor como 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor da Classificação Padrão </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Classificação </span> estiver selecionado como o Tipo de dados. </p> <p>Controla o valor de classificação usado se um documento não contiver nenhuma das meta tags definidas para esse campo de classificação. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor de Classificação Mais Importante </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Classificação </span> estiver selecionado como o Tipo de dados. </p> <p>Controla o valor de classificação que representa a classificação máxima de qualquer documento. </p> <p>Se as classificações do documento variam de 0 para a classificação mais baixa a 10 para a classificação mais alta, você definirá esse valor como 10. </p> <p>Se as classificações do documento variam de 1 para a classificação mais alta a 10 para a classificação mais baixa, você definirá esse valor como 1. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Unidades padrão </p> </td> 
      <td colname="col2"> <p>Disponível somente se o tipo de dados <span class="uicontrol"> Local </span> estiver selecionado como o Tipo de dados. </p> <p>Controla o tratamento dos valores de distância para pesquisas de proximidade. </p> <p>Se você definir as unidades padrão como <span class="uicontrol"> Milhas </span>, qualquer critério de distância mínima/máxima de pesquisa de proximidade aplicado a este campo (por meio da 
      <code>
        sp_q_min[_#] 
      </code> ou o 
      <code>
        sp_q_max[_#] 
      </code> Parâmetros CGI de pesquisa) são tratados como milhas, caso contrário, como quilômetros. </p> <p>Essa opção também controla as unidades de distância padrão aplicadas à saída do 
      <code>
        &lt;Search-Display-Field&gt; 
      </code> marca de modelo de resultados de pesquisa quando aplicada a um campo de saída de pesquisa de proximidade. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Sobre pesquisa de proximidade </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Criar descrição do intervalo? </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Número </span> estiver selecionado como o Tipo de dados. </p> <p>Controla a criação automática de descrições de Intervalo de campo, para uso com <span class="uicontrol"> Design </span> &gt; <span class="uicontrol"> Navegação </span> &gt; <span class="uicontrol"> Facets </span>. </p> <p>Consulte <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> Sobre as facetas </a>. </p> <p> <p>Observação:  Se este campo tiver <span class="uicontrol"> Campo de atualização vertical </span> marcado, o campo de descrição Intervalo de campo gerado será atualizado durante uma atualização vertical. No entanto, é recomendável que o campo identificado em <span class="uicontrol"> Campo de intervalo </span> também tenha <span class="uicontrol"> Campo de atualização vertical </span> marcado. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Campo de intervalo </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado. </p> <p>O campo <span class="uicontrol"> Texto </span> a ser atualizado com descrições de intervalo do campo atual. Esta lista contém todos os campos <span class="uicontrol"> Texto </span> que ainda não estão sendo usados com outros campos para geração de Intervalo de campo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valores do intervalo </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Uma lista de pontos de dados delimitada por branco a ser usada ao criar as descrições de Intervalo de campo. Por exemplo: </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>É possível inserir esses valores em qualquer ordem. Os valores são classificados e as duplicatas são removidas antes de serem salvas. Também é possível especificar valores negativos e não inteiros. </p> <p>Para cada valor deste campo: 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">se o valor for menor que (&lt;) o menor valor em <span class="uicontrol"> Valores do Intervalo </span>, o <span class="uicontrol"> Formato "Menor que" </span> será usado </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">se o valor for maior ou igual a (&gt;=) o maior valor em <span class="uicontrol"> Valores do Intervalo </span>, será usado o <span class="uicontrol"> Formato "Maior que" </span>. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">caso contrário, um "intervalo" é encontrado onde o valor do campo fica entre dois <span class="uicontrol"> Valores do Intervalo </span> consecutivos (maior que (&gt;) o valor menor e menor que ou igual a (&lt;=) o valor maior) e o <span class="uicontrol"> Formato Intermédio </span> é usado. </li> 
    </ul> </p> <p>Por exemplo, o conjunto de valores de exemplo acima definirá um conjunto de descrições para valores: 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">menos de 10 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">maior ou igual a 10 e menor que 20 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">maior ou igual a 20 e menor que 50 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">maior ou igual a 50 e menor que 100 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">maior ou igual a 100 e inferior a 10000 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">maior ou igual a 10000 </li> 
      </ul> </p> <p>Consulte <span class="uicontrol"> Testar usando maior que? </span> para alterar a forma como esses testes são executados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato "Menor que" </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Este é o modelo usado para especificar a descrição do intervalo para valores menores que o menor valor encontrado em <span class="uicontrol"> Valores do Intervalo </span>. O menor valor será representado usando o token numérico de espaço reservado <span class="uicontrol"> ~N~ </span>. Por exemplo: </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>or: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>Normalmente, o valor será formatado como está, ou seja, para uma definição <span class="uicontrol"> de Valores de Intervalo </span> de "5 10 20" e um valor fornecido de 1, a descrição do intervalo gerado seria simplesmente algo como "Menos de 5". Se, em vez disso, quiser que seja "4.99 e inferior", defina <span class="uicontrol"> Precision </span> para <span class="uicontrol"> 2 </span> e use este formato: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p>No <span class="uicontrol"> Formato "Menor que" </span>, as letras minúsculas <span class="uicontrol"> ~n~ </span> farão com que o valor seja arredondado <i>para baixo</i> de acordo com a configuração <span class="uicontrol"> Precision </span>. </p> <p>Observação: para incluir qualquer espaço reservado numérico na descrição do intervalo, como está, especifique com um prefixo de barra invertida (\) - por exemplo <span class="uicontrol"> \~N~ </span> ou <span class="uicontrol"> \~n~ </span>. Para incluir um caractere de barra invertida, especifique-o com outra barra invertida - por exemplo <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato intermediário </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Este é o modelo usado para especificar a descrição do intervalo para valores que estão em algum lugar entre os menores e maiores valores encontrados em <span class="uicontrol"> Valores do Intervalo </span>. Para o intervalo especificado, o valor do intervalo inferior será representado usando o token numérico de espaço reservado <span class="uicontrol"> ~L~ </span>, e o valor do intervalo superior será representado usando o token <span class="uicontrol"> ~H~ </span>. Por exemplo: </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>ou: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>ou: </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>Normalmente, os valores serão formatados como estão - ou seja, para uma definição <span class="uicontrol"> de Valores de Intervalo </span> de "5 10 20" e um valor fornecido de 8, a descrição do intervalo gerado seria simplesmente algo como "Entre 5 e 10". Se preferir que seja "Entre 5 e 9,99", com o valor mais alto ajustado <i>para baixo</i>, defina <span class="uicontrol"> Precisão </span> para <span class="uicontrol"> 2 </span> e use este formato: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>Da mesma forma, <span class="uicontrol"> ~L~ </span> pode ser substituído por <span class="uicontrol"> ~l~ </span> para ter o valor mais baixo ajustado <i>para cima</i>, também de acordo com a configuração <span class="uicontrol"> Precision </span>. Isso significa que uma definição como: </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>com um valor <span class="uicontrol"> Precision </span> de <span class="uicontrol"> 2 </span> criaria "Entre 5.01 e 10". </p> <p>O <span class="uicontrol"> ~l~ </span> minúsculo fará com que o valor mais baixo seja arredondado <i>para cima</i> de acordo com a configuração <span class="uicontrol"> Precisão </span>, e o <span class="uicontrol"> ~h~ </span> minúsculo fará com que o valor mais alto seja arredondado <i>para baixo</i>. </p> <p>Observação: para incluir qualquer espaço reservado numérico na descrição do intervalo, como está, especifique com um prefixo de barra invertida (\) - por exemplo <span class="uicontrol"> \~L~ </span> ou <span class="uicontrol"> \~h~ </span>. Para incluir um caractere de barra invertida, especifique-o com outra barra invertida - por exemplo <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato "Maior que" </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Este é o modelo usado para especificar a descrição do intervalo para valores maiores que o maior valor encontrado em <span class="uicontrol"> Valores do Intervalo </span>. O maior valor será representado usando o token numérico de espaço reservado <span class="uicontrol"> ~N~ </span>. Por exemplo: </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>ou: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>Normalmente, o valor será formatado como está, ou seja, para uma definição <span class="uicontrol"> de Valores de Intervalo </span> de "5 10 20" e um valor fornecido de 30, a descrição do intervalo gerado seria simplesmente algo como "Maior que 20". Se preferir que seja "20.01 e superior", defina <span class="uicontrol"> Precision </span> para <span class="uicontrol"> 2 </span> e use este formato: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p>Em <span class="uicontrol"> Formato "Maior que" </span>, as letras minúsculas <span class="uicontrol"> ~n~ </span> farão com que o valor seja arredondado <i>para cima</i> de acordo com a configuração <span class="uicontrol"> Precision </span>. </p> <p>Observação: para incluir qualquer espaço reservado numérico na descrição do intervalo, como está, especifique com um prefixo de barra invertida (\) - por exemplo <span class="uicontrol"> \~N~ </span> ou <span class="uicontrol"> \~n~ </span>. Para incluir um caractere de barra invertida, especifique-o com outra barra invertida - por exemplo <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Precisão </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Um valor inteiro que especifica o número de dígitos à direita de um ponto decimal. Este método também controla as operações de arredondamento. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tirar zeros à esquerda? </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado, um item <span class="uicontrol"> Campo de intervalo </span> será selecionado e um valor <span class="uicontrol"> Precision </span> diferente de zero foi definido. </p> <p>Devemos exibir "0,50" como ".50"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Retirar zeros à direita? </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado, um item <span class="uicontrol"> Campo de intervalo </span> será selecionado e um valor <span class="uicontrol"> Precision </span> diferente de zero foi definido. </p> <p>Devemos exibir "10.00" como "10"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar separadores de milhares? </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Devemos exibir "10.000" como "10.000"? Valores específicos da localidade serão usados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajustar valores zero? </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Quando valores zero arredondados são exibidos, eles devem ser arredondados para cima ou para baixo de acordo com a configuração <span class="uicontrol"> Precision </span>? ou seja, exibir "0,01"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Testar usando Maior que? </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Como cada valor é comparado aos valores em <span class="uicontrol"> Valores de Intervalo </span>, processados em <i><b>ordem decrescente</b></i>, ele é comparado, por padrão, usando o operador Maior que ou Igual (&gt;=) , parando assim que o teste for bem-sucedido. Isso significa que, com um conjunto de <span class="uicontrol"> Valores de Intervalo </span> como "10 20 50 100 1000", o valor 100 cairá no intervalo de 100 a 1000, pois 100 é realmente &gt;= 100. Se preferir que caia no intervalo de 50 a 100, marque essa opção, o que fará com que as comparações usem o operador Maior que (&gt;), em vez disso. </p> <p>Por exemplo, para cada valor desse campo, quando essa opção é marcada: 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">se o valor for menor ou igual a (&lt;=) o menor valor em <span class="uicontrol"> Valores do Intervalo </span>, o <span class="uicontrol"> Formato "Menor que" </span> será usado </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">se o valor for maior que (&gt;) o maior valor em <span class="uicontrol"> Valores do Intervalo </span>, será usado o <span class="uicontrol"> Formato "Maior que" </span> </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">caso contrário, um intervalo será encontrado onde o valor do campo fica entre dois <span class="uicontrol"> Valores do Intervalo </span> consecutivos (maior que ou igual a (&gt;=) o valor menor e menor que (&lt;) o valor maior), e o <span class="uicontrol"> Formato Intermédio </span> será usado </li> 
    </ul> </p> <p>e, quando desmarcado: 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">se o valor for menor que (&lt;) o menor valor em <span class="uicontrol"> Valores do Intervalo </span>, o <span class="uicontrol"> Formato "Menor que" </span> será usado </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">se o valor for maior ou igual a (&gt;=) o maior valor em <span class="uicontrol"> Valores do Intervalo </span>, será usado o <span class="uicontrol"> Formato "Maior que" </span> </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">caso contrário, um intervalo será encontrado onde o valor do campo cai entre dois <span class="uicontrol"> Valores do Intervalo </span> consecutivos (maior que (&gt;) o valor menor e menor que ou igual a (&lt;=) o valor maior), e o <span class="uicontrol"> Formato Intermédio </span> será usado </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Teste </p> </td> 
      <td colname="col2"> <p>Disponível somente se <span class="uicontrol"> Criar descrição de intervalo </span> estiver marcado e um item <span class="uicontrol"> Campo de intervalo </span> estiver selecionado. </p> <p>Forneça uma amostra de valor numérico e pressione o botão <span class="uicontrol"> Test </span> para ver como o Campo de intervalo é criado. A descrição do Intervalo gerado será exibida na janela. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Consulte também [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Clique em **[!UICONTROL Add]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Definitions] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edição de campos de meta tag predefinidos ou definidos pelo usuário {#task_0A7657B63596421BB6DB3ED44F827AB3}

Você pode editar apenas determinados campos em metatags predefinidas ou editar todos os campos em metatags definidas pelo usuário.

Antes que os efeitos das alterações de meta tag sejam visíveis para os clientes, você deve recriar o índice do site.

**Para editar campos de meta tag predefinidos ou definidos pelo usuário**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Na página [!DNL Definitions], na coluna [!DNL Actions] da tabela, clique em **[!UICONTROL Edit]** na linha do nome do campo da meta tag que deseja alterar.
1. Na página [!DNL Pinned Keyword Results Manager] , na tabela, clique em **[!UICONTROL Edit]** na linha da palavra-chave que deseja alterar.
1. Na página [!DNL Edit Field], defina as opções desejadas.

   Se você optou por fazer alterações em um campo de meta tag predefinido, esteja ciente de que nem todos os campos são editáveis.

   Consulte a tabela de opções em [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Definitions] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Exclusão de um campo de meta tag definido pelo usuário {#task_9361EF38B5E743038B6672FA6CF70FD3}

Você pode excluir um campo de meta tag definido pelo usuário que não é mais necessário ou usado.

Não é possível excluir campos de meta tag predefinidos. No entanto, é possível editar determinados campos.

Consulte [Edição de campos de metatag predefinidos ou definidos pelo usuário](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3).

Antes que os efeitos da meta tag de exclusão sejam visíveis para os clientes, você deve reconstruir o índice do site.

**Para excluir um campo de meta tag definido pelo usuário**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Na página [!DNL Definitions], na seção [!DNL User-defined fields] da tabela, clique em **[!UICONTROL Delete]** na linha do nome do campo da meta tag que deseja remover.
1. Na caixa de diálogo Confirmação, clique em **[!UICONTROL OK]**.
1. (Opcional) Reconstrua o índice do site preparado se desejar visualizar os resultados.

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) Na página [!DNL Definitions] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre Injeções {#concept_DA091920671948A0A893A26B3A2FAAE5}

Você pode usar [!DNL Injections] para inserir conteúdo em suas páginas da Web sem precisar editar as próprias páginas.

Você pode anexar conteúdo a campos indexados específicos, como &quot;target&quot; ou &quot;body&quot;, ou substituir o conteúdo indexado por novos valores. Por exemplo, se você inseriu novo conteúdo no campo da meta tag &quot;target&quot;, Essas informações serão tratadas da mesma forma que o conteúdo da página codificada. Você pode editar o conteúdo de qualquer campo de meta tag predefinido, independentemente de as páginas do site terem o conteúdo correspondente. Por exemplo, você pode editar o conteúdo dos seguintes nomes predefinidos de campo da meta tag :

* alt
* body
* charset
* date
* desc
* teclas
* language
* target
* title
* url

## Trabalhar com injeções de campo de teste {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

Opcionalmente, você pode usar **[!UICONTROL Test]** na página [!DNL Staged Injections]. Você insere um nome de campo de teste (por exemplo, &quot;título&quot; ou &quot;corpo&quot;), o valor do campo original (por exemplo, &quot;Página inicial&quot;) e um URL de teste do seu site. O valor resultante é exibido para sua referência. Os valores atuais não são alterados durante o teste.

## Trabalhando com Definições de Injeção de Campo {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

As definições de injeção têm a seguinte forma:

```
append|replace field [regexp] URL value
```

O `append|replace`, `field`, `URL`. os itens e `value` são obrigatórios. Introduza uma definição de injeção por linha. O exemplo a seguir contém seis definições diferentes de injeção.

```
replace title  https://www.yoursite.com/company/contactus.html Adobe: Contact Us 
append body https://www.yoursite.com/products/* On Sale Now! 
append target https://www.yoursite.com/news/bob_white/ Regular Weekly Feature 
append target regexp https://www.yoursite.com/travel/mr_travel/.*\column.html$ Regular Weekly Feature 
replace charset https://www.yoursite.com/japanese/intro.txt shift-jis 
replace language https://www.yoursite.com/japanese/intro.txt ja_JP
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Definição de injeção </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> append|replace  </span> </p> </td> 
   <td colname="col2"> <p>Escolha "append" (anexar) para adicionar o valor da definição de injeção ("Adobe: Entre em contato conosco" ou "Na venda agora!" nos exemplos acima) ao conteúdo dos campos existentes. Escolha "replace" para substituir o conteúdo do campo existente pelo valor definido. Se um campo não tiver conteúdo no momento, o valor definido será adicionado automaticamente, independentemente de qual opção (anexar ou substituir) for usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> campo  </span> </p> </td> 
   <td colname="col2"> <p>É necessário um nome de campo. A seguir estão dez nomes de campo predefinidos que podem ser usados: </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> Alt </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> data </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> teclas  </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> target  </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> título </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>Cada nome de campo corresponde aos elementos nas páginas do site. Por exemplo, se você especificar o nome do campo <span class="codeph"> desc </span>, poderá adicionar o valor da definição de injeção ao campo que corresponde à descrição Meta tags nas páginas do site. </p> <p>Se nenhuma meta tag de descrição existir em suas páginas, o conteúdo definido criará a tag para você. O conteúdo especificado em uma injeção <span class="codeph"> desc </span> é exibido na sua página de resultados da mesma forma que o conteúdo Metdescrição codificado seria. </p> <p>Também é possível criar várias definições com o mesmo nome de campo. Por exemplo, suponha que você tenha as seguintes injeções: </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>Todas as páginas do site no exemplo acima recebem um título inserido "Bem-vindo a Meu Site". As páginas na pasta "/company/" são inseridas com um novo título "Meu site: Fale conosco" que substitui o anterior. </p> <p>Observe que as injeções são aplicadas na ordem em que aparecem na caixa de texto <span class="wintitle"> Definições de Injeção de Campo </span>. Se o mesmo campo ("título" neste exemplo) for definido mais de uma vez para páginas no mesmo local, a definição posterior terá prioridade. </p> <p> <span class="codeph"> [regexp]  </span> - opcional. Se você optar por usar a opção <span class="codeph"> regexp </span>, o URL definido será tratado como uma expressão regular. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares </a>. </p> <p>Na seguinte definição: </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "Informações importantes" é inserido no campo "destino" em todas as páginas que correspondem à expressão regular <span class="codeph"> ^.*/products/.*\.html$ </span>. </p> <p>Portanto, você tem o seguinte: </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>No exemplo a seguir: </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>A injeção anexa "Millennium Science" ao conteúdo "title" de todas as páginas que terminam com uma extensão de nome de arquivo ".pdf". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>Um URL é necessário e especifica quais documentos são inseridos. </p> <p>O URL é qualquer um dos seguintes: </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> Um caminho completo, como em https://www.mydomain.com/products.html </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> Um caminho parcial, como em https://www.mydomain.com/products </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> Um URL que usa curingas, como em https://www.mydomain.com/*.html </li> 
     </ul> </p> <p>O valor do URL não deve ter caracteres de espaço. Se a opção <span class="codeph"> regexp </span> for usada, o URL será tratado como uma expressão regular. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Um valor é obrigatório e é usado para substituir ou adicionar ao conteúdo do campo existente. É possível especificar vários valores para o mesmo nome de campo. Por exemplo: </p> <p>anexar <b>chaves</b> https://www.mysite.com/travel/ <b>verão</b>, <b>praia</b>, <b>e</b> </p> <p>anexar <b>chaves</b> https://www.mysite.com/travel/fare/*.html <b>tíquetes baratos</b> </p> <p>No exemplo acima, as palavras "verão, praia, areia" são anexadas ao campo "chaves" em todas as páginas no diretório "/Travel/". As palavras "passagens baratas" também são anexadas ao campo "chaves" em todas as páginas do diretório "/Travel/fare/". </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte também [Selecionar tipos de conteúdo para rastrear e indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

## Adição de definições de injeção de campo {#task_E86566FA1FF74CF68115C0ADA05172AE}

Você pode usar [!DNL Injections] para inserir conteúdo em suas páginas da Web sem precisar editar as próprias páginas.

Opcionalmente, você pode usar **[!UICONTROL Test]** na página [!DNL Injections]. Você insere um nome de campo de teste (por exemplo, &quot;título&quot; ou &quot;corpo&quot;), o valor do campo original (por exemplo, &quot;Página inicial&quot;) e um URL de teste do seu site. O valor resultante é exibido para sua referência. Os valores atuais não são alterados durante o teste.

**Para adicionar definições de injeção de campo**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**.
1. (Opcional) Na página [!DNL Injections], na área [!DNL Test Field Injections], insira o campo de teste, o valor original do teste e o URL de teste e clique em **[!UICONTROL Test]**.
1. No campo [!DNL Field Injection Definitions], insira uma definição de injeção por linha.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Sobre o carregador de atributos {#concept_9EF38E98811B42CDA41996432B9AD209}

Use [!DNL Attribute Loader] para definir fontes de entrada adicionais para aumentar os dados rastreados de um site.

>[!NOTE]
>
>Para usar o Carregador de atributos, talvez seja necessário ativá-lo em sua conta pelo representante da conta do Adobe ou pelo Suporte ao Adobe.

Você pode usar uma fonte de entrada de feed de dados para acessar o conteúdo armazenado em um formulário diferente do que é normalmente descoberto em um site. Faça isso usando um dos métodos de rastreamento disponíveis. Os dados dessas fontes podem então ser inseridos em dados de conteúdo rastreado.

Após adicionar uma definição de Carregador de Atributo à página [!DNL Staged Attribute Loader Definitions], é possível alterar qualquer configuração, exceto os valores Nome e os valores Tipo

A página [!DNL Attribute Loader] mostra as seguintes informações:

* O nome da configuração definida do Carregador de atributos que você configurou e adicionou.
* Um dos seguintes tipos de fonte de dados para cada conector adicionado:

   * **Texto**  - Arquivos simples &quot;simples&quot;, delimitados por vírgulas, delimitados por tabulação ou outros formatos delimitados de forma consistente.
   * **Feed**  - Feeds XML.

* Se a configuração está ativada ou não para o próximo rastreamento e indexação.
* O endereço da fonte de dados.

Consulte também [Como o processo de injeção de atributo funciona para Texto e Feed...](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

Consulte também [Sobre a configuração de vários carregadores de atributo](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

Consulte também [Sobre o uso de Visualização quando você adiciona um Atributo...](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## Como o processo de injeção de atributo funciona nas configurações de Texto e Feed no Carregador de atributos {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Etapa  </p> </th> 
   <th colname="col2" class="entry"> <p>Processo </p> </th> 
   <th colname="col3" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Baixe a fonte de dados. </p> </td> 
   <td colname="col3"> <p>Para configurações de Texto e Feed, é um download de arquivo simples. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Analise a fonte de dados baixada em pseudo-documentos individuais. </p> </td> 
   <td colname="col3"> <p>Para <span class="uicontrol"> Texto </span>, cada linha de texto delimitada por linha corresponde a um documento individual e é analisada usando o delimitador especificado, como uma vírgula ou tabulação. </p> <p>Para <span class="uicontrol"> Feed </span>, os dados de cada documento são extraídos usando um padrão de expressão regular no seguinte formulário: </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Usando <span class="uicontrol"> Mapeie </span> na página <span class="wintitle"> Adição do Carregador de Atributos </span>, crie uma cópia em cache dos dados e crie uma lista de links para o rastreador. Os dados são armazenados em um cache local e são preenchidos com os campos configurados. </p> <p>Os dados analisados são gravados no cache local. </p> <p>Esse cache é lido posteriormente para criar os documentos HTML simples necessários ao crawler. Por exemplo, </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>O elemento <span class="codeph"> &lt;title&gt; </span> só é gerado quando existe um mapeamento para o campo de metadados Title . Da mesma forma, o elemento <span class="codeph"> &lt;body&gt; </span> só é gerado quando existe um mapeamento para o campo de metadados do Corpo. </p> <p> <b>Importante</b>: Não há suporte para a atribuição de valores à meta tag de URL predefinida. </p> <p>Para todos os outros mapeamentos, as tags <span class="codeph"> &lt;meta&gt; </span> são geradas para cada campo que tem dados encontrados no documento original. </p> <p>Os campos de cada documento são adicionados ao cache. Para cada documento gravado no cache, um link também é gerado como nos exemplos a seguir: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>O mapeamento da configuração deve ter um campo identificado como Chave primária. Esse mapeamento forma a chave usada quando os dados são obtidos do cache. </p> <p>O crawler reconhece o índice de URL <span class="codeph">: </span> prefixo do esquema, que pode então acessar os dados armazenados em cache localmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Rastreie o conjunto de documentos em cache. </p> </td> 
   <td colname="col3"> <p>O índice <span class="codeph">: </span> os links são adicionados à lista pendente do crawler e são processados na sequência de rastreamento normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Processar cada documento. </p> </td> 
   <td colname="col3"> <p>O valor da chave de cada link corresponde a uma entrada no cache, portanto, o rastreamento de cada link resulta na busca dos dados desse documento do cache. Ele é então "montado" em uma imagem HTML que é processada e adicionada ao índice. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sobre a configuração de vários carregadores de atributo {#section_4CC49C74EF294608A184E233F215ADFF}

É possível definir várias configurações do Carregador de atributos para qualquer conta.

Ao adicionar um Carregador de Atributo, você pode usar opcionalmente o recurso **[!UICONTROL Setup Maps]** para baixar uma amostra da fonte de dados. Os dados são examinados quanto à sua adequação.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Tipo de carregador de atributos </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texto </p> </td> 
   <td colname="col2"> <p>Determina o valor do delimitador experimentando as guias primeiro e depois as barras verticais ( <span class="codeph"> | </span>) e finalmente vírgulas ( <span class="codeph"> , </span>). Se você já especificou um valor de delimitador antes de clicar em <span class="uicontrol"> Configurar Mapas </span>, esse valor é usado. </p> <p>O esquema de melhor ajuste resulta no preenchimento dos campos de Mapa com suposições nos valores de Tag e Campo apropriados. Além disso, uma amostragem dos dados analisados é exibida. Certifique-se de selecionar <span class="uicontrol"> Cabeçalhos na Primeira Linha </span> se você sabe que o arquivo inclui uma linha de cabeçalho. A função de configuração usa essas informações para identificar melhor as entradas de mapa resultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Feed </p> </td> 
   <td colname="col2"> <p>Baixe a fonte de dados e executa uma análise XML simples. </p> <p>Os identificadores XPath resultantes são exibidos nas linhas de tag da tabela Map e valores semelhantes em Campos. Essas linhas identificam apenas os dados disponíveis e não geram as definições XPath mais complicadas. No entanto, ainda é útil, pois descreve os dados XML e identifica a Itemtag. </p> <p> <p>Observação:  A função Configurar Mapas baixa toda a origem XML para executar sua análise. Se o arquivo for grande, essa operação pode esgotar o tempo limite. </p> </p> <p>Quando bem-sucedida, essa função identifica todos os itens XPath possíveis, muitos dos quais não são desejáveis para uso. Certifique-se de examinar as definições de Mapa resultantes e remover as que não são necessárias ou não. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O recurso de Mapas de configuração pode não funcionar para grandes conjuntos de dados XML porque o analisador de arquivos tenta ler o arquivo inteiro na memória. Como resultado, você pode experimentar uma condição de falta de memória. No entanto, quando o mesmo documento é processado no momento da indexação, ele não é lido na memória. Em vez disso, documentos grandes são processados &quot;em movimento&quot; e não são lidos inteiramente na memória primeiro.

## Sobre o uso de Visualização ao adicionar um Carregador de atributos {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

Os dados do Carregador de atributos são carregados antes de uma operação Índice.

No momento em que você adiciona um Carregador de Atributo, é possível usar opcionalmente o recurso **[!UICONTROL Preview]** para validar os dados, como se estivesse salvando. Ele executa um teste em relação à configuração, mas sem salvar a configuração na conta. O teste acessa a fonte de dados configurada. No entanto, ele grava o cache de download em um local temporário; ele não entra em conflito com a pasta de cache principal que o crawler de indexação usa.

A Visualização só processa um padrão de cinco documentos, conforme controlado por **Acct:IndexConnector-Preview-Max-Documents**. Os documentos visualizados são exibidos no formulário de origem, conforme são apresentados ao crawler de indexação. A exibição é semelhante a um recurso &quot;Exibir fonte&quot; em um navegador da Web. Você pode navegar pelos documentos no conjunto de visualização usando links de navegação padrão.

A visualização não oferece suporte a configurações XML porque esses documentos são processados diretamente e não baixados no cache.

## Adicionar uma definição do Carregador de atributos {#task_A735E5EF763343A9B675E1A3B09AFDBC}

Cada configuração do Carregador de atributos define uma fonte de dados e os mapeamentos para relacionar os itens de dados definidos para essa fonte aos campos de metadados no índice.

>[!NOTE]
>
>Para usar o Carregador de atributos, talvez seja necessário ativá-lo em sua conta pelo representante da conta do Adobe ou pelo Suporte ao Adobe.

Antes que os efeitos da definição nova e ativada sejam visíveis para os clientes, recrie o índice do site.

**Para adicionar uma definição de Carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Stage Attribute Loader Definitions], clique em **[!UICONTROL Add New Attribute Loader]**.
1. Na página [!DNL Attribute Loader Add], defina as opções de configuração desejadas. As opções disponíveis dependem do **[!UICONTROL Type]** que você selecionou.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nome </p> </td> 
      <td colname="col2"> <p>O nome exclusivo da configuração do Carregador de atributos. Você pode usar caracteres alfanuméricos. Os caracteres "_" e "-" também são permitidos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo </p> </td> 
      <td colname="col2"> <p>A fonte de seus dados. O tipo de fonte de dados selecionado afeta as opções resultantes disponíveis na página <span class="wintitle"> Adicionar </span> Carregador de Atributo. Você pode escolher entre: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texto </span> <p>Arquivos de texto simples, delimitados por vírgulas, delimitados por tabulação ou outros formatos consistentemente delimitados. Cada linha de texto delimitada por linha corresponde a um documento individual e é analisada usando o delimitador especificado. </p> <p>Você pode mapear cada valor, ou coluna, para um campo de metadados, referenciado pelo número da coluna, começando em 1 (um). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Feed </span> <p>Faz o download de um documento XML principal que contém várias "linhas" de informações. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fonte de dados: Texto</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativado </p> </td> 
      <td colname="col2"> <p>Ativa a configuração "ativada" para uso. Ou você pode desativar a configuração para impedir que if seja usado. </p> <p> <b>Observação</b>: As configurações do Carregador de atributos desativado são ignoradas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Endereço do host </p> </td> 
      <td colname="col2"> <p>Especifica o endereço do host do servidor onde seus dados estão localizados. </p> <p>Se desejar, você pode especificar um caminho URI completo (Identificador de recurso uniforme) para o documento da fonte de dados, como nos exemplos a seguir: </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>ou </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>O URI é dividido nas entradas apropriadas para os campos Endereço do Host, Caminho do Arquivo, Protocolo e, opcionalmente, Nome de Usuário e Senha </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o arquivo de texto simples, delimitado por vírgulas, delimitado por tabulação ou outro arquivo de formato delimitado de forma consistente. </p> <p>O caminho é relativo à raiz do endereço de host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica o protocolo usado para acessar o arquivo. Você pode escolher entre: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Se necessário, você pode inserir credenciais de autenticação apropriadas para acessar o servidor HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Se necessário, você pode inserir credenciais de autenticação apropriadas para acessar o servidor HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Você deve inserir credenciais de autenticação apropriadas para acessar o servidor FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Você deve inserir credenciais de autenticação apropriadas para acessar o servidor SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Arquivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tempo limite </p> </td> 
      <td colname="col2"> <p>Especifica o tempo limite, em segundos, para conexões FTP, SFTP, HTTP ou HTTPS. Esse valor deve estar entre 30 e 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tentativas </p> </td> 
      <td colname="col2"> <p>Especifica o número máximo de tentativas para conexões FTP, SFTP, HTTP ou HTTPS com falha. Esse valor deve estar entre 0 e 10. </p> <p>Um valor zero (0) impedirá tentativas de repetição. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codificação </p> </td> 
      <td colname="col2"> <p>Especifica o sistema de codificação de caracteres usado no arquivo de fonte de dados especificado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Delimitador </p> </td> 
      <td colname="col2"> <p>Especifica o caractere que você deseja usar para delinear cada campo no arquivo de fonte de dados especificado. </p> <p>O caractere de vírgula ( <span class="codeph"> , </span>) é um exemplo de delimitador. A vírgula atua como um delimitador de campo que ajuda a separar campos de dados no arquivo de fonte de dados especificado. </p> <p>Selecione <span class="uicontrol"> Guia? </span> para usar o caractere de tabulação horizontal como delimitador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Cabeçalhos na Primeira Linha </p> </td> 
      <td colname="col2"> <p>Indica que a primeira linha do arquivo de fonte de dados contém apenas informações de cabeçalho, não dados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dias obsoletos </p> </td> 
      <td colname="col2"> <p>Define o intervalo mínimo entre downloads de dados do Carregador de atributos. Os downloads acionados por índice que ocorrem dentro do intervalo de frequência de atualização do download são ignorados. Quando você define esse valor como o padrão de 1, os dados do Carregador de atributos não são baixados mais de uma vez em um período de 24 horas. Todos os índices de Pesquisa que ocorrem no intervalo de frequência de atualização de download usam o último conjunto de dados que foi baixado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Especifica mapeamentos de coluna para metadados, usando números de coluna. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Coluna </span> <p> Especifica um número de coluna, com a primeira coluna sendo 1 (uma). Para adicionar novas linhas de mapa para cada coluna, em <span class="wintitle"> Ação </span>, clique em <span class="uicontrol"> + </span>. </p> <p>Não é necessário fazer referência a cada coluna na fonte de dados. Em vez disso, você pode optar por ignorar os valores. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Campo </span> <p>Define o valor do atributo de nome usado para cada tag &lt;meta&gt; gerada. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metadados? </span> <p>Faz com que <span class="uicontrol"> Campo </span> se torne uma lista suspensa na qual você pode selecionar campos de metadados definidos para a conta atual. </p> <p>O valor <span class="uicontrol"> Campo </span> pode ser um campo de metadados indefinido, se desejado. Um campo de metadados indefinido às vezes é útil para criar conteúdo usado por um <span class="wintitle"> Script de filtragem </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Sobre o script de filtragem </a>. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Chave primária?  </span> <p>Somente um campo é identificado como a chave primária. Este campo será usado como a "chave estrangeira" para corresponder os dados do Carregador de atributos ao documento correspondente no índice. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> Strip HTML?  </span> <p>Quando essa opção é marcada, todas as tags HTML encontradas nos dados deste campo são removidas. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Ação </span> <p>Permite adicionar linhas ao mapa ou remover linhas do mapa. A ordem das linhas não é importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fonte de dados: Feed</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ativado </p> </td> 
      <td colname="col2"> <p>Ativa a configuração "ativada" para uso. Ou você pode desativar a configuração para impedir que if seja usado. </p> <p> <b>Observação</b>: As configurações do Carregador de atributos desativado são ignoradas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Endereço do host </p> </td> 
      <td colname="col2"> <p>Especifica o endereço do host do servidor onde seus dados estão localizados. </p> <p>Se desejar, você pode especificar um caminho URI completo (Identificador de recurso uniforme) para o documento da fonte de dados, como nos exemplos a seguir: </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>ou </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>O URI é dividido nas entradas apropriadas para os campos Endereço do Host, Caminho do Arquivo, Protocolo e, opcionalmente, Nome de Usuário e Senha. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caminho do arquivo </p> </td> 
      <td colname="col2"> <p>Especifica o caminho para o documento XML principal que contém várias "linhas" de informações. </p> <p>O caminho é relativo à raiz do endereço de host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica o protocolo usado para acessar o arquivo. Você pode escolher entre: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Se necessário, você pode inserir credenciais de autenticação apropriadas para acessar o servidor HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Se necessário, você pode inserir credenciais de autenticação apropriadas para acessar o servidor HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Você deve inserir credenciais de autenticação apropriadas para acessar o servidor FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Você deve inserir credenciais de autenticação apropriadas para acessar o servidor SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Arquivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifica o elemento XML que pode ser usado para identificar linhas XML individuais no arquivo de fonte de dados especificado. </p> <p>Por exemplo, no fragmento de Feed a seguir de um documento Adobe XML, o valor de Itemtag é <span class="codeph"> record </span>: </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; 
        &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome do campo de referência cruzada </p> </td> 
      <td colname="col2"> <p>Especifica um campo de metadados cujos valores são usados como "chaves" de pesquisa nos dados da configuração do Carregador de atributos. Se nenhum valor for selecionado (<b>—None—</b>), os dados dessa configuração não estarão disponíveis para uso em Cálculos de classificação (<b>Regras</b> &gt; <b>Regras de classificação</b> &gt; <b>Editar regras</b>). Quando você seleciona um valor, os valores desse campo são usados para fazer referência cruzada aos documentos de pesquisa/comercialização do site com os dados dessa configuração. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dias obsoletos </p> </td> 
      <td colname="col2"> <p>Define o intervalo mínimo entre downloads de dados do Carregador de atributos. Os downloads acionados por índice que ocorrem dentro do intervalo de frequência de atualização do download são ignorados. Quando você define esse valor como o padrão de 1, os dados do Carregador de atributos não são baixados mais de uma vez em um período de 24 horas. Todos os índices de Pesquisa que ocorrem no intervalo de frequência de atualização de download usam o último conjunto de dados que foi baixado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite que você especifique mapeamentos de elemento para metadados XML, usando expressões XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Adicionar tag </span> <p>Especifica uma representação XPath dos dados XML analisados. Usando o documento Adobe XML de exemplo acima, na opção Item , ele pode ser mapeado usando a seguinte sintaxe: </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>A sintaxe acima é traduzida da seguinte maneira: </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>O atributo <span class="codeph"> display </span> do elemento <span class="codeph"> record </span> mapeia para o campo de metadados <span class="codeph"> page-url </span>. </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido num elemento <span class="codeph"> de registro </span>, cujo atributo de nome é <span class="codeph"> título </span>, mapeia para o campo de metadados <span class="codeph"> título &lt;a11/ &gt;.</span> </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido num elemento <span class="codeph"> de metadados </span>, contido no elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> descrição </span>, mapeia para o campo de metadados <span class="codeph"> desc </span>. </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>O atributo <span class="codeph"> content </span> de qualquer elemento <span class="codeph"> meta </span> contido em um elemento <span class="codeph"> de metadados </span>, contido no elemento <span class="codeph"> record </span>, cujo atributo name é <span class="codeph"> descrição </span>, mapeia para o campo de metadados <span class="codeph"> body &lt;a11/ &gt;.</span> </p> </li> 
        </ul> </p> <p>XPath é uma notação relativamente complicada. Mais informações estão disponíveis no seguinte local: </p> <p>Consulte <a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xml/xpath_intro.asp </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Campo </span> <p>Define o valor do atributo de nome usado para cada tag <span class="codeph"> &lt;meta&gt; </span> gerada. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metadados? </span> <p>Faz com que <span class="uicontrol"> Campo </span> se torne uma lista suspensa na qual você pode selecionar campos de metadados definidos para a conta atual. </p> <p>O valor <span class="uicontrol"> Campo </span> pode ser um campo de metadados indefinido, se desejado. Um campo de metadados indefinido às vezes é útil para criar conteúdo usado por <span class="wintitle"> Filtering Script </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Sobre o script de filtragem </a>. </p> <p>Quando o Carregador de atributos processa documentos XML com várias ocorrências em qualquer campo de mapa, os vários valores são concatenados em um único valor no documento em cache resultante. Por padrão, esses valores são combinados com um delimitador de vírgula. No entanto, suponha que o valor <span class="wintitle"> Campo </span> correspondente seja um campo de metadados definido. Além disso, esse campo tem o conjunto de atributos <span class="wintitle"> Lista de permissões </span>. Nesse caso, o valor Delimitadores de lista do campo, que é o primeiro delimitador definido, é usado na concatenação. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Chave primária?  </span> <p>Somente um campo é identificado como a chave primária. Este campo será usado como a "chave estrangeira" para corresponder os dados do Carregador de atributos ao documento correspondente no índice. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> Strip HTML?  </span> <p>Quando essa opção é marcada, todas as tags HTML encontradas nos dados deste campo são removidas. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Ação </span> <p>Permite adicionar linhas ao mapa ou remover linhas do mapa. A ordem das linhas não é importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Clique em **[!UICONTROL Setup Maps]** para baixar uma amostra da fonte de dados. Os dados são examinados quanto à sua adequação.
1. Clique em **[!UICONTROL Add]** para adicionar a configuração à página [!DNL Attribute Loader Definitions].
1. Na página [!DNL Attribute Loader Definitions], clique em **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) Na página [!DNL Attribute Loader Definitions] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma definição do Carregador de atributos {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

Você pode editar um Carregador de atributos existente que tenha definido.

>[!NOTE]
>
>Para usar o Carregador de atributos, talvez seja necessário ativá-lo em sua conta pelo representante da conta do Adobe ou pelo Suporte ao Adobe.

Nem todas as opções do Carregador de atributos estão disponíveis para alteração, como Nome do carregador de atributos ou Tipo na lista suspensa [!DNL Type].

**Para editar uma definição do Carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Edit]** para obter um nome de definição de Carregador de Atributo cujas configurações você deseja alterar.
1. Na página [!DNL Attribute Loader Edit], defina as opções desejadas.

   Consulte a tabela de opções em [Adicionar uma definição de Carregador de Atributo](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC).
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Na página [!DNL Attribute Loader Definitions], clique em **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) Na página [!DNL Attribute Loader Definitions] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copiando uma definição do Carregador de atributos {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

Você pode copiar uma definição de Carregador de Atributo existente para usar como a base para um novo Carregador de Atributo que deseja criar.

>[!NOTE]
>
>Para usar o Carregador de atributos, talvez seja necessário ativá-lo em sua conta pelo representante da conta do Adobe ou pelo Suporte ao Adobe.

Ao copiar uma definição de Carregador de atributo, a definição copiada é desativada por padrão. Para ativar ou &quot;ativar&quot; a definição, você deve editá-la na página [!DNL Attribute Loader Edit] e selecionar **[!UICONTROL Enable]**.

Consulte [Editar uma definição de Carregador de Atributo](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80).

**Para copiar uma definição do Carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader] , no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Copy]** para obter um nome de definição do Carregador de Atributo cujas configurações você deseja duplicar.
1. Na página [!DNL Attribute Loader Copy], insira o novo nome da definição.
1. Clique em **[!UICONTROL Copy]**.
1. (Opcional) Na página [!DNL Attribute Loader Definitions] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Renomear uma definição do Carregador de atributos {#task_58D5DFD7EBC04111BCB91118E4440DB4}

Você pode alterar o nome de uma definição existente do Carregador de atributos.

>[!NOTE]
>
>Para usar o Carregador de atributos, talvez seja necessário ativá-lo em sua conta pelo representante da conta do Adobe ou pelo Suporte ao Adobe.

**Para renomear uma definição de Carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Rename]** para obter o nome da definição do Carregador de Atributo que você deseja alterar.
1. Na página [!DNL Attribute Loader Rename], insira o novo nome da definição no campo [!DNL Name].
1. Clique em **[!UICONTROL Rename]**.
1. (Opcional) Na página [!DNL Attribute Loader Definitions] , siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Carregamento de dados do carregador de atributos {#task_2F3C55189B0A4049AB2113F2291CC181}

Você pode baixar os dados configurados do Carregador de atributos em pesquisa/merchandising do site.

A página [!DNL Data Load] mostra as seguintes informações sobre o status da última operação Carregamento de dados do carregador de atributos:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Campo de status </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> <p>Indica o sucesso ou a falha da última tentativa de carregamento de dados. Ou exibe o status de uma operação de carregamento de dados já em andamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora inicial </p> </td> 
   <td colname="col2"> <p>Exibe a data e a hora em que a última operação de carregamento de dados foi iniciada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora de Parada </p> </td> 
   <td colname="col2"> <p>Exibe a data e a hora de conclusão da última operação de carregamento de dados. Ou indica que a operação de carregamento de dados atual ainda está em andamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Para carregar dados do carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader Definitions], clique em **[!UICONTROL Load Attribute Loader Data]**.
1. Na página **[!UICONTROL Attribute Loader Data Load]**, execute um dos seguintes procedimentos:

   * Clique em **[!UICONTROL Start Load]** para iniciar a operação de carregamento.

      Durante uma operação de carregamento de dados, a linha **Progress** fornece informações sobre seu progresso.

   * Clique em **[!UICONTROL Stop Load]** para interromper a operação de carregamento.

1. Clique em **[!UICONTROL Close]** para retornar à página [!DNL Attribute Loader Definitions].

## Visualização de dados do carregador de atributos {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Você pode usar Visualização para exibir os dados carregados mais recentemente do Carregador de atributos.

A coluna Linha na tabela mostra o número para cada linha de dados, indicando a ordem original de carregamento dos valores do Carregador de Atributo.

As colunas restantes mostram os valores associados a cada entrada.

Se a tabela estiver vazia, significa que você ainda não carregou dados do Carregador de atributos. Você pode fechar a página [!DNL Attribute Loader Data Preview] e carregar os dados do Carregador de atributos.

Consulte [Carregando dados do carregador de atributos](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Para visualizar os dados do carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader Definitions], na coluna [!DNL Actions], clique em **[!UICONTROL Preview]** para a configuração cujos dados baixados você deseja visualizar.
1. Na página [!DNL Attribute Loader Data Preview] , use as opções de navegação e visualização na parte superior e inferior da página para visualizar os dados.

   Clique em qualquer título de coluna na tabela para classificar os dados em ordem crescente ou decrescente.
1. Siga um destes procedimentos:

   * Clique em **[!UICONTROL Download to Desktop]** para baixar e salvar a tabela como um arquivo .xlt.
   * Feche a página quando terminar de visualizar os dados do Carregador de atributos e retornar à página visualizada anteriormente.

## Exibindo as configurações de uma definição do Carregador de atributos {#task_EA99A9694FE948ADA82C1DBA0667851B}

Você pode revisar as configurações de uma definição existente do Carregador de atributos.

Depois que uma definição de Carregador de atributo é adicionada à página [!DNL Attribute Loader Definitions], não é possível alterar a configuração Tipo. Em vez disso, você deve excluir a definição e, em seguida, adicionar uma nova.

>[!NOTE]
>
>Para usar o Carregador de atributos, talvez seja necessário ativá-lo em sua conta pelo representante da conta do Adobe ou pelo Suporte ao Adobe.

**Para exibir as configurações de uma definição do Carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Edit]** para obter um nome de definição do Carregador de Atributo cujas configurações você deseja revisar ou editar.

## Como visualizar o log a partir do carregamento de dados mais recente do Carregador de atributos {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Você pode usar [!DNL View Log] para examinar o arquivo de log de dados do Carregador de Atributo do processo de download mais recente. Você também pode usar a visualização de log para monitorar um download em execução.

Consulte [Carregando dados do carregador de atributos](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Para exibir o log do carregamento de dados mais recente do Carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader Definitions], clique em **[!UICONTROL View Log]**. Página de registro,
1. Na página [!DNL Attribute Loader Data Log] , use as opções de navegação e visualização na parte superior e inferior da página para exibir as informações de log.
1. Quando terminar, feche a página para retornar à página [!DNL Attribute Loader Definitions].

## Excluindo uma definição do Carregador de atributos {#task_E8980F66888B476E98C228C1D307EDF8}

É possível excluir uma definição existente do Carregador de atributos que não é mais necessária ou usada.

>[!NOTE]
>
>Para usar o Carregador de atributos, talvez seja necessário ativá-lo em sua conta pelo representante da conta do Adobe ou pelo Suporte ao Adobe.

**Para excluir uma definição do Carregador de atributos**

1. No menu do produto, clique em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Na página [!DNL Attribute Loader Definitions], no cabeçalho da coluna [!DNL Actions], clique em **[!UICONTROL Delete]** para obter o nome da definição do Carregador de Atributo que deseja remover.
1. Na página [!DNL Attribute Loader Delete], clique em **[!UICONTROL Delete]**.
