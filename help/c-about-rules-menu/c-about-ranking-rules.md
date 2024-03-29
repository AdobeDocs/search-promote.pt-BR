---
description: Você pode usar as Regras de classificação para controlar o posicionamento relativo ou a classificação dos resultados de pesquisa de um cliente com base no conteúdo da meta tag contida e nas métricas relacionadas do Adobe Analytics.
solution: Target
subtopic: Ranking Rules
title: Sobre as regras de classificação
topic-legacy: Rules,Site search and merchandising
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
exl-id: 7f66c4f6-7659-4faf-9f05-b650cf8c7d47
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '4616'
ht-degree: 0%

---

# Sobre as Regras de Classificação{#about-ranking-rules}

Você pode usar as Regras de classificação para controlar o posicionamento relativo ou a classificação dos resultados de pesquisa de um cliente com base no conteúdo da meta tag contida e nas métricas relacionadas do Adobe Analytics.

## Usando Regras de Classificação {#concept_F555C076759B4E81B925441CFE707397}

Você define regras de classificação para afetar o posicionamento relativo dos documentos nos resultados da pesquisa, com base no conteúdo de cada documento. É possível basear as regras de classificação no conteúdo da meta tag, nas métricas do Adobe Analytics (se a conta estiver configurada para funcionar com o Adobe Analytics) ou nas métricas do Adobe Analytics HBX (se a conta estiver configurada para funcionar com o Adobe Analytics HBX).

É possível definir páginas da Web que contêm metatags com as características desejadas, como um determinado nome de marca ou preço, ou páginas da Web que tenham indicadores-chave de desempenho do Adobe Analytics desejáveis, como visualizadores únicos, para receber uma classificação maior que as páginas da Web que não possuem. As características &quot;desejáveis&quot; são facilmente atualizadas adicionando ou editando Regras de classificação e, em seguida, reindexando seu site.

Se você tiver mais de uma meta tag do tipo &quot;classificação&quot; definida, poderá criar coleções separadas de regras para usar no cálculo dos vários campos de classificação. Você pode adicionar um grupo de regras de classificação, que pode ser atribuído a um dos campos de Classificação definidos. Os grupos de regras normalmente contêm uma ou mais definições de regra, mas também podem se referir a outros grupos de Regras, para que você possa criar um ou mais grupos de regras usadas com frequência que são compartilhadas durante o cálculo de suas várias classificações.

