---
title: Source och hantera målgrupper
description: Lär dig hur du hämtar och hanterar målgrupper i Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 9355535e067afeedff33f5c6468bc6fcb1f58e08
workflow-type: tm+mt
source-wordcount: '3347'
ht-degree: 0%

---

# Source och hantera målgrupper

{{limited-availability-release-note}}

Målgrupper är specifika grupper av användare eller kunder som segmenteras utifrån olika attribut. Dessa gör det möjligt för medarbetare att samarbeta om riktad marknadsföring och personaliserade upplevelser för mer effektiva annonskampanjer. Den här guiden beskriver hur du hämtar målgrupper till Real-Time CDP Collaboration, visar målgruppspanelen och hanterar enskilda målgrupper.

## Source målgrupper i Collaboration {#source-audiences}

>[!IMPORTANT]
>
>Om du vill skapa en källa för målgrupper måste användaren tilldelas en roll som innehåller två behörigheter för profilhantering - **[!UICONTROL View Profiles]** och **[!UICONTROL View Segments]**. Mer information om hur du tilldelar nödvändiga behörigheter finns i [målgruppskällans](../permissions/overview.md#audience-sourcing)-handboken om behörigheter.

Innan ni kan aktivera målgrupper med medarbetare och köra överlappningsberäkningar måste målgrupperna hämtas till Collaboration. Om du vill hämta målgrupper följer du arbetsflödesstegen i avsnittet nedan.

Välj ikonen Lägg till (**[!UICONTROL My audiences]** ikonen Lägg till) på fliken **[!UICONTROL Setup]** på arbetsytan ![.](/help/assets/icons/plus.png)) och välj sedan **[!UICONTROL Audience]**. Om det här är din första målgrupp kan du även välja alternativet **[!UICONTROL Add]**.

![Min målgruppsarbetsyta med alternativet Lägg till och Publiker markerat.](/help/assets/setup/add-manage-audiences/add-audiences.png){zoomable="yes"}

### Välj dataanslutning {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Marknadsföringsåtgärder"
>abstract="<p>Använd marknadsföringsåtgärder för att styra vilka målgruppsdata som ska importeras till Real-Time CDP Collaboration från Experience Platform. Marknadsföringsåtgärden <strong>Data Collaboration</strong> stöder etiketter för C4-, C5- och C9-dataanvändning. Marknadsföringsåtgärden <strong>Data Science</strong> stöder C9-dataanvändningsetiketten.</p> <p> <ul><li> Med kryssrutan <em>aktiverad</em> exkluderas alla data som är markerade med etiketterna som anropas ovan i Experience Platform och <strong>hämtas </strong> inte till Real-Time CDP Collaboration.</li><li> Med kryssrutan <em>inaktiverad</em> finns det ingen begränsning för data från Experience Platform som kan hämtas till Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html" text="Översikt över etiketter för dataanvändning"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html" text="Etikettordlista för dataanvändning"

