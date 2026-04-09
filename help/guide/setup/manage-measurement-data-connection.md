---
title: Hantera anslutningar för mätdata
description: Lär dig hur du hanterar anslutningar för mätdata, inklusive detaljer och matchningsnycklar i Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 494277f421606eda62b74c254f1fdd29b22e3473
workflow-type: tm+mt
source-wordcount: '1270'
ht-degree: 0%

---

# Hantera anslutningar för mätdata

{{limited-availability-release-note}}

## Översikt

Använd mätdataanslutningar i Real-Time CDP Collaboration för att hämta konverteringsdata från olika plattformar. Lär dig hur du hanterar information och matchar nycklar för dina befintliga dataanslutningar.

## Visa måttdataanslutningar {#view-measurement-data-connections}

Du kan visa information om alla befintliga måttdataanslutningar, inklusive hur konverteringsdata hämtas, vilka matchningsnycklar som används och alla konverteringshändelser som är länkade till anslutningen.

Navigera från arbetsytan **[!UICONTROL Setup]** till fliken **[!UICONTROL My data connections]**. Alla dina nuvarande måttdataanslutningar visas under avsnittet **[!UICONTROL Measurement]** i tabell- eller stödrastervyn. Välj **[!UICONTROL View data connection]** på det aktuella anslutningskortet eller markera dataanslutningsnamnet i tabellvyn för att öppna arbetsytan och visa all information.

![Fliken Mina dataanslutningar markerar ett anslutningskort för mätdata och alternativet Visa dataanslutning.](/help/assets/setup/manage-measurement-data-connection/view-measurement-data-connection.png){zoomable="yes"}

### Anslutningsinformation för mätningsdata {#measurement-data-connection-details}

I det här avsnittet visas följande information om dataanslutningen:

| Fält | Beskrivning |
|-------------------|-------------|
| Status | Aktuellt läge för måttdataanslutningen, till exempel **[!UICONTROL Active]**. |
| Source | Den plattform eller det system som tillhandahåller mätdata för anslutningen. |
| Sandbox | Namnet på den sandlåda där anslutningen för mätningsdata är konfigurerad. |
| Datauppsättning | Namnet på den datauppsättning som används för att hämta mätdata i anslutningen. |
| Senast uppdaterad | Tidsstämpeln för den senaste uppdateringen av måttdataanslutningen. |
| Senast uppdaterad av | Användaren som senast ändrade måttdataanslutningen. |
| Skapad | Tidsstämpeln när måttdataanslutningen skapades. |
| Skapad av | Användaren som ursprungligen skapade måttdataanslutningen. |

{style="table-layout:auto"}

### Matcha nycklar {#match-keys}

