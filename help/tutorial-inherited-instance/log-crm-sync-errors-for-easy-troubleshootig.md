---
title: Registrar erros de sincronização do CRM para facilitar a solução de problemas
description: Saiba como usar um log de erros de sincronização do CRM para investigar problemas de sincronização do CRM e mantê-lo em execução sem problemas.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00.000Z
jira: KT-13875
thumbnail: KT-13875.jpeg
index: true
exl-id: 3b7e6127-28fd-4dce-915d-5af9bcce984b
TQID: https://experienceleague.adobe.com/JM26ZReC9P8rKS8IqjIV5TKLxT0xInUHysdM7zo0LzM
product_v2: id: b27e5950-9033-45ac-9f86-eb22e567f615
feature_v2: id: d1d0a9cd-295d-4976-8c39-ddae266f240e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0f8ea3988fd586ccbd4b414b3558f6e5f36882bf
workflow-type: tm+mt
source-wordcount: 470
ht-degree: 0%

---

# Registrar erros de sincronização do CRM para facilitar a solução de problemas

Como administrador do Marketo Engage, verificar se sua instância está sincronizada com o CRM deve ser uma parte essencial da sua [rotina diária](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. Embora a [seção Notificações](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} (encontre-a no canto superior direito da interface do Marketo Engage) seja o local em que você começará a encontrar e investigar problemas frequentes de sincronização, há uma dica profissional que pode ajudá-lo a gerenciar a integridade da instância de maneira organizada. Adobe Marketo Champion (2019-2022), Amy Goldfine recomenda que os usuários administradores mantenham um log dos erros de sincronização do CRM para facilitar a solução de problemas.

![Captura de tela da guia Erros de sincronização](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Por que manter um registro de Erros de Sincronização do CRM?

Ao registrar os erros de sincronização do CRM, os administradores do Marketo Engage podem revisar os problemas e as tendências com os administradores do CRM para corrigir a causa raiz. Siga as etapas abaixo para documentar seus problemas de Sincronização do CRM para sua instância.

## Como manter um log de erros de sincronização do CRM

Antes de começar, baixe o [modelo de Log de Erros de Sincronização do CRM](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Etapa 1:** Vá para a seção *[!UICONTROL Admin]* no Marketo Engage. Em *[!UICONTROL Integração]*, clique em *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* ou *[!DNL Veeva]*, dependendo do [!DNL CRM] usado, em seguida, na guia *[!UICONTROL Erros de Sincronização]*.

**Etapa 2:** Você pode optar por [exportar os registros de erros como um  [!DNL CSV] arquivo por meio do painel [!UICONTROL Filtro]](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}. Se você tiver poucas horas, copie e cole diretamente da guia *[!UICONTROL Erros de sincronização]*.

**Etapa 3:** Observe a data em que o erro ocorreu.

**Etapa 4:** Insira o número de registros de pessoas afetados por esse erro. (Às vezes, o CRM só emitirá um erro para uma pessoa. Às vezes, haverá muitas pessoas com o mesmo erro ao mesmo tempo.)

**Etapa 5:** Anote o endereço de email de uma pessoa afetada pelo erro. Isso facilita a referência e a discussão dos erros com o administrador do CRM.

**Etapa 6:** Colar links para o registro de pessoa em [!DNL Marketo Engage] e no [!UICONTROL Registro de Cliente Potencial/Contato do CRM] dessa pessoa.

**Etapa 7:** na última coluna, cole o texto real do erro.

## O que está por vir?

**Identificar Códigos de Erro:** Para entender os códigos de erro, procure as descrições na [tabela Códigos de Erro de Nível de Resposta](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} da documentação de desenvolvedores e localize as próximas etapas típicas para resolver os erros.

## Autores

**Amy Goldfine**\
Adobe Marketo Champion(2019-2022)
*Fundador, MarketingOpsAdvice.com*

![Amy Goldfine](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Gerenciador de marketing de adoção e retenção na Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
