---
title: Kommunicera med annonsörer eller utgivare
description: Lär dig hur du skapar kopplingar och börjar samarbeta i projekt när du har upptäckt potentiella medarbetare.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: 81cedb2a06d930734b1f97304de82d450c06bf79
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Kommunicera med annonsörer eller utgivare

{{limited-availability-release-note}}

Att upprätta en förbindelse mellan två parter i ett samarbete (vanligen en annonsörer och en utgivare) är en förutsättning i Real-Time CDP Collaboration för att företag ska kunna samarbeta i kampanjer. Både utgivare och annonsörer kan skapa anslutningar. Den part som initierar anslutningen blir sedan *anslutningsägaren*.

## Arbetsflöde på hög nivå

På en hög nivå ser arbetsflödet ut så här för att upprätta en anslutning mellan en annonsörer och en utgivare:

1. Annonsören [bläddrar bland utgivare och upptäcker](/help/guide/connect/discover-publishers.md) som de vill arbeta med
2. Annonsören skickar en anslutningsinbjudan.
3. Utgivaren accepterar inbjudan.
4. Annonsören skickar anslutningsinställningar som bland annat matchar nycklar. De här anslutningsinställningarna representerar produktvillkoren för samarbetet.
5. Utgivaren accepterar anslutningsinställningar. Utgivaren kan vid behov avvisa de ursprungliga anslutningsinställningarna och begära att annonsören skickar ändrade anslutningsinställningar.

![Högnivådiagram över anslutningsprocessen mellan annonser och utgivare.](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png){zoomable="yes"}

