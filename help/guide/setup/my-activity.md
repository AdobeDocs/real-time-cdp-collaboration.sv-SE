---
title: Spåra din kreditförbrukningsaktivitet
description: Lär dig hur du spårar din organisations kreditförbrukningsaktivitet i Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 4fc9b4e814f7392e1dfdb5847b7189d7d6e21702
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Spåra din kreditförbrukningsaktivitet {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="Läs mer"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**90-dagars period utan övertäckning**: Kunder i berättigade regioner omfattas av en 90-dagars period utan övertäckning som börjar från det datum då de finns tillgängliga i respektive region. Under denna tid tar kunderna inte ut någon extra avgift för att de överskridit sin rätt till krediter.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Kreditförbrukningstabellen avrundas uppåt och aggregeras per dag för övervakning. Siffrorna på kontrollpanelen **[!UICONTROL My Activity]** representerar en *uppskattad* kreditförbrukning. Den *faktiska*-kreditförbrukningen som används för fakturering spåras i interna system och är tillgänglig för dig på begäran. Kontakta din Adobe-representant för att få dessa uppgifter.

Om du vill komma åt din beräknade kreditförbrukningsaktivitet går du till **[!UICONTROL Setup]** i huvudnavigeringen och väljer sedan fliken **[!UICONTROL My activity]**.

![Min aktivitetspanel visar information om kreditförbrukning](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>Vyn **[!UICONTROL My activity]** innehåller ingen information om användaråtgärder i olika delar av Collaboration användargränssnitt. Använd funktionen [granskningsloggar](/help/guide/setup/audit-logs.md) för att hämta den informationen.

## Förstå din aktivitetspanel {#understand-dashboard}

På aktivitetspanelen visas en omfattande lista med alla kreditförbrukande åtgärder på ditt konto. Varje rad representerar en distinkt aktivitet och ger viktig information om kreditanvändningen:

>[!NOTE]
>
>**[!UICONTROL Audience Management]** aktiviteter är inte associerade med någon annan medarbetare, så kolumnerna **[!UICONTROL Connection ID]** och **[!UICONTROL Connection name]** för de här aktivitetstyperna anger ett **[!UICONTROL -]**-värde.

| Kolumn | Beskrivning |
|------------|--------------|
| **[!UICONTROL Date]** | Det datum då aktiviteten inträffade, vilket visas i formatet MM/DD/ÅÅÅÅ. |
| **[!UICONTROL Connection ID]** | En unik identifierare för varje anslutning som är associerad med en kreditförbrukande aktivitet, som representeras av en alfanumerisk sträng. |
| **[!UICONTROL Connection name]** | Namnet på den medarbetare som är associerad med anslutningen och den kreditförbrukande aktiviteten. |
| **[!UICONTROL Activity]** | Den typ av aktivitet som har utförts, till exempel **Aktivering - matchning**, **Aktivering - Klänning** eller **Målgruppshantering**. |
| **[!UICONTROL Inputs processed]** | Det totala antalet indata (till exempel ID:n eller rader) som bearbetats för aktiviteten. |
| **[!UICONTROL Total credits used]** | Det totala antalet krediter som används av aktiviteten. |
| **[!UICONTROL My credit share]** | Kontots andel av krediterna som används för aktiviteten. |

{style="table-layout:auto"}

## Typ av verksamhet {#types-of-activities}

Kolumnen **[!UICONTROL Activity]** visar olika typer av kreditförbrukande åtgärder.

* **[!UICONTROL Audience Management]**: Medarbetare förbrukas när målgrupper hämtas till Collaboration. Krediter förbrukas som en funktion av antalet ID (i miljoner) som indexerats inom Collaboration för alla målgrupper och frekvensen för indexeringen (varje dag, var tredje dag eller varje vecka). Läs handboken [Källa och hantera målgrupper](/help/guide/setup/onboard-audiences.md) om du vill veta mer.
* **[!UICONTROL Activation - Matching]** - Medarbetare förbrukas som en funktion av antalet ID som matchas och förbereds för aktivering. Läs handboken [Aktivera målgrupper](/help/guide/collaborate/activate.md) om du vill veta mer.
* **[!UICONTROL Activation - Egress]** - Medarbetare förbrukas som en funktion av antalet ID:n som skickas till ett mål. Detta debiteras alltid den medarbetare som tar emot publiken. Läs handboken [Aktivera målgrupper](/help/guide/collaborate/activate.md) om du vill veta mer.
* **[!UICONTROL Measurement]** - Kör aktiviteter i Collaboration för att generera rapporter och insikter om kampanjresultat. Krediter förbrukas baserat på antalet rader i kampanjrapporter för alla kampanjer och rapporteringsfrekvensen (varje dag, var tredje dag eller varje vecka).

## Hantera din kreditförbrukning {#manage-credit-consumption}

Så här hanterar du din kreditförbrukning effektivt:

1. **Förstå** kreditförbrukningen som är kopplad till varje aktivitet. Se [Collaboration produktbeskrivning](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} för en tabell över krediter som används per aktivitet.
2. **Övervaka regelbundet**: Kontrollera din aktivitetspanel ofta för att få information om användningsmönster.
3. **Spåra via anslutning**: Använd anslutningsnamnet för att identifiera vilka anslutningar som förbrukar flest krediter.
