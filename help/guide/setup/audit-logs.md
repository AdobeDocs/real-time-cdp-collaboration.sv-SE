---
title: Granskningsloggar
description: Lär dig hur du använder funktionen Granskningsloggar i Real-Time CDP Collaboration för att spåra användaraktiviteter och ändringar.
audience: admin
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 1%

---

# Granskningsloggar

{{limited-availability-release-note}}

För att öka insynen i och synligheten för aktiviteter som utförs i systemet kan du granska användaraktivitet för olika tjänster och funktioner i form av granskningsloggar i Adobe Experience Platform. Loggarna utgör en verifieringskedja som kan hjälpa till med felsökning i Adobe Real-Time CDP Collaboration och hjälpa ditt företag att effektivt följa företagets policyer för datahantering och lagstadgade krav.

I grundläggande bemärkelse anger en granskningslogg *vem* utförde *vad*-åtgärden och *när*. Varje åtgärd som registreras i en logg innehåller metadata som anger åtgärdstyp, datum och tid, e-post-ID för användaren som utförde åtgärden samt ytterligare attribut som är relevanta för åtgärdstypen.

Använd granskningsloggsfunktionen i Collaboration för att spåra användaraktiviteter och ändringar på plattformen. Den här funktionen är integrerad med Experience Platform granskningstjänst och användargränssnittet för den här funktionen finns i Experience Platform.

![Skärm med översikt på hög nivå över granskningsloggsfunktionen.](/help/assets/setup/audit-logs/audit-logs-overview.png)

