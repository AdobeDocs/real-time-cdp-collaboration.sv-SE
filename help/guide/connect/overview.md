---
title: Anslutningar - översikt
description: Läs mer om anslutningar i Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 5c08738cdc8e1e208203ee1f9a1cf1891b5b07cb
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Anslutningar - översikt

{{limited-availability-release-note}}

Innan medarbetare kan samarbeta i kampanjer måste de skapa en anslutning. Med den här anslutningen kan de aktivera målgrupper, skapa projekt och köra rapporter om kampanjresultat.

Anslutningar upprättas baserat på ditt valda samarbetsmönster. Collaboration har stöd för tre viktiga samarbetsmönster: annonser-till-utgivare, varumärke-till-reklam och annonser-till-annonsplattform. Mer information om mönstren finns i guiden [för samarbetsmönster](/help/guide/overview/collaboration-patterns.md).

Om du vill lära dig hur du upprättar en anslutning läser du avsnittet nedan som motsvarar ditt samarbetsmönster:

- [Anslutning mellan annonsörer och utgivare](#advertiser-to-publisher-connection)
- [Varumärkesbaserad koppling](#brand-to-brand-connection)
- [Anslutning mellan annonsörer och reklamplattformar](#advertiser-to-advertising-platform-connection)

## Anslutning mellan annonsörer och utgivare {#advertiser-to-publisher-connection}

![Högnivådiagram över anslutningsprocessen mellan annonser och utgivare.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

I mönstret för annonser-till-utgivare upptäcker en annonsörer en utgivare som de vill arbeta med via arbetsytan **[!UICONTROL Discover publishers]** och skickar en anslutningsinbjudan. Utgivaren granskar sedan inbjudan och godkänner den, så att annonsören kan föreslå anslutningsinställningar. När utgivaren har godkänt anslutningsinställningarna upprättas anslutningen, och båda medarbetarna kan börja arbeta tillsammans i projekt.

### Översikt på hög nivå

För att upprätta en anslutning mellan en annonsörer och en utgivare gäller följande steg:

1. [Identifiera utgivare](./discover-collaborators.md): Annonsören identifierar potentiella utgivare att samarbeta med.
2. [Skicka inbjudan](./establishing-connections.md#send-invite): Annonsören skickar en anslutningsinbjudan till den valda utgivaren.
3. [Acceptera inbjudan](./establishing-connections.md#accept-invite): Utgivaren granskar och accepterar inbjudan.
4. [Konfigurera anslutningsinställningar](./establishing-connections.md#configure-connection-settings): Annonsören konfigurerar anslutningsinställningarna och skickar dem till utgivaren för granskning.
5. [Bekräfta anslutningsinställningar](./establishing-connections.md#review-connection-settings): Utgivaren granskar anslutningsinställningarna och godkänner eller avvisar dem. Om anslutningen godkänns upprättas den. Om det inte godkänns kan utgivaren ge återkoppling för revideringar utanför produkten. Annonsören kan sedan granska inställningarna och skicka dem på nytt för granskning.

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

1. [Skicka inbjudan om privat anslutning](./establishing-connections.md#private-connection-invite): En medarbetare skickar en privat anslutningsinbjudan till en annan medarbetare.
2. [Acceptera inbjudan till privat anslutning](./establishing-connections.md#accept-invite): Mottagaren granskar och accepterar inbjudan till privat anslutning.
3. [Konfigurera anslutningsinställningar](./establishing-connections.md#configure-connection-settings): Ägaren konfigurerar anslutningsinställningarna och skickar dem till mottagaren för granskning och godkännande.
4. [Bekräfta anslutningsinställningar](./establishing-connections.md#review-connection-settings): Mottagaren granskar anslutningsinställningarna och godkänner eller avvisar dem.

När anslutningsinställningarna har godkänts upprättas anslutningen och medarbetare är redo att [skapa ett projekt](/help/guide/collaborate/manage-projects.md#create-project) för att börja samarbeta med kampanjer.

## Anslutning mellan annonsörer och reklamplattformar {#advertiser-to-advertising-platform-connection}

Med anslutningsprocessen mellan annonsörer och annonseringsplattformar kan annonsörer ansluta till annonseringsplattformar från tredje part, som Amazon Marketing Cloud (AMC), för att förbättra sina marknadsföringsfunktioner.

### Översikt på hög nivå

Anslutningsprocessen mellan en annonsörer och en annonseringsplattform omfattar flera steg. Kontrollera att du har ett aktivt konto på annonsplattformen och att du har godkänts för att använda deras tjänster innan anslutningsprocessen börjar. I följande steg beskrivs anslutningsprocessen:

1. [Identifiera annonsplattformar](./discover-collaborators.md): Annonsören identifierar möjliga annonsplattformar att samarbeta med.
2. [Anslut till annonseringsplattform](./advertising-platforms/overview.md#advertising-platforms-overview): Annonsören initierar anslutningsprocessen genom att välja den annonsplattform som han/hon vill ansluta till och följer anvisningarna för att autentisera och auktorisera anslutningen.
