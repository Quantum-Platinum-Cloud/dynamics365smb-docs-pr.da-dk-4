---
title: Forbinde dataene med Flow | Microsoft Docs
description: "Du kan gøre dine Financials-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/21/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5d7fa359ee99cd177a445e025ddf8d156c6e2421
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow
Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. Gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/) i din webbrowser, og log på.
2. Vælg **Mine Flows** på båndet øverst på siden.
3. Der er to måder at oprette et flow på: **Opret fra skabelon** og **Opret fra tom**. En skabelon er et foruddefineret flow, der er oprettet for dig.  Hvis du vil bruge skabelonen, skal du blot vælge den og oprette en forbindelse for hver tjeneste, skabelonen bruger. Med en tom skabelon kan du oprette et nyt flow helt forfra. 
4. Hvis du vil oprette fra tom, skal du i vinduet **Mine Flows** vælge indstillingen **Opret fra tom**.
5. Søg efter **Konnektor til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. På listen over tilgængelige udløsere, skal du vælge en af de [!INCLUDE[d365fin](includes/d365fin_md.md)]-udløsere, der er tilgængelige:  
    *Når der anmodes om godkendelse af en debitor*,  
    *Når der anmodes om godkendelse af en finanskladdekørsel*,  
    *Når der anmodes om godkendelse af en finanskladdelinje*,  
    *Når der anmodes om godkendelse af en vare*,  
    *Når der anmodes om godkendelse af et købsdokument*,  
    *Når der anmodes om godkendelse af et salgsdokument* eller  
    *Når der anmodes om godkendelse af en kreditor*.
7. Du bliver bedt om at vælge en virksomhed i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-lejer samt de betingelser i dine data, du vil overvåge. 

Nu har du oprettet forbindelse til dine Business Central-data og er klar til at opbygge dit flow. 

8. Hvis du vil oprette fra en skabelon, skal du vælge indstillingen **Opret fra skabelon**.
9. Søg efter **Skabeloner til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**. 
10. På listen over tilgængelige skabeloner, skal du vælge en af skabelonerne.  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgsordre*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgstilbud*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgsfaktura*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgskreditnota*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-debitor*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-købsordre*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-købsfaktura*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-købskreditnota*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-vare*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-kreditor*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdekørsel*  
    *Anmode om godkendelse af Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdelinjer*.  
11. Flow beder dig om at vælge et firma i din [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-lejer. Da hvert trin i Flow er uafhængigt af det næste, kan du blive nødt til at definere virksomheden flere gange, når du bruger en [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-skabelon.
12. Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-skabelonen integreres med det centrale workflowprogram i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Det betyder, at hver gang du bruger en af skabelonerne til at oprette et flow, oprettes et tilsvarende workflow i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Se workflowdokumentationen til Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

Du kan finde flere oplysninger i [Flow-dokumentationen](https://docs.microsoft.com/en-us/flow/getting-started).

For fejlfinding af Microsoft Flow skal du se [Fejlfinding af integration med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se også
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)   
[Administrere [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-workflows](across-use-workflows.md)  
[Brugeropsætning af godkendelser](across-how-to-set-up-approval-users.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
