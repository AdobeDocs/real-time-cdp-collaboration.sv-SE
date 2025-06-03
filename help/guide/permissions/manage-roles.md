---
title: Hantera roller via behörigheter
description: Förstå alla tillgängliga rollresurser som ger åtkomst till olika komponenter i Real-Time CDP Collaboration användargränssnitt.
audience: admin
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/se/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Hantera roller {#manage-roles}

{{limited-availability-release-note}}

En [administratör](./manage-user-access.md#system-admin-gain-access) kan definiera och tilldela roller för att hantera användaråtkomst för olika komponenter i Real-Time CDP Collaboration-gränssnittet. Roller definierar åtkomsten som en administratör eller användare har till [resurser](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/home#permissions){target="_blank"} i din organisation. Den här guiden innehåller information om standardrollerna i Real-Time CDP Collaboration samt de individuella behörigheter du kan tilldela anpassade roller.

Administratören måste ha tillgång till Experience Platform-produkten för att kunna börja hantera roller. Mer information om hur du får administrativ åtkomst eller om hur du får åtkomst till Experience Platform finns i handboken [Hantera användaråtkomst](./manage-user-access.md#manage-user-access-through-permissions).

## Standardroller {#standard-roles}

Du har två standardroller som fyller i två vanliga fall av åtkomstkontroll. Det här är skrivskyddade roller, vilket innebär att de inte kan anpassas.

| Rollnamn | Rollbeskrivning | Behörigheter |
| --- | --- | --- | 
| Collaboration Managers | Det här är en åtkomstbehörighet som innehåller alla 15 behörigheter. Detta gör att användaren kan läsa, skapa och redigera alla data. Den ger även åtkomst till sandlådan **[!UICONTROL Prod]** i Experience Platform, så att du kan importera målgrupper till Real-Time CDP Collaboration. | Allt från tabellen nedan. |
| Collaboration Viewers | Detta är en skrivskyddad åtkomstbehörighet. En användare kan läsa och upptäcka data, aktiviteter, anslutningar och annat. Den ger även åtkomst till sandlådan **[!UICONTROL Prod]** i Experience Platform, så att du kan importera målgrupper till Real-Time CDP Collaboration. | Alla läsbehörigheter från tabellen nedan. |

{style="table-layout:auto"}

## Skapa specifika åtkomstroller {#specific-access-roles}

Du kommer troligen att vilja skapa ytterligare roller som ger olika åtkomstnivåer för olika användare. När du skapar roller kan du hantera olika åtkomstnivåer genom att välja specifika behörigheter i resursen **[!UICONTROL Collaborations]**. Mer information om hur du skapar och hanterar roller finns i guiden [roller](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"}.

>[!NOTE]
> För att få åtkomst till Real-Time CDP Collaboration måste en användare ha åtkomst till sandlådan **[!UICONTROL Prod]** i Experience Platform. Om du vill ge en användare åtkomst till den här sandlådan måste de tilldelas en roll som innehåller behörigheten **[!UICONTROL Prod]** i resursen **[!UICONTROL Sandboxes]**.

Nedan visas en lista över tillgängliga behörigheter i samarbetsresursen:

| Hög behörighet | Beskrivning |
| --- | --- |
| Hantera Collaboration-instanser | Visa, skapa, uppdatera och ta bort en organisations samarbetsinstanser. Upptäck hur andra organisationer samarbetar. |
| Läs Collaboration-instanser | Läs en organisations samarbetsinstanser och se andra organisationers samarbetsinstanser. |
| Hantera anslutningsinbjudningar | Visa, skapa och ta bort anslutningsinbjudningar som initierats av din organisation. Acceptera och avböj inbjudan om anslutning som initierats av andra organisationer. |
| Läs anslutningsinbjudningar | Visa anslutningsinbjudningar. |
| Hantera Collaboration-anslutningar | En annonsör kan visa, skapa och uppdatera inställningar samt skicka och ta bort anslutningar. En utgivare kan visa, acceptera eller neka anslutningar. |
| Läs Collaboration Connections | Visa anslutningar. |
| Hantera målgruppsdata | Anlita och identifiera målgrupper. Uppdatera publika, privata och anpassade målgrupper och hantera metadatainställningar för Audience Inventory. |
| Läs målgruppsdata | Läs och identifiera målgrupper. |
| Hantera mätningsdata | Lägg in, uppdatera och ta bort mätdata. |
| Läs mätningsdata | Läs mätdata. |
| Hantera projekt | Visa, skapa, uppdatera och ta bort projekt för någon av aktiviteterna för upptäckt, delning, aktivering och mätning. |
| Läs projekt | Visa projekt för någon av aktiviteterna för upptäckt, delning, aktivering och mätning. |
| Läs användaraktiviteter | Läs användaraktiviteter. |
| Exportera användaraktiviteter | Exportera användaraktiviteter. |
| Läs Collaboration kreditövervakning | Kreditövervakning på organisations- och instansnivå. |

{style="table-layout:auto"}

## Nästa steg

När du har skapat roller som definierar åtkomst till Real-Time CDP Collaborations måste du [tilldela rollerna](./manage-user-access.md#assign-a-role) till administratörer och användare. I guiden [Hantera behörigheter för en roll](https://experienceleague.adobe.com/sv/docs/experience-platform/access-control/abac/permissions-ui/permissions) finns en fullständig översikt över hur du hanterar roller.
