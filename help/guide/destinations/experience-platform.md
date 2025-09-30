---
title: Konfigurera Adobe Experience Platform som mål
description: Lär dig hur du konfigurerar och hanterar Adobe Experience Platform som mål i Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# Konfigurera Adobe Experience Platform som mål

{{limited-availability-release-note}}

Konfigurera den här destinationen för att aktivera målgrupper från ditt projekt till Adobe Experience Platform. Genom att aktivera målgrupper för Adobe Experience Platform kan ni utnyttja plattformens funktioner för målgruppssegmentering, analys och aktivering i olika marknadsföringskanaler. Mer information om Adobe Experience Platform finns i [Experience Platform-översikten](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"}.

>[!WARNING]
>
>Du kan inte uppdatera ett mål efter att det har skapats. Om du behöver ändra några inställningar måste du ta bort det befintliga målet och skapa ett nytt.

## Konfigurera mål {#configure-destination}

Om du vill konfigurera Adobe Experience Platform som mål går du till **[!UICONTROL Setup]** och väljer fliken **[!UICONTROL My destinations]**. Välj **[!UICONTROL Set up]** för Adobe Experience Platform.

![Arbetsytan Mina mål med alternativet Konfigurera markerat för Adobe Experience Platform-målet.](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

Arbetsflödet **[!UICONTROL Create destination]** visas.

![Arbetsflödet Skapa mål för Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### Konfigurera sandlåda {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Förfallotid för publik"
>abstract="Den tidsperiod efter vilken målgruppen inte längre är tillgänglig i Adobe Experience Platform. Standardvärdet är 30 dagar, men du kan ange ett värde mellan 1 och 30 dagar."

Först måste du markera sandlådan där målgruppsdata ska skickas.

>[!IMPORTANT]
>
>Du kan bara välja en sandlåda som användaren har åtkomst till. Som standard har alla Collaboration-användare åtkomst till sandlådan **Prod**. För att få åtkomst till ytterligare sandlådor måste en administratör lägga till ytterligare sandlådor i en roll som tilldelats användaren. Mer information om hur du hanterar roller finns i guiden [hantera roller](../permissions/manage-roles.md).

I avsnittet **[!UICONTROL Configure sandbox]** väljer du listrutan **[!UICONTROL Sandbox]** eller skriver namnet på en sandlåda.

![Listrutan Sandbox är markerad i arbetsflödet Skapa mål.](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

Du kan också välja **[!UICONTROL Browse sandbox]** om du vill visa alla tillgängliga sandlådor samt deras **[!UICONTROL Type]**, **[!UICONTROL Status]** och **[!UICONTROL Region]**. Markera den sandlåda som du vill använda och välj sedan **[!UICONTROL Save]**.

Konfigurera sedan **[!UICONTROL Audience Expiration]**. Som standard är målgruppens förfallodatum 30 dagar. Du kan välja att ange förfallodatum var som helst mellan 1 och 30 dagar. Efter utgångsdatumet är målgruppen inte längre tillgänglig i Adobe Experience Platform.

![Avsnittet Förfallotid för publik är markerat i arbetsflödet Skapa mål.](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

### Skapa aktiveringsmappning {#create-activation-mapping}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="Aktiveringsmatchningsnycklar"
>abstract="Aktiveringsmatchningsnycklar visas baserat på de matchningsnycklar du valde när du skapade din organisation."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_mapping"
>title="Läs mer"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Målnamnutrymmen"
>abstract="Målnamnutrymmen anger vilket identitetsnamnutrymme som matchningsnyckeln ska mappas till i Adobe Experience Platform. Hash-kodade matchningsnycklar måste mappas till ett målnamnutrymme som stöder hash-värden."

Alla matchningsnycklar som är aktiverade för ditt konto inkluderas som standard i aktiveringsmappningen. Om du inte vill mappa en matchningsnyckel direkt till ett målnamnutrymme kan du använda alternativet för länkad nyckel för att ersätta den med en annan matchningsnyckel. Mer information om länkade nycklar finns i avsnittet [nedan](#linked-keys).

#### Mappa målnamnutrymmen {#map-target-namespaces}

Om du vill mappa varje matchningsnyckel till ett målnamnområde markerar du fältet **[!UICONTROL Target namespaces]** bredvid matchningsnyckeln. Dialogrutan **[!UICONTROL Select source field]** visas. Sök efter målnamnutrymmet i listan eller sök efter ett specifikt namnutrymme. Markera målnamnområdet som du vill använda för matchningsnyckeln och välj sedan **[!UICONTROL Select]**.

>[!IMPORTANT]
>
>Hash-kodade matchningsnycklar måste mappas till ett målnamnutrymme som stöder hash-värden. Matchningsnyckeln **[!UICONTROL Hashed email]** måste till exempel mappas till identitetsnamnområdet **[!UICONTROL Email(SHA256, lowercased)]** i Adobe Experience Platform. Du kan inte mappa matchningsnyckeln **[!UICONTROL Hashed email]** till identitetsnamnområdet **[!UICONTROL Email]** eftersom namnområdet inte stöder hash-värden.

![Dialogrutan Välj källfält med alternativet Välj markerat.](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Upprepa den här processen för varje matchningsnyckel som du vill inkludera i aktiveringsmappningen. Om du inte vill inkludera en matchningsnyckel kan du ta bort den eller använda alternativet för länkad nyckel för att ersätta den med en annan matchningsnyckel.

#### Länkade nycklar {#linked-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="Länkad nyckel"
>abstract="Med länkade nycklar kan du ange att en annan matchningsnyckel ska användas i stället för den ursprungliga matchningsnyckeln vid aktiveringen. För att en profil ska aktiveras måste den ha värden för både den ursprungliga matchningsnyckeln och den länkade matchningsnyckeln."

Med länkade nycklar kan du ange att en annan matchningsnyckel ska användas i stället för den ursprungliga matchningsnyckeln vid aktiveringen. Om du vill förstå hur länkade nycklar fungerar kan du titta på följande exempel:

En återförsäljare vill skicka de data som aktiveras till Experience Platform till sitt CRM-system. Återförsäljaren har aktiverat Hashed IP som matchningsnyckel för sitt konto för att öka matchningsfrekvensen när målgrupper aktiveras. Detaljhandelns CRM-system stöder emellertid inte Hashed IP som ett identitetsnamnutrymme, så de vill använda matchningsnyckeln för CRM ID i stället när de aktiverar målgrupper för Experience Platform. Återförsäljaren kan använda alternativet med den länkade nyckeln för att aktivera målgrupper till Experience Platform med hjälp av CRM ID i stället för Hashed IP.

>[!NOTE]
>
>För att en profil ska aktiveras måste den ha värden för både den ursprungliga matchningsnyckeln och den länkade matchningsnyckeln. Om till exempel ett Hash-kodat ID är länkat till CRM-ID måste en profil ha värden för att både Hashed ID och CRM ID ska aktiveras. Om något av värdena saknas aktiveras inte profilen.

Om du vill använda en länkad nyckel aktiverar du alternativet **[!UICONTROL Linked key]** bredvid den matchningsnyckel som du vill använda i stället. Avsnittet **[!UICONTROL Linked key]** visas och du uppmanas att skapa mappningen.

![Alternativet och avsnittet för den länkade nyckeln är markerat i arbetsflödet för att skapa mål.](/help/assets/destinations/adobe-experience-platform/linked-key.png)

Välj den **[!UICONTROL Linked key]** som du vill använda i listrutan. I exemplet ovan skulle återförsäljaren välja **[!UICONTROL CRM ID]** som länkad nyckel.

![Listrutan för länkad nyckel markerad i arbetsflödet för att skapa mål.](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

Sedan vill du ange målnamnutrymmet för den länkade nyckeln om du inte redan har gjort det. Om du redan har valt målnamnområdet för matchningsnyckeln i avsnittet **[!UICONTROL Create activation mapping]** fylls detta i automatiskt. Om du ännu inte har valt ett målnamnutrymme för den länkade nyckeln kan du göra det nu.

Markera fältet **[!UICONTROL Target namespaces]** bredvid den länkade nyckeln. Dialogrutan **[!UICONTROL Select source field]** visas. Sök efter målnamnutrymmet i listan eller sök efter ett specifikt namnutrymme. Markera målnamnområdet som du vill använda för den länkade nyckeln och välj sedan **[!UICONTROL Select]**.

![Dialogrutan Välj källfält.](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

Den länkade nyckeln är nu konfigurerad.

>[!NOTE]
>
>Du kan bara använda ett länkat nyckelmålnamnutrymme per aktiveringsmappning. Om du t.ex. länkar Hash-kodat ID till CRM-ID kommer även aktivering av alternativet för länkad nyckel för ett annat fält att länka det till CRM-ID.

När du är klar med mappningen av alla matchningsnycklar granskar du inställningarna. Avsnittet **[!UICONTROL Preview]** innehåller en sammanfattning av din konfiguration.

![Avsnittet Förhandsgranska i arbetsflödet Skapa mål.](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>För närvarande aktiveras varje matchningsnyckel för Experience Platform som en separat målgrupp. Om du till exempel har [!UICONTROL Hashed email] och [!UICONTROL Hashed phone] som matchningsnycklar skapas två separata målgrupper i Audience Portal när en målgrupp aktiveras.

När du är nöjd med konfigurationen väljer du **[!UICONTROL Create destination]**. Ett bekräftelsemeddelande visas som anger att målet har skapats.

## Använda Adobe Experience Platform som mål

När du har konfigurerat Experience Platform som mål kan du börja [aktivera målgrupper](../collaborate/activate.md) på plattformen via dina projekt. För närvarande är aktiveringsprocessen en process i ett enda steg som initierats av medarbetaren. När en annonsör till exempel aktiverar en målgrupp skickas den till utgivarens förkonfigurerade mål (Experience Platform). Utgivaren behöver inte vidta några ytterligare åtgärder för att skicka målgruppen till målet. Samma sak gäller för samarbetet mellan varumärken.

>[!IMPORTANT]
>
>Du **måste** konfigurera Experience Platform som mål *innan* din medarbetare aktiverar en målgrupp. Om målet inte är konfigurerat skickas målgruppen till dig och visas på fliken **[!UICONTROL Activate]** i ett projekt, men målgruppen aktiveras inte för Experience Platform.

När målgruppen har aktiverats är den tillgänglig i [målportalen](#audience-portal) i Experience Platform med Real-Time CDP Collaboration som ursprung.  Dessa målgrupper kan sedan användas i kampanjer och kundengagemang.

### Målgruppsportal {#audience-portal}

Nu när du har konfigurerat Adobe Experience Platform som mål kan du visa de aktiverade målgrupperna i målportalen. Audience Portal är ett centralt nav i Adobe Experience Platform som gör att ni kan visa och hantera era målgrupper. Målportalen ger nu Real-Time CDP Collaboration som ursprung när ni filtrerar era era målgrupper.

>[!IMPORTANT]
>
>Du ansvarar för att använda nödvändiga etiketter för dataanvändning på de målgrupper du aktiverar för Adobe Experience Platform. Mer information finns i guiden [Etiketter för dataanvändning](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![Målportalen med Real-Time CDP Collaboration som ursprung i filteralternativen.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Mer information om Audience Portal finns i guiden [Översikt över målportalen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
