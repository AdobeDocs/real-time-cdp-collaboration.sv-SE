---
title: Anlita och hantera organisationen
description: Läs om hur du kan integrera och hantera olika aspekter av din organisation i Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 27faef284a07be114ea0a9a7beeae75ec6265d53
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Anlita och hantera organisationen

{{limited-availability-release-note}}

Lär dig hur du kan få med din organisation på Real-Time CDP Collaboration och hantera olika aspekter av ditt företag. På den här sidan beskrivs stegen för hur du kan integrera en organisation i Adobe Real-Time CDP Collaboration, inklusive hur du ställer in matchningsnycklar, önskade identiteter och fler alternativ.

![Konfigurationssida](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Inledande konfiguration av organisation

Du måste först konfigurera din organisation och organisationsinformation. Navigera till **[!UICONTROL Setup]** i den vänstra listen, markera symbolen **+** i det övre högra hörnet och välj **[!UICONTROL Account]**.

>[!TIP]
>
>När du har konfigurerat ett första konto som du vill arbeta med kan du använda samma arbetsflöde för att skapa ytterligare konton i samma organisation.

![Välj Konto om du vill lägga till en ny organisation i Real-Time CDP Collaboration](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

Arbetsflödet för att konfigurera din organisation omfattar de två sidorna nedan:

* [Ställ in information](#set-up-details)
* [Konfigurera matchningsnycklar](#set-up-match-keys)

>[!IMPORTANT]
>
>Alla *matchande nycklar* som du väljer på organisationsnivå kommer sedan att tricksas ned till [projektnivå](/help/guide/collaborate/manage-projects.md) i samarbetet mellan annonsörer och utgivare. På projektnivå kan du sedan ta bort matchningsnycklar, men du kan *inte* lägga till fler som inte har valts på organisationsnivå på den här skärmen.

### Ställ in information {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-postadress"
>abstract="Ange ett team- eller rollbaserat e-postmeddelande, till exempel `collaboration@yourcompany.com`. Personliga eller individuella e-postadresser ska inte användas."

![Information och användningsexempel för att konfigurera en organisation](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

1. Lägg till en **[!UICONTROL Organization name]** för ditt företag.
2. Lägg till en **[!UICONTROL Description]** om ditt företag.
3. Välj din **[!UICONTROL Company role]**. Du kan välja mellan **[!UICONTROL Advertiser]** och **[!UICONTROL Publisher]**. Läs arbetsflödesdokumentet [från början till slut](/help/guide/end-to-end-workflow.md) om du vill se likheter och små skillnader i arbetsflödet mellan de två rolltyperna för organisationen.
4. Välj **[!UICONTROL Industry]** för din organisation. Några exempel är **[!UICONTROL Retail]**, **[!UICONTROL Telecommunications]** eller **[!UICONTROL Financial services]**.
5. Välj **[!UICONTROL Region]** för din organisation. I den aktuella versionen av produkten är **[!UICONTROL North America]** det förinställda standardvalet.
6. Lägg till en **[!UICONTROL Contact email]** för din organisation. Detta ska vara en team- eller rollbaserad e-postadress. Personliga e-postadresser ska inte anges.
7. Överför en **[!UICONTROL Logo]** för ditt företag. För närvarande stöds bilder av SVG-typ.
8. Välj en bild för företagets rubrikbild.

När du är nöjd med ditt val kan du använda **[!UICONTROL Next]** för att gå till nästa sida och välja önskade matchningsnycklar som din organisation ska använda.

### Ställ in matchningsnycklar {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Matcha nycklar"
>abstract="Matchningsnycklar är identifierare som används för att stämma av medlemmar mellan olika målgrupper från olika datakällor. Ta med matchningsnycklar som företaget kan arbeta med."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="Personliga ID:n för första part"
>abstract="Personliga ID:n från första part, som hash-kodade e-postadresser eller telefonnummer, är direkt kopplade till en enskild profil. ID:n som stöds för närvarande är hashkodade e-postmeddelanden och telefonnummer."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="Enhets-ID:n från första part"
>abstract="Första parts enhets-ID som ECID eller IP-adresser är direkt anslutna till enheter, som kan delas mellan flera personer. IPv4 är det enda enhets-ID som stöds för tillfället."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="Partners-ID som stöds"
>abstract="Partner-ID:n som är kopplade till profiler utökar räckvidden till en viss profil."

Matcha nycklar, som e-postadresser, enhets-ID:n eller kund-ID:n, hjälper annonsörer och utgivare att samarbeta genom att aktivera korrekt och sekretesscentrerad datasynkronisering, vilket ger en mer exakt målgruppsanpassning och mätning.

![Bild som visar tillgängliga identifierare för den första utgåvan av Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Välj de matchningsnycklar som du vill använda när du förenar medlemmar i utgivar- och annonsörernas målgrupper. Ta med matchningsnycklar som företaget kan arbeta med. Planera för framtiden och välj de matchningsnycklar som du tror att du kommer att använda i framtida annonskampanjer. Om du behöver välja ytterligare matchningsnycklar för din organisation kan du även göra det senare i arbetsflödet för [redigeringsorganisationen](#edit-organization).

![Välj nycklar.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Välj upp till fem matchningsnycklar som du tänker använda. När du senare konfigurerar anslutningar kan du ta bort oönskade matchningsnycklar, men inte lägga till nya.

Tillgängliga matchningsnycklar i Real-Time CDP Collaboration kan vara av tre typer:

* Personliga ID:n för första part
* Enhets-ID:n från första part
* Partner-ID

De tillgängliga matchningsnycklarna för den första utgåvan av Real-Time CDP Collaboration är:

* Hash-kodad e-post

<!--

not available in the Limited GA release

* Hashed phone
* IPv4

-->

När det är klart väljer du **[!UICONTROL Complete]** för att slutföra arbetsflödet för organisationskonfiguration.

## Redigera organisation {#edit-organization}

När du har konfigurerat din organisation kan du när som helst redigera vissa aspekter av organisationen. Om du vill redigera din organisation väljer du **[!UICONTROL Edit]** i vyn **[!UICONTROL My organization]**.

![Redigera organisationskontroll är markerat.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

Nu kan du uppdatera företagsnamnet, beskrivningen, logotypen och organisationsprofilbilden.

![Redigerbara alternativ för organisationer.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

Du kan också uppdatera de matchningsnycklar som du valde från början när du introducerade organisationen, samt det lägsta tröskelvärdet för identiteter som motsvarar matchningsnycklar som ska vara synliga och användbara i målgruppsöverlappningar och andra produktområden. Välj **[!UICONTROL Edit]** på fliken **[!UICONTROL Match keys]** om du vill lägga till fler matchningsnycklar eller uppdatera identitetströsklar.

![Redigera matchningsnycklar](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Nästa steg

När du har konfigurerat din organisation kan du [importera målgrupper](/help/guide/setup/onboard-audiences.md) till Real-Time CDP Collaboration.
