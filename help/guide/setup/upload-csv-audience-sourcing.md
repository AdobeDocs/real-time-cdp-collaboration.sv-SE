---
title: Överför CSV-fil för målgruppskälla
description: Lär dig hur du överför din CSV-fil som en självbetjäningsdatakälla för att importera målgruppsdata till Real-Time CDP Collaboration.
source-git-commit: 96d3f87cedcfde73ce01c2b53c0b2ce4365fd277
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---

# Överför CSV-fil för målgruppskälla

Den här guiden innehåller steg för hur du överför en CSV-fil i Adobe Real-Time CDP Collaboration-gränssnittet för att hämta målgruppsdata för samarbetsprojekt.

## Översikt {#overview}

CSV-filöverföring är en metod för att hämta förstahandsdata för samarbetsprojekt. Detta är ett alternativ till [att ansluta din AWS S3-bucket](./configure-aws-s3-audience-sourcing.md) eller [hämta målgrupper från Experience Platform](./onboard-audiences.md).

Följ det här arbetsflödet när du vill överföra en CSV-fil som innehåller målgruppsdata till en källa och hantera förstahandsmålgrupper inom Collaboration. Du kan mappa identitetsfält för aktivering och överlappningsanalys. När din fil har överförts och bearbetats blir målgruppen tillgänglig på arbetsytan i **[!UICONTROL My audiences]**, där du kan granska, aktivera och hantera dina samarbetsprojekt.

>[!IMPORTANT]
>
>* Publiker som har hämtats via CSV-överföring är tillgängliga i **7 dagar**. Efter den här perioden upphör målgruppen att gälla och måste laddas upp igen för att kunna användas i dina samarbetsprojekt.
>
>* Du kan överföra en CSV-fil per session just nu. Om du vill lägga till fler målgrupper slutför du överföringsarbetsflödet igen för varje fil som du vill hämta.

## Förhandskrav {#prerequisites}

Innan du kan överföra CSV-filer för målgruppskälla måste du se till att du har:

* Kontointroduktionen har slutförts i Real-Time CDP Collaboration. Gå till [Anlita ditt konto](./onboard-account.md) om du vill ha stegvisa instruktioner.
* Behörigheter som krävs för att lägga till målgrupper i organisationen.
* En CSV-fil som innehåller målgruppsdata med identitetsfält som e-post eller telefon.

## Överföra en CSV-fil {#upload-csv-file}

Välj ikonen Lägg till (**[!UICONTROL My audiences]** ikonen Lägg till) på fliken **[!UICONTROL Setup]** på arbetsytan ![.](/help/assets/icons/plus.png)) och välj sedan **[!UICONTROL Audience]**.

Om det här är din första målgrupp kan du även välja alternativet **[!UICONTROL Add]**.

![Fliken Mina målgrupper på arbetsytan Konfigurera med ikonen Lägg till och alternativet Lägg till målgrupp visas.](../../assets/setup/add-manage-audiences/add-audiences.png)

Arbetsflödet Lägg till målgrupp visas. Välj **[!UICONTROL Add a new data connection]** och sedan **[!UICONTROL Next]**.

