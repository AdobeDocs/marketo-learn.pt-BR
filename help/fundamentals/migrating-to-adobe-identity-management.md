---
title: Migração para o Adobe Identity Management
description: Este tutorial ajudará você a coordenar a migração das assinaturas e usuários do Marketo Engage para o Adobe Admin Console.
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: ht
source-wordcount: '1250'
ht-degree: 100%

---

# Migração para o Adobe Identity Management

A Adobe está aprimorando a forma de gerenciar assinaturas e usuários do Adobe Marketo Engage. Estamos trazendo um aumento de produtividade para sua organização por migrar as assinaturas e usuários do Marketo Engage para o Adobe Admin Console.

Este tutorial ajudará você com a migração para que seja possível começar a gerenciar o Adobe Marketo Engage com outras contas e produtos Adobe de seus usuários em um único local. A migração é necessária e não afetará o fluxo de trabalho de marketing, o conteúdo, as integrações ou os ativos.

## Lista de verificação de pré-migração para admins do Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Para garantir que a organização possa migrar o Adobe Marketo Engage para o Adobe Admin Console, recomendamos seguir a lista de verificação abaixo para gerenciar as alterações futuras.

### &#x200B;1. Identifique o(s) admin(s) do sistema e a equipe de TI e converse sobre as ações necessárias {#identify-your-system-administrators}

* Se não tiver certeza de quem são os(as) admins do sistema na organização, entre em contato com a equipe de contas da Adobe ou com o Suporte da Adobe `marketocares@marketo.com`.

