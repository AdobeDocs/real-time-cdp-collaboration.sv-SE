---
title: Amazon Marketing Cloud
description: Läs om hur du samarbetar med Amazon Marketing Cloud i Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 57b847c25edbf88f4708bda74be41fe6141472a7
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

När annonsörer har skapat en anslutning till [!DNL Amazon Marketing Cloud] ([!DNL AMC]) kan de [skapa ett projekt](../manage-projects.md#create-project) som de kan samarbeta med [!DNL AMC] för att utnyttja sina avancerade analysfunktioner. När du har skapat ett projekt kan du använda avsnittet **[!UICONTROL Discover]** för att jämföra målgruppsinsikter och identifiera relevanta målgrupper för dina kampanjer.

>[!IMPORTANT]
>
>De enda användningsfall som stöds med [!DNL AMC] är **Målgruppsidentifiering** och **Mått**. För närvarande är bara avsnittet **[!UICONTROL Discover]** tillgängligt i ditt projekt med [!DNL AMC].

## Upptäck {#discover}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Jämför målgrupper"
>abstract="Jämför er målgrupp med alla kunder som Amazon Ads når."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Relevanta målgrupper"
>abstract="Amazon inriktar sig på segment som er målgrupp har störst överlappning med tanke på att endast DSP-visningar förekommer (dessa segment kan bara användas i DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="Lösta ID:n"
>abstract="Antalet ID:n Amazon Identity Resolution kunde matchas med era målgruppsdata."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="Överlappande och exponerade ID"
>abstract="Detta visar antalet&quot;Lösta ID:n&quot; från den överförda publiken som också har exponerats för en annons via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="Överlappa %"
>abstract="Andelen&quot;Lösta ID:n&quot; som har exponerats för en annons via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Uppdelning efter Amazon-produkt"
>abstract="Uppdelningen av överlappande och exponerade ID:n som nås av antingen Amazon Ads Sponsored Product och/eller Amazon Ads DSP."

I avsnittet **[!UICONTROL Discover]** kan du jämföra din AMC-målgrupp med alla kunder som nås av dina Amazon Ads. Du kan också visa segment för målgruppsanpassning i Amazon som publiken har störst överlappning med, med tanke på att det bara är DSP-visningar (dessa segment kan bara användas i DSP).

>[!IMPORTANT]
>
>Målgruppsdata bearbetas från de målgrupper som har överförts till ditt [!DNL Amazon Ads]-konto. Läs [!DNL Amazon Ads]Amazon Ads-anslutningsguiden[&#x200B; om du vill lära dig hur du skickar med Experience Platform Destinations-funktionen för att skicka dina målgrupper till ditt &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/amazon-ads)-konto.

![Avsnittet Discover i ett projekt med Amazon Marketing Cloud.](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### Jämför målgrupper {#compare-audiences}

Avsnittet **[!UICONTROL Compare audiences]** innehåller insikter om hur din [!DNL AMC]-målgrupp överlappar de kunder som nås av dina Amazon Ads. I avsnittet **[!UICONTROL Compare audiences]** kan du visa följande mått:

| Mått | Beskrivning |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL Resolved IDs] | Antalet ID:n [!DNL Amazon’s Identity Resolution] kunde matchas med dina målgruppsdata. |
| [!UICONTROL Overlapping ad exposed IDs] | Antalet [!UICONTROL Resolved IDs] från den överförda målgruppen som också har exponerats för en annons via [!DNL Amazon Ads]. |
| [!UICONTROL Overlap %] | Andelen [!UICONTROL Resolved IDs] som har exponerats för en annons via [!DNL Amazon Ads]. |
| [!UICONTROL Breakdown by Amazon ad product] | Uppdelningen av [!UICONTROL Overlapping ad exposed IDs] har nåtts av antingen [!UICONTROL Sponsored Product] och/eller [!UICONTROL DSP]. Varje värde representeras som en individuell procentandel av det totala antalet annonserade exponerade ID:n. Eftersom ett ID kan tillhöra både [!UICONTROL Sponsored Products] och [!UICONTROL DSP] får procentsatserna inte vara 100 %. |


### Relevanta målgrupper {#relevant-audiences}

Avsnittet **[!UICONTROL Relevant audiences]** innehåller insikter om [!DNL Amazon] målsegment, eller målgrupper, som din målgrupp har störst överlappning med, med hänsyn enbart till DSP-visningar (dessa segment kan bara användas i DSP). Du kan växla mellan alla relevanta målgrupper och inom varje avsnitt kan du visa följande mätvärden:

| Mått | Beskrivning |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL Resolved IDs] | Antalet ID:n [!DNL Amazon’s Identity Resolution] kunde matchas med dina målgruppsdata. |
| [!UICONTROL Overlapping ad exposed IDs] | Detta representerar antalet [!UICONTROL Resolved IDs] från den överförda målgruppen som också har exponerats för en annons via [!DNL Amazon Ads]. Detta gäller endast DSP intryck. |
| [!UICONTROL Overlap %] | Andelen [!UICONTROL Resolved IDs] som har exponerats för en annons via [!DNL Amazon Ads]. |
| [!UICONTROL Categories] | Kategorin eller kategorierna som målgruppen tillhör. En målgrupp kan tillhöra flera kategorier. |

### Identifiera överlappningar med [!DNL Amazon Marketing Cloud] {#discover-overlaps}

Avsnittet **[!UICONTROL Discover overlaps with Amazon Marketing Cloud]** ger insikter om hur era målgrupper överlappar [!DNL Amazon] målgruppssegment eller målgrupper. Du kan visa följande mått:

| Mått | Beskrivning |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL Resolved IDs] | Antalet ID:n [!DNL Amazon’s Identity Resolution] kunde matchas med dina målgruppsdata. |
| [!UICONTROL Overlapping ad exposed IDs] | Detta representerar antalet [!UICONTROL Resolved IDs] från den överförda målgruppen som också har exponerats för en annons via [!DNL Amazon Ads]. Detta gäller endast DSP intryck. |
| [!UICONTROL Overlap %] | Andelen [!UICONTROL Resolved IDs] som har exponerats för en annons via [!DNL Amazon Ads]. |