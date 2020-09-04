---
description: Você pode usar Regras de classificação para controlar o posicionamento relativo ou a classificação dos resultados de pesquisa de um cliente com base no conteúdo da meta tag contida e nas métricas relacionadas do Adobe Analytics.
seo-description: Você pode usar Regras de classificação para controlar o posicionamento relativo ou a classificação dos resultados de pesquisa de um cliente com base no conteúdo da meta tag contida e nas métricas relacionadas do Adobe Analytics.
seo-title: Sobre regras de classificação
solution: Target
subtopic: Ranking Rules
title: Sobre regras de classificação
topic: Rules,Site search and merchandising
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '4647'
ht-degree: 0%

---


# Sobre regras de classificação{#about-ranking-rules}

Você pode usar Regras de classificação para controlar o posicionamento relativo ou a classificação dos resultados de pesquisa de um cliente com base no conteúdo da meta tag contida e nas métricas relacionadas do Adobe Analytics.

## Usando regras de classificação {#concept_F555C076759B4E81B925441CFE707397}

Você define regras de classificação para afetar a colocação relativa dos documentos nos resultados da pesquisa, com base no conteúdo de cada documento. Você pode basear as regras de classificação no conteúdo da meta tag, nas métricas do Adobe Analytics (se sua conta estiver configurada para funcionar com o Adobe Analytics) ou nas métricas do Adobe Analytics HBX (se sua conta estiver configurada para funcionar com o Adobe Analytics HBX).

É possível definir páginas da Web que contêm meta tags com as características desejadas, como um determinado nome de marca ou preço, ou páginas da Web que tenham indicadores-chave de desempenho da Adobe Analytics desejados, como visualizadores únicos, para receber uma classificação maior que as páginas da Web que não possuem. As características &quot;desejáveis&quot; são facilmente atualizadas adicionando ou editando Regras de classificação e, em seguida, reindexando seu site.

Se você tiver mais de uma meta tag do tipo &quot;classificação&quot; definida, poderá criar coleções separadas de regras para usar no cálculo dos vários campos de classificação. Você pode adicionar um grupo de regras de classificação, que pode ser atribuído a um dos campos de Classificação definidos. Os grupos de regras normalmente contêm uma ou mais definições de regras, mas também podem se referir a outros grupos de Regras, para que você possa criar um ou mais grupos de regras comumente usadas que sejam compartilhados durante o cálculo de suas várias classificações.

