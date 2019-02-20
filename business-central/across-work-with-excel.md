---
title: Visning og redigering i Excel fra Business Central | Microsoft Docs
description: "Få mere at vide om, hvordan du kan åbne siderne i Microsoft Excel fra Business Central for at få en bedre dataanalyse."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.contentlocale: da-dk
ms.lasthandoff: 01/22/2019

---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visning og redigering i Excel fra Business Central 

Med sider, der viser en liste over poster i rækker og kolonner, f.eks. en liste over debitorer, salgsordrer eller fakturaer, kan du også få vist posterne ved hjælp af Microsoft Excel. Du har to muligheder for at gøre dette. Du kan vælge enten handlingen **Åbn i Excel** eller handlingen **Rediger i Excel** på siden. Forskellen på de to handlinger er følgende:  

## <a name="open-in-excel"></a>Åbn i Excel

-    Med denne handling respekterer Excel eventuelle filtre på siden, som begrænser, hvilke poster der vises. Det betyder, at Excel-projektmappen indeholder de samme rækker og kolonner, der vises på den side i [!INCLUDE[prodshort](includes/prodshort.md)].

-    Du kan foretage ændringer af posterne i Excel, men du kan ikke publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan kun gemme ændringerne til en Excel-fil på computeren. 

-    Denne handling fungerer både på Windows og macOS. 

>[!NOTE]
>For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø er handlingen **Åbn i Excel** ikke tilgængelig, hvis handlingen **Rediger i Excel** er det.

## <a name="edit-in-excel"></a>Rediger i Excel

-    Med denne handling respekterer Excel-projektmappen ikke eventuelle filtre på siden, som begrænser, hvilke poster der vises. Det betyder, at Excel-projektmappen indeholder alle de tilgængelige poster og kolonner, uanset hvad der vises på siden. 

-    Fordelen ved handlingen **Rediger i Excel** er, at du kan ændre poster i Excel og derefter publicere ændringerne tilbage til [!INCLUDE[prodshort](includes/prodshort.md)].

-    Det fungerer kun i Windows, ikke i macOS.

>[!NOTE]
>For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø, er handlingen **Rediger i Excel** kun tilgængelig, hvis Excel-tilføjelsesprogrammet er installeret af administratoren. Til administratorer, hvis du vil vide, hvordan du installerer Excel-tilføjelsesprogrammet, skal du se [Konfigurere Excel-tilføjelsesprogrammet](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

## <a name="see-also"></a>Se også

[Arbejde med Business Central](ui-work-product.md)  
