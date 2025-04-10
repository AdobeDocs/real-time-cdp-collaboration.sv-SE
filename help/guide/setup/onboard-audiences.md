---
title: Importera och hantera målgrupper
description: Läs om hur du importerar och hanterar målgrupper i Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: ff22dde9730fab89481338753b1dc4a0adf1d57e
workflow-type: tm+mt
source-wordcount: '2577'
ht-degree: 0%

---

# Importera och hantera målgrupper

{{limited-availability-release-note}}

Målgrupper är specifika grupper av användare eller kunder som segmenteras utifrån olika attribut. Dessa gör det möjligt för annonsörer och utgivare att samarbeta om riktad marknadsföring och personaliserade upplevelser för mer effektiva annonskampanjer.

Använd den här sidan som språng för att förstå alla relevanta mätvärden som ni kan visa för era målgrupper, samt arbetsflödesstegen för att importera en målgrupp till Adobe Real-Time CDP Collaboration.

>[!TIP]
>
>Använd informationen på den här skärmen för att få all information du behöver om era målgrupper, och [identifiera och överlappa skärmar](/help/guide/collaborate/discover.md) för att få insikter om vilka av era målgrupper som fungerar bäst för olika kampanjtyper, jämfört med utgivarens lager.

>[!BEGINSHADEBOX]

Vad du hittar på den här dokumentationssidan:

