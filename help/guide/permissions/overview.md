---
title: Översikt över åtkomstkontroll
description: Lär dig hur du får tillgång till Adobe Real-Time Customer Data Platform (CDP) Collaboration.
audience: admin
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: af48f5ea-8258-42a6-a39e-f4a4ca5b4a69
source-git-commit: 56872a2cd91ae040aba51ed5784c86b055f88756
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 1%

---

# Översikt över åtkomstkontroll

{{limited-availability-release-note}}

>[!IMPORTANT]
>
> Om du är en slutanvändare som vill ha tillgång till Real-Time CDP Collaboration kontaktar du system- eller produktadministratören för att kontrollera om du har tillgång till programmet. Om du inte vet vem systemadministratören är kan du kontakta Adobe.

Åtkomstkontroll för Real-Time Customer Data Platform (CDP) Collaboration tillhandahålls via Admin Console och behörigheter i [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}. I den här guiden får du lära dig hur du ger åtkomst till dig själv eller andra medlemmar i ditt team, beroende på ditt användningssätt.

## Åtkomstkontrollhierarki {#hierarchy}

Du **måste** ha behörighet som system- eller produktadministratör för att konfigurera åtkomstkontroll för Real-Time CDP Collaboration. En systemadministratör har inga begränsningar och etableras under introduktionsprocessen. Samtidigt kan en produktadministratör tillhandahålla administrativa funktioner för alla produkter som de har tilldelats. En produktadministratör måste ges produktåtkomst och administrativ åtkomst av en systemadministratör.

Dessa handböcker beskriver hur du konfigurerar åtkomst för systemadministratörer, produktadministratörer och slutanvändare. Se tabellen nedan för att förstå skillnaden mellan rollerna.

| Roll | Beskrivning |
| --- | --- | 
| Systemadministratör | Superanvändaren för organisationen. De kan utföra alla administrativa uppgifter i Admin Console och har behörighet att delegera administrativa funktioner till andra användare. |
| Produktadministratör | Administrerar de produkter som tilldelats dem och alla tillhörande administrativa funktioner, som att lägga till användare i organisationer, lägga till eller ta bort användare från produktprofiler samt lägga till eller ta bort andra produktadministratörer från en produkt. |
| Slutanvändare | De användare i organisationen som använder produkterna. |

{style="table-layout:auto"}

