---
title: "Sådan bogføres kapaciteter | Microsoft Docs"
description: "I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren. Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6114149372b786c20ee7edbe13022abe688ed9a2
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a>Bogføre kapaciteter
I kapacitetskladden kan du bogføre forbrugt kapacitet, der ikke er knyttet til produktionsordren. Vedligeholdelsesarbejde skal f.eks. knyttes til kapaciteten, men ikke til en produktionsordre.  

## <a name="to-post-capacities"></a>Sådan bogføres kapaciteter  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kapacitetskladder**, og vælg derefter det relaterede link.  
2.  Udfyld felterne **Bogføringsdato** og **Bilagsnr** .  
3.  Angiv den type kapacitet, du bogfører, i feltet **Type**, enten **Produktionsressource** eller **Arbejdscenter**.  
4.  I feltet **Nummer** skal du angive nummeret på produktionsressourcen eller arbejdscentret.  
5.  Angiv de relevante data i de andre felter, f.eks. **Starttidspunkt**, **Sluttidspunkt**, **Antal** og **Spild**.  
6.  Vælg handlingen **Bogfør** for at bogføre kapaciteterne.  

## <a name="to-view-work-center-ledger-entries"></a>Sådan vises arbejdscenterposter  
I vinduerne **Arbejdscenterkort** og **Prod.ress.kort** kan du få vist de bogførte kapaciteter som følge af færdige produktionsordrer.    
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Arbejdsskift**, og vælg derefter det relaterede link.  
2.  Åbn det relevante **arbejdscenter**-kort på listen, og vælg derefter handlingen **Kapacitetsposter**.  

Vinduet **Kapacitetsposter** vises med posterne i den rækkefølge, de er bogført.   

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
