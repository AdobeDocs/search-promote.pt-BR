---
description: As ocorrências diretas permitem redirecionar um cliente para um URL especificado quando o cliente pesquisa por um termo correspondente. Esse tipo de funcionalidade permite melhorar a navegação da pesquisa do site.
solution: Target
title: Sobre ocorrências diretas
topic-legacy: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
exl-id: 251dfa47-f55a-469c-8fca-e187877b7759
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---

# Sobre ocorrências diretas{#about-direct-hits}

As ocorrências diretas permitem redirecionar um cliente para um URL especificado quando o cliente pesquisa por um termo correspondente. Esse tipo de funcionalidade permite melhorar a navegação da pesquisa do site.

## Uso de ocorrências diretas {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

As ocorrências diretas consistem em dois elementos principais: o URL do seu site e um ou mais termos de pesquisa delimitados por vírgulas. As ocorrências diretas são especificadas da seguinte maneira:

```
    website_URL: term
    website_URL: term, term, term
```

Por exemplo, suponha que você tenha um site corporativo com uma página que especifique todos os seus termos e condições. Quando um cliente pesquisa seus termos e condições, em vez de mostrar os resultados, você pode redirecionar o cliente para a página de termos e condições.

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

Se o termo de consulta não corresponder a nenhuma ocorrência direta, os resultados da pesquisa serão retornados da maneira usual.

## Configuração de ocorrências diretas {#task_64DFB8C554874C699FCC0C2F26C3669F}

Você pode especificar termos de pesquisa que redirecionam um navegador da Web para um URI em vez de retornar resultados de pesquisa.

<!-- 

t_configuring_direct_hits.xml

 -->

São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash).

**Para configurar ocorrências diretas**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. No campo [!DNL Direct Hits], insira o URL do site e um ou mais termos de pesquisa delimitados por vírgulas.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Teste de ocorrências diretas {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

Antes de impulsionar regras de ocorrência direta, você pode testar ocorrências diretas inserindo um termo.

<!-- 

t_testing_direct_hits.xml

 -->

Se você testar um termo que não é coberto por uma regra de ocorrência direta, uma mensagem será exibida informando você. Em tal cenário, se a regra de ocorrência direta estivesse ativa no seu site, os resultados da pesquisa seriam retornados como de costume. Se você testar um termo coberto por uma regra de ocorrência direta, uma mensagem será exibida informando que ocorreu um redirecionamento para o URL especificado.

**Para testar ocorrências diretas**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. No campo [!DNL Test Direct Hits], insira um termo de pesquisa e clique em **[!UICONTROL Test]**.
1. (Opcional) Siga um destes procedimentos:

   * Clique em **[!UICONTROL History]** para reverter as alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Exibição das configurações ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio das configurações do estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
