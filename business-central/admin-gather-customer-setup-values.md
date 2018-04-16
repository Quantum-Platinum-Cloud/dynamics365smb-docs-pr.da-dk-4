---
title: "Indsaml debitoropsætningsværdier | Microsoft Docs"
description: "Du kan bruge konfigurationsspørgeskemaet for at reducere arbejdsbelastningen ved implementering ved at strømline opgave til at oprette en ny virksomhed. Du kan generere konfigurationsspørgeskemaet i Business Central og derefter give den til kunden som en Excel- (.xls) eller XML-fil."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a1333567069d24bc5eff48d668dca8b480b85914
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="gather-customer-setup-values"></a>Indsaml debitoropsætningsværdier
Du kan bruge konfigurationsspørgeskemaet for at reducere arbejdsbelastningen ved implementering ved at strømline opgave til at oprette en ny virksomhed. Du kan generere konfigurationsspørgeskemaet i [!INCLUDE[d365fin](includes/d365fin_md.md)] og derefter give det til kunden som en Excel- eller XML-fil.  

Du kan ændre alle standardværdier i et spørgeskema, så de bedre opfylder kundens behov.  

> [!TIP]  
>  Du kan finde flere oplysninger om definition af konfigurationsværdier i felterne til forsyningsplanlægning i [Oprette bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md).  

Når kunden har udfyldt spørgeskemaet, importerer du filen til kundens nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-virksomhed. Du og din kunde validerer svarene til spørgeskemaet, før du anvender dem i regnskabet.

## <a name="to-create-a-configuration-questionnaire"></a>Sådan oprettes et konfigurationsspørgeskema
Du kan bruge et spørgeskema til at hjælpe dig med at afgøre omfanget af og behovet for konfiguration. Du kan oprette et nyt spørgeskema eller redigere et eksisterende spørgeskema ved at tilføje nye spørgsmål eller spørgeområder.  

 Du kan kun oprette spørgeskemaer til tabeller af opsætningstypen. Du kan f.eks. bruge værktøjet til at angive oplysninger i følgende vinduer:  

-   Virksomhedsoplysninger  
-   Anlægsopsætning  
-   Opsætning af Finans  
-   Opsætning af Lager  
-   Montagekonfiguration
-   Produktionsopsætning  
-   Købsopsætning  
-   Marketingopsætning  
-   Serviceopsætning  
-   Salgsopsætning  
-   Logistikopsætning  

> [!NOTE]  
>  Hvis du vil se en fuldstændig liste over opsætningstabeller, skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Opsætning** og derefter vælge det relaterede link. Til at afgøre omfanget af overflytning af data i poster, skal du bruge funktionerne til overflytning. Du kan finde flere oplysninger i [Overflytning af debitordata](admin-migrate-customer-data.md).  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfigurationsspørgeskema**, og vælg det relaterede link.  
2. Vælg handlingen **Ny**. Vinduet **Konfig.spørgeskema** åbnes.  
3. Vælg handlingen **Spørgsmålsområder**. Vinduet **Spørgsmålsområder** åbnes.  
4. Vælg handlingen **Ny**. Vinduet **Konfig.spørgsmålsområde** åbnes.  
5. I feltet **Tabel-id** skal du vælge id'et på den tabel, du vil indsamle oplysninger om. Feltet **Tabelnavn** udfyldes automatisk.  
6. Vælg handlingen **Opdater spørgsmål**. Hvert felt i tabellen føjes til spørgeskemaet med et spørgsmålstegn efter dets etiket.

Du kan omformulere etiketten for at gøre det klart, hvordan spørgsmålet skal besvares. Hvis et felt f.eks. kaldes "Navn", kan du redigere det til at angive "Hvad er navnet på <data being collected>". Du kan også vejlede andre i feltet **Reference**, inklusive en URL-adressen til en side, der indeholder yderligere oplysninger.  

Du kan også slette eventuelle spørgsmål, du ikke vil medtage i spørgeskemaet.  

> [!NOTE]  
>  Feltet **Svarindstilling** beskriver typen og formatet af de data i svaret, som er relevante. Feltet **Svar** indeholder oplysninger, der er angivet af brugeren.  
>   
>  Efter behov, kan du også definere standardsvar i feltet **Svar**. Disse værdier bruges som standard til brugerdefineret installation. Den person, der udfylder spørgeskemaet, kan dog redigere og opdatere svaret.  

## <a name="to-complete-the-configuration-questionnaire"></a>Sådan udfyldes konfigurationsspørgeskemaet
Du kan bruge konfigurationsspørgeskemaet til at strukturere og dokumentere en detaljeret diskussion om kundens specifikke behov. Du også bruge det til at indsamle opsætningsdata fra kunden for at konfigurere de relevante [!INCLUDE[d365fin](includes/d365fin_md.md)]-opsætningstabeller, såsom regnskab, lager og kunder.  

