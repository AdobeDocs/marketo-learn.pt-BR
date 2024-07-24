---
title: Migração para o Adobe Identity Management
description: Descrição em breve.
role: User
level: Beginner
hide: true
hidefromtoc: true
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: fe760c2fc53b96d5c176de377730bce2e89dbc74
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# Migração para o Adobe Identity Management

O Adobe está aprimorando a forma como você gerencia assinaturas e usuários do Adobe Marketo Engage. Estamos trazendo aumento de produtividade para você e sua organização ao migrar suas assinaturas de Marketo Engage e usuários para a Adobe Admin Console.

Este tutorial permite navegar pela migração para gerenciar o Adobe Marketo Engage com outras contas e produtos Adobe para seus usuários em um local central. A migração é necessária e não afetará o fluxo de trabalho de marketing, o conteúdo, as integrações ou os ativos.

## Lista de verificação de pré-migração para administradores do Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Para garantir que sua organização possa migrar o Adobe Marketo Engage para o Adobe Admin Console, recomendamos que você siga a lista de verificação abaixo para gerenciar as alterações futuras.

### 1. Identifique o(s) administrador(es) do sistema e discuta as ações que ele(s) pode(m) precisar realizar {#identify-your-system-administrators}

* Se não tiver certeza de quem são os Administradores do sistema na organização, contate a equipe de Conta do Adobe ou entre em contato com o Suporte do Adobe `marketocares@marketo.com`.

* Confirme a Adobe Admin Console (ou Adobe Org) para a qual suas assinaturas de Marketo Engage serão migradas.  as assinaturas de Marketo Engage devem ser implantadas na mesma organização do Dynamic Chat, uma ferramenta nativa de automação de conversação integrada com o Marketo Engage.
  `TBD LINK TO https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete`

* Saiba mais sobre como se comunicar com os Administradores do sistema na [seção Email de exemplo](#announce-the-migration-timeline).

### 2. Familiarize-se com as alterações e os impactos da migração para a Identidade do Adobe {#familiarize-yourself-with-the-changes}

No vídeo abaixo, a equipe de Gerenciamento de produto do Marketo Engage orienta você sobre a jornada de migração e sobre o que esperar.

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?quality=12&learn=on){transcript=true}

Mais ajuda sobre esse tópico para administradores do Marketo Engage podem ser encontradas nos seguintes artigos de ajuda:

* [Lista de verificação de Instalação do Usuário](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Visão geral do Adobe Identity Management](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Noções básicas sobre assinatura do Marketo e migração de usuários para o Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migrando para a Identidade do Adobe com o Console de Migração](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Saiba como usar o Adobe Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html){target="_blank"}

### 3. Anuncie o cronograma de migração e a preparação necessária para suas equipes internas {#announce-the-migration-timeline}

* Marque a data de migração nos calendários dos administradores do Marketo Engage e usuários depois do agendamento.

