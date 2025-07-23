---
title: Hantera dataanslutningar
description: Lär dig hantera dataanslutningar, inklusive matchningsnycklar, schemaläggning, användningsfall och målgruppsfiltrering i Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '584'
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
>abstract="Matchningsnycklar avgör hur data från olika källor matchas. Välj de matchande nycklar som är mest relevanta för dina användningsfall och sekretesspolicyer."

Matchningsnycklar är identifierare som används för att stämma av medlemmar mellan olika målgrupper från olika datakällor. Du kan inte redigera de matchningsnycklar som du ursprungligen valde för din dataanslutning.

>[!IMPORTANT]
> 
>Matchningsnycklar kan inte redigeras efter att dataanslutningen har skapats. Om du vill uppdatera matchningsnycklar måste du skapa en ny dataanslutning.

Tillgängliga matchningsnycklar är:

- **Hash-kodad e-post**

![En arbetsyta för dataanslutningar med avsnittet Matcha nycklar markerat.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Schemaläggning {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Schemaläggning"
>abstract="Visa schemaläggningsinformation för din dataanslutning och redigera uppdateringsfrekvensen om det behövs."

Visa och hantera schemainställningarna för dataanslutningarna. Schemaläggningen bestämmer hur ofta målgruppen uppdateras.

När en dataanslutning har skapats kan du uppdatera uppdateringsfrekvensen direkt från avsnittet **[!UICONTROL Scheduling]** på arbetsytan för dataanslutning.

>[!NOTE]
>
>När ni hämtar målgrupper från Adobe Experience Platform blir målgrupperna tillgängliga inom 24 timmar efter det att dataanslutningen har upprättats. Efter den första importen uppdateras målgruppsdata enligt den angivna frekvensen.

Mer information om schemaläggning finns i avsnittet [schemaläggning](/help/guide/setup/onboard-audiences.md#schedule) i guiden för att konfigurera målgrupper.

![En dataanslutnings arbetsyta med avsnittet Schemaläggning markerat.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

#### Redigera schemaläggning {#edit-scheduling}

Du kan redigera frekvensen för en befintlig dataanslutning för att bättre kontrollera hur ofta målgrupperna uppdateras. Om du vill redigera schemat väljer du **[!UICONTROL Edit]** i dataanslutningen på schemaläggningskortet.

I dialogrutan **[!UICONTROL Scheduling]** väljer du listrutan för att uppdatera **[!UICONTROL Frequency]**. Ställ in uppdateringsfrekvensen så att den körs dagligen eller varannan till var sjätte dag. När du är klar väljer du **[!UICONTROL Save]** för att tillämpa ändringarna.

![Dialogrutan Schemaläggning innehåller alternativ för att ange frekvens och datumintervall.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

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
