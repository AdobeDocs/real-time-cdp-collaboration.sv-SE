---
title: Aktivera målgrupper
description: Lär dig aktivera målgrupper i Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Aktivera målgrupper

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Activate]** är bara tillgänglig om **målgruppsaktiveringen** aktiverades [ under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

Med målgruppsaktivering kan ni aktivera målgrupper för användning i kampanjer. Aktivering kan utföras av någon av medarbetarna beroende på målgruppens aktiveringsinställningar [som har konfigurerats i anslutningen](/help/guide/connect/establishing-connections.md#configure-connection-settings). När du [har identifierat de bästa målgrupperna för din kampanj](./discover.md) aktiverar du målgrupperna så att de blir tillgängliga för användning. När du aktiverar en målgrupp skickas den till medarbetarens förkonfigurerade mål, som Adobe Experience Platform, där den blir tillgänglig för användning i kampanjer. Mer information om hur du ställer in mål finns i guiden [Målöversikt](../destinations/overview.md).

## Aktivera nya målgrupper {#activate-new-audiences}

Om du vill aktivera målgrupper går du till fliken **[!UICONTROL Activate]** på projektarbetsytan.

>[!IMPORTANT]
>
>**Innan** du kan aktivera en målgrupp måste **din medarbetare** konfigurera ett mål. När du aktiverar en målgrupp skickas den automatiskt till medarbetarens konfigurerade mål. Om inget mål har konfigurerats kan du inte aktivera målgrupper.
>
>![Arbetsytan Aktivera när medarbetaren inte har något konfigurerat mål.](/help/assets/collaborate/activate/no-destination-configured.png)

Välj ikonen Lägg till (![ikonen Lägg till).](/help/assets/icons/plus.png)) eller alternativet **[!UICONTROL Activate audience]** om inga tidigare målgrupper har skickats för aktivering.

![Arbetsytan Aktivera i ett projekt utan tillagda målgrupper.](/help/assets/collaborate/activate/activate-new-audiences.png)

Arbetsflödet för att aktivera målgrupper öppnas, där du kan välja vilken målgrupp du vill skicka till din medarbetare. Använd listrutan för att välja en målgrupp eller söka efter en viss målgrupp. Om du vill visa mer information om målgrupperna innan du väljer **[!UICONTROL Browse audiences]**

![Arbetsflödet för målgruppsaktivering med alternativen för listrutor och målgrupper markerade.](/help/assets/collaborate/activate/audience-activation.png)

I **[!UICONTROL Browse audiences]** kan du se **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]** och **[!UICONTROL Overlap %]** för varje publik.

![Dialogrutan Bläddra bland målgrupper visar tillgängliga målgrupper.](/help/assets/collaborate/activate/browse-audiences.png)

Välj den målgrupp som du vill aktivera i kampanjer och välj sedan **[!UICONTROL Save]**. Publiken visas nu och du kan se **[!UICONTROL Identity count]**, **[!UICONTROL Overlapping identities]** och **[!UICONTROL Overlap %]** för den valda publiken.

![Arbetsflödet för målgruppsaktivering med den valda målgruppen visas.](/help/assets/collaborate/activate/audience-selected.png)

### Redigera matchningsnycklar {#edit-match-keys}

Därefter kan du redigera målgruppens matchningsnycklar genom att välja **[!UICONTROL Edit match keys]** inom den valda målgruppen. De här alternativen ärvs från dina val av matchningsnycklar när anslutningen mellan medarbetarna först konfigurerades. Du kan ta bort matchningsnycklar som har valts om de inte gäller för en viss kampanj, men du kan inte lägga till nya matchningsnycklar.

![Arbetsflödet för målgruppsaktivering med alternativet Redigera matchningsnycklar markerat.](/help/assets/collaborate/activate/edit-match-keys.png)

Dialogrutan **[!UICONTROL Edit match keys]** öppnas, där du kan inaktivera matchningsnycklarna som du inte vill använda. Välj **[!UICONTROL Save]** om du vill spara ändringarna.

>[!NOTE]
>
>Minst en matchningsnyckel måste väljas. I den aktuella versionen är den enda matchande nyckeln **[!UICONTROL Hashed email]**, så du kan inte ta bort den här matchningsnyckeln.

