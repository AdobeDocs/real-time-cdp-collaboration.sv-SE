---
title: Real-Time CDP Collaboration snabbstartsguide
description: Lär dig hur du kan integrera din organisation i Real-Time CDP Collaboration, inklusive hur du skapar roller och organisationer, hämtar målgrupper, aktiverar och mäter. Den här guiden hjälper medarbetare att konfigurera anslutningsinställningar så att de kan börja använda sina målgrupper på ett säkert och effektivt sätt.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
source-git-commit: 9355535e067afeedff33f5c6468bc6fcb1f58e08
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# Real-Time CDP Collaboration snabbstartsguide

{{limited-availability-release-note}}

Kom igång med Real-Time CDP Collaboration genom att konfigurera organisationen, skaffa målgrupper och aktivera och mäta sekretessfokuserad aktivering.

## Förhandskrav

Innan du börjar bör du kontrollera att du har följande:

- En aktiv Real-Time CDP Collaboration-licens.
- [System- eller produktadministratörsåtkomst till Adobe Experience Platform](./permissions/overview.md).
- [Åtkomst har etablerats för slutanvändare](./permissions/manage-user-access.md).
- [Roller som skapats för din organisation och tilldelats användare](./permissions/manage-roles.md).
- Tillgång till varumärkesresurser, t.ex. organisationens namn, logotyp och banderoll.
- En [definierad matchningsnyckelstrategi](./setup/onboard-account.md#set-up-match-keys)
- (Valfritt) Åtkomst till en molnkälla som stöds (Amazon S3 eller Snowflake) om du inte använder Experience Platform för målgruppshantering.

## Steg 1: Slutför rollbaserad konfiguration {#complete-role-based-setup}

Din organisations åtkomstroller avgör vad användare kan se och göra i Collaboration. Innan du fortsätter bör du kontrollera att rollbaserade behörigheter är korrekt konfigurerade för att säkerställa lämplig åtkomst och synlighet på plattformen.

**Resurser:**

- [Dokumentation för användaråtkomst](./permissions/manage-user-access.md)
- [Dokumentation för rollkonfiguration](./permissions/manage-roles.md)


I den här videon får du lära dig hur du tilldelar produktåtkomst och behörigheter till Collaboration med Admin Console och Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452216/?learn=on&enablevpops)

## Steg 2: Konfigurera ditt Collaboration-konto {#set-up-your-account}

Innan du kan hämta målgrupper måste du konfigurera ditt konto i Collaboration. Detta styr hur du ser ut och vad du har tillgång till i gränssnittet.

Om du inte har den behörighet som krävs kan du gå tillbaka till steg 1 eller kontakta organisationens administratör för hjälp med att slutföra konfigurationen.

Definiera kontots roll i Collaboration, tillhandahåll varumärkesresurser och konfigurera matchningsnycklar för att justera målgrupper över olika anslutningar.

>[!NOTE]
>
>Du kan skapa ett eller flera konton (till exempel annonsörer och utgivare) under installationen. Vissa fält, som varumärkesprofilering och e-post för kontakt, kan uppdateras senare på arbetsytan i **[!UICONTROL Settings]**.

- **Tilldela en roll** - Avgör om ditt konto är en annonsörer eller en utgivare. Din roll definierar vilka funktioner du har i Collaboration. Mer information om hur roller påverkar arbetsflödet för samarbete finns i guiden [roller](./overview/roles.md).
- **Varumärkesresurser** - Lägg till följande i ditt konto:
   - Kontonamn (max 100 tecken)
   - Beskrivning (max 1 000 tecken)
   - Logotyp (SVG &lt;20 kB, ideellt fyrkantig)

>[!NOTE]
>
>Om du skapar ett utgivarkonto och vill vara synligt för alla i Collaboration anslutningskatalog kontaktar du Adobe. Utgivarkonton kräver en anpassad varumärkesbanderoll (JPG 2688x1536). Den här filen kan delas direkt med din representant.

- **E-postadress till kontakt** - Ange ett e-postmeddelande till samarbetspartners som ska användas när en anslutning har upprättats.
- **Konfigurera matchningsnycklar** - Välj identifierare som används för målgruppsmatchning.

