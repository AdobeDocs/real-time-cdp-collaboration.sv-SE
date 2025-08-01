---
title: Hantera användaråtkomst via behörigheter
description: Hantera behörigheter och ge användare åtkomst till olika komponenter i Real-Time CDP Collaboration användargränssnitt.
audience: admin
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0155f6a6-5e67-4415-af96-1848345842e4
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Hantera användaråtkomst via behörigheter {#manage-user-access}

{{limited-availability-release-note}}

Hantera behörigheter och användaråtkomst för enskilda komponenter i Adobe Real-Time CDP Collaboration via Experience Cloud [Permissions](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/abac/permissions-ui/browse){target="_blank"} -gränssnitt. Med behörigheter kan system- och produktadministratörer definiera [roller](./manage-roles.md) för att hantera användaråtkomst till specifika funktioner och resurser.

## Konfigurera åtkomst till behörigheter {#permissions-access}

För att få åtkomst till behörigheter måste du ha både produktadministratör och användaråtkomst till Adobe Experience Platform-produkten. En systemadministratör krävs för att konfigurera produktadministratörsbehörighet, medan användarbehörigheter kan konfigureras av en system- eller produktadministratör. Mer information om de administrativa rollerna finns i guiden [Åtkomstkontrollierhet](./overview.md#hierarchy).

>[!TIP]
>
>I den här guiden hänvisar en **administratör** till **både system- och produktadministratörer**.

### Systemadministratörer: konfigurera produktadministratörsåtkomst {#admin-access}

Ge en användare produktadministratör behörighet att ge dem administratörsfunktioner i Experience Platform-produkten genom följande steg:

>[!IMPORTANT]
>
>Som systemadministratör har du direkt tillgång till vissa Experience Cloud-produkter, som Adobe Admin Console. Om du vill använda behörigheter måste du ge dig själv produktadministratör och användare tillgång till Experience Platform-produkten. Följ de stegvisa instruktionerna nedan för att ge dig själv åtkomst som systemadministratör.

Logga in på [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} med dina autentiseringsuppgifter. Hemvyn visas med en lista över dina tillgängliga produkter i avsnittet **[!UICONTROL Quick access]**. Välj **[!UICONTROL Admin Console]**.

![Experience Cloud hemvy med Admin Console markerat.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Kontrollpanelen för översikten [Adobe Admin Console](https://adminconsole.adobe.com/) visas. Välj **[!UICONTROL Adobe Experience Platform]** i listan **[!UICONTROL Products]** under **[!UICONTROL Products and services]**.

![Admin Console översiktspanel med Adobe Experience Platform-produkten markerad.](../../assets/permissions/admin-console.png){zoomable="yes"}

Adobe Experience Platform kontrollpanel visas. Markera fliken **[!UICONTROL Admins]** och välj sedan **[!UICONTROL Add admin]**.

![Adobe Experience Platform produktkontrollpanel med fliken Administratörer markerad och Lägg till administratör markerad.](../../assets/permissions/add-admin.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Add product administrators]** visas. Ange användarens e-postadress eller användarnamn i textfältet **[!UICONTROL Email or username]** och välj sedan rätt konto i listrutan. Välj **[!UICONTROL Save]** om du vill lägga till användaren som produktadministratör.

![Dialogrutan Lägg till produktadministratörer med användarinformation ifylld och alternativet Spara markerat.](../../assets/permissions/add-product-administrators.png){zoomable="yes"}

Användaren har nu administratörsbehörighet för produkten och kan utföra administrativa funktioner, som att lägga till användare eller andra administratörer, för produkten i Admin Console. Därefter behöver de åtkomst till Experience Platform-produkten för att få tillgång till och utföra funktioner i behörigheterna.

### Administratörer: konfigurera användaråtkomst till Experience Platform {#user-access}

Nu när du har gett användaren produktadministratörsbehörighet måste du ge användaren åtkomst till Experience Platform-produkten. Som en del av åtkomstkonfigurationerna tilldelar du de användarspecifika [produktprofilerna](https://helpx.adobe.com/se/enterprise/using/manage-product-profiles.html).

>[!TIP]
>
>Om du följer med i det föregående avsnittet finns du redan i Adobe Experience Platform-produkten och du kan hoppa över det första steget.

Navigera till [Admin Console](https://adminconsole.adobe.com/){target="_blank"} och välj **[!UICONTROL Adobe Experience Platform]** i listan **[!UICONTROL Products]** under **[!UICONTROL Products and services]**.

![Experience Cloud hemvy med Admin Console markerat.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Markera fliken **[!UICONTROL Users]** och välj sedan **[!UICONTROL Add users]**.

![Adobe Experience Platform produktkontrollpanel med fliken Användare markerad och Lägg till användare markerad.](../../assets/permissions/add-users.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Add users to this product]** visas. Ange användarens namn eller e-postadress i textfältet **[!UICONTROL Name, user group or email address]** och välj sedan rätt konto i listrutan. Välj sedan alternativet **[!UICONTROL Products]** för att lägga till.

![Alternativet Lägg till användare i den här produktdialogrutan med användarinformation ifylld och alternativet Lägg till produkter markerat.](../../assets/permissions/add-users-to-product.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Select product profiles]** visas. Markera **[!UICONTROL AEP-Default-All-Users]** och **[!UICONTROL Default Production All Access]** och välj sedan **[!UICONTROL Apply]**.

![Dialogrutan Välj produktprofiler med alternativen AEP-Default-All-Users och Default Production All Access markerade och Använd markerade.](../../assets/permissions/select-product-profiles.png){zoomable="yes"}

Kontrollera att informationen är korrekt och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Lägg till användare i produkter med användarinformation och produktprofiler markerade och Spara markerade.](../../assets/permissions/save-selections.png){zoomable="yes"}

Användaren bör nu ha produktadministratörs- och produktåtkomst till Experience Platform och få åtkomst till behörigheterna. Därefter måste du tilldela användaren två grundläggande roller för att ge dem åtkomst till användargränssnittet i Experience Platform.

### Administratörer: konfigurera åtkomst till Experience Platform UI {#product-access}

I Real-Time CDP Collaboration arbetar administratörer och slutanvändare med data från Experience Platform, till exempel målgrupper och granskningsloggar. Dessa data lagras i instanser av Experience Platform som kallas sandlådor. För att användare ska kunna interagera med dessa data måste du tilldela användaren [standardroller](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/home#default-roles){target="_blank"}.

Börja med att navigera till [Adobe Experience Cloud](https://experience.adobe.com/). Du bör nu se **[!UICONTROL Experience Platform]** och **[!UICONTROL Permissions]** inuti **[!UICONTROL Quick access]**.

![Experience Cloud hemvy med Experience Platform och Behörigheter markerade.](../../assets/permissions/experience-cloud-products.png){zoomable="yes"}

>[!NOTE]
>
> Produkterna kan ta flera minuter att få åtkomst till och du får ett e-postmeddelande som informerar dig om att du har fått åtkomst. Om du inte ser Experience Platform eller behörigheter i Adobe Experience Cloud när du har fått e-postmeddelandet loggar du ut och sedan in igen på ditt konto.

I det här skedet kan du nu komma åt **[!UICONTROL Permissions]**. Om du försöker få åtkomst till **[!UICONTROL Experience Platform]** får du en varning om att inga sandlådor är aktiverade, vilket visas nedan. För att lösa detta måste du tilldela standardrollerna till användaren. Börja genom att välja **[!UICONTROL Permissions]**.

![Experience Cloud hemvy med en varning och behörigheten markerade.](../../assets/permissions/experience-cloud-warning.png){zoomable="yes"}

Kontrollpanelen **[!UICONTROL Permissions]** visas. Välj **Användare** i den vänstra panelen och välj sedan användarens namn.

![Kontrollpanelen Behörigheter visas med arbetsytan Användare markerad.](../../assets/permissions/permissions-user.png){zoomable="yes"}

Markera fliken **[!UICONTROL Roles]** och välj sedan **[!UICONTROL Add roles]**.

![Användararbetsytan med fliken Roller och Lägg till roller markerade.](../../assets/permissions/user-roles.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Add Roles]** visas. Markera **[!UICONTROL Default Production All Access]** och **[!UICONTROL Sandbox Administrators]** och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Lägg till roller med standardfunktionerna för produktion, åtkomst och sandlådeadministratörer markerade och Spara markerad.](../../assets/permissions/add-roles.png){zoomable="yes"}

Nu har du tillgång till Experience Platform och behörigheter. I det sista steget ger du åtkomst till Real-Time CDP Collaboration.

### Administratörer: konfigurera Real-Time CDP Collaboration-åtkomst {#RTCDP-collaboration-access}

Om du vill ge användare åtkomst till Collaboration använder du ett åtkomstkontrollskoncept som kallas roller. Roller definierar åtkomstnivån som en administratör eller användare har till [resurser](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/home#permissions) i din organisation.

När du konfigurerar individuell åtkomst till Collaboration tilldelar du användarroller som innehåller behörigheter från samarbetsresursen. Du kan använda guiden [hantera roller](./manage-roles.md) för att ta reda på mer om:

- de [två standardrollerna](./manage-roles.md#standard-roles) och de åtkomstnivåer de ger till Collaboration
- skapar [anpassade roller](./manage-roles.md#specific-access-roles) med Collaboration-resursen
- listan över behörigheter som ingår i samarbetsresursen

>[!NOTE]
>
>Dessutom måste en användare tilldelas en roll som innehåller behörigheten **[!UICONTROL Prod]** i resurserna **[!UICONTROL Sandboxes]**. Båda standardrollerna innehåller den här behörigheten. Om du väljer att tilldela en användare en anpassad roll i stället för en standardroll, måste du se till att en av rollerna de är tilldelade till innehåller den här behörigheten.

När du har valt eller skapat en roll som omfattar den åtkomstnivå som användaren behöver måste du tilldela användaren till den rollen.

#### Tilldela en roll

Du kan tilldela flera roller till en enskild användare eller tilldela flera användare till en enda roll. Det första fallet behandlades tidigare när [standardrollerna](#product-access) tilldelades för att ge en användare åtkomst till Experience Platform. I nästa steg ska du tilldela användare direkt till den valda rollen.

I **[!UICONTROL Permissions]** väljer du **[!UICONTROL Roles]** i den vänstra panelen och väljer sedan din roll i listan.

![Kontrollpanelen Behörigheter där arbetsytan Roller visas och en roll är markerad.](../../assets/permissions/select-role.png){zoomable="yes"}

Rollens detaljsida visas. Markera fliken **[!UICONTROL Users]** och välj sedan **[!UICONTROL Add Users]**.

![Rollens detaljarbetsyta med fliken Användare och Lägg till användare markerat.](../../assets/permissions/role-users.png){zoomable="yes"}

Dialogrutan **[!UICONTROL Add Users]** visas. Välj användare i listan och välj sedan **[!UICONTROL Save]**.

![Dialogrutan Lägg till användare med en användare markerad och alternativet Spara markerat.](../../assets/permissions/add-users-to-role.png){zoomable="yes"}

Användaren ska nu se **[!UICONTROL RTCDP Collaboration]** som en produkt under **[!UICONTROL Quick Access]** i Experience Cloud.

![Experience Cloud med RTCDP Collaboration-produkt markerad under Snabbåtkomst](../../assets/permissions/rtcdp-experience-cloud.png)

## Nästa steg

Nu när användarna har tillgång till Real-Time CDP Collaboration kan de börja använda produkten. Läs [översiktsguiden](../home.md) om du vill veta mer om produkten som helhet.
