---
title: Mät prestanda
description: Mät kampanjernas resultat i olika kanaler. Lär dig hur du använder och tolkar olika rapporter.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Mät prestanda

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Measure]** är bara tillgänglig om användningsfallet **Measurement** aktiverades [ under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

Läs mer om tillgängliga rapporter i Adobe Real-Time CDP Collaboration och förstå hur ni mäter och analyserar hur era marknadsföringskampanjer fungerar i olika kanaler.

## Förhandskrav

Innan du kan komma åt mätrapporterna i Collaboration har du redan:

* [Ansluten](/help/guide/connect/establishing-connections.md) till en annonsör eller utgivare med användningsfallet **Mått** aktiverat och börjat samarbeta i [projekt](/help/guide/collaborate/manage-projects.md)
* Kör en kampanj och [överförde mätdata](/help/guide/setup/onboard-measurement-data.md) till Collaboration.

<!--

## Create a report {#create-report}

Hidden until functionality is live. At that point, move the contextualhelp from below into this section. 

The syntax rtcdp_collaboration_measurement_create_report is currently implemented in the UI. However, a preference would be to imlement the other contextualhelp ID from below instead, since that explicitly includes campaignID in the syntax. Need to sync up with UI team. More details in CORE-116991.

-->

## Visa rapporter {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="Kampanj-ID"
>abstract="Platshållare för att lägga till relevant information i användargränssnittet om vad kampanj-ID:n är."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report"
>title="Kampanj-ID"
>abstract="Platshållare för att lägga till relevant information i användargränssnittet om vad kampanj-ID:n är."

Så här visar du de rapporter som finns på fliken Mått:

1. Navigera till **[!UICONTROL Collaborate]** > **[!UICONTROL My projects]**.
2. Välj **[!UICONTROL View]** för det önskade projektet.
3. Välj fliken **[!UICONTROL Measure]** i projektet.

Välj **[!UICONTROL View full report]** om du vill komma åt de olika tillgängliga rapporterna, som beskrivs närmare nedan.

![Så här kommer du till mätfliken i ett projekt.](/help/assets/collaborate/measure/measurement.gif)

### Sammanfattningsvy

I den övre delen av sidan på mätfliken visas en kampanjsammanfattning med några högnivånummer som du kan referera till:

**[!UICONTROL Impressions]**: Det totala antalet gånger som den kreativa har visats.
**[!UICONTROL Unique reach]**: Antalet enskilda identiteter som har sett den kreativa.
**[!UICONTROL Total average frequency]**: Antalet visningar delat med unika identiteter har uppnåtts. Den här bilden visar hur ofta varje identitet visades för den kreativa.

![Kampanjsammanfattningsvy](/help/assets/collaborate/measure/campaign-summary.png)

### Mätvärden över tid {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="Mätvärden över tid"
>abstract="Använd mätvärden över tiden för att förstå det totala antalet visningar som visas för dina kreatörer under kampanjperioden. Du kan välja högst två dimensioner som ska visas i rapporten."

Använd mätvärden över tiden för att förstå det totala antalet visningar som visas för dina kreatörer under kampanjperioden. Observera att du kan välja högst två mätvärden som ska visas och analyseras i rapporten.

![Mätvärden över tid.](/help/assets/collaborate/measure/metrics-over-time.png)

### Frekvensfördelning {#frequency-distribution}

Använd frekvensfördelningsvyn för att förstå hur många visningar som har visats för varje unik användare. Den här vyn kan hjälpa er att i framtida kampanjer avgöra vid vilken tidpunkt ni vill börja undertrycka målgrupper. Du kanske vill inaktivera profiler som redan har sett en kreatör tre gånger.

![Vyn Frekvensfördelning.](/help/assets/collaborate/measure/frequency-distribution.gif)

### Mått efter dimension {#metric-by-dimension}

Analysera olika mätvärden, som visningar, visningsbara exponeringar, unik räckvidd, kostnad med mera i det sammanhang där placeringsmediet används. Analysera vilket medium (till exempel mobil direktuppspelning, CTV-programmering eller andra) som ger bäst resultat för era kampanjer.

![Mått per dimension.](/help/assets/collaborate/measure/metric-by-dimension.png)

### Kumulativ nålskurva {#cumulative-reach-curve}

I takt med att kampanjen fortskrider och antalet visningar ökade, förstår du om antalet användare du kunde nå också har ökat. Ett vanligt mönster i kampanjer är att man efter en viss tidpunkt når en platå där den kreativa effekten visas för samma personer om och om igen. Den här vyn kan hjälpa dig att justera längden på framtida kampanjer, beroende på när nya personer inte längre nås.

![Kumulativ räckvidd-kurva.](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### Impression efter placering {#impressions-by-placement}

Förstå vilket medium som ger kreativiteten ett intryck. Detta kan hjälpa er att bestämma var ni ska investera annonskostnaderna i framtida kampanjer.

![Impressions efter placering.](/help/assets/collaborate/measure/impressions-by-placement.png)

## Nästa steg

![Identifiera, aktivera, mät för annonsörer.](/help/assets/end-to-end-workflow/discover-activate-measure.png)

I samma anda som cykliciteten i bilden ovan använder du de insikter du får när du tittar på rapporterna i planeringen av nästa kampanj. Som annonsörer kan du vid behov gå tillbaka till olika utgivare och köra överlappningar för att identifiera olika målgrupper för dina nästa kampanjer.