När objekten ovan är slutförda kan medarbetarna fortsätta med att [skapa ett projekt](/help/guide/collaborate/manage-projects.md#create-project) för att [köra överlappningsrapporter](/help/guide/collaborate/discover.md) och starta reklamkampanjer.

>[!IMPORTANT]
>
>När anslutningen mellan två medarbetare har upprättats kan anslutningsinställningarna inte ändras längre.

## Skicka inbjudan {#send-invite}

Om du vill konfigurera en anslutning väljer du **[!UICONTROL Connect]** när du bläddrar i utgivarens lager på skärmen Identifieringsutgivare.

![Anslut väljare](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

Nu är inbjudan ute och du kan förhandsgranska anslutningsinställningarna, men inte redigera dem. Du kan visa den väntande inbjudan på fliken **[!UICONTROL My connections]**. Anslutningens status är **[!UICONTROL Invite sent]**.

![Väntande inbjudan har skickats till utgivaren visas i vyn Mina anslutningar.](/help/assets/connect/establish-connection/pending-invite-sent.png){zoomable="yes"}

När medarbetaren godkänt inbjudan kan du konfigurera anslutningsinställningarna och skicka dem till medarbetaren för granskning och godkännande.

## Anslutningsinställningar {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Användningsfall"
>abstract="Användningsexemplen är förifyllda med alla alternativ. Du kan redigera användningsexemplen innan du skickar in anslutningsinställningarna."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Matcha nycklar"
>abstract="Matchningsnycklar är förifyllda med de som du har valt på organisationsnivå. Du kan inaktivera matchningsnycklar som du inte vill använda i den här anslutningen."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="Kreditdelning"
>abstract="I det här avsnittet anges vem som betalar för motsvarande aktiviteter inom Real-Time CDP Collaboration. För närvarande går det bara att konfigurera målgruppsdelning."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Målgruppsdelning"
>abstract="Målgruppsdelning är den aktivitet som en part tar när de begär att matchade data ska aktiveras av deras samarbetspartner."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Rättsligt avtal"
>abstract="Kontrollera att det finns ett datadelningsavtal mellan de två parterna."

När inbjudan har skickats kan du förhandsgranska anslutningsinställningarna. Inbjudan måste accepteras innan du kan slutföra konfigurationen av anslutningen.

![Vyn med anslutningsinställningar i förhandsgranskningsläget.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

När anslutningen har godkänts av din medarbetare kan du nu börja konfigurera anslutningsinställningarna för anslutningen. Anslutningsinställningarna definierar villkoren för ditt samarbete, t.ex. de användningsfall som du ska utföra tillsammans, matchningsnycklar som du ska använda i projekt och mycket annat.

Om du vill konfigurera och dela anslutningsinställningar med din medarbetare går du till **[!UICONTROL My connections]**. För alla anslutningar med statusen **[!UICONTROL Pending]** kan du välja **[!UICONTROL Set up connection]** för att konfigurera anslutningsinställningarna.

![Vyn Mina anslutningar med en väntande anslutning och anslutningsalternativet Konfigurera markeras.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Du kan redigera och definiera fälten nedan:

![Konfigurera anslutningsvy](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Användningsfall

Användningsexempel är förifyllda med alla tillgängliga användningsfall. Du kan välja vilka användningsfall din anslutning ska använda genom att välja **[!UICONTROL Edit]** och stänga av de användningsfall du inte vill använda. De valda användningsfallen påverkar vilka vyer och alternativ som är [tillgängliga i dina projekt](../collaborate/manage-projects.md#project-use-cases).

![Användningsfall](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Matcha tangenter

Matchningsnycklar är förifyllda med de som du [har valt på din organisationsnivå](/help/guide/setup/onboard-organization.md#set-up-match-keys). Du kan inaktivera matchningsnycklar som du inte vill använda i den här anslutningen, men du kan inte lägga till matchningsnycklar som inte var valda när du konfigurerade organisationen.

![Matcha nycklar](/help/assets/connect/establish-connection/match-keys.png)

+++

+++kreditdelning

Använd kreditdelningsavsnittet för att avgöra vilken av de två samarbetande parterna som ska täcka kostnaderna för aktiviteterna.

![Kreditdelning](/help/assets/connect/establish-connection/edit-billing-ownership.png)

+++

+++Avtal

Innan du kan fortsätta med den här anslutningen måste du bekräfta att det finns ett datadelningsavtal mellan de två parterna.

![Juridiska avtal.](/help/assets/connect/establish-connection/legal-agreement.png)

+++

När du har gjort ditt val väljer du **[!UICONTROL Submit]** för att skicka de föreslagna inställningarna till din medarbetare för granskning.

Om du får föreslagna anslutningsinställningar från din medarbetare kan du antingen **[!UICONTROL Accept]** eller **[!UICONTROL Reject]** dessa inställningar. Innan du godkänner anslutningsinställningarna måste du bekräfta att det finns ett giltigt avtal mellan dig och medarbetaren. Om du avvisar anslutningsinställningar kan du kontakta en annan person utanför produkten och diskutera hur de ska ändra anslutningsinställningarna så att du kan acceptera dem.

## Ta bort anslutningar {#delete-connections}

Du kan ta bort alla anslutningar med medarbetare som du inte vill fortsätta arbeta med. Ta bort befintliga anslutningar:

1. Navigera till **[!UICONTROL Connect]** > **[!UICONTROL My connections]**.
2. Välj **[!UICONTROL View connection]** på anslutningskortet för att få åtkomst till anslutningen som du vill ta bort.
3. Markera borttagningsikonen ![ta bort-ikonen](/help/assets/common/delete.svg) för att visa bekräftelsedialogrutan för borttagning av anslutning.
   ![Ta bort anslutningsikonen är markerad.](/help/assets/connect/establish-connection/delete-icon-highlighted.png){zoomable="yes"}
4. Bekräfta borttagningen genom att välja **[!UICONTROL Delete]**.
   ![Dialog som bekräftar borttagning av en anslutning. ](/help/assets/connect/establish-connection/delete-connection-dialog.png){zoomable="yes"}

>[!WARNING]
>
>När anslutningen har tagits bort är du inte längre ansluten till medarbetaren och alla befintliga projekt som ingår i samarbetet tas bort permanent och går inte att återställa.

## Nästa steg

När du har upprättat en anslutning till din medarbetare kan du och din medarbetare nu [skapa projekt](/help/guide/collaborate/manage-projects.md#create-project).
