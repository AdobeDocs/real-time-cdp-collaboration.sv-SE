---
title: Konfigurera och hantera ditt konto
description: Lär dig konfigurera och hantera olika aspekter av ditt konto i Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: c9e2e8607dde87c4a36b131ed434195ef77730e6
workflow-type: tm+mt
source-wordcount: '1297'
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
>abstract="Matchningsnycklar är identifierare som används för att matcha målgruppsprofiler från olika datakällor. Inkludera matchande nycklar som ert varumärke kan arbeta med."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_setup_match_keys"
>title="matchningsnycklar"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="Personliga ID:n för första part"
>abstract="Personliga ID:n från första part, som hash-kodade e-postadresser, hashade telefonnummer eller CRM-ID:n, är direkt kopplade till en enskild profil."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="Enhets-ID:n från första part"
>abstract="Första parts enhets-ID, t.ex. ECID eller IP-adresser, är direkt anslutna till enheter, som kan delas mellan flera personer. IPv4 är det enda enhets-ID som stöds för tillfället."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="Partners-ID som stöds"
>abstract="Partner-ID:n är identifierare som tillhandahålls av externa partner för målgruppsavstämning. Partner-ID:n är inte direkt kopplade till en enskild profil."

![Matchningsnycklar som stöds.](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>De matchningsnycklar som du väljer under kontokonfigurationen avgör vilka matchningsnycklar som är tillgängliga i dina anslutningar. Du kan [ta bort oönskade matchningsnycklar](../connect/establishing-connections.md#connection-settings) under anslutningskonfigurationen, men det går inte att lägga till matchningsnycklar efter att en anslutning har upprättats. Det är viktigt att du väljer **alla** matchningsnycklar som du tänker använda i framtida kampanjer under kontokonfigurationen.

Matcha nycklar hjälper medarbetare att samarbeta genom att möjliggöra korrekt och sekretesscentrerad datasynkronisering, vilket ger en mer exakt målgruppsanpassning och mätning. Matcha nycklar som valts under kontokonfiguration avgör vilka matchningsnycklar som är tillgängliga i framtida anslutningar. De används också för att [mappa fält](./onboard-audiences.md#map-fields) från din dataanslutning till målfälten i Collaboration när målgrupper hämtas.

Välj de matchningsnycklar som du vill använda när du förenar målgruppsprofiler. Planera för framtiden och inkludera matchningsnycklar som ni kan arbeta med och förutse med i framtida kampanjer. Om du behöver välja ytterligare matchningsnycklar för ditt konto vid ett senare tillfälle kan du göra det i arbetsflödet för [redigera konto](#edit-account). Eventuella matchningsnycklar som läggs till efter den första konfigurationen kommer dock inte att vara tillgängliga för användning i befintliga anslutningar.

#### Matchningsnycklar som stöds {#supported-match-keys}

Collaboration har stöd för tre typer av matchningsnycklar: ID:n för första part, enhets-ID:n för första part och partner-ID:n. Alla matchningsnycklar måste uppfylla följande krav:

* Matchningsnycklar måste vara **trimmade**, **nedsänkta**
* Hash-kodade matchningsnycklar måste vara **SHA256-hashed**.
* Om du anger hash-värden som använder versaler konverteras de automatiskt till gemener i Collaboration.
* Om källan innehåller **klartextidentifierare** använder du alternativet **[!UICONTROL Apply transformation]** under [dataanslutningskonfigurationen](./manage-data-connection.md#match-keys) för att tillämpa hashning. Det här alternativet är endast tillgängligt när du hämtar målgrupper från Experience Platform och stöds inte för molnbaserade källor.

##### Personliga ID:n för första part

Personliga ID:n för första part är direkt kopplade till en enskild profil. Följande ID stöds för närvarande:

* **[!UICONTROL Hashed email]**
* **[!UICONTROL Hashed phone]**
* **[!UICONTROL CRM IDs]**
* **[!UICONTROL Loyalty IDs]**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### Enhets-ID:n från första part

Första parts enhets-ID är identifierare som är anslutna till en viss enhet. Följande ID stöds för närvarande:

* **[!UICONTROL Hashed IPv4]**: Hash-kodade IPv4-adresser

##### Partner-ID

Partner-ID:n är identifierare som tillhandahålls av externa partner för målgruppsavstämning. Följande ID stöds för närvarande:

* **[!UICONTROL AdFixus ID]**

>[!NOTE]
>
>Adobe-integrering med [!DNL AdFixus] mappar unika [!UICONTROL AdFixus IDs] för varje konto till ett gemensamt Adobe-kodat format. Dessa mappningar används för att identifiera överlappningar mellan medarbetare. När målgrupper aktiveras med **[!UICONTROL AdFixus ID]** används de ursprungliga ID:na. Det Adobe-kodade formatet lämnar aldrig Collaboration.

När du väljer **[!UICONTROL AdFixus ID]** måste du ange motsvarande ID från din externa partner i avsnittet **[!UICONTROL Account credentials]**. Det här alternativet är endast tillgängligt *efter att* har aktiverats på **[!UICONTROL AdFixus ID]**. Ange ditt AdFixus-ID i fältet **[!UICONTROL Account ID]** och kontrollera att värdet är korrekt.

![Dialogrutan Matcha nycklar med AdFixus-ID aktiverat och avsnittet med kontoinloggningsuppgifter markerat.](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

När du har valt alla matchningsnycklar väljer du **[!UICONTROL Complete]** för att slutföra kontokonfigurationsarbetsflödet.

![Arbetsytan Konfigurera konto med avsnittet Matcha nycklar visas.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Redigera konto {#edit-account}

När du har konfigurerat ditt konto kan du när som helst redigera informationen och matcha nycklarna.

### Redigera information {#edit-details}

Du kan redigera de flesta detaljer för ditt konto när som helst, med undantag för **[!UICONTROL Role]**. Regionen ställs in automatiskt baserat på ditt Adobe Experience Cloud-konto och kan inte ändras.

Om du vill redigera ditt konto väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL My account]** på arbetsytan i **[!UICONTROL Setup]**.

![Arbetsytan Konfigurera med fliken Mitt konto och alternativet Redigera markerat.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Nu kan du redigera din kontoinformation. Uppdatera de fält som du vill ändra och markera sedan **[!UICONTROL Save]** för att bekräfta ändringarna.

![Dialogrutan Redigera kontoinformation.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### Redigera matchningsnycklar {#edit-match-keys}

>[!IMPORTANT]
>
>Om du redigerar matchningsnycklar påverkas inte dina befintliga anslutningar. När en anslutning har upprättats är de matchningsnycklar som du väljer under anslutningsinställningarna fasta. Det är viktigt att du väljer **alla** matchningsnycklar som du tänker använda i framtida kampanjer under kontokonfigurationen.

Du kan också uppdatera de matchningsnycklar som du valde från början när du skapade ditt konto. Dessa matchningsnycklar avgör vilka matchningsnycklar som är tillgängliga för framtida anslutningar.

Välj **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Match keys]**.

![Arbetsytan Konfigurera med alternativet Redigera markerat i avsnittet Matcha nycklar för kontot.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Match keys]** visas. Aktivera och inaktivera matchningsnycklar eller uppdatera **[!UICONTROL Account ID]** för [!UICONTROL AdFixus ID's] och välj sedan **[!UICONTROL Save]** för att bekräfta ändringarna.

>[!IMPORTANT]
>
>Om du ändrar [!UICONTROL AdFixus ID] utlöses ingen [dataskiss](../glossary.md#sketches)-uppdatering för dina befintliga dataanslutningar med matchningsnyckeln. När dina data har skisserats återspeglas inte eventuella ändringar i [!UICONTROL AdFixus ID] förrän nästa målgrupp uppdateras enligt inställningarna för [dataanslutningsschemat](./manage-data-connection.md#scheduling). Om du behöver göra ändringar innan du uppdaterar nästa gång kan du ta bort och återskapa din dataanslutning.

![Dialogrutan Matcha nycklar med alternativet Spara markerat.](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

## Nästa steg

När du har konfigurerat dina konton är du redo att [hämta målgrupper](/help/guide/setup/onboard-audiences.md) till Real-Time CDP Collaboration.