>[!IMPORTANT]
>
>När ni har etablerat er till er första dataanslutning och tagit fram den första målgruppen kan ni sedan hämta flera målgrupper från den befintliga dataanslutningen. När du lägger till ytterligare målgrupper börjar du med steget [välj målgrupp](#select-audiences) eftersom dataanslutningen redan har upprättats.

En dataanslutning är datakällan som du hämtar målgrupper från. För närvarande är Adobe Experience Platform den enda dataanslutning som stöds.

Alla inställningar som du konfigurerar för din dataanslutning tillämpas på alla målgrupper som kommer från den här dataanslutningen.

>[!TIP]
>
>Det finns ett separat arbetsflöde där du kan visa och redigera dina dataanslutningar. Mer information finns i guiden [Hantera dataanslutningar](/help/guide/setup/manage-data-connection.md).

Om du vill börja lägga till din dataanslutning väljer du **[!UICONTROL Add a new data connection]** och sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med alternativet Lägg till en ny dataanslutning markerat.](/help/assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

#### Välj datakälla

Därefter väljer du källa för dataanslutningen. De tillgängliga källorna är:

* **Adobe Experience Platform**: Välj det här alternativet om du vill hämta målgrupper från Adobe Experience Platform.
* **CSV-fil** (kommande version): Överför en CSV-fil som innehåller målgruppsdata för snabb och enkel datainhämtning.
* **Amazon Web Services** (kommande version): Anslut till din Amazon S3-lagring för att hämta målgruppsdata direkt från dina S3-bucket.
* **Snowflake** (kommande version): Använd Snowflake datalager för att hämta in målgruppsdata sömlöst.
* **Google Cloud-plattform** (kommande version): Anslut till Google Cloud-lagringsutrymmet för att hämta målgruppsdata direkt från dina GCS-bibliotek.

<!-- Add list item in final draft:
* **Amazon Web Services**: Connect to your Amazon S3 storage to source audience data directly from your S3 buckets. See the [Configure AWS S3 for audience sourcing](./configure-aws-s3-audience-sourcing.md) guide for step-by-step instructions.
 -->

Markera datakällan och välj sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med alternativet Adobe Experience Platform markerat.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png){zoomable="yes"}

#### Välj sandlåda

När du har valt datakälla måste du markera den sandlåda som innehåller de målgrupper som du vill använda för Collaboration. Markera sandlådan i listan över tillgängliga sandlådor och välj sedan **[!UICONTROL Next]**

![Arbetsytan Lägg till målgrupper med en markerad sandlåda.](/help/assets/setup/add-manage-audiences/select-sandbox.png){zoomable="yes"}

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

![Arbetsytan Lägg till målgrupper i avsnittet Styrningsprincip och verkställighetsåtgärder.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png){zoomable="yes"}

När du har valt marknadsföringsåtgärder och godkännanderegler väljer du **[!UICONTROL Next]** för att fortsätta till nästa steg. En bekräftelsedialogruta visas där du ombeds godkänna villkoren. Markera kryssrutan och markera sedan **[!UICONTROL OK]** för att bekräfta.

![Dialogrutan Styrningsprincip och verkställandeåtgärder med kryssrutan och alternativet OK markerat.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png){zoomable="yes"}

### Ange information

Ange sedan ett namn och en beskrivning för dataanslutningen. Den här informationen hjälper dig att identifiera dataanslutningen senare.

![Arbetsytan Lägg till målgrupper med alternativet att ange ett namn och en beskrivning.](/help/assets/setup/add-manage-audiences/data-connection-details.png){zoomable="yes"}

### Kartfält {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Source"
>abstract="Source-fält är identitetsnamnutrymmen och attribut från din implementering av Experience Platform. Du kan mappa dessa till målfält som definieras i Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Målfält"
>abstract="Målfält är de matchningsnycklar som väljs under kontoinställningarna. Som standard är alla matchningsnycklar tillgängliga."

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
>abstract="Välj attribut från unionsschemat för klassen Profile i Experience Platform. I den här vyn visas attribut som finns i unionsschemat och tillhör klassen XDM Individual Profile."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html" text="Unionsschema i Experience Platform"

Därefter väljer du källfält som ska mappas till målfält i Collaboration. Tillgängliga målfält baseras på de matchningsnycklar som du valde under kontokonfigurationen.

>[!IMPORTANT]
>
>För närvarande kan du inte redigera dataanslutningar för att inkludera nya kartfält. Om du lägger till nya matchningsnycklar till ditt konto efter att dataanslutningen har skapats, måste du skapa en ny dataanslutning för att mappa till dem.

![Arbetsytan Lägg till målgrupper med alternativet att mappa källfält till målfält.](/help/assets/setup/add-manage-audiences/add-map-fields.png){zoomable="yes"}

