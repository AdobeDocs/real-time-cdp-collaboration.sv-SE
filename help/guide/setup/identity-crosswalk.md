---
title: Korsningar av identiteter
description: Lär dig allt om korsningar av identiteter i Real-Time CDP Collaboration, inklusive hur du kan ta fram korsningar av identiteter från olika källor och hur du hanterar korsningar av identiteter
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hidefromtoc: true
hide: true
exl-id: a51f112d-3da7-4482-a24a-6d9f269d28d1
source-git-commit: fda414120decc0c76712616ff85b83febede53e9
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Korsningar av identiteter

{{limited-availability-release-note}}

Lär dig allt om korsningar av identiteter i Real-Time CDP Collaboration, inklusive hur du tar in korsningar av identiteter från olika källor och hur du hanterar korsningar av identiteter.

Identitetskorsningar underlättar säker och integritetskompatibel länkning av kundidentiteter mellan flera datauppsättningar och plattformar. Genom att använda hash-kodade identifierare ser Real-Time CDP Collaboration till att användare kan synkronisera och stämma av identiteter utan att exponera personligt identifierbar information (PII). Detta ger en enhetlig bild av kunden för bättre samarbete och riktade marknadsföringssatsningar.

<!--
In Real-Time CDP Collaboration, use identity crosswalks alongside your audiences by [TODO] insert material here. 
-->


Som ett första steg måste du importera identitetskorsningar till Real-Time CDP Collaboration. Läs avsnittet nedan om du vill importera identitetskorsningar till Real-Time CDP Collaboration:

>[!NOTE]
>
>I betaversionen av Real-Time CDP Collaboration kan du importera identitetskorsningar från dina datauppsättningar i Real-Time CDP. Ytterligare alternativ kommer att finnas i efterföljande versioner.

## Importera identitetskorsningar till Real-Time CDP Collaboration {#import-crosswalk}

Gå till fliken **[!UICONTROL Setup]** > **[!UICONTROL Identity crosswalks]** och välj ikonen Lägg till (![ikonen Lägg till.](/help/assets/icons/plus.png)) och välj **[!UICONTROL Identity crosswalk]**

![Inspelning av hur du kommer till skärmen för att lägga till identitetskorsning](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### Välj korsgångskälla

Välj en källa som du vill importera identitetskorsningen från. I den första utgåvan av Real-Time CDP Collaboration är Experience Platform den enda källa som stöds för import av korsningar.

>[!TIP]
>
>Korsningarna som du importerar från Experience Platform kallas *datamängder* i plattformen.

När du har valt Experience Platform som källa för dina korsningar väljer du [Experience Platform-sandlådan](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) som du importerar identitetskorsningen från.

![Inspelning av hur du väljer en övergångskälla](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### Markera korsningen

När du har valt Experience Platform som källa för dina korsningar

### Ange information

Ange ett namn och en beskrivning för den identitetskorsning som du importerar till produkten.

### Välj kopplingsnyckel {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="Kopplingstangent"
>abstract="En kopplingsnyckel är en unik identifierare som används för att matcha och länka poster mellan olika datauppsättningar. Det säkerställer att data från olika källor kan kopplas till samma person eller enhet på ett korrekt sätt. Alla kolumnrubriker från den markerade korsningen kan fungera som kopplingsnycklar."

En kopplingsnyckel är en unik identifierare som används för att matcha och länka poster mellan olika datauppsättningar. Det säkerställer att data från olika källor kan kopplas till samma person eller enhet på ett korrekt sätt. Genom att välja rätt kopplingsnyckel kan ni effektivt sammanfoga och stämma av data, vilket ökar exaktheten och fullständigheten hos era kampanjer.

Alla kolumnrubriker från den markerade korsningen kan fungera som kopplingsnycklar.

Välj önskad kopplingsnyckel för korsgångstabellen och välj **[!UICONTROL Next]** för att fortsätta till nästa steg.

### Granska

Granska något av valen i föregående skärmar. När du är nöjd med ditt val väljer du **[!UICONTROL Next]** för att slutföra arbetsflödet.

## Nästa steg

När du har lärt dig att importera identitetskorsningar till Real-Time CDP kan du visa alla identitetskorsningar som du hittills har lagt till i Real-Time CDP Collaboration. Nu kan du även använda de identitetskorsningar som du har importerat när du importerar målgrupper till Real-Time CDP Collaboration.
