---
title: Upptäck överlappningar och jämför målgrupper
description: Upptäck överlappningar mellan era och medarbetarnas målgrupper. Lär dig hur ni hittar de bästa målgrupperna som kan användas i era kampanjer.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: 75e76a43de75a7b1c84bdd79cb4a072855ba02df
workflow-type: tm+mt
source-wordcount: '2009'
ht-degree: 0%

---

# Upptäck överlappningar och jämför målgrupper

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Discover]** är bara tillgänglig om **målgruppsidentifiering** har aktiverats [ under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

När du har [skapat ett projekt](/help/guide/collaborate/manage-projects.md) kan du jämföra dina målgrupper med dina medarbetare. Detta hjälper er att identifiera relevanta målgrupper för kampanjer och avgöra vilka som ska skickas till medarbetare för aktivering.

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
| **[!UICONTROL Audience index]** | Ett poängtal som anger hur starkt en viss målgrupp relaterar till en annan baserat på antalet underliggande målgrupper och överlappningar. Läs avsnittet [målgruppsindexpoäng](#audience-index-score) om du vill veta mer om vad poängen innebär. Poäng för målgruppsindex är inte tillgängliga vid jämförelse med medarbetarens baslinje (alla målgrupper). |
| **[!UICONTROL Identities breakdown by match key]** | Uppdelningen av identiteter för varje matchningsnyckel som valts i projektet, baserat på valda målgrupper för varje medarbetare. |

{style="table-layout:auto"}

>[!NOTE]
>
>Procenttalet för överlappning och poängtalet för målgruppsindex kanske inte alltid är tillgängligt för alla målgrupper. Synligheten för överlappningsprocenten och målgruppsindexvärdet beror på inställningen som medarbetaren valde för en målgrupp i avsnittet [metadatasynlighet](/help/guide/setup/onboard-audiences.md#metadata-visibility).

Om medarbetaren inte har aktiverat målgruppsindexet eller överlappningsprocenten kommer målgruppen inte att ha några tillgängliga jämförelsedata.

## Relevanta målgrupper {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Relevanta målgrupper"
>abstract="Dessa målgrupper, som baseras på överlappningsprocentsatser, kan passa bra för er kampanj. <br><br> <b>Identitetsantalet</b> är medarbetarens målgruppsstorlek. <br><br> <b>Överlappande identiteter</b> representerar överlappningen mellan den rekommenderade målgruppen och alla dina målgrupper. <br><br> <b>Överlappningen %</b> representerar antalet överlappande identiteter dividerat med storleken på <i>alla</i> dina målgrupper."

Avsnittet **[!UICONTROL Relevant audiences]** på fliken **[!UICONTROL Discover]** innehåller en förvaltad lista över de fem främsta målgrupperna baserat på överlappningsprocenten mellan medarbetarens målgrupp och alla dina målgrupper. Med den här funktionen kan ni snabbt identifiera målgrupper med den högsta överlappningen, så att ni kan inrikta er på kampanjer mer effektivt. Växla mellan de relevanta målgrupperna med hjälp av sidväljarna i det övre högra hörnet av avsnittet.

![Arbetsytan Identifiera med avsnittet Relevanta målgrupper markerat.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>Visningen av dina medarbetares målgrupper beror på den inställning som medarbetaren har valt för en målgrupp i [sektionen för åtkomst till anslutningen](/help/guide/setup/onboard-audiences.md#connection-access) och i avsnittet [synlighet för metadata](/help/guide/setup/onboard-audiences.md#metadata-visibility). Om din medarbetare har angett alla målgrupper som privata visas inga målgrupper i det här avsnittet.

I avsnittet **[!UICONTROL Relevant audiences]** visas följande information för varje rekommenderad målgrupp:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Identity count]** | Antalet unika ID:n inom målgruppen. |
| **[!UICONTROL Overlapping identities]** | Antalet unika ID:n som överlappar mellan den rekommenderade målgruppen och alla era målgrupper. |
| **[!UICONTROL Overlap %]** | Procentandelen överlappande identiteter mellan den rekommenderade målgruppen och alla era målgrupper. |
| **[!UICONTROL Audience index]** | Ett poängtal som anger hur starkt en viss målgrupp relaterar till en annan baserat på antalet underliggande målgrupper och överlappningar. Läs avsnittet [målgruppsindexpoäng](#audience-index-score) om du vill veta mer om vad poängen innebär. |
| **[!UICONTROL Audience categories]** | De kategorier som din medarbetare har tilldelat publiken. |
| **[!UICONTROL Match keys]** | De matchningsnycklar som medarbetaren valt för målgruppen. |

{style="table-layout:auto"}

Om målgruppsindexpoäng är aktiverat för någon av dina medarbetares målgrupper, kommer relevanta målgrupper att baseras på poängen för målgruppsindexet, och målgrupper där målgruppsindexet inte är aktiverat kommer inte att tas med. Relevanta målgrupper baserat på målgruppsindexets poäng sorteras så att det högsta indexvärdet visas först. Om målgruppsindex inte är aktiverat för någon av dina medarbetares målgrupper, kommer de relevanta målgrupperna att baseras på överlappningsprocenten.

## Upptäck överlappningar {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Upptäck överlappningar med enskilda målgrupper"
>abstract="Få insikter om överlappningar mellan era målgrupper och medarbetarnas målgrupper."

Upptäck överlappningar för att få insikter i hur era målgrupper står sig jämfört med era medarbetares målgrupper. Som standard jämförs alla era målgrupper i det här avsnittet med alla era medarbetares målgrupper. Använd sidnumreringskontrollen längst ned i avsnittet för att navigera bland de tillgängliga målgrupperna.

![Arbetsytan Identifiera med avsnittet Identifiera överlappning markerat.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>Visningen av dina medarbetares målgrupper beror på den inställning som medarbetaren har valt för en målgrupp i [sektionen för åtkomst till anslutningen](/help/guide/setup/onboard-audiences.md#connection-access) och i avsnittet [synlighet för metadata](/help/guide/setup/onboard-audiences.md#metadata-visibility). Om din medarbetare har angett alla målgrupper som privata visas inga målgrupper i det här avsnittet.

Om medarbetaren inte har aktiverat målgruppsindexet eller överlappningsprocenten visas inte målgruppen.

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
| **[!UICONTROL Audience index]** | Ett poängtal som anger hur starkt en viss målgrupp relaterar till en annan baserat på antalet underliggande målgrupper och överlappningar. Läs avsnittet [målgruppsindexpoäng](#audience-index-score) om du vill veta mer om vad poängen innebär. |
| **[!UICONTROL Audience categories]** | De kategorier som din medarbetare har tilldelat publiken. |
| **[!UICONTROL Match keys]** | De matchningsnycklar som medarbetaren valt för målgruppen. |

{style="table-layout:auto"}

## Målgruppsindexpoäng {#audience-index-score}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_audience_index_score"
>title="Målgruppsindexpoäng"
>abstract="Poängen för målgruppsindex är en ny mätmetod som visar hur mycket en målgrupp relaterar till en annan baserat på underliggande målgruppsantal och överlappningar. Poängen för råindex översätts till relevansband, som kategoriserar poängen för målgruppsindexet från mycket låg till mycket hög. På så sätt kan ni snabbt bedöma styrkan i relationen mellan er målgrupp och medarbetarens målgrupp."

Poängen för målgruppsindex är en ny mätmetod som visar hur mycket en målgrupp relaterar till en annan baserat på underliggande målgruppsantal och överlappningar. Detta hjälper er att kontextualisera målgruppsinsikter och identifiera potentiella målgrupper för prospektering och kampanjanpassning.

Indexpoängen beräknas med följande formel:

![Formeln för beräkning av indexpoäng.](/help/assets/collaborate/discover/index-score-formula.png)

Tänk dig en biltillverkare som vill genomföra en reklamkampanj med en stor CTV-utgivare för en ny SUV-modell. Biltillverkaren har uppgifter om vem som för närvarande äger en liknande modell och vill använda den för att hitta fler potentiella kunder som kan konvertera dem till kunder. Biltillverkaren tittar på tittarna på förlaget för tv-reklam för att hitta en relevant målgrupp som nära matchar de nuvarande SUV-ägarna.

![Bilannonsören kontra CTV-utgivarens målgrupper.](/help/assets/collaborate/discover/audience-index-score-example.png)

Beräkningar av indexpoäng görs och kan användas för att avgöra om kampanjen kommer att lyckas:

| CTV Publisher Audience | Formel | Indexpoäng (i) | Tolkning |
|------------------------|-------------|----------------|----------------|
| Baslinje (alla målgrupper) | ((1,3 MB/1,3 MB) / (50 MB/50 MB)) * 100 | 100 | Detta fungerar som den baslinje som medarbetarens andra målgrupper jämförs med. |
| Binge Watchers | ((500 kB/1,3 MB) / (20 MB/50 MB)) * 100 | 96 | Om ni riktar er till den här målgruppen är sannolikheten att nå SUV-ägare 4 % mindre jämfört med baslinjen. |
| Komedi Lovers | (200 kB/1,3 MB) / (6 MB/50 MB) * 100 | 128 | Genom att rikta in er på den här målgruppen är ni 28 % mer benägna att nå SUV-ägare jämfört med baslinjen. |
| Män 25-34 | ((700 kB/1,3 MB) / (12 MB/50 MB)) * 100 | 224 | Genom att rikta in er på den här målgruppen är ni 124 % mer benägna att nå SUV-ägare jämfört med baslinjen. |
| Teknikentusiaster | ((500 kB / 1,3 MB) / (8 MB / 50 MB)) * 100 | 240 | Genom att rikta in er på den här målgruppen är ni 140 % mer benägna att nå SUV-ägare jämfört med baslinjen. |

{style="table-layout:auto"}

För att få en bättre förståelse för hur indexpoängen kommer att påverka er kampanj finns det relevanta band tillsammans med poängen.

### Relevansband {#audience-index-relevance-bands}

För att det ska vara enkelt att jämföra olika målgrupper och kampanjer översätter Collaboration indexpoängen till relevansband (mycket låg till mycket hög). På så sätt kan ni snabbt bedöma styrkan i relationen mellan er målgrupp och medarbetarens målgrupp.

| Indexpoäng (i) | Relevansband | Beskrivning |
|---------------|----------|-----------|
| i &lt; 60 | Mycket låg | Överlappningen är mycket mindre förekommande hos målgruppen än hos er målgrupp, vilket tyder på en mycket svag relation. Kunder som använder den här målgruppen är mycket mindre benägna att nå sin målgrupp. |
| 60 &lt; i &lt; 80 | Låg | Överlappningen är något mindre utbredd hos målgruppen jämfört med målgruppen, vilket tyder på en svag relation. Kunder som använder den här målgruppen är mindre benägna att nå sin målgrupp. |
| 80 &lt; i &lt; 120 | Medium | Överlappningen är ungefär lika stor i målgruppen som i målgruppen, vilket tyder på en typisk relation. Kunder som använder den här målgruppen har en genomsnittlig sannolikhet att nå sin målgrupp. |
| 120 &lt; i &lt; 140 | Hög | Överlappningen är vanligare hos målgruppen jämfört med målgruppen, vilket visar på en stark relation. Kunder som använder den här målgruppen är mer benägna att nå målgruppen. |
| i > 140 | Mycket hög | Överlappningen är mycket vanligare hos målgruppen jämfört med målgruppen, vilket avspeglar en mycket stark relation. Kunder som använder den här målgruppen är mer benägna att nå sin målgrupp. |

{style="table-layout:auto"}

I avsnittet om upptäckt överlappar kommer målgruppsindexets poäng att visa relevansbandet bredvid poängen. Poängen färgkodas för att indikera relevansbandet, vilket gör det enkelt att snabbt identifiera relationens styrka. Mycket låga och låga relevansband visas i orange, medelrelevanta band i svart och högkvalitativa och mycket högkvalitativa band i grönt.

## Nästa steg

När du har utforskat och identifierat de önskade målgrupperna är det dags att [aktivera](/help/guide/collaborate/activate.md) de målgrupper som ska användas i kampanjerna.
