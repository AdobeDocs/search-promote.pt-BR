---
description: A Proximity Search permite associar um local exclusivo a qualquer página do seu site e, em seguida, pesquisar e classificar os resultados por proximidade (distância) de um determinado local.
seo-description: A Proximity Search permite associar um local exclusivo a qualquer página do seu site e, em seguida, pesquisar e classificar os resultados por proximidade (distância) de um determinado local.
seo-title: Sobre a pesquisa de proximidade
solution: Target
title: Sobre a pesquisa de proximidade
topic: Appendices,Site search and merchandising
uuid: 24fc9265-3400-46a7-b6e0-4de5b049a39a
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---


# Sobre a pesquisa de proximidade{#about-proximity-search}

A Proximity Search permite associar um local exclusivo a qualquer página do seu site e, em seguida, pesquisar e classificar os resultados por proximidade (distância) de um determinado local.

Por exemplo, suponha que você tenha preenchido páginas em seu site com metadados de CEP dos Estados Unidos, como o seguinte:

```
<meta name="zipcode" content="84057">
```

Em seguida, você configura sua conta para indexar seus metadados do CEP. Em **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** > **[!UICONTROL Add New Field]**, na página [!DNL Add Field], defina as seguintes opções:

* Nome do campo: `zip`
* Nome(s) da tag meta: `zipcode`
* Tipo de dados: **[!UICONTROL Location]**
* Classificação: **[!UICONTROL Ascending]**
* Unidades padrão: **[!UICONTROL Miles]**

Depois de indexar o site, execute a seguinte pesquisa:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_s=zip_proximity
```

O conjunto de resultados contém quaisquer documentos localizados a 100 milhas do código ZIP 84057, classificados em ordem crescente de distância desse código ZIP.

Você também pode usar códigos de área telefônica para locais nos Estados Unidos. Ou você pode usar pares de latitude/longitude para especificar locais nos metadados do site e nos critérios de pesquisa. O tipo de local é determinado automaticamente a partir do formulário dos dados fornecidos.

Valores de localização de três dígitos (&quot;DDD&quot;, em que cada &quot;D&quot; representa um dígito decimal de 0 a 9) são tratados como um código de área telefônica dos Estados Unidos.

Valores de localização de cinco ou cinco traço e quatro dígitos (&quot;DDDDD&quot; ou &quot;DDDDD-DDDD&quot;) são tratados como um CEP postal dos Estados Unidos.

Os valores de localização na forma exata de &quot;±DD.DDDD±DDD.DDDD&quot; são tratados como um par de latitude/longitude. O primeiro valor numérico assinado especifica a latitude e o segundo valor numérico assinado representa a longitude.

**Importante**: Se você especificar um valor de latitude positivo, um valor de longitude positivo ou ambos, o caractere &quot;+&quot; no URL deverá ser codificado como  `%2b`. Caso contrário, &quot;+&quot; é interpretado como um espaço e o valor não é reconhecido como um local válido. Por exemplo, suponha que você tenha um valor de latitude de +49,2394 e um valor de longitude de -123,1892. A parte do local do URL, com &quot;+&quot; codificado, seria semelhante ao seguinte:

```
...&sp_q_location_1=%2b49.2394-123.1892...
```

* Valores de latitude positivos representam graus a norte do equador.
* Valores de latitude negativa representam graus a sul do equador.
* Os valores positivos de longitude representam graus a leste de Prime Meridiano.
* Valores negativos de longitude representam graus a oeste de Prime Meridiano.

Por exemplo, o valor &quot;+48.8577+002.2950&quot; representa 48.8577 graus a norte do equador, 2.295 graus a leste do Prime Meridiano, a localização exata da Torre Eiffel em Paris, França. Os sinais numéricos e cada dígito são necessários, mesmo os zeros à esquerda e à direita. Por exemplo, os três valores &quot;48.8577+2.2950&quot;, &quot;+48.8577+2.2950&quot; e &quot;+48.8577+02.295&quot; não são locais. O primeiro valor está sem o sinal de entrelinha na latitude. O segundo valor não possui os dois zeros à esquerda na longitude. O terceiro valor está sem o zero à direita na longitude. Certifique-se de examinar seu registro de índice cuidadosamente para verificar se há problemas relacionados à localização.

Quando você pesquisa por proximidade, há um &quot;campo de saída de proximidade&quot; especial criado para essa pesquisa. O campo é preenchido com a distância relativa entre o local especificado nos critérios de pesquisa e o local associado a cada resultado de pesquisa. Esse campo especial é nomeado para o campo tipo localização usado nos critérios de pesquisa com &quot;_proximity&quot; adicionado ao final.

No exemplo de pesquisa acima, os resultados são classificados em ordem crescente de &quot;zip_proximity&quot;. Ou seja, a distância entre o CEP especificado (84057) e a localização do campo &quot;CEP&quot; de cada resultado. Você também pode usar esse &quot;campo de saída de proximidade&quot; especial para exibir a distância relativa para cada resultado de pesquisa, em quilômetros ou milhas, usando a tag do modelo de pesquisa `<Search-Display-Field>`.

Consulte [Pesquisar marcas de modelo](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Também é possível pesquisar sem a opção sp_s. Nesse caso, os resultados são classificados por pontuação (sp_s=0, que é o padrão). A pontuação é influenciada pela distância relativa de cada resultado do local de pesquisa de proximidade especificado por meio do parâmetro sp_q_location[_#]. Um novo parâmetro cgi sp_q_max_relevant_distance[#] é adicionado para, opcionalmente, controlar o cálculo de relevância aplicado às pesquisas de proximidade.

Este é um exemplo de pesquisa de proximidade:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_q_2=shirt&sp_x_2=title&sp_q_max_relevant_distance_2=50
```

O conjunto de resultados contém quaisquer documentos localizados a 100 milhas do CEP 84057 e contém a palavra &quot;camisa&quot; no campo de título, ordenado por pontuação que é influenciada pela pontuação de relevância de proximidade. Uma pontuação de relevância perfeita para o componente de proximidade representaria uma distância de 0. Uma pontuação de relevância mínima para o componente de proximidade representaria uma distância pouco acima de 50 milhas.

Você pode obter mais informações sobre a pesquisa de proximidade analisando `sp_location`, `sp_location_#`, `sp_q_min`, `sp_q_min_#`, `sp_q_max`, `sp_q_max_#` e `sp_s` no tópico de referência Pesquisar parâmetros CGI.

Consulte [Pesquisar parâmetros CGI](../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890).

Consulte [Adicionar um novo campo de tag meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
