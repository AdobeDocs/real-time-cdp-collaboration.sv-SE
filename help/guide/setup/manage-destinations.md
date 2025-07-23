---
title: Konfigurera och hantera mål
description: Lär dig hur du konfigurerar och hanterar mål i Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Konfigurera och hantera mål

{{limited-availability-release-note}}

Destinationer är integrationer som används för att skicka målgrupper till externa plattformar. Dessa integreringar gör att ni kan aktivera målgrupper över olika marknadsföringskanaler och plattformar för användning i kampanjer och kundengagemang.

För närvarande är mål endast tillgängliga för utgivare i Real-Time CDP Collaboration. Utgivare kan konfigurera destinationer för att aktivera målgrupper för externa plattformar, som Adobe Experience Platform, för användning i kampanjer. Annonsörer kan sedan [skicka målgrupper inom ett projekt](../collaborate/activate.md), som skickas till utgivarens konfigurerade mål.

![Fliken Mina mål på arbetsytan Konfigurera innehåller aktiva Adobe Experience Platform-mål.](/help/assets/setup/manage-destinations/my-destinations-overview.png)

Mer information om destinationer finns i guiden [Målöversikt](../destinations/overview.md).

## Konfigurera mål {#configure-destinations}

Målen konfigureras i avsnittet **[!UICONTROL Setup]** i Collaboration. Om du vill konfigurera ett mål går du till **[!UICONTROL Setup]** och väljer fliken **[!UICONTROL My destinations]**. Här kan du visa alla tillgängliga destinationer.

>[!IMPORTANT]
>
>Användaren måste ha en roll med behörigheten **Hantera målgruppsdata** tilldelad till sig för att kunna konfigurera och hantera designer. Mer information om hur du hanterar roller finns i guiden [hantera roller](../permissions/manage-roles.md).

![Fliken Mina mål på arbetsytan Konfigurera visar tillgängliga mål.](/help/assets/setup/manage-destinations/my-destinations.png)

Konfigurationsprocessen för destinationer beror på vilket mål du konfigurerar. Se katalogen [tillgängliga destinationer](../destinations/overview.md#available-destinations) för att visa tillgängliga destinationer och deras konfigurationsguider.

>[!NOTE]
>
>För närvarande är endast Adobe Experience Platform tillgängligt som självbetjäningsmål inom Real-Time CDP Collaboration. Om du är intresserad av att konfigurera ett annat mål kontaktar du Adobe.

## Ta bort mål {#delete-destinations}

Om du tar bort ett mål tas det bort från organisationen, tidigare skickade målgrupper tas bort från målgruppen och framtida målgrupper inte kan skickas till det målet.

Om du vill ta bort ett mål går du till fliken **[!UICONTROL My destinations]** i avsnittet **[!UICONTROL Setup]**. Välj alternativet **[!UICONTROL Delete]** för målet som du vill ta bort.

![Arbetsytan Mina mål med alternativet Ta bort markerat för Adobe Experience Platform-målet.](/help/assets/setup/manage-destinations/delete-destination.png)

En bekräftelsedialogruta visas där du kan bekräfta att du vill ta bort målet. Välj **[!UICONTROL Delete]** om du vill ta bort målet.

![Dialogrutan Ta bort mål med alternativet Ta bort markerat.](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## Nästa steg

När du har konfigurerat ditt mål kan du börja samarbeta med dina annonsörer för att [aktivera målgrupper](../collaborate/activate.md) i dina projekt.
