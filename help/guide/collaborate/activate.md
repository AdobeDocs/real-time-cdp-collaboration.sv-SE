---
title: Aktivera målgrupper
description: Som utgivare kan du lära dig hur du aktiverar i kampanjer som målgrupper delas med dig av din medarbetare.
audience: admin, publisher
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# Aktivera målgrupper

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>Arbetsytan **[!UICONTROL Activate]** är bara tillgänglig om du är utgivare och **målgruppsdelning och aktivering** har aktiverats [under anslutningsprocessen](../connect/establishing-connections.md#connection-settings). Mer information om användningsfall finns i guiden [hantera projekt](./manage-projects.md#project-use-cases).

Som utgivare kan du se hur du aktiverar målgrupper med Adobe Real-Time CDP Collaboration. För närvarande kan ni aktivera målgrupper på Amazon S3-platser. Ytterligare aktiveringskanaler planeras.

Endast **utgivarorganisationer** kan aktivera målgrupper för kampanjer. Annonsörorganisationer kan [dela målgrupper](/help/guide/collaborate/share.md) med utgivare, som aktiverar dessa målgrupper i projekt. Läs mer om det [kompletta arbetsflödet](/help/guide/end-to-end-workflow.md) för annonsörer och utgivare.

## Förhandskrav {#prerequisites}

Som utgivare som använder Real-Time CDP Collaboration måste du först arbeta med Adobe aktiverings- och ingenjörsteam för att skapa en anslutning till den önskade Amazon S3-platsen. När du har konfigurerat detta kan du aktivera, eller exportera, målgrupper från Real-Time CDP Collaboration till din Amazon S3-plats. Kontakta din Adobe-representant för att få igång det här arbetsflödet.

Dessutom måste din anslutning ha **målgruppsdelning och aktivering** aktiverat.

## Aktiveringsbeteende {#activation-behavior}

När din annonsörsanslutning delar en målgrupp för aktivering visas den här målgruppen omedelbart i din **[!UICONTROL Activate]**-vy. Publiken exporteras till den angivna platsen med det intervall som anges av annonsören på deras målgruppsdelningsskärm.

![Aktivera arbetsflöde till ett Amazon S3-mål.](/help/assets/collaborate/activate/activate-to-amazon-s3.png)

## Nästa steg {#next-steps}

När du har aktiverat data och kört kampanjer kan du arbeta med Adobe aktiverings- och ingenjörsteam för att överföra mätdata och visa motsvarande [mätrapporter](/help/guide/collaborate/measure.md).
