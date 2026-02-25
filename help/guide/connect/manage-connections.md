---
title: Hantera anslutningar
description: Lär dig hur du hanterar dina anslutningar i Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Begränsad tillgänglighet" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
source-git-commit: 46d2596bd0ccdc5da32067493968945c61f8acc4
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 0%

---

# Hantera anslutningar {#manage-connections}

{{limited-availability-release-note}}

Arbetsytan i **[!UICONTROL My connections]** erbjuder en central plats för hantering av dina anslutningar. Du kan visa befintliga anslutningar i avsnittet **[!UICONTROL Existing connections]** och se alla anslutningar som kräver åtgärder i avsnittet **[!UICONTROL Action required]**.

## Visa anslutning {#view-connection}

Om du vill visa dina befintliga anslutningar går du till arbetsytan **[!UICONTROL Connect]**. Som utgivare visas din befintliga anslutning. Som annonsörer bör du sedan navigera till **[!UICONTROL My connections]**.

![Anslutningsalternativet Visa är markerat för en anslutning på arbetsytan Mina anslutningar.](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

Arbetsytan för anslutningsöversikt visas med information om anslutningen och dess aktiva projekt. Välj **[!UICONTROL Connection settings]** om du vill visa anslutningsinställningarna.

![Alternativet Anslutningsinställningar är markerat på arbetsytan för anslutningsöversikt.](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

Arbetsytan för anslutningsinställningar visas och visar anslutningsinformationen mellan dig och medarbetaren. Här kan du visa alla inställningar som har valts under anslutningsprocessen, aktuell status för anslutningen, anslutningsägare och kontaktinformation för medarbetaren. Mer information om särskilda anslutningsinställningar finns i handboken [Anslutningsinställningar](/help/guide/connect/establishing-connections.md#connection-settings).

![Arbetsytan för anslutningsinställningar med anslutningsinformation.](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## Ta bort anslutning {#delete-connection}

Du kan ta bort alla anslutningar med medarbetare som du inte vill fortsätta arbeta med. Om du vill ta bort en anslutning navigerar du till anslutningen som du vill ta bort och väljer sedan borttagningsikonen ![ta bort ](/help/assets/common/delete.svg) på arbetsytan för anslutningen.

![Ikonen Ta bort är markerad på arbetsytan för anslutning.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

En bekräftelsedialogruta visas där du ombeds bekräfta borttagningen av anslutningen. Markera **[!UICONTROL Delete]** för att bekräfta borttagningen.

![Bekräftelsedialogrutan för att ta bort en anslutning.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>När anslutningen har tagits bort tas alla befintliga projekt i samarbetet bort permanent och kan inte återställas. Anslutningsbegäran kommer att förbli i ett väntande läge i avsnittet **[!UICONTROL Action required]** i **[!UICONTROL My connections]**, men anslutningen och dess konfigurationer kommer inte längre att vara aktiva. Du måste återupprätta anslutningen om du vill ansluta till medarbetaren igen.

## Redigera anslutning {#edit-connection}

Som ägare av en samarbetsanslutning kan du redigera anslutningsinställningarna med medarbetaren när anslutningen har upprättats. Du kan:

* Lägg till användningsfall
* Lägg till matchningsnycklar. Det kommer att finnas stöd för borttagning av matchningsnyckel i framtiden.
* Uppdatera behörigheter för målaktivering
* Uppdatera inställningar för kreditdelning

>[!IMPORTANT]
>
>När ett användningsfall eller en matchningsnyckel har lagts till i en anslutning kan det inte tas bort.

>[!TIP]
>
>**owner** är medarbetaren som initierar anslutningen genom att skicka inbjudan till **mottagaren**. Mer information finns i [dokumentationen om att upprätta anslutningar med medarbetare](./establishing-connections.md).

Om du vill redigera anslutningsinställningarna går du till arbetsytan för anslutningsinställningar. Välj ikonen med tre punkter (![Tre punkter).](/help/assets/icons/more.png)) om du vill visa tillgängliga åtgärder väljer du **[!UICONTROL Edit]**.

![Arbetsytan för anslutningsinställningar med alternativet Redigera markerat.](/help/assets/connect/manage-connections/edit-connection.png){zoomable="yes"}

En dialogruta visas med en uppmaning om att redigera och skicka in inställningarna för granskning av medarbetare. Välj **[!UICONTROL Edit]**.

![Dialogrutan Redigera anslutningsinställningar med alternativet Redigera markerat.](/help/assets/connect/manage-connections/edit-connection-settings-dialog.png){zoomable="yes"}

### Redigera målgruppsaktivering {#edit-audience-activation}

Inställningarna för målgruppsaktivering avgör vilka medarbetare i anslutningen som kan aktivera målgrupper till mål. Om du vill ändra de här inställningarna väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Audience activation]**.

![Skärmen Redigera anslutningsinställningar visar avsnittet Målgruppsaktivering och alternativet Redigera.](/help/assets/connect/manage-connections/edit-audience-activation.png){zoomable="yes"}

Använd listrutan i dialogrutan **[!UICONTROL Audience activation]** för att uppdatera målgruppsaktiveringsbehörigheterna. Du kan välja en medarbetare eller tillåta båda medarbetarna att aktivera målgrupper.

![Dialogrutan Målgruppsaktivering visar en listruta som utökats för uppdatering av målgruppsaktiveringsbehörigheter.](/help/assets/connect/manage-connections/audience-activation-dropdown-menu.png){zoomable="yes"}

När du är klar väljer du **[!UICONTROL Save]**.

![Dialogrutan Målgruppsaktivering visar de nya målgruppsaktiveringsbehörigheterna och alternativet Spara.](/help/assets/connect/manage-connections/audience-activation-dialog.png){zoomable="yes"}

### Lägg till användningsfall {#add-use-cases}

I Collaboration avgör exempel på användningsområden som Discover, Activate och Measurement vilka projektavsnitt och funktioner du kan använda tillsammans med medarbetaren. Du kan lägga till fler användningsfall till en befintlig anslutning för framtida projekt. Mer information finns i [användningsfall för samarbete](../overview/use-cases.md).

Om du vill lägga till nya användningsfall väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Use cases]**.

![Skärmen Redigera anslutningsinställningar visar avsnittet Användningsfall och alternativet Redigera.](/help/assets/connect/manage-connections/edit-use-cases.png){zoomable="yes"}

I dialogrutan **[!UICONTROL Use cases]** aktiverar du de nya användningsfall som du vill lägga till, följt av **[!UICONTROL Save]**.

![Dialogrutan Användningsfall där alternativet Spara visas markerat.](/help/assets/connect/manage-connections/use-cases-dialog.png){zoomable="yes"}

>[!NOTE]
>
>När du [lägger till nya användningsfall](#add-use-cases), till exempel&quot;Målgruppsaktivering&quot; eller&quot;Mått&quot;, uppdateras skärmen för redigeringsinställningar så att avsnitten **[!UICONTROL Audience activation]** och **[!UICONTROL Credit split]** finns med. Du måste konfigurera lämpliga inställningar för dessa nya användningsfall. Mer information finns i handböckerna [målgruppsaktivering](../connect/establishing-connections.md#audience-activation) och [kreditdelning](../connect/establishing-connections.md#credit-split).
>
>![Skärmen Redigera anslutningsinställningar visar Målgruppsaktivering och Kreditdelning när nya användningsexempel har lagts till.](/help/assets/connect/manage-connections/setup-audience-activation-credit-split.png){zoomable="yes"}

### Lägg till matchningsnycklar {#add-match-keys}

Endast matchande nycklar som har konfigurerats på ditt konto och som även har valts av din medarbetare är tillgängliga för anslutningen. När du [lägger till nya matchningsnycklar i ditt konto](../setup/onboard-account.md#edit-match-keys) och din medarbetare också väljer samma nycklar, kan du aktivera dem i dina befintliga anslutningar.

På skärmen Redigera anslutningsinställningar väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Match keys]**.

![Skärmen Redigera anslutningsinställningar visar avsnittet Matcha nycklar och alternativet Redigera.](/help/assets/connect/manage-connections/edit-connection-match-keys.png){zoomable="yes"}

En **[!UICONTROL Match keys]**-dialogruta visas med de befintliga matchningsnycklarna som har konfigurerats för anslutningen. Välj de matchningsnycklar som du vill lägga till, följt av **[!UICONTROL Save]**.

![Dialogrutan Matcha nycklar visar de nya matchningsnycklarna och alternativet Spara.](/help/assets/connect/manage-connections/connection-match-keys-dialog.png){zoomable="yes"}

### Redigera kreditdelning {#edit-credit-split}

Inställningarna för kreditdelning anger vilken medarbetare som ansvarar för kostnaderna för varje användningsfall i anslutningen. Om du vill uppdatera de här inställningarna väljer du **[!UICONTROL Edit]** i avsnittet **[!UICONTROL Credit split]**.

![Skärmen för redigeringsinställningar visar avsnittet för kreditdelning och alternativet Redigera.](/help/assets/connect/manage-connections/edit-credit-split.png){zoomable="yes"}

I dialogrutan **[!UICONTROL Credit split]** väljer du önskade inställningar för [!UICONTROL Activation-Matching] och [!UICONTROL Measurement]. Välj sedan **[!UICONTROL Save]** för att bekräfta.

![Dialogrutan för kreditdelning visar inställningarna för kreditdelning och alternativet Spara.](/help/assets/connect/manage-connections/credit-split-dialog.png){zoomable="yes"}

### Granska och skicka ändringar {#review-and-submit-changes}

Granska och välj **[!UICONTROL Submit changes]** när du är klar med redigeringen av anslutningsinställningarna. Uppdateringar av anslutningsinställningarna skickas till din medarbetare för granskning.

![Skärmen Redigera anslutningsinställningar visar uppdateringarna och alternativet Skicka ändringar.](/help/assets/connect/manage-connections/review-and-submit-changes.png){zoomable="yes"}

#### Spara ändringar av anslutningsinställningar som utkast

Du kan spara anslutningsinställningarna som ett utkast och sedan gå tillbaka och uppdatera anslutningsinställningarna när du vill.

Om du vill spara ändringarna som ett utkast väljer du **[!UICONTROL Cancel]** bredvid **[!UICONTROL Submit changes]**. I dialogrutan **[!UICONTROL Unsubmitted changes]** väljer du sedan **[!UICONTROL Continue later]** för att bekräfta.

![Skärmen Redigera anslutningsinställningar.](/help/assets/connect/manage-connections/unsubmitted-changes-dialog.png){zoomable="yes"}

Ändringarna sparas nu som ett utkast. På arbetsytan för anslutningsinställningar visas ett meddelande om att det finns ändringar som inte har skickats. Välj **[!UICONTROL Continue editing]** om du vill göra fler uppdateringar.

![Ett meddelande på arbetsytan för anslutningsinställningar visar att det finns oskickade ändringar som väntar på granskning och överföring.](/help/assets/connect/manage-connections/continue-editing-connection.png){zoomable="yes"}
