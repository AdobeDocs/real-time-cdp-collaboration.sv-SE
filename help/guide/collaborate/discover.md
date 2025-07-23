---
title: Upptäck överlappningar och jämför målgrupper
description: Upptäck överlappningar mellan era och medarbetarnas målgrupper. Lär dig hur ni hittar de bästa målgrupperna som kan användas i era kampanjer.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---

# Upptäck överlappningar och jämför målgrupper

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Discover]** är bara tillgänglig om **målgruppsidentifiering** har aktiverats [ under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

När du har [skapat ett projekt](/help/guide/collaborate/manage-projects.md) kan du jämföra dina målgrupper med dina medarbetare. Detta hjälper er att identifiera relevanta målgrupper för kampanjer och avgöra vilka som ska skickas till utgivare för aktivering.

>[!IMPORTANT]
>
>Alla [dataskisser](/help/guide/glossary.md#sketches) som inte uppdateras eller uppdateras kommer att tas bort efter 7 dagar. När detta händer kommer siffrorna som visas i de olika överlappande rapporterna på den här sidan att nollställas och målgruppsdelning blir otillgänglig för dessa utgångna målgrupper. Dataskiseringar uppdateras automatiskt för målgrupper med ett [aktivt uppdateringsschema](/help/guide/setup/onboard-audiences.md#schedule).

De matchningsnycklar som används för att identifiera och jämföra målgrupper ställs in [under anslutningsprocessen](/help/guide/connect/establishing-connections.md#connection-settings). Matchningsnycklar används för att beräkna överlappningen mellan era målgrupper och kan aktiveras och inaktiveras. Om du vill redigera matchningsnycklarna väljer du alternativet **[!UICONTROL Edit match keys]**.

![Flikarbetsytan Upptäck, som visar målgruppsinsikter.](/help/assets/collaborate/discover/discover-overview.png)

Dialogrutan **[!UICONTROL Edit match keys]** öppnas, där du kan inaktivera matchningsnycklarna som du inte vill använda. Välj **[!UICONTROL Save]** om du vill spara ändringarna.

![Dialogrutan Redigera matchningsnycklar på arbetsytan Identifiera.](/help/assets/collaborate/discover/edit-match-keys.png)

## Förhandskrav {#prerequisites}

Om du vill börja använda fliken **[!UICONTROL Discover]** i ditt projekt måste du ha:

* [Källade målgrupper](/help/guide/setup/onboard-audiences.md) till ditt konto
* [Ansluten](/help/guide/connect/establishing-connections.md) till en medarbetare med användningsfallet **Målgruppsidentifiering** aktiverat
* [Skapade ett projekt](/help/guide/collaborate/manage-projects.md) mellan dig och en medarbetare

När dessa förutsättningar är uppfyllda kan ni börja utforska och jämföra överlappningar mellan er och medarbetarens målgrupper.

## Jämför målgrupper {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Jämför målgrupper"
>abstract="Upptäck överlappningar mellan er och medarbetarens målgrupper. Du kan justera inställningarna i listruteväljaren för att upptäcka överlappningar mellan en eller flera av dina målgrupper och en eller flera av dina medarbetares målgrupper."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Ditt identitetsantal"
>abstract="Antalet unika ID:n inom den valda målgruppen, baserat på matchningsnycklarna som du och din medarbetare har kommit överens om för projektet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Identitetsantal för medarbetare"
>abstract="Antalet unika ID:n inom medarbetarens målgrupp, baserat på matchningsnycklarna som du och medarbetaren har kommit överens om för projektet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Antal överlappande identiteter"
>abstract="Antalet unika ID:n som finns både i din och medarbetarens målgrupper, baserat på matchningsnycklarna som du och din medarbetare har kommit överens om för projektet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Procentandel överlappande identiteter"
>abstract="Procentandelen överlappande identiteter mellan dig och medarbetarens valda målgrupp."

Använd jämförelseområdet för att få utförlig information om överlappningen mellan er och medarbetarens målgrupper. Om du vill ändra målgruppsvalet använder du listrutesväljaren högst upp i avsnittet **[!UICONTROL Compare audiences]**. Du kan välja en eller alla målgrupper och en eller alla dina medarbetares målgrupper att jämföra med varandra.

![Arbetsytan Identifiera med målgruppsväljaren markerad i avsnittet Jämför målgrupper.](/help/assets/collaborate/discover/compare-audiences-selector.png)

I avsnittet för att jämföra målgrupper kan du se följande mätvärden, som baseras på de matchningsnycklar som du och din medarbetare har kommit överens om för projektet:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Identity count]** (din) | Antalet unika ID:n inom de valda målgrupperna. |
| **[!UICONTROL Identity count]** (din medarbetare) | Antalet unika ID:n inom medarbetarens målgrupp(er). |
| **[!UICONTROL Overlapping identities]** | Antalet unika ID:n som finns både i din och medarbetarens målgrupper. |
| **[!UICONTROL Overlap %]** | Procentandelen profiler som överlappar den valda målgruppen för er och medarbetaren. |
| **[!UICONTROL Identities breakdown by match key]** | Uppdelningen av identiteter för varje matchningsnyckel som valts i projektet, baserat på valda målgrupper för varje medarbetare. |

{style="table-layout:auto"}

>[!NOTE]
>
>Procenttalet för överlappning kanske inte alltid är tillgängligt för alla målgrupper. Hur synlig indikatorn för överlappningsprocenten är beror på inställningen som medarbetaren valde för en målgrupp i [metadatasynlighetsavsnittet](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Relevanta målgrupper {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Relevanta målgrupper"
>abstract="Dessa målgrupper, som baseras på överlappningsprocentsatser, kan passa bra för er kampanj. <br><br> <b>Identitetsantalet</b> är medarbetarens målgruppsstorlek. <br><br> <b>Överlappande identiteter</b> representerar överlappningen mellan den rekommenderade målgruppen och alla dina målgrupper. <br><br> <b>Överlappningen %</b> representerar antalet överlappande identiteter dividerat med storleken på <i>alla</i> dina målgrupper."

Avsnittet **[!UICONTROL Relevant audiences]** på fliken **[!UICONTROL Discover]** innehåller en förvaltad lista över de fem främsta målgrupperna baserat på överlappningsprocenten mellan medarbetarens målgrupp och alla dina målgrupper. Med den här funktionen kan ni snabbt identifiera målgrupper med den högsta överlappningen, så att ni kan inrikta er på kampanjer mer effektivt. Växla mellan de relevanta målgrupperna med hjälp av sidväljarna i det övre högra hörnet av avsnittet.

![Arbetsytan Identifiera med avsnittet Relevanta målgrupper markerat.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>Visningen av dina medarbetares målgrupper beror på inställningen som medarbetaren valde för en målgrupp i avsnittet [metadatasynlighet](/help/guide/setup/onboard-audiences.md#metadata-visibility). Om din medarbetare har angett alla målgrupper som privata visas inga målgrupper i det här avsnittet.

I avsnittet **[!UICONTROL Relevant audiences]** visas följande information för varje rekommenderad målgrupp:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Identity count]** | Namnet på unika ID:n inom målgruppen. |
| **[!UICONTROL Overlapping identities]** | Antalet unika ID:n som överlappar mellan den rekommenderade målgruppen och alla era målgrupper. |
| **[!UICONTROL Overlap %]** | Procentandelen överlappande identiteter mellan den rekommenderade målgruppen och alla era målgrupper. |
| **[!UICONTROL Audience categories]** | De kategorier som din medarbetare har tilldelat publiken. |
| **[!UICONTROL Match keys]** | De matchningsnycklar som medarbetaren valt för målgruppen. |

{style="table-layout:auto"}

## Upptäck överlappningar {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Upptäck överlappningar med enskilda målgrupper"
>abstract="Få insikter om överlappningar mellan era målgrupper och medarbetarnas målgrupper."

Upptäck överlappningar för att få insikter i hur era målgrupper står sig jämfört med era medarbetares målgrupper. Som standard jämförs alla era målgrupper i det här avsnittet med alla era medarbetares målgrupper. Använd sidnumreringskontrollen längst ned i avsnittet för att navigera bland de tillgängliga målgrupperna.

![Arbetsytan Identifiera med avsnittet Identifiera överlappning markerat.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>Visningen av dina medarbetares målgrupper beror på inställningen som medarbetaren valde för en målgrupp i avsnittet [metadatasynlighet](/help/guide/setup/onboard-audiences.md#metadata-visibility). Om din medarbetare har angett alla målgrupper som privata visas inga målgrupper i det här avsnittet.

Välj **[!UICONTROL Change audience]** om du vill ändra ditt målgruppsval.

![Arbetsytan Identifiera med alternativet Ändra målgrupp markerat.](/help/assets/collaborate/discover/change-audience.png)

Dialogrutan **[!UICONTROL Change audience]** öppnas där du kan välja en specifik målgrupp att jämföra med dina medarbetares målgrupper. Markera önskade målgrupper eller rensa dina markeringar för att markera alla målgrupper och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Ändra målgrupp på arbetsytan Identifiera.](/help/assets/collaborate/discover/change-audience-selection.png)

När du har valt önskade målgrupper visar avsnittet **[!UICONTROL Discover overlaps]** följande information för varje målgrupp:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Identity count]** | Antalet unika ID:n inom målgruppen. |
| **[!UICONTROL Overlapping identities]** | Antalet unika ID:n som överlappar mellan den rekommenderade målgruppen och alla era målgrupper. |
| **[!UICONTROL Overlap %]** | Procentandelen överlappande identiteter mellan den rekommenderade målgruppen och alla era målgrupper. |
| **[!UICONTROL Audience categories]** | De kategorier som din medarbetare har tilldelat publiken. |
| **[!UICONTROL Match keys]** | De matchningsnycklar som medarbetaren valt för målgruppen. |

{style="table-layout:auto"}

## Nästa steg

När du har utforskat och identifierat de önskade målgrupperna är det dags att [aktivera](/help/guide/collaborate/activate.md) de målgrupper som ska användas i kampanjerna.