Consulte [Adicionar um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de regras de classificação.

Um valor de classificação positivo promove os resultados da pesquisa para o topo; um valor de classificação negativo representa os resultados da pesquisa na parte inferior dos resultados da pesquisa. O intervalo normal para valores de classificação é 1,0, que é a promoção máxima nos resultados da pesquisa, enquanto -1,0 é a despromoção máxima. Embora você possa personalizar esse intervalo editando o campo Classificação nas definições de metadados, esse tipo de personalização geralmente é desnecessário.

Consulte [Sobre Definições](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620).

Se você tiver definido mais de um campo de classificação em Configurações > Metadados > Definições, terá a opção de criar conjuntos adicionais de regras de classificação, um para cada campo de classificação. Você pode definir conjuntos adicionais de regras de classificação sem estar diretamente associado a um campo de classificação. Essa flexibilidade permite criar conjuntos de Regras comuns que podem ser compartilhados no cálculo de um ou mais valores de classificação.

**Importante**: Antes de usar as Regras de classificação, há várias etapas de configuração de conta que devem ser concluídas.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## Configuração da classificação {#task_4CEBC13925B047FC95BDC217B48089C5}

Antes de usar as regras de classificação, há várias etapas de configuração de conta que devem ser concluídas.

**Para configurar a classificação**

1. Escolha dentre as seguintes opções:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Tarefa </p> </th> 
      <th colname="col2" class="entry"> <p>Configuração </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Para criar regras de classificação baseadas em tags meta </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> No menu do produto, clique em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>. </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> Na página Definições, clique em <span class="uicontrol"> Adicionar novo campo </span>. </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> Na página Adicionar campo, no campo de <span class="uicontrol"> texto Nome do </span> campo, digite <code>
        rank 
      </code>; no campo de texto Nome da <span class="uicontrol"> tag </span> , digite <code>
        rank 
      </code>; na lista suspensa Tipo <span class="uicontrol"> de dados </span> , selecione <span class="uicontrol"> Classificação </span>. Deixe todas as outras opções de campo como estão. <p>Consulte o parâmetro de query <span class="codeph"> sp_sr </span> nos parâmetros CGI de pesquisa <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> de backend </a>. </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">Clique em <span class="uicontrol">Adicionar </span>. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Para criar regras de classificação baseadas em métricas do Adobe Analytics </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> Certifique-se de configurar a autenticação do Adobe Analytics a partir da pesquisa/comercialização do site. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> Configurando a autenticação de métricas do Adobe Analytics </a>. </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> Selecione e adicione um conjunto de relatórios disponível. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> Adicionando um conjunto de relatórios da Adobe Analytics </a>. </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> Configure a lista de métricas do Adobe Analytics que você deseja que estejam disponíveis para a criação de novas Regras de classificação. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Editando as métricas do Adobe Analytics de um Conjunto de relatórios </a>. </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Carregue as métricas iniciais do Adobe Analytics para suas páginas do site. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> Carregamento de dados do Adobe Analytics </a>. </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Adicione uma ou mais regras de classificação.

   Consulte [Adicionar uma regra](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classificação.

1. Clique em **[!UICONTROL regenerate your staged site index]** para executar um reíndice completo de seu site (de **[!UICONTROL Index]** > **[!UICONTROL Full Index]**).

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Configurar um índice incremental de um site](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)de preparo.
1. Verifique os valores na coluna Classificação em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** para verificar se as Regras de classificação foram aplicadas corretamente.

## Sobre a classificação de documentos por idade {#topic_770815CF1B2A491F83FF765871B6F1B8}

Você pode classificar um documento HTML por sua idade com uma função de decaimento exponencial. A taxa de decaimento é especificada com uma constante de semivida escolhida, a quantidade de tempo que deve passar antes que o valor caia para metade do seu valor inicial.

A classificação por idade baseia-se nas duas equações a seguir:

`K = -ln(2) / H`

`RANK = e^(K * T)`

Variáveis `H` e `T` são entradas para esta função: `H` é o período de semivida desejado e `T` é a idade do documento, expressa em segundos. `K` é a semivida calculada e `RANK` é a diminuição exponencial do valor etário especificado. O valor resultante é de 0 a 1. Um documento mais recente tem um valor de classificação mais próximo de 1 em comparação a um documento mais antigo. Em teoria, os documentos nunca devem alcançar o valor de 0, mas os erros de arredondamento podem fazer com que o resultado se torne 0.

## Requisitos para a utilização da classificação etária {#section_D716507D589442C6B7848892BD28F966}

* Sua conta já deve estar configurada corretamente para classificação. Se não estiver configurado, consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).
* O documento HTML deve ter um campo de tag meta HTML que represente sua data de nascimento, sua criação como um carimbo de data e hora ou algum outro valor de data significativo.
* A função incorporada especial, `search_get_age_rank()`, conforme especificada nas páginas Adicionar ou Editar regra de classificação, é usada para calcular a classificação etária de um documento. As seções seguintes descrevem pormenorizadamente a utilização geral da função de classificação por idade. Também é apresentado um exemplo que demonstra o recurso de classificação etária.

## Usando search_get_age_rank () na página Adicionar regra de classificação ou na página Editar regra de classificação {#section_34BC5276F2AB4419AD92872A397CA0AF}

Especifique `search_get_age_rank()` o seguinte:

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* Data de nascimento - A data de nascimento ou de início do arquivo deve ser uma string formatada por data, de acordo com os formatos de data do campo. Essa string formatada por data deve ser uma referência de campo, como em `{field_name}`.
* Half_Life - A meia-vida é a quantidade de tempo que deve ser passada antes que o valor caia para metade de seu valor inicial. Esse valor é expresso no número de dias e é um número inteiro ou um número de ponto flutuante.
* Default_Rank - A classificação padrão é usada como uma rede de segurança caso a data de nascimento seja inválida ou a data esteja no futuro. Não é possível usar esse valor padrão se o campo de metadados associado tiver um valor padrão válido também. O valor aqui é um número de ponto flutuante ou um número inteiro. Consulte abaixo para obter sugestões se encontrar problemas com o valor padrão que está sendo usado.