Mer information om granskningsloggar finns i [Experience Platform granskningsloggsdokumentation](https://experienceleague.adobe.com/sv/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Åtkomst till granskningsloggar

Du kan komma åt granskningsloggar på två sätt, vilket beskrivs i avsnitten nedan. Båda alternativen visar en lista med granskningsloggar som hämtar olika aktiviteter som utförs i Collaboration.

### Få åtkomst till granskningsloggar från Collaboration användargränssnitt

1. Gå till fliken **[!UICONTROL My Activity]** i arbetsytan för **[!UICONTROL Setup]** i Collaboration.
2. Klicka på länken Experience Platform i texten längst upp på sidan.

![Åtkomst till granskningsloggar från fliken Min aktivitet i Collaboration.](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Få åtkomst till granskningsloggar direkt i Experience Platform användargränssnitt

1. Navigera till [Experience Platform](https://platform.adobe.com/) och välj avsnittet **[!UICONTROL Audits]** på den vänstra menyn. Kontakta organisationens systemadministratörer för att få den behörighet som krävs om du inte kan visa granskningsloggar.

![Få åtkomst till granskningsloggar från Experience Platform.](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Visa och använda granskningsloggar

Så här visar du granskningsloggarna:

1. Navigera till avsnittet **[!UICONTROL Audits]** i Experience Platform.
2. Använd [filters](#filter-audit-logs) för att begränsa loggarna utifrån dina kriterier.
3. Välj en loggpost om du vill visa detaljerad information, inklusive tidsstämpel, begärande-ID, resursinformation och åtgärdsstatus.

![Detaljerad granskningslogg](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Infångade aktiviteter

Granskningsloggar samlar in detaljerad information om användaraktiviteter, inklusive:

* **Tidsstämpel**: Exakt datum och tid för åtgärden som utfördes i formatet månad/dag/år/timme:minute AM/PM.
* **Resursnamn**: Namnet på resursen som åtgärden utfördes på.
* **Kategori**: Den typ av resurs som åtgärden utfördes på.
* **Åtgärd**: Den specifika åtgärd som har utförts, till exempel skapa eller ta bort.
* **Användare**: E-postadressen till användaren som utförde åtgärden.

Dessa loggar ger en omfattande spårbarhet för alla aktiviteter i din Collaboration-instans, vilket är användbart för datastyrning och regelefterlevnad. Läs mer om att [hantera granskningsloggar i användargränssnittet](https://experienceleague.adobe.com/sv/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filtrera granskningsloggar {#filter-audit-logs}

Användargränssnittet för granskningsloggar innehåller flera filter som du kan använda för att söka efter specifika loggar:

* **Kategori**: Den typ av resurs som åtgärden utfördes på, till exempel Collaboration Instance eller Collaboration Connection Invite.
* **Åtgärd**: Den typ av åtgärd som utfördes. Vilka åtgärder som är tillgängliga beror på vilken kategori du har valt. Exempel: åtgärder för Collaboration Instance är skapa, uppdatera och ta bort.
* **ID för begäran**: En unik identifierare för begäran.
* **Användare**: E-postadressen till användaren som utförde åtgärden.
* **Status**: Åtgärdens status, till exempel Tillåt eller Neka.
* **Datumintervall**: Datumintervallet som du vill visa loggar för.

Läs mer om [filtrering av granskningsloggar](https://experienceleague.adobe.com/sv/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

## Fördelar

Granskningsloggar har flera fördelar för organisationer som använder Collaboration:

* **Datastyrning**: Använd granskningsloggar för att se till att alla aktiviteter inom plattformen spåras och kan spåras.
* **Regelefterlevnad**: Funktionen ger en översikt över användaraktiviteter för att uppfylla lagstadgade krav.
* **Felsökning**: Granskningsloggar hjälper dig att identifiera och lösa problem genom att tillhandahålla detaljerade loggar med användaråtgärder.

## Kategorier och åtgärdsreferens

Tabellen nedan innehåller en referens för alla kategorier och åtgärder för Real-Time CDP Collaboration.

![Tillgängliga kategorier är markerade i Real-Time CDP Collaboration granskningsloggar.](/help/assets/setup/audit-logs/available-categories.png)

| Kategori | Instruktioner | Beskrivning |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Collaboration Instance]** | skapa, uppdatera, ta bort | Hantera konton, inklusive att skapa, uppdatera och ta bort konton. Mer information finns i guiden [Konfigurera dina konton](/help/guide/setup/onboard-account.md). |
| **[!UICONTROL Collaboration Connection Invite]** | skapa, uppdatera, ta bort, godkänna, avvisa | Hantera anslutningsinbjudningar, inklusive att skapa, uppdatera, ta bort, godkänna och avvisa inbjudningar. Mer information finns i guiden [upprättar anslutningar](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Collaboration Connection]** | skapa, uppdatera, ta bort, godkänna, avvisa, begära godkännande | Hantera anslutningar, inklusive att skapa, uppdatera, ta bort, godkänna, avslå och begära godkännande för anslutningar. |
| **[!UICONTROL Collaboration Data Connection]** | skapa, uppdatera, ta bort | Hantera dataanslutningarna där du hämtar och hanterar målgrupper, inklusive att skapa, uppdatera och ta bort dataanslutningar. Mer information finns i guiden [Hantera dataanslutningar](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Collaboration Data Entity]** | skapa, uppdatera, ta bort | Hantera datatabeller för Collaboration, inklusive att skapa, uppdatera och ta bort datatabeller. Dataenheter i detta sammanhang avser målgrupper. Mer information finns i guiden [Källa och hantera målgrupper](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Collaboration Project]** | skapa, uppdatera, ta bort | Hantera projekt i Collaboration, inklusive att skapa, uppdatera och ta bort projekt. Mer information finns i guiden [Hantera projekt](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Collaboration Module]** | skapa, uppdatera, ta bort | Hantera olika moduler i projekt, inklusive att skapa, uppdatera och ta bort olika moduler i användargränssnittet. Till exempel möjligheten att [aktivera målgrupper](/help/guide/collaborate/activate.md). |

{style="table-layout:auto"}

Genom att utnyttja granskningsloggsfunktionen kan ni föra en tydlig och detaljerad förteckning över alla aktiviteter inom Collaboration, vilket säkerställer öppenhet och ansvar.
