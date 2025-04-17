---
title: Tutorial - Como acionar uma campanha inteligente no Marketo Engage usando a API REST e tokens
description: Saiba como acionar uma Campanha inteligente no Marketo Engage usando a API REST e personalizar o email usando Meus tokens.
feature: REST API
role: Admin, Developer
level: Experienced
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 1%

---

# Como acionar uma campanha inteligente no Marketo Engage usando a API REST e os tokens

Este tutorial mostra como acionar uma Campanha inteligente no Marketo Engage usando a API REST e personalizar o email usando Meus tokens. Esse caso de uso é ideal para notificações acionadas pelo cliente, como lembretes de webinário, etapas de integração ou acompanhamentos pós-compra.

## Caso de uso {#use-case}

Uma pessoa se registra em um webinário por meio de uma plataforma externa (por exemplo, aplicativo personalizado, Pendo, Eventbrite). Você deseja:

* Acionar um email de lembrete do Marketo Engage
* Personalize-o com:
   * O nome da pessoa
   * Título do webinário
   * Um link de join exclusivo

Isso pode ser feito usando a API REST e Meus tokens.

## Etapa 1: criar a campanha inteligente {#step-one}

1. Vá para **Atividades de marketing** e, na pasta [Programas](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/creating-programs/understanding-programs){target="_blank"}, crie uma nova [Campanha inteligente](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/understanding-smart-campaigns){target="_blank"} chamada `Send Webinar Reminder`.

1. Na guia **Smart List**, [adicione um acionador](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/creating-a-smart-campaign/define-smart-list-for-smart-campaign-trigger){target="_blank"} para permitir que a campanha seja chamada por meio da API:

   * Selecionar **Campanha solicitada** como acionador
   * Definir o **Source** para `Web Service API`

![Configuração do acionador da lista inteligente](assets/trigger-smart-campaign-rest-api-1.png)

## Etapa 2: definir o conteúdo do email {#step-two}

Crie ou edite um [ativo de email](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/assets/emails){target="_blank"} que faça referência à Pessoa e aos [Meus Tokens](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/tokens/managing-my-tokens){target="_blank"}.

>[!NOTE]
>
>Insira os tokens diretamente no conteúdo do email, como mostrado abaixo.

```html
Hi {{lead.First Name:default=Customer}}

You're registered for **{{my.WebinarTitle}}**.

Join here: {{my.JoinLink}}
```

>[!IMPORTANT]
>
>Se você estiver usando um token para inserir dinamicamente uma URL de imagem (por exemplo, `{{my.WebinarImage}}`), envolva o token em uma tag de imagem do HTML:
>
> ```html
> <img src="{{my.WebinarImage}}" alt="Webinar banner" />
> ```
>
>O Marketo Enagage **não** renderizará a imagem, a menos que o token seja colocado dentro de uma marca de imagem válida.

![Editor de email mostrando o uso do token](assets/trigger-smart-campaign-rest-api-2.png)

## Etapa 3: adicionar tokens ao programa {#step-three}

Para transmitir valores dinamicamente por meio da API, os tokens já devem existir no Marketo Engage. Você precisará criá-los na guia **Meus tokens** do seu programa.

1. Vá para a guia **Meus tokens** do seu programa principal.

2. Arraste um **Token de texto** do painel direito para cada valor dinâmico.

* `{{my.WebinarTitle}}` - Token de texto
* `{{my.JoinLink}}` - Token de texto
* `{{my.WebinarImage}}` - Token de texto (será usado como `src` em uma marca `<img>`)

![Guia Meus tokens na campanha](assets/trigger-smart-campaign-rest-api-3.png)

## Etapa 4: definir regras de qualificação de campanha e ativar a campanha {#step-four}

1. Configure as [regras de qualificação](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/using-smart-campaigns/edit-qualification-rules-in-a-smart-campaign){target="_blank"} para controlar a frequência com que uma pessoa pode executar a Campanha Inteligente.

1. Depois de configurado, clique em **Ativar** para habilitar o Smart Campaign para receber solicitações acionadas por API.

![Regra de qualificação do Smart Campaign](assets/trigger-smart-campaign-rest-api-4.png)

## Etapa 5: acionar a campanha por meio da API REST {#step-five}

### Encontrar a ID da campanha {#find-the-campaign-id}

Para acionar uma Campanha Inteligente via API, você precisará da **ID da campanha**:

1. Localize e selecione a Campanha inteligente que deseja acionar.

1. Examine o URL em seu navegador. Será mais ou menos assim: `https://app-XXX.marketo.com/#/classic/SC`**1234**`A1ZN38`.

1. Os 4 dígitos depois de `SC` é a ID da campanha. No exemplo acima, a ID da campanha inteligente é &#39;1234&#39;

Usar o seguinte ponto de extremidade:

```
POST /rest/v1/campaigns/{campaignId}/trigger.json
```

Exemplo:

```
POST /rest/v1/campaigns/1234/trigger.json
```

### Exemplo de corpo da solicitação {#example-request-body}

```json
{
  "input": {
    "leads": [
      {
        "id": 1002200
      }
    ],
    "tokens": [
      {
        "name": "{{my.WebinarTitle}}",
        "value": "Scaling Customer Engagement in 2025"
      },
      {
        "name": "{{my.JoinLink}}",
        "value": "https://webinars.company.com/join/abc123"
      },
      {
        "name": "{{my.WebinarImage}}",
        "value": "https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/events/media_1c6f338a518ada11550084c8ab3a6bbf554ff6eac.jpeg"
      }
    ]
  }
}
```

>[!IMPORTANT]
>
>Substitua `1002200` no exemplo de corpo acima pela ID de pessoa correta da sua instância do Marketo Engage.

## Autorização {#authorization}

Todas as solicitações de API REST do Marketo exigem um token de acesso OAuth 2.0.

Para recuperar o token de acesso, use o seguinte endpoint:

```
GET /identity/oauth/token?grant_type=client_credentials&client_id=XXX&client_secret=YYY
```

Depois de receber seu token de acesso, inclua-o como um _parâmetro de consulta_ em todas as solicitações de API:

```
Authorization: Bearer YOUR_ACCESS_TOKEN
```

## Práticas recomendadas {#best-practices}

* Adicione valores de fallback/padrão aos tokens para testes e controle de qualidade
* Use `{{lead.token}}` para campos de pessoa e `{{my.token}}` para valores dinâmicos com escopo de campanha
* O Marketo Engage suporta até 100 pessoas por solicitação
* As pessoas devem atender aos critérios da Smart List; caso contrário, serão ignoradas silenciosamente

## Resumo {#summary}

Com essa abordagem, você pode personalizar comunicações usando Campanhas inteligentes acionadas de plataformas externas por meio da API. Isso é útil para cenários como confirmações de registro em webinários, emails de integração e notificações transacionais, tudo isso enquanto injeta dados em tempo real usando Meus tokens.
