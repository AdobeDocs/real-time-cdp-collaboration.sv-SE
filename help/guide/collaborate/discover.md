---
title: Upptäck överlappningar och jämför målgrupper
description: Upptäck överlappningar mellan era och medarbetarnas målgrupper. Lär dig hur ni hittar de bästa målgrupperna som kan användas i era kampanjer.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---

# Upptäck överlappningar och jämför målgrupper

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Discover]** är bara tillgänglig om **målgruppsidentifiering** har aktiverats [ under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

När du har [skapat ett projekt](/help/guide/collaborate/manage-projects.md) i en samarbetsyta mellan en annonsörer och en utgivare kan du nu jämföra dina målgrupper med dina medarbetares målgrupper. På så sätt kan ni upptäcka överlappningar mellan olika målgrupper och få insikter nedbrutna efter matchningsnycklar eller identiteter. Detta hjälper annonsörer att avgöra vilka målgrupper de ska dela med utgivare för aktivering.

>[!IMPORTANT]
>
>Alla [dataskisser](/help/guide/glossary.md#sketches) som inte uppdateras eller uppdateras kommer att tas bort efter 7 dagar. När detta händer kommer siffrorna som visas i de olika överlappande rapporterna på den här sidan att nollställas och målgruppsdelning blir otillgänglig för dessa utgångna målgrupper. Dataskiseringar uppdateras automatiskt för målgrupper med ett [aktivt uppdateringsschema](/help/guide/setup/onboard-audiences.md#schedule).

![Identifiera överlappningar](/help/assets/collaborate/discover-overlaps/discover-overlaps.png)

De matchningsnycklar som används för att identifiera och jämföra målgrupper anges när du [ansluter till en utgivare](/help/guide/connect/establishing-connections.md#connection-settings). Om du vill ändra de överlappningsprocentsatser som anges som förberedelse för pågående kampanjer kan du ta bort matchningsnycklar, men du kan inte lägga till nya matchningsnycklar just nu. Gå till [anslutningsinställningarna](/help/guide/connect/establishing-connections.md#connection-settings) mellan medarbetarna för att göra det.

![Skärmen Redigera matchande tangenter](/help/assets/collaborate/discover-overlaps/edit-match-keys.png)

## Förhandskrav {#prerequisites}

Om du vill utnyttja funktionerna på fliken **[!UICONTROL Discover]** i arbetsflödet **[!UICONTROL Collaborate]** till fullo har du redan:

* [Importerade målgrupper](/help/guide/setup/onboard-audiences.md)
* [Ansluten](/help/guide/connect/establishing-connections.md) till en annonsör eller utgivare med **Användningsfall för målgruppsidentifiering** aktiverat
* [Skapade ett projekt](/help/guide/collaborate/manage-projects.md) mellan dig och en medarbetare

När ovanstående förutsättningar är uppfyllda kan ni börja utforska och jämföra överlappningen mellan er och medarbetarens målgrupper.

## Jämför målgrupper {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Jämför målgrupper"
>abstract="Upptäck överlappningar mellan er och medarbetarens målgrupper. Du kan justera inställningarna i listruteväljaren för att upptäcka överlappningar mellan en eller flera av dina målgrupper och en eller flera av dina medarbetares målgrupper."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Ditt identitetsantal"
>abstract="Antalet profiler med den valda identiteten som är en del av den valda målgruppen"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Identitetsantal för medarbetare"
>abstract="Antalet profiler med den valda identiteten som är en del av medarbetarens valda målgrupp"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Antal överlappande identiteter"
>abstract="Antalet profiler med den valda identiteten som finns både i din och medarbetarens målgrupp"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Procentandel överlappande identiteter"
>abstract="Procentandelen profiler som överlappar den valda målgruppen för er och medarbetaren."

Använd jämförelsekortet för att få omfattande information om överlappningen mellan er och medarbetarens målgrupper. Du kan välja att jämföra följande målgruppskombinationer:

* En av era målgrupper mot en av era medarbetare
* En av era målgrupper mot alla era medarbetares målgrupper
* Alla era målgrupper mot en av era medarbetares målgrupper
* Alla era målgrupper mot alla era medarbetares målgrupper

Den information som visas gäller:

| Mått | Beskrivning |
|---------|----------|
| **[!UICONTROL Identity count]** (din) | Antalet profiler med en vald identitet som ingår i den valda målgruppen. |
| **[!UICONTROL Identity count]** (din medarbetare) | Antalet profiler med en vald identitet som ingår i medarbetarens valda målgrupp. |
| **[!UICONTROL Overlapping identities]** | Antalet profiler med en vald identitet som finns både i din och medarbetarens målgrupp. |
| **[!UICONTROL Overlap percentage]** | Procentandelen profiler som överlappar den valda målgruppen för er och medarbetaren. |
| **[!UICONTROL Identities breakdown by match key]** | Baserat på de matchningsnycklar du och din medarbetare kommit överens om för projektet kan du visa identitetsdispositionen i överlappningsberäkningarna med enskilda matchningsnycklar. |

{style="table-layout:auto"}

>[!TIP]
>
>Procenttalet för överlappning kanske inte alltid är tillgängligt för alla målgrupper. Hur synlig indikatorn för överlappningsprocenten är beror på inställningen som medarbetaren valde för en målgrupp i [metadatasynlighetsavsnittet](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Relevanta målgrupper {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Relevanta målgrupper"
>abstract="Utifrån överlappningsprocentsatser kan dessa utgivarmålgrupper vara ett bra val för er kampanj. <br><br> <b>Identitetsantalet</b> är utgivarens målgruppsstorlek. <br><br> <b>Överlappande identiteter</b> representerar överlappningen mellan den rekommenderade utgivarens målgrupp och alla annonsörers målgrupper. <br><br> <b>Överlappningen %</b> representerar antalet överlappande identiteter dividerat med storleken på <i>alla</i> annonsörer."

Vyn **[!UICONTROL Relevant audiences]** i modulen **[!UICONTROL Discover]** innehåller en strukturerad lista över de fem främsta målgrupperna baserat på överlappningsprocenten. Med den här funktionen kan ni snabbt identifiera målgrupperna med den största överlappningen med era aktuella data, vilket gör att ni kan inrikta era kampanjer mer effektivt.

* **[!UICONTROL Identity count]** är utgivarens målgruppsstorlek.
* **[!UICONTROL Overlapping identities]** representerar överlappningen mellan den rekommenderade utgivarens målgrupp och alla annonsörers målgrupper.
* **[!UICONTROL Overlap %]** representerar antalet överlappande identiteter dividerat med storleken på *alla* annonsörer.

![Vyn Relevanta målgrupper](/help/assets/collaborate/discover-overlaps/relevant-audiences-highlighted.png)

## Upptäck överlappningar {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Upptäck överlappningar med enskilda målgrupper"
>abstract="Få insikter om den här målgruppens befolkning och hur den överlappar medarbetarens värld av identiteter."

![Upptäck överlappningar med olika målgruppsvy](/help/assets/collaborate/discover-overlaps/discover-overlaps-cards-view.png)

Få omfattande information om någon av era medarbetares målgrupper och visa överlappande information som jämför dessa målgrupper med antingen hela din populationsmängd för alla era målgrupper eller mot specifika målgrupper.

>[!TIP]
>
>En del av de siffror som visas på skärmbilden kanske inte alltid är tillgängliga för alla målgrupper. Hur synliga de är beror på inställningen som medarbetaren valde för en målgrupp i avsnittet [metadatasynlighet](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Nästa steg

När du har utforskat och identifierat de önskade målgrupperna är det dags att [dela](/help/guide/collaborate/share.md) de målgrupper som ska användas i kampanjerna med utgivaren.
