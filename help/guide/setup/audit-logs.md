---
title: Granskningsloggar
description: Lär dig hur du använder funktionen Granskningsloggar i Real-Time CDP Collaboration för att spåra användaraktiviteter och ändringar.
audience: admin
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: ff22dde9730fab89481338753b1dc4a0adf1d57e
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 1%

---

# Granskningsloggar

{{limited-availability-release-note}}

För att öka insynen i och synligheten för aktiviteter som utförs i systemet kan du granska användaraktivitet för olika tjänster och funktioner i form av granskningsloggar i Adobe Real-Time Customer Data Platform (CDP). Loggarna utgör en verifieringskedja som kan hjälpa till med felsökning i Real-Time CDP Collaboration och hjälpa ditt företag att effektivt följa företagets policyer för datahantering och lagstadgade krav.

I grundläggande bemärkelse anger en granskningslogg *vem* utförde *vad*-åtgärden och *när*. Varje åtgärd som registreras i en logg innehåller metadata som anger åtgärdstyp, datum och tid, e-post-ID för användaren som utförde åtgärden samt ytterligare attribut som är relevanta för åtgärdstypen.

Använd granskningsloggsfunktionen i Real-Time CDP Collaboration för att spåra användaraktiviteter och ändringar på plattformen. Den här funktionen är integrerad med Adobe Experience Platform granskningstjänst och användargränssnittet för den här funktionen finns i Experience Platform.

![Skärm med översikt på hög nivå över granskningsloggsfunktionen](/help/assets/setup/audit-logs/audit-logs-overview.png)