Matchningsnycklar är de målfält som du mappade källfälten till när du [hämtade mätdata](./onboard-measurement-data.md). Mer information om hur matchningsnycklar fungerar finns i guiden [matchningsnycklar](./onboard-account.md#set-up-match-keys).

![En arbetsyta för anslutning av mätdata med avsnittet Matcha nycklar markerat.](/help/assets/setup/manage-measurement-data-connection/view-match-keys.png){zoomable="yes"}

### Konverteringshändelser {#conversion-events}

En lista över konverteringshändelser som är kopplade till dataanslutningen visas längst ned på arbetsytan. I listan visas en kort översikt över varje händelse, inklusive dess status, konverteringstyp och källa. Du kan markera händelsenamnet om du vill visa och redigera dess konfigurationer eller ta bort konverteringshändelsen med borttagningsalternativet (![Ta bort ikon](/help/assets/common/delete.svg)). En fullständig guide om hur du hanterar en konverteringshändelse finns i handboken [Lägg till och hantera måttdata](./onboard-measurement-data.md) .

![En arbetsyta för anslutning av mätdata med avsnittet konverteringshändelser markerat.](/help/assets/setup/manage-measurement-data-connection/view-conversion-events.png){zoomable="yes"}

## Redigera måttdataanslutning {#edit-measurement-data-connection}

Du kan uppdatera informationen och matchningsnycklarna för en befintlig mätdataanslutning när som helst för att säkerställa att rapporteringen och analysen förblir korrekta. Börja med att navigera till fliken **[!UICONTROL My data connections]** och markera den måttdataanslutning som du vill redigera. Då öppnas arbetsytan för dataanslutning, där du kan följa stegen nedan för att göra nödvändiga ändringar.

### Redigera namn och beskrivning {#edit-name-and-description}

Om du vill uppdatera dataanslutningens namn och beskrivning väljer du redigeringsikonen (![redigeringsikonen](/help/assets/icons/edit.png)) bredvid det aktuella anslutningsnamnet.

![Arbetsytan för anslutning av mätdata markerar redigeringsikonen bredvid dataanslutningsnamnet.](/help/assets/setup/manage-measurement-data-connection/edit-name-description.png){zoomable="yes"}

Uppdatera fälten i dialogrutan **[!UICONTROL Edit data connection]** med önskade värden och välj sedan **[!UICONTROL Save]** för att tillämpa ändringarna.

![Dialogrutan Redigera dataanslutning med alternativet Spara markerat.](/help/assets/setup/manage-measurement-data-connection/edit-name-description-dialog.png){zoomable="yes"}

En bekräftelsedialogruta visas som bekräftar att informationen har uppdaterats.

### Redigera matchningsnycklar {#edit-match-keys}

>[!IMPORTANT]
>
>Observera följande innan du redigerar matchningsnycklarna för en dataanslutning:
>
>* Endast matchande nycklar som har konfigurerats för ditt konto kan användas för dataanslutningar.
>* För närvarande kan du lägga till ytterligare matchningsnycklar i en dataanslutning, men när en matchningsnyckel har aktiverats kan den inte tas bort.

Välj **[!UICONTROL Edit]** på panelen **[!UICONTROL Match keys]** på arbetsytan för dataanslutning.

![Avsnittet Matcha nycklar med alternativet Redigera markerat.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys.png){zoomable="yes"}

En bekräftelsedialogruta visas som förklarar att eventuella ändringar i dataanslutningen kommer att gälla för alla associerade konverteringar. Bekräfta genom att välja **[!UICONTROL OK]**. Du kan välja att hoppa över den här bekräftelsen i framtiden.

![Bekräftelsedialogrutan som visar att eventuella ändringar i dataanslutningen kommer att gälla för alla associerade konverteringar.](/help/assets/setup/manage-measurement-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

I dialogrutan **[!UICONTROL Match keys]** kan du granska anrikningsinställningarna och se de aktuella mappningarna mellan källfälten och målfälten (matchningsnycklar).

![Dialogrutan Matcha nycklar som visar anrikningsinställningar och befintliga mappningar mellan källfält och motsvarande målfält.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys-dialog.png){zoomable="yes"}

#### Berikning {#enrichment}

Om anrikning inte var aktiverat när du [hämtade dina mätdata](./onboard-measurement-data.md) kan du berika din händelsedatamängd med attribut från kundprofilen i realtid. Observera att när berikning har aktiverats för mätdata kan den inte inaktiveras. Du kan fortfarande uppdatera anrikningsnycklarna efter behov.

När du aktiverar berikning i dialogrutan **[!UICONTROL Match keys]** utökas användargränssnittet så att fler konfigurationsalternativ visas under avsnittet **[!UICONTROL Enrich your event data with IDs from profiles]**.

Välj alternativet **[!UICONTROL Source field join key]**.

![Dialogrutan Matcha nycklar med alternativet för kopplingsnyckeln i Source-fältet markerad.](../../assets/setup/manage-measurement-data-connection/enrich-event-data.png){zoomable="yes"}

I dialogrutan **[!UICONTROL Source field join key]** väljer du källfältet följt av **[!UICONTROL Select]**.

![Source-fältets dialogruta för kopplingsnyckel där det markerade källfältet och alternativet Nästa markeras.](../../assets/setup/manage-measurement-data-connection/source-field-join-key-dialog.png){zoomable="yes"}

Välj sedan alternativet **[!UICONTROL Profile join key]**. Välj profilfältet i listan i dialogrutan **[!UICONTROL Profile join key]**. Du kan använda alternativet Sök för att hitta det önskade fältet. Välj sedan **[!UICONTROL Select]** för att bekräfta.

![Dialogrutan för anslutningsnyckel för profil markerar det valda profilfältet och alternativet Välj.](../../assets/setup/manage-measurement-data-connection/profile-join-key-dialog.png){zoomable="yes"}

#### Redigera mappning {#edit-mapping}

Om du vill redigera en befintlig matchningsnyckel uppdaterar du dess associerade källfält och målfält i dialogrutan **[!UICONTROL Match keys]**. Om du vill inkludera en ny matchningsnyckel väljer du **[!UICONTROL Add field]**. Då skapas en tom rad där du kan definiera ytterligare mappning mellan käll- och målfält.

![När du har valt Lägg till fält visas en tom ny mappningsrad klar för indata i dialogrutan Matcha nycklar.](/help/assets/setup/manage-measurement-data-connection/add-new-field.png){zoomable="yes"}

Välj sedan det tomma källfältet. Dialogrutan **[!UICONTROL Select source field]** visas med en lista över tillgängliga källfält grupperade under alternativ som **[!UICONTROL Identity namespaces]** och **[!UICONTROL Profile attributes]**. Du kan filtrera listan och hitta det önskade källfältet med sökalternativet.

Välj det källfält som du vill använda, följt av **[!UICONTROL Select]**.

![Dialogrutan Välj källfält där sökalternativet, telefonkällfältet och alternativet Välj markeras.](/help/assets/setup/manage-measurement-data-connection/select-source-field.png){zoomable="yes"}

Använd listrutemenyn i dialogrutan **[!UICONTROL Match keys]** för att mappa det nya källfältet till ett målfält. Alla tillgängliga målfält är matchningsnycklar som konfigurerats för ditt medarbetarkonto. Om du inte ser målfältet som du behöver kan du [redigera kontots matchningsnycklar](./onboard-account.md#edit-match-keys) för att lägga till det.

Använd alternativet **[!UICONTROL Apply transformation]** om du vill att ett icke-hash-kodat fält ska hämtas till ett hash-kodat målfält, till exempel när du mappar ett vanligt textfält för telefonens källa till målfältet i **[!UICONTROL Hashed phone]**.

![Listrutan med alla tillgängliga målfält som ska mappas med det nya källfältet.](/help/assets/setup/manage-measurement-data-connection/target-field-dropdown.png){zoomable="yes"}

När du är klar med mappningen av fält granskar du uppdateringarna och väljer **[!UICONTROL Confirm]** för att tillämpa ändringarna.

![Dialogrutan Matcha nycklar visar den uppdaterade fältmappningen med alternativet Bekräfta markerat.](/help/assets/setup/manage-measurement-data-connection/confirm-edit-match-keys.png){zoomable="yes"}

En bekräftelsedialogruta bekräftar att matchningsnycklarna har uppdaterats.

## Ta bort dataanslutning

Om du tar bort en dataanslutning tas alla underliggande konverteringar, associerade inställningar och användning bort i Collaboration. Det går inte att ångra den här åtgärden.

Om du vill ta bort en befintlig dataanslutning markerar du ikonen Ta bort (![ikonen Ta bort](/help/assets/common/delete.svg)) på en enskild dataanslutnings arbetsyta.

![En arbetsyta för dataanslutningar med borttagningsalternativet markerat.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection.png){zoomable="yes"}

En bekräftelsedialogruta visas. Välj **[!UICONTROL Delete]** om du vill ta bort dataanslutningen.

![Dialogrutan Ta bort dataanslutning med alternativet Ta bort markerat.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection-confirm.png){zoomable="yes"}

En bekräftelsedialogruta bekräftar att dataanslutningen har tagits bort.

## Nästa steg {#next-steps}

När du har hanterat mätdataanslutningarna kan du:

* Lägg till fler konverteringshändelser som är länkade till din dataanslutning efter behov. Mer information finns i dokumentationen för [Lägg till och hantera mätdata](./onboard-measurement-data.md).
* Generera mätrapporter för att få insikter om kampanjens resultat och påverkan. Mer information om tillgängliga rapporttyper och hur du skapar dem finns i guiden [Måttprestanda](/help/guide/collaborate/measure.md).
