---
title: Desenvolver um guia de governança de instância com a documentação
description: Saiba como estabelecer um procedimento robusto para criar e manter a documentação e o changelog para sua instância Marketo Engage. Isso não só economizará tempo para o compartilhamento de conhecimento da sua equipe, como também melhorará a integridade e a eficiência da sua instância.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: false
exl-id: 4313b54a-1848-4684-b037-7a7795dd01ec
source-git-commit: 681d390ce5ab336a7e24cc63256659a492288517
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---

# Desenvolver um guia de governança de instância com a documentação

À medida que você entra em uma instância herdada do [!DNL Marketo Engage], ela geralmente aparece com o desafio de não ter uma documentação funcional e técnica atualizada. Como administrador, estabelecer diretrizes para garantir o controle adequado da instância é uma responsabilidade principal que não pode ser ignorada. É uma das estratégias críticas para [aumentar a eficiência ao trabalhar em uma instância de Marketo Engage estabelecida](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Este tutorial passo a passo com origem no [!DNL Adobe Marketo Champion] (2018), Nick Hajdin, guiará você por esse processo para destacar a configuração da sua instância, documentar seus principais programas operacionais e manter um [!DNL changelog] para aplicar uma política de governança rigorosa.

## Por que desenvolver um guia e uma documentação de governança de instância para sua instância herdada?

A documentação detalhada e um [!DNL changelog] são vitais para o gerenciamento eficiente e a transferência de conhecimento na sua instância [!DNL Marketo Engage]. Acompanhar as alterações e decisões tomadas durante a configuração da instância pode ajudar a:

1. Treine usuários internos com mais facilidade e de maneira escalável.
2. Crie com mais eficiência em [!DNL Marketo Engage] a longo prazo.
3. Mantenha a integridade e a higiene de sua instância avançando para evitar que você passe horas pesquisando emails, [trilha de auditoria](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html?lang=pt-BR) e [log de atividades](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html?lang=pt-BR) para obter contexto.
4. Economize tempo ao transferir o conhecimento sobre o [!DNL Marketo Engage] para um novo administrador do [!DNL Marketo Engage] se a equipe passar por algum volume de negócios.

## Guia de governança 101 do [!DNL Marketo Engage]

Um guia de governança serve como a fonte da verdade dos requisitos de configuração da instância e do design do sistema. As principais informações recomendadas para inclusão neste documento são:

* Estruturas de programa/pasta
* Permissão de usuário e função
* Limites de comunicação
* Padrões de governança
* Treinamento interno do usuário antes de conceder a ele acesso à plataforma

## Como desenvolver e manter um guia de governança para sua instância [!DNL Marketo Engage]

### Etapa 1: identificar o estado atual do guia de governança e da documentação

* **Não consigo localizar nenhuma documentação para minha instância herdada:** Se você iniciou recentemente uma nova função e não pode localizar nenhuma documentação para sua instância herdada, **vá para a etapa 2** e comece a usar um modelo para download fornecido.
* **Tenho documentação em arquivo:** Parabéns, este é um bom sinal! Revise sua relevância para ver quando a última alteração está sendo feita. Se os membros da sua equipe não estiverem fazendo a manutenção ativa, é recomendável atualizá-los e informar seus usuários internos sobre como mantê-los atualizados.

### Etapa 2: Identifique os elementos a serem incluídos em sua Documentação do [!DNL Marketo Engage] e [!DNL Changelogs]

O formato varia de uma plataforma baseada em nuvem para um documento compartilhado. Você pode projetar o formato que atenda às necessidades da sua organização. [Esta é uma documentação simples e um modelo do changelog excel](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) que aborda os elementos importantes com os quais você pode começar a trabalhar. Isso inclui:

* Documentação
   * Nome do modelo de programa
   * Canal
   * Data de criação
   * Criado por
   * Finalidade do programa
   * Status
   * Vincular ao modelo do programa
   * Observação
* Changelog
   * Nome do modelo de programa
   * Data da alteração
   * Atualizado por
   * Finalidade da atualização
   * Experiência antes da alteração (incluir links/capturas de tela)
   * Experiência após a alteração (incluir links/capturas de tela)
   * URL para o programa

### Etapa 3: identificar e documentar o estado atual dos programas operacionais principais

Comece identificando os principais programas operacionais com impactos no nível da assinatura. Os exemplos incluem Campanhas de gerenciamento de dados, ciclo de vida do lead, pontuação do lead, sincronização [!DNL CRM] e capacidade de entrega.

Para cada programa operacional identificado, documentar o seu estado atual. Isso inclui detalhes sobre a finalidade do programa, a configuração, as campanhas inteligentes associadas e a integração com outras ferramentas (se aplicável).

### Etapa 4: Impor Manutenção de [!DNL Changelog]

A próxima etapa é estabelecer uma política de governança rigorosa para sua instância [!DNL Marketo Engage] que exija a manutenção de &quot;[!DNL Changelog]&quot;. Essa política garante que todas as atualizações feitas nos programas operacionais em toda a instância sejam documentadas detalhadamente.

Informe sua equipe sobre a importância desses documentos e como acessá-los e atualizá-los corretamente. Pode ser útil atribuir responsabilidades para manter o log de alterações, de modo que alguns membros ou administradores designados da equipe de Operação de marketing estejam constantemente registrando alterações e fornecendo aprovações.

### Etapa 5: Centralizar a documentação

Estabeleça um local central ou repositório para armazenar toda a documentação relacionada à sua instância do [!DNL Marketo Engage]. Pode ser uma unidade compartilhada, uma pasta dedicada ou um sistema baseado em nuvem.

### Etapa 6: revisar e atualizar regularmente

Programe revisões regulares de sua documentação para garantir que ela permaneça precisa e atualizada. Pode ser facilmente ignorado durante os horários de maior movimento. Configure lembretes proativamente no seu calendário para garantir que sua equipe faça atualizações regularmente para refletir quaisquer alterações ou otimizações em seus programas operacionais.

## O que está por vir?

Comece baixando este [modelo simples](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Siga as etapas acima para desenvolver seu guia de governança e documentação. Ao trabalhar durante o processo, lembre-se das seguintes regras básicas:

**Atualize sua documentação existente:**
É crucial manter sua documentação atualizada. Se não tiver sido modificado nos últimos 3 anos, confirme tempo para revisar sua documentação enquanto audita sua instância.

**Compartilhar e treinar:**
Compartilhe sua documentação e o [!DNL changelog] com membros relevantes da equipe e informe-os sobre como atualizar esses registros.

**Revisão Periódica:** agendou o horário para revisão e manutenção durante todo o ano para incluir novas alterações, otimizações ou ajustes à medida que ocorrerem.

Manter uma documentação abrangente e atualizada para sua instância do Marketo Engage economizará tempo e esforço a longo prazo e facilitará o gerenciamento eficaz da instância.

### Autores

**Nick Hajdin**
[!DNL Adobe Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![Nick Hajdin](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Gerenciador de marketing de adoção e retenção, Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
