---
title: Beräkna överlappningsantal och procentsatser
description: Förstå hur överlappningsräknare och procentsatser beräknas i olika delar av Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 23dc33af83366806f7d99161b4b713a33daeec76
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---


# Beräkna överlappningsantal och procentsatser

I Adobe Real-Time CDP Collaboration är det viktigt att förstå målgruppernas överlappning för att optimera era marknadsföringsstrategier och säkerställa ett effektivt samarbete mellan annonsörer och utgivare. I det här dokumentet förklaras hur överlappningsantal och procentsatser i olika produktområden beräknas med hjälp av exempeldata.

## Exempeldata - identitetsantal

### Antaganden för beräkningssyften

I det här exemplet kan du anta att:

* Annonsören har tre målgrupper (A1, A2, A3).
* Utgivaren har tre målgrupper (P1, P2, P3).
* Alla matchande nyckelidentiteter utesluter varandra för alla målgrupper.

>[!NOTE]
>
>I verkligheten skulle det finnas en viss överlappning mellan varje målgrupps matchande nyckelidentiteter, men för enkelhetens skull förutsätter det här exemplet att de är exklusiva i det här fallet.

### Annonsörspubliker

| Annonsörspubliker | A1 | A2 | A3 | ALLA |
|----------------------|------|------|------|------|
| Hash-kodade e-postidentiteter | 300 kB | 450 kB | 250 kB | 1 MB |
| ID-identiteter för Liveramp | 500 kB | 200 kB | 700 kB | 1,4 MB |
| Totalt antal identiteter | 800 kB | 650 kB | 950 kB | 2,4 MB |

### Utgivarens målgrupper

| Utgivarens målgrupper | P1 | P2 | P3 | ALLA |
|---------------------|------|------|------|------|
| Hash-kodade e-postidentiteter | 150 kB | 600 kB | 550 kB | 1,3 MB |
| Identiteter för Liveramp-ID | 400 kB | 350 kB | 100 000 | 850 km-lopp |
| Totalt antal identiteter | 550 km-lopp | 950 km-lopp | 800 km-lopp | 2,3 MB |

## Beräkna överlappningsräknare och procentandelar

### Exempeldata - överlappningsantal

#### Advertiser Each vs Publisher each

|                     | A1 - P1 | A2 - P2 | A3 - P3 |
|---------------------|---------|---------|---------|
| Överlappa med Hash-kodad e-post | 100 000 | 300 kB | 150 kB |
| Överlappa med liveramp-ID | 200 km-lopp | 150 kB | 50 kB |
| Total överlappning | 300 kB | 450 kB | 200 kB |

#### Advertiser Each vs Publisher ALL

|                     | A1 - P ALL | A2 - P ALL | A3 - P ALL |
|---------------------|------------|------------|------------|
| Överlappa med Hash-kodad e-post | 250 kB | 400 kB | 200 kB |
| Överlappa med överlägg av överlägg-ID | 350 kB | 150 kB | 230 kB |
| Total överlappning | 600 kB | 550 kB | 430 kB |

#### Advertiser ALL vs Publisher Each

|                     | A ALL - P1 | A ALL - P2 | A ALL - P3 |
|---------------------|------------|------------|------------|
| Överlappning av hashad e-post | 120 km-lopp | 530 km-lopp | 200 km-lopp |
| Överlappa med liveramp-ID | 350 kB | 330 kB | 50 kB |
| Total överlappning | 470 kB | 860 kB | 250 kB |

#### Advertiser ALL vs Publisher ALL

|                     | A ALL - P ALL |
|---------------------|---------------|
| Överlappa med Hash-kodad e-post | 850 kB |
| Överlappa med överlägg av överlägg-ID | 730 kB |
| Total överlappning | Cirka 1,58 miljoner |

## Upptäck modul

Modulen **[!UICONTROL Discover]** i Adobe Real-Time CDP Collaboration ger värdefulla insikter om era målgruppsdata. Genom att förstå vilka målgrupper som överlappar kan ni identifiera potentiella samarbetsmöjligheter mellan utgivare och annonsörer. Avsnittet **[!UICONTROL Audience Insights]** i modulen **[!UICONTROL Discover]** hjälper dig att analysera antalet överlappningar och procentandelar mellan olika målgrupper.

![Identifieringsmodulen för arbetsflödet.](/help/assets/reference/overlap-calculations/discover-module-overlap-calculations.png)

Visa exempelberäkningar och formler för olika överlappningsscenarier nedan.

### Alla annonsörer och alla förlag