Consulte [Adicionar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

Um valor de classificação positivo promove os resultados da pesquisa para o topo; um valor negativo de classificação demostra os resultados da pesquisa na parte inferior dos resultados da pesquisa. O intervalo normal para valores de classificação é 1,0, que é a promoção máxima nos resultados da pesquisa, enquanto -1,0 é a remoção máxima. Embora você possa personalizar esse intervalo editando o campo Classificação nas definições de metadados, esse tipo de personalização geralmente é desnecessário.

Consulte [Sobre Definições](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620).

Se tiver definido mais de um campo de classificação em Configurações > Metadados > Definições, você terá a opção de criar conjuntos adicionais de regras de classificação, um para cada campo de classificação. Você pode definir conjuntos adicionais de regras de classificação sem estar diretamente associado a um campo de classificação. Essa flexibilidade permite criar conjuntos de regras comuns que podem ser compartilhadas no cálculo de um ou mais valores de classificação.

**Importante**: Antes de usar Regras de classificação, há várias etapas de configuração de conta que você deve concluir.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## Configuração da classificação {#task_4CEBC13925B047FC95BDC217B48089C5}

Antes de usar regras de classificação, há várias etapas de configuração de conta que você deve concluir.

**Para configurar a classificação**

1. Escolha entre as opções a seguir:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Tarefa </p> </th> 
      <th colname="col2" class="entry"> <p>Configuração </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Para criar regras de classificação baseadas em metatags </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> No menu do produto, clique em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>. </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> Na página Definições , clique em <span class="uicontrol"> Adicionar novo campo </span>. </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> Na página Adicionar campo , no campo de texto <span class="uicontrol"> Nome do campo </span>, digite 
      <code>
        rank 
      </code>; no campo de texto <span class="uicontrol"> Nome da Meta Tag </span>, digite 
      <code>
        rank 
      </code>; na lista suspensa <span class="uicontrol"> Tipo de dados </span> , selecione <span class="uicontrol"> Classificação </span>. Deixe todas as outras opções de campo como estão. <p>Consulte o parâmetro de consulta <span class="codeph"> sp_sr </span> em <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parâmetros CGI de pesquisa de backend </a>. </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">Clique em <span class="uicontrol">Adicionar </span>. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Para criar regras de classificação baseadas nas métricas do Adobe Analytics </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> Certifique-se de configurar a autenticação do Adobe Analytics a partir da pesquisa/comercialização do site. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> Configuração da autenticação de métricas do Adobe Analytics </a>. </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> Selecione e adicione um conjunto de relatórios disponível. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> Adicionando um conjunto de relatórios do Adobe Analytics </a>. </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> Configure a lista de métricas do Adobe Analytics que você deseja disponibilizar para a criação de novas Regras de classificação. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Editar as métricas do Adobe Analytics de um Conjunto de relatórios </a>. </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Carregue as métricas iniciais do Adobe Analytics para as páginas de seu site. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> Carregando dados do Adobe Analytics </a>. </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Adicione uma ou mais regras de classificação.

   Consulte [Adicionar uma regra de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

1. Clique em **[!UICONTROL regenerate your staged site index]** para executar uma reindexação completa do seu site (de **[!UICONTROL Index]** > **[!UICONTROL Full Index]**).

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. Verifique os valores na coluna Classificação em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** para verificar se as Regras de classificação foram aplicadas corretamente.

## Sobre documentos de classificação por idade {#topic_770815CF1B2A491F83FF765871B6F1B8}

Você pode classificar um documento HTML por idade com uma função de declínio exponencial. A taxa de decaimento é especificada com uma constante de meia-vida escolhida, a quantidade de tempo que deve passar antes que o valor caia para metade do seu valor inicial.

A classificação por idade baseia-se nas duas equações a seguir:

`K = -ln(2) / H`

`RANK = e^(K * T)`

As variáveis `H` e `T` são entradas para esta função: `H` é o período de meia-vida desejado e `T` é a idade do documento, expressa em segundos. `K` é a meia-vida calculada e  `RANK` é a decadência exponencial do valor de idade especificado. O valor resultante é de 0 a 1. Um documento mais recente tem um valor de classificação mais próximo de 1 em comparação a um documento mais antigo. Em teoria, os documentos nunca devem alcançar o valor 0, mas o arredondamento de erros pode fazer com que um resultado se torne 0.

## Requisitos para usar a classificação de idade {#section_D716507D589442C6B7848892BD28F966}

* Sua conta já deve estar configurada corretamente para classificação. Se não estiver configurado, consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).
* O documento HTML deve ter um campo de meta tag HTML que represente sua data de nascimento, sua criação como um carimbo de data e hora ou algum outro valor de data significativo.
* A função incorporada especial, `search_get_age_rank()`, conforme especificado nas páginas Adicionar ou Editar Regra de Classificação, é usada para calcular a classificação etária de um documento. As seções seguintes descrevem pormenorizadamente a utilização geral da função de classificação por idade. Um exemplo também é apresentado e demonstra o recurso de classificação por idade.

## Usando search_get_age_rank () na página Adicionar Regra de Classificação ou na página Editar Regra de Classificação {#section_34BC5276F2AB4419AD92872A397CA0AF}

Especifique `search_get_age_rank()` da seguinte maneira:

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* Birthdate - A data de nascimento ou data de início do arquivo deve ser uma string formatada por data de acordo com os formatos de data do campo. Essa string formatada por data deve ser uma referência de campo, como em `{field_name}`.
* Half_Life - A meia-vida é a quantidade de tempo que deve passar antes que o valor caia para metade de seu valor inicial. Esse valor é expresso no número de dias e é um número inteiro ou um número de ponto flutuante.
* Default_Rank - A classificação padrão é usada como uma rede de segurança caso a data de nascimento seja inválida ou a data esteja no futuro. Não é possível usar esse valor padrão se o campo de metadados associado também tiver um valor padrão válido. O valor aqui é um número de ponto flutuante ou um número inteiro. Veja as sugestões abaixo se tiver problemas com o valor padrão em uso.

Consulte [Adicionar uma regra de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

Consulte [Editar uma regra de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).

**Exemplo**

No exemplo a seguir,

`search_get_age_rank({birthdate}#28#0.20)`

a data contida no campo `birthdate` do documento é passada como carimbo de data e hora. A meia-vida é de 28 dias. O valor de classificação padrão é 0,20 se a data for inválida.

Consulte a tabela de opções em [Adicionar uma regra de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

Na seção Valores/classificações da página Adicionar regra de classificação ou Editar regra de classificação , você só pode usar `search_get_age_rank` com regras personalizadas. Portanto, escolha **Personalizado** na lista suspensa Valores/classificações . Quando a regra usa a função de classificação por idade, nenhum espaço é permitido na parte de valores da regra. Verifique se não há espaços nos argumentos da função ou entre eles. E não há espaços entre operadores matemáticos ou condicionais.

Este é um exemplo de uma regra de valores/classificações, uma regra associada a um campo de texto:

`regexp .* search_get_age_rank({other_field}#365#0.20)`

Esse exemplo assume que `other_field` contém um valor de data. Se esse campo não for um campo do tipo data, esse valor será interpretado usando os formatos de data associados ao campo Date predefinido. Caso contrário, os formatos de data desse campo serão usados. Essa entrada de valores/classificações é usada sempre que o campo do documento, que a Fonte de Dados da Regra identifica, não está vazio e o valor de retorno da função (de 0 a 1) é a classificação atribuída.

Para uma Regra associada a um campo Numérico, especificamente um campo Data :

`9999999999 search_get_age_rank({other_field}#365#0.20)`

À medida que cada documento é processado, o valor em `other_field` é convertido no formulário Unix &quot;epoch&quot;, usando as definições de formato de data do campo. Esse valor é usado na chamada `search_get_age_rank()` . Como cada valor de &quot;época&quot; é menor que 9999999999 (por enquanto, pelo menos), a Regra simplesmente fornece o valor de retorno da função (de 0 a 1) como a classificação.

Em ambos os exemplos anteriores, é típico que a Fonte de Dados da Regra seja o mesmo campo usado na função `search_get_age_rank()` - `other_field` nesse caso.

## Um exemplo da integração da classificação de idade nas regras de classificação {#section_A86D909687CC45E19D4EA7A4A9283F28}

Este é um exemplo de como você pode integrar a classificação de idade às regras de classificação. O exemplo também mostra os resultados brutos da função de classificação por idade e os resultados das regras de classificação. O exemplo assume o seguinte:

* As páginas da Web que estão rastreadas têm uma meta tag HTML chamada &quot;data de nascimento&quot;. O conteúdo dessa tag é um carimbo de data e hora relacionado ao documento.
* As definições de metadados têm um campo de metatag definido para a tag de data de nascimento. Este campo é definido para o tipo &quot;data&quot;.

**Regras de classificação**

Consulte [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

Agora você adiciona uma nova regra de classificação. A regra é definida para usar o campo &quot;data de nascimento&quot; no documento. Uma nova regra de classificação é adicionada com o seguinte conjunto de propriedades:

* Tipo de Fonte de Dados: Meta tag
* Nome da Fonte de Dados: data de nascimento
* Pesos/Condições: 10 - Importância máxima
* Valores/classificações: 9999999999 search_get_age_rank({data de nascimento}#14#0.10)
* Classificação padrão: -1

A regra faz várias coisas. O peso da regra é definido como 10. O valor de classificação é simplesmente o resultado da função de classificação por idade, um valor de 0 a 1. Não é possível usar espaços com `search_get_age_rank()`. Além disso, observe que o campo &quot;data de nascimento&quot; está entre chaves. Finalmente, ao salvar essa regra, as vírgulas na definição Valores/Fileiras são substituídas por caracteres `#`; esse comportamento é normal.

**Visualização dos resultados**

Use o recurso Exibição de dados para ver rapidamente os resultados da função de classificação etária. Adicione os campos de Metadados apropriados. No exemplo, `age_val` e `myrank` são os dois campos de Metadados que devem ser adicionados à Exibição de dados. O campo `myrank` mostra como a classificação de idade afeta os valores de classificação. O campo `age_val` mostra a saída bruta da função de declínio exponencial para esse documento.

## Valores padrão {#section_CB109EF78F914E92955D512ACFC3310E}

A seguir estão três valores padrão envolvidos com a função `search_get_age_rank()`:

* O valor padrão que você pode inserir na própria função `search_get_age_rank()`.
* O valor de classificação padrão da regra de Classificação.
* O valor padrão da definição de Metadados.

Dependendo de onde a falha ocorre, é possível obter valores padrão diferentes.

Por exemplo, o valor padrão da definição de Metadados nunca deve ocorrer se a Classificação e a Filtragem forem implementadas corretamente. Esse valor padrão é o último valor de recurso quando não existe nenhum conteúdo válido ou conhecido para esse campo de Metadados. O valor padrão das regras de classificação pode aparecer quando `search_get_age_rank()` estiver referenciando sua própria tag associada e a tag estiver ausente no documento. Nesse caso, essa regra vai diretamente para o valor padrão da regra. Se a função de classificação por idade fizer referência à tag de outra regra de classificação, é possível que o valor padrão passado para essa função de classificação por idade seja usado se a tag referenciada estiver ausente ou inválida.

## Adicionar uma regra de classificação {#task_A132789FD4E5423DAD090DCDA7311E8A}

Você pode adicionar [!DNL Ranking Rules] para afetar o posicionamento relativo das páginas da Web nos resultados da Pesquisa, com base no conteúdo de cada página da Web.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Para adicionar uma regra de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Caso tenha criado um grupo de regras e adicionado regras ao grupo, na página [!DNL Define Ranking Rules] , na lista suspensa **[!UICONTROL Select Rule Group]**, selecione um grupo de regras que contenha as regras que deseja editar.

   Consulte [Adicionar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).
1. Na página [!DNL Define Ranking Rules] , clique em **[!UICONTROL Add Rule]** para adicionar uma nova Regra de Classificação ou para adicionar uma referência a um conjunto de Regras.
1. Na página [!DNL Add Ranking Rule], defina as opções desejadas. Os campos marcados com um asterisco (*) são obrigatórios.

   O Tipo de fonte de dados selecionado afeta as opções disponíveis na lista suspensa [!DNL Data Source Name]. Por exemplo, se você selecionou **[!UICONTROL Meta Tag]** como o Tipo de fonte de dados, o Nome da fonte de dados se refere ao nome de uma meta tag nas páginas do site. Se você selecionou **[!UICONTROL Adobe Analytics Metric (Number)]**, o Nome da Fonte de Dados refere-se a um dos nomes de métricas do Adobe Analytics que você selecionou em um Conjunto de relatórios, conforme encontrado na página **[!UICONTROL Edit Adobe Analytics Metrics]** em pesquisa/merchandising do site.

   Consulte [Editar as métricas do Adobe Analytics de um Report Suite](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

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
      <td colname="col2"> <p>Determina as características da fonte de dados usada como entrada para essa regra de classificação. </p> <p>Os tipos de fonte de dados que você pode selecionar incluem: 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> Meta tag  </span> <p> Baseia essa regra em dados numéricos ou textuais armazenados em uma meta tag nomeada nas páginas do site. </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Métrica do Adobe Analytics (Número)  </span> <p>Baseia essa regra em uma métrica numérica do Adobe Analytics associada às páginas do site. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nome da fonte de dados </p> </td> 
      <td colname="col2"> <p>Se você escolheu <span class="uicontrol"> Meta tag </span> como o Tipo de fonte de dados, esse é o nome de uma meta tag encontrada nas páginas do seu site. Os nomes no menu suspenso vêm da lista de valores de metadados definidos que foram configurados em Configurações &gt; Metadados &gt; Definições. </p> <p>Consulte <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> Adicionar um novo campo de metatag </a>. </p> <p>Caso tenha escolhido Métrica do Adobe Analytics (Número) como Tipo de fonte de dados, esse é o nome de uma métrica do Adobe Analytics. Os nomes no menu suspenso vêm da lista que define as métricas disponíveis do Adobe Analytics que foram configuradas em Configurações &gt; Adobe Analytics &gt; Métricas &gt; Editar. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Editar as métricas do Adobe Analytics de um Conjunto de relatórios </a>. </p> <p>Se o nome da métrica do Adobe Analytics selecionada ainda não estiver definido em <span class="uicontrol"> Configurações </span> &gt; <span class="uicontrol"> Metadados </span> &gt; <span class="uicontrol"> Definições </span>, um campo de texto e um botão Adicionar serão exibidos. Insira o nome do Nome do campo de metadados (o nome do campo de metadados não pode exceder 20 caracteres) e clique em <span class="uicontrol"> Adicionar </span>. </p> <p>Quando as páginas são encontradas com várias chaves Adobe Analytics, assim como com uma página de produto exibindo vários produtos, o Esquema Composto especifica como lidar com os vários valores de métrica do Adobe Analytics associados a essa página. Selecione uma das opções a seguir: </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> Soma </span> <p>Retorna a soma dos valores da métrica. </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> Média </span> <p>Retorna a média dos valores (a soma dividida pelo número de valores). </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> Máximo  </span> <p>Retorna o maior dos valores. </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> Primeiro </span> <p>Retorna o valor correspondente à primeira chave. </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> Última </span> <p>Retorna o valor correspondente à última chave. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesos/Condições </p> </td> 
      <td colname="col2"> <p>Contém um número de peso de regra simples, único ou uma lista emparelhada de números de peso de regras e condições de teste. </p> <p>Um número de peso de regra é um valor de 1 a 10 que indica a importância dessa regra de classificação em relação às outras regras de classificação na determinação da classificação geral de um documento. Um peso de regra mais alto indica maior importância. Um peso de zero (0) ignora a regra. </p> <p>Escolha <span class="uicontrol"> Personalizado </span> na lista suspensa para personalizar o peso da regra para várias páginas, definindo uma lista de pares de peso da regra/condições de teste. As condições de teste são fragmentos de Perl usados para testar os Valores da Fonte de Dados ou variáveis globais que são definidas dentro do script de filtro personalizado (por exemplo, preço, marca, estação ou exibições de página, como no exemplo a seguir). Se uma condição de teste for avaliada como "true", o valor de peso da regra associado será aplicado. Se uma condição de teste for avaliada como "false", a próxima condição na lista será avaliada. <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>No exemplo de peso/condição criado e personalizado acima, o peso da regra 0 é aplicado se a primeira condição de teste for avaliada como "true". Ou seja, o preço contém um valor maior que 50 e a marca contém "Kuhl"). Se a primeira condição de teste for avaliada como "false", a próxima condição será avaliada. Se nenhuma das condições anteriores for atendida, o peso da regra 5 será atribuído. </p> <p>Você sempre deve fornecer um peso de regra sem condição no final da lista. Se você não fizer isso, a regra obterá um peso de 0 no caso em que nenhum dos testes de condição for avaliado como "true". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valores/classificações </p> </td> 
      <td colname="col2"> <p>Consiste em uma das funções de classificação incorporadas ou no conteúdo possível da Fonte de Dados, juntamente com as classificações desejadas. </p> <p>Se você escolher <span class="uicontrol"> Métrica do Adobe Analytics (Número) </span> como o Tipo de fonte de dados, você verá uma lista suspensa com as seguintes opções: 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> Classificação automática por pedido (padrão)  </span> <p>Calcula uma classificação baseada na posição relativa do documento, de acordo com a Métrica do Adobe Analytics. Por exemplo, quanto mais próxima a posição do documento em relação ao documento de primeira classificação, maior a sua classificação. </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> Classificação automática por valor  </span> <p>Calcula uma classificação com base no valor relativo do documento, de acordo com a Métrica do Adobe Analytics. Por exemplo, quanto mais próximo o valor do documento estiver do valor do documento classificado mais alto, maior será a sua classificação. </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol"> Personalizado </span> <p>Especifica configurações personalizadas. Por exemplo, uma fonte de dados com o nome de "marca" pode conter o nome da marca de um produto específico. Você pode especificar a importância relativa de cada marca, listando-a junto com sua classificação. </p> </li> 
      </ul> </p> <p>Os valores de classificação retornados dos cálculos de Classificação automática estão no intervalo de 0,0 (o mais baixo) a 1,0 (o mais alto). Elas não são ajustadas de acordo com os intervalos definidos para o campo Classificação em Configurações &gt; Metadados &gt; Definições. </p> <p>No exemplo a seguir, se a Fonte de Dados da marca para um resultado de pesquisa específico corresponder exatamente a "DKNY", a classificação aplicada para esse resultado será 0,5. Caso contrário, se a marca for "Levis", a classificação aplicada será 0,1. O conteúdo da Fonte de Dados deverá corresponder ao valor definido. Em outras palavras, se o conteúdo da Fonte de Dados for "Levis Corp.", ele não corresponderá ao valor "Levis". O caso é ignorado, portanto, "DKNY" corresponde a "dkny" e "Dkny". <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>Como opção mais avançada, você pode especificar valores como expressões regulares. Por exemplo, suponha que algumas de suas páginas do site contenham um valor de marca de "Levis" e outras páginas contenham um valor de marca de "jeans Levis". Você pode usar uma expressão regular especificada com a palavra-chave 
      <code>
        regexp 
      </code>. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressões regulares </a>. </p> <p>No exemplo a seguir, um documento de resultado de pesquisa contendo o conteúdo da marca "jeans Levis" recebe uma classificação de 0.1. Como na comparação padrão, maiúsculas e minúsculas são ignoradas para expressões regulares. <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classificação padrão </p> </td> 
      <td colname="col2"> <p> Especifica a classificação a ser aplicada para documentos de resultados de pesquisa que não correspondem a nenhum dos valores especificados. No exemplo acima, um documento de resultados de pesquisa com uma Fonte de Dados de "marca" contendo "a lacuna" é atribuído ao valor de classificação padrão porque "a lacuna" não corresponde a nenhum dos valores definidos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Notas </p> </td> 
      <td colname="col2"> <p>Adicione informações que pertencem à definição de regra de classificação ou à definição de grupo de regras criada. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   O intervalo de valores de classificação válidos é normalmente de -1,0 a 1,0, como no seguinte:

   * `-1.0` é &quot;Classificação mínima (exibir menor nos resultados da pesquisa)&quot;.
   * `0.0` é &quot;Classificação neutra (não altere a ordem dos resultados da pesquisa)&quot;.
   * `1.0` é &quot;Classificação máxima (exibir maior nos resultados da pesquisa&quot;.

   As classificações definidas devem estar dentro do mesmo intervalo para cada regra. Os intervalos de classificação também devem corresponder aos intervalos definidos para o campo Classificação em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

   Consulte também [Editar uma regra de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).
1. Clique em **[!UICONTROL Add]**.
1. Para visualizar os resultados da adição da regra, clique em **[!UICONTROL regenerate your staged site index]** para recriar o índice do site preparado.

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editando uma regra de classificação {#task_5EBF55A43D6545FEA46BAE5E586FA275}

É possível editar uma regra de classificação existente que já foi adicionada.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Para editar uma regra de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Se você tiver criado um grupo de regras e adicionado regras ao grupo, na página **[!UICONTROL Define Ranking Rules]**, na lista suspensa **[!UICONTROL Select Rule Group]**, selecione um grupo de regras que contenha as regras que deseja editar.

   Consulte [Adicionar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).
1. Na tabela, no cabeçalho da coluna **[!UICONTROL Actions]**, clique em **[!UICONTROL Edit]** para obter o nome da fonte de dados que deseja alterar.
1. Na página [!DNL Edit Ranking Rule], defina as opções desejadas. Os campos marcados com um asterisco (*) são obrigatórios.

   Consulte a tabela de opções em [Adicionar uma regra de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).
1. Clique em **[!UICONTROL Save Changes]**.
1. Reconstrua o índice do site preparado para visualizar os resultados da edição de regras.

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo uma regra de classificação {#task_742A3BCC2A6E4164BE84CC7408807EBB}

Você pode excluir regras de classificação que não precisam mais ser usadas.

Consulte [Configuração da classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Consulte [Adicionar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para excluir uma regra de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Se você tiver criado um grupo de regras e adicionado regras ao grupo, na página [!DNL Define Ranking Rules], na lista suspensa **[!UICONTROL Select Rule Group]**, selecione um grupo de regras que contenha regras que deseja excluir.
1. Na tabela, no cabeçalho da coluna **[!UICONTROL Actions]**, clique em **[!UICONTROL Delete]** para obter o nome da fonte de dados que deseja alterar.
1. Na página [!DNL Delete Ranking Rule], clique em **[!UICONTROL Delete]**.

   Você é retornado à página [!DNL Define Ranking Rules].
1. Recrie o índice do site preparado para visualizar os resultados da exclusão de regra.

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Adicionar um grupo de regras de classificação {#task_B65081B3CC9E4330A7FEE77B7BCD36C8}

Se você tiver definido mais de uma meta tag do tipo &quot;classificação&quot;, poderá criar coleções separadas de regras para usar no cálculo dos vários campos de classificação. Você pode adicionar um grupo de regras de classificação, que pode ser atribuído a um dos campos de Classificação definidos.

Os grupos de regras geralmente contêm uma ou mais regras adicionadas. No entanto, os grupos de Regras também podem se referir a outros grupos de Regras. Por exemplo, você pode criar um ou mais grupos de regras e adicionar regras comumente usadas a cada um. Essas regras são compartilhadas durante o cálculo de suas várias classificações.

Consulte [Editar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5).

Consulte [Excluindo um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA).

Consulte [Revisando grupos de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E).

**Para adicionar um grupo de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na página [!DNL Define Ranking Rules], à direita da lista suspensa **[!UICONTROL Select Rule Group]**, clique em **[!UICONTROL Add]**.
1. Na página [!DNL Add Ranking Rule Group], no campo **[!UICONTROL Rule Group Name]**, digite um nome exclusivo para o novo grupo de regras.
1. Na lista suspensa **[!UICONTROL Rank Field Name]**, selecione um nome de campo de metadados de classificação que deseja associar ao novo grupo de regras. Selecione **[!UICONTROL None]** se não quiser atribuir uma classificação.

   A lista de nomes de campos de classificação vem das definições de metadados que foram adicionadas em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte a tabela de opções em [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Clique em **[!UICONTROL Add]**.
1. Reconstrua o índice do site preparado para visualizar os resultados da adição da regra.

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editando um grupo de regras de classificação {#task_D3EC0437E47144BC9E754FEF99C725E5}

É possível editar as configurações de um grupo de regras de classificação existente.

Consulte [Adicionar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para editar um grupo de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na página [!DNL Define Ranking Rules], à direita da lista suspensa **[!UICONTROL Select Rule Group]**, clique em **[!UICONTROL Edit]**.
1. Na página [!DNL Edit Ranking Rule Group], no campo **[!UICONTROL Rule Group Name]**, digite um nome exclusivo para o grupo de regras.
1. Na lista suspensa **[!UICONTROL Rank Field Name]**, selecione um nome de campo de metadados de classificação que deseja associar ao grupo de regras. Selecione **[!UICONTROL None]** se não quiser atribuir uma classificação.

   A lista de nomes de campos de classificação vem das definições de metadados que foram adicionadas em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte a tabela de opções em [Adicionar um novo campo de metatag](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Clique em **[!UICONTROL Save Changes]**.
1. Reconstrua o índice do site preparado para visualizar os resultados da adição da regra.

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Excluindo um grupo de regras de classificação {#task_BE5BE01F377843BEA9846E094A07F2EA}

É possível excluir um Grupo de regras de classificação que não é mais necessário ou usado. Quando você exclui um grupo, quaisquer Regras que foram adicionadas ao grupo também são excluídas. Não é possível excluir o grupo padrão &quot;Regras de classificação&quot;.

O conteúdo de qualquer Grupo de regras contido no grupo de exclusão não é excluído; apenas as referências a esses grupos são removidas.

Certifique-se de reindexar seu site para que a alteração seja refletida corretamente nos resultados da pesquisa.

Consulte [Adicionar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para excluir um grupo de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na página [!DNL Define Ranking Rules] , na lista suspensa **[!UICONTROL Select Rule Group]**, selecione um grupo que deseja excluir.
1. À direita da lista suspensa **[!UICONTROL Select Rule Group]**, clique em **[!UICONTROL Delete]**.
1. Na página [!DNL Delete Ranking Rule Group], clique em **[!UICONTROL Delete]**.
1. Reconstrua o índice do site preparado para visualizar os resultados da adição da regra.

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Revisando grupos de regras de classificação {#task_5694459D050C4254A25186038CD66B6E}

Você pode usar a Visão geral de grupos de regras de classificação para ver cada grupo Nome do campo de classificação, fonte de dados e ponderação associados.

Consulte [Adicionar um grupo de regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para analisar grupos de regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na página [!DNL Define Ranking Rules], à direita da lista suspensa **[!UICONTROL Select Rule Group]**, clique em **[!UICONTROL Overview]**.
1. Na página [!DNL Ranking Rule Groups Overview] , clique em **[!UICONTROL Close]** para retornar à página [!DNL Define Ranking Rules].
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Teste das regras de classificação {#task_56F64EE7ED5B42E481F0990A9DD98ADB}

Você pode fornecer um URL adequado para testar as definições de Regra de classificação que você configurou. As métricas usadas nos cálculos são exibidas, juntamente com o valor de Classificação calculado.

Consulte [Sobre regras de classificação](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

**Para testar as regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. Na página [!DNL Define Ranking Rules], na área **[!UICONTROL Test URL]**, digite o URL para uma página da Web que esteja em seu site.
1. Clique em **[!UICONTROL Test]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ajustar o peso associado às regras de classificação {#task_3CB6FC92A66F4D99874A42D55825DB64}

Você pode alterar as contribuições relativas de suas Regras de classificação individuais e a contribuição da Classificação para os resultados finais da pesquisa.

Quando a Classificação não está definida, os resultados da pesquisa são 100% no lado **[!UICONTROL Natural Relevance]** da barra deslizante Regras e relevância na página **[!UICONTROL Adjust Ranking Weights]**. Esse equilíbrio significa simplesmente que os resultados da pesquisa são ordenados com base apenas nos termos de pesquisa.

Quando a Classificação é definida, o campo de metadados de Classificação associado recebe um valor de Relevância, que varia de 1 a 10. Um valor de 1 significa que a Classificação calculada representa 10% da ordem do resultado da pesquisa e a Relevância natural representa os 90% restantes.

Se você tiver mais de uma Regra definida em um grupo de Regras, o valor de Peso de cada Regra determinará quanto o resultado dessa Regra contribuirá para a Classificação calculada total. Por exemplo, suponha que você tenha uma Relevância natural de 80%, o que significa que a relevância do campo Classificação associado é 2. Você também definiu duas Regras: um com peso de 3 e o segundo com peso de 7. Nesse caso, a primeira contribuição da Regra para o resultado final é de 6% ((3 / (3+7)) * 20%). A segunda contribuição da Regra para o resultado final é de 14% ((7 / (3+7)) * 20%).

**Para ajustar o peso associado às regras de classificação**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Adjust Weights]**.
1. Na página [!DNL Adjust Ranking Weights] , na lista suspensa **[!UICONTROL Select Rule Group]**, selecione um grupo cujos pesos de classificação você deseja ajustar.
1. Arraste os controles deslizantes para alterar os valores de contribuição correspondentes.

   O gráfico de pizza reflete suas alterações graficamente.
1. Clique em **[!UICONTROL Save Changes]**.
1. Reconstrua o índice do site preparado para visualizar os resultados da adição da regra.

   Consulte [Executar um índice completo de um site ativo ou temporário...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Executar um índice incremental de um site ativo ou temporário...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