![Arbetsytan Lägg till målgrupper med alternativet Lägg till en ny dataanslutning markerat.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Välj CSV-fil som dataanslutning {#select-csv-file}

Välj **[!UICONTROL CSV File]** som dataanslutning, följt av **[!UICONTROL Next]**.

![Väljningsskärmen för dataanslutning med CSV-fil är tillgänglig som ett valbart alternativ.](../../assets/setup/csv-audience-sourcing/select-csv-data-connection.png)

### Välj fil {#select-file}

Välj **[!UICONTROL Select from computer]** om du vill överföra en CSV-fil från det lokala systemet. Du kan också dra och släppa den CSV-fil som du vill överföra till panelen [!UICONTROL Drag and drop a CSV file].

>[!IMPORTANT]
>
>Endast CSV-filer stöds. Den maximala filstorleken är **2 GB**.

![Välj en CSV-fil som innehåller målgruppsdata från ditt lokala system.](../../assets/setup/csv-audience-sourcing/select-file.png)

När användargränssnittet har överförts visas en sammanfattning med antalet kolumner, ett uppskattat radantal, filens struktur och en förhandsgranskning av de första 10 raderna med data.

Granska sammanfattningen och välj sedan **[!UICONTROL Next]**.

![Förhandsgranska exempelmålgruppsdata från din CSV-fil.](../../assets/setup/csv-audience-sourcing/preview-sample-data.png)

#### Ersätt fil {#replace-file}

Om du behöver överföra en annan CSV-fil väljer du **[!UICONTROL Replace file]** och väljer den nya filen. Gränssnittet uppdateras sedan för att visa en uppdaterad sammanfattning av nya data.

När du har granskat den reviderade sammanfattningen väljer du **[!UICONTROL Next]**.

![Välj alternativet Ersätt fil om du vill överföra en annan CSV-fil.](../../assets/setup/csv-audience-sourcing/replace-file.png)

### Bekräfta bekräftelse av godkännande {#confirm-consent}

Innan du fortsätter måste du bekräfta att avanmälan om samtycke har tagits bort från målgruppsdata. Collaboration kräver rena målgruppsdata utan användare som har valt att sluta dela data.

Markera bekräftelserutan följt av **[!UICONTROL OK]** för att bekräfta. Dialogrutan stängs och du fortsätter till skärmen för kartfält.

![Bekräftelsedialogrutan för avanmälan som kräver bekräftelse innan du fortsätter.](../../assets/setup/csv-audience-sourcing/consent-optout-acknowledgment.png)

### Mappa käll-ID-fält {#map-fields}

Fältmappning avgör hur Collaboration använder era målgruppsdata för aktivering och överlappningsanalys. Använd listrutemenyerna på skärmen **[!UICONTROL Map fields]** för att mappa varje källidentitetsfält från CSV-filen till rätt målfält i Collaboration.

Om du behöver mer information om ett målfält, inklusive datatypen eller beskrivningen, väljer du **[!UICONTROL Target fields details]** om du vill ha mer information.

![Listrutan för att mappa ett källidentitetsfält från CSV-målgruppsdata till målfältet i Collaboration.](../../assets/setup/csv-audience-sourcing/map-fields.png)

Granska sedan de mappade fälten och välj **[!UICONTROL Next]**.

![Skärmen för fältmappning visar mappade käll- och målidentitetsfält.](../../assets/setup/csv-audience-sourcing/confirm-mapped-fields.png)

### Granska och slutför överföringen {#review-and-complete}

Skärmen **[!UICONTROL Review]** visas med en sammanfattning av målgruppsinställningarna från din CSV-fil. Granska informationen i följande avsnitt:

* **[!UICONTROL File Information]**: Visar filnamnet, antalet kolumner och det beräknade antalet rader.
* **[!UICONTROL Mapping]**: Visar hur källfälten från den överförda målfilen (till exempel `email`) mappas till målfält som används i Collaboration (till exempel Hash-kodad e-post).

Välj pennikonen om du behöver redigera ett avsnitt. Välj **[!UICONTROL Complete]** om du vill bekräfta alla avsnitt.

![Granska sammanfattningen av överföringsinställningar, inklusive CSV-filinformation och fältmappningsinformation.](../../assets/setup/csv-audience-sourcing/review-upload-summary.png)

En förloppsindikator visas under sammanfattningsavsnitten för att visa överföringsförloppet. När överföringen är klar visas en bekräftelsedialogruta som bekräftar att din CSV-publik har skapats och att målgruppsinhämtning pågår.

![När filen har överförts visas en bekräftelsedialogruta som anger att CSV-målgruppen har skapats och att målgruppskällan pågår.](../../assets/setup/csv-audience-sourcing/upload-success-sourcing-in-progress.png)

## Granska målgrupper från olika källor {#review-sourced-audiences}

När du har överfört din CSV-fil börjar Collaboration hämta målgrupper från filen. Den här processen kan ta flera minuter. När källan är klar är dina målgrupper tillgängliga på fliken **[!UICONTROL My Audiences]** med samma funktioner och information som målgrupper som kommer från Experience Platform.

![Fliken Publiker som visar en lista över källgrupper i stödrastervyn.](../../assets/setup/csv-audience-sourcing/csv-audiences-list.png)

I stödrastervyn eller tabellvyn väljer du ett radobjekt eller **[!UICONTROL View audience]** om du vill se en översikt över en viss målgrupp. Där visas målgruppens status, källa och dataanslutningsnamn tillsammans med detaljerade paneler för:

**[!UICONTROL Identities]**: Visar det totala antalet identiteter och uppdelningen när data blir tillgängliga.
**[!UICONTROL Categories]**: Visar alla taggar som används för att ordna eller filtrera målgruppen.
**[!UICONTROL Connection access]**: Visar om målgruppen är privat, offentlig eller delad med specifika medarbetare.
**[!UICONTROL Metadata visibility]**: Visar vilken målgruppsinformation (till exempel identitetsantal, överlappningsprocent och index) som visas för medarbetare.

Använd den här vyn för att bekräfta inställningar för målgruppskonfiguration och synlighet innan du använder målgruppen i samarbetsprojekt. Mer information finns i [Så här visar du en enskild publik](./onboard-audiences.md#view-individual-audiences).

## Nästa steg {#next-steps}

Du har nu överfört din CSV-fil till Collaboration. När ni är klara kan ni

* Skapa samarbetsprojekt med era målgrupper. Se [Identifiera målgrupper](../../guide/collaborate/discover.md).
* Aktivera målgrupper för anslutna destinationer. Se [Aktivera målgrupper](../../guide/collaborate/activate.md).
* Granska överlappande målgrupper och insikter. Se [Mät kampanjens prestanda](../../guide/collaborate/measure.md).
* Hantera målgruppsinställningar och synlighet. Se [Source och hantera målgrupper](./onboard-audiences.md).

Mer information om andra metoder för målgruppskälla finns i [Konfigurera AWS S3 för målgruppskälla](./configure-aws-s3-audience-sourcing.md) eller [Source-målgrupper från Experience Platform](./onboard-audiences.md).
