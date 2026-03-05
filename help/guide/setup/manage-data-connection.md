---
title: Hantera dataanslutningar
description: Lär dig hantera dataanslutningar, inklusive matchningsnycklar, schemaläggning, användningsfall och målgruppsfiltrering i Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: 4bfa57ba36336dd835551fb846f1d567d6830bf9
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---

# Hantera dataanslutningar

{{limited-availability-release-note}}

## Översikt

Använd dataanslutningar i Real-Time CDP Collaboration för att hämta målgrupper från olika plattformar. Lär dig hur du hanterar matchningsnycklar och schemalägger datauppdatering för dina befintliga dataanslutningar. Dessutom kan ni filtrera målgrupperna utifrån olika attribut för mer detaljerade insikter.

## Visa dataanslutningar

Om du vill visa befintliga dataanslutningar går du till **[!UICONTROL Setup]** och väljer fliken **[!UICONTROL My data connections]**. Alla dina aktuella dataanslutningar visas med en kort översikt för varje anslutning. Om du vill visa information om en dataanslutning, inklusive matchningsnycklar, schemaläggningsinformation och målgrupper, väljer du **[!UICONTROL View data connection]** på motsvarande anslutning.

![Arbetsytan Konfigurera med flikvyn Mina dataanslutningar visas och markeras.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Matcha nycklar {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Matcha nycklar"
>abstract="Matchningsnycklar avgör hur data från olika källor matchas. De matchningsnycklar som visas nedan är de målfält som du har mappat källfälten till."

Matchande nycklar är de målfält som du [mappade dina källfält till ](./onboard-audiences.md#map-fields). Mer information om hur matchningsnycklar fungerar finns i guiden [matchningsnycklar](./onboard-account.md#set-up-match-keys).

![En arbetsyta för dataanslutningar med avsnittet Matcha nycklar markerat.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Schemaläggning {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Schemaläggning"
>abstract="Visa schemaläggningsinformation för din dataanslutning och redigera konfigurationerna om det behövs."

Visa och hantera schemainställningarna för dataanslutningarna. Schemaläggningen bestämmer hur ofta målgruppen uppdateras.

När en dataanslutning har skapats kan du uppdatera dess uppdateringsfrekvens, startdatum och slutdatum direkt från avsnittet **[!UICONTROL Scheduling]** på arbetsytan för dataanslutning.

>[!NOTE]
>
>När ni hämtar målgrupper från Adobe Experience Platform blir målgrupperna tillgängliga inom 24 timmar efter det att dataanslutningen har upprättats. Efter den initiala källan uppdateras målgruppsdata enligt den definierade frekvensen.

Mer information om schemaläggning finns i avsnittet [schemaläggning](/help/guide/setup/onboard-audiences.md#schedule) i guiden för att konfigurera målgrupper.

![En dataanslutnings arbetsyta med avsnittet Schemaläggning markerat.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Redigera dataanslutning {#edit-data-connection}

Läs följande avsnitt för att lära dig hur du uppdaterar matchningsnycklar och schemaläggningsinställningar för en befintlig dataanslutning.

### Redigera matchningsnycklar {#edit-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_edit_measurement_data_connection_enrichment"
>title="Berikning"
>abstract="Inaktivering av anrikning stöds inte. Du kan ändra anrikningsnycklarna i stället."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-manage-dataconnections" text="Berikning"

>[!IMPORTANT]
>
>Observera följande innan du redigerar matchningsnycklarna för en dataanslutning:
>
>* Endast matchande nycklar som har konfigurerats för ditt konto kan användas för dataanslutningar.
>* För närvarande kan du lägga till ytterligare matchningsnycklar i en dataanslutning, men när en matchningsnyckel har aktiverats kan den inte tas bort.

Välj **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Match keys]**.

![Avsnittet Matcha nycklar med alternativet Redigera markerat.](/help/assets/setup/manage-data-connection/edit-match-keys.png){zoomable="yes"}

En bekräftelsedialogruta visas som förklarar att eventuella ändringar i dataanslutningen kommer att gälla för alla associerade målgrupper. Bekräfta genom att välja **[!UICONTROL OK]**. Du kan välja att hoppa över den här bekräftelsen i framtiden.

![Bekräftelsedialogruta som visar att alla ändringar i dataanslutningen kommer att gälla för alla associerade målgrupper.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

I dialogrutan **[!UICONTROL Match keys]** kan du visa befintliga mappningar mellan källfält och deras motsvarande målfält (matchningsnycklar). Du kan redigera en matchningsnyckel genom att uppdatera det mappade källfältet eller lägga till ytterligare mappningsfältrader för att fylla i nya matchningsnycklar.

![Dialogrutan Matcha nycklar visar befintliga mappningar mellan källfält och motsvarande målfält.](/help/assets/setup/manage-data-connection/match-keys-dialog.png){zoomable="yes"}

#### Lägg till matchningsnycklar {#add-match-keys}

Välj **[!UICONTROL Add field]** om du vill lägga till en ny fältrad.

![När du har valt Lägg till fält visas ett tomt nytt mappningsfält som är klart för indata i dialogrutan Matcha nycklar.](/help/assets/setup/manage-data-connection/add-new-field.png){zoomable="yes"}

Välj sedan det tomma källfältet. Dialogrutan **[!UICONTROL Select source field]** visas med alternativen **[!UICONTROL Identity namespaces]** och **[!UICONTROL Profile attributes]**. Du kan filtrera listan och hitta det önskade källfältet med sökalternativet.

Välj det källfält som du vill använda, följt av **[!UICONTROL Select]**.

![Dialogrutan Välj källfält med alternativet GAID markerat.](/help/assets/setup/manage-data-connection/select-source-field.png){zoomable="yes"}

Använd listrutemenyn i dialogrutan **[!UICONTROL Match keys]** för att mappa det nya källfältet till ett målfält. Alla tillgängliga målfält är matchningsnycklar som konfigurerats för ditt medarbetarkonto. Om du inte ser målfältet som du behöver kan du [redigera kontots matchningsnycklar](./onboard-account.md#edit-match-keys) för att lägga till det.

Använd alternativet **[!UICONTROL Apply transformation]** om du vill skapa ett icke-hash-kodat fält till ett hash-kodat målfält, till exempel när du mappar ett e-postkällfält med oformaterad text till målfältet **[!UICONTROL Hashed email]**.

![Listrutan med alla tillgängliga målfält som ska mappas med det nya källfältet.](/help/assets/setup/manage-data-connection/select-target-field.png){zoomable="yes"}

När du är klar med mappningen av fält granskar du uppdateringarna och väljer **[!UICONTROL Confirm]** för att tillämpa ändringarna.

![Dialogrutan Matcha nycklar visar den uppdaterade fältmappningen med alternativet Bekräfta markerat.](/help/assets/setup/manage-data-connection/review-and-confirm.png){zoomable="yes"}

En bekräftelsedialogruta bekräftar att matchningsnycklarna har uppdaterats.

### Redigera schemaläggning {#edit-scheduling}

När en dataanslutning har skapats kan du uppdatera dess uppdateringsfrekvens, startdatum och slutdatum direkt från avsnittet **[!UICONTROL Scheduling]** på arbetsytan för dataanslutning.

Du kan redigera frekvensen för en befintlig dataanslutning för att bättre kontrollera hur ofta målgrupperna uppdateras. Om du vill redigera schemat väljer du **[!UICONTROL Edit]** i dataanslutningen på schemaläggningskortet.

![Avsnittet Schemaläggning med alternativet Redigera markerat.](/help/assets/setup/manage-data-connection/edit-scheduling.png){zoomable="yes"}

En bekräftelsedialogruta visas som förklarar att eventuella ändringar i dataanslutningen kommer att gälla för alla associerade målgrupper. Bekräfta genom att välja **[!UICONTROL OK]**. Du kan välja att hoppa över den här bekräftelsen i framtiden.

![Bekräftelsedialogruta som visar att alla ändringar i dataanslutningen kommer att gälla för alla associerade målgrupper.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

I dialogrutan **[!UICONTROL Scheduling]** väljer du listrutan för att uppdatera **[!UICONTROL Frequency]**. Ställ in uppdateringsfrekvensen så att den körs dagligen eller varannan till var sjätte dag.

![Dialogrutan Schemaläggning med listrutan Frekvens utökad för att visa alternativ för målgruppens uppdateringsfrekvens.](../../assets/setup/manage-data-connection/edit-frequency.png){zoomable="yes"}

Välj sedan **[!UICONTROL Date range]** om du vill uppdatera den period under vilken målgrupper fylls i och uppdateras.

![Dialogrutan Schemaläggning visar listrutan Datumintervall utökat för att redigera start- och slutdatum för målgruppspopulationen och uppdatera.](../../assets/setup/manage-data-connection/edit-date-range.png){zoomable="yes"}

När du är klar granskar du uppdateringarna och väljer **[!UICONTROL Save]** för att tillämpa ändringarna.

![I dialogrutan Schemaläggning markeras uppdateringarna och alternativet Spara.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

## Ta bort dataanslutning

Om du tar bort en dataanslutning tas alla underliggande målgrupper, associerade inställningar och användning bort i Collaboration. Det går inte att ångra den här åtgärden.

Om du vill ta bort en befintlig dataanslutning markerar du ikonen Ta bort (![ikonen Ta bort](/help/assets/common/delete.svg)) på en enskild dataanslutnings arbetsyta.

![En arbetsyta för dataanslutningar med borttagningsalternativet markerat.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

En bekräftelsedialogruta visas. Välj **[!UICONTROL Delete]** om du vill ta bort dataanslutningen.

![Dialogrutan Ta bort dataanslutning med alternativet Ta bort markerat.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Hantera målgrupper {#manage-audiences}

En lista över målgrupper som är kopplade till dataanslutningen visas längst ned på arbetsytan. I listan visas en kort översikt över varje målgrupp, inklusive dess status, källa och anslutningsåtkomst. Om du vill redigera en målgrupps kategorier, anslutningsåtkomst eller metadatavisbarhet markerar du målgruppens namn. En fullständig guide om hur du hanterar en målgrupp finns i guiden [Visa enskilda målgrupper](./onboard-audiences.md#view-individual-audiences).

![En arbetsyta för dataanslutningar med målgrupperna markerade.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Nästa steg

När du har hanterat dina dataanslutningar kan du [identifiera överlappningar](/help/guide/collaborate/discover.md) mellan dina målgrupper och de målgrupper som din medarbetare har gjort identifierbara.
