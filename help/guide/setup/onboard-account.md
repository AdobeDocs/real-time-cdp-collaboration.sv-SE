---
title: Konfigurera och hantera ditt konto
description: Lär dig konfigurera och hantera olika aspekter av ditt konto i Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# Konfigurera och hantera ditt konto

{{limited-availability-release-note}}

Lär dig hur du konfigurerar ditt konto i Real-Time CDP Collaboration för att förbereda för anslutningar med andra medarbetare. Den här guiden beskriver den inledande konfigurationen av ditt konto, inklusive att lägga till kontoinformation, välja matchningsnycklar och hantera kontoinställningarna.

![Installationsarbetsytan visar ett konfigurerat konto.](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## Konfigurera ditt konto {#set-up-account}

När du första gången öppnar Collaboration uppmanas du att konfigurera ditt konto. Detta är en engångsprocess som gör att du kan konfigurera din kontoinformation och matcha nycklar. Om det här är din organisations första konto dirigeras du direkt genom introduktionsprocessen och börjar med att konfigurera din [kontoinformation](#set-up-details).

Om du vill lägga till fler organisationer går du till **[!UICONTROL Setup]** i den vänstra listen och väljer ikonen Lägg till (![ikonen Lägg till.](/help/assets/icons/plus.png)) i det övre högra hörnet. Välj sedan **[!UICONTROL Account]**.

![Konfigurationsarbetsytan med fliken Mitt konto och kontoalternativet markerat.](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### Ställ in information {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-postadress"
>abstract="Ange ett team- eller rollbaserat e-postmeddelande, till exempel **collaboration@yourcompany.com**. Personliga eller individuella e-postadresser ska inte användas."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Anslut kod"
>abstract="Anslutningskoden är en unik identifierare för ditt konto. Det används för att skapa kontakter med andra medarbetare i Real-Time CDP Collaboration."

För att börja konfigurera ditt konto måste du först konfigurera kontoinformationen. Detta kräver att du lägger till följande information:

* Lägg till en **[!UICONTROL Account name]** som tydligt representerar ditt varumärke.
* Lägg till en **[!UICONTROL Description]** om ditt varumärke. Detta är valfritt, men hjälper andra medarbetare att förstå ert varumärke bättre.
* Välj din **[!UICONTROL Role]**. Du kan välja mellan **[!UICONTROL Advertiser]** och **[!UICONTROL Publisher]**. Läs guiden [roles](/help/guide/overview/roles.md) om du vill se likheter och små skillnader i arbetsflödet mellan de två rolltyperna för kontot.
<!-- The above will need to be updated when I update things for B2B -->
* Välj **[!UICONTROL Industry]** för ditt konto. Några exempel är **[!UICONTROL Retail]**, **[!UICONTROL Telecommunications]** eller **[!UICONTROL Financial services]**.
* **[!UICONTROL Region]** anges automatiskt baserat på ditt Adobe Experience Cloud-konto. Detta kan inte ändras när som helst.
* Lägg till en **[!UICONTROL Contact email]** för ditt konto. Detta ska vara en team- eller rollbaserad e-postadress. Personliga e-postadresser ska inte anges.
* Överför en **[!UICONTROL Logo]** för ditt konto. För närvarande stöds bilder av SVG-typ. Detta är valfritt, men om du överför en logotyp kan du återge ditt varumärke visuellt i Collaboration gränssnitt
* Välj en bild för din kontorubrikbild.

>[!NOTE]
>
>Även om du kan redigera de flesta av dessa uppgifter när som helst går det inte att redigera **[!UICONTROL Role]** efter den första konfigurationen. När du är klar använder du **[!UICONTROL Next]** för att gå till nästa sida och välja de matchningsnycklar som din organisation ska använda.

![Arbetsytan Konfigurera konto med avsnittet Detaljer markerat och alternativet Nästa markerat.](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### Ställ in matchningsnycklar {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Matcha nycklar"
>abstract="Matchningsnycklar är identifierare som används för att stämma av medlemmar mellan olika målgrupper från olika datakällor. Inkludera matchande nycklar som ert varumärke kan arbeta med."

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

>[!IMPORTANT]
>
>De matchningsnycklar som du väljer under kontokonfigurationen avgör vilka matchningsnycklar som är tillgängliga för de anslutningar som du skapar med andra medarbetare. Du kan ta bort matchningsnycklar under anslutningskonfigurationen, men du kan inte lägga till nya matchningsnycklar. Det är viktigt att välja **alla** matchningsnycklar som du vill använda i framtida kampanjer under kontokonfigurationen.

Matcha nycklar, som e-postadresser, enhets-ID:n eller kund-ID:n, hjälper medarbetarna att samarbeta genom att aktivera korrekt och sekretesscentrerad datasynkronisering, vilket ger en mer exakt målgruppsanpassning och mätning.

![Bild som visar tillgängliga identifierare för den första utgåvan av Collaboration.](/help/assets/setup/manage-account/available-identifiers.png)

<!-- Eventually replace this image above to match branding better. -->

Välj de matchningsnycklar som du vill använda när du förenar målgruppsprofiler. Inkludera alla matchningsnycklar som du kan arbeta med. Planera för framtiden och välj de matchningsnycklar som ni tror att ni kommer att använda i framtida kampanjer. Om du behöver välja ytterligare matchningsnycklar för ditt konto vid ett senare tillfälle kan du göra det i arbetsflödet för [redigera konto](#edit-account).

Välj upp till fem matchningsnycklar som du tänker använda. När du senare konfigurerar anslutningar kan du ta bort oönskade matchningsnycklar, men inte lägga till nya.

Det finns tre typer av tillgängliga matchningsnycklar:

* Personliga ID:n för första part
* Enhets-ID:n från första part
* Partner-ID

>[!IMPORTANT]
>
>Den enda matchningsnyckel som stöds för närvarande är hashad e-post.

När det är klart väljer du **[!UICONTROL Complete]** för att slutföra arbetsflödet för organisationskonfiguration.

![Arbetsytan Konfigurera organisation med avsnittet Matcha nycklar visas.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Redigera konto {#edit-account}

När du har konfigurerat ditt konto kan du när som helst redigera vissa aspekter och detaljer för kontot. Om du vill redigera ditt konto väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL My account]** på arbetsytan **[!UICONTROL Setup]**.

![Arbetsytan Konfigurera med fliken Mitt konto och alternativet Redigera markerat.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Nu kan du redigera din kontoinformation, med undantag för **[!UICONTROL Role]**. Observera att regionen ställs in automatiskt baserat på ditt Adobe Experience Cloud-konto och inte kan ändras när som helst.

![Dialogrutan Redigera kontoinformation.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

Du kan också uppdatera de matchningsnycklar som du valde från början när du kom igång med organisationen. Välj **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Match keys]** om du vill lägga till fler matchningsnycklar.

![Arbetsytan Konfigurera med alternativet Redigera markerat i avsnittet Matcha nycklar för kontot.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

## Nästa steg

När du har konfigurerat dina konton är du redo att [hämta målgrupper](/help/guide/setup/onboard-audiences.md) till Real-Time CDP Collaboration.
