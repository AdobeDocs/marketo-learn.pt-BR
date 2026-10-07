---
title: Vídeo de como API do Marketo - Como definir o token de acesso em uma variável
description: Saiba como configurar o aplicativo do Postman e como aproveitar variáveis para salvar dados na variável para fins de reutilização.
feature: REST API
role: Admin, Developer
level: Experienced
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00.000Z
jira: KT-15548
exl-id: 4da86ed6-1072-4e0e-a648-16587badaeb3
product_v2:
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: dca84292-69e9-4116-a575-667d31fa060d
    internal-label: APIs
subfeature_v2:
  - id: cf1396d8-ab85-4e93-b35d-d9b573024abf
    internal-label: REST APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 4768ecb20d4d9c70452ae084256928261f3a80eb
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 27%
---
# Ajuda da API - Como definir o token de acesso em uma variável

Saiba como configurar o aplicativo do Postman e salvar dados em variáveis para fins de reutilização. Saiba também como fazer sua primeira chamada à API REST do Marketo Engage para obter o token de acesso.

>[!PREREQUISITES]
>
>Antes de iniciar este vídeo, crie um nome de usuário Somente API com uma função AOI e crie um serviço Launchpad. Siga as etapas nos artigos abaixo:
>
>* [Criar uma função de usuário somente API](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user-role){target="_blank"}
>
>* [Criar um Usuário Somente de API](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user){target="_blank"}
>
>* [Criar um serviço personalizado para usar com a API REST](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}

**Referências usadas neste vídeo:**

* Ponto de extremidade de autenticação do Marketo: `{{{}base_url{}}}/identity/oauth/token?grant_type=client_credentials&client_id={{{}client_id{}}}&client_secret={{{}client_secret{}}}`

* Script JS para coletar access_token do corpo da resposta (locais na guia Scripts: ):

```
var jsonData = pm.response.json();
pm.environment.set("access_token", jsonData.access_token);
```

* [Documentação de desenvolvedores do Marketo Engage](https://experienceleague.adobe.com/pt-br/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