Você pode modificar a data de migração em **Admin** > **Console de Migração** > **Pré-Migração** para alinhar-se melhor à sua linha do tempo interna. Saiba mais sobre o reagendamento e as limitações do [modificação da data de migração](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* Envie um email para se comunicar com os administradores do sistema.

Veja abaixo um exemplo de email para enviar aos Administradores do sistema. Normalmente, seu departamento de TI gerencia todas as suas licenças de Adobe.

`---------------------------------------------------`

**Assunto: Suporte Necessário — Migração de Assinaturas do Marketo Engage para o Adobe Admin Console**

Prezado(a) `[IT Administrator/NAME]`,

Nossa assinatura do Marketo Engage será migrada em breve para o Sistema Adobe Identity Management. O `[Marketing Operation team]` precisa de sua ajuda para concluir algumas etapas necessárias antes de iniciar a migração do usuário, para minimizar o impacto nos usuários do Marketo Engage.

`1.` Confirme se a organização já gerencia outros produtos Adobe na(s) Adobe Admin Console(s) e se o Marketo Engage será migrado para o mesmo console.

* Observe que as assinaturas de Marketo Engage devem estar na mesma organização que o Dynamic Chat, uma ferramenta nativa de automação de conversação integrada ao Marketo Engage.

* Em caso de dúvidas ou preocupações relacionadas ao Admin Console que terá o Marketo Engage adicionado, entre em contato com a equipe de suporte em `marketocares@marketo.com` e inclua-nos em sua comunicação.

`2.` Fique atento a um email do Adobe com a linha de assunto &quot;Ação necessária para gerenciar o acesso do usuário ao Adobe Marketo Engage `[Package Tier]`&quot;. Este email foi enviado depois que as licenças de Marketo Engage foram provisionadas em nosso Admin Console. Somente administradores do sistema receberão esse email. Por favor, informe-nos imediatamente quando você recebê-lo.

* O Adobe pode solicitar o seu consentimento, que é o administrador do sistema do Admin Console, para migrar automaticamente os usuários para o console existente da sua organização. No email com a linha de assunto &quot;Ação necessária para gerenciar o acesso do usuário ao Adobe Marketo Engage `[Package Tier]`&quot;, clique no botão &quot;Introdução&quot; para navegar até a página de consentimento.

`3.` **Opcional:** Configurando o SSO (Logon Único) na Adobe Admin Console.

* Para beneficiar nossos usuários de fazer logon com SSO em sua identidade Adobe daqui em diante, solicitamos que você auxilie na configuração do SSO no Adobe Admin Console antes que a migração de usuário ocorra.
Agradecemos sua cooperação durante essa transição. Avise-me quando você concluir essas etapas para que eu possa continuar com a migração do usuário com o Marketo Engage.
Atenciosamente,

`[Your Name]`

`---------------------------------------------------`

* Envie um email para usuários do Marketo Engage.

Veja abaixo um exemplo de email que você pode usar para anunciar a migração futura para os usuários do Marketo Engage que não têm privilégios de administrador.

`---------------------------------------------------`

**Assunto: Atualização Importante — Migração de Assinaturas do Marketo Engage para o Adobe Admin Console**

Prezados usuários do Marketo Engage,

Temos um anúncio importante sobre nossa instância do Marketo Engage e como você fará logon. O Adobe está transferindo assinaturas de Marketo Engage e usuários para o Adobe Admin Console para permitir que os clientes centralizem toda a administração de produtos em um único local. Isso não afetará workflows de marketing, conteúdo, integrações ou ativos.

Detalhes da chave:

* Data de migração: [Especifique a data agendada. Encontre isso no Marketo Engage em **Admin** > **Console de migração** > **Pré-migração**]

* Horário: a migração começa por volta da meia-noite, horário local da nossa assinatura.

* Impacto: não haverá perda de acesso ao produto durante a migração do usuário. Se você estiver conectado quando sua conta estiver sendo migrada, será desconectado e solicitado a fazer logon novamente em minutos usando a Identidade do Adobe após a migração.

* Benefícios: autenticar Marketo Engage e outros produtos de Adobe usando uma única identidade de Adobe, seja Adobe ID ou Adobe Federated ID (SSO).

O que você precisa fazer:

`1.` Preparar: a verificação de email é necessária para que você seja migrado para uma Identidade Adobe.

i. Você recebeu um email de solicitação de verificação por email com um link (permanece válido por 3 dias). Se o link tiver expirado, você poderá reenviar o email de verificação em **Admin** > **Minha Conta** > **Configurações da Conta** e clicando em **Reenviar Verificação**.
ii) Uma sessão de usuário ativa é necessária para o sucesso da verificação de email. Faça logon na assinatura do Marketo Engage usando primeiro o URL do provedor de identidade (IdP).

`2.` Integrado: assim que sua conta de usuário for migrada, você receberá um email do Adobe sobre as alterações em seu método de entrada.

i. Aceite o novo convite clicando no botão &quot;Aceitar convite&quot; e entrando usando a Identidade do Adobe.
ii) Na página de logon do Adobe, faça logon com uma Adobe ID existente.

`3.` Contato: Se tiver dúvidas ou precisar de assistência após a migração da sua conta ou se a conta não for migrada e você perder acesso ao Marketo Engage, entre em contato com a equipe de migração do Marketo Engage em `[your internal contact email/phone]`.

Agradecemos sua cooperação durante essa transição. Agradecemos sua compreensão e seu compromisso em manter nossos sistemas seguros.

Melhor,

`[Your Name]`

`---------------------------------------------------`
