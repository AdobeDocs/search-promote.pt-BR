---
description: Um atualizador sobre a sintaxe e as regras de construção de expressões regulares.
solution: Target
title: Expressões regulares
topic-legacy: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
exl-id: 6deb9385-9b17-47c2-b6d9-b63f13df8399
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 1%

---

# Expressões regulares{#regular-expressions}

Um atualizador sobre a sintaxe e as regras de construção de expressões regulares.

Consulte também [Configuração de um índice incremental de um site de preparo](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Sintaxe de expressões regulares**

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Texto</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Qualquer caractere único </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [caracteres] </p> </td> 
   <td colname="col3"> <p> Classe de caracteres: Um dos caracteres </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [^caracteres] </p> </td> 
   <td colname="col3"> <p>Classe de caracteres: Nenhum caractere </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> text1|text2 </p> </td> 
   <td colname="col3"> <p> Alternativa: text1 ou text2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Quantificadores</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ? </p> </td> 
   <td colname="col3"> <p> 0 ou 1 do texto anterior </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> * </p> </td> 
   <td colname="col3"> <p> 0 ou N do texto anterior (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> + </p> </td> 
   <td colname="col3"> <p>1 ou N do texto anterior (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Grupos</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> (text) </p> </td> 
   <td colname="col3"> <p> Agrupamento de texto, para definir as bordas de uma alternativa ou para fazer referências retroativas, onde o grupo Nth é usado no RHS de uma RewriteRule com $N) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Âncoras</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ^ </p> </td> 
   <td colname="col3"> <p> Início da âncora da linha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> $ </p> </td> 
   <td colname="col3"> <p> Âncora de fim de linha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Escapar</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>\char </p> </td> 
   <td colname="col3"> <p>Escape o carro em particular. Por exemplo, para especificar os caracteres ".[]()" e assim por diante. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Regras sobre expressões regulares**

* Um caractere comum — não um dos caracteres especiais descritos abaixo — é uma expressão regular de um caractere que corresponde a si mesmo.
* Uma barra invertida (\) seguida por qualquer caractere especial é uma expressão regular de um caractere que corresponde ao próprio caractere especial. Caracteres especiais incluem:

   * `.` (ponto),  `*` (asterisco),  `?` (ponto de interrogação),  `+` (sinal de adição),  `[` (colchete quadrado esquerdo),  `|` (barra vertical) e  `\` (barra invertida) são sempre caracteres especiais, exceto quando aparecem entre colchetes.
   * `^` (sinal de interpolação ou circunflexo) é especial no início de uma expressão regular ou quando segue imediatamente a esquerda de um par de colchetes.
   * `$` (cifrão) é especial no final de uma expressão regular.
   * `.` (ponto) é uma expressão regular de um caractere que corresponde a qualquer caractere, incluindo caracteres suplementares de conjunto de códigos, com exceção da nova linha.
   * Uma string não vazia de caracteres delimitada em `[ ]` (colchetes à esquerda e à direita) é uma expressão regular de um caractere que corresponde a um caractere, incluindo caracteres suplementares do conjunto de códigos, nessa string.

      No entanto, se o primeiro caractere da string for `^` (circunflexo), a expressão regular de um caractere corresponderá a qualquer caractere, incluindo caracteres suplementares de conjunto de códigos, com exceção da nova linha e dos caracteres restantes na string.

      O `^` tem esse significado especial somente se ocorrer primeiro na string. Você pode usar `-` (sinal de menos) para indicar um intervalo de caracteres consecutivos, incluindo caracteres de conjunto de código suplementares. Por exemplo, [0-9] é equivalente a [0123456789].

      Os caracteres que especificam o intervalo devem ser do mesmo conjunto de códigos. Quando os caracteres são de conjuntos de códigos diferentes, um dos caracteres que especificam o intervalo é correspondido. O `-` perde esse significado especial se ocorrer primeiro (após um `^` inicial, se houver) ou o último na string. O `]` (colchete direito) não encerra essa string quando é o primeiro caractere dentro dela, depois de um `^` inicial, se houver. Por exemplo, `[]a-f]` corresponde a `]` (colchete direito) ou a uma das letras ASCII a f inclusive. Os quatro caracteres listados como caracteres especiais acima são posicionados dentro de uma string de caracteres.

**Regras para construir expressões regulares a partir de expressões regulares de um caractere**

Você pode usar as seguintes regras para criar expressões regulares a partir de expressões regulares de um caractere:

* Uma expressão regular de um caractere é uma expressão regular que corresponde ao que a expressão regular de um caractere corresponde.
* Uma expressão regular de um caractere seguida por um `*` (asterisco) é uma expressão regular que corresponde a zero ou mais ocorrências da expressão regular de um caractere, que pode ser um caractere de conjunto de códigos suplementar. Se houver alguma escolha, a string mais longa à esquerda que permitir uma correspondência será escolhida.
* Uma expressão regular de um caractere seguida por um `?` (ponto de interrogação) é uma expressão regular que corresponde a zero ou uma ocorrência da expressão regular de um caractere, que pode ser um caractere de conjunto de códigos suplementar. Se houver alguma escolha, a string mais longa à esquerda que permitir uma correspondência será escolhida.
* Uma expressão regular de um caractere seguida por um `+` (sinal de mais) é uma expressão regular que corresponde a uma ou mais ocorrências da expressão regular de um caractere, que pode ser um caractere de conjunto de códigos suplementar. Se houver alguma escolha, a string mais longa à esquerda que permitir uma correspondência será escolhida.
* Uma expressão regular de um caractere seguida por `{m}`, `{m,}` ou `{m,n}` é uma expressão regular que corresponde a um intervalo de ocorrências da expressão regular de um caractere. Os valores de m e n devem ser inteiros não negativos inferiores a 256; `{m}` corresponde exatamente a m ocorrências; `{m,}` corresponde pelo menos a m ocorrências; `{m,n}` corresponde a qualquer número de ocorrências entre m e n, inclusive. Sempre que uma opção existe, a expressão regular corresponde ao máximo de ocorrências possível.
* A concatenação de expressões regulares é uma expressão regular que corresponde à concatenação das strings correspondidas por cada componente da expressão regular.
* Uma expressão regular delimitada entre as sequências de caracteres ( e ) é uma expressão regular que corresponde a qualquer correspondência de expressão regular não adornada.
* Uma expressão regular seguida por um `|` (barra vertical) seguido por uma expressão regular é uma expressão regular que corresponde à primeira expressão regular (antes da barra vertical) ou à segunda expressão regular (após a barra vertical).

Também é possível restringir uma expressão regular para corresponder apenas a um segmento inicial ou final de uma linha, ou ambos.

* Um `^` (circunflexo) no início de uma expressão regular restringe essa expressão regular para corresponder a um segmento inicial de uma linha.
* Um `$` (cifrão) no final de uma expressão regular inteira restringe essa expressão regular para corresponder a um segmento final de uma linha.
* A construção ^regular expression$ restringe a expressão regular para corresponder a toda a linha.

Há alguns nomes de classe de caracteres predefinidos que podem ser usados no lugar de expressões regulares com colchetes complexos. Por exemplo, um dígito pode ser representado pela expressão regular de um caractere [0-9] ou pela expressão regular de um caractere da classe de caractere [[:dígito:]].

As classes de caracteres predefinidas e seus significados são os seguintes:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Classe de caractere </p> </th> 
   <th colname="col2" class="entry"> <p>Significado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:alnum:]] </p> </td> 
   <td colname="col2"> <p> Um caractere alfabético ou um dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:alpha:]] </p> </td> 
   <td colname="col2"> <p>Um caractere alfabético. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:em branco:]] </p> </td> 
   <td colname="col2"> <p>Um espaço ou uma guia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cntrl:]] </p> </td> 
   <td colname="col2"> <p> Um código de controlo; caractere não imprimível. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:dígito:]] </p> </td> 
   <td colname="col2"> <p>Um dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:gráfico:]] </p> </td> 
   <td colname="col2"> <p> Qualquer caractere de impressão exceto espaço. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:lower:]] </p> </td> 
   <td colname="col2"> <p>Um caractere alfabético em letras minúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:print:]] </p> </td> 
   <td colname="col2"> <p> Qualquer caractere de impressão, incluindo espaço. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:punct:]] </p> </td> 
   <td colname="col2"> <p> Pontuação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:espaço:]] </p> </td> 
   <td colname="col2"> <p> Espaço em branco, como um espaço, uma guia ou um fim de linha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:upper:]] </p> </td> 
   <td colname="col2"> <p> Um caractere alfabético em maiúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:xdígito:]] </p> </td> 
   <td colname="col2"> <p> Um dígito hexadecimal, maiúsculo ou minúsculo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dois nomes de classe de caractere especiais correspondem ao espaço nulo no início e no fim de uma palavra. Em outras palavras, elas não correspondem a um caractere real. Uma palavra é considerada qualquer sequência de caracteres alfabéticos, dígitos ou sublinhados (_).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Classe de caractere </p> </th> 
   <th colname="col2" class="entry"> <p>Significado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:&lt;:]] </p> </td> 
   <td colname="col2"> <p> início de uma palavra </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:&gt;:]] </p> </td> 
   <td colname="col2"> <p>fim de uma palavra </p> </td> 
  </tr> 
 </tbody> 
</table>
