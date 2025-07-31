---
title: Konfigurera Adobe Experience Platform som mål
description: Lär dig hur du konfigurerar och hanterar Adobe Experience Platform som mål i Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: 4ef7f8c7c27935f0e5b3620da63e7129f2714b37
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Konfigurera Adobe Experience Platform som mål

{{limited-availability-release-note}}

Konfigurera den här destinationen för att aktivera målgrupper från ditt projekt till Adobe Experience Platform. Genom att aktivera målgrupper för Adobe Experience Platform kan ni utnyttja plattformens funktioner för målgruppssegmentering, analys och aktivering i olika marknadsföringskanaler. Mer information om Adobe Experience Platform finns i [Experience Platform-översikten](https://experienceleague.adobe.com/sv/docs/experience-platform/landing/home){target="_blank"}.

## Konfigurera mål {#configure-destination}

Om du vill konfigurera Adobe Experience Platform som mål går du till **[!UICONTROL Setup]** och väljer fliken **[!UICONTROL Destinations]**. Välj **[!UICONTROL Set up]** för Adobe Experience Platform.

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
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Målnamnutrymmen"
>abstract="Målnamnutrymmen anger vilket identitetsnamnutrymme som matchningsnyckeln ska mappas till i Adobe Experience Platform. Hash-kodade matchningsnycklar måste mappas till ett målnamnutrymme som stöder hash-värden."

Därefter måste du skapa en aktiveringsmappning som definierar hur målgruppsdata ska skickas till Adobe Experience Platform. Du kan mappa varje [matchningsnyckel](../setup/onboard-account.md#set-up-match-keys) som du valde när du skapade din organisation till ett målnamnområde. Målnamnutrymmena anger vilket [ID-namnområde](https://experienceleague.adobe.com/sv/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} matchningsnyckeln ska mappas till i Adobe Experience Platform.

>[!IMPORTANT]
>
>Hash-kodade matchningsnycklar måste mappas till ett målnamnutrymme som stöder hash-värden. Matchningsnyckeln **[!UICONTROL Hashed email]** måste till exempel mappas till identitetsnamnområdet **[!UICONTROL Email(SHA256, lowercased)]** i Adobe Experience Platform. Du kan inte mappa matchningsnyckeln **[!UICONTROL Hashed email]** till identitetsnamnområdet **[!UICONTROL Email]** eftersom namnområdet inte stöder hash-värden.

Markera fältet **[!UICONTROL Target namespaces]** bredvid varje matchningsnyckel. Dialogrutan **[!UICONTROL Select source field]** visas. Sök efter målnamnutrymmet i listan eller sök efter ett specifikt namnutrymme. Markera målnamnområdet som du vill använda för matchningsnyckeln och välj sedan **[!UICONTROL Select]**.

![Dialogrutan Välj källfält med alternativet Välj markerat.](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

När du är klar med mappningen av alla matchningsnycklar granskar du dina inställningar och väljer sedan **[!UICONTROL Create]** för att slutföra skapandet av ditt mål.

## Använda Adobe Experience Platform som mål

När du har konfigurerat Adobe Experience Platform som mål kan du börja [aktivera målgrupper](../collaborate/activate.md) på plattformen via dina projekt. För närvarande är aktiveringsprocessen en process i ett enda steg som initieras av annonsören. När annonsören aktiverar en målgrupp skickas den till utgivarens förkonfigurerade mål (i det här fallet Adobe Experience Platform). Utgivaren behöver inte vidta några ytterligare åtgärder för att skicka målgruppen till målet.

>[!IMPORTANT]
>
>Du **måste** konfigurera Adobe Experience Platform som mål *innan* din medarbetare aktiverar en målgrupp. Om målet inte är konfigurerat skickas målgruppen till dig och visas på fliken **[!UICONTROL Activate]** i ett projekt, men målgruppen aktiveras inte för Adobe Experience Platform.

När målgruppen har aktiverats är den tillgänglig i [målportalen](#audience-portal) i Experience Platform med Real-Time CDP Collaboration som ursprung.  Dessa målgrupper kan sedan användas i kampanjer och kundengagemang.

### Målgruppsportal {#audience-portal}

Nu när du har konfigurerat Adobe Experience Platform som mål kan du visa de aktiverade målgrupperna i målportalen. Audience Portal är ett centralt nav i Adobe Experience Platform som gör att ni kan visa och hantera era målgrupper. Målportalen ger nu Real-Time CDP Collaboration som ursprung när ni filtrerar era era målgrupper.

>[!IMPORTANT]
>
>Du ansvarar för att använda nödvändiga etiketter för dataanvändning på de målgrupper du aktiverar för Adobe Experience Platform. Mer information finns i guiden [Etiketter för dataanvändning](https://experienceleague.adobe.com/sv/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![Målportalen med Real-Time CDP Collaboration som ursprung i filteralternativen.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Mer information om Audience Portal finns i guiden [Översikt över målportalen](https://experienceleague.adobe.com/sv/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