Consulte [Adicionar uma regra](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classificação.

See [Editing a ranking rule](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).

**Exemplo**

No exemplo a seguir,

`search_get_age_rank({birthdate}#28#0.20)`

a data contida no campo documento `birthdate` é transmitida como carimbo de data/hora. A meia-vida é de 28 dias. O valor de classificação padrão é 0,20 se a data for inválida.

Consulte a tabela de opções em [Adicionar uma regra](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classificação.

Na seção Valores/fileiras da página Adicionar regra de classificação ou Editar regra de classificação, você só pode usar `search_get_age_rank` com regras personalizadas. Portanto, escolha **Personalizado** na lista suspensa Valores/fileiras. Quando a regra usa a função de classificação por idade, nenhum espaço é permitido na parte de valores da regra. Verifique se não há espaços nos argumentos da função ou entre eles. E não há espaços entre operadores matemáticos ou condicionais.

A seguir está um exemplo de uma regra de valores/fileiras — uma regra associada a um campo de texto:

`regexp .* search_get_age_rank({other_field}#365#0.20)`

Este exemplo supõe que `other_field` contenha um valor de data. Se esse campo não for um campo do tipo data, esse valor será interpretado usando os formatos de data associados ao campo Data predefinido. Caso contrário, os formatos de data desse campo serão usados. Essa entrada de valores/fileiras é usada sempre que o campo documento, que a Fonte de Dados da Regra identifica, não está vazio e o valor de retorno da função (de 0 a 1) é a classificação atribuída.

Para uma regra associada a um campo numérico, especificamente um campo de Data:

`9999999999 search_get_age_rank({other_field}#365#0.20)`

Conforme cada documento é processado, o valor em `other_field` é convertido no formulário Unix &quot;epoch&quot;, usando as definições de formato de data do campo. Esse valor é usado na `search_get_age_rank()` chamada. Como cada valor de &quot;época&quot; é menor que 9999999999 (no momento, pelo menos), a Regra simplesmente fornece o valor de retorno da função (de 0 a 1) como a classificação.

Em ambos os exemplos anteriores, é típico que a Fonte de Dados da Regra seja o mesmo campo usado na `search_get_age_rank()` função - `other_field` nesse caso.

## Exemplo de integração da classificação etária em regras de classificação {#section_A86D909687CC45E19D4EA7A4A9283F28}

A seguir está um exemplo de como integrar a classificação por idade às regras de classificação. O exemplo também mostra os resultados brutos da função de classificação etária e os resultados das regras de classificação. O exemplo considera o seguinte:

* As páginas da Web que são rastreadas têm uma meta tag HTML chamada &quot;data de nascimento&quot;. O conteúdo dessa tag é um carimbo de data e hora relacionado ao documento.
* As definições de metadados têm um campo de metatag definido para a tag de data de nascimento. Este campo está definido para digitar &quot;date&quot;.

**Regras de classificação**

Consulte [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.

Agora você adiciona uma nova regra de classificação. A regra é definida para usar o campo &quot;data de nascimento&quot; no documento. Uma nova regra de classificação é adicionada com o seguinte conjunto de propriedades:

* Tipo de fonte de dados: Meta tag
* Nome da fonte de dados: data de nascimento
* Pesos/Condições: 10 - Importância máxima
* Valores/fileiras: 9999999999 search_get_age_rank({data de nascimento}#14#0.10)
* Classificação padrão: -1

A regra faz várias coisas. O peso da regra é definido como 10. O valor de classificação é simplesmente o resultado da função de classificação etária, um valor de 0 a 1. Não é possível usar espaços com `search_get_age_rank()`. Além disso, observe que o campo &quot;data de nascimento&quot; está entre chaves. Finalmente, ao salvar essa regra, as vírgulas na definição Valores/fileiras são substituídas por `#` caracteres; esse comportamento é normal.

**Exibição dos resultados**

Use o recurso Visualização de dados para ver rapidamente os resultados da função de classificação etária. Adicione os campos Metadados apropriados. No exemplo, `age_val` e `myrank` são os dois campos de Metadados que devem ser adicionados à Visualização de dados. O `myrank` campo mostra como a classificação etária afeta os valores de classificação. O `age_val` campo mostra a saída bruta da função de decaimento exponencial para esse documento.

## Valores padrão {#section_CB109EF78F914E92955D512ACFC3310E}

Estes são três valores padrão envolvidos com a função `search_get_age_rank()`:

* O valor padrão que você pode inserir na própria `search_get_age_rank()` função.
* O valor de classificação padrão da regra de classificação.
* O valor padrão da definição de Metadados.

Dependendo de onde a falha ocorre, você pode obter valores padrão diferentes.

Por exemplo, o valor padrão da definição de Metadados nunca deve ocorrer se a Classificação e a Filtragem forem implementadas corretamente. Esse valor padrão é o último valor de recurso quando não existe nenhum conteúdo válido ou conhecido para esse campo de Metadados. O valor padrão das regras de classificação pode aparecer quando `search_get_age_rank()` estiver referenciando sua própria tag associada e a tag estiver ausente no documento. Nesse caso, essa regra vai diretamente para o valor padrão da regra. Se a função de classificação etária fizer referência à tag de outra regra de classificação, é possível que o valor padrão passado para essa função de classificação etária seja usado se a tag referenciada estiver ausente ou for inválida.

## Adicionar uma regra de classificação {#task_A132789FD4E5423DAD090DCDA7311E8A}

Você pode adicionar para afetar [!DNL Ranking Rules] a posição relativa das páginas da Web nos resultados da pesquisa, com base no conteúdo de cada página da Web.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Para adicionar uma regra de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Se você tiver criado um grupo de regras e adicionado regras ao grupo, na [!DNL Define Ranking Rules] **[!UICONTROL Select Rule Group]** página, na lista suspensa, selecione um grupo de regras que contenha as regras que deseja editar.

   Consulte [Adicionar um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de regras de classificação.
1. Na [!DNL Define Ranking Rules] página, clique **[!UICONTROL Add Rule]** para adicionar uma nova Regra de classificação ou para adicionar uma referência a um conjunto de regras.
1. Na [!DNL Add Ranking Rule] página, defina as opções desejadas. Os campos marcados com um asterisco (*) são obrigatórios.

   O Tipo de fonte de dados selecionado afeta as opções disponíveis na lista [!DNL Data Source Name] suspensa. Por exemplo, se você selecionou **[!UICONTROL Meta Tag]** como Tipo de fonte de dados, o Nome da fonte de dados se refere ao nome de uma tag meta nas páginas do site. Se você selecionou **[!UICONTROL Adobe Analytics Metric (Number)]**, o Nome da fonte de dados se refere a um dos nomes de métricas do Adobe Analytics que você selecionou em um Conjunto de relatórios, conforme encontrado na **[!UICONTROL Edit Adobe Analytics Metrics]** página em pesquisa/comercialização do site.

   Consulte [Editar as métricas do Adobe Analytics de um Conjunto](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664)de relatórios.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opção </p> </th> 
      <th colname="col2" class="entry"> <p>Descrição </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Tipo de fonte de dados </p> </td> 
      <td colname="col2"> <p>Determina as características da fonte de dados usada como entrada para essa regra de classificação. </p> <p>Os tipos de fonte de dados que podem ser selecionados incluem: 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> Meta tag </span> <p> Baseia essa regra em dados numéricos ou dados textuais armazenados em uma meta tag nomeada nas páginas do site. </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Métrica do Adobe Analytics (número) </span> <p>Baseia essa regra em uma métrica numérica do Adobe Analytics associada às páginas do site. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome da fonte de dados </p> </td> 
      <td colname="col2"> <p>Se você escolher <span class="uicontrol"> Meta Tag </span> como o Tipo de fonte de dados, este é o nome de uma meta tag encontrada nas páginas do seu site. Os nomes no menu suspenso vêm da lista de valores de metadados definidos que foram configurados em Configurações &gt; Metadados &gt; Definições. </p> <p>Consulte <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> Adicionando um novo campo de tag meta </a>. </p> <p>Se você escolher Métrica do Adobe Analytics (Número) como o Tipo de fonte de dados, esse será o nome de uma métrica do Adobe Analytics. Os nomes no menu suspenso vêm das métricas Adobe Analytics disponíveis definidas pela lista que foram configuradas em Configurações &gt; Adobe Analytics &gt; Métricas &gt; Editar. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Editando as métricas do Adobe Analytics de um Conjunto de relatórios </a>. </p> <p>Se o nome da métrica do Adobe Analytics que você selecionou ainda não estiver definido em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>, um campo de texto e um botão Adicionar serão exibidos. Digite o nome do campo Metadados (o nome do campo de metadados não pode exceder 20 caracteres) e clique em <span class="uicontrol"> Adicionar </span>. </p> <p>Quando as páginas são encontradas com várias chaves do Adobe Analytics, assim como com uma página de produto que exibe vários produtos, o Esquema composto especifica como lidar com os vários valores de métrica do Adobe Analytics associados a essa página. Selecione uma das seguintes opções: </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> Soma </span> <p>Retorna a soma dos valores da métrica. </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> Média </span> <p>Retorna a média dos valores (a soma dividida pelo número de valores). </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> Máximo </span> <p>Retorna o maior dos valores. </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> Primeiro </span> <p>Retorna o valor correspondente à primeira chave. </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> Última </span> <p>Retorna o valor correspondente à última chave. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesos/Condições </p> </td> 
      <td colname="col2"> <p>Contém um número de peso simples de regra única ou uma lista emparelhada de números de pesos de regras e condições de teste. </p> <p>Um número de peso de regra é um valor de 1 a 10 que indica a importância dessa regra de classificação em relação às outras regras de classificação para determinar a classificação geral de um documento. Um peso de regra superior indica maior importância. Um peso de zero (0) ignora a regra. </p> <p>Escolha <span class="uicontrol"> Personalizado </span> na lista suspensa para personalizar o peso da regra para várias páginas, definindo uma lista de pares de pesos de regras/condições de teste. As condições de teste são fragmentos de Perl usados para testar Valores da Fonte de Dados ou variáveis globais que são definidas dentro do script de filtro personalizado (por exemplo, preço, marca, estação ou visualizações de página, como no exemplo a seguir). Se uma condição de teste for avaliada como "true", o valor do peso da regra associado será aplicado. Se uma condição de teste for avaliada como "false", a próxima condição na lista será avaliada. <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>No exemplo de peso/condição criado personalizado acima, o peso de regra 0 será aplicado se a primeira condição de teste for avaliada como "true". Ou seja, o preço contém um valor maior que 50 e a marca contém "Kuhl"). Se a primeira condição de teste for avaliada como "false", a próxima condição será avaliada. Se nenhuma das condições anteriores for cumprida, a regra peso 5 será atribuída. </p> <p>Você sempre deve fornecer um peso de regra sem nenhuma condição no final da lista. Se você não fizer isso, a regra obterá um peso de 0 no caso em que nenhum dos testes de condição for avaliado como "true". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valores/classificações </p> </td> 
      <td colname="col2"> <p>Consiste em uma das funções de classificação incorporadas, ou em um conteúdo possível da Fonte de dados junto com as classificações desejadas. </p> <p>Se você escolher Métrica <span class="uicontrol"> Adobe Analytics (Número) </span> como o Tipo de fonte de dados, será apresentada uma lista suspensa com as seguintes opções: 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> Classificação automática por pedido (padrão) </span> <p>Calcula uma classificação baseada na posição relativa do documento, de acordo com sua Métrica do Adobe Analytics. Por exemplo, quanto mais próximo o documento estiver da posição mais alta, maior será a sua posição. </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> Classificação automática por valor </span> <p>Calcula uma classificação com base no valor relativo do documento, de acordo com sua Métrica do Adobe Analytics. Por exemplo, quanto mais próximo o valor do documento do documento classificado, maior será a sua classificação. </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol"> Personalizado </span> <p>Especifica configurações personalizadas. Por exemplo, uma Fonte de dados com o nome de "marca" pode conter o nome da marca de um produto específico. Você pode especificar a importância relativa de cada marca listando-a junto com sua classificação. </p> </li> 
      </ul> </p> <p>Os valores de classificação retornados dos cálculos de Classificação automática estão no intervalo de 0,0 (menor) a 1,0 (maior). Eles não são ajustados de acordo com os intervalos definidos para o campo Classificação em Configurações &gt; Metadados &gt; Definições. </p> <p>No exemplo a seguir, se a Fonte de Dados da marca para um resultado de pesquisa específico corresponder exatamente a "DKNY", a classificação aplicada para esse resultado será 0,5. Caso contrário, se a marca for "Levis", a classificação aplicada será 0,1. O conteúdo da Fonte de Dados deve corresponder ao valor definido. Em outras palavras, se o conteúdo da Fonte de Dados for "Levis Corp.", ele não corresponderá ao valor "Levis". O caso é ignorado, então "DKNY" corresponde a "dkny" e "Dkny". <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>Como uma opção mais avançada, você pode especificar valores como expressões regulares. Por exemplo, suponha que algumas de suas páginas do site contenham o valor de marca "Levis" e outras páginas do site contenham o valor de marca "jeans Levis". Você pode usar uma expressão regular especificada com a palavra-chave <code>
        regexp 
      </code>. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares </a>. </p> <p>No exemplo a seguir, um documento de resultado de pesquisa contendo o conteúdo da marca "jeans Levis" recebe uma classificação de 0.1. Como na comparação padrão, as letras maiúsculas e minúsculas são ignoradas para expressões regulares. <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação padrão </p> </td> 
      <td colname="col2"> <p> Especifica a classificação a ser aplicada para documentos de resultado de pesquisa que não correspondem a nenhum dos valores especificados. No exemplo acima, um documento de resultados de pesquisa com uma Fonte de Dados de "marca" contendo "a lacuna" recebe o valor padrão de classificação porque "a lacuna" não corresponde a nenhum dos valores definidos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Notas </p> </td> 
      <td colname="col2"> <p>Adicione informações relacionadas à definição de regra de classificação ou à definição de grupo de regras que você criou. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   O intervalo de valores de classificação válidos é normalmente de -1,0 a 1,0, como a seguir:

   * `-1.0` é &quot;Classificação mínima (exibir inferior nos resultados da pesquisa)&quot;.
   * `0.0` é &quot;Classificação neutra (não altere a ordem dos resultados da pesquisa)&quot;.
   * `1.0` é &quot;Classificação máxima (exibir maior nos resultados da pesquisa.&quot;

   As classificações definidas devem estar dentro do mesmo intervalo para cada regra. Os intervalos de classificação também devem corresponder aos intervalos definidos para o campo Classificação em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.

   Consulte também [Edição de uma regra](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275)de classificação.
1. Clique em **[!UICONTROL Add]**.
1. Para pré-visualização dos resultados da adição da regra, clique em **[!UICONTROL regenerate your staged site index]** para recriar o índice do site preparado.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editar uma regra de classificação {#task_5EBF55A43D6545FEA46BAE5E586FA275}

Você pode editar uma regra de classificação existente que já tenha adicionado.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Para editar uma regra de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Se você tiver criado um grupo de regras e adicionado quaisquer regras ao grupo, na **[!UICONTROL Define Ranking Rules]** **[!UICONTROL Select Rule Group]** página, na lista suspensa, selecione um grupo de regras que contenha as regras que deseja editar.

   Consulte [Adicionar um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de regras de classificação.
1. Na tabela, no cabeçalho da **[!UICONTROL Actions]** coluna, clique **[!UICONTROL Edit]** no nome da fonte de dados que deseja alterar.
1. Na [!DNL Edit Ranking Rule] página, defina as opções desejadas. Os campos marcados com um asterisco (*) são obrigatórios.

   Consulte a tabela de opções em [Adicionar uma regra](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A)de classificação.
1. Clique em **[!UICONTROL Save Changes]**.
1. Recrie o índice do site preparado para pré-visualização dos resultados da edição da regra.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma regra de classificação {#task_742A3BCC2A6E4164BE84CC7408807EBB}

Você pode excluir regras de classificação que não precisam mais ser usadas.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Consulte [Adicionar um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de regras de classificação.

**Para excluir uma regra de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Se você tiver criado um grupo de regras e adicionado quaisquer regras ao grupo, na [!DNL Define Ranking Rules] **[!UICONTROL Select Rule Group]** página, na lista suspensa, selecione um grupo de regras que contenha regras que deseja excluir.
1. Na tabela, no cabeçalho da **[!UICONTROL Actions]** coluna, clique **[!UICONTROL Delete]** no nome da fonte de dados que deseja alterar.
1. Na [!DNL Delete Ranking Rule] página, clique em **[!UICONTROL Delete]**.

   Você será redirecionado para a [!DNL Define Ranking Rules] página.
1. Recrie o índice do site preparado para pré-visualização nos resultados da exclusão da regra.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Adicionar um grupo de regras de classificação {#task_B65081B3CC9E4330A7FEE77B7BCD36C8}

Se você tiver definido mais de uma meta tag do tipo &quot;classificação&quot;, poderá criar coleções separadas de regras para usar no cálculo dos vários campos de classificação. Você pode adicionar um grupo de regras de classificação, que pode ser atribuído a um dos campos de Classificação definidos.

Os grupos de regras geralmente contêm uma ou mais regras que você adicionou. No entanto, os grupos de Regras também podem se referir a outros grupos de Regras. Por exemplo, você pode criar um ou mais grupos de regras e adicionar regras comumente usadas a cada um. Essas regras são compartilhadas durante o cálculo de suas múltiplas classificações.

Consulte [Edição de um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5)de regras de classificação.

Consulte [Excluindo um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA)de regras de classificação.

Consulte [Revisando grupos](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E)de regras de classificação.

**Para adicionar um grupo de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na [!DNL Define Ranking Rules] página, à direita da lista **[!UICONTROL Select Rule Group]** suspensa, clique em **[!UICONTROL Add]**.
1. Na [!DNL Add Ranking Rule Group] página, no **[!UICONTROL Rule Group Name]** campo, digite um nome exclusivo para o novo grupo de regras.
1. Na lista **[!UICONTROL Rank Field Name]** suspensa, selecione um nome de campo de metadados de classificação que você deseja associar ao novo grupo de regras. Selecione **[!UICONTROL None]** se você não deseja atribuir uma classificação.

   A lista de nomes de campos de classificação provém de definições de metadados que foram adicionadas em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte a tabela de opções em [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.
1. Clique em **[!UICONTROL Add]**.
1. Recrie o índice do site preparado para pré-visualização dos resultados da adição da regra.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edição de um grupo de regras de classificação {#task_D3EC0437E47144BC9E754FEF99C725E5}

É possível editar as configurações de um grupo de regras de classificação existente.

Consulte [Adicionar um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de regras de classificação.

**Para editar um grupo de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na [!DNL Define Ranking Rules] página, à direita da lista **[!UICONTROL Select Rule Group]** suspensa, clique em **[!UICONTROL Edit]**.
1. Na [!DNL Edit Ranking Rule Group] página, no **[!UICONTROL Rule Group Name]** campo, digite um nome exclusivo para o grupo de regras.
1. Na lista **[!UICONTROL Rank Field Name]** suspensa, selecione um nome de campo de metadados de classificação que você deseja associar ao grupo de regras. Selecione **[!UICONTROL None]** se você não deseja atribuir uma classificação.

   A lista de nomes de campos de classificação provém de definições de metadados que foram adicionadas em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte a tabela de opções em [Adicionar um novo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de tag meta.
1. Clique em **[!UICONTROL Save Changes]**.
1. Recrie o índice do site preparado para pré-visualização dos resultados da adição da regra.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo um grupo de regras de classificação {#task_BE5BE01F377843BEA9846E094A07F2EA}

Você pode excluir um Grupo de regras de classificação que não precisa mais ou não usa. Quando você exclui um grupo, quaisquer Regras que foram adicionadas ao grupo também são excluídas. Não é possível excluir o grupo padrão &quot;Regras de classificação&quot;.

O conteúdo de qualquer Grupo de regras contido no grupo de exclusão não é excluído; somente as referências a esses grupos são removidas.

Certifique-se de reindexar seu site para que a alteração seja refletida corretamente nos resultados da pesquisa.

Consulte [Adicionar um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de regras de classificação.

**Para excluir um grupo de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na [!DNL Define Ranking Rules] página, na lista **[!UICONTROL Select Rule Group]** suspensa, selecione um grupo que deseja excluir.
1. À direita da lista **[!UICONTROL Select Rule Group]** suspensa, clique em **[!UICONTROL Delete]**.
1. Na [!DNL Delete Ranking Rule Group] página, clique em **[!UICONTROL Delete]**.
1. Recrie o índice do site preparado para pré-visualização dos resultados da adição da regra.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Revisando grupos de regras de classificação {#task_5694459D050C4254A25186038CD66B6E}

Você pode usar a Visão geral dos grupos de regras de classificação para ver cada grupo Nome do campo de classificação, fonte de dados e ponderação associados.

Consulte [Adicionar um grupo](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8)de regras de classificação.

**Para revisar grupos de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na [!DNL Define Ranking Rules] página, à direita da lista **[!UICONTROL Select Rule Group]** suspensa, clique em **[!UICONTROL Overview]**.
1. Na [!DNL Ranking Rule Groups Overview] página, clique **[!UICONTROL Close]** para retornar à [!DNL Define Ranking Rules] página.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Testando regras de classificação {#task_56F64EE7ED5B42E481F0990A9DD98ADB}

Você pode fornecer um URL adequado para testar as definições de Regra de classificação que você configurou. As métricas usadas nos cálculos são exibidas, juntamente com o valor de Classificação calculado.

Consulte [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

**Para testar regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na [!DNL Define Ranking Rules] página, na área **[!UICONTROL Test URL]** , digite o URL para uma página da Web que esteja em seu site.
1. Clique em **[!UICONTROL Test]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Uso da opção](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Histórico.

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ajustar o peso associado às regras de classificação {#task_3CB6FC92A66F4D99874A42D55825DB64}

Você pode alterar as contribuições relativas de suas Regras de classificação individuais e a contribuição da classificação para os resultados da pesquisa final.

Quando a classificação não está definida, os resultados da pesquisa são 100% no **[!UICONTROL Natural Relevance]** lado da barra deslizante Regras e relevância na **[!UICONTROL Adjust Ranking Weights]** página. Esse equilíbrio simplesmente significa que os resultados da pesquisa são ordenados com base apenas em termos de pesquisa.

Quando a Classificação é definida, o campo de metadados de Classificação associado recebe um valor de Relevância, que varia de 1 a 10. Um valor de 1 significa que a Classificação calculada representa 10% da ordem do resultado da pesquisa, e a Relevância Natural representa os 90% restantes.

Se você tiver mais de uma Regra definida em um grupo de Regras, o valor de Peso de cada Regra determinará o quanto o resultado dessa Regra contribui para a Classificação calculada total. Por exemplo, suponha que você tenha uma Relevância Natural de 80%, o que significa que a relevância do campo Classificação associado é 2. Você também definiu duas Regras: um com peso de 3 e o segundo com peso de 7. Nesse caso, a contribuição da primeira Regra para o resultado final é de 6% ((3 / (3+7)) * 20%). A contribuição da segunda regra para o resultado final é de 14% ((7 / (3+7)) * 20%).

**Para ajustar o peso associado às regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Adjust Weights]**.
1. Na [!DNL Adjust Ranking Weights] página, na lista **[!UICONTROL Select Rule Group]** suspensa, selecione um grupo cujos pesos de classificação você deseja ajustar.
1. Arraste os controles deslizantes para alterar os valores de contribuição correspondentes.

   O gráfico setorial reflete suas alterações graficamente.
1. Clique em **[!UICONTROL Save Changes]**.
1. Recrie o índice do site preparado para pré-visualização dos resultados da adição da regra.

   Consulte [Executando um índice completo de um site ao vivo ou preparado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executando um índice incremental de um site ao vivo ou preparado...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Visualizar configurações](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)ativas.

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Colocar configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
