---
description: As ocorrências diretas permitem redirecionar um cliente para um URL especificado quando o cliente procura um termo correspondente. Esse tipo de funcionalidade permite que você aprimore a navegação da pesquisa de seu site.
seo-description: As ocorrências diretas permitem redirecionar um cliente para um URL especificado quando o cliente procura um termo correspondente. Esse tipo de funcionalidade permite que você aprimore a navegação da pesquisa de seu site.
seo-title: Sobre ocorrências diretas
solution: Target
title: Sobre ocorrências diretas
topic: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 1%

---


# Sobre ocorrências diretas{#about-direct-hits}

As ocorrências diretas permitem redirecionar um cliente para um URL especificado quando o cliente procura um termo correspondente. Esse tipo de funcionalidade permite que você aprimore a navegação da pesquisa de seu site.

## Usando Ocorrências Diretas {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

As ocorrências diretas consistem em dois elementos principais: o URL do seu site e um ou mais termos de pesquisa delimitados por vírgulas. As ocorrências diretas são especificadas da seguinte maneira:

```
    website_URL: term
    website_URL: term, term, term
```

Por exemplo, suponha que você tenha um site corporativo com uma página que especifique todos os seus termos e condições. Quando um cliente procura seus termos e condições, em vez de mostrar os resultados, você pode redirecionar o cliente para a página de termos e condições.

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

Se o termo do query não corresponder a nenhuma ocorrência direta, os resultados da pesquisa serão retornados da maneira usual.

## Configuração de ocorrências diretas {#task_64DFB8C554874C699FCC0C2F26C3669F}

Você pode especificar termos de pesquisa que redirecionam um navegador da Web para um URI em vez de retornar os resultados da pesquisa.

<!-- 

t_configuring_direct_hits.xml

 -->

São permitidas linhas em branco e linhas de comentário que começam com um caractere &#39;#&#39; (hash).

**Configuração de ocorrências diretas**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. No campo [!DNL Direct Hits], insira o URL do seu site e um ou mais termos de pesquisa delimitados por vírgulas.
1. Clique em **[!UICONTROL Save Changes]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Testando ocorrências diretas {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

Antes de colocar as regras de ocorrência direta em funcionamento, você pode testar as ocorrências diretas inserindo um termo.

<!-- 

t_testing_direct_hits.xml

 -->

Se você testar um termo que não está coberto por uma regra de ocorrência direta, uma mensagem será exibida informando você. Em tal cenário, se a regra de ocorrência direta fosse ativada em seu site, os resultados da pesquisa seriam retornados como de costume. Se você testar um termo coberto por uma regra de ocorrência direta, uma mensagem será exibida informando que ocorreu um redirecionamento para o URL especificado.

**Para testar ocorrências diretas**

1. No menu do produto, clique em **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. No campo [!DNL Test Direct Hits], insira um termo de pesquisa e clique em **[!UICONTROL Test]**.
1. (Opcional) Execute um dos procedimentos a seguir:

   * Clique em **[!UICONTROL History]** para reverter quaisquer alterações feitas.

      Consulte [Usando a opção Histórico](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Clique em **[!UICONTROL Live]**.

      Consulte [Ver definições ativas](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Clique em **[!UICONTROL Push Live]**.

      Consulte [Envio de configurações de estágio ao vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