Mer information om administrativa roller finns på [Adobe Help Center](https://helpx.adobe.com/enterprise/using/admin-roles.html).

>[!TIP]
>
>Användningen av **administratörer** i dessa handböcker avser **både system- och produktadministratörer**.

## Ytterligare produkter {#products}

Innan du kan ge åtkomst till Real-Time CDP Collaboration måste du ha tillgång till flera produkter, beroende på ditt [användningsfall](#use-cases). Handböckerna för åtkomstkontroll kan fungera genom flera användargränssnitt medan du arbetar, och var och en har ett visst syfte i åtkomstkonfigurationsprocessen. Se tabellen nedan för att få en bättre förståelse för vad varje produkt kommer att användas till.

| Produkt | Användningsområden |
| --- | --- |
| [Admin Console](https://adminconsole.adobe.com/) | Administratörer använder detta för att tilldela användare produkt- och/eller administratörsåtkomst. |
| [Behörigheter](https://experience.adobe.com/) | Administratörer använder detta för att tilldela administratörer eller slutanvändarroller. |
| [Experience Platform](https://platform.adobe.com/) | Administratörer och slutanvändare måste ges åtkomst till Experience Platform-produkter för att kunna tilldela dem till roller. |

## Var ska börja? {#use-cases}

Nu när du har en djupare förståelse för vilka användare och administrativa roller, liksom för de olika Experience Cloud-produkterna, kan du börja ge åtkomst till Real-Time CDP Collaboration. Det finns två huvudfaktorer som påverkar de steg du måste ta:

- om du tilldelar administratörs- eller slutanvändaråtkomst
- om användarna redan har tillgång till Experience Platform-produkten

Se tabellen nedan för att se vilka som krävs för att konfigurera behörigheterna och var de ska börja baserat på ditt fall av åtkomstkontroll. **Kom ihåg att följa självstudiekursen till slutet av guiden från din startplats.**

>[!TIP]
>
> En superanvändare refererar till den högsta åtkomstnivån som systemadministratören kan få. En superanvändare kan utföra alla administrativa uppgifter och alla användarfunktioner. En systemadministratör har inte produktfunktionalitet som är färdig och måste ge sig själv lämplig åtkomst, vilket visas i diagrammet nedan.

| Användningsfall | Nödvändig roll | Var ska börja? |
| --- | --- | --- | 
| Superanvändare utan Experience Platform produktåtkomst. | En systemadministratör. | [Konfigurera produktadministratörsåtkomst](./manage-user-access.md#admin-access) |
| Superanvändare för en befintlig Experience Platform-systemadministratör **med** Experience Platform-gränssnittsåtkomst. | En systemadministratör. | [Konfigurera Real-Time CDP Collaboration-åtkomst](./manage-user-access.md#RTCDP-collab-access) |
| Superanvändare för en befintlig Experience Platform-systemadministratör **utan** åtkomst till Experience Platform UI. | En systemadministratör. | [Konfigurera produktadministratörsåtkomst](./manage-user-access.md#admin-access) |
| Administratörsrättigheter och Real-Time CDP Collaboration-åtkomst för en ny produktadministratör. | En systemadministratör. | [Konfigurera produktadministratörsåtkomst](./manage-user-access.md#admin-access) |
| Real-Time CDP Collaboration-åtkomst för en befintlig Experience Platform-produktadministratör **med** Experience Platform-gränssnittsåtkomst. | En system- eller produktadministratör. | [Konfigurera Real-Time CDP Collaboration-åtkomst](./manage-user-access.md#RTCDP-collab-access) |
| Real-Time CDP Collaboration-åtkomst för en befintlig Experience Platform-produktadministratör **utan** åtkomst till Experience Platform UI. | En system- eller produktadministratör. | [Konfigurera användaråtkomst](./manage-user-access.md#user-access) |
| Real-Time CDP Collaboration-åtkomst för en ny slutanvändare. | En system- eller produktadministratör. | [Konfigurera användaråtkomst](./manage-user-access.md#user-access) |
| Real-Time CDP Collaboration-åtkomst för en befintlig användare med Experience Platform-åtkomst. | En system- eller produktadministratör. | [Konfigurera Real-Time CDP Collaboration-åtkomst](./manage-user-access.md#RTCDP-collab-access) |

{style="table-layout:auto"}

## Ytterligare behörigheter

När du har fått tillgång till Real-Time CDP Collaboration kan du behöva ytterligare Experience Platform-behörigheter för att få tillgång till vissa funktioner.

### Målgruppsimport {#audience-importation}

Innan du kan börja dela målgrupper med medarbetare måste du importera målgrupper till Real-Time CDP Collaboration. För närvarande är Experience Platform den enda dataanslutning som stöds för att importera målgrupper. Till att börja med måste de användare som hanterar mottagarnas introduktion tilldelas en roll som innehåller följande **resursbehörigheter för profilhantering**:

| Behörighet | Beskrivning |
| ---- | ---- |
| Visa segment | Låter användaren se listan över tillgängliga målgrupper i en sandlåda. |
| Visa profiler | Låter användaren se de fält som är tillgängliga för mappning till samarbetsfält. |

Nedan visas en exempelroll med behörigheterna ovan tillagda. Mer information om hur du skapar eller tilldelar roller finns i handboken [Hantera roller](./manage-roles.md).

![Resursens arbetsyta i Behörigheter med behörigheterna Visa segment och Visa profiler har lagts till i resursen Profilhantering.](../../assets/permissions/sample-audience-role.png)

>[!NOTE]
>
>Användare kan arbeta med målgrupper inom Real-Time CDP Collaboration efter att de har importerats utan någon av ovanstående behörigheter.

## Nästa steg

När du har bestämt var du ska börja följer du instruktionslänken till ditt användningsfall för att komma igång med att konfigurera åtkomst. Om du vill veta mer om hur du konfigurerar åtkomst till Real-Time CDP Collaboration som administratör utöver dessa användningsfall, se [hanteraren för användaråtkomst](manage-user-access.md) . Om du vill veta mer om roller och deras roll när det gäller att konfigurera åtkomst till olika komponenter i Real-Time CDP Collaboration kan du läsa guiden [hantera roller](manage-roles.md).
