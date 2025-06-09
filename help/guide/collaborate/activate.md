---
title: Aktivera målgrupper
description: Lär dig aktivera målgrupper i Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Aktivera målgrupper

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Activate]** är bara tillgänglig om **målgruppsaktiveringen** aktiverades [ under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

Med målgruppsaktivering kan ni aktivera målgrupper i kampanjer. Aktivitetsprocessen är ett samarbete mellan annonsörer och utgivare. När [har identifierat de bästa målgrupperna för din kampanj](./discover.md) kan målgrupperna sedan aktivera målgrupperna. Publikationer som aktiveras skickas till utgivarens förkonfigurerade mål, t.ex. Adobe Experience Platform, för användning i kampanjer. Mer information om hur du ställer in destinationen finns i guiden [Målöversikt](../destinations/overview.md).

>[!IMPORTANT]
>
>När annonsörer aktiverar målgrupper aktiveras de automatiskt till det mål som utgivaren har konfigurerat för sin organisation. Utgivaren **måste** konfigurera ett mål *innan* annonsören aktiverar en målgrupp. Om inget mål har konfigurerats skickas målgruppen till utgivaren, men kan inte aktiveras i några kampanjer.

## Aktivera nya målgrupper

Om du vill aktivera målgrupper går du till fliken **[!UICONTROL Activate]** på projektarbetsytan.

Välj ikonen Lägg till (![ikonen Lägg till).](/help/assets/icons/plus.png)) eller alternativet **[!UICONTROL Activate audience]** om inga tidigare målgrupper har skickats för aktivering.

![Arbetsytan Aktivera i ett projekt utan tillagda målgrupper.](/help/assets/collaborate/activate/activate-new-audiences.png)

Arbetsflödet för att aktivera målgrupper öppnas, där du kan välja vilken målgrupp du vill skicka till din medarbetare. Använd listrutan för att välja en målgrupp eller söka efter en viss målgrupp. Om du vill visa mer information om målgrupperna innan du väljer **[!UICONTROL Browse audiences]**

![Arbetsflödet för målgruppsaktivering med alternativen för listrutor och målgrupper markerade.](/help/assets/collaborate/activate/audience-activation.png)

I **[!UICONTROL Browse audiences]** kan du se **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]** och **[!UICONTROL Overlap %]** för varje publik.

![Dialogrutan Bläddra bland målgrupper visar tillgängliga målgrupper.](/help/assets/collaborate/activate/browse-audiences.png)

Välj den målgrupp som du vill aktivera i kampanjer och välj sedan **[!UICONTROL Save]**. Publiken visas nu och du kan se **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]** och **[!UICONTROL Overlap %]** för den valda publiken.

![Arbetsflödet för målgruppsaktivering med den valda målgruppen visas.](/help/assets/collaborate/activate/audience-selected.png)

### Redigera matchningsnycklar

Därefter kan du redigera målgruppens matchningsnycklar genom att välja **[!UICONTROL Edit match keys]** inom den valda målgruppen. De här alternativen ärvs från dina val av matchningsnycklar när anslutningen mellan medarbetarna först konfigurerades. Du kan ta bort matchningsnycklar som har valts om de inte gäller för en viss kampanj, men du kan inte lägga till nya matchningsnycklar.

![Arbetsflödet för målgruppsaktivering med alternativet Redigera matchningsnycklar markerat.](/help/assets/collaborate/activate/edit-match-keys.png)

Dialogrutan **[!UICONTROL Edit match keys]** öppnas, där du kan inaktivera matchningsnycklarna som du inte vill använda. Välj **[!UICONTROL Save]** om du vill spara ändringarna.

>[!NOTE]
>
>Minst en matchningsnyckel måste väljas. I den aktuella versionen är den enda matchande nyckeln **[!UICONTROL Hashed email]**, så du kan inte ta bort den här matchningsnyckeln.

![Dialogrutan Redigera matchningsnycklar i Audiece-aktiveringsarbetsflödet.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Ange uppdateringsfrekvens och intervall för målgruppen

Ange slutligen önskad frekvens och datumintervall för att publiken ska uppdatera. I den aktuella versionen är det enda frekvensalternativ som stöds **[!UICONTROL Once]**. Frekvensen **[!UICONTROL Once]** innebär att målgrupperna aktiveras en gång och inte uppdateras. Alternativet **[!UICONTROL Date]** fylls i automatiskt med aktuellt datum.

![Arbetsflödet för målgruppsaktivering med avsnittet Frekvens markerat.](/help/assets/collaborate/activate/audience-frequency.png)

När du är nöjd med dina val väljer du **[!UICONTROL Activate]** för att slutföra arbetsflödet. Publiken är nu aktiverad och du kan visa den på fliken **[!UICONTROL Activate]**. Den kommer också att vara tillgänglig för din medarbetare på fliken **[!UICONTROL Activate]** där de kan använda den i kampanjer.

Du kan redigera publikens ikon för namnredigering (![Pennikon.](/help/assets/icons/edit.png)) eller inaktivera målgruppen genom att välja **[!UICONTROL Deactivate]**.

![Fliken Aktivera där den aktiva målgruppen visas och alternativen Redigera och Inaktivera är markerade.](/help/assets/collaborate/activate/edit-activate-audience.png)

## Visa aktiverade målgrupper

På fliken **[!UICONTROL Activate]** kan både utgivare och annonsörer visa de målgrupper som är aktiverade. För närvarande skickas målgrupper automatiskt till utgivarens konfigurerade mål när annonsören aktiverar dem.

![Översikt över fliken Aktivera och visar en aktiverad målgrupp.](/help/assets/collaborate/activate/activate-overview.png)

Inom varje aktiverad målgrupp kan du se följande mätvärden:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Activated identities]** | Anger antalet aktiverade identiteter inom målgruppen. |
| **[!UICONTROL Overlapping identities]** | Anger antalet överlappande identiteter mellan den här målgruppen och den totala populationen profiler i medarbetarens lager. |
| **[!UICONTROL Match key breakdown]** | Visar antalet identiteter för varje identitet som används i målgruppen. Ett totalt antal identiteter för 500 kB-användare kan till exempel bestå av 400 kB-användare som har inaktiverat den hashas-e-postidentiteten och 100 kB-användare som har inaktiverat en mobil-ID. Observera att i det exempel som beskrivs här kan samma person vara närvarande två gånger i målgruppen med sina e-post- och mobil-ID-identiteter. |

## Nästa steg {#next-steps}

När du har aktiverat data och kört kampanjer kan du arbeta med Adobe aktiverings- och ingenjörsteam för att överföra mätdata och visa motsvarande [mätrapporter](/help/guide/collaborate/measure.md).
