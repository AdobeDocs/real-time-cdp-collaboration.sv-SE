---
title: Skapa och hantera projekt
description: Lär dig skapa och hantera projekt i Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: ae492846-bc0a-4422-86ca-577bcc1fa60c
source-git-commit: 0cf888e36ffc4730fc8de4d8adccae0e0fc2caa8
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# Skapa och hantera projekt

{{limited-availability-release-note}}

Projekt är central i ditt arbetsflöde i Adobe Real-Time CDP Collaboration. Efter att ha anslutit till medarbetare kan du skapa ett projekt för att köra målgruppsöverlappningsberäkningar och identifiera relevanta målgrupper för kampanjer.

>[!TIP]
>
>Projekt bör i allmänhet vara kopplade till en enda kampanj.

![Kontrollpanelen Samarbeta visar alla aktuella projekt.](/help/assets/collaborate/manage-view-projects/projects-overview-page.png){zoomable="yes"}

Du kan bara använda filter för att visa projekt som du har startat med vissa medarbetare, vilket visas nedan:

![Filtrerad vy över projekt med en medarbetare.](/help/assets/collaborate/manage-view-projects/filtered-project-view.png){zoomable="yes"}

## Skapa projekt {#create-project}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_create_project_advertisername_amc"
>title="Advertiser name (Amazon Marketing Cloud)"
>abstract="För Amazon Marketing Cloud-anslutningar (AMC) representerar det här fältet den AMC-instans som din Amazon Ads-inloggning har åtkomst till. Det återspeglar inte ett annonsörsnamn. Om den begärda instansen inte finns med i listan kontaktar du Amazon Marketing Cloud-administratören och begär åtkomst."

Om du vill skapa ett projekt måste du först [upprätta en anslutning](/help/guide/connect/establishing-connections.md) med en medarbetare. När anslutningen har upprättats kan du skapa ett projekt med den medarbetaren.

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_projects_advertisername"
>title="Advertiser-namn"
>abstract="Välj annonsörens namn i listrutan. Alternativen är förkonfigurerade av utgivaren i anslutningsinställningarna för att säkerställa kompatibilitet med deras system."

Navigera till **[!UICONTROL Collaborate]** och sedan till **[!UICONTROL My Projects]**. Om det här är ditt första projekt kan du välja **[!UICONTROL Create a project]**. Annars kan du välja ikonen Lägg till (![ikonen Lägg till.](/help/assets/icons/plus.png)) när du vill skapa ett nytt projekt.

![Välj plustecken eller Skapa ett projekt för att konfigurera ett nytt projekt.](/help/assets/collaborate/manage-view-projects/create-project.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Create project]** visas. Välj **[!UICONTROL Collaborator]** som du skapar projektet med via listrutan. Om du är utgivare och anger annonsörnamn under anslutningsinställningarna kan du välja **[!UICONTROL Advertiser name]**.

>[!NOTE]
>
> Om du konfigurerade ett annonsörsnamn i anslutningsinställningarna visas det som standard. Om inget annonsörnamn har ställts in är annonsörens **[!UICONTROL Name]** förmarkerat som **[!UICONTROL Advertiser name]**.

![Skapa projektdialogruta med medarbetare markerad och annonsörens namn markerat.](/help/assets/collaborate/manage-view-projects/create-project-advertiser-names.png){zoomable="yes"}

Lägg sedan till **[!UICONTROL Project name]** och **[!UICONTROL Description]** för ditt projekt. Välj sedan en bild som ska representera projektet. Den här bilden hjälper till att skilja på projektet på sidan med projektöversikten. När du är klar väljer du **[!UICONTROL Create]** för att skapa projektet.

![Obligatoriska alternativ för att konfigurera ett nytt projekt](/help/assets/collaborate/manage-view-projects/create-project-required-info.png){zoomable="yes"}

Du kan nu visa ditt nya projekt, dess information och tillgängliga avsnitt baserat på de användningsfall som valts under anslutningskonfigurationen.

![Arbetsytan för projektöversikt.](/help/assets/collaborate/manage-view-projects/project-overview.png){zoomable="yes"}

## Hantera kampanj-ID {#manage-campaign-id}

Ett **kampanj-ID** länkar ditt projekt till en viss kampanj och krävs för att [generera mätrapporter](./measure.md#create-measurement-report). Du kan lägga till flera kampanj-ID:n i ett projekt om du kör flera kampanjer tillsammans med samma medarbetare. Alla dessa kampanjer kan väljas ut vid rapportering.

- **Utgivare**: Ange eller uppdatera kampanj-ID:n och associerade namn i Collaboration-gränssnittet innan du kör rapporter.
- **Annonsörer**: Begär att din samarbetspartner (utgivare) lägger till kampanj-ID efter behov.

Om du vill lägga till eller uppdatera kampanj-ID:n går du till arbetsytan **[!UICONTROL Collaborate]** och väljer **[!UICONTROL View]** i det aktuella projektkortet.

![Arbetsytan Samarbeta markerar alternativet Visa på ett projektkort.](/help/assets/collaborate/manage-view-projects/view-project.png){zoomable="yes"}

Motsvarande **[!UICONTROL Project overview]**-arbetsyta visas med ett **[!UICONTROL Campaign ID and name]**-avsnitt som visar alla kampanjer som är kopplade till projektet. Om du inte har lagt till någon kampanj än väljer du **[!UICONTROL Add]**. Om det redan finns kampanjer väljer du **[!UICONTROL Edit]** om du vill uppdatera informationen eller lägga till fler.

![Arbetsytan för projektöversikt som visar avsnittet Kampanj-ID och namn med alternativet Redigera markerat.](/help/assets/collaborate/manage-view-projects/edit-campaign-id.png){zoomable="yes"}

I dialogrutan **[!UICONTROL Campaign ID and name]** väljer du **[!UICONTROL Add campaign ID]** för att lägga till en ny rad där du kan ange kampanjinformation.

![Dialogrutan för kampanj-ID och namn visar den tomma kampanjraden efter att du har valt alternativet Lägg till kampanj-ID.](/help/assets/collaborate/manage-view-projects/add-campaign-row.png){zoomable="yes"}

Ange **[!UICONTROL Campaign ID]** och **[!UICONTROL Campaign name]** och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Kampanj-ID och namn med den nya kampanjinformationen och alternativet Spara markerat.](/help/assets/collaborate/manage-view-projects/save-campaign-id.png){zoomable="yes"}

Gå till avsnittet **[!UICONTROL Campaign ID and name]** för att visa dina senaste kampanjer och senaste ändringar. Nu kan du använda de nya kampanj-ID:n för att generera mätningsrapporter.

![Arbetsytan för projektöversikt som visar det uppdaterade avsnittet för kampanj-ID och namn.](/help/assets/collaborate/manage-view-projects/view-updated-campaigns.png){zoomable="yes"}
