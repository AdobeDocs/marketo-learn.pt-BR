---
title: Registrar erros de sincronização do CRM para facilitar a solução de problemas
description: Saiba como usar um log de erros de sincronização do CRM para investigar problemas de sincronização do CRM e mantê-lo em execução sem problemas.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: false
source-git-commit: 4dc6aeed353fdd8bac960603af22b060ae2d7f00
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---


# Registrar erros de sincronização do CRM para facilitar a solução de problemas

Como administrador de Marketo Engage, verificar se sua instância está sincronizada com o CRM deve ser uma parte essencial do [rotina diária](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. While the [Notifications section](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} (encontre-o no canto superior direito da interface do Marketo Engage) é onde você começará a encontrar e investigar problemas frequentes de sincronização. Há uma dica profissional que pode ajudar você a gerenciar a integridade da instância de maneira organizada.  Adobe Marketo Champion(2022), Amy Goldfine recomenda que os usuários administradores mantenham um registro dos erros de sincronização do CRM para facilitar a solução de problemas.

![Captura de tela da guia Erros de sincronização](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Por que manter um registro de Erros de Sincronização do CRM?

Registrando os erros de sincronização do CRM, os administradores de Marketo Engage podem analisar os problemas e as tendências com os administradores de CRM para corrigir a causa raiz. Siga as etapas abaixo para documentar seus problemas de Sincronização do CRM para sua instância.

## Como manter um log de erros de sincronização do CRM

Antes de começar, baixe o [Modelo de log de erros de sincronização do CRM](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Etapa 1:** Vá para a *[!UICONTROL Admin] seção* em Marketo Engage. Em *[!UICONTROL Integração]*, clique em *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* ou *[!DNL Veeva]*, dependendo de qual [!DNL CRM] você usa, depois a variável *[!UICONTROL Erros de sincronização]* guia.

**Etapa 2:** Você pode optar por [exportar os registros de erros como um [!DNL CSV] arquivo por meio da [!UICONTROL Filtro] painel](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}. Se você tiver poucas horas, copie e cole diretamente do *[!UICONTROL Erros de sincronização]* guia seria o caminho a seguir.

**Etapa 3:** Observe a data em que o erro ocorreu.

**Etapa 4:** Informe o número de registros de pessoas afetados por esse erro. (Às vezes, o CRM só emitirá um erro para uma pessoa. Às vezes, haverá muitas pessoas com o mesmo erro ao mesmo tempo.)

**Etapa 5:** Anote o endereço de email de uma pessoa afetada pelo erro. Isso facilita a referência e a discussão dos erros com o administrador do CRM.

**Etapa 6:** Colar links para o registro de pessoa em [!DNL Marketo Engage] e [!UICONTROL Cliente Potencial/Contato do CRM] registro dessa pessoa.

**Etapa 7:** Na última coluna, cole o texto real do erro.

## O que está por vir?

**Identificar códigos de erro:** Para entender os códigos de erro, procure as descrições na documentação dos desenvolvedores [Tabela de Códigos de Erro de Nível de Resposta](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} e encontre as próximas etapas típicas para resolver os erros.

## Autores

**Amy Goldfine**\
Adobe Marketo Champion(2022)
*Gerente sênior, Operações de marketing, Iterável*

![Amy Goldfine](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Gerenciador de marketing de adoção e retenção no Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}

