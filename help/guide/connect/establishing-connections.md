---
title: Upprättar anslutningar
description: Lär dig hur du skapar kopplingar och börjar samarbeta i projekt när du har upptäckt potentiella medarbetare.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: 899b6c2a0111ccaebbaf2818772e1d743d6de914
workflow-type: tm+mt
source-wordcount: '3274'
ht-degree: 0%

---

# Upprättar anslutningar {#establishing-connections}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Jämför målgrupper"
>abstract="Jämför er målgrupp med alla kunder som Amazon Ads når."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Relevanta målgrupper"
>abstract="Amazon inriktar sig på segment som er målgrupp har störst överlappning med tanke på att endast DSP-visningar förekommer (dessa segment kan bara användas i DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="Lösta ID:n"
>abstract="Antalet ID:n Amazon Identity Resolution kunde matchas med era målgruppsdata."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="Överlappande och exponerade ID"
>abstract="Detta visar antalet&quot;Lösta ID:n&quot; från den överförda publiken som också har exponerats för en annons via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="Överlappa %"
>abstract="Andelen&quot;Lösta ID:n&quot; som har exponerats för en annons via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Uppdelning efter Amazon-produkt"
>abstract="Uppdelningen av överlappande och exponerade ID:n som nås av antingen Amazon Ads Sponsored Product och/eller Amazon Ads DSP."

{{limited-availability-release-note}}

Innan medarbetare kan samarbeta i kampanjer måste de skapa en anslutning. Med den här anslutningen kan de aktivera målgrupper, skapa projekt och köra rapporter om kampanjresultat.

Anslutningar upprättas baserat på ditt valda samarbetsmönster. Collaboration har stöd för två viktiga samarbetsmönster: annonser-till-utgivare och varumärken. Mer information om mönstren finns i handboken [use case](/help/guide/overview/use-cases.md).

Om du vill lära dig hur du upprättar en anslutning läser du avsnittet nedan som motsvarar ditt samarbetsmönster:

