---
title: Senaste versionsinformation för Real-Time CDP Collaboration
description: Följ de senaste versionerna av Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 8ab3cc35872f45b1337bac7b0fa453c9937d78da
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 1%

---

# Senaste versionsinformation för Real-Time CDP Collaboration

{{limited-availability-release-note}}

**Senast uppdaterad**: augusti 2025.

Versionsinformationen innehåller information om de funktioner som lanserats i Adobe Real-Time CDP Collaboration. Collaboration-releaser fungerar enligt en kontinuerlig leveransmodell, vilket möjliggör en ungefärlig månadsvis publiceringsgräns. Versionsinformationen uppdateras ofta, så kontrollera dem regelbundet.

## Augusti 2025 {#august-2025}

Real-Time CDP Collaboration är nu tillgängligt för kunder i **Kanada**. Det är automatiskt tillgängligt för kunder som har Real-Time CDP Prime och Ultimate i dessa länder.

* Collaboration har nu stöd för följande [matchningsnycklar](../setup/onboard-account.md#supported-match-keys):
   * Hash-kodad e-post
   * Hash-kodat telefonnummer
   * CRM-ID
   * Förmåns-ID
   * Hash-kodad IPv4
   * AdFixus-ID
* Flera matchningsnycklar finns nu tillgängliga i hela Collaboration, vilket ger er möjlighet att utöka er målgruppsstorlek och förbättra matchningsfrekvensen. Flera matchningsnycklar kan användas när målgrupper hämtas, ansluts och målgrupper aktiveras. Läs [Konfigurera matchningsnycklar](../setup/onboard-account.md) och [hämta målgruppsguider](../setup/onboard-audiences.md#map-fields) om du vill veta mer om hur du använder flera matchningsnycklar.

>[!IMPORTANT]
>
>Vid aktivering av målgrupper där flera matchningsnycklar används, om en (eller flera) matchningsnyckel inte har några överlappningar, inget antal målgrupper eller faller under tröskelvärdet, misslyckas hela aktiveringen. Se till att era målgrupper har tillräcklig överlappning och att de uppfyller det lägsta tröskelvärdet på 1 000 ID:n för alla matchningsnycklar innan de aktiveras.

* Adobe Experience Platform-destinationen har nu stöd för aktivering av målgrupper med flera matchningsnycklar. Dessutom kan du nu använda en länkad nyckel när du konfigurerar målmappningen för att ange vilken matchningsnyckel som skickas under aktiveringen. Läs [Experience Platform-målguiden](../destinations/experience-platform.md#linked-keys) om du vill veta mer.
* Medarbetare kan nu redigera flera målgrupper samtidigt. Nu kan du redigera målgruppsmetadata, anslutningsåtkomst, namn, beskrivningar och kategorier för flera målgrupper med hjälp av gruppredigeringsverktyget. Läs handboken [Hantera målgrupper](../setup/onboard-audiences.md#edit-audiences) om du vill veta mer om hur du redigerar målgrupper.

## Juli 2025 {#july-2025}

CDP Collaboration i realtid har nu stöd för varumärkessamarbete. Medarbetare kan nu skapa formuläranslutningar oavsett om de är annonsörer eller utgivare. På så sätt får ni flexiblare samarbetsmöjligheter och varumärkena kan utnyttja varandras data och insikter. Om du vill veta mer om skillnaderna mellan varumärkessamarbete och samarbete mellan annonsörer och utgivare läser du [samarbetsmönstren](../overview/collaboration-patterns.md).

* Medarbetare kan nu ansluta till varandra med [privata anslutningsinbjudningar](../connect/establishing-connections.md#private-connection-invites). Dela kontots unika anslutningskod med en medarbetare som sedan kan använda den för att ansluta direkt till dig. Detta är en viktig funktion i samarbetet mellan varumärken, som gör det möjligt för samarbetspartners att skapa anslutningar utöver annonsörer som utforskar katalogen **[!UICONTROL Discover publishers]**.
* [Självbetjäningsmål](../setup/manage-destinations.md) är nu tillgängliga för både annonsörer och utgivare.
* Målgruppsaktivering är nu tillgänglig för båda medarbetarna i en anslutning, oavsett deras [kontoroll](../overview/roles.md). Inställningarna för målgruppsaktivering konfigureras medan [anslutningar](../connect/establishing-connections.md#configure-connection-settings) upprättas, vilket gör att du kan ange vilken medarbetare som kan aktivera målgrupper. Läs guiden [Aktivera målgrupper](../collaborate/activate.md) om du vill veta mer om målgruppsaktivering.
* **[!UICONTROL Activate]**-användningsexemplet har konfigurerats om så att det stöder samarbete mellan varumärken. Fliken **[!UICONTROL Activate]** i ett projekt visar nu vilka målgrupper som har skickats till din medarbetare och vilka målgrupper som har aktiverats till ditt mål av din medarbetare. Läs handboken [Aktivera målgrupper](../collaborate/activate.md) om du vill veta mer. <br> ![Kontrollpanelen Aktivera med avsnitten Målgrupper skickade till och Publiker aktiverade.](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}
* Poängen för målgruppsindex är nu tillgängliga på fliken **[!UICONTROL Discover]** i ett projekt. Poängen i målgruppsindexet är ett mått på hur bra en målgrupp matchar medarbetarens målgrupp. Poängen beräknas utifrån underliggande antal målgrupper och överlappningar. Läs guiden [målgruppsindexpoäng](../collaborate/discover.md#audience-index-score) om du vill veta mer om poängen i målgruppsindexen.

## Maj 2025 {#may-2025}

* Real-Time CDP Collaboration är nu tillgängligt för kunder i **Australien** och **Nya Zeeland**. Det är automatiskt tillgängligt för kunder som har Real-Time CDP Prime och Ultimate i dessa länder.
* Real-Time CDP Collaboration erbjuder nu [självbetjäningsmål](../setup/manage-destinations.md) via fliken **[!UICONTROL My destinations]** i avsnittet **[!UICONTROL Setup]**. Med destinationer kan ni aktivera målgrupper på tredjepartsplattformar, som annonsnätverk eller datahanteringsplattformar, för att nå era kunder i olika kanaler. För närvarande stöds endast Adobe Experience Platform-mål. Om du är intresserad av att konfigurera ett annat mål kontaktar du Adobe. Mer information om destinationer finns i guiden [Målöversikt](../destinations/overview.md).
   * Destinationer lägger även till stöd för att visa Collaboration-målgrupper i [Adobe Experience Platform målportalen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences).
* Nu kan du redigera målgruppens uppdateringsfrekvens för befintliga dataanslutningar i Collaboration. För närvarande kan ni välja att uppdatera era målgrupper dagligen eller varannan till var sjätte dag. Läs guiden [Hantera dataanslutningar](../setup/manage-data-connection.md#scheduling) om du vill veta mer om hur du redigerar målgruppens uppdateringsfrekvens.
* Kreditdelningar mellan medarbetare ställs nu in för varje användningsfall som väljs i anslutningen. Du kan ange olika regler för kreditförbrukning för varje användningsfall för att bättre kontrollera hur dina krediter används. Mer information om kreditdelningsfunktionerna finns i guiden [anslutningsinställningar](../connect/establishing-connections.md#connection-settings). Läs handboken [Kreditaktivitetstyper](../setup/my-activity.md#types-of-activities) om du vill veta mer om hur krediter förbrukas. <br> ![Skärmen Anslutningsinställningar visar funktionen för kreditdelning.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Utgivare kan nu ange annonsörernas namn och ID:n innan de godkänner anslutningsinställningarna från en annonsörer. Utgivare kan ange namn och ID:n som är anpassade till deras interna system, som kan skilja sig från annonsörens namn och ID:n. Läs handboken [Anslutningsinställningar](../connect/establishing-connections.md#connection-settings.md) om du vill veta mer om hur du lägger till annonsörnamn och ID:n. <br> ![Skärmen Anslutningsinställningar visar utgivarens inställningar för annonsörnamn och ID.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## April 2025 {#april-2025}

* En ny **[!UICONTROL Inputs Processed]**-kolumn har lagts till i registret för kreditförbrukningsaktivitet. I den här kolumnen visas det totala antalet indata (till exempel ID eller rader) som bearbetas för varje aktivitet. [Läs mer](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Inmatar bearbetad kolumn som är markerad i Min aktivitetsvy.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* Ett nytt e-postalternativ för kontakt har lagts till för att skapa konto. Detta hjälper partnersamarbetspartners att kontakta dig vid behov under anslutningsprocessen. [Läs mer](../setup/onboard-account.md).

## Mars 2025 {#march-2025}

* När [hämtar målgrupper](/help/guide/setup/onboard-audiences.md) till Collaboration kan du nu ange en målgruppsuppdateringsfrekvens från **var och en till sex dagar** för att bättre hantera [Audience Management-kreditaktiviteten](/help/guide/setup/my-activity.md#types-of-activities). Mer information finns i guiden [Hantera målgrupper](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences). <br> ![Schemaläggningsskärmen visar olika frekvensintervall för uppdatering av målgruppsmedlemskap.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Schemaläggningsskärmen visar olika frekvensintervall för uppdatering av målgruppsmedlemskap."){width="250" align="center" zoomable="yes"}
* När du upprättar en anslutning med en medarbetare kan du nu välja bland fördefinierade **användningsfall**. Det valda användningsfallet avgör vilka projektavsnitt och vilken produktfunktionalitet som blir tillgänglig. Mer information finns i guiden [hantera projekt](/help/guide/collaborate/manage-projects.md#project-use-cases).
   * *Mätning* aktiverar projektavsnittet **Åtgärd**.
   * *Målgruppsidentifiering* aktiverar projektavsnittet **Discover**.
   * *Målgruppsaktivering* aktiverar **Aktivera** projektavsnitt <br>
* Nu kan du ta bort anslutningar med medarbetare som du inte längre vill arbeta med. Läs handboken [Ta bort anslutningar](/help/guide/connect/establishing-connections.md#delete-connections) om du vill lära dig hur du tar bort anslutningar.

## Februari 2025 {#february-2025}

Adobe Real-Time CDP Collaboration, som är konstruerat för att göra det möjligt för annonsörer och utgivare att upptäcka, aktivera och mäta värdefulla målgrupper utan cookies från tredje part, är nu allmänt tillgängligt i USA.

### Kom igång

1. **Åtkomstinställningar**: Systemadministratörer konfigurerar åtkomstbehörigheter för användare. Läs guiden [Hantera användaråtkomst](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access) om du vill veta mer om hur du konfigurerar åtkomstbehörigheter.
2. **Koppla datakällor**: Source målgrupper som ska användas i Collaboration. Läs [källan och hantera målgrupper](/help/guide/setup/onboard-audiences.md) om du vill börja anlita målgrupper.
3. **Upprätta anslutningar**: Börja samarbeta med betrodda annonsörer eller utgivare. Mer information om hur du skapar anslutningar finns i guiden [upprättar anslutningar](/help/guide/connect/establishing-connections.md).
4. **Identifiera och aktivera**: Skapa projekt för att identifiera värdefulla målgrupper som ska aktiveras i kampanjer. Mer information om hur du skapar projekt finns i guiden [hantera projekt](/help/guide/collaborate/manage-projects.md).

### Tillgänglighet

* Adobe Real-Time CDP Collaboration är för närvarande endast tillgängligt för kunder i USA.
* Det är automatiskt tillgängligt för kunder som har Adobe Real-Time CDP Prime och Ultimate

Mer information finns i:

* [Collaboration - översikt](/help/guide/home.md)
* [Arbetsflöde från början till slut](/help/guide/overview/end-to-end-workflow.md)
* [Översikt över behörigheter](/help/guide/permissions/overview.md)
