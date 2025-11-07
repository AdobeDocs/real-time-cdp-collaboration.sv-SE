---
title: Konfigurera [!DNL Amazon S3] för målgruppskälla
description: Lär dig hur du konfigurerar och ansluter ditt [!DNL Amazon S3] lagringsutrymme som en självbetjäningsdatakälla för att importera målgruppsdata till Real-Time CDP Collaboration.
source-git-commit: 05fd7ec466ba2b20264490bbbfadc9bb6d361bc8
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 0%

---

# Konfigurera [!DNL Amazon S3] för målgruppskälla

Lär dig hur du konfigurerar och ansluter ditt [!DNL Amazon S3]-lagringsutrymme i Adobe Real-Time CDP Collaboration till målgruppsdata för aktivering och överlappningsanalys.

>[!IMPORTANT]
>
>Innan du följer den här guiden måste du ha slutfört stegen för att godkänna Adobe IAM-rollen på ditt AWS-konto.\
>Se guiden **[Konfigurera AWS-behörigheter för målgruppskälla](./configure-aws-permissions-audience-sourcing.md)** för steg-för-steg-instruktioner.

## Översikt {#overview}

Använd det här arbetsflödet för att hämta och hantera förstahandsmålgrupper direkt från [!DNL Amazon S3]. Efter konfigurationen hämtar Collaboration automatiskt in målgrupper från er S3-bucket och gör dem tillgängliga för insikter och aktivering.

Målgrupper som köps via S3 följer samma regler för styrning och datahantering som de som hämtas från Adobe Experience Platform.

## Förhandskrav {#prerequisites}

Innan du konfigurerar din S3-dataanslutning bör du kontrollera följande:

* Du har åtkomst till en aktiv **[!DNL Amazon S3]-bucket** som innehåller målgruppsfiler som uppfyller **[specifikationen för målgruppskälla (v1.1)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1.pdf)**.
* Du har skapat en **IAM-roll** i AWS som ger Adobe behörighet att komma åt din bucket med metoden **antagen role** (inte åtkomst/hemliga nycklar). Mer information finns i **[Konfigurera AWS-behörigheter för målgruppskälla](./configure-aws-permissions-audience-sourcing.md)**. IAM-rollen måste innehålla följande behörigheter:

   * `ListBucket`
   * `GetBucketLocation`
   * `GetObject`

* Du har följande värden klara:

   * **IAM-roll Amazon Resource Name (ARN)**
   * **S3-bucket, namn**
   * **Mappsökväg** (katalogprefixet som innehåller målgruppsfilerna)

>[!NOTE]
>
>Målgruppsfiler måste finnas i **rotmappssökvägen** för din auktoriserade S3-bucket. Undermappsstrukturer stöds inte.

## Konfigurera din [!DNL Amazon S3]-anslutning {#configure-aws-s3-connection}

Välj ikonen Lägg till (**[!UICONTROL My audiences]** ikonen Lägg till) på fliken **[!UICONTROL Setup]** på arbetsytan ![.](/help/assets/icons/plus.png)) och välj sedan **[!UICONTROL Audience]**.

Om det här är din första målgrupp kan du även välja alternativet **[!UICONTROL Add]**.

![Fliken Mina målgrupper på arbetsytan Konfigurera med ikonen Lägg till och alternativet Lägg till målgrupp visas.](../../assets/setup/add-manage-audiences/add-audiences.png)