>[!TIP]
>
>Du kan mappa flera källfält till samma målfält. Om du till exempel har e-postadresser i två separata fält i Experience Platform kan du mappa var och en av dem till målfältet **[!UICONTROL Hashed email]** som två separata rader. Använd alternativet **[!UICONTROL Add field]** om du vill lägga till ytterligare mappningsrader.

>[!BEGINSHADEBOX]

**[!UICONTROL Source fields]** är identitetsnamnutrymmen och attribut från Experience Platform. Dessa innehåller både [standard](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#standard){target="_blank"} och [anpassade &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#create-namespaces){target="_blank"} identitetsnamnutrymmen. De innehåller även profilattribut som finns i [union-schemat](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html){target="_blank"} och tillhör klassen XDM Individual Profile.

Source-fält mappas till målfälten som definierats i Collaboration.

**[!UICONTROL Target fields]** anger hur identiteterna refereras i Collaboration. Målfält är de matchningsnycklar som väljs under kontoinställningarna. Som standard är alla matchningsnycklar tillgängliga.

Använd alternativet **[!UICONTROL Apply transformation]** när du hämtar *icke-hash*-fält till hash-kodade fält. Collaboration kommer att tillämpa hashen och omforma fälten. Hash-algoritmen som används av Adobe är SHA256.

>[!ENDSHADEBOX]

Om du vill börja mappa fält markerar du det tomma källfältet bredvid målfältet. Dialogrutan **[!UICONTROL Select source field]** visas. Välj mellan alternativen **[!UICONTROL Identity namespaces]** och **[!UICONTROL Profile attributes]** för att hitta det önskade källfältet och välj sedan fältet i listan. Du kan också använda sökalternativet för att hitta det önskade fältet.

![Dialogrutan Välj källfält med e-postalternativen visade.](/help/assets/setup/add-manage-audiences/select-source-field.png){zoomable="yes"}

Använd alternativet **[!UICONTROL Apply transformation]** om du vill hantera källa för ett icke-hash-kodat fält till ett hash-kodat målfält. Om du till exempel vill lägga till ett andra e-postfält markerar du alternativet **[!UICONTROL Add field]** för att lägga till en ny rad och väljer sedan **[!UICONTROL Hashed email]** som målfält. Markera ett icke-hash-kodat källfält för e-post och välj sedan **[!UICONTROL Apply transformation]**.

![Arbetsytan Lägg till målgrupper med e-postkällfälten mappade till målfältet, med Apply-omvandling aktiverad för ett.](/help/assets/setup/add-manage-audiences/apply-transformation.png){zoomable="yes"}

Fortsätt lägga till mappningspar för varje målfält. Om du inte vill använda en matchningsnyckel kan du ta bort den med ikonen Ta bort (![Ta bort ikon](/help/assets/icons/delete.png)) bredvid fältet. Om matchningsnyckeln tas bort kan du inte använda den när du hämtar målgrupper från anslutningen.

![Arbetsytan Lägg till målgrupper med alternativet Ta bort bredvid ett målfält markerat.](/help/assets/setup/add-manage-audiences/remove-target-field.png){zoomable="yes"}

När du är klar med mappningen av fält väljer du **[!UICONTROL Next]** för att fortsätta.

![Arbetsytan Lägg till målgrupper med kartfälten ifyllda och alternativet Nästa markerat.](/help/assets/setup/add-manage-audiences/confirm-field-mapping.png){zoomable="yes"}

### Schema {#schedule}

Schemalägg sedan när målgrupperna ska börja och sluta. Publiken kommer att uppdateras enligt detta schema.

![Arbetsytan Lägg till målgrupp med schemaläggningsalternativen visas.](/help/assets/setup/add-manage-audiences/audience-scheduling.png){zoomable="yes"}

>[!IMPORTANT]
>
>Genom att justera frekvensen för målgruppsuppdateringar kan du hantera [Audience Management-kreditaktiviteten](/help/guide/setup/my-activity.md#types-of-activities), som beräknas per målgruppsuppdatering. Om du väljer en högre frekvens kan det påverka aktualiteten hos de data som är tillgängliga för målgruppsrapporter och målgruppsaktivering.

Välj frekvensen för målgruppsuppdateringen i listrutan **[!UICONTROL Frequency]**.

![Arbetsytan Lägg till målgruppsplanering med listrutan Frekvens öppen.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png){zoomable="yes"}

Välj sedan **[!UICONTROL Date range]**. Startdatumet är det datum då målgruppen börjar fylla i profiler och slutdatumet är då målgruppen slutar uppdatera.

![Arbetsytan Lägg till målgruppsplanering med alternativet Datumintervall visas.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png){zoomable="yes"}

>[!IMPORTANT]
>
>Efter slutdatumet i datumintervallet kommer alla målgrupper som kommer från den här dataanslutningen att sluta uppdatera. Om du vill förnya anslutningen följer du guiden [Hantera dataanslutning](/help/guide/setup/manage-data-connection.md).

### Välj målgrupper {#select-audiences}

När du har valt målgruppskälla väljer du vilka specifika målgrupper du vill inkludera. Använd sök- och filteralternativen för att hitta relevanta målgrupper från din dataanslutning. Välj önskade målgrupper och välj sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med en lista över tillgängliga målgrupper.](/help/assets/setup/add-manage-audiences/select-audience.png){zoomable="yes"}

### Granska

Granska alla konfigurationer och inställningar innan du slutför målgruppstillägget. Kontrollera att alla detaljer är korrekta och välj sedan **[!UICONTROL Complete]** för att slutföra dataanslutningen.

![Arbetsytan Lägg till målgrupper med alla valda konfigurationer visas.](/help/assets/setup/add-manage-audiences/review-connection.png){zoomable="yes"}

## Visa målgruppspanelen {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Saknade identiteter"
>abstract="Antalet identiteter blir tillgängligt efter nästa dataanslutningsuppdatering enligt det konfigurerade schemat. Den första uppdateringen sker vanligtvis inom 24 timmar efter att dataanslutningen har konfigurerats. Pågående uppdateringar följer det konfigurerade schemat."

När målgrupper har hämtats visar arbetsytan i **[!UICONTROL My audiences]** alla målgrupper som för närvarande är inhämtade i Collaboration.

![Arbetsytan Mina målgrupper visar alla målgrupper som har hämtats.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Varje målgrupp innehåller en översikt över följande information:

| Objekt | Beskrivning |
|----------|---------|
| **[!UICONTROL Name]** | Namnet på publiken. |
| **[!UICONTROL Identities]** | Anger antalet identiteter som finns i den här målgruppen. Observera att om samma profil har två eller flera identiteter och dessa identiteter används som matchningsnycklar i projektet, visas profilen två gånger i antalet. |
| **[!UICONTROL Status]** | Anger om målgruppen är aktiv och kan användas i projekt. En **[!UICONTROL Pending]**-status anger att målgruppen nyligen har skapats och att identiteterna ännu inte har fyllts i. Källgrupperna kommer att fylla i profiler efter den första uppdateringen, som vanligtvis sker inom 24 timmar efter att dataanslutningen har konfigurerats. |
| **[!UICONTROL Source]** | Anger var målgruppen kom ifrån. I den aktuella versionen av Collaboration är Experience Platform den enda källa som stöds. |
| **[!UICONTROL Data connection]** | Den dataanslutning som målgruppen kommer ifrån. Du kan markera namnet för att visa dataanslutningen. |
| **[!UICONTROL Connection access]** | Definierar om målgruppen är privat eller offentlig. Offentliga målgrupper kan upptäckas i överlappande rapporter och kan aktiveras inom ett projekt. |
| **[!UICONTROL Created]** | Anger när målgruppen ursprungligen kom till Collaboration. |
| **[!UICONTROL Last updated]** | Anger det senaste datumet och den senaste tidpunkten då målgruppen uppdaterades i Collaboration. Detta gäller inte när målgruppen senast uppdaterades, utan snarare när målgruppens konfiguration eller metadata senast ändrades. |

![Arbetsytan Min målgrupp visar alla målgrupper som har hämtats.](/help/assets/setup/add-manage-audiences/audiences-workspace.png){zoomable="yes"}

Om du vill utföra snabba åtgärder för en målgrupp väljer du ellipsen **...** bredvid målgruppens namn. Följande alternativ är tillgängliga:

* Med **[!UICONTROL Edit categories]** kan du lägga till olika kategoritaggar för målgruppen. Mer information finns i avsnittet [categories](#categories) nedan.
* **[!UICONTROL Delete]** tar bort målgruppen från dataanslutningen.

![Arbetsytan Mina målgrupper med ellipsmenyn öppen och kategorierna Redigera och Ta bort markerade.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png){zoomable="yes"}

## Visa enskilda målgrupper {#view-individual-audiences}

Om du vill visa och uppdatera information för en enskild målgrupp väljer du målgruppen på arbetsytan **[!UICONTROL My audiences]**. På målgruppsarbetsytan visas detaljerad information om den valda målgruppen, inklusive information, identiteter, kategorier, anslutningsåtkomst och inställningar för metadatasynlighet.

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

![En enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details.png){zoomable="yes"}

#### Identiteter {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identiteter"
>abstract="En detaljvy över de identiteter som den här målgruppen består av, avgränsade med matchningsnyckeln."

Avsnittet **[!UICONTROL Identities]** anger antalet identiteter som finns i målgruppen. Avsnittet innehåller också en identitetsuppdelning av identiteter efter matchningsnyckel som hjälper dig att förstå målgruppens komposition.

![Avsnittet Identiteter i en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-identities.png){zoomable="yes"}

Genom att hovra över de enskilda delarna av uppdelningen av matchningsnycklar får du ett korrekt identitetsantal för den relevanta nyckeln.

![Avsnittet Identiteter i en enskild målgrupps arbetsyta med en matchningsnyckels uppdelning visade.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

#### Kategorier {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Kategorier"
>abstract="Tagga era målgrupper för enkel sortering, filtrering och hämtning. Du kan tagga en målgrupp med flera kategorier och sedan använda dessa kategoritaggar för att filtrera de önskade målgrupperna i andra delar av produkten."

För smidig målgruppsorganisation, filtrering och hämtning kan ni tagga era målgrupper. Du kan tagga en målgrupp med flera kategorier och sedan använda dessa kategoritaggar för att filtrera dina önskade målgrupper i produktområdet [discover](/help/guide/collaborate/discover.md) när målgrupper överlappar rapporter.

Om du vill lägga till kategorier väljer du alternativet **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Categories]**.

![Kategoriavsnittet för en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-categories.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Categories]** visas så att du kan välja de kategorier som du vill lägga till för målgruppen. Om du vill välja en enskild kategori markerar du kryssrutan bredvid kategorinamnet.


#### Anslutningsåtkomst {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Anslutningsåtkomst"
>abstract="<p>Målgrupper kan vara av tre typer: public, private och custom.</p><p> Hur tillgängliga de är för användning i projekt med medarbetare varierar beroende på inställningen för anslutningsåtkomst.</p>"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_access"
>title="Läs mer"
>abstract=""

En målgrupps tillgänglighet för användning i projekt med medarbetare skiljer sig åt beroende på inställningen för anslutningsåtkomst. I avsnittet **[!UICONTROL Connection access]** kan du välja om målgruppen ska vara privat, offentlig eller endast tillgänglig för specifika anslutningar. Offentliga målgrupper kan användas och upptäckas i kontakter.

Om du vill uppdatera målgruppens anslutningsåtkomst väljer du alternativet **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Connection access]**.

![Avsnittet Anslutningsåtkomst för en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Connection access]** visas med tre tillgängliga anslutningsåtkomstalternativ:

* **[!UICONTROL Private audience]**. Dessa målgrupper är *inte* tillgängliga för användning i överlappningsrapporter eller för aktivering i anslutningar med medarbetare. Även om målgrupperna inte är tillgängliga för medarbetare att visa eller använda, bidrar målgruppspopulationen fortfarande till den totala populationen i vyn **[!UICONTROL All audiences]** i avsnittet [Jämför målgrupper](/help/guide/collaborate/discover.md#compare-audiences). Ändra inställningen till publik eller anpassad för att använda målgrupperna i anslutningar med medarbetare.
* **[!UICONTROL Public audience]**. Dessa målgrupper kan användas i överlappningsrapporter och för aktivering i kontakter med medarbetare.
* **[!UICONTROL Custom audience]**. Dessa målgrupper är tillgängliga för användning i överlappningsrapporter och för aktivering endast i angivna anslutningar. Även om målgrupperna inte är tillgängliga för medarbetare att visa eller använda, bidrar målgruppspopulationen fortfarande till den totala populationen i vyn **[!UICONTROL All audiences]** i avsnittet [Jämför målgrupper](/help/guide/collaborate/discover.md#compare-audiences).

Välj önskat alternativ för anslutningsåtkomst och välj sedan **[!UICONTROL Save]** för att tillämpa ändringarna.

![Dialogrutan Anslutningsåtkomst med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png){zoomable="yes"}

>[!IMPORTANT]
>
>Oberoende av åtkomststatus (public, private eller custom) bidrar målgruppspopulationen till **[!UICONTROL All audiences]**-populationen i **[!UICONTROL Compare audiences]** -avsnittet i ett projekt.

Tillgängligheten för målgrupper som kan användas i projekt med medarbetare skiljer sig åt beroende på inställningen för anslutningsåtkomst.

#### Synlighet för metadata {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Synlighet för metadata"
>abstract="<p>Anger vilka av målgruppens metadata som är synliga för andra medarbetare innan de ansluter till dig eller inom projektvyer.</p> <p> **Identitetsantal** kontrollerar om din medarbetare kan visa identitetsantal för dina målgrupper när de visar överlappningsrapporter på fliken Identifiering.</p><p> **Målgruppen överlappar %** kontrollerar om medarbetare kan identifiera överlappande procentandelar mellan sina målgrupper och dina.</p><p> **[!UICONTROL Audience index]** kontrollerar om medarbetare kan visa målgruppsindexet i ett projekt. Den här funktionen är bara tillgänglig om du har tre eller fler aktiva målgrupper.</p> <br> För att inställningarna för metadatasynlighet ska börja gälla måste målgruppen anges till public eller custom."

>[!NOTE]
>
>Om din medarbetare har alla målgrupper inställda på privata, kommer **[!UICONTROL Relevant audiences]**-avsnittet i arbetsytan **[!UICONTROL Discover]** för ett projekt att vara tomt. Mer information finns i guiden [Upptäck](/help/guide/collaborate/discover.md#relevant-audiences).

Metadatasynlighet anger synligheten för en målgrupps metadata till andra medarbetare innan de ansluter till dig, eller inom olika projektvyer. Om du vill uppdatera målgruppens metadatasynlighet väljer du alternativet **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Metadata visibility]**.

![Sektionen för metadatavisning för en enskild målgrupps arbetsyta.](/help/assets/setup/add-manage-audiences/audience-details-metadata-visibility.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Metadata visibility]** visas så att du kan konfigurera visningsinställningar för målgruppen. Det finns två inställningar för metadatasynlighet som du kan konfigurera för varje målgrupp:

**[!UICONTROL Show identity count]**: Den här inställningen kontrollerar om din medarbetare kan visa identitetsantal för dina målgrupper när [du visar överlappningsrapporter på identifieringsfliken](/help/guide/collaborate/discover.md#discover-overlaps) i ett projekt.

**[!UICONTROL Show audience overlap %]**: Den här inställningen kontrollerar om medarbetare kan [identifiera överlappande procentandelar](/help/guide/collaborate/discover.md#compare-audiences) mellan sina målgrupper och dina målgrupper.

**[!UICONTROL Audience index]**: Om värdet är true kan dina medarbetare visa [målgruppsindexet](/help/guide/collaborate/discover.md#audience-index-score) i ett projekt. Den här funktionen är bara tillgänglig om du har tre eller fler aktiva målgrupper.

>[!NOTE]
>
>För att inställningarna för metadatasynlighet ska börja gälla måste målgruppen ställas in på public eller custom.

![Dialogrutan för synlighet av metadata med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png){zoomable="yes"}

## Redigera flera målgrupper {#edit-audiences}

På publiken kan du redigera flera målgrupper samtidigt. Om du vill göra det markerar du de målgrupper du vill redigera genom att markera rutorna bredvid namnen. När du har valt målgrupper kan du utföra åtgärder med alternativen på redigeringsmenyn.

![Arbetsytan Mina målgrupper med två valda målgrupper och redigeringsmenyn markerad.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit.png)

### Redigera metadatasynlighet gruppvis {#bulk-edit-metadata-visibility}

Välj **[!UICONTROL Edit metadata visibility]** på redigeringsmenyn när du har valt dina målgrupper på målgruppspanelen.

![Arbetsytan Mina målgrupper med synlighetsalternativet Redigera metadata markerat.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-metadata.png)

Dialogrutan **[!UICONTROL Metadata visibility]** visas, där du kan konfigurera synlighetsinställningarna för de valda målgrupperna. Som standard markeras inget av alternativen. Välj de alternativ som du vill tillämpa på alla valda målgrupper och välj sedan **[!UICONTROL Save]**.

![Dialogrutan för synlighet av metadata med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

### Redigera anslutningsåtkomst gruppvis {#bulk-edit-connection-access}

Välj **[!UICONTROL Edit connection access]** på redigeringsmenyn när du har valt dina målgrupper på målgruppspanelen.

![Arbetsytan Mina målgrupper med alternativet Redigera anslutningsåtkomst markerat.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-connection-access.png)

Dialogrutan **[!UICONTROL Connection access]** visas så att du kan konfigurera åtkomstinställningarna för de valda målgrupperna. Som standard markeras alternativet **[!UICONTROL Private audience]**. Välj de alternativ som du vill tillämpa på alla valda målgrupper och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Anslutningsåtkomst med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

### Redigera publiknamn och beskrivningar gruppvis {#bulk-edit-audience-names-descriptions}

Välj **[!UICONTROL Edit name and description]** på redigeringsmenyn när du har valt dina målgrupper på målgruppspanelen.

![Arbetsytan Mina målgrupper med alternativet Redigera namn och beskrivning markerat.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description.png)

Dialogrutan **[!UICONTROL Name and description]** visas, där du kan konfigurera namn och beskrivning för varje vald målgrupp. Som standard visas de aktuella namnen och beskrivningarna för varje målgrupp. Gör ändringarna och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Namn och beskrivning med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description-dialog.png)

### Redigera kategorier gruppvis {#bulk-edit-categories}

Välj **[!UICONTROL Edit categories]** på redigeringsmenyn när du har valt dina målgrupper på målgruppspanelen.

![Arbetsytan Mina målgrupper med alternativet Redigera kategorier markerat.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories.png)

Dialogrutan **[!UICONTROL Categories]** visas, där du kan konfigurera kategorierna för varje vald målgrupp. Som standard markeras inga kategorier. Om du vill markera en kategori väljer du först huvudkategorin och sedan de underkategorier som du vill inkludera. Gör ändringarna och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Kategorier med tillgängliga alternativ visas.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories-dialog.png)

## Nästa steg

Efter att målgrupper har inhämtats är det dags att upptäcka medarbetare för att [ansluta](/help/guide/connect/establishing-connections.md) till och samarbeta i projekt.
