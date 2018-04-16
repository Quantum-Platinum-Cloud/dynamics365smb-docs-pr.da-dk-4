---
title: "Definition af statisk allokeringer baseret på fordelingsforholdet | Microsoft Docs"
description: "Metoden statisk allokering er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b4d26e3cb8a1364745dd25ca5341635c49a5718
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Scenarieeksempel: Definition af statisk allokeringer baseret på fordelingsforholdet
Metoden statisk allokering er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.  

Dette emne beskriver, hvordan du definerer tre nye fordelingsmålsomkostningsobjekter til fordelingskilden PROD-omkostningssted ved hjælp af det etablerede fordelingsforhold 5:2:4. De tre målomkostningsobjekter er ACCESSO, PAINT og FITTINGS.  

> [!NOTE]  
>  I eksemplet bruges demonstrationsdataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Sådan defineres fordelingskilden PROD-omkostningssted på oversigtspanelet Generelt  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Omkostningsfordeling**, og vælg derefter det relaterede link.  
2.  I vinduet **Omkostningsfordeling** skal du vælge handlingen **Ny**.  
3.  I feltet **Id** skal du trykke på Enter eller indtaste et id.  
4.  Angiv **1** i feltet **Niveau**.  
5.  I felterne **Gyldig fra** og **Gyldig til** skal du angive relevante datoer.  
6.  I feltet **Omkostningsstedskode** skal du angive **PROD**.  
7.  Angiv omkostningstypen **9903** i feltet **Kredit til omkostningstype**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Sådan angives fordelingsmålsomkostningsobjekter på oversigtspanelet Linjer  

1.  Angiv **9903** i feltet **Målomkostningstype** på den første linje.  
2.  Vælg **TILBEHØR** i feltet **Målomkostningstype** på den første linje.  
3.  På den første linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
4.  På den første linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
5.  På den første linje i feltet **Fordeling** skal du angive fordelingsforholdet **5**.  
6.  Angiv **9903** i feltet **Målomkostningstype** på den anden linje.  
7.  Vælg **MALING** i feltet **Målomkostningsemne** på den anden linje.  
8.  På den anden linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
9. På den anden linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
10. På den anden linje i feltet **Fordeling** skal du angive fordelingsforholdet **2**.  
11. Angiv **9903** i feltet **Målomkostningstype** på den tredje linje.  
12. Vælg **BESLAG** i feltet **Målomkostningsemne** på den første linje.  
13. På den tredje linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
14. På den tredje linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
15. På den tredje linje i feltet **Fordeling** skal du angive fordelingsforholdet **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk feltet **Procent** ved hjælp af en procentsats , der er afhængig af alle tre fordelingsforhold, der er angivet i feltet **Fordeling** for alle tre linjer.  

## <a name="see-also"></a>Se også  
[Konfigurere fordelingskilde og mål](finance-how-to-set-up-allocation-source-and-targets.md)   
[Definere og allokere omkostninger](finance-define-and-allocate-costs.md)   
[Scenarieeksempel: Definition af dynamiske fordelinger baseret på solgte varer](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
[Definere og allokere omkostninger](finance-define-and-allocate-costs.md)