* Confirme o Adobe Admin Console (ou a Adobe Org) para o qual as assinaturas do Marketo Engage serão migradas. Você provavelmente tem um Adobe Admin Console para o [Dynamic Chat](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"}, uma ferramenta nativa de automação de conversas no Marketo Engage. As assinaturas do Marketo Engage devem ser implantadas na mesma organização do Dynamic Chat.

* Trabalhe com a equipe de TI para incluir na lista de permissões todos os domínios da Adobe listados [na parte superior deste artigo](https://experienceleague.adobe.com/pt-br/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}, a fim de evitar a interrupção do acesso ao Marketo Engage após a migração para a identidade da Adobe.

* **Opcional:** [implemente o logon único (SSO)](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"} antes da migração do usuário.

  >[!NOTE]
  >
  >Há diferenças entre o SSO compatível com o Marketo Engage e o SSO do Adobe Admin Console. Sendo assim, pode ser necessário implementar alterações na configuração.

* **Opcional:** personalize a [duração máxima desejada da sessão](https://helpx.adobe.com/br/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} antes da migração para que os usuários do Marketo Engage permaneçam autenticados.

* Saiba o que comunicar a admins do sistema na [seção de e Email de amostra](#announce-the-migration-timeline).

### &#x200B;2. Familiarize-se com as alterações e os impactos da migração para a identidade da Adobe {#familiarize-yourself-with-the-changes}

No vídeo abaixo, a equipe de gerenciamento de produtos do Marketo Engage dá orientações sobre a jornada de migração e o que esperar dela.

>[!VIDEO](https://video.tv.adobe.com/v/3432366/?captions=por_br&t=170/?quality=12&learn=on){transcript=true}

Para obter mais ajuda sobre esse tópico para admins do Marketo Engage, acesse os seguintes artigos de ajuda:

* [Lista de verificação da configuração do usuário](https://experienceleague.adobe.com/pt-br/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Visão geral do Adobe Identity Management](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Noções básicas sobre a assinatura do Marketo e a migração do usuário para o Adobe Admin Console](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migração para a identidade da Adobe com o console de migração](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Saiba como usar o Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html){target="_blank"}

### &#x200B;3. Anuncie o cronograma da migração e a preparação necessária para suas equipes internas {#announce-the-migration-timeline}

* Após agendada, marque a data da migração nos calendários de admins e usuários do Marketo Engage.

   * É possível modificar a data de migração em **Admin** > **Console de migração** > **Pré-migração** para que ela se ajuste melhor ao cronograma interno. Saiba mais sobre o reagendamento e as limitações da [modificação da data de migração](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* **Envie um email para admins do sistema**

Veja abaixo um email de amostra para enviar a admins. Normalmente, o departamento de TI gerencia todas as licenças da Adobe.

+++ Email de amostra a ser enviado a admins do sistema

**Assunto: suporte necessário - Migração de assinaturas do Marketo Engage para o Adobe Admin Console**

Prezado(a) `[IT Administrator/NAME]`,

Nossa assinatura do Marketo Engage em breve será migrada para o sistema de gerenciamento de identidades da Adobe. Uma `[Marketing Operation team]` precisa de sua ajuda para concluir algumas etapas necessárias antes do início da migração do usuário, com o objetivo de minimizar o impacto aos usuários do Marketo Engage.

`1.` Confirme se a organização já gerencia outros produtos da Adobe no Adobe Admin Console e se o Marketo Engage será migrado para o mesmo console.

* As assinaturas do Marketo Engage devem estar na mesma organização que o Dynamic Chat, uma ferramenta nativa de automação de conversas integrada ao Marketo Engage.

* Em caso de dúvidas ou preocupações relacionadas ao Admin Console, entre em contato com o suporte da Adobe pelo email `marketocares@marketo.com` e inclua-nos em CC.

`2.` Fique atento(a) a um email da Adobe com a linha de assunto &quot;Ação necessária para gerenciar o acesso do usuário ao `[Package Tier]` do Adobe Marketo Engage&quot;. Este email foi enviado depois que as licenças do Marketo Engage foram provisionadas no nosso Admin Console. Somente admins do sistema receberão este email. Informe-nos imediatamente quando recebê-lo.

* A Adobe pode solicitar o seu consentimento como admin de sistema do Admin Console para migrar automaticamente os usuários para o console existente da nossa organização. No email com a linha de assunto “Ação necessária para gerenciar o acesso do usuário ao `[Package Tier]` do Adobe Marketo Engage”, clique em “Introdução” para navegar até a página de consentimento.

`3.` Após a migração, não será mais possível acessar o Marketo Engage pelo domínio experience.adobe.com. O acesso se dará pela Adobe Experience Cloud. Inclua na lista de permissões todos os domínios da Adobe listados [na parte superior deste artigo](https://experienceleague.adobe.com/pt-br/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} para evitar a interrupção do acesso ao Marketo Engage.

`4.` **Opcional:** configure o SSO (Logon único) no Adobe Admin Console.

* Daqui em diante, para beneficiar nossos usuários que fazem logon com o SSO em suas identidades da Adobe, auxilie com a configuração de SSO no Adobe Admin Console antes que a migração do usuário ocorra.

`5.` **Opcional:** defina uma [duração máxima de sessão](https://helpx.adobe.com/br/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} maior no Adobe Admin Console.

* Para evitar que os usuários precisem fazer logon com frequência, personalize a duração da sessão nas Configurações avançadas com um tempo maior.

Agradecemos sua cooperação durante essa transição. Avise-me quando concluir essas etapas para que eu possa continuar com a migração.

Atenciosamente,

`[Your Name]`

+++

* **Enviar um email para usuários do Marketo Engage**

Veja abaixo um email de amostra para usuários do Marketo Engage que **não** têm privilégios de admin.

+++ Email de amostra anunciando a migração futura

**Assunto: atualização importante - Migração de assinaturas do Marketo Engage para o Adobe Admin Console**

Prezados usuários do Marketo Engage,

Temos um comunicado importante sobre nossa instância do Marketo Engage e como será feito o logon. A Adobe está transferindo assinaturas e usuários do Marketo Engage para o Adobe Admin Console, para que possamos centralizar toda a administração de produtos em um único local. Isso não afetará fluxos de trabalho de marketing, conteúdo, integrações ou ativos.

**Detalhes principais:**

* **Data da migração**: `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **Horário**: a migração da nossa assinatura começa por volta da meia-noite (horário local). 

* **Impacto**: não haverá perda de acesso ao produto durante a migração do usuário. Se estiver conectado(a) durante a migração da conta, você será desconectado(a) e solicitado(a) a fazer logon novamente em alguns minutos usando a identidade da Adobe, após a migração.

* **Vantagens**: autenticar o Marketo Engage e outros produtos Adobe com uma única identidade da Adobe, seja uma Adobe ID ou uma Adobe Federated ID (SSO).

**O que você precisa fazer:**

`1.` **Preparar-se**: a verificação de email é necessária na migração para uma identidade da Adobe.

i. Você recebeu um email de solicitação de verificação de email com um link (permanece válido por 3 dias). Se o link tiver expirado, você poderá reenviar o email de verificação a partir do Marketo Engage clicando no ícone “Meu perfil” e navegando até **Minha conta** > **Configurações da conta** > **Reenviar verificação**.

ii.  Uma sessão de usuário ativa é necessária para o sucesso da verificação de email. Faça logon na assinatura do Marketo Engage usando primeiro o URL do provedor de identidade (IdP).

`2.` **Integrar**: assim que a conta de usuário for migrada, você receberá um email da Adobe sobre as alterações no método de entrada.

i. Aceite o novo convite clicando em &quot;Aceitar convite&quot; e fazendo logon com a Identidade da Adobe.

ii.  Na página de logon da Adobe, faça logon com uma Adobe ID existente.

iii. Primeiro, faça logon na instância do Marketo Engage para acessar qualquer URL salvo anteriormente no domínio engage-xx.marketo.com ao qual esteja navegando.

`3.` **Contato**: se tiver dúvidas ou precisar de assistência após a migração da conta, ou se a conta não for migrada e você perder acesso ao Marketo Engage, entre em contato com a equipe de migração do Marketo Engage em `[your internal contact email/phone]`.

Agradecemos sua cooperação durante essa transição. Agradecemos sua compreensão e compromisso em manter nossos sistemas seguros.

Atenciosamente,

`[Your Name]`

+++
