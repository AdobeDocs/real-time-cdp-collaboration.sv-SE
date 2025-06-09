---
title: Senaste versionsinformation för Real-Time CDP Collaboration
description: Följ de senaste versionerna av Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 6b945c78202ca7ad6366baa265a08381953adc2e
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 3%

---

# Senaste versionsinformation för Real-Time CDP Collaboration

{{limited-availability-release-note}}

**Senast uppdaterad**: april 2025.

Versionsinformationen innehåller information om de funktioner som finns i Real-Time Customer Data Platform Collaboration. Real-Time CDP Collaboration-releaser fungerar enligt en kontinuerlig leveransmodell, vilket möjliggör en ungefärlig månadsvis publiceringsgräns. Versionsinformationen uppdateras ofta, så kontrollera dem regelbundet.

## Maj 2025 {#may-2025}

* Real-Time CDP Collaboration är nu tillgängligt för kunder i **Australien** och **Nya Zeeland**. Det är automatiskt tillgängligt för kunder som har Real-Time CDP Prime och Ultimate i dessa länder.
* Real-Time CDP Collaboration erbjuder nu [självbetjäningsdesigner](../setup/manage-destinations.md) via fliken Mina designer under Konfigurera. Med destinationer kan ni aktivera målgrupper på tredjepartsplattformar, som annonsnätverk eller datahanteringsplattformar, för att nå era kunder i olika kanaler. För närvarande stöds endast Adobe Experience Platform-mål. Om du är intresserad av att konfigurera ett annat mål kontaktar du Adobe. Mer information om destinationer finns i guiden [Målöversikt](../destinations/overview.md).
   * Destinationer lägger även till stöd för att visa Real-Time CDP Collaboration-målgrupper i [Adobe Experience Platform målportalen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences.).
* Nu kan du redigera målgruppens uppdateringsfrekvens för befintliga dataanslutningar i Real-Time CDP Collaboration. För närvarande kan ni välja att uppdatera era målgrupper dagligen eller varannan till var sjätte dag. Läs guiden [Hantera dataanslutningar](../setup/manage-data-connection.md#scheduling) om du vill veta mer om hur du redigerar målgruppens uppdateringsfrekvens.
* Kreditdelningar mellan medarbetare ställs nu in för varje användningsfall som väljs i anslutningen. Du kan ange olika regler för kreditförbrukning för varje användningsfall för att bättre kontrollera hur dina krediter används. Mer information om kreditdelningsfunktionerna finns i guiden [anslutningsinställningar](../connect/establishing-connections.md#connection-settings). Läs handboken [Kreditaktivitetstyper](../setup/my-activity.md#types-of-activities) om du vill veta mer om hur krediter förbrukas. <br> ![Skärmen Anslutningsinställningar visar funktionen för kreditdelning.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Utgivare kan nu ange annonsörernas namn och ID:n innan de godkänner anslutningsinställningarna från en annonsörer. Utgivare kan ange namn och ID:n som är anpassade till deras interna system, som kan skilja sig från annonsörens namn och ID:n. Läs handboken [Anslutningsinställningar](../connect/establishing-connections.md#connection-settings.md) om du vill veta mer om hur du lägger till annonsörnamn och ID:n. <br> ![Skärmen Anslutningsinställningar visar utgivarens inställningar för annonsörnamn och ID.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## April 2025 {#april-2025}

* En ny **[!UICONTROL Inputs Processed]**-kolumn har lagts till i registret för kreditförbrukningsaktivitet. I den här kolumnen visas det totala antalet indata (till exempel ID eller rader) som bearbetas för varje aktivitet. [Läs mer](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Inmatar bearbetad kolumn som är markerad i Min aktivitetsvy.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* Ett nytt e-postalternativ för kontakt har lagts till för att skapa konto. Detta hjälper partnersamarbetspartners att kontakta dig vid behov under anslutningsprocessen. [Läs mer](../setup/onboard-organization.md).

## Mars 2025 {#march-2025}

* När du [importerar målgrupper](/help/guide/setup/onboard-audiences.md) till Real-Time CDP Collaboration kan du nu ange en målgruppsuppdateringsfrekvens från **var och en till sex dagar** för att bättre hantera [målgruppshanteringens kreditaktivitet](/help/guide/setup/my-activity.md#types-of-activities). [Läs mer](/help/guide/setup/onboard-audiences.md#schedule). <br> ![Schemaläggningsskärmen visar olika frekvensintervall för uppdatering av målgruppsmedlemskap.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Schemaläggningsskärmen visar olika frekvensintervall för uppdatering av målgruppsmedlemskap."){width="250" align="center" zoomable="yes"}
* När du upprättar en anslutning med en medarbetare kan du nu välja bland fördefinierade **användningsfall**. Det valda användningsfallet avgör vilka projektavsnitt och vilken produktfunktionalitet som blir tillgänglig. [Läs mer](/help/guide/collaborate/manage-projects.md#project-use-cases).
   * *Kampanjmätning* aktiverar projektavsnittet **Åtgärd**.
   * *Målgruppsidentifiering* aktiverar projektavsnittet **Discover**.
   * *Målgruppsaktivering* aktiverar **Aktivera** projektavsnitt <br>
* Nu kan du ta bort anslutningar med medarbetare som du inte längre vill arbeta med. [Läs mer](/help/guide/connect/establishing-connections.md#delete-connections).


## Februari 2025 - Allmän tillgänglighet för kunder i USA {#february-2025-ga}

Real-Time CDP Collaboration, som är konstruerat för att göra det möjligt för annonsörer och utgivare att upptäcka, aktivera och mäta värdefulla målgrupper utan cookies från tredje part, är nu allmänt tillgängligt i USA.

### Kom igång

1. **Åtkomstinställningar**: Systemadministratörer konfigurerar åtkomstbehörigheter för användare. [Läs mer](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access).
2. **Anslut datakällor**: Importera målgrupper som ska användas i Real-Time CDP Collaboration. [Läs mer](/help/guide/setup/onboard-audiences.md).
3. **Upprätta partneranslutningar**: Börja samarbeta med betrodda varumärken eller utgivare. [Läs mer](/help/guide/connect/establishing-connections.md).
4. **Identifiera och aktivera**: Skapa projekt för att identifiera värdefulla målgruppssegment och aktivera i kampanjer. [Läs mer](/help/guide/collaborate/manage-projects.md).

### Tillgänglighet

* Real-Time CDP Collaboration är för närvarande endast tillgängligt för kunder i USA.
* Det är automatiskt tillgängligt för kunder som har Real-Time CDP Prime och Ultimate

Mer information finns i:

* [Real-Time CDP Collaboration - översikt](/help/guide/home.md)
* [Arbetsflöde från början till slut](/help/guide/end-to-end-workflow.md)
* [Översikt över behörigheter](/help/guide/permissions/overview.md)
