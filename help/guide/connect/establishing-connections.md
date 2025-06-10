---
title: Kommunicera med annonsörer eller utgivare
description: Lär dig hur du skapar kopplingar och börjar samarbeta i projekt när du har upptäckt potentiella medarbetare.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: c9b96753a9a78bd85002ede3369c5f20eb430548
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Kommunicera med annonsörer eller utgivare

{{limited-availability-release-note}}

Innan medarbetare (vanligtvis en annonsörer och en utgivare) kan samarbeta i kampanjer måste de skapa en anslutning. Med den här anslutningen kan de aktivera målgrupper, skapa projekt och köra rapporter om kampanjresultat.

## Arbetsflöde på hög nivå

För att upprätta en anslutning mellan en annonsörer och en utgivare krävs följande steg:

1. Annonsören [bläddrar bland utgivare och upptäcker](/help/guide/connect/discover-publishers.md) som de vill arbeta med.
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

![Kontrollpanelen Anslut med alternativet Anslut markerat på en specifik utgivare.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

När inbjudan har skickats kan du förhandsgranska (men inte redigera) anslutningsinställningarna. Visa väntande inbjudningar på fliken **[!UICONTROL My connections]**. Anslutningsstatusen visas som **[!UICONTROL Invite sent]**.

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
>abstract="I det här avsnittet anges vem som betalar för motsvarande aktiviteter inom Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Dela målgrupper"
>abstract="Eftertexter för målgruppsaktivering förbrukas baserat på antalet matchade ID:n som förberetts för aktivering."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Mått"
>abstract="Utför aktiviteter för att generera kampanjresultatrapporter och insikter. Krediter förbrukas baserat på antalet rader i kampanjrapporter för alla kampanjer och rapporteringsfrekvensen (varje dag, var tredje dag eller varje vecka)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Rättsligt avtal"
>abstract="Kontrollera att det finns ett datadelningsavtal mellan de två parterna."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Advertiser-namn"
>abstract="<p>Valfri inställning. Anger det namn och ID som annonsören är känd av.</p><p>Annonsörsnamnet som du lägger till här är förifyllt i steget Skapa projekt.</p><ul><li>Om utgivaren har konfigurerat flera namn väljer du ett i listan.</li><li>Om bara ett namn är konfigurerat markeras det automatiskt.</li><li>Om inga namn är konfigurerade kommer fältet att fyllas i i förväg med annonsörens kontonamn från Real-Time CDP Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Skapa ett projekt"

När inbjudan har skickats kan du förhandsgranska anslutningsinställningarna. Inbjudan måste accepteras innan du kan slutföra konfigurationen av anslutningen.

![Vyn med anslutningsinställningar i förhandsgranskningsläget.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

### Anslutningsinställningar för Advertiser {#advertiser-connection-settings}

När din medarbetare har godkänt anslutningen ställer du in anslutningsinställningarna. De här inställningarna definierar dina samarbetsvillkor, inklusive de användningsfall du ska arbeta med, matchningsnycklar för projekt och andra konfigurationer.

Börja med att navigera till **[!UICONTROL My connections]**. För alla anslutningar med statusen **[!UICONTROL Pending]** kan du välja **[!UICONTROL Set up connection]** för att konfigurera anslutningsinställningarna.

![Arbetsytan Mina anslutningar med en väntande anslutning och anslutningsalternativet Konfigurera är markerat.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Du kan redigera och definiera fälten nedan:

![Arbetsytan för anslutningsinställningar innan den fylls i.](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Användningsfall

Användningsexempel är förifyllda med alla tillgängliga alternativ. Om du vill anpassa dem väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Use cases]** och stänger av alla som du inte vill ha. Valda användningsfall avgör vilka vyer och alternativ som är [tillgängliga i dina projekt](../collaborate/manage-projects.md#project-use-cases).

![Inställningar för användningsfall på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Matcha tangenter

Matchningsnycklar är förifyllda med de du valde när du [konfigurerade din organisation](/help/guide/setup/onboard-organization.md#set-up-match-keys). Du kan inaktivera matchningsnycklar som du inte vill använda, men du kan inte lägga till matchningsnycklar som inte valdes under organisationens konfiguration.

![Inställningarna för Matcha nyckel på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/match-keys.png){zoomable="yes"}

+++

+++kreditdelning

Använd kreditdelningsavsnittet för att avgöra vilken av de två samarbetande parterna som ska täcka kostnaderna för aktiviteterna. Alternativ för kreditdelning bestäms av de valda användningsfallen för anslutningen. Användningsfallet **[!UICONTROL Measurement]** kräver att en part ska täcka kostnaderna, men **[!UICONTROL Activation - Matching]** ger ytterligare ett alternativ att låta varje part täcka sina egna kostnader. Mer information om kostnadsfördelning finns i handboken [Kreditaktivitetstyper](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Målgrupp - Egress täcks alltid av den medarbetare som tar emot målgruppen, och därför behövs inget urval.

![Dialogrutan för kreditdelning med alternativ på arbetsytan för anslutning.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}
+++

+++Avtal

Innan du kan fortsätta med den här anslutningen måste du bekräfta att det finns ett datadelningsavtal mellan de två parterna.

![Avsnittet Rättsligt avtal markeras och bekräftas på arbetsytan för anslutning.](/help/assets/connect/establish-connection/legal-agreement.png){zoomable="yes"}

+++

När du har gjort dina val väljer du **[!UICONTROL Submit]** för att skicka de föreslagna inställningarna till din medarbetare för granskning.

### Inställningar för utgivaranslutning {#publisher-connection-settings}

Utgivaren måste sedan granska anslutningsinställningarna och antingen godkänna eller avvisa dem. Om du vill granska anslutningsinställningarna går du till **[!UICONTROL My connections]** och väljer **[!UICONTROL Review connection settings]** på anslutningskortet.

![Alternativet Granska anslutningsinställningar är markerat i vyn Mina anslutningar.](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

Granska de inställningar som medarbetaren har föreslagit. Innan du godkänner anslutningsinställningarna måste du bekräfta att det finns ett giltigt avtal mellan dig och medarbetaren. Dessutom kan du lägga till valfritt annonsörnamn som du känner till i dina system.

![Arbetsytan för anslutningsinställningar med de föreslagna inställningarna från medarbetaren och avsnittet Advertiser-namn och avtal markerade.](/help/assets/connect/establish-connection/publisher-connection-settings.png){zoomable="yes"}

+++Advertiser-namn

Som utgivare som arbetar med anslutningsinställningarna kan du välja att lägga till annonsörnamn som du känner till i dina system. Som utgivare kan du lägga till flera annonsörnamn i en anslutning, till exempel om den annonsörer du arbetar med har en närvaro i flera olika länder. När du senare under processen [skapar ett projekt](/help/guide/collaborate/manage-projects.md#create-project) som du vill samarbeta med, kan du eller din medarbetare välja annonsörnamnet som du vill associera med projektet.

![Dialogrutan Advertiser-namn på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

Så här fungerar valet av annonsörnamn när du skapar ett projekt:

1. **Inget annonsörnamn har angetts**: Om inga annonsörnamn har lagts till används annonserarens namn som annonsörsnamn som standard i Real-Time CDP Collaboration.
2. **En annonsörnamnsuppsättning**: Om ett annonsörnamn läggs till använder Real-Time CDP Collaboration automatiskt det namnet som annonsörnamn för projektet.
3. **Flera annonsörnamn anges**: Om fler än ett annonsörnamn läggs till kan du eller din medarbetare välja något av de angivna namnen när projektet skapas.

![Arbetsytan för anslutningsinställningar med delen Advertiser-namn ifylld.](/help/assets/connect/establish-connection/advertiser-names.png)

+++

>[!NOTE]
>
> När du har godkänt anslutningsinställningarna kan du inte längre lägga till eller redigera annonsörernas namn.

Om du är nöjd med de föreslagna anslutningsinställningarna väljer du **[!UICONTROL Accept]** för att upprätta anslutningen. Om du vill begära ändringar av anslutningsinställningarna väljer du **[!UICONTROL Reject]**. Medarbetaren kan sedan granska anslutningsinställningarna och skicka dem på nytt för granskning.

## Ta bort anslutningar {#delete-connections}

Du kan ta bort alla anslutningar med medarbetare som du inte vill fortsätta arbeta med. Navigera till **[!UICONTROL Connect]** om du vill ta bort befintliga anslutningar. Annonsörer bör sedan navigera till **[!UICONTROL My connections]**. Välj **[!UICONTROL View connection]** på anslutningskortet för att öppna anslutningen som du vill ta bort.

![Anslutningsalternativet Visa är markerat i vyn Mina anslutningar.](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

Markera borttagningsikonen ![ta bort ikon](/help/assets/common/delete.svg) på arbetsytan för anslutningen om du vill ta bort anslutningen.

![Ikonen Ta bort är markerad på arbetsytan för anslutning.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

En bekräftelsedialogruta visas där du ombeds bekräfta borttagningen av anslutningen. Markera **[!UICONTROL Delete]** för att bekräfta borttagningen.

![Bekräftelsedialogrutan för att ta bort en anslutning.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>När anslutningen har tagits bort är du inte längre ansluten till medarbetaren och alla befintliga projekt som ingår i samarbetet tas bort permanent och går inte att återställa.

## Nästa steg

När du har upprättat en anslutning till din medarbetare kan du och din medarbetare nu [skapa projekt](/help/guide/collaborate/manage-projects.md#create-project).
