---
title: Source och hantera målgrupper
description: Lär dig hur du hämtar och hanterar målgrupper i Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 2f2a128f1591ac864d2ebef09c58ecc93bed8d98
workflow-type: tm+mt
source-wordcount: '2863'
ht-degree: 0%

---

# Source och hantera målgrupper

{{limited-availability-release-note}}

Målgrupper är specifika grupper av användare eller kunder som segmenteras utifrån olika attribut. Dessa gör det möjligt för medarbetare att samarbeta om riktad marknadsföring och personaliserade upplevelser för mer effektiva annonskampanjer. Den här guiden beskriver hur du hämtar målgrupper till Real-Time CDP Collaboration, visar målgruppspanelen och hanterar enskilda målgrupper.

>[!BEGINSHADEBOX]

Vad du hittar på den här dokumentationssidan:

* [Source målgrupper i Collaboration](#source-audiences)
* [Visa målgruppspanelen](#view-audiences-dashboard)
* [Visa enskilda målgrupper](#view-individual-audiences)

>[!ENDSHADEBOX]

## Source målgrupper i Collaboration {#source-audiences}

>[!IMPORTANT]
>
>Om du vill skapa en källa för målgrupper måste användaren tilldelas en roll som innehåller två behörigheter för profilhantering - **[!UICONTROL View Profiles]** och **[!UICONTROL View Segments]**. Mer information om hur du tilldelar nödvändiga behörigheter finns i [målgruppskällans](../permissions/overview.md#audience-sourcing)-handboken om behörigheter.

Innan ni kan aktivera målgrupper med medarbetare och köra överlappningsberäkningar måste målgrupperna hämtas till Collaboration. Om du vill hämta målgrupper följer du arbetsflödesstegen i avsnittet nedan.

Välj ikonen Lägg till (**[!UICONTROL My audiences]** ikonen Lägg till) på fliken **[!UICONTROL Setup]** på arbetsytan ![.](/help/assets/icons/plus.png)) och välj sedan **[!UICONTROL Audience]**. Om det här är din första målgrupp kan du även välja alternativet **[!UICONTROL Add]**.

![Min målgruppsarbetsyta med alternativet Lägg till och Publiker markerat.](/help/assets/setup/add-manage-audiences/add-audiences.png)

### Välj dataanslutning {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Marknadsföringsåtgärder"
>abstract="<p>Använd marknadsföringsåtgärder för att styra vilka målgruppsdata som ska importeras till Real-Time CDP Collaboration från Experience Platform. Marknadsföringsåtgärden <strong>Data Collaboration</strong> stöder etiketter för C4-, C5- och C9-dataanvändning. Marknadsföringsåtgärden <strong>Data Science</strong> stöder C9-dataanvändningsetiketten.</p> <p> <ul><li> Med kryssrutan <em>aktiverad</em> exkluderas alla data som är markerade med etiketterna som anropas ovan i Experience Platform och <strong>hämtas </strong> inte till Real-Time CDP Collaboration.</li><li> Med kryssrutan <em>inaktiverad</em> finns det ingen begränsning för data från Experience Platform som kan importeras till Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html" text="Översikt över etiketter för dataanvändning"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html" text="Etikettordlista för dataanvändning"

>[!IMPORTANT]
>
>När du har upprättat till din första dataanslutning och importerat din första målgrupp kan du sedan importera flera målgrupper från den befintliga dataanslutningen. När du lägger till ytterligare målgrupper börjar du med steget [välj målgrupp](#select-audiences) eftersom dataanslutningen redan har upprättats.

En dataanslutning är datakällan som du hämtar målgrupper från. För närvarande är Adobe Experience Platform den enda dataanslutning som stöds.

Alla inställningar, till exempel schemaläggning som du konfigurerar för dataanslutningen, tillämpas på alla målgrupper som kommer från den här dataanslutningen.

>[!TIP]
>
>Det finns ett separat arbetsflöde där du kan visa och redigera dina dataanslutningar. Mer information finns i guiden [Hantera dataanslutningar](/help/guide/setup/manage-data-connection.md).

Om du vill börja lägga till din dataanslutning väljer du **[!UICONTROL Add a new data connection]** och sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med alternativet Lägg till en ny dataanslutning markerat.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

#### Välj datakälla

Därefter väljer du källa för dataanslutningen. De tillgängliga källorna är:

* **Adobe Experience Platform**: Välj det här alternativet om du vill hämta målgrupper från Adobe Experience Platform.
* **CSV-fil** (kommande version): Överför en CSV-fil som innehåller målgruppsdata för snabb och enkel datainhämtning.
* **Amazon Web Services** (kommande version): Anslut till din Amazon S3-lagring för att hämta målgruppsdata direkt från dina S3-bucket.
* **Snowflake** (kommande version): Använd Snowflake datalager för att hämta in målgruppsdata sömlöst.
* **Google Cloud-plattform** (kommande version): Anslut till Google Cloud-lagringsutrymmet för att hämta målgruppsdata direkt från dina GCS-bibliotek.

Välj datakälla och välj sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med alternativet Adobe Experience Platform markerat.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png)

#### Välj sandlåda

När du har valt datakälla måste du välja den sandlåda som innehåller de målgrupper som du vill använda Collaboration. Markera sandlådan i listan över tillgängliga sandlådor och välj sedan **[!UICONTROL Next]**

![Arbetsytan Lägg till målgrupper med en markerad sandlåda.](/help/assets/setup/add-manage-audiences/select-sandbox.png)

#### Styrningspolitik och verkställighetsåtgärder {#governance-policy-and-enforcement-actions}

Därefter måste du se till att rätt marknadsföringsåtgärder ställs in på källdata. Du måste också ge medgivande för att data från Experience Platform ska kunna användas för datasamarbete.

Använd marknadsföringsåtgärder för att styra vilka målgruppsdata som ska hämtas till Collaboration från Experience Platform. Marknadsföringsåtgärden **[!UICONTROL Data Collaboration]** stöder etiketter för dataanvändning i C4, C5 och C9. Marknadsföringsåtgärden **[!UICONTROL Data Science]** stöder etiketten för C9-dataanvändning.

Läs mer om etiketterna för dataanvändning i [C4, C5 och C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* När kryssrutan är ***aktiverad*** exkluderas alla data som är märkta i Experience Platform enligt beskrivningen ovan och **hämtas inte** till Collaboration.
* Med kryssrutan ***inaktiverad*** finns ingen begränsning för data som har hämtats från Experience Platform.

Läs mer om dataanvändningsetiketter i Experience Platform-dokumentationen:

* [Översikt över etiketter för dataanvändning](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Etikettordlista för dataanvändning](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Dessutom vill du välja vilka regler för samtycke som ska gälla för data som hämtas till Collaboration.

![Arbetsytan Lägg till målgrupper i avsnittet Styrningsprincip och verkställighetsåtgärder.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

När du har valt marknadsföringsåtgärder och godkännanderegler väljer du **[!UICONTROL Next]** för att fortsätta till nästa steg. En bekräftelsedialogruta visas där du ombeds godkänna villkoren. Markera kryssrutan och markera sedan **[!UICONTROL OK]** för att bekräfta.

![Dialogrutan Styrningsprincip och verkställandeåtgärder med kryssrutan och alternativet OK markerat.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png)

### Ange information

Ange sedan ett namn och en beskrivning för dataanslutningen. Den här informationen hjälper dig att identifiera dataanslutningen senare.

![Arbetsytan Lägg till målgrupper med alternativet att ange ett namn och en beskrivning.](/help/assets/setup/add-manage-audiences/data-connection-details.png)

### Kartfält {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Source"
>abstract="Source-fält är identitetsnamnutrymmen och attribut från din implementering av Experience Platform. Du kan mappa dessa till målfält som definieras i Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Målfält"
>abstract="För närvarande är hash-kodade e-postmeddelanden de enda matchningsnycklar som stöds."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Använd omformning"
>abstract="När du hämtar *icke-hash*-fält kan du använda det här alternativet om du vill att Collaboration ska tillämpa hashningen och omforma de enkla fälten till hash-kodade fält."

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

Därefter väljer du källfält som ska mappas till målfält i Collaboration.

![Arbetsytan Lägg till målgrupper med alternativet att mappa källfält till målfält.](/help/assets/setup/add-manage-audiences/add-map-fields.png)

>[!TIP]
>
>Du kan mappa flera källfält till samma målfält. Om du till exempel har e-postadresser i två separata fält i Experience Platform kan du mappa var och en av dem till målfältet **[!UICONTROL Hashed email]** som två separata rader.

>[!BEGINSHADEBOX]

**[!UICONTROL Source fields]** är identitetsnamnutrymmen och attribut från Experience Platform. Det är så här identiteterna finns i plattformen som du hämtar data från. Source-fält mappas till målfälten som definierats i Collaboration.

**[!UICONTROL Target fields]** anger hur identiteterna refereras i Collaboration. För närvarande är hash-kodade e-postmeddelanden de enda matchningsnycklar som stöds.

Använd alternativet **[!UICONTROL Apply transformation]** när du importerar *icke-hash*-fält från källan. I det här fallet använder Collaboration hashen och omformar fälten. Hash-algoritmen som används av Adobe är SHA256.

>[!ENDSHADEBOX]

Markera det tomma källfältet bredvid målfältet. Dialogrutan **[!UICONTROL Select source field]** visas. Välj mellan alternativen **[!UICONTROL Identity namespaces]** och **[!UICONTROL Profile attributes]** för att hitta det önskade källfältet och välj sedan fältet i listan. Du kan också använda sökalternativet för att hitta det önskade fältet.

![Dialogrutan Välj källfält med e-postalternativen visade.](/help/assets/setup/add-manage-audiences/select-source-field.png)

Om du vill hantera flera e-postfält mappar du det icke-hash-kodade e-postkällfältet med **[!UICONTROL Apply transformation]**.

![Arbetsytan Lägg till målgrupper med e-postkällfälten mappade till målfältet, med Apply-omvandling aktiverad för ett.](/help/assets/setup/add-manage-audiences/apply-transformation.png)

Fortsätt lägga till mappningspar efter behov och välj sedan **[!UICONTROL Next]**.

### Schema {#schedule}

Schemalägg sedan när målgrupperna ska börja och sluta. Publiken kommer att uppdateras enligt detta schema.

![Arbetsytan Lägg till målgrupp med schemaläggningsalternativen visas.](/help/assets/setup/add-manage-audiences/audience-scheduling.png)

>[!IMPORTANT]
>
>Genom att justera frekvensen för målgruppsuppdateringar kan du hantera [Audience Management-kreditaktiviteten](/help/guide/setup/my-activity.md#types-of-activities), som beräknas per målgruppsuppdatering. Om du väljer en högre frekvens kan det påverka aktualiteten hos de data som är tillgängliga för målgruppsrapporter och målgruppsaktivering.

Välj frekvensen för målgruppsuppdateringen i listrutan **[!UICONTROL Frequency]**.

![Arbetsytan Lägg till målgruppsplanering med listrutan Frekvens öppen.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png)

Välj sedan **[!UICONTROL Date range]**. Startdatumet är det datum då målgruppen börjar fylla i profiler och slutdatumet är då målgruppen slutar uppdatera.

![Arbetsytan Lägg till målgruppsplanering med alternativet Datumintervall visas.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png)

>[!IMPORTANT]
>
>Efter slutdatumet i datumintervallet kommer alla målgrupper som kommer från den här dataanslutningen att sluta uppdatera. Om du vill förnya anslutningen följer du guiden [Hantera dataanslutning](/help/guide/setup/manage-data-connection.md).

### Välj målgrupper {#select-audiences}

När du har valt målgruppskälla väljer du vilka specifika målgrupper du vill inkludera. Använd sök- och filteralternativen för att hitta relevanta målgrupper från datakällan. Välj önskade målgrupper och välj sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med en lista över tillgängliga målgrupper.](/help/assets/setup/add-manage-audiences/select-audience.png)

### Granska

Granska alla konfigurationer och inställningar innan du slutför målgruppstillägget. Kontrollera att alla detaljer är korrekta och välj sedan **[!UICONTROL Complete]** för att slutföra dataanslutningen.

![Arbetsytan Lägg till målgrupper med alla valda konfigurationer visas.](/help/assets/setup/add-manage-audiences/review-connection.png)

## Visa målgruppspanelen {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Saknade identiteter"
>abstract="Antalet identiteter blir tillgängligt efter nästa dataanslutningsuppdatering enligt det konfigurerade schemat. Den första uppdateringen sker vanligtvis inom 24 timmar efter att dataanslutningen har konfigurerats. Pågående uppdateringar följer det konfigurerade schemat."

När målgrupper har hämtats visar arbetsytan i **[!UICONTROL My audiences]** alla målgrupper som för närvarande är inhämtade i Collaboration.

Varje målgrupp innehåller en översikt över följande information:

| Objekt | Beskrivning |
|----------|---------|
| **[!UICONTROL Identities]** | Anger antalet identiteter som finns i den här målgruppen. Observera att om samma profil har två eller flera identiteter och dessa identiteter används som matchningsnycklar i projektet, visas profilen två gånger i antalet. |
| **[!UICONTROL Status]** | Anger om målgruppen är aktiv och kan användas i projekt. En **[!UICONTROL Pending]**-status anger att målgruppen nyligen har skapats och att identiteterna ännu inte har fyllts i. Källgrupperna kommer att fylla i profiler efter den första uppdateringen, som vanligtvis sker inom 24 timmar efter att dataanslutningen har konfigurerats. |
| **[!UICONTROL Source]** | Anger var målgruppen kom ifrån. I den aktuella versionen av Collaboration är Experience Platform den enda källa som stöds. |
| **[!UICONTROL Data connection]** | Den dataanslutning som målgruppen kommer ifrån. Du kan markera namnet för att visa dataanslutningen. |
| **[!UICONTROL Connection access]** | Definierar om målgruppen är privat eller offentlig. Offentliga målgrupper kan upptäckas i överlappande rapporter och kan aktiveras inom ett projekt. |
| **[!UICONTROL Created]** | Anger när målgruppen ursprungligen kom till Collaboration. |
| **[!UICONTROL Last updated]** | Anger det senaste datumet och den senaste tidpunkten då målgruppen uppdaterades i Collaboration. Detta gäller inte när målgruppen senast uppdaterades, utan snarare när målgruppens konfiguration eller metadata senast ändrades. |

![Arbetsytan Min målgrupp visar alla målgrupper som har hämtats.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Om du vill utföra snabba åtgärder för en målgrupp väljer du ellipsen **...** bredvid målgruppens namn. Följande alternativ är tillgängliga:

* Med **[!UICONTROL Edit categories]** kan du lägga till olika kategoritaggar för målgruppen. Mer information finns i avsnittet [categories](#categories) nedan.
* **[!UICONTROL Delete]** tar bort målgruppen från dataanslutningen.

![Arbetsytan Mina målgrupper med ellipsmenyn öppen och kategorierna Redigera och Ta bort markerade.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png)

## Visa enskilda målgrupper {#view-individual-audiences}

Om du vill visa mer information och redigera konfigurationer för en enskild målgrupp väljer du målgruppen på arbetsytan **[!UICONTROL My audiences]**. På målgruppsarbetsytan visas detaljerad information om den valda målgruppen, inklusive information, identiteter, kategorier, anslutningsåtkomst och inställningar för metadatavisning.

### Målgruppsinformation

Följande information visas för varje enskild målgrupp:

| Objekt | Beskrivning |
|----------|---------|
| **[!UICONTROL Status]** | Anger om målgruppen är aktiv och kan användas i projekt. |
| **[!UICONTROL Source]** | Anger var målgruppen kom ifrån. I den aktuella versionen av Collaboration är Experience Platform den enda källa som stöds. |
| **[!UICONTROL Data connection]** | Den dataanslutning som målgruppen kommer ifrån. |
| **[!UICONTROL Last updated]** | Anger det senaste datumet och den senaste tidpunkten då målgruppen uppdaterades i Collaboration. Detta gäller inte när målgruppen senast uppdaterades, utan snarare när målgruppens konfiguration eller metadata senast ändrades |
| **[!UICONTROL Last updated by]** | Anger den användare som senast uppdaterade målgruppen. |
| **[!UICONTROL Created]** | Anger när målgruppen ursprungligen kom till Collaboration. |
| **[!UICONTROL Created by]** | Anger den användare som köpte målgruppen till Collaboration. |

![En enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details.png)

Dessutom är följande kontroller tillgängliga på arbetsytan för målgrupper:

* **[!UICONTROL Delete]**: Ta bort målgruppen från din dataanslutning.
* **[!UICONTROL Edit]**: Redigera publikens namn eller beskrivning.

![En enskild målgrupps arbetsyta med alternativet Redigera och ta bort markerat.](/help/assets/setup/add-manage-audiences/audience-details-edit-delete.png)

Därefter kan du uppdatera följande avsnitt på målgruppens arbetsyta:

* [Identiteter](#identities)
* [Kategorier](#categories)
* [Anslutningsåtkomst](#connection-access)
* [Synlighet för metadata](#metadata-visibility)

### Identiteter {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identiteter"
>abstract="En detaljvy över de identiteter som den här målgruppen består av samt det totala antalet profiler med respektive identitet."

Avsnittet **[!UICONTROL Identities]** anger antalet profiler i målgruppen med någon av de identiteter du valde när du hämtade målgruppen. Avsnittet innehåller också en identitetsuppdelning som gör att du kan se vilka identiteter som utgör det mesta av målgruppen.

![Avsnittet Identiteter i en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

### Kategorier {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Kategorier"
>abstract="Tagga era målgrupper för enkel sortering, filtrering och hämtning. Du kan tagga en målgrupp med flera kategorier och sedan använda dessa kategoritaggar för att filtrera de önskade målgrupperna i andra delar av produkten."

För smidig målgruppsorganisation, filtrering och hämtning kan ni tagga era målgrupper. Du kan tagga en målgrupp med flera kategorier och sedan använda dessa kategoritaggar för att filtrera dina önskade målgrupper i produktområdet [discover](/help/guide/collaborate/discover.md) när målgrupper överlappar rapporter.

Om du vill lägga till kategorier väljer du alternativet **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Categories]**.

![Kategoriavsnittet för en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-categories.png)

Dialogrutan **[!UICONTROL Categories]** visas så att du kan välja de kategorier som du vill lägga till för målgruppen. Om du vill välja en enskild kategori markerar du kryssrutan bredvid kategorinamnet.

![Dialogrutan Kategorier med tillgängliga kategorier visas.](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png)

### Anslutningsåtkomst {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Anslutningsåtkomst"
>abstract="<p>Målgrupper kan vara av tre typer: public, private och custom.</p><p> Hur tillgängliga de är för användning i projekt med medarbetare varierar beroende på inställningen för anslutningsåtkomst. Du kan alltid ändra anslutningsåtkomsten från privat till offentlig, men du kan inte ändra den inställningen igen när en målgrupp har aktiverats med medarbetare.</p>"

En målgrupps tillgänglighet för användning i projekt med medarbetare skiljer sig åt beroende på inställningen för anslutningsåtkomst. I avsnittet **[!UICONTROL Connection access]** kan du välja om målgruppen ska vara privat eller offentlig. Offentliga målgrupper kan användas och upptäckas i kontakter.

Om du vill uppdatera målgruppens anslutningsåtkomst väljer du alternativet **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Connection access]**.

![Avsnittet Anslutningsåtkomst för en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png)

Dialogrutan **[!UICONTROL Connection access]** visas med tre tillgängliga anslutningsåtkomstalternativ:

* **[!UICONTROL Private audience]**. Dessa målgrupper är *inte* tillgängliga för användning i överlappningsrapporter eller för aktivering i anslutningar med medarbetare. Även om målgrupperna inte är tillgängliga för medarbetare att visa eller använda, bidrar målgruppspopulationen fortfarande till den totala populationen i vyn **[!UICONTROL All audiences]** i avsnittet [Jämför målgrupper](/help/guide/collaborate/discover.md#compare-audiences). Ändra inställningen till publik eller anpassad för att använda målgrupperna i anslutningar med medarbetare.
* **[!UICONTROL Public audience]**. Dessa målgrupper kan användas i överlappningsrapporter och för aktivering i kontakter med medarbetare.
* **[!UICONTROL Custom audience]**. Dessa målgrupper är tillgängliga för användning i överlappningsrapporter och för aktivering endast i angivna anslutningar. Även om målgrupperna inte är tillgängliga för medarbetare att visa eller använda, bidrar målgruppspopulationen fortfarande till den totala populationen i vyn **[!UICONTROL All audiences]** i avsnittet [Jämför målgrupper](/help/guide/collaborate/discover.md#compare-audiences).

Välj önskat alternativ för anslutningsåtkomst och välj sedan **[!UICONTROL Save]** för att tillämpa ändringarna.

![Dialogrutan Anslutningsåtkomst med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

>[!IMPORTANT]
>
>Oberoende av åtkomststatus (public, private eller custom) bidrar målgruppspopulationen till **[!UICONTROL All audiences]**-populationen i **[!UICONTROL Compare audiences]** -avsnittet i ett projekt.

Tillgängligheten för målgrupper som kan användas i projekt med medarbetare skiljer sig åt beroende på inställningen för anslutningsåtkomst. Du kan alltid ändra anslutningsåtkomsten från privat till offentlig, men du kan inte ändra den inställningen igen när en viss målgrupp har aktiverats.

### Synlighet för metadata {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Synlighet för metadata"
>abstract="<p>Anger vilka av målgruppens metadata som är synliga för andra medarbetare innan de ansluter till dig eller inom projektvyer.</p> <p> **Identitetsantal** kontrollerar om din medarbetare kan visa identitetsantal för dina målgrupper när de visar överlappningsrapporter på fliken Identifiering.</p><p> **Målgruppen överlappar %** kontrollerar om medarbetare kan identifiera överlappande procentandelar mellan sina målgrupper och dina.</p><p> **[!UICONTROL Audience index]** kontrollerar om medarbetare kan visa målgruppsindexet i ett projekt. Den här funktionen är bara tillgänglig om du har tre eller fler aktiva målgrupper.</p> <br> För att inställningarna för metadatasynlighet ska börja gälla måste målgruppen anges till public eller custom."

>[!NOTE]
>
>Om din medarbetare har alla målgrupper inställda på privata, kommer **[!UICONTROL Relevant audiences]**-avsnittet i arbetsytan **[!UICONTROL Discover]** för ett projekt att vara tomt. Mer information finns i guiden [Upptäck](/help/guide/collaborate/discover.md#relevant-audiences).

Metadatasynlighet anger synligheten för en målgrupps metadata till andra medarbetare innan de ansluter till dig, eller inom olika projektvyer. Om du vill uppdatera målgruppens metadatasynlighet väljer du alternativet **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Metadata visibility]**.

![Sektionen för metadatavisning för en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-metadata.png)

Dialogrutan **[!UICONTROL Metadata visibility]** visas så att du kan konfigurera visningsinställningar för målgruppen. Det finns två inställningar för metadatasynlighet som du kan konfigurera för varje målgrupp:

**[!UICONTROL Show identity count]**: Den här inställningen kontrollerar om din medarbetare kan visa identitetsantal för dina målgrupper när [du visar överlappningsrapporter på identifieringsfliken](/help/guide/collaborate/discover.md#discover-overlaps) i ett projekt.

**[!UICONTROL Show audience overlap %]**: Den här inställningen kontrollerar om medarbetare kan [identifiera överlappande procentandelar](/help/guide/collaborate/discover.md#compare-audiences) mellan sina målgrupper och dina målgrupper.

**[!UICONTROL Audience index]**: Om värdet är true kan dina medarbetare visa [målgruppsindexet](/help/guide/collaborate/discover.md#audience-index-score) i ett projekt. Den här funktionen är bara tillgänglig om du har tre eller fler aktiva målgrupper.

>[!NOTE]
>
>För att inställningarna för metadatasynlighet ska börja gälla måste målgruppen ställas in på public eller custom.

![Dialogrutan för synlighet av metadata med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

## Nästa steg

Efter att målgrupper har inhämtats är det dags att identifiera utgivare att [ansluta](/help/guide/connect/establishing-connections.md) till för att samarbeta i projekt.
