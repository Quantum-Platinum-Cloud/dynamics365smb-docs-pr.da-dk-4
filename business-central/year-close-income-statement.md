---
title: "Nulstille resultatopgørelseskonti | Microsoft Docs"
description: "Ved årsregnskabets afslutning skal du udføre kørslen Nulstil resultatopgørelse for at afslutte de regnskabsperioder, der udgør regnskabsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3cea438b7d3dc1b14baaf76ae1b7ff97195f2191
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="close-income-statement-accounts"></a>Nulstille resultatopgørelseskonti
Når regnskabsåret er slut, skal du afslutte de perioder, det indeholder. Brug kørslen **Nulstil resultatopgørelse** for at gøre dette. Denne kørsel overfører årets resultat til en konto i balancen og nulstiller resultatopgørelseskonti. Det gør du ved at oprette linjer i en kladde, som du derefter kan bogføre.

## <a name="to-run-the-close-income-statement-batch-job"></a>Sådan udføres kørslen Nulstil resultatopgørelse
1. Afslut regnskabsåret. Regnskabsåret skal være afsluttet, før kørslen kan sættes i gang. Du kan finde flere oplysninger i [Afslutte regnskabsperioder](year-close-account-periods.md).
2. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Nulstil resultatopgørelse**, og vælg derefter det relaterede link.
3. Vælg **OK** for at eksekvere kørslen.

## <a name="about-the-close-income-statement-batch-job"></a>Om kørslen Nulstil resultatopgørelse
Ved kørslen behandles alle finansposter af typen Resultatopgørelse, og der oprettes poster, som tilbagefører balancerne. Hver post er totalen af alle finansposter i kontoen i regnskabsåret. Disse nye poster placeres i en kladde, hvor du skal angive en modkonto og en resultatkonto i balancen, inden du bogfører. Når du bogfører kladden, bliver der bogført en post på hver resultatopgørelseskonto, der får saldoen til at gå i nul, og samtidig overfører årets resultat til balancen.

Du skal selv bogføre kladden. Posterne bogføres ikke automatisk ved kørslen, undtagen når der bruges en ekstra rapporteringsvaluta. Når der bruges ekstra rapporteringsvaluta, bogfører kørslen posterne direkte til finansposterne.

Datoen på de linjer, som kørslen indsætter i kladden, vil altid være en ultimodato for regnskabsåret. Ultimodatoen er en fiktiv dato mellem den sidste dag i det gamle regnskabsår og den første i det nye. Fordelen ved at bogføre på ultimodatoen er, at du stadig har de korrekte saldi for de almindelig dage i regnskabsåret.

Kørslen **Nulstil resultatopgørelse** kan bruges flere gange. Du kan bogføre i et tidligere regnskabsår, også efter resultatopgørelseskontiene er nulstillet, hvis du udfører kørslen igen.

## <a name="see-also"></a>Se også
[Afslutningregnskab](year-close-books.md)  
[Bogføre årsafslutningsposten](year-how-post-year-end-close-entry.md)  
[Åbne et nyt regnskabsår](finance-how-open-new-fiscal-year.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
