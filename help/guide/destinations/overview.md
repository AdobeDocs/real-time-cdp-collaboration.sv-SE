---
title: Översikt över dekorationer
description: Läs mer om destinationer i Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
source-git-commit: 4ef7f8c7c27935f0e5b3620da63e7129f2714b37
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# Översikt över destinationer

{{limited-availability-release-note}}

Destinationer är integrationer som används för att skicka målgrupper till externa plattformar. Dessa integreringar gör att ni kan aktivera målgrupper över olika marknadsföringskanaler och plattformar för användning i kampanjer och kundengagemang.

Medarbetare kan konfigurera destinationer för att skicka målgrupper till externa plattformar, som Adobe Experience Platform, för användning i kampanjer. Medarbetare kan sedan [aktivera målgrupper inom ett projekt](../collaborate/activate.md), som skickas till anslutningens konfigurerade mål. Aktivering kan utföras av någon av medarbetarna beroende på målgruppens aktiveringsinställningar [som har konfigurerats i anslutningen](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>När medarbetare aktiverar målgrupper i ett projekt skickas de för närvarande automatiskt till anslutningens konfigurerade mål. Du **måste** konfigurera ett mål innan medarbetaren kan aktivera målgrupper i ett projekt.

## Konfigurera mål {#configure-destinations}

Om du vill konfigurera ett mål går du till **[!UICONTROL Setup]** och väljer fliken **[!UICONTROL My destinations]**. Här kan du visa alla tillgängliga destinationer.

>[!NOTE]
>
> För närvarande är endast Adobe Experience Platform tillgängligt som självbetjäningsmål inom Collaboration. Om du är intresserad av att konfigurera ett mål som Amazon S3 eller Snowflake kontaktar du Adobe.

![Fliken Mina mål på arbetsytan Konfigurera visar tillgängliga mål.](/help/assets/destinations/overview/my-destinations-overview.png)

Om du vill börja konfigurera ett mål väljer du alternativet **[!UICONTROL Set up]** i det mål du väljer. Mer information om hur du konfigurerar specifika mål finns i guiderna i tabellen [tillgängliga mål](#available-destinations).

![Arbetsytan Mina mål med alternativet Konfigurera markerat för Adobe Experience Platform-destinationen.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Tillgängliga destinationer {#available-destinations}

Följande mål kan konfigureras i Collaboration. Om du vill visa konfigurationsguiden för det målet väljer du målnamnet i tabellen nedan. Om du är intresserad av att konfigurera ett mål som för närvarande inte är tillgängligt kontaktar du Adobe.

| Mål | Tillgänglighet |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Tillgänglig |
| Amazon S3 | Kommer snart. |
| Snowflake | Kommer snart. |
| Google Cloud-lagring | Kommer snart. |
| Azure Blob Storage | Kommer snart. |

## Nästa steg

När du har konfigurerat ditt mål kan du börja [aktivera målgrupper](../collaborate/activate.md) i dina projekt.