Mer information om granskningsloggar finns i [dokumentationen för Adobe Experience Platform-granskningsloggar](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Åtkomst till granskningsloggar

Du kan komma åt granskningsloggar på två sätt, vilket beskrivs i avsnitten nedan. Båda alternativen visar en lista med granskningsloggar som hämtar olika aktiviteter som utförs i Real-Time CDP Collaboration användargränssnitt

### Få åtkomst till granskningsloggar från Real-Time CDP Collaboration användargränssnitt

1. Gå till fliken **[!UICONTROL My Activity]** i Real-Time CDP Collaboration-gränssnittet.
2. Klicka på länken Experience Platform i gränssnittstexten längst upp på sidan.

![Åtkomst till granskningsloggar från Real-Time CDP Collaboration-gränssnittet](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Få åtkomst till granskningsloggar direkt i Experience Platform användargränssnitt

1. Navigera till användargränssnittet för Adobe Experience Platform och välj avsnittet **[!UICONTROL Audits]** på den vänstra menyn. Kontakta organisationens systemadministratörer för att få den behörighet som krävs om du inte kan visa granskningsloggar.

![Åtkomst till granskningsloggar från Experience Platform-gränssnittet](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Visa och använda granskningsloggar

Så här visar du granskningsloggarna:

1. Navigera till avsnittet **[!UICONTROL Audits]** i Adobe Experience Platform-gränssnittet.
2. Använd filtren för att begränsa loggarna utifrån dina kriterier.
3. Välj en loggpost om du vill visa detaljerad information, inklusive tidsstämpel, begärande-ID, resursinformation och åtgärdsstatus.

![Detaljerad granskningslogg](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Infångade aktiviteter

Granskningsloggar samlar in detaljerad information om användaraktiviteter, inklusive:

* **Användar-ID**: Identifieraren för användaren som utförde åtgärden.
* **Åtgärd**: Den typ av åtgärd som har utförts (t.ex. skapa, uppdatera, ta bort).
* **Resurs**: Resursen som ändrades eller skapades.
* **Tidsstämpel**: Tidpunkten då åtgärden utfördes.

Dessa loggar ger en omfattande spårbarhet för alla aktiviteter i din Real-Time CDP Collaboration-instans, vilket är användbart för datastyrning och regelefterlevnad. Läs mer om att [hantera granskningsloggar i användargränssnittet](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filtrera granskningsloggar

Användargränssnittet för granskningsloggar innehåller flera filter som du kan använda för att söka efter specifika loggar:

* **Kategori**: Refererar till resurstypen (till exempel: samarbetsinstans, anslutning, projekt).
* **Åtgärd**: Den typ av åtgärd som har utförts (till exempel: skapa, ta bort, uppdatera).
* **ID för begäran**: En unik identifierare för begäran.
* **E-postadress för användare**: E-postadressen till användaren som utförde åtgärden.
* **Status**: Åtgärdens status (till exempel: tillåten, nekad).
* **Datumintervall**: Datumintervallet som du vill visa loggar för.

Läs mer om [filtrering av granskningsloggar](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

### Exempel på användning

Granskningsloggar genereras och visas i Experience Platform granskningsgränssnitt när du utför åtgärder i Real-Time CDP Collaboration-gränssnittet, som att hantera målgrupper, utöka anslutningsinbjudningar, skapa projekt och så vidare. Åtgärder för att skapa eller uppdatera delar av ett projekt hämtas till exempel enligt nedan:

![Exempel på granskningsloggar som genereras när delar av ett projekt skapas och uppdateras.](/help/assets/setup/audit-logs/create-project-audits.png)

## Fördelar

Förstå några av fördelarna med att använda granskningsloggar:

* **Datastyrning**: Använd granskningsloggar för att se till att alla aktiviteter inom plattformen spåras och kan spåras.
* **Regelefterlevnad**: Funktionen ger en översikt över användaraktiviteter för att uppfylla lagstadgade krav.
* **Felsökning**: Granskningsloggar hjälper dig att identifiera och lösa problem genom att tillhandahålla detaljerade loggar med användaråtgärder.

## Kategorier och åtgärdsreferens

Tabellen nedan innehåller en referens för alla kategorier och åtgärder för Real-Time CDP Collaboration.

![Tillgängliga kategorier är markerade i Real-Time CDP Collaboration granskningsloggar.](/help/assets/setup/audit-logs/available-categories.png)

| Kategori | Instruktioner | Beskrivning |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Collaboration Instance]** | skapa, uppdatera, ta bort | Hantera organisationskonton, inklusive att skapa, uppdatera och ta bort organisationer. Läs mer om att [konfigurera organisationer](/help/guide/setup/onboard-organization.md). |
| **[!UICONTROL Collaboration Connection Invite]** | skapa, uppdatera, ta bort, godkänna, avvisa | Hantera anslutningsinbjudningar, inklusive att skapa, uppdatera, ta bort, godkänna och avvisa inbjudningar. Läs mer om [anslutningsinbjudningar](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Collaboration Connection]** | skapa, uppdatera, ta bort, godkänna, avvisa, begära godkännande | Hantera samarbetsanslutningar, inklusive att skapa, uppdatera, ta bort, godkänna, avslå och begära godkännande för anslutningar. |
| **[!UICONTROL Collaboration Data Connection]** | skapa, uppdatera, ta bort | Hantera dataanslutningar för samarbete för att importera och hantera målgrupper, inklusive att skapa, uppdatera och ta bort dataanslutningar. Läs mer om [hantering av dataanslutningar](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Collaboration Data Entity]** | skapa, uppdatera, ta bort | Hantera dataentiteter för samarbete, inklusive att skapa, uppdatera och ta bort dataentiteter. Dataenheter i detta sammanhang avser målgrupper. Läs mer om [att importera och hantera målgrupper](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Collaboration Project]** | skapa, uppdatera, ta bort | Hantera projekt i samarbete, inklusive att skapa, uppdatera och ta bort projekt. Läs mer om [att hantera projekt](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Collaboration Module]** | skapa, uppdatera, ta bort | Hantera olika moduler i samarbetsprojekt, inklusive att skapa, uppdatera och ta bort olika moduler i användargränssnittet. Till exempel möjligheten att [dela målgrupper](/help/guide/collaborate/share.md). |

{style="table-layout:auto"}

Genom att utnyttja granskningsloggsfunktionen kan ni föra en tydlig och detaljerad förteckning över alla aktiviteter i er Real-Time CDP Collaboration-instans och säkerställa öppenhet och ansvar.