Arbetsflödet Lägg till målgrupp visas. Välj **[!UICONTROL Add a new data connection]** och sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med alternativet Lägg till en ny dataanslutning markerat.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Välj [!DNL Amazon S3] som dataanslutning {#select-aws-s3}

Välj **[!UICONTROL Amazon S3]** som dataanslutning, följt av **[!UICONTROL Next]**.

![Väljningsskärmen för dataanslutning med [!DNL Amazon S3] tillgänglig som ett valbart alternativ.](../../assets/setup/aws-audience-sourcing/select-s3-data-connection.png)

### Granska kraven på målgruppsfiler {#review-audience-requirements}

En dialogruta som förklarar hur målgruppsfilerna måste struktureras visas. Använd länken till **[[!UICONTROL Audience Sourcing Specification]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1.pdf)** för att lära dig att formatera och strukturera målgruppsdata från [!DNL Amazon S3] så att Collaboration kan läsa dem korrekt.

>[!IMPORTANT]
>
>Du måste ha auktoriserat Adobe som [!DNL Amazon S3]-användare så att Adobe kan hämta data från ditt [!DNL Amazon S3]-lagringsutrymme för bearbetning.

Publiken måste följa specifikationen för målgruppskällan. Matchningsnycklarna mappas automatiskt baserat på det format som krävs.

Viktiga överväganden:

* Filerna måste vara i CSV-format och använda kommatecken som avgränsare och rör (`|`) för flera värden.
* Om du överför flera filer måste du se till att alla filer innehåller identiska kolumner.
* Varje målgruppspost måste innehålla en `AUDIENCE_ID` och minst en matchningsnyckel, till exempel `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID` eller `ADFIXUS_ID`.
* Datauppdateringar görs var 1-6:e dag baserat på ditt val under källkonfigurationen i Collaboration.

![Dialogrutan Förbered dina data för Källa med en länk till specifikationerna för målgruppskälla.](../../assets/setup/aws-audience-sourcing/prepare-data-sourcing-dialog.png)

### Autentisera din S3-anslutning {#authenticate-s3-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_sources_s3_folderpath"
>title="Sökvägsformat för mapp"
>abstract="Ange mappsökvägen (prefix) i [!DNL Amazon S3]-bucket där målgruppsfilerna lagras.<br><ul><li>Starta inte banor med ett snedstreck (/).</li><li>Inkludera ett avslutande snedstreck i slutet av banan.</li><ul><br>Giltigt exempel: `base/path/`<br>Ogiltigt exempel: `/base/path`"

Ange sedan dina [!DNL Amazon S3]-autentiseringsuppgifter för att ansluta S3-bucket till Collaboration.

Följ stegen som beskrivs i **[Konfigurera AWS-behörigheter för målgruppskälla](./configure-aws-permissions-audience-sourcing.md)** för att ge Adobe åtkomst till dina
[!DNL Amazon S3] lagring. När du är klar anger du dina värden i följande gränssnittsfält:

* IAM-roll
* S3 Buckennamn
* Mappsökväg

![Anslutningsformuläret [!DNL Amazon S3] med fält för IAM-rollen, S3-buffertnamn och mappsökväg.](../../assets/setup/aws-audience-sourcing/s3-authentication-credentials-form.png)

### Bekräfta bekräftelse av godkännande {#confirm-consent}

Du måste bekräfta att avanmälan om samtycke har tagits bort innan du fortsätter. Markera bekräftelserutan följt av **[!UICONTROL OK]** för att bekräfta.

![Bekräftelsedialogrutan för avanmälan som kräver bekräftelse innan du fortsätter.](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### Validera autentiseringsresultat {#validate-authentication}

Efter anslutningen validerar systemet dina autentiseringsuppgifter och visar ett av följande meddelanden:

| Status | Meddelande | Beskrivning |
|---| ---|---|
| **Lyckades** | **[!UICONTROL Authentication successful]** | Anslutningen till [!DNL Amazon S3] har upprättats. |
| **Misslyckades** | **[!UICONTROL Authentication failed]** | Granska dina inloggningsuppgifter och försök igen. |
| **Åtkomst nekad** | **[!UICONTROL Access denied]** | Dina autentiseringsuppgifter har inte den behörighet som krävs för att komma åt den här [!DNL Amazon S3]-bucket. Kontrollera åtkomstinställningarna eller kontakta administratören. |
| **Ogiltigt filformat** | **[!UICONTROL Invalid file format]** | Målgruppsdata matchar inte den förväntade strukturen. Se till att dina filer överensstämmer med specifikationerna för målgruppskälla. |
| **Inga målgruppsfiler hittades** | **[!UICONTROL No audience files found]** | Kontrollera att målgruppsfilerna finns i den angivna mappsökvägen och att sökvägen är tillgänglig. |
| **Internt fel** | **[!UICONTROL An internal error has occurred]** | Försök igen. Kontakta kundsupport om problemet kvarstår. |


### Ange anslutningsinformation {#provide-connection-details}

Ange ett beskrivande namn och en valfri beskrivning för din S3-dataanslutning. Ange värden i följande gränssnittsfält:

* **[!UICONTROL Data connection name]** (obligatoriskt)
* **[!UICONTROL Data connection description]** (valfritt)

![Formuläret för dataanslutningsinformation med fält för anslutningsnamn och beskrivning.](../../assets/setup/aws-audience-sourcing/s3-connection-name-description.png)

### Granska automatiskt mappade identitetsfält {#auto-mapped-fields}

Skärmen **[!UICONTROL Mapping]** är skrivskyddad. Du kan inte lägga till, ta bort eller använda omformningar. Collaboration mappar automatiskt källidentifieringsfält från målgruppsfiler till målfält baserat på specifikationen för målgruppskälla.

Bekräfta de mappade fälten visuellt och välj **[!UICONTROL Next]** för att fortsätta.

![Skärmen för fältmappning visar automatiskt mappade käll- och målidentitetsfält.](../../assets/setup/aws-audience-sourcing/s3-field-mapping-auto-mapped.png)

### Schemalägg uppdateringsfrekvens och datumintervall {#schedule-refresh}

Vyn **[!UICONTROL Schedule]** visas. Använd listrutan för att välja en uppdateringsfrekvens mellan en och sex dagar och ange sedan det aktiva datumintervallet. Använd kalenderikonen för att ange start- och slutdatum.

>[!IMPORTANT]
>
>Om du vill hantera dina Collaboration-krediter effektivt ställer du in uppdateringsfrekvensen så att den matchar eller överskrider uppdateringsfrekvensen för underliggande S3-data. Det minsta uppdateringsintervall som stöds är en gång var sjätte dag.

![Skärmen för schemainställningar med alternativ för uppdateringsfrekvens och datumintervallkonfiguration.](../../assets/setup/aws-audience-sourcing/s3-schedule-refresh-frequency.png)

### Granska och slutför anslutningen {#review-and-complete}

Granska slutligen dina konfigurationsinställningar i sammanfattningsfönstret. Den här vyn innehåller en sammanfattning av följande avsnitt:

* **[!UICONTROL Data connection]**: Visar IAM-rollen, S3-bucket-namnet och mappsökvägen som du konfigurerade.
* **[!UICONTROL Details]**: Visar namnet på och den valfria beskrivningen av din dataanslutning så att den kan identifieras senare.
* **[!UICONTROL Mapping]**: Visar hur källfälten från dina överförda målfiler (till exempel `HASHED_EMAIL`) mappas till målfält som används i Collaboration (till exempel Hash-kodad e-post).
* **[!UICONTROL Schedule]**: Sammanfattar hur ofta anslutningen uppdaterar målgruppsdata och det aktiva datumintervallet för källa.

Välj pennikonen om du behöver redigera ett avsnitt. Välj **[!UICONTROL Complete]** om du vill bekräfta alla avsnitt.

![Granskningssammanfattningsskärmen visar dataanslutning, information, mappning och schemaavsnitt.](../../assets/setup/aws-audience-sourcing/s3-connection-review-summary.png)

En bekräftelse visas som anger att dataanslutningen har skapats och att målgruppen håller på att hämta data.

## Granska målgrupper från olika källor {#review-sourced-audiences}

När konfigurationen är klar börjar Collaboration hämta målgrupper från din S3-bucket. Publiker som har skapats med en [!DNL Amazon S3]-bucket visas på fliken **[!UICONTROL My Audiences]** och har samma funktioner och information som målgrupper som har hämtats från Experience Platform.

Om målgruppsinhämtning pågår visas en banderoll högst upp på skärmen. Enskilda målgrupper visas endast när källan är klar.

![Fliken Publiker visar att källinläsning pågår för [!DNL Amazon S3] målgrupper.](../../assets/setup/aws-audience-sourcing/s3-audiences-sourcing-in-progress.png)

När S3-målgrupperna är insamlade visas din lista över tillgängliga målgrupper i en tabell eller kortvy.

>[!TIP]
>
>Tidsperioden för målgruppskällan varierar beroende på storleken på dina S3-data och den uppdateringsfrekvens du konfigurerade. Det kan ta längre tid att visa större datauppsättningar eller mindre vanliga uppdateringsscheman på arbetsytan i **[!UICONTROL My audiences]**.

![Fliken Publiker som visar en lista över målgrupper som kommer från en tabell.](../../assets/setup/aws-audience-sourcing/s3-audiences-list-view.png)

I stödrastervyn eller tabellvyn väljer du ett radobjekt eller **[!UICONTROL View audience]** om du vill se en översikt över en viss målgrupp. Där visas målgruppens status, källa och dataanslutningsnamn tillsammans med detaljerade paneler för:

**[!UICONTROL Identities]**: Visar det totala antalet identiteter och uppdelningen när data blir tillgängliga.
**[!UICONTROL Categories]**: Visar alla taggar som används för att ordna eller filtrera målgruppen.
**[!UICONTROL Connection access]**: Anger om målgruppen är privat, offentlig eller delad med specifika medarbetare.
**[!UICONTROL Metadata visibility]**: Definierar vilken målgruppsinformation (till exempel identitetsantal, överlappningsprocent och index) som ska visas för medarbetare.

Använd den här vyn för att bekräfta inställningar för målgruppskonfiguration och synlighet innan du använder målgruppen i samarbetsprojekt.

Mer information finns i [Visa dokumentationen för målgruppspanelen](https://experienceleague.adobe.com/sv/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#view-audiences-dashboard).

## Visa din S3-dataanslutning {#view-s3-connection}

Din nyligen tillagda [!DNL Amazon S3]-anslutning är omedelbart tillgänglig på fliken **[!UICONTROL My data connections]**. Publiken visas som [!UICONTROL Amazon S3].

Din S3-dataanslutning innehåller samma funktioner och information som andra målgruppsdataanslutningar, förutom att du inte kan lägga till eller redigera målgrupper direkt från den här vyn.

>[!NOTE]
>
>[!DNL Amazon S3] dataanslutningar kan inte redigeras. Du kan inte ändra inställningar som uppdateringsfrekvensen när anslutningen har skapats. Om du vill uppdatera konfigurationen måste du ta bort den befintliga anslutningen och skapa en ny.

![Fliken Mina dataanslutningar som visar dataanslutningen [!DNL Amazon S3] med källstatusinformation.](../../assets/setup/aws-audience-sourcing/s3-data-connections-tab.png)

## Nästa steg {#next-steps}

Du har nu konfigurerat och anslutit lagringsutrymmet [!DNL Amazon S3] som en datakälla i Collaboration. Genom att slutföra det här arbetsflödet möjliggjorde ni säker inhämtning av egna målgruppsdata för aktivering och överlappningsanalys.

När källan är klar visas dina målgrupper på arbetsytan **[!UICONTROL My audiences]**, redo för samarbete och aktivering. Detaljerade hanteringsalternativ finns i [källan och i dokumentationen för målgrupper](./onboard-audiences.md).
