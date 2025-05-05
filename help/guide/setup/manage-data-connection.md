---
title: Hantera dataanslutningar
description: Lär dig hantera dataanslutningar, inklusive matchningsnycklar, schemaläggning, användningsfall och målgruppsfiltrering i Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Hantera dataanslutningar

{{limited-availability-release-note}}

## Översikt

Använd dataanslutningar i Real-Time CDP Collaboration för att importera målgrupper från olika källor. Lär dig hur du hanterar matchningsnycklar och schemalägger dataimport för dina befintliga dataanslutningar. Dessutom kan ni filtrera målgrupperna utifrån olika attribut för mer detaljerade insikter.

Innan du hanterar dina dataanslutningar här bör du först konfigurera dem under [målgruppsarbetsflödet för onboarding](./onboard-audiences.md). Detta säkerställer att rätt datakällor är anslutna för användning i Real-Time CDP Collaboration.

## Visa dataanslutningar

>[!IMPORTANT]
>
>Det går inte att ta bort en dataanslutning i Real-Time CDP Collaboration användargränssnitt. Om du vill ta bort en dataanslutning kontaktar du Adobe eller [skapar en kundsupportanmälan](https://experienceleague.adobe.com/home?lang=sv-SE&amp;support-tab=open-ticket#support){target="_blank"}.

Om du vill visa befintliga dataanslutningar går du till **[!UICONTROL Setup]** > **[!UICONTROL My audiences]** och väljer **[!UICONTROL Manage data connections]**.

![Konfigurera arbetsyta med Hantera dataanslutningar markerat.](/help/assets/setup/manage-data-connection/manage-data-connection-highlighted.png){zoomable="yes"}

Detta ger en översikt över alla era nuvarande dataanslutningar, med information om antalet målgrupper i var och en av dem, datakällan för dataanslutningen med mera. Välj **[!UICONTROL View data connection]** om du vill visa information om matchningsnycklar, schemaläggning och målgrupper som är en del av den här dataanslutningen.

![Hantera dataanslutningar med anslutningar Visa dataanslutningar markerade. ](/help/assets/setup/manage-data-connection/view-data-connection-highlighted.png){zoomable="yes"}

### Matcha nycklar {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Matcha nycklar"
>abstract="Matchningsnycklar avgör hur data från olika källor matchas. Välj de matchande nycklar som är mest relevanta för dina användningsfall och sekretesspolicyer."

Matchningsnycklar är identifierare som används för att stämma av medlemmar mellan olika målgrupper från olika datakällor. Tillgängliga matchningsnycklar är:

- **Hash-kodad e-post**

Du kan inte redigera matchningsnycklarna som används i den här dataanslutningen.

![En arbetsyta för dataanslutningar med avsnittet Matcha nycklar markerat.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Schemaläggning {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Schemaläggning"
>abstract="I den här vyn visas de schemaläggningsalternativ som du valde från början för din dataanslutning."

Du kan inte redigera de schemaläggningsalternativ som du valde från början för din dataanslutning. Mer information om schemaläggningsalternativ finns i avsnittet [schemaläggning](/help/guide/setup/onboard-audiences.md#schedule) i arbetsflödesdokumentet för målgruppsimport.

![En arbetsyta för dataanslutningar med avsnittet Schemaläggning markerat.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Hantera målgrupper {#manage-audiences}

När du visar en lista över målgrupper från din dataanslutning kan du välja att visa målgrupperna, redigera deras kategorier eller ta bort dem från dataanslutningen.

![En arbetsyta för dataanslutningar med målgrupperna markerade.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Nästa steg

När du har hanterat dina dataanslutningar kan du [identifiera överlappningar](/help/guide/collaborate/discover.md) mellan dina målgrupper och de målgrupper som din medarbetare har gjort identifierbara.
