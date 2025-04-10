---
title: Dela målgrupper
description: Lär dig dela målgrupper med dina samarbetspartners för annonskampanjer.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0fdf0598-89c9-452d-a2e3-ce868df0b9d2
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# Dela målgrupper

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Share]** är bara tillgänglig om **målgruppsdelning och aktivering** har aktiverats [ under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

Som annonsörer kan du lära dig att dela målgrupper med utgivare så att de kan köra kampanjer. Om ditt samarbete har aktiverat **Identifiera målgrupper** kan du börja med att köra överlappningsrapporter på fliken [Identifiera](/help/guide/collaborate/discover.md) för att identifiera de bästa målgrupperna för delning.

## Dela nya målgrupper

Om du vill börja dela målgrupper går du till fliken **[!UICONTROL Share]** på projektarbetsytan. Endast **annonsörorganisationer** kan dela målgrupper för kampanjer. På den här fliken kan du granska och hantera delade målgrupper.

**Välj plustecknet (+),** eller alternativet **[!UICONTROL Share audience]** om inga tidigare målgrupper har delats, för att starta målgruppsdelningsprocessen.

![Standardvy utan delade målgrupper.](/help/assets/collaborate/share/share-new-audiences.png)

En ny panel visas där du kan välja vilka målgrupper du vill dela med din medarbetare.

![Dela nytt målgruppsarbetsflöde.](/help/assets/collaborate/share/share-audiences-workflow.png)

### Välj målgrupper att dela

I fönstret för val av målgrupp kan du söka efter specifika målgrupper att dela genom att ange målgruppens namn i sökfältet. Välj **[!UICONTROL Browse audiences]** och använd de tillgängliga sorteringsalternativen för att hitta exakt de målgrupper du behöver.

![Bläddra i målgruppsvyn med valda målgrupper.](/help/assets/collaborate/share/browse-audiences-view.png)

### Redigera matchningsnycklar och ange inriktningsalternativ

När du har valt önskade målgrupper att dela kan du nu välja andra konfigurationsalternativ för delningsaktiviteten.

![Redigera matchningsnycklar och mål- eller undertrycksväljare markerade](/help/assets/collaborate/share/match-keys-and-targeting.png)

Välj **[!UICONTROL Edit match keys]** för att ange vilka matchningsnycklar som ska användas för identiteterna i målgruppen. De här alternativen ärvs från de inställningar som valdes när anslutningen mellan medarbetare först konfigurerades. Du kan ta bort matchningsnycklar som har valts vid den tidpunkten om de inte gäller för den här specifika kampanjen, men du kan inte lägga till nya matchningsnycklar just nu.

![Redigera matchningsnycklar.](/help/assets/collaborate/share/update-match-keys.png)

För varje målgrupp väljer du om du vill att medlemmarna i målgruppen ska vara riktade eller undertryckta i kampanjen. Undertryckta profiler kommer specifikt inte att vara en del av den målgrupp som aktiveras av utgivaren.

### Ange uppdateringsfrekvens och intervall för målgruppen

Ange slutligen önskad frekvens och datumintervall för målgruppens uppdatering. De lägen som stöds för målgruppsuppdatering är **[!UICONTROL Once]** och **[!UICONTROL Daily]**.

När du väljer **[!UICONTROL Once]** uppdateras inte målgruppsmedlemskapet under en kampanjtid. När du väljer **[!UICONTROL Daily]** uppdateras målgruppsmedlemskapet en gång om dagen under en kampanjtid.

![Frekvensalternativen är markerade.](/help/assets/collaborate/share/audience-refresh-frequency.png)

När du är nöjd med dina val väljer du **[!UICONTROL Share]** för att slutföra arbetsflödet.

>[!SUCCESS]
>
>Du kan nu se en ny målgruppsdelningsaktivitet på fliken **[!UICONTROL Sharing]** . Om du vill kan du gå tillbaka och redigera något av de val du har gjort.

## Visa målgrupper som för närvarande delas

På fliken **[!UICONTROL Sharing]** kan du visa de målgrupper som för närvarande delas mellan medarbetarna, grupperade tillsammans i målgruppsdelningsaktiviteter.

![Översikt över delningsfliken.](/help/assets/collaborate/share/share-tab-overview.png)

<!--

The banner at the top of the page shows figures across all audience sharing activities. 

![The hero banner in the sharing tab.](/help/assets/collaborate/share/share-hero-banner.png)


|Metric | Description |
|---------|----------|
| **[!UICONTROL Shared audiences]** | Indicates the number of audiences shared between collaborators in this project, across all audience sharing modules. |
| **[!UICONTROL Estimated addressable reach]** | Indicates the approximate number of profiles that you can reach across all the audiences that are currently shared in the project. [TODO: ADD INFORMATION ABOUT HOW THIS IS CALCULATED] |
| **[!UICONTROL Target identities]** | The number of identities across all audiences shared in this project for which you selected to target the profiles. |
| **[!UICONTROL Suppress identities]** | The number of identities across all audiences shared in this project for which you selected to suppress the profiles and thereby not target them in campaigns. |

-->

Inom varje målgruppsdelningsaktivitet kan ni få information om varje delad målgrupp.

| Metrisk | Beskrivning |
|---------|----------|
| **[!UICONTROL Identity count]** | Anger antalet profiler för alla identiteter som är knutna till den här målgruppen, enligt den senaste utvärderingen av antalet identiteter. Dessa siffror uppdateras var 24:e timme. |
| **[!UICONTROL Overlapping identities]** | Anger antalet överlappande identiteter mellan medlemmarna i den här målgruppen och den totala populationen av profiler i medarbetarens inventering. |
| **[!UICONTROL Match key breakdown]** | Visar antalet identiteter för varje identitet som används i målgruppen. Till exempel kan ett totalt identitetsantal på 500 000 användare bestå av 400 000 användare som har en nyckel av den hash-kodade e-postidentiteten och 100 000 användare som har en mobil-ID-identitet. Observera att i det exempel som beskrivs här kan samma person vara närvarande två gånger i målgruppen med sina e-post- och mobil-ID-identiteter. |
| **[!UICONTROL Objective]** | **[!UICONTROL Suppress]** eller **[!UICONTROL Target]**. Anger om en målgrupps medlemmar ska målgruppsanpassas eller uteslutas från kampanjer. |

Sidan innehåller även kontroller för dig till **[!UICONTROL Pause sharing]** och **[!UICONTROL Edit audiences]**.

## Redigera målgrupper {#edit-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_share_edit_audiences_usecases"
>title="Rikta in eller ignorera användningsfall"
>abstract="<p>Välj **Mål** om du vill att profilerna i målgruppen ska visas annonser i kampanjen.</p> <p>Välj **Suppress** om du vill utesluta profilerna i målgruppen från kampanjmeddelandena.</p>"

Välj **[!UICONTROL Edit audiences]** om du vill ändra vilka målgrupper som delas i en målgruppsdelningsmodul samt ändra flera konfigurationer som är relaterade till hur målgrupper delas.

![Vy över redigeringsgrupper modal](/help/assets/collaborate/share/edit-audiences-modal.png)

<!--

Search for audiences that you want to add to the sharing module. 

For each audience, you can select whether you'd like to target or suppress those profiles in campaigns. 

To remove an audience from the sharing module, select the trash can icon [TODO: add spectrum icon and folder].

Select how often you would like the audience membership to be refreshed and the date range within which you want the membership of the audience to be refreshed. 

TODO: are there any limitations for frequency in the M1 release?

-->

## Nästa steg

När utgivaren har tagit emot de delade målgrupperna [aktiverar](/help/guide/collaborate/activate.md) dem nu i digitala annonskampanjer.
