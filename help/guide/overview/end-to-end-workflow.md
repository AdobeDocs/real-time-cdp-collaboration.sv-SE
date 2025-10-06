---
title: Arbetsflöde från början till slut
description: Förstå arbetsflödet från ax till limpa med Real-Time CDP Collaboration baserat på ditt samarbetsmönster.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
source-git-commit: 5c08738cdc8e1e208203ee1f9a1cf1891b5b07cb
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Arbetsflöde från början till slut

{{limited-availability-release-note}}

I Adobe Real-Time CDP Collaboration varierar arbetsflödet från början till slut beroende på vilket samarbetsmönster du väljer. Arbetsflödet beskriver stegen som krävs för att skapa och köra ett samarbetsprojekt, från att skapa konton och källgrupper till att skapa anslutningar och skapa projekt. Att förstå det här arbetsflödet är nödvändigt för att utnyttja plattformens möjligheter att nå era marknadsföringsmål på ett effektivt sätt.

## Komma igång

Innan du börjar ser du till att du har en god förståelse för dessa viktiga begrepp:

- **Collaboration-mönster**: De här mönstren definierar hur medarbetare arbetar tillsammans. Det finns två skilda mönster: [annonser-till-utgivare](./collaboration-patterns.md#advertiser-to-publisher) och [varumärke-till-varumärke](./collaboration-patterns.md#brand-to-brand).
- **Kontoroller**: Kontoroller avgör vilka funktioner du kan använda på plattformen. De bör överensstämma med organisationens mål, varumärke och mål. Det finns två kontoroller: [annonser](./roles.md#advertiser) och [utgivare](./roles.md#publisher).
- **Användningsfall**: Använd fall för att definiera hur du kan utnyttja Collaboration för att uppnå dina marknadsföringsmål. Det finns tre användningsfall för samarbete: [Upptäck](./use-cases.md#discover), [Aktivera](./use-cases.md#activate) och [Mät](./use-cases.md#measure).

I den här guiden används tre dummyassistenter för att illustrera hela arbetsflödet:

- **[!UICONTROL Luma]**: Ett sportklädmärke. De är en annonsör som vill nå specifika målgrupper genom riktade marknadsföringskampanjer.
- **[!UICONTROL TV Tube]**: En digital direktuppspelningsleverantör. De är ett förlag som tillhandahåller målgruppsdata som annonsörerna kan använda.
- **[!UICONTROL Fit Apparel]**: Ett annat sportkläder. De är en andra annonsör som vill samarbeta för att dela målgruppsdata och insikter för att få bättre marknadsföringssatsningar.

## Arbetsflöde mellan annonsörer och utgivare {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], ett atletiskt detaljhandelsföretag, vill skapa en anslutning till [!UICONTROL TV Tube], en digital strömningsleverantör, för att nå specifika målgrupper genom riktade marknadsföringskampanjer.

Till att börja med måste [!UICONTROL Luma] [skapa ett konto](../setup/onboard-account.md) med annonsörrollen, medan [!UICONTROL TV Tube] skapar ett konto med utgivarrollen.

När de har upprättat sina konton måste både [!UICONTROL Luma] och [!UICONTROL TV Tube] [skapa en dataanslutning och en källpublik](../setup/onboard-audiences.md). Endast [!UICONTROL TV Tube] aktiverar målgrupper för marknadsföringskampanjer, så de måste [konfigurera ett mål](../setup/manage-destinations.md).

När båda medarbetarna har sina konton konfigurerade är de redo att [skapa en anslutning](../connect/establishing-connections.md) inom plattformen. [!UICONTROL Luma] använder funktionen [Identifiera medarbetare](../connect/discover-collaborators.md) för att hitta [!UICONTROL TV Tube] och initiera en anslutningsbegäran. När [!UICONTROL TV Tube] har godkänt anslutningsbegäran konfigurerar [!UICONTROL Luma] anslutningsinställningarna för att definiera hur samarbetet ska fungera. [!UICONTROL TV Tube] accepterar anslutningsbegäran för att upprätta en säker länk mellan de två varumärkena.

När anslutningen har upprättats skapar [!UICONTROL Luma] [ett projekt](../collaborate/manage-projects.md) för att starta samarbetet med [!UICONTROL TV Tube]. Under projektkonfigurationen väljer de användningsfall för samarbete som passar deras mål bäst: [Upptäck](../collaborate/discover.md), [Aktivera](../collaborate/activate.md) och [Åtgärd](../collaborate/measure.md).

[!UICONTROL Luma] utnyttjar [Discover](../collaborate/discover.md)-användningsfallet för att få insikter om målgruppsdata för [!UICONTROL TV Tube]. När [!UICONTROL Luma] har identifierat målgruppssegmenten [Aktiverar](../collaborate/activate.md) de här målgrupperna.

När målgrupperna har aktiverats kör [!UICONTROL TV Tube] riktade marknadsföringskampanjer och överför data till [Mät](../collaborate/measure.md) resultaten för att utvärdera kampanjens effektivitet.

## Märkesbaserat arbetsflöde {#brand-to-brand-workflow}

[!UICONTROL Fit Apparel], ett atletiskt klädmärke, vill samarbeta med [!UICONTROL Luma], ett annat atletiskt klädmärke, för att dela målgruppsdata och insikter för bättre marknadsföringssatsningar.

När de har skapat sina konton måste både [!UICONTROL Fit Apparel] och [!UICONTROL Luma] [skapa en dataanslutning och en källpublik](../setup/onboard-audiences.md). Både [!UICONTROL Fit Apparel] och [!UICONTROL Luma] aktiverar målgrupper för marknadsföringskampanjer, så båda måste [konfigurera ett mål](../setup/manage-destinations.md).

När målgrupperna har inhämtats bildar [!UICONTROL Fit Apparel] och [!UICONTROL Luma] [ en anslutning](../connect/establishing-connections.md) inom plattformen för att på ett säkert sätt dela målgruppsdata. För att kunna göra det måste de använda funktionen [privat inbjudan](../connect/establishing-connections.md#private-connection-invite) för anslutning. [!UICONTROL Luma] delar sin anslutningskod med [!UICONTROL Fit Apparel], som sedan använder den för att initiera en anslutningsbegäran. När [!UICONTROL Luma] har godkänt anslutningsbegäran konfigurerar [!UICONTROL Fit Apparel] anslutningsinställningarna för att definiera hur de ska samarbeta. I konfigurationen anger [!UICONTROL Fit Apparel] att båda medarbetarna kan aktivera målgrupper för marknadsföringskampanjer. [!UICONTROL Luma] accepterar begäran om att upprätta en säker länk mellan de två varumärkena för att slutföra anslutningen.

När anslutningen har upprättats skapar [!UICONTROL Fit Apparel] [ett projekt](../collaborate/manage-projects.md) för att starta samarbetet med [!UICONTROL Luma]. Under projektkonfigurationen väljer de användningsfall för samarbete som passar deras mål bäst: [Upptäck](../collaborate/discover.md), [Aktivera](../collaborate/activate.md) och [Åtgärd](../collaborate/measure.md).

[!UICONTROL Fit Apparel] och [!UICONTROL Luma] kan båda använda [Discover](../collaborate/discover.md) för att få insikt i varandras målgruppsdata. När de har identifierat värdefulla målgruppssegment [aktiverar](../collaborate/activate.md) de valda målgrupperna för marknadsföringskampanjer.

När kampanjerna har slutförts överför båda varumärkena data till [Mät](../collaborate/measure.md) resultaten och utvärderar hur effektivt deras samarbete är.

## Plattformsarbetsflöde för annonsering mellan annonsörer {#advertiser-to-advertising-platform-workflow}

[!UICONTROL Luma], ett atletiskt detaljhandelsföretag, vill ansluta till [!DNL Amazon Marketing Cloud] ([!DNL AMC]) för att förbättra sina marknadsföringsfunktioner genom att utnyttja [!DNL AMC] verktyg för identitetsupplösning och målinriktning. Luma har redan ett aktivt [!DNL Amazon Advertising]-konto och har godkänts för användning av [!DNL AMC].

Till att börja med måste [!UICONTROL Luma] [skapa ett konto](../setup/onboard-account.md) med annonsörrollen. När kontot har skapats måste [!UICONTROL Luma] [skapa en dataanslutning och en källpublik](../setup/onboard-audiences.md). Eftersom [!UICONTROL Luma] aktiverar målgrupper för marknadsföringskampanjer måste de [konfigurera ett mål](../setup/manage-destinations.md).

När [!UICONTROL Luma] har skapat sitt konto är de redo att [skapa en anslutning](../connect/establishing-connections.md) med [!DNL AMC] inom plattformen. [!UICONTROL Luma] använder funktionen [Identifiera medarbetare](../connect/discover-collaborators.md) för att hitta [!UICONTROL Amazon Marketing Cloud] och [initiera en anslutningsbegäran](../connect/advertising-platforms/amc.md). När anslutningen har autentiserats och auktoriserats via inloggningssidan [!DNL Amazon] upprättas anslutningen med [!DNL AMC].

När anslutningen har upprättats skapar [!UICONTROL Luma] [ett projekt](../collaborate/manage-projects.md) för att starta samarbetet med [!DNL AMC]. Anslutningsinställningarna, inklusive användningsfall, är förkonfigurerade beroende på annonseringsplattformen. För [!DNL AMC] är det tillgängliga användningsexemplet [Discover](../collaborate/advertising-platforms/amc.md#discover).

[!UICONTROL Luma] utnyttjar [Identifiera](../collaborate/advertising-platforms/amc.md#discover)-användningsfallet för att få insikter och målgruppsdata från [!DNL AMC]. Med hjälp av dessa insikter kan [!UICONTROL Luma] optimera sina marknadsföringsstrategier och förbättra kampanjeffektiviteten.