- [Anslutning mellan annonsörer och utgivare](#advertiser-to-publisher-connection)
- [Varumärkesbaserad koppling](#brand-to-brand-connection)

## Anslutning mellan annonsörer och utgivare {#advertiser-to-publisher-connection}

![Högnivådiagram över anslutningsprocessen mellan annonser och utgivare.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

I mönstret för annonser-till-utgivare upptäcker en annonsörer en utgivare som de vill arbeta med via arbetsytan **[!UICONTROL Discover publishers]** och skickar en anslutningsinbjudan. Utgivaren granskar sedan inbjudan och godkänner den, så att annonsören kan föreslå anslutningsinställningar. När utgivaren har godkänt anslutningsinställningarna upprättas anslutningen, och båda medarbetarna kan börja arbeta tillsammans i projekt.

### Översikt på hög nivå

För att upprätta en anslutning mellan en annonsörer och en utgivare gäller följande steg:

1. [Identifiera utgivare](#discover-publishers): Annonsören identifierar potentiella utgivare att samarbeta med.
1. [Skicka inbjudan](#send-invite): Annonsören skickar en anslutningsinbjudan till den valda utgivaren.
1. [Acceptera inbjudan](#accept-invite): Utgivaren granskar och accepterar inbjudan.
1. [Konfigurera anslutningsinställningar](#configure-connection-settings): Annonsören konfigurerar anslutningsinställningarna och skickar dem till utgivaren för granskning.
1. [Bekräfta anslutningsinställningar](#establish-connection): Utgivaren granskar anslutningsinställningarna och godkänner eller avvisar dem. Om anslutningen godkänns upprättas den. Om det inte godkänns kan utgivaren ge återkoppling för revideringar utanför produkten. Annonsören kan sedan granska inställningarna och skicka dem på nytt för granskning.

När anslutningsinställningarna har godkänts upprättas anslutningen och medarbetare är redo att [skapa ett projekt](/help/guide/collaborate/manage-projects.md#create-project) för att börja samarbeta med kampanjer.

## Varumärkesbaserad koppling {#brand-to-brand-connection}

![Bild på hög nivå av varumärkesanslutningsprocessen.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>Termen **varumärke** används för att referera till ett företag eller ett varumärke utanför Collaboration. Termen **medarbetare** avser alla konton som kan bilda en anslutning i Collaboration, oavsett om de är annonsörer eller utgivare.

I varumärkesprofilmönstret kan två varumärken som har kommunicerat utanför produkten ansluta direkt i Collaboration med en [privat anslutningsinbjudan](#private-connection-invite). Ett varumärke kan antingen vara en annonsörer eller en utgivare. Det här mönstret är särskilt användbart för varumärken som kanske inte passar den traditionella annonsörmodellen, som två annonsörer eller två utgivare.

Till att börja med skickar en medarbetare en privat anslutningsinbjudan till en annan medarbetare. Mottagaren granskar inbjudan och accepterar den, vilket gör att ägaren kan föreslå anslutningsinställningar. När mottagaren har godkänt anslutningsinställningarna upprättas anslutningen och båda medarbetarna kan börja arbeta tillsammans i projekt.

### Översikt på hög nivå

>[!TIP]
>
>När du diskuterar anslutningsprocessen görs en skillnad mellan **ägaren** och **mottagaren**. Ägaren är medarbetaren som initierar anslutningen genom att skicka inbjudan, medan mottagaren är medarbetaren som tar emot och granskar inbjudan.

Anslutningsprocessen mellan två varumärken omfattar flera steg. Innan anslutningsprocessen börjar måste vissa villkor vara uppfyllda:

1. Två varumärken kommunicerar utanför produkten för att diskutera den potentiella anslutningen.
1. Varumärken [skapar konton](/help/guide/setup/onboard-account.md) i Collaboration om de inte redan gjort det, och måste välja lämplig rolltyp (annonsörer eller utgivare).

   När förutsättningarna är uppfyllda kan anslutningsprocessen börja. I följande steg beskrivs processen:

1. [Skicka inbjudan om privat anslutning](#send-private-connection-invite): En medarbetare skickar en privat anslutningsinbjudan till en annan medarbetare.
1. [Acceptera inbjudan till privat anslutning](#accept-private-connection-invite): Mottagaren granskar och accepterar inbjudan till privat anslutning.
1. [Konfigurera anslutningsinställningar](#configure-connection-settings): Ägaren konfigurerar anslutningsinställningarna och skickar dem till mottagaren för granskning och godkännande.
1. [Bekräfta anslutningsinställningar](#establish-connection): Mottagaren granskar anslutningsinställningarna och godkänner eller avvisar dem.

När anslutningsinställningarna har godkänts upprättas anslutningen och medarbetare är redo att [skapa ett projekt](/help/guide/collaborate/manage-projects.md#create-project) för att börja samarbeta med kampanjer.

## Anslut {#connect}

På arbetsytan i **[!UICONTROL Connect]** kan du hantera dina anslutningar med medarbetare, skicka anslutningsinbjudningar och där annonsörer kan bläddra i utgivarkatalogen. Arbetsytan är uppdelad i två huvudflikar:

### Upptäck förlag {#discover-publishers}

>[!IMPORTANT]
>
>Endast annonsörer kan identifiera utgivare med arbetsytan **[!UICONTROL Discover publishers]**. Om du vill veta mer om hur du ansluter till medarbetare oavsett deras roll läser du avsnittet [varumärkesanslutning](#brand-to-brand-connection).

Om du vill identifiera utgivare går du till arbetsytan **[!UICONTROL Discover publishers]** på fliken **[!UICONTROL Connect]**. Här kan du bläddra igenom listan med tillgängliga utgivare med hjälp av sidnumreringskontrollerna längst ned på arbetsytan. Mer information om arbetsytan **[!UICONTROL Discover publishers]** finns i handboken [Identifiera utgivare](/help/guide/connect/discover-publishers.md).

![Arbetsytan Identifiera utgivare som visar en lista över tillgängliga utgivare.](/help/assets/connect/establish-connection/discover-publishers.png){zoomable="yes"}

### Skicka inbjudan {#send-invite}

>[!IMPORTANT]
>
>I det här avsnittet beskrivs processen för annonsörer som skickar anslutningsinbjudningar till utgivare via arbetsytan **[!UICONTROL Discover publishers]**. Om du vill veta mer om hur du skapar anslutningar mellan varumärken oavsett deras roller kan du läsa avsnittet [varumärkesanslutning](#brand-to-brand-connection) eller gå till avsnittet [inbjudan till privat anslutning](#private-connection-invite).

När du har identifierat en utgivare som du vill samarbeta med väljer du alternativet **[!UICONTROL Connect]** på utgivarkortet. Den här åtgärden initierar anslutningsprocessen.

![Alternativet Anslut är markerat på en viss utgivare på arbetsytan Identifiera utgivare.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

En dialogruta visas där du uppmanas att skicka en anslutningsinbjudan till utgivaren. Välj **[!UICONTROL Send invite]** om du vill fortsätta.

![Dialogrutan Skicka-inbjudan med knappen Skicka inbjudan markerad.](/help/assets/connect/establish-connection/send-connection-invite-dialog.png){zoomable="yes"}

>[!NOTE]
>
>Om du vill ansluta till en utgivare som du har kommunicerat med utanför produkten kan du använda alternativet för inbjudan till privat anslutning. Mer information finns i avsnittet [Inbjudan till privat anslutning](#private-connection-invite).

Väntande inbjudan visas på fliken **[!UICONTROL My connections]** i avsnittet **[!UICONTROL Action required]**. Anslutningsstatusen visas som **[!UICONTROL Invite sent]**. Du kan förhandsgranska anslutningsinställningarna genom att välja **[!UICONTROL Preview connection]**, men du kan inte redigera dem förrän utgivaren accepterar inbjudan.

![Den väntande anslutningen visas på arbetsytan Mina anslutningar i avsnittet Åtgärd krävs.](/help/assets/connect/establish-connection/preview-connection.png){zoomable="yes"}

### Inbjudan till privat anslutning {#private-connection-invite}

Med privata anslutningsinbjudningar kan du ansluta till medarbetare som du har kommunicerat med utanför produkten med hjälp av en **[!UICONTROL Connect code]**. Om du vill skapa en privat anslutning måste du hämta **[!UICONTROL Connect code]** från medarbetaren som du vill ansluta till utanför produkten. Du kan sedan använda den här koden för att skicka en privat anslutningsinbjudan till medarbetaren i arbetsytan **[!UICONTROL Connect]**.

#### Anslut kod {#connect-code}

Innan du kan skicka en privat anslutningsinbjudan måste den medarbetare du vill ha ge dig tillgång till deras unika **[!UICONTROL Connect code]**. Om du vill söka efter och kopiera din **[!UICONTROL Connect code]** går du till fliken **[!UICONTROL My account]** på arbetsytan i **[!UICONTROL Setup]**. **[!UICONTROL Connect code]** visas i din kontoinformation.

![Fliken Mitt konto på arbetsytan Konfigurera med Connect-koden markerad.](/help/assets/connect/establish-connection/connect-code.png){zoomable="yes"}

Välj kopieringsikonen (![kopieringsikonen](/help/assets/icons/copy.png)) bredvid **[!UICONTROL Connect code]** för att kopiera den till Urklipp. Sedan kan du dela koden med medarbetaren utanför produkten.

![Connect-koden med kopieringsikonen markerad.](/help/assets/connect/establish-connection/copy-connect-code.png){zoomable="yes"}

##### Uppdatera anslutningskoden {#refresh-connect-code}

Du kan när som helst uppdatera din **[!UICONTROL Connect code]**. När du uppdaterar koden genereras en ny unik kod som du kan dela med medarbetare. Detta är användbart om du vill göra den föregående koden ogiltig av säkerhetsskäl. Alla anslutningar som upprättats med den gamla koden förblir aktiva, men nya medarbetare måste använda den nya koden för att ansluta till dig.

>[!IMPORTANT]
>
>Om du uppdaterar **[!UICONTROL Connect code]** under en väntande inbjudan kan det leda till att inbjudan inte accepteras. Om du uppdaterar koden kan din medarbetare behöva skicka om den privata anslutningsinbjudan med den nya koden.

Om du vill uppdatera **[!UICONTROL Connect code]** väljer du uppdateringsikonen (![uppdateringsikonen](/help/assets/icons/refresh.png)) bredvid **[!UICONTROL Connect code]**.

![Koden Anslut med uppdateringsikonen markerad.](/help/assets/connect/establish-connection/refresh-connect-code.png){zoomable="yes"}

>[!IMPORTANT]
>
>Konton som skapats innan funktionen **[!UICONTROL Connect code]** introducerades har ingen genererad anslutningskod och anslutningsfältet visas som **[!UICONTROL Unavailable]**. Använd uppdateringsalternativet för att generera en ny anslutningskod.

#### Skicka inbjudan om privat anslutning {#send-private-connection-invite}

När du har **[!UICONTROL Connect code]** från din medarbetare kan du skicka en privat anslutningsinbjudan. Det gör du genom att navigera till arbetsytan **[!UICONTROL Connect]** och välja plusikonen (![plustecknet ](/help/assets/icons/plus.png)) i det övre högra hörnet.

![Plustecknet är markerat på arbetsytan Anslut.](/help/assets/connect/establish-connection/private-connection-invite.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Connect]** visas och du uppmanas att ange **[!UICONTROL Connect code]** för den medarbetare som du vill ansluta till. Klistra in koden i textfältet och välj **[!UICONTROL Continue]** för att fortsätta.

![Dialogrutan Anslut med kodfältet Anslut ifyllt och alternativet Fortsätt markerat.](/help/assets/connect/establish-connection/private-connection-invite-connect.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Connect]** visar sedan medarbetaren som koden är kopplad till, så att du kan bekräfta att du ansluter till rätt medarbetare. Om medarbetaren har rätt väljer du **[!UICONTROL Connect]** för att skicka inbjudan till den privata anslutningen.

![Dialogrutan Anslut med information om medarbetare visas och alternativet Anslut är markerat.](/help/assets/connect/establish-connection/private-connection-invite-connect-confirm.png){zoomable="yes"}

### Acceptera inbjudan {#accept-invite}

>[!TIP]
>
>När du diskuterar anslutningsprocessen görs en skillnad mellan **ägaren** och **mottagaren**. Ägaren är medarbetaren som initierar anslutningen genom att skicka inbjudan, medan mottagaren är medarbetaren som tar emot och granskar inbjudan.

Innan ägaren kan konfigurera anslutningsinställningarna måste mottagaren acceptera anslutningsinbjudan. Om du vill göra det går du till arbetsytan **[!UICONTROL Connect]** och söker efter den väntande anslutningen i avsnittet **[!UICONTROL Action required]**. Anslutningsstatusen visas som **[!UICONTROL Invite received]**. Välj **[!UICONTROL Accept]** om du vill acceptera inbjudan.

![Den väntande anslutningen visas Åtgärdsavsnitt som krävs på arbetsytan Anslut med alternativet Acceptera markerat.](/help/assets/connect/establish-connection/accept-connection.png){zoomable="yes"}

En dialogruta visas där du uppmanas att acceptera inbjudan. Välj **[!UICONTROL Accept invite]** om du vill fortsätta.

![Dialogrutan Acceptera inbjudan med alternativet Acceptera inbjudan markerat.](/help/assets/connect/establish-connection/accept-connection-invite.png){zoomable="yes"}

Anslutningens status ändras till **[!UICONTROL Pending]**. Ägaren kan nu konfigurera anslutningsinställningarna.

### Konfigurera anslutningsinställningar {#configure-connection-settings}

Anslutningsinställningarna definierar villkoren mellan två medarbetare. De här inställningarna omfattar användningsfall, matchningsnycklar, kreditdelning och juridiska avtal. Medarbetare som ansluter till annonsörer kan också lägga till annonsörnamn i anslutningsinställningarna, som används när projekt skapas.

När mottagaren har accepterat inbjudan kan ägaren konfigurera anslutningsinställningarna. Om du vill göra det går du till **[!UICONTROL My connections]** och söker efter den väntande anslutningen i avsnittet **[!UICONTROL Action required]**. Välj **[!UICONTROL Set up connection]** om du vill konfigurera anslutningsinställningarna.

![Arbetsytan Anslut med anslutningsalternativet Konfigurera markerat i avsnittet Åtgärd krävs.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Arbetsytan för anslutningsinställningar visas, så att du kan konfigurera de olika inställningarna för anslutningen.

![Arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/connection-set-up.png){zoomable="yes"}

#### Anslutningsinställningar {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Användningsfall"
>abstract="Användningsexemplen är förifyllda med alla alternativ. Du kan redigera användningsexemplen innan du skickar in anslutningsinställningarna."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Matcha nycklar"
>abstract="Matchningsnycklar är förifyllda med vanliga matchningsnycklar som du och din medarbetare har valt på kontonivån. Du kan inaktivera matchningsnycklar som du inte vill använda i den här anslutningen."
>additional-url="https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys" text="Kontomatchningsnycklar"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="Kreditdelning"
>abstract="I det här avsnittet anges vem som betalar för motsvarande aktiviteter inom Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Dela målgrupper"
>abstract="Eftertexter för målgruppsaktivering förbrukas baserat på antalet matchade ID:n som förberetts för aktivering."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Mått"
>abstract="Utför aktiviteter för att generera kampanjresultatrapporter och insikter. Krediter förbrukas baserat på antalet rader i kampanjrapporter för alla kampanjer och rapporteringsfrekvensen (varje dag, var tredje dag eller varje vecka)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Advertiser-namn"
>abstract="<p>Valfri inställning. Anger det namn och ID som annonsören är känd av.</p><p>Annonsörsnamnet som du lägger till här är förifyllt i steget Skapa projekt.</p><ul><li>Om utgivaren har konfigurerat flera namn väljer du ett i listan.</li><li>Om bara ett namn är konfigurerat markeras det automatiskt.</li><li>Om inga namn är konfigurerade kommer fältet att fyllas i i förväg med annonsörens kontonamn från Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Skapa ett projekt"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Målgruppsaktivering"
>abstract="Med målgruppsaktivering kan ni välja vilka medarbetare som kan initiera målgruppsaktivering."

Du kan konfigurera följande anslutningsinställningar:

##### Målgruppsaktivering {#audience-activation}

>[!IMPORTANT]
>
>Alla anslutningar som skapats innan funktionen **[!UICONTROL Audience activation]** introducerades får automatiskt inställningen för målgruppsaktivering inställd på anslutningsägaren. Om du vill tillåta båda medarbetarna att aktivera målgrupper behöver du [ta bort din nuvarande anslutning](#delete-connections) och skapa en ny med de uppdaterade inställningarna.

Med målgruppsaktivering kan ni välja vilka medarbetare som kan aktivera målgrupper i anslutningen. Målgruppsaktivering är bara ett alternativ om **[!UICONTROL Audience activation]**-användningsfallet har valts. Om du väljer att ta bort användningsfallet under anslutningsprocessen tas inställningen för målgruppsaktivering bort från anslutningsinställningarna. Mer information om målgruppsaktivering finns i handboken [activate](/help/guide/collaborate/activate.md).

Om du vill konfigurera målgruppsaktivering väljer du **[!UICONTROL Set up]** i avsnittet **[!UICONTROL Audience activation]**. Använd listrutan för att ange vilka medarbetare som kan aktivera målgrupper. Du kan välja en medarbetare eller tillåta båda medarbetarna att aktivera målgrupper.

![Dialogrutan Målgruppsaktivering med alternativ på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/audience-activation.png){zoomable="yes"}

När du är klar väljer du **[!UICONTROL Save]** för att spara ändringarna.

![Dialogrutan Målgruppsaktivering med alternativet Spara på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/audience-activation-confirm.png){zoomable="yes"}

##### Användningsfall {#use-cases}

Användningsexempel fylls i automatiskt med alla tillgängliga alternativ. De valda användningsfallen avgör vilka vyer och alternativ som är tillgängliga i dina projekt. Läs handboken [Projektanvändningsfall](/help/guide/collaborate/manage-projects.md#project-use-cases) om du vill veta mer.

Om du vill anpassa dina användningsfall väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Use cases]** och stänger av alla du inte vill inkludera i projekt med medarbetaren. När du är klar väljer du **[!UICONTROL Save]** för att spara ändringarna.

![Inställningar för användningsfall på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

##### Matcha nycklar {#match-keys}

>[!IMPORTANT]
>
>Vid aktivering av målgrupper där flera matchningsnycklar används, om en (eller flera) matchningsnyckel inte har några överlappningar, inget antal målgrupper eller faller under tröskelvärdet, misslyckas hela aktiveringen. Se till att era målgrupper har tillräcklig överlappning och att de uppfyller det lägsta tröskelvärdet på 1 000 ID:n för alla matchningsnycklar innan de aktiveras.

Matchningsnycklar fylls automatiskt i med de vanliga matchningsnycklar som du och din medarbetare valde när du [konfigurerade dina konton](/help/guide/setup/onboard-account.md#set-up-match-keys). Endast matchande nycklar som både du och din medarbetare har valt **och** visas.

![Arbetsytan för anslutningsinställningar med avsnittet Matcha nycklar markerat med vanliga matchningsnycklar.](/help/assets/connect/establish-connection/auto-populated-match-keys.png){zoomable="yes"}

När anslutningsägaren konfigurerar anslutningsinställningarna kan de [redigera kontouppdelementen](../setup/onboard-account.md#edit-match-keys) för att inkludera ytterligare matchningsnycklar. När du har aktiverat fler matchningsnycklar i dina kontoinställningar kan dessa matchningsnycklar aktiveras i anslutningsinställningarna om medarbetaren också har valt dem. Matchningsnycklar som läggs till när anslutningsprocessen väl har börjat fylls inte i automatiskt och måste aktiveras manuellt.

Om du vill anpassa matchningsnycklarna väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Match keys]** och inaktiverar alla matchningsnycklar som du inte vill använda i den här anslutningen. När du är klar väljer du **[!UICONTROL Save]** för att spara ändringarna.

![Arbetsytan för anslutningsinställningar med dialogrutan Matcha nycklar öppen med en inaktiverad matchningsnyckel.](/help/assets/connect/establish-connection/additional-match-key-selected.png){zoomable="yes"}

>[!IMPORTANT]
>
>När din medarbetare har godkänt anslutningsinställningarna kommer matchningsnycklarna att vara låsta och kan inte ändras.

##### Kreditdelning {#credit-split}

Använd kreditdelningsavsnittet för att avgöra vilken av de två samarbetande parterna som ska täcka kostnaderna för aktiviteterna. Alternativ för kreditdelning bestäms av de valda användningsfallen för anslutningen. Användningsfallet **[!UICONTROL Measurement]** kräver att en part ska täcka kostnaderna, men **[!UICONTROL Activation - Matching]** ger ytterligare ett alternativ att låta varje part täcka sina egna kostnader. Mer information om kostnadsfördelning finns i handboken [Kreditaktivitetstyper](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Målgrupp - Egress täcks alltid av den medarbetare som tar emot målgruppen, och därför behövs inget urval.

Om du vill konfigurera kreditdelningen väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Credit split]**. Du kan sedan välja lämpliga alternativ för varje användningsfall. När du är klar väljer du **[!UICONTROL Save]** för att spara ändringarna.

![Dialogrutan för kreditdelning med alternativ på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}

##### Advertiser-namn {#advertiser-names}

>[!NOTE]
>
>Det här alternativet kan visas under konfigurationen av anslutningsinställningarna eller granskningen av anslutningsinställningarna, beroende på vem som initierar anslutningen.

Om du är en utgivare som skapar en anslutning till en annonsörer kan du välja att lägga till annonsörnamn i anslutningsinställningarna. På så sätt kan du lägga till flera namn som annonsören är känd med i dina system. Detta är särskilt användbart om annonsören finns på flera platser eller om de är kända med olika namn i olika sammanhang. När du sedan skapar ett projekt kan du välja lämpligt annonsörnamn i listan med namn som har konfigurerats i anslutningsinställningarna.

![Advertiser-namnen på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/advertiser-names.png){zoomable="yes"}

Om du vill lägga till annonsörnamn väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Advertiser names]**. Du kan sedan ange **[!UICONTROL Advertiser ID]** som du känner till som i ditt system och en **[!UICONTROL Advertiser name]** som du kan koppla till det ID:t i Collaboration. Du kan lägga till flera annonsörnamn genom att välja alternativet **[!UICONTROL Add]**.

![Dialogrutan Advertiser-namn med alternativ på arbetsytan för anslutningsinställningar.](/help/assets/connect/establish-connection/advertiser-names-dialog.png){zoomable="yes"}

När du är klar väljer du **[!UICONTROL Save]** för att spara ändringarna.

När du skapar ett projekt kommer annonsörens namn att fyllas i i förväg baserat på följande inställningar som har angetts under anslutningen    :

1. **Inget annonsörnamn har angetts**: Om inga annonsörnamn har lagts till används annonserarens namn som annonsörsnamn som standard i Collaboration.
2. **En annonsörnamnsuppsättning**: Om ett annonsörnamn läggs till använder Collaboration automatiskt det namnet som annonsörnamn för projektet.
3. **Flera annonsörnamn anges**: Om fler än ett annonsörnamn läggs till kan du eller din medarbetare välja något av de angivna namnen när projektet skapas.

>[!NOTE]
>
> När du har skickat anslutningsinställningarna kan du inte längre lägga till eller redigera annonsörernas namn.

![Arbetsytan för anslutningsinställningar med delen Advertiser-namn ifylld.](/help/assets/connect/establish-connection/add-advertiser-names.png)

När du har gjort dina val väljer du **[!UICONTROL Submit]** för att skicka de föreslagna inställningarna till mottagaren för granskning.

### Granska anslutningsinställningar {#review-connection-settings}

Därefter måste mottagaren granska de anslutningsinställningar som ägaren har föreslagit. Mottagaren kan göra detta genom att gå till fliken **[!UICONTROL My connections]** på arbetsytan i **[!UICONTROL Connect]**. Anslutningen visas i avsnittet **[!UICONTROL Action required]**. Välj **[!UICONTROL Review connection settings]** om du vill granska de föreslagna anslutningsinställningarna.

![Arbetsytan Mina anslutningar med anslutningsalternativet Granska markerat.](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

Granska de inställningar som medarbetaren har föreslagit. Du kan antingen acceptera eller ignorera anslutningsinställningarna. Om du avvisar anslutningsinställningarna måste du kontakta medarbetaren om de ändringar du vill göra utanför produkten. Medarbetarens kontaktinformation visas i avsnittet **[!UICONTROL Contact]** på arbetsytan för anslutningsinställningar. Ägaren kan sedan ändra anslutningsinställningarna och skicka om dem för granskning.

![Arbetsytan för anslutningsinställningar med alternativet Acceptera och ignorera markerat.](/help/assets/connect/establish-connection/accept-connection-settings.png){zoomable="yes"}

Om du är en utgivare som ansluter till en annonsör kan du nu lägga till annonsörnamn i anslutningsinställningarna. Mer information om den här processen finns i avsnittet [anslutningsinställningar](#connection-settings).

>[!NOTE]
>
> När du har godkänt anslutningsinställningarna kan du inte längre lägga till eller redigera annonsörernas namn.

Välj sedan **[!UICONTROL Accept]** för att fortsätta med anslutningen. Anslutningsstatusen ändras till **[!UICONTROL Active]** och du kan nu börja samarbeta i projekt.

## Ta bort anslutningar {#delete-connections}

Du kan ta bort alla anslutningar med medarbetare som du inte vill fortsätta arbeta med. Navigera till **[!UICONTROL Connect]** om du vill ta bort befintliga anslutningar. Som utgivare visas din befintliga anslutning. Som annonsörer bör du sedan navigera till **[!UICONTROL My connections]**.

Välj **[!UICONTROL View connection]** på det anslutningskort som du vill ta bort.

![Anslutningsalternativet Visa är markerat i vyn Mina anslutningar.](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

Markera borttagningsikonen ![ta bort ikon](/help/assets/common/delete.svg) på arbetsytan för anslutningen om du vill ta bort anslutningen.

![Ikonen Ta bort är markerad på arbetsytan för anslutning.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

En bekräftelsedialogruta visas där du ombeds bekräfta borttagningen av anslutningen. Markera **[!UICONTROL Delete]** för att bekräfta borttagningen.

![Bekräftelsedialogrutan för att ta bort en anslutning.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>När anslutningen har tagits bort tas alla befintliga projekt i samarbetet bort permanent och kan inte återställas. Anslutningsbegäran kommer att vara i ett väntande tillstånd, men anslutningen och dess konfigurationer kommer inte längre att vara aktiva. Du måste återupprätta anslutningen om du vill ansluta till medarbetaren igen.

## Nästa steg

När du har upprättat en anslutning till din medarbetare kan du och din medarbetare nu [skapa projekt](/help/guide/collaborate/manage-projects.md#create-project).