* [Importera målgrupper till Real-Time CDP Collaboration](#import-audiences)
* [Visa målgruppspanelen](#view-audiences-dashboard)
* [Visa enskilda målgrupper](#view-individual-audiences)

>[!ENDSHADEBOX]

## Importera målgrupper till Real-Time CDP Collaboration {#import-audiences}

>[!IMPORTANT]
>
>Om du vill importera målgrupper måste användaren tilldelas en roll som innehåller två behörigheter för profilhantering - Visa profiler och Visa segment. Mer information om hur du tilldelar nödvändiga behörigheter finns i guiden [målgruppsimport](../permissions/overview.md#audience-importation).

Innan du kan dela målgrupper med medarbetare och köra överlappningsberäkningar måste målgrupperna importeras till Real-Time CDP Collaboration. Om du vill importera målgrupper följer du arbetsflödesstegen i avsnittet nedan.

![Min målgruppsskärm innan någon målgrupp har lagts till i organisationen.](/help/assets/setup/add-manage-audiences/org-without-audiences-added.png)

Välj plustecknet **+** på fliken **[!UICONTROL My audiences]** och välj **Målgrupp**.

### Välj dataanslutning {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Marknadsföringsåtgärder"
>abstract="<p>Använd marknadsföringsåtgärder för att styra vilka målgruppsdata som ska importeras till Real-Time CDP Collaboration från Experience Platform. Marknadsföringsåtgärden <strong>Data Collaboration</strong> stöder etiketter för C4-, C5- och C9-dataanvändning. Marknadsföringsåtgärden <strong>Data Science</strong> stöder C9-dataanvändningsetiketten.</p> <p> <ul><li> Med kryssrutan <em>aktiverad</em> exkluderas alla data som är markerade med etiketterna som anropas ovan i Experience Platform och <strong>hämtas </strong> inte till Real-Time CDP Collaboration.</li><li> Med kryssrutan <em>inaktiverad</em> finns det ingen begränsning för data från Experience Platform som kan importeras till Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html" text="Översikt över etiketter för dataanvändning"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html" text="Etikettordlista för dataanvändning"

>[!IMPORTANT]
>
>När du har anslutit till din första dataanslutning och importerat din första målgrupp kan du välja att importera flera målgrupper från den befintliga dataanslutningen. I det här fallet tar arbetsflödet dig direkt till steget [välj målgrupp](#select-audience) eftersom all nödvändig information från de andra stegen importeras från den befintliga anslutningen.

En dataanslutning är datakällan som du importerar målgrupper från till Real-Time CDP Collaboration. I den första utgåvan av Real-Time CDP Collaboration är Adobe Experience Platform den enda dataanslutning som stöds.

Alla inställningar som du konfigurerar för din dataanslutning, till exempel identitetsmappning eller schemaläggning, tillämpas på alla målgrupper som importeras från den här dataanslutningen.

>[!TIP]
>
>Det finns ett separat arbetsflöde där du alltid kan visa och redigera alla dataanslutningar som du har lagt till i det här steget. Läs mer om [hantering av dataanslutningar](/help/guide/setup/manage-data-connection.md).

![Välj målgruppskälla med alternativ för AEP RTCDP, CSV-fil, Amazon S3 och Snowflake.](/help/assets/setup/add-manage-audiences/Step-Select-Audience-Source.png)

#### Välj datakälla

I det här steget väljer du källa för målgruppsdata. De tillgängliga källorna är:

* **Adobe Experience Platform**: Välj det här alternativet om du vill hämta målgrupper från Adobe Experience Platform Real-Time CDP.
* **CSV-fil** (kommande version): Överför en CSV-fil som innehåller målgruppsdata för snabb och enkel datainhämtning.
* **Amazon Web Services** (kommande version): Anslut till ditt Amazon S3-lagringsutrymme om du vill importera målgruppsdata direkt från dina S3-butiker.
* **Snowflake** (kommande version): Använd Snowflake datalager för att hämta in målgruppsdata sömlöst.

#### Välj sandlåda

När du har valt **Adobe Experience Platform** som datakälla måste du markera sandlådan som innehåller de målgrupper som du vill importera.

![Välj sandlåda för att importera målgrupper](/help/assets/setup/add-manage-audiences/import-audiences-select-sandbox.png)

Välj **[!UICONTROL Next]** när du har markerat önskad sandlåda.

#### Styrningspolitik och verkställighetsåtgärder {#governance-policy-and-enforcement-actions}

Därefter måste du se till att rätt marknadsföringsåtgärder anges för importerade data. Du måste också ge samtycke till att data som importeras från Real-Time CDP används för datasamarbete.

Använd marknadsföringsåtgärder för att styra vilka målgruppsdata som ska importeras till Real-Time CDP Collaboration från Experience Platform. Marknadsföringsåtgärden **Data Collaboration** stöder etiketter för C4-, C5- och C9-dataanvändning. Marknadsföringsåtgärden **Data Science** stöder C9-dataanvändningsetiketten.

Läs mer om etiketterna för dataanvändning i [C4, C5 och C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Med kryssrutan *aktiverad* exkluderas alla data som är markerade med etiketterna som anropas ovan i Experience Platform och *hämtas* inte till Real-Time CDP Collaboration.
* Med kryssrutan *inaktiverad* finns det ingen begränsning för data från Experience Platform som kan importeras till Real-Time CDP Collaboration.

Läs mer om dataanvändningsetiketter i Experience Platform-dokumentationen:

* [Översikt över etiketter för dataanvändning](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Etikettordlista för dataanvändning](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

![Marknadsföringsåtgärder som krävs för datasamarbete.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

### Ange information

Ange sedan ett namn och en beskrivning så att du kan känna igen den här dataanslutningen i framtiden.

<!--

>[!IMPORTANT]
>
>Note a difference in terminology where the sandbox selected from Real-Time CDP is considered a dataset in the UI in Real-Time CDP Collaboration.

-->

### Kartfält {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Source"
>abstract="Source-fält är identitetsnamnutrymmen och attribut från din befintliga implementering av Real-Time CDP. Du kan mappa dessa till målfält som definieras i Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Målfält"
>abstract="Målfälten motsvarar de matchningsnycklar som du valde när du introducerade ditt företag. För närvarande är hash-kodade e-postmeddelanden de enda matchningsnycklar som stöds."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Använd omformning"
>abstract="När du importerar *icke-hash*-fält från källan använder du det här alternativet om du vill att Real-Time CDP Collaboration ska tillämpa hash-koden och omforma de enkla fälten till hash-kodade fält."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Identitetsnamnutrymmen"
>abstract="Välj ett identitetsnamnutrymme bland de standardnamnutrymmen och anpassade identitetsnamnutrymmen som finns i din Experience Platform-organisation."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#standard" text="Standard- och identitetsnamnutrymmen i Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Profilattribut"
>abstract="Välj attribut från unionsschemat för klassen Profile i Experience Platform. I den här vyn visas attribut som finns i unionens schema och tillhör klassen XDM Individual Profile."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html" text="Unionsschema i Experience Platform"

![Skärmen Kartfält visar källfält som är mappade till målfält.](/help/assets/setup/add-manage-audiences/Step-Map-Fields.png)

I steget för kartfält kan du välja hur identitetsfält för profilerna som hämtas från dataanslutningen ska mappas till de matchningsnycklar som du har valt i organisationen.

>[!TIP]
>
>Du kan mappa flera källfält till samma målfält. Om du till exempel har e-postadresser i två separata fält i Experience Platform kan du mappa båda dessa till målfältet **[!UICONTROL Hashed email]** som två separata rader.

>[!BEGINSHADEBOX]

**[!UICONTROL Source fields]** anger hur identiteterna refereras i källan som du importerar data från.

**[!UICONTROL Target fields]** anger hur identiteterna refereras i Real-Time CDP Collaboration. De värden som du kan välja här motsvarar matchningsnycklarna som du ställer in i företagets introduktionsarbetsflöde.

Använd alternativet **[!UICONTROL Apply transformation]** när du importerar *icke-hash*-fält från källan. I det här fallet använder Real-Time CDP Collaboration hashen och omformar fälten. Hash-algoritmen som används av Adobe är SHA256.

>[!ENDSHADEBOX]

Lägg till så många mappningspar du behöver och välj **[!UICONTROL Next]** för att fortsätta till nästa steg.

<!--

In this step, you can also add any identity crosswalks that you would like to use.

Identity crosswalks will be supported after the beta release.

#### Add identity crosswalk

Use identity crosswalks to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. 

TODO add GIF Identity crosswalks screen showing a list of available identity crosswalks with details.

Select **[!UICONTROL Add identity crosswalk]** to see a screen where you can choose from various identity crosswalks that you have previously [imported into Real-Time CDP Collaboration](/help/guide/setup/identity-crosswalk.md#import-crosswalk). Each entry includes details such as the table name, type, description, and creation date.

After selecting the desired crosswalk, use a source field join key to map to the crosswalk table join key. 

>[!NOTE]
>
>After selecting an identity crosswalk, the **[!UICONTROL Add identity crosswalk]** control is greyed out. 

For further reading about identity crosswalks, refer to the [glossary](/help/guide/glossary.md).

-->


<!-- will uncomment this part when Manage use cases part becomes available

### Manage use cases {#manage-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_usecases"
>title="Use cases for identities"
>abstract="This control is disabled in the initial release of Real-Time CDP Collaboration"

![Manage use cases screen.](/help/assets/setup/add-manage-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases that you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

Note that this control is disabled in the initial release of Real-Time CDP Collaboration.

After selecting the desired use cases for each identity, proceed to the next step. 

-->

### Schema {#schedule}

Schemalägg när målgrupperna ska börja och sluta med att fylla i och uppdatera. Publiken kommer att uppdateras enligt detta schema.

![Schemaläggningsskärmen visar start- och slutdatum för målgrupper.](/help/assets/setup/add-manage-audiences/Step-Schedule.png)

Välj uppdateringsintervall för målgrupperna. Tillgängliga alternativ är mellan en och sex dagars uppdateringsintervall.

>[!IMPORTANT]
>
>Genom att justera frekvensen för målgruppsuppdateringar kan du hantera [Audience Management-kreditaktiviteten](/help/guide/setup/my-activity.md#types-of-activities), som beräknas för varje målgruppsmedlemskapsuppdatering. Effekten av detta kan bli mindre färska data tillgängliga för målgruppsrapporter och målgruppsdelning och aktivering.

![Schemaläggningsskärmen visar olika frekvensintervall för uppdatering av målgruppsmedlemskap.](/help/assets/setup/add-manage-audiences/Step-Schedule-Set-Frequency.png)

>[!IMPORTANT]
>
>Efter slutdatumet i datumintervallet kommer alla målgrupper som importeras från den här dataanslutningen att sluta uppdatera. Om du vill förnya anslutningen går du till [Hantera dataanslutning](/help/guide/setup/manage-data-connection.md) och anger ett nytt slutdatum.

### Välj målgrupper {#select-audience}

När du har valt målgruppskälla väljer du vilka specifika målgrupper du vill inkludera. Använd sök- och filteralternativen på sidan för att hitta relevanta målgrupper från den valda datakällan.

![Välj målgruppsskärm med en lista över tillgängliga målgrupper med kryssrutor för att välja dem.](/help/assets/setup/add-manage-audiences/Step-Select-Audience.png)

### Granska

Granska alla konfigurationer och inställningar innan du slutför målgruppstillägget. Kontrollera att alla detaljer är korrekta och välj **[!UICONTROL Complete]** för att slutföra processen.

## Visa målgruppspanelen {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Saknade identiteter"
>abstract="Antalet identiteter visar en `-` under ungefär de första 24 timmarna efter att en målgrupp har importerats till Real-Time CDP Collaboration. Efter den här tidsramen uppdateras identitetsantalet med antalet profiler i målgruppen."

När du har importerat målgrupper till Real-Time CDP Collaboration kan du få information om dem i en kontrollpanelsvy. I standardvyn på sidan **[!UICONTROL My audiences]** visas alla målgrupper som din organisation för närvarande importerar till Real-Time CDP Collaboration.

![Sidan Publiköversikt som visar alla målgrupper som importerats av en annonsörer](/help/assets/setup/add-manage-audiences/audiences-overview.png)

Du kan visa följande relevanta information om varje målgrupp:

| Objekt | Beskrivning |
|----------|---------|
| **[!UICONTROL Identities]** | Anger antalet identiteter som finns i den här målgruppen. Observera att om samma profil har två eller flera identiteter och dessa identiteter används som matchningsnycklar i projektet, visas profilen två gånger i antalet. |
| **[!UICONTROL Status]** | Anger om målgruppen är aktiv och kan användas i projekt. En väntande status anger att målgruppen nyligen har importerats och att målgruppsmedlemmarna ännu inte har fyllt i. De importerade målgrupperna har vanligtvis profiler inom 24 timmar. |
| **[!UICONTROL Source]** | Anger källan som målgruppen importerades från. I den aktuella versionen av Real-Time CDP Collaboration är Adobe Experience Platform den enda källa som stöds. |
| **[!UICONTROL Data connection]** | Mer detaljerad information om var den här målgruppen importerades från. Om du till exempel importerar målgrupper från Experience Platform-källan betraktas de enskilda sandlådor som din organisation har åtkomst till som dataanslutningar. |
| **[!UICONTROL Connection access]** | Definierar om den här målgruppen är privat eller offentlig. Offentliga målgrupper kan upptäckas i överlappande rapporter och kan delas med medarbetare. |
| **[!UICONTROL Created]** | Anger när målgruppen importerades till Real-Time CDP Collaboration. |
| **[!UICONTROL Last updated]** | Anger det senaste datumet och den senaste tidpunkten då någon aspekt av den här målgruppen uppdaterades. |

Välj **[!UICONTROL Manage data connections]** om du vill visa och redigera alla dataanslutningar som du har konfigurerat.
Markera elipsen och **[!UICONTROL Delete]** för att ta bort målgruppen.
Markera listan och **[!UICONTROL Edit categories]** om du vill lägga till olika kategoritaggar för målgruppen. Mer information finns i avsnittet [categories](/#categories) nedan.
Välj målgruppens namn för att inspektera eller redigera enskilda målgrupper.

## Visa enskilda målgrupper {#view-individual-audiences}

Publiken visar mer information om er målgrupp.

![Visa och inspektera enskilda målgrupper.](/help/assets/setup/add-manage-audiences/view-inspect-audience.png)

Mätvärden som du kan visa på den här skärmen beskrivs nedan:

| Objekt | Beskrivning |
|----------|---------|
| **[!UICONTROL Status]** | Anger om målgruppen är aktiv och kan användas i projekt. |
| **[!UICONTROL Source]** | Anger källan som målgruppen importerades från. I den aktuella versionen av Real-Time CDP Collaboration är Adobe Experience Platform den enda källa som stöds. |
| **[!UICONTROL Data connection]** | Mer detaljerad information om var den här målgruppen importerades från. Om du till exempel importerar målgrupper från Experience Platform-källan betraktas de enskilda sandlådor som din organisation har åtkomst till som dataanslutningar. |
| **[!UICONTROL Last updated]** | Anger det senaste datumet och den senaste tidpunkten då någon aspekt av den här målgruppen uppdaterades. |
| **[!UICONTROL Last updated by]** | Anger den användare som senast uppdaterade den här målgruppen. |
| **[!UICONTROL Created]** | Anger när målgruppen importerades till Real-Time CDP Collaboration. |
| **[!UICONTROL Created by]** | Anger den användare som importerade målgruppen till Real-Time CDP Collaboration. |


Du kan använda ytterligare två kontroller på sidan för att redigera eller ta bort målgrupper:

* **[!UICONTROL Delete]**: Ta bort målgruppen från ditt lager
* **[!UICONTROL Edit]**: Redigera målgruppsmetadata som namn eller beskrivning.

![Visa och inspektera enskilda målgrupper.](/help/assets/setup/add-manage-audiences/audiences-edit-delete-controls.png)

Mer information om publiken finns i widgetarna nedan och kan delvis redigeras:

![Visa och inspektera enskilda målgrupper.](/help/assets/setup/add-manage-audiences/audiences-further-info-boxes.png)

* [Identiteter](#identities)
* [Kategorier](#categories)
* [Anslutningsåtkomst](#connection-access)
* [Synlighet för metadata](#metadata-visibility)

### Identiteter {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identiteter"
>abstract="Få en detaljerad bild av de identiteter som den här målgruppen består av, samt ett totalt antal profiler med respektive identitet."

I det här avsnittet anges antalet profiler som finns i målgruppen med någon av de identiteter som du angav när du importerade målgrupperna. Avsnittet innehåller också en identitetsuppdelning som gör att du kan se vilka identiteter som utgör det mesta av målgruppen.

### Kategorier {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Kategorier"
>abstract="Tagga era målgrupper för enkel sortering, filtrering och hämtning. Du kan tagga en målgrupp med flera kategorier och sedan använda dessa kategoritaggar för att filtrera de önskade målgrupperna i andra delar av produkten."

För smidig målgruppsorganisation, filtrering och hämtning kan ni tagga era målgrupper. Du kan tagga en målgrupp med flera kategorier och sedan använda dessa kategoritaggar för att filtrera dina önskade målgrupper i produktområdet [discover](/help/guide/collaborate/discover.md) när målgrupper överlappar rapporter.

### Anslutningsåtkomst {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Anslutningsåtkomst"
>abstract="<p>Målgrupper kan vara av tre typer: public, private och custom.</p><p> Hur tillgängliga de är för användning i projekt med medarbetare varierar beroende på inställningen för anslutningsåtkomst. Du kan alltid ändra anslutningsåtkomsten från privat till offentlig, men du kan inte ändra den inställningen igen när en målgrupp har delats med medarbetare.</p>"

Välj om målgruppen ska vara privat eller användbar och kan identifieras i anslutningar. De tre tillgängliga alternativen är:

* **[!UICONTROL Public audience]**. Dessa målgrupper kan användas i överlappningsrapporter och för delning och aktivering i kontakter med medarbetare.
* **[!UICONTROL Private audience]**. Dessa målgrupper är *inte* tillgängliga för användning i överlappningsrapporter och för delning och aktivering i anslutningar med medarbetare. Även om det inte går att visa eller använda för medarbetare, bidrar målgruppens population fortfarande till den totala populationen i vyn **[!UICONTROL All audiences]** i avsnittet [Identifiera och överlappa ](/help/guide/collaborate/discover.md#compare-audiences). Ändra inställningen till publik eller anpassad för att använda målgrupperna i anslutningar med medarbetare.
* **[!UICONTROL Custom audience]**. Dessa målgrupper kan endast användas i överlappningsrapporter och för delning och aktivering i angivna anslutningar. Även om alla medarbetare inte kan visa eller använda, bidrar målgruppens population fortfarande till den totala populationen i vyn **[!UICONTROL All audiences]** i avsnittet [Identifiera och överlappa ](/help/guide/collaborate/discover.md).

>[!IMPORTANT]
>
>Oavsett åtkomststatus (public, private eller custom) bidrar alla målgruppers populationer till **[!UICONTROL All audiences]**-populationen i vyn för överlappningsanalys för Audience Discovery. <br> ![Den systemgenererade målgruppen **Alla målgrupper** i överlappningsanalysen för Audience Discovery omfattar målgrupper med alla anslutningsåtkomststatusar (public, private, custom).](/help/assets/setup/add-manage-audiences/all-audiences-view.png "Den systemgenererade **Alla målgrupper** i överlappningsanalysen **Audience Discovery** omfattar målgrupper med alla anslutningsåtkomststatusar (public, private, custom)."){width="100" zoomable="yes"}

Tillgängligheten för målgrupper som kan användas i projekt med medarbetare skiljer sig åt beroende på inställningen för anslutningsåtkomst. Du kan alltid ändra anslutningsåtkomsten från privat till offentlig, men du kan inte ändra den inställningen igen när en målgrupp har delats med medarbetare.

### Synlighet för metadata {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Synlighet för metadata"
>abstract="<p>Anger vilken av målgruppens metadatainformation som är synlig för andra organisationer innan de ansluter till din organisation. </p> <p> **Identitetsantal** kontrollerar om din partner kan visa identitetsantal för dina målgrupper när du visar överlappningsrapporter på identifieringsfliken. **Målgruppen överlappar %** kontrollerar om medarbetare kan identifiera överlappande procentandelar mellan sina målgrupper och dina."

>[!NOTE]
>
>Om din medarbetare har alla målgrupper inställda på privata blir **[!UICONTROL Relevant audiences]**-vyn i målgruppsinsikter tom. [Läs mer](/help/guide/collaborate/discover.md#relevant-audiences).

Anger vilken av målgruppens metadatainformation som är synlig för andra organisationer innan de ansluter till din organisation eller inom olika projektvyer.

**[!UICONTROL Show identity count]**: Den här inställningen kontrollerar om din partner kan visa identitetsantal för dina målgrupper när [överlappningsrapporter visas på identifieringsfliken](/help/guide/collaborate/discover.md#discover-overlaps).

![Bilder sida vid sida med alternativet för att visa identitetsantal avmarkerat och markerat.](/help/assets/setup/add-manage-audiences/show-identity-count.png)

**[!UICONTROL Show audience overlap %]**: När värdet är true kan medarbetare [upptäcka överlappande procentandelar](/help/guide/collaborate/discover.md#compare-audiences) mellan sina målgrupper och den målgrupp som tillhör dig. I inspelningen nedan har till exempel målgruppen `agora-advertiser-aud3` den här konfigurationen inställd på true och en medarbetare kan visa överlappande procentsatser med den målgruppen. Publiken `agora-advertiser-aud1` har den här inställningen inställd på false, så medarbetaren kan inte visa procentvärden för överlappning.

![Målgruppen överlappar procentandelen för två olika målgrupper.](/help/assets/setup/add-manage-audiences/audience-overlap-percentage.gif)

## Nästa steg

När du har importerat målgrupper kan du använda avsnittet [Anslut](/help/guide/connect/establishing-connections.md) för att identifiera utgivare som kan ansluta till och börja samarbeta i projekt.
