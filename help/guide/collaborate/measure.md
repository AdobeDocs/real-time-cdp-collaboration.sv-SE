---
title: Mät prestanda
description: Mät kampanjernas resultat i olika kanaler. Lär dig hur du använder och tolkar olika rapporter.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: 0cf888e36ffc4730fc8de4d8adccae0e0fc2caa8
workflow-type: tm+mt
source-wordcount: '1868'
ht-degree: 0%

---

# Mät prestanda

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Measure]** är bara tillgänglig om användningsfallet **Measurement** aktiverades [&#x200B; under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

Läs mer om tillgängliga rapporter i Adobe Real-Time CDP Collaboration och förstå hur ni mäter och analyserar hur era marknadsföringskampanjer fungerar i olika kanaler.

## Förutsättningar {#prerequisites}

Innan du kan komma åt mätrapporterna i Collaboration måste du:

* [Anslut](/help/guide/connect/establishing-connections.md) till en medarbetare med användningsfallet **Mått** aktiverat
* Samarbeta i minst ett projekt med din medarbetare. Lär dig hur du [skapar ett projekt](/help/guide/collaborate/manage-projects.md#create-project).
* Kör kampanjen och kontrollera att ett [kampanj-ID har angetts för kampanjen](../collaborate/manage-projects.md#manage-campaign-id):
   * Om du är utgivare anger du det kampanj-ID som är länkat till din annonsörs kampanj.
   * Om du är annonsörer ska du begära att din samarbetspartner (utgivare) anger kampanjens ID. Detta krävs för att [generera rapporter på arbetsytan Mätning](#create-measurement-report).
* [Överför mätdata](/help/guide/setup/onboard-measurement-data.md) till Collaboration om du vill [skapa attributrapporter](#create-attribution-report).

## Visa rapporter {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="Kampanj-ID"
>abstract="Platshållare för att lägga till relevant information i användargränssnittet om vad kampanj-ID:n är."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report"
>title="Kampanj-ID"
>abstract="Platshållare för att lägga till relevant information i användargränssnittet om vad kampanj-ID:n är."

Så här visar du de rapporter som finns på fliken Mått:

1. Navigera till **[!UICONTROL Collaborate]** > **[!UICONTROL My projects]**.
2. Välj **[!UICONTROL View]** för det önskade projektet.
3. Välj fliken **[!UICONTROL Measure]** i projektet.

Välj **[!UICONTROL View full report]** om du vill komma åt de olika tillgängliga rapporterna, som beskrivs närmare nedan.

![Så här kommer du till mätfliken i ett projekt.](/help/assets/collaborate/measure/measurement.gif)

### Sammanfattningsvy

I den övre delen av sidan på mätfliken visas en kampanjsammanfattning med några högnivånummer som du kan referera till:

**[!UICONTROL Impressions]**: Det totala antalet gånger som den kreativa har visats.
**[!UICONTROL Unique reach]**: Antalet enskilda identiteter som har sett den kreativa.
**[!UICONTROL Total average frequency]**: Antalet visningar delat med unika identiteter har uppnåtts. Den här bilden visar hur ofta varje identitet visades för den kreativa.

![Kampanjsammanfattningsvy](/help/assets/collaborate/measure/campaign-summary.png)

### Mätvärden över tid {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="Mätvärden över tid"
>abstract="Använd mätvärden över tiden för att förstå det totala antalet visningar som visas för dina kreatörer under kampanjperioden. Du kan välja högst två dimensioner som ska visas i rapporten."

Använd mätvärden över tiden för att förstå det totala antalet visningar som visas för dina kreatörer under kampanjperioden. Observera att du kan välja högst två mätvärden som ska visas och analyseras i rapporten.

![Mätvärden över tid.](/help/assets/collaborate/measure/metrics-over-time.png)

### Frekvensfördelning {#frequency-distribution}

Använd frekvensfördelningsvyn för att förstå hur många visningar som har visats för varje unik användare. Den här vyn kan hjälpa er att i framtida kampanjer avgöra vid vilken tidpunkt ni vill börja undertrycka målgrupper. Du kanske vill inaktivera profiler som redan har sett en kreatör tre gånger.

![Vyn Frekvensfördelning.](/help/assets/collaborate/measure/frequency-distribution.gif)

### Mått efter dimension {#metric-by-dimension}

Analysera olika mätvärden, som visningar, visningsbara exponeringar, unik räckvidd, kostnad med mera i det sammanhang där placeringsmediet används. Analysera vilket medium (till exempel mobil direktuppspelning, CTV-programmering eller andra) som ger bäst resultat för era kampanjer.

![Mått per dimension.](/help/assets/collaborate/measure/metric-by-dimension.png)

### Kumulativ nålskurva {#cumulative-reach-curve}

I takt med att kampanjen fortskrider och antalet visningar ökade, förstår du om antalet användare du kunde nå också har ökat. Ett vanligt mönster i kampanjer är att man efter en viss tidpunkt når en platå där den kreativa effekten visas för samma personer om och om igen. Den här vyn kan hjälpa dig att justera längden på framtida kampanjer, beroende på när nya personer inte längre nås.

![Kumulativ räckvidd-kurva.](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### Impression efter placering {#impressions-by-placement}

Förstå vilket medium som ger kreativiteten ett intryck. Detta kan hjälpa er att bestämma var ni ska investera annonskostnaderna i framtida kampanjer.

![Impressions efter placering.](/help/assets/collaborate/measure/impressions-by-placement.png)

### Kumulativa konverteringar {#cumulative-conversions}

I den här vyn visas en detaljerad beskrivning av de konverteringshändelser du väljer att mäta i ett tabellformat. Tabellen innehåller följande:

* **Konverteringshändelse**: Namn på varje konverteringshändelse som du spårar.
* **Antal konverteringar**: Totalt antal konverteringar som har gjorts för varje händelse.
* **Uppskattad intäkt**: Uppskattat värde som tilldelats varje konverteringshändelse.

Granska den här tabellen för att utvärdera hur effektiv kampanjen är när det gäller de önskade åtgärderna.

![Kumulativa konverteringar.](/help/assets/collaborate/measure/cumulative-conversions.png)

### Konverteringar per dag {#conversions-by-day}

I det här diagrammet ges en daglig uppdelning av konverteringar för varje händelse som har ställts in när du skapar en attributrapport. Använd den här vyn för att identifiera dagliga mönster, identifiera perioder med hög eller låg konverteringsaktivitet och jämföra hur olika konverteringshändelser fungerar över kampanjens tidslinje.

![Konverteringar per dag.](/help/assets/collaborate/measure/conversions-by-day.gif)

## Skapa mätningsrapport {#create-measurement-report}

I Collaboration kan du skapa två huvudtyper av mätrapporter:

* **Kampanjsammanfattning**: Visar högnivåstatistik som räckvidd, visningar, genomsnittlig frekvens och leverans per kanal, vilket ger en snabb översikt över det övergripande kampanjresultatet.
* **Attribution**: Mäter hur kampanjexponeringar driver efterföljande åtgärder som konverteringar eller köp, vilket hjälper dig att förstå kampanjens effektivitet.

Du kan köra Campaign-sammanfattningsrapporten fristående, medan attribueringsrapporten kräver att båda rapporttyperna väljs tillsammans.

### Skapa kampanjsammanfattningsrapport {#create-campaign-summary-report}

Både utgivare och annonsörer kan generera **kampanjsammanfattningsrapporter** för att utvärdera kampanjens resultat. Använd de här rapporterna för att få insikter i viktiga mätvärden som [räckvidd](#cumulative-reach-curve), [frekvens](#frequency-distribution) och [visningar](#impressions-by-placement) och förstå hur kampanjen levererades och hur den fick en generell effekt.

Om du vill generera en **kampanjsammanfattningsrapport** går du till projektarbetsytan från arbetsytan **[!UICONTROL Collaborator]**. På fliken **[!UICONTROL Measure]** väljer du ikonen Lägg till (![ikonen Lägg till.](/help/assets/icons/plus.png)) och välj sedan **[!UICONTROL Measure]**.

Om det här är din första rapport kan du även välja alternativet **[!UICONTROL Run report]**.

![Fliken Mått markerar rapportalternativet Kör och måttalternativet.](/help/assets/collaborate/measure/run-measure-report.png)

Skärmen **[!UICONTROL Create measurement report]** visas med informations- och inmatningsfält grupperade under avsnitten **[!UICONTROL Billing details]**, **[!UICONTROL Campaign details]** och **[!UICONTROL Report details]**.

#### Faktureringsinformation {#billing-details}

I det här avsnittet beskrivs hur krediter används när mätningsrapporter genereras. Kreditansvar har etablerats under [anslutningsinställningen](../connect/establishing-connections.md#credit-split). Innan du kör några rapporter måste du kontrollera och bekräfta inställningarna för kreditdelning och rapportroller med medarbetaren.

#### Kampanjinformation {#campaign-details}

I avsnittet **[!UICONTROL Campaign details]** väljer du lämpligt **Advertiser-ID** som ska kopplas till rapporten. Dessa annonsörnamn eller ID:n lades till under [anslutningskonfigurationen](../connect/establishing-connections.md#advertiser-names). Om bara ett namn har konfigurerats visas det som standard. Om inget namn har ställts in är fältet **[!UICONTROL Advertiser ID (Name)]** inaktiverat och förifyllt med annonsörens kontonamn.

![Skärmen Skapa mätningsrapport visar att alternativet Advertiser ID (Namn) är inaktiverat.](/help/assets/collaborate/measure/advertiser-id.png)

Välj sedan önskad kampanj i listrutan **[!UICONTROL Campaign ID]**. I den här menyn visas alla kampanj-ID som angetts av utgivaren för ditt projekt. Om kampanjen du behöver inte är tillgänglig [lägger du till den i gränssnittet](./manage-projects.md#manage-campaign-id) innan du genererar rapporten.

![Skärmen Skapa mätningsrapport visar den utökade listrutan för kampanj-ID.](/help/assets/collaborate/measure/campaign-id.png)

Ange sedan den period som du vill att rapporten ska omfatta. Välj **[!UICONTROL Report date range]** och använd sedan kalendern för att välja start- och slutdatum.

![Skärmen Skapa mätningsrapport visar kalendern för rapportdatumintervall.](/help/assets/collaborate/measure/report-date-range.png)

#### Rapportdetaljer {#report-details}

**Rapportera körningsdatum**

I avsnittet **[!UICONTROL Report details]** väljer du det datum då rapporten ska köras. Välj **[!UICONTROL Report run date]** och välj önskat datum i kalendern.

* Om du väljer dagens datum eller ett tidigare datum körs rapporten **Kampanjsammanfattning** direkt.
* Om du väljer ett framtida datum kommer rapporten **Kampanjsammanfattning** att köras den dagen.

![Skärmen Skapa mätningsrapport visar kalendern för rapportkörningsdatum.](/help/assets/collaborate/measure/report-run-date.png)

**Typ av rapportering**

* Om du är annonsörer kan du välja rapporttypen **[!UICONTROL Campaign summary]** bland de tillgängliga alternativen. Endast annonsörer kan generera attribueringsrapporter.
* Om du är utgivare är rapporttypen **[!UICONTROL Campaign summary]** förvald och kan inte ändras. Utgivare kan för närvarande inte köra attribueringsrapporter.

![Skärmen Skapa mätningsrapport visar alternativet Kampanjsammanfattning som en förvald och oföränderlig rapporttyp.](/help/assets/collaborate/measure/cs-report-type.png)

Granska slutligen dina inställningar och välj **[!UICONTROL Create]**. Din kampanjsammanfattningsrapport genereras omedelbart om körningsdatumet är i dag eller tidigare, eller på det valda framtida datumet. Du kan redigera den schemalagda rapporten före dess körningsdatum. Stegvisa instruktioner finns i avsnittet [Redigera mätningsrapport].

När rapporten är tillgänglig kan du när som helst visa den på fliken **[!UICONTROL Measure]** på din projektarbetsyta.

![Skärmen Skapa mätningsrapport visar informationen och alternativet Skapa markerat.](/help/assets/collaborate/measure/cs-review.png)

### Skapa attribueringsrapport {#create-attribution-report}

Som annonsörer kan du generera **Attribution**-rapporter för att utvärdera hur dina kampanjexponeringar bidrar till viktiga resultat, till exempel registreringar eller köp. Använd dessa rapporter för att förstå användarinteraktioner med er kampanj, identifiera vilka kontaktytor som ger störst effekt och informera om mer effektiva marknadsföringsstrategier.

>[!IMPORTANT]
>
> Du måste [hämta dina mätdata](../setup/onboard-measurement-data.md#add-measurement-data) till Collaboration innan du kan generera attribueringsrapporter.
>![Fliken Mått med kraven för Mätdata och det inaktiverade måttalternativet.](/help/assets/collaborate/measure/require-measurement-data.png)

Om du vill generera en **attribueringsrapport** går du till projektarbetsytan från arbetsytan **[!UICONTROL Collaborator]**. På fliken **[!UICONTROL Measure]** väljer du ikonen Lägg till (![ikonen Lägg till.](/help/assets/icons/plus.png)) och välj sedan **[!UICONTROL Measure]**.

Om det här är din första rapport kan du även välja alternativet **[!UICONTROL Run report]**.

![Fliken Mått markerar rapportalternativet Kör och måttalternativet.](/help/assets/collaborate/measure/run-measure-report-attribution.png)

Skärmen **[!UICONTROL Create measurement report]** visas med informations- och inmatningsfält grupperade under avsnitten **[!UICONTROL Billing details]**, **[!UICONTROL Campaign details]** och **[!UICONTROL Report details]**.

Läs och följ stegen i avsnittet [Skapa kampanjsammanfattningsrapport](#create-campaign-summary-report) för att konfigurera följande inställningar:

* [Faktureringsinformation](#billing-details)
* [Kampanjinformation](#campaign-details)

#### Rapportdetaljer för attributrapporter {#report-details-attribution}

**Rapportera körningsdatum**

>[!IMPORTANT]
>
> För attribueringsrapporter måste rapportens kördatum vara ett framtida datum och måste inträffa minst en dag efter rapportens slutdatum plus hela varaktigheten för det definierade uppslagsfönstret.
> **Rapportera körningsdatum ≥ rapportens slutdatum + uppslagsfönster + 1**
> 
> Om rapportens datumintervall till exempel upphör den 15 juni och uppslagsfönstret är 14 dagar är rapportens körningsdatum den 30 juni eller senare.

I avsnittet **[!UICONTROL Report details]** väljer du det datum då rapporten ska köras. Välj **[!UICONTROL Report run date]** och välj önskat datum i kalendern.

**Typ av rapportering**

Som annonsörer kan du välja **[!UICONTROL Attribution]** som rapporttyp förutom **[!UICONTROL Campaign summary]**. När ni väljer attribueringsrapporten innehåller resultaten både standardvärden för kampanjsammanfattning och detaljerad attribueringsanalys, vilket ger en heltäckande bild av kampanjresultatet.

![Skärmen Skapa mätningsrapport visar både kampanjsammanfattningen och de rapporttyper för Attribution som har valts.](/help/assets/collaborate/measure/attribution-report-type.png)

När du väljer **[!UICONTROL Attribution]** som rapporttyp visas ett **[!UICONTROL Attribution]**-konfigurationsavsnitt med ytterligare nödvändiga inställningar:

* **Fönstret Uppslag i dagar**: Definierar hur långt bakåt rapporten ska ta hänsyn till kampanjvisningar före varje konvertering. Endast exponeringar inom denna period är berättigade till attribueringskredit.
* **Konverteringshändelser**: Anger vilka konverteringsåtgärder du vill mäta, till exempel inköp eller registreringar. Dessa händelser måste konfigureras i förväg när du [hämtar mätdata](../setup/onboard-measurement-data.md#add-conversion-event) till Collaboration.

Ange först ett värde för fältet **[!UICONTROL Lookback window in days]** eller justera det med alternativen för ökning/minskning.

![Skärmen Skapa mätningsrapport visar värdet för fönstret Lookback i dagar.](/help/assets/collaborate/measure/lookback-window-in-days.png)

Välj sedan upp till **3** konverteringshändelser i listan. Om du vill ha mer information om en viss händelse väljer du ikonen **[!UICONTROL i]** för att visa information om den.

![Skärmen Skapa mätningsrapport visar de valda konverteringshändelserna och informationen om inköpshändelsen.](/help/assets/collaborate/measure/attribution-conversion-events.png)

Granska slutligen dina inställningar och välj **[!UICONTROL Create]** för att schemalägga rapporten. Din attribueringsrapport genereras på det angivna körningsdatumet. Du kan redigera den schemalagda rapporten före dess körningsdatum. Stegvisa instruktioner finns i avsnittet [Redigera mätningsrapport].

När rapporten är tillgänglig kan du när som helst visa den på fliken **[!UICONTROL Measure]** på din projektarbetsyta.

![Skärmen Skapa mätningsrapport visar informationen och alternativet Skapa markerat.](/help/assets/collaborate/measure/attribution-review.png)