Mer information om inledande kontokonfiguration, inklusive hur du definierar roller, överför varumärkesresurser och konfigurerar matchningsnycklar, finns i handboken [Första kontokonfiguration](./setup/onboard-account.md#initial-account-setup){target="_blank"}.

I den här videon får du en stegvis genomgång av en annonsörinställning, som att skapa konto, profilera och matcha nyckelkonfiguration.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Steg 3: Source målgrupper (från Experience Platform eller en molnkälla) {#source-audiences}

När ditt konto har skapats och ditt varumärke och dina matchningsnycklar har konfigurerats är du redo att börja anlita målgrupper. Välj någon av följande källmetoder baserat på ditt datalager och företagets behov.

### Alternativ A: Source från Experience Platform

[Använd Collaboration för att länka en sandlåda som innehåller målgrupper](./setup/onboard-audiences.md). Använd denna självbetjäningsmetod för att referera till befintliga målgruppssegment inifrån Experience Platform-instansen.

#### Konfigurera målgrupper

Konfigurera hur målgrupper förbereds, matchas och styrs för användning i anslutningar.

- **Välj målgrupper** *(endast Experience Platform)* - Välj målgruppssegment med identifierare som stöds.
- **Kartmatchningsnycklar** - Justera målgruppsfält med de konfigurerade matchningsnycklarna.
- **Använd omformningar** - Hash-textvärden (till exempel e-post) om det behövs.
- **Schemauppdateringar** - Definiera uppdateringsfrekvens (till exempel dagligen).
- **Konfigurera inställningar för samtycke** - Bestäm vilka profiler som kan inkluderas i anslutningar genom att välja ett medgivandeläge: anmälan, avanmälan eller ingen.

>[!NOTE]
>
>Du kan lägga till eller ta bort målgrupper och uppdatera uppdateringsschemat direkt i Collaboration. Om du vill ändra andra inställningar, till exempel matchningsnycklar eller medgivandeläge, måste du ta bort och återskapa dataanslutningen.

>[!IMPORTANT]
>
>**Maximalt antal målgrupper per medarbetarroll:**
>
>- **Advertisers** kan hämta upp till 25 målgrupper.
>- **Utgivare** kan hämta upp till 250 målgrupper (var och en med minst 1 000 ID).

>[!IMPORTANT]
>
>**Matcha nyckelkrav:**
>
>Alla matchningsnycklar måste vara **trimmade**, **nedsänkta**
>&#x200B;>Hash-kodade matchningsnycklar måste vara **SHA256-hashed**.\
>Om du anger hash-värden som använder versaler konverteras de automatiskt till gemener i Collaboration.\
>Om källan innehåller **klartextidentifierare** använder du alternativet **[!UICONTROL Apply transformation]** för att tillämpa hashning. Det här alternativet är endast tillgängligt när du hämtar målgrupper från Experience Platform och stöds inte för molnbaserade källor.
>
>Mer information finns i avsnittet [kartfält](./setup/onboard-audiences.md#map-fields) i källan och i handboken för målgrupper.

Titta på videon nedan om du vill se en genomgång av hur du hämtar målgrupper med Collaboration.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

Du kan även läsa dokumentet om att [hämta målgrupper i Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Alternativ B: Source från Snowflake eller Amazon S3

Om du vill konfigurera en molnkälla (till exempel [!DNL AWS S3] eller [!DNL Snowflake]) förbereder du dina målgruppsdata med följande [Målgruppsspecifikation PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.1.pdf). När du är klar, eller om du har frågor, kan du kontakta din Adobe-kontorepresentant för att slutföra konfigurationen. Den här metoden är inte självbetjäning och kräver Adobe hjälp.

<!-- Add in the below in final draft: 

To configure a cloud source, such as [!DNL Snowflake] or [!DNL AWS S3], prepare your audience data using the [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.1)

[!DNL AWS S3] can now be configured as a self-service source. For setup instructions, see the [AWS S3 sourcing guide](./setup/configure-aws-s3-audience-sourcing.md)

If you are using [!DNL Snowflake], or other cloud service provider, contact your Adobe account representative to finalize the setup. -->

>[!IMPORTANT]
>
>Molnbaserade målgruppsfiler måste följa det schema som beskrivs i PDF för målgruppsspecifikation. Filerna måste innehålla hash-kodade identifierare (nedsänkt SHA256), obligatoriska metadatafält som `segment_name` och `activation_id`, och format som stöds som CSV eller Parquet måste användas. Adobe normaliserar inte data före aktiveringen. TTL används utifrån målgruppens livstid.
>
>Alla målgrupper i den överförda filen är helt källkodade i det här skedet. Visningsinställningen [för målgrupper](/help/guide/setup/onboard-audiences.md#metadata-visibility) avgör om dina medarbetare kan visa din målgrupp och hanteras via Collaboration användargränssnitt.

## Steg 4: Aktivera målgrupper (till Experience Platform eller ett molnmål) {#activate-audiences}

Aktivera sedan målgrupperna antingen i din Experience Platform-instans eller i ett molnmål.

### Alternativ A: Aktivera till Experience Platform

Utför följande steg som beskrivs i [Konfigurera Adobe Experience Platform som en målguide](/help/guide/destinations/experience-platform.md).

- **Skapa ett mål** - Använd användargränssnittet för att konfigurera ett Experience Platform-mål (sandlådenivå).
- **Kartmatchningsnycklar** - Välj identifierare (t.ex. `hashedEmail`).
- **Definiera TTL** - Ange förfallodatum (1-30 dagar).
- **Verifiera i målgruppsportalen** - När en medarbetare skickar en målgrupp till dig kontrollerar du att den visas i målportalen under originalet [!UICONTROL Real-Time CDP Collaboration].

### Alternativ B: Aktivera till molnet

Om du vill konfigurera ett molnmål (till exempel [!DNL AWS S3] eller [!DNL Snowflake]) kontaktar du Adobe-kontorepresentant för att starta installationsprocessen. Beroende på molnmålet måste du ange information om molnmål, t.ex. filsökväg, autentiseringsuppgifter, kontolokaliserare osv. När du har angett nödvändig information konfigurerar Adobe molndestinationsinställningarna.

Målgruppsdata som skickas till ett molnmål följer ett fördefinierat schema. Om du vill ha en detaljerad beskrivning av de obligatoriska fälten och formaten hämtar du [Collaboration Audience Activation Guide](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

## Steg 5: Ange mått (valfritt) {#set-up-measurement}

>[!AVAILABILITY]
>
>Den här funktionen är i **beta** och är endast tillgänglig för kunder i programmet Begränsad tillgänglighet. Kontakta din Adobe-representant för att få åtkomst.

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Measure]** är bara tillgänglig om **[!UICONTROL Measurement]** use case var aktiverat [&#x200B; under anslutningsprocessen](./connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./collaborate/manage-projects.md#project-use-cases).

Collaboration erbjuder en mängd rapporter för att analysera kampanjernas räckvidd, frekvens och effektivitet. Även om arbetsytan **[!UICONTROL Measure]** är tillgänglig i användargränssnittet kan fullständiga rapportfunktioner kräva backend-aktivering.

Mer information om hur du visar och tolkar mätningsrapporter finns i [mätningsguiden](./collaborate/measure.md). Det omfattar attribuering, kampanjsammanfattningsstatistik och instrumentpaneler som räckvidd-kurvor och frekvensfördelning.

<!-- 
Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."

### Configure measurement workflow

Collaboration supports two measurement workflows:

- **Attribution using Adobe Experience Platform datasets**
- **Campaign summary using only partner-provided data**

Choose the appropriate workflow below based on your campaign measurement goals.

#### Option A: Attribution using Experience Platform datasets

Use this workflow to measure conversion activity using datasets stored in Experience Platform.

1. **Create a measurement data connection**
   - Select the dataset that contains your conversion events.
   - Map identity fields from your dataset to the match keys used in Collaboration.
   - Manage consent and governance settings.
   - Define one or more conversion events to measure.
   - Review and confirm your setup.

2. **Run a measurement report**
   - Go to the **[!UICONTROL Measure]** workspace within the associated project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Attribution]** as the report type.
   - Select the defined conversion event(s).
   - Submit the report. It will run on the specified date and populate within 24 hours.

#### Option B: Campaign summary using partner-provided data

Use this workflow to generate campaign summary insights based on advertiser-supplied identifiers (for example, campaign ID).

1. **Set up the connection**
   - In the connection settings, ensure **[!UICONTROL Measurement]** is selected as a use case.
   - Create a project under the connection with **[!UICONTROL Measurement]** as an activity.

2. **Provide campaign context**
   - Input required campaign identifiers (for example, **Campaign ID**) for the partner to reference.
   - Align with your partner on campaign scope and reporting timeline.

3. **Run a measurement report**
   - Navigate to the **[!UICONTROL Measure]** workspace within the project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Campaign summary]** as the report type.
   - Submit the report. It will run on the selected date and populate within 24 hours. 
-->

## Steg 6: Kommunicera med medarbetare {#connect-with-collaborators}

När konfigurationen är klar är organisationen nu redo att ansluta till medarbetare genom att skicka eller acceptera inbjudningar och skicka in projektinställningar för godkännande. Den här anslutningsprocessen innebär att skicka eller ta emot inbjudningar, granska och skicka anslutningsinställningar (t.ex. användningsfall och kreditförbrukning) och bekräfta anslutningen.

Använd arbetsytan **[!UICONTROL Connect]** på den vänstra navigeringsmenyn för att bläddra bland tillgängliga utgivare. Medarbetare kan också ansluta till varandra direkt via [privata anslutningsinbjudningar](./connect/establishing-connections.md#private-connection-invite){target="_blank"}.

>[!NOTE]
>
>För närvarande kan bara annonsörer bläddra bland utgivare. Utgivare kan inte bläddra bland eller initiera anslutningar med annonsörer.

En översikt över det här flödet finns i [guiden om att upprätta anslutningar](./connect/establishing-connections.md){target="_blank"}. Titta på videon [Konfigurera annonskonto](https://experienceleague.adobe.com/sv/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"} om du vill få en visuell genomgång av anslutningsprocessen, bland annat om hur du bläddrar bland medarbetare och hanterar anslutningsinställningar.

## Nästa steg

Du har nu slutfört den första konfigurationen och konfigurerat din organisation för säkert samarbete. Utforska sedan följande resurser för att fördjupa din förståelse för aktivering, mätning och datastyrning:

- [Arbetsflödesdokumentation för målaktivering](./collaborate/activate.md)
- [Användningsexempel för mätning](./collaborate/measure.md)
- [Bästa praxis för styrning av Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
