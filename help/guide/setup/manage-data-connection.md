---
title: Hantera dataanslutningar
description: Lär dig hantera dataanslutningar, inklusive matchningsnycklar, schemaläggning, användningsfall och målgruppsfiltrering i Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: 8d620828bb0fb0bf116396f884b1bbd35d7c5d69
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Hantera dataanslutningar

{{limited-availability-release-note}}

## Översikt

Använd dataanslutningar i Real-Time CDP Collaboration för att importera målgrupper från olika källor. Lär dig hur du hanterar matchningsnycklar och schemalägger dataimport för dina befintliga dataanslutningar. Dessutom kan ni filtrera målgrupperna utifrån olika attribut för mer detaljerade insikter.

## Visa dataanslutningar

Om du vill visa befintliga dataanslutningar går du till **[!UICONTROL Setup]** och väljer fliken **[!UICONTROL My data connections]**. Alla dina aktuella dataanslutningar visas med en kort översikt för varje anslutning. Om du vill visa information om en dataanslutning, inklusive matchningsnycklar, schemaläggningsinformation och målgrupper, väljer du **[!UICONTROL View data connection]** på motsvarande anslutning.

![Arbetsytan Konfigurera med flikvyn Mina dataanslutningar visas och markeras.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Matcha nycklar {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Matcha nycklar"
>abstract="Matchningsnycklar avgör hur data från olika källor matchas. Välj de matchande nycklar som är mest relevanta för dina användningsfall och sekretesspolicyer."

Matchningsnycklar är identifierare som används för att stämma av medlemmar mellan olika målgrupper från olika datakällor. Du kan inte redigera de matchningsnycklar som du ursprungligen valde för din dataanslutning.

Tillgängliga matchningsnycklar är:

- **Hash-kodad e-post**

![En arbetsyta för dataanslutningar med avsnittet Matcha nycklar markerat.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Schemaläggning {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Schemaläggning"
>abstract="I den här vyn visas de schemaläggningsalternativ som du valde från början för din dataanslutning."

Du kan inte redigera de schemaläggningsalternativ som du valde från början för din dataanslutning. Mer information om schemaläggningsalternativ finns i avsnittet [schemaläggning](/help/guide/setup/onboard-audiences.md#schedule) i arbetsflödesdokumentet för målgruppsimport.

![En arbetsyta för dataanslutningar med avsnittet Schemaläggning markerat.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Ta bort dataanslutning

Om du tar bort en dataanslutning tas alla underliggande målgrupper, associerade inställningar och användning bort på plattformen. Det går inte att ångra den här åtgärden.

Om du vill ta bort en befintlig dataanslutning markerar du ikonen Ta bort (![ikonen Ta bort](/help/assets/common/delete.svg)) på en enskild dataanslutnings arbetsyta.

![En arbetsyta för dataanslutningar med borttagningsalternativet markerat.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

En bekräftelsedialogruta visas. Välj **[!UICONTROL Delete]** om du vill ta bort dataanslutningen.

![Dialogrutan Ta bort dataanslutning med alternativet Ta bort markerat.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Hantera målgrupper {#manage-audiences}

En lista över målgrupper som är kopplade till dataanslutningen visas längst ned på arbetsytan. I listan visas en kort översikt över varje målgrupp, inklusive dess status, källa och anslutningsåtkomst. Om du vill redigera en målgrupps kategorier, anslutningsåtkomst eller metadatavisbarhet markerar du målgruppens namn. En fullständig guide om hur du hanterar en målgrupp finns i guiden [Visa enskilda målgrupper](./onboard-audiences.md#view-individual-audiences).

![En arbetsyta för dataanslutningar med målgrupperna markerade.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Nästa steg

När du har hanterat dina dataanslutningar kan du [identifiera överlappningar](/help/guide/collaborate/discover.md) mellan dina målgrupper och de målgrupper som din medarbetare har gjort identifierbara.