> [!NOTE]  
>  Du kan også oprette dit eget konfigurationsspørgeskema, som opfylder dine behov.  

1. Åbn det ønskede regnskab, du vil udfylde spørgeskemaet for.
2. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfigurationsspørgeskema**, og vælg derefter det relaterede link.  
3. Vælg spørgeskemaet for virksomheden, og vælg derefter handlingen **Udlæs til Excel** og eventuelt handlingen **Udlæs til XML**.
4. Få kunden til at udfylde konfigurationsspørgeskemaet ved at angive svarene i Excel-projektmappen. Der er et regneark for hvert spørgsmålsområde i spørgeskemaet.   
5. Vælg handlingen **Indlæs fra Excel**, og vælg .xlsx-filen med kundens svar.  
6. Vælg handlingen **Spørgeområder** for at begynde processen med at validere og anvende svarene på konfigurationsspørgeskemaet.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Sådan udfyldes et spørgeskema fra konfigurationsregnearket  
Den følgende procedure er en alternativ måde til at få adgang til konfigurationsspørgeskemaer. Det forudsættes, at konfigurationspakken, som du har fået leveret, indeholder spørgeskemaer.  

1. Når du har importeret en konfigurationspakke, skal du åbne konfigurationsregnearket.  
2. For hver tabel, hvor der er et spørgsmålsområde, skal du vælge handlingen **Spørgsmål**. Spørgeskemasiden åbnes.  
3. Besvar spørgsmålene, og vælg derefter handlingen **Anvend svar**.  
4. Vælg knappen **OK** for at lukke spørgeskemaet.

## <a name="to-validate-the-configuration-questionnaire"></a>Sådan valideres konfigurationsspørgeskemaet
Det er vigtigt at validere konfigurationsspørgeskemaet, før du anvender det på [!INCLUDE[d365fin](includes/d365fin_md.md)]-formatet. Det er en måde at sikre, at dataformateringen bevaers under import fra Excel.  

En almindelig valideringsopgave er at kontrollere, at tekststrenge ikke er indsat i datofelter. Denne revisionsproces er nødvendig, fordi formatet for svaret i spørgeskemaet ikke valideres automatisk, når funktionen **Anvend svar** køres.  

> [!NOTE]  
>  Validering af konfigurationsspørgeskemaet er generelt en manuel proces. Der er dog kontrol for regionale formateringsuoverensstemmelser. Desuden vil du få fejl, hvis strukturen i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-database ikke stemmer overens med strukturen i overflytningsdatabasen.  

1. I vinduet **Konfigurationsspørgeskema** skal du vælge det relevante spørgeskema og derefter vælge handlingen **Spørgsmålsområder**.  
2. Åbn det relevante spørgsmålsområde.  
3. For hvert spørgsmål skal du kontrollere, at værdien i feltet **Svar** svarer til det format, der er anført i feltet **Svarindstilling**. Kontrollér f.eks., at adressen på en virksomhed er i tekstformat.  
4. Hvis du finder fejl, kan du foretage fejlfinding og foretage rettelser i Excel ved at udlæse spørgeskemaet og derefter indlæse det igen. Du kan også rette fejl direkte i [!INCLUDE[d365fin](includes/d365fin_md.md)], efterhånden som du gennemgår svarene i vinduet **Konfig.spørgsmålsområde**.  
5. Gentag disse trin for hvert spørgsmålsområde.  

Når du har fuldført din validering, er dataene klar til at blive anvendt til databasen.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Sådan anvendes svar fra konfigurationsspørgeskemaet
Når du har indlæst og valideret oplysninger fra et konfigurationsspørgeskema, kan du overføre eller anvende opsætningsdata til de tilsvarende tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Konfigurationsspørgeskema**, og vælg derefter det relaterede link. Vinduet **Konfig.spørgeskema** åbnes.  
2. Vælg et konfigurationsspørgeskema på listen, og vælg derefter handlingen **Rediger liste**.  
3. Du kan anvende svar på en af to måder.  

- Hvis du vil anvende hele spørgeskemaet, skal du vælge handlingen **Anvend svar**.  
- Hvis du vil anvende svar kun for et bestemt **Spørgsmålsområde**, skal du vælge handlingen **Spørgeområder**, vælge et **Spørgsmålsområde** på listen og derefter vælge handlingen **Anvend svar**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Sådan kontrollerer du, at svarene er blevet anvendt korrekt  
1. Kontrollér opsætningsvinduerne for de forskellige funktionelle områder i [!INCLUDE[d365fin](includes/d365fin_md.md)]. For at finde vinduet skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") angive navnet på konfigurationsvinduet og derefter vælge det relaterede link.  
2. Kontrollér, at felterne er blevet udfyldt med de korrekte data fra de forskellige spørgsmålsområder i konfigurationsspørgeskemaet.  

Du har nu konfigureret opsætning med debitorens forretningsmæssige oplysninger og regler.

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