| Annonsörspubliker | Utgivare | Identitetsantal (A) | Överlappande identiteter (B) | Överlappningsprocent | Matcha nyckeluppdelning | Fördelning av matchnyckel % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| ALLA | ALLA | Totalt antal identiteter för ALLA annonsörer <br> Identitetsantal = 1M + 1,4M = 2,4M | Total överlappning mellan ALLA annonsörer och ALLA utgivarmålgrupper för alla matchningsnycklar <br> Överlappande identiteter = 1,58 MB | Procent av överlappande identiteter över det totala antalet identiteter för alla annonsörer <br> Överlappning % = (B / A) * 100 = (1,58 MB / 2,4 MB) * 100 = 65,83 % <br> Överlappningsprocent = 65,83 % | Överlappande identiteter per matchningsnyckel <br> Överlappa med Hashed-e-post = 850K <br> Överlappa med Liveramp-ID = 730K | Procent av matchningsnyckelöverlappning över totalt antal överlappande identiteter <br> Matcha nyckel % för hashad e-post = (850 kB / 1,58 MB) * 100 = 53,8 % <br> för Liveramp ID = (730 kB / 1,58 MB) * 100 = 46,2 % |

### Alla annonsörers målgrupper och en utgivare

| Annonsörspubliker | Utgivare | Identitetsantal (A) | Överlappande identiteter (B) | Överlappningsprocent | Matcha nyckeluppdelning | Matcha nyckelfördelning % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| ALLA | 1 P2 | Totalt antal identiteter för alla annonsörer <br> Identitetsantal = 1M + 1,4M = 2,4M | Total överlappning mellan ALLA annonsörer och vald publik P2 för alla matchningsnycklar <br> Överlappande identiteter = 860 kB | Procent av överlappande identiteter över totalt antal identiteter för alla annonsörer <br> överlappar % = (B / A) * 100 = (860 kB / 2,4 MB) * 100 = 35,83 % <br> Överlappningsprocent = 35,83 % | Överlappande identiteter per matchningsnyckel <br> Överlappa med Hashed-e-post = 530K <br> Överlappa med Liveramp-ID = 330K | Procent av matchningsnyckelöverlappning över totalt antal överlappande identiteter <br> Matcha nyckel % för hashad e-post = (530 kB / 860 kB) * 100 = 61,62 % <br> för Liveramp-ID = (330 kB / 860 k) * 100 = 38 % |

### En annonsörs- och alla förläggarmålgrupper

| Annonsörspubliker | Utgivare | Identitetsantal (A) | Överlappande identiteter (B) | Överlappningsprocent | Matcha nyckeluppdelning | Matcha nyckelfördelning % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A1 | ALLA | Totalt antal identiteter för den valda målgruppen A1 <br> Identitetssiffra = 300K + 500K = 800K | Total överlappning mellan annonsörer A1 och ALLA utgivarmålgrupper för alla matchningsnycklar <br> Överlappande identiteter = 600 kB | Procent av överlappande identiteter jämfört med identitetsantal för den valda målgruppen (A1) <br> Överlappning % = (B / A) * 100 = (600 kB / 800 kB) * 100 = 75 % <br> Överlappningsprocent = 75 % | Överlappande identiteter per matchningsnyckel <br> Överlappa med Hashed-e-post = 250 kB <br> Överlappa med Liveramp-ID = 350 kB | Procent av matchningsnyckelöverlappning över totalt antal överlappande identiteter <br> Matcha nyckel % för hashad e-post = (250 kB/600 kB) * 100 = 41,67 % <br> för Liveramp-ID = (350 kB/600 kB) * 100 = 5,33 % |

### En annonsörgrupp och en utgivare

| Annonsörspubliker | Utgivare | Identitetsantal (A) | Överlappande identiteter (B) | Överlappningsprocent | Matcha nyckeluppdelning | Fördelning av matchnyckel % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A2 | 1 P2 | Totalt antal identiteter för annonsörens valda målgrupp A2 <br> Antal identiteter = 450K + 200K = 650K | Total överlappning mellan vald annonsörsmålgrupp A2 och vald utgivarmålgrupp P2 för alla matchningsnycklar <br> Överlappande identiteter = 450K | Procent av överlappande identiteter över identitetsantal för min valda målgrupp (A2) <br> Överlappning % = (B / A) * 100 = (450 kB / 650 kB) * 100 = 69,23 % <br> Överlappningsprocent = 69,23 % | Överlappande identiteter per matchningsnyckel <br> Överlappa med Hashed-e-post = 300K <br> Överlappa med Liveramp-ID = 150K | Procent av matchningsnyckelöverlappning över totalt antal överlappande identiteter <br> Matcha nyckel % för hashad e-post = (300 kB / 450 kB) * 100 = 66,67 % <br> för Liveramp-ID = (150 kB / 450 kB) * 100 = 3,3 % |
