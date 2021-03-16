---
description: É possível definir os formatos de data usados ao analisar e indexar qualquer campo com um tipo de dados de "data".
solution: Target
title: Formatos de data
topic: Apêndices,Pesquisa e comercialização do site
uuid: 148914b5-33ef-41db-8404-67c03f6f0832
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 3%

---


# Formatos de data{#date-formats}

É possível definir os formatos de data usados ao analisar e indexar qualquer campo com um tipo de dados de &quot;data&quot;.

O formato da data e hora é especificado com uma string de formato. A string de formato consiste em zero ou mais especificações de conversão (uma especificação de conversão consiste em um sinal de porcentagem e um outro caractere) e caracteres comuns. Uma lista padrão é fornecida de sequências de formato de data para cada campo de data.

Você tem controle total sobre essa lista e pode adicioná-la ou modificá-la de acordo com as necessidades de seu site. A string de formato superior tem prioridade e as strings de formato subsequentes só serão usadas se a análise do conteúdo de determinada tag de metadados causar um erro.

Por exemplo, suponha que você tenha especificado os seguintes formatos de data:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> <p>%b %d, %Y %T %Z </p> <p>%A %B %d, %Y %T %Z </p> <p>%A %b %d, %Y %T %Z </p> <p>%a %B %d, %Y %T %Z </p> <p>%a %b %d, %Y %T %Z </p> <p>%d %b %Y %T %Z </p> </td> 
  </tr> 
 </tbody> 
</table>

O primeiro formato, &quot;%B %d, %Y %T %Z&quot;, corresponde a datas como as seguintes &quot;20 de setembro de 2014 13:12:00 PDT&quot;. Se não for possível analisar o conteúdo da tag de metadados com esta cadeia de caracteres de formato, haverá a tentativa do próximo formato disponível &quot;%b %d, %Y %T %Z&quot;. Esse formato corresponde a datas como as seguintes: &quot;20 de setembro de 2014 3:12:00 PDT&quot;. Se o conteúdo da tag de metadados não puder ser analisado com essa string de formato, a pesquisa/comercialização do site será movida para baixo na lista de strings de formato até que encontre uma string de formato que funcione.

A tabela a seguir descreve as cadeias de caracteres de formato de data disponíveis:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Formato dos dados </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%Um </p> </td> 
   <td colname="col2"> <p>Corresponde à representação nacional do nome completo do dia da semana, por exemplo, "Segunda-feira". A representação nacional é determinada a partir da definição "Idioma" da opção "Palavras e Idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> corresponde à representação nacional do nome abreviado do dia da semana, em que a abreviatura corresponde aos três primeiros caracteres, por exemplo "Lua." A representação nacional é determinada a partir da definição "Idioma" da opção "Palavras e Idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> corresponde à representação nacional do nome completo do mês, por exemplo "Junho." A representação nacional é determinada a partir da definição "Idioma" da opção "Palavras e Idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> corresponde à representação nacional do nome abreviado do mês, em que a abreviatura corresponde aos três primeiros caracteres, por exemplo "Jun." A representação nacional é determinada a partir da definição "Idioma" da opção "Palavras e Idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p> é equivalente a "%m/%d/%y", por exemplo "06/06/01" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> corresponde ao dia do mês como um número decimal (01-31) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> corresponde ao dia do mês com um número decimal (1-31); dígitos únicos são precedidos por um em branco </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> corresponde à hora (relógio de 24 horas) como um número decimal (00-23) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> corresponde à representação nacional do nome abreviado do mês, em que a abreviatura corresponde aos três primeiros caracteres, por exemplo "Jun" (igual a %b) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> corresponde à hora (relógio de 12 horas) como um número decimal (01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> corresponde ao dia do ano como um número decimal (001-366) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> corresponde à hora (relógio de 24 horas) como um número decimal (0-23); dígitos únicos são precedidos por um em branco </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> corresponde à hora (relógio de 12 horas) como um número decimal (1-12); dígitos únicos são precedidos por um em branco </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> corresponde ao minuto como um número decimal (00-59) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> corresponde ao mês como um número decimal (01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> corresponde à representação nacional de "ante meridiem" ou "post meridiem", conforme adequado, por exemplo "PM." A representação nacional é determinada a partir da definição "Idioma" da opção "Palavras e Idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p> é equivalente a "%H:%M", por exemplo "13:23" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p> é equivalente a "%I:%M:%S %p", por exemplo "23:23:45" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> corresponde o segundo como um número decimal (00-60) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p> é equivalente a "%H:%M:%S", por exemplo "13:26:47" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> corresponde ao número da semana do ano (domingo como primeiro dia da semana) como um número decimal (00-53) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p> é equivalente a "%e-%b-%Y", por exemplo "6-jun-2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> corresponde ao ano com século como um número decimal, por exemplo "2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> corresponde ao ano sem século como um número decimal (00-99) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> corresponde ao nome do fuso horário </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> matches "%" </p> </td> 
  </tr> 
 </tbody> 
</table>

**Strings de formato padrão**

As strings de formato padrão a seguir são usadas por modelos. Você pode adicionar a essa lista ou editá-la conforme necessário.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sequência de caracteres de formato padrão </p> </th> 
   <th colname="col2" class="entry"> <p>Exemplo resultante </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 de setembro de 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 de setembro de 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> domingo 5 de setembro de 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> domingo 5 de setembro de 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Dia 5 de setembro de 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 de setembro de 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d %b %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 de setembro de 1999 13:12:00 PDT </p> </td> 
  </tr> 
 </tbody> 
</table>

