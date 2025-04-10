---
title: Spåra din kreditförbrukningsaktivitet
description: Lär dig hur du spårar din organisations kreditförbrukningsaktivitet i Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 1e8c2fdb3294111562f206ac141cfa39d5193c6c
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Spåra din kreditförbrukningsaktivitet

{{limited-availability-release-note}}

Använd fliken **[!UICONTROL My Activity]** för att övervaka och spåra din organisations beräknade kreditförbrukning för alla samarbetsaktiviteter. Den här funktionen ger detaljerad information om hur krediter används i olika sammanhang och aktiviteter, vilket hjälper dig att hantera dina resurser effektivt.

>[!IMPORTANT]
>
>Kreditförbrukningstabellen avrundas uppåt och aggregeras per dag för övervakning. Siffrorna på kontrollpanelen **[!UICONTROL My Activity]** representerar en *uppskattad* kreditförbrukning. Den *faktiska*-kreditförbrukningen som används för fakturering spåras i interna system och är tillgänglig för dig på begäran. Kontakta din Adobe-representant för att få dessa uppgifter.

Om du vill komma åt din beräknade kreditförbrukningsaktivitet går du till **[!UICONTROL Setup]** i huvudnavigeringen och väljer sedan fliken **[!UICONTROL My activity]**.

![Min aktivitetspanel visar information om kreditförbrukning](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>Vyn **[!UICONTROL My activity]** innehåller ingen information om användaråtgärder i olika delar av Collaboration CDP-användargränssnittet i realtid. Använd funktionen [granskningsloggar](/help/guide/setup/audit-logs.md) för att hämta den informationen.

## Förstå din aktivitetspanel

På aktivitetspanelen visas en omfattande lista med alla kreditförbrukande åtgärder inom organisationen. Varje rad representerar en distinkt aktivitet och ger viktig information om kreditanvändningen:

>[!NOTE]
>
>**[!UICONTROL Audience Management]** aktiviteter är inte associerade med någon annan medarbetare, så kolumnerna **[!UICONTROL Connection ID]** och **[!UICONTROL Connection name]** för de här aktivitetstyperna anger ett **[!UICONTROL N/A]**-värde.

| Kolumn | Beskrivning |
|--------|-------------|
| **[!UICONTROL Date]** | Det datum då aktiviteten inträffade, vilket visas i formatet MM/DD/ÅÅÅÅ. |
| **[!UICONTROL Connection ID]** | En unik identifierare för varje anslutning som är associerad med en kreditförbrukande aktivitet, som representeras av en alfanumerisk sträng. |
| **[!UICONTROL Connection name]** | Namnet på den medarbetare som är associerad med anslutningen och den kreditförbrukande aktiviteten. |
| **[!UICONTROL Activity]** | Den typ av aktivitet som har utförts, till exempel **Aktivering - delning**, **Aktivering - utlänning** eller **målgruppshantering**. |
| **[!UICONTROL Total credits used]** | Det totala antalet krediter som används av aktiviteten. |
| **[!UICONTROL My credit share]** | Organisationens andel av de krediter som används för aktiviteten. |

{style="table-layout:auto"}

## Typ av verksamhet {#types-of-activities}

Kolumnen **[!UICONTROL Activity]** visar olika typer av kreditförbrukande åtgärder.

* **[!UICONTROL Audience Management]**: Medarbetare förbrukas när målgrupper importeras till Real-Time CDP Collaboration. Krediter förbrukas som en funktion av antalet ID (i miljoner) som indexerats inom Real-Time CDP Collaboration för alla målgrupper och frekvensen för indexeringen (varje dag, var tredje dag eller varje vecka) under faktureringsperioden. Läs mer om [att importera och hantera målgrupper](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Activation - Sharing]** - Krediter förbrukas som en funktion av antalet ID:n som aktiveras från Real-Time CDP Collaboration under faktureringsperioden. Läs mer om att [dela](/help/guide/collaborate/share.md) och [aktivera målgrupper](/help/guide/collaborate/activate.md) i Real-Time CDP Collaboration.
* **[!UICONTROL Activation - Egress]** - Krediter förbrukas som en funktion av antalet ID:n som aktiveras från Real-Time CDP Collaboration under faktureringsperioden. Läs mer om att [dela](/help/guide/collaborate/share.md) och [aktivera målgrupper](/help/guide/collaborate/activate.md) i Real-Time CDP Collaboration.


<!--

**[!UICONTROL Audience Overlaps]** – Credits are consumed as a function of the number of matched IDs across 2 or more shared audiences throughout the billing period. Read more about [audience overlaps in the discover tab](/help/guide/collaborate/discover.md).

Collaboration Measurement – Credits are consumed as a function of the number of rows existing in campaign reports across all campaigns, and the frequency of that reporting (daily, every three days, or weekly).

-->


## Hantera din kreditförbrukning {#manage-credit-consumption}

Så här hanterar du din kreditförbrukning effektivt:

1. **Förstå** kreditförbrukningen som är associerad med varje aktivitet. Se [Real-Time CDP Collaboration produktbeskrivning](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} för en tabell över samarbetskrediter som används per aktivitet.
2. **Övervaka regelbundet**: Kontrollera din aktivitetspanel ofta för att få information om användningsmönster.
3. **Spåra via anslutning**: Använd anslutningsnamnet för att identifiera vilka partnerskap som förbrukar flest krediter.

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->