![Dialogrutan Redigera matchningsnycklar i Audiece-aktiveringsarbetsflödet.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Ange uppdateringsfrekvens för målgruppen {#set-audience-refresh-frequency}

Ange slutligen önskad frekvens och datumintervall för att publiken ska uppdatera. I den aktuella versionen är det enda frekvensalternativ som stöds **[!UICONTROL Once]**. Frekvensen **[!UICONTROL Once]** innebär att målgrupperna aktiveras en gång och inte uppdateras. Alternativet **[!UICONTROL Date]** fylls i automatiskt med aktuellt datum.

![Arbetsflödet för målgruppsaktivering med avsnittet Frekvens markerat.](/help/assets/collaborate/activate/audience-frequency.png)

När du är nöjd med dina val väljer du **[!UICONTROL Activate]** för att slutföra arbetsflödet.

## Aktivera instrumentpanel {#activate-dashboard}

På fliken **[!UICONTROL Activate]** kan du visa alla målgrupper som har skickats till din medarbetare, samt alla målgrupper som din medarbetare har aktiverat till ditt mål.

![Kontrollpanelen Aktivera som visar avsnitten Skickade målgrupper och Aktiverade målgrupper.](/help/assets/collaborate/activate/activate-dashboard.png)

## Visa skickade målgrupper {#view-sent-audiences}

I avsnittet för **[!UICONTROL Sent audiences to]**-medarbetare visas alla målgrupper som du har skickat. För närvarande skickas målgrupper automatiskt till medarbetarens konfigurerade mål när du har skickat dem. I din medarbetares vy visas dessa målgrupper i avsnittet **[!UICONTROL Activated audiences]**.

Inom varje sänd publik kan du se följande mätvärden:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Name]** | Namnet på publiken. |
| **[!UICONTROL Status]** | Status för den skickade målgruppen. |
| **[!UICONTROL Identity count]** | Antalet identiteter i publiken. |
| **[!UICONTROL Overlapping identities]** | Antalet överlappande identiteter mellan den här målgruppen och den totala populationen profiler i medarbetarens lager. |
| **[!UICONTROL Created]** | Det datum då målgruppen ursprungligen skickades. |
| **[!UICONTROL Last sent]** | Det datum då målgruppen senast skickades till din medarbetare. |
| **[!UICONTROL Match keys]** | Anger den matchningsnyckel som används för målgruppen. |

## Visa aktiverade målgrupper {#view-activated-audiences}

I avsnittet **[!UICONTROL Activated audiences]** kan du se alla målgrupper som har aktiverats för ditt mål.

Inom varje aktiverad målgrupp kan du se följande mätvärden:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Name]** | Namnet på publiken. |
| **[!UICONTROL Status]** | Status för den aktiverade målgruppen. |
| **[!UICONTROL Identity count]** | Antalet identiteter som aktiverades, baserat på de överlappande identiteterna när medarbetaren skickade målgruppen. |
| **[!UICONTROL Created]** | Datumet då målgruppen aktiverades. |
| **[!UICONTROL Last refreshed]** | Det datum då målgruppen senast uppdaterades, baserat på det uppdateringsschema som valdes under aktiveringen. |
| **[!UICONTROL Destination]** | Målet dit målgruppen aktiverades. |
| **[!UICONTROL Match keys]** | Anger den matchningsnyckel som används för målgruppen. |

## Ta bort skickade målgrupper {#delete-sent-audiences}

Du kan ta bort skickade målgrupper som du inte längre vill aktivera. När du tar bort en skickad målgrupp tas den bort från avsnittet **[!UICONTROL Sent audiences to]** och aktiveras inte längre till din medarbetares mål.

Om du vill ta bort en skickad målgrupp väljer du ikonen **[!UICONTROL Delete]** (![Ta bort.](/help/assets/icons/delete.png)) bredvid målgruppen i avsnittet **[!UICONTROL Sent audiences to]**.

![Alternativet Ta bort i avsnittet Skickade målgrupper till.](/help/assets/collaborate/activate/delete-sent-audiences.png)

En bekräftelsedialogruta öppnas där du ombeds bekräfta borttagningen. Bekräfta genom att välja **[!UICONTROL Delete]**.

![Bekräftelsedialogrutan för borttagning.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## Nästa steg {#next-steps}

När du har aktiverat målgrupper och kört kampanjer kan du tillsammans med Adobe aktiverings- och ingenjörsteam överföra mätdata och visa motsvarande [mätrapporter](/help/guide/collaborate/measure.md).
