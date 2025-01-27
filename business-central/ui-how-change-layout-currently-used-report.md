---
title: Ændre udseendet af en rapport ved at vælge et andet layout
description: Du kan bruge forskellige layout til en rapport og skifte mellem layout for at ændre udseendet af en rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
---
# <a name="legacy-set-the-layout-used-by-a-report" />(Ældre) Angive det layout, der bruges af en rapport

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

En rapport kan konfigureres med flere rapportlayout, som du kan skifte mellem efter behov.

Afhængig af de layout, der er tilgængelige for en rapport, kan du vælge at bruge et indbygget RDLC-rapportlayout, et indbygget Word-rapportlayout eller et brugerdefineret layout. Find flere oplysninger om RDLC- og Word-rapportlayout, indbyggede og brugerdefinerede layout og mere under [Administration af rapportlayout](ui-manage-report-layouts.md).

Når der er defineret brugerdefinerede rapportlayout, kan du vælge dem fra debitor- og leverandørkortene for at angive, at det valgte layout skal bruges til de dokumenter, som du har oprettet for den pågældende debitor eller leverandør. Du kan finde flere oplysninger i [Definition af Dokumentlayouts til debitorer og leverandører](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Rapporter af typen dokument (ikke lister), der bruger et Word-rapportlayout, er typisk hurtigere end dem, der bruger et RDLC-rapportlayout. Så hvis du har mulighed for at vælge mellem et Word- eller et RDLC-rapportlayout for en rapport af typen dokument, skal du bruge Word-rapportlayoutet til at få den bedste ydeevne.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document" />Sådan ændres det rapportlayout, der skal bruges til en rapport eller et dokument

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valg af rapportlayout**, og vælg derefter det relaterede link.
  
   Siden **Valg af rapportlayout** viser en liste over alle de rapporter, der er tilgængelige i den virksomhed, der er angivet i feltet **Virksomhed** øverst på siden. **Layoutbeskrivelse** <!-- **Selected Layout** -->-feltet angiver det rapportlayout, der aktuelt bruges på rapporten.
2. Angiv feltet **Virksomhed** øverst på siden til det firma, der indeholder rapporten.

   I dette felt kan du oprette forskellige layout for samme rapport rapport i forskellige regnskaber.

3. Hvis du vil ændre layoutet for en rapport, skal du på rækken for rapporten angive feltet **Valgt layout** til en af følgende indstillinger:
   * **RDLC (indbygget)**, bruger det indbyggede RDLC-rapportlayout i rapporten.
   * **Word (indbygget)**, bruger det indbyggede Word-rapportlayout i rapporten.
   * **Brugerdefineret**, bruger et brugerdefineret layout i rapporten.  

> [!NOTE]
> Hvis du vælger et rapportlayout af typen **RDLC (indbygget)** eller **Word (indbygget)** , og du får en fejlmeddelelse om, at rapporten ikke har et layout med den angivne type, skal du vælge en anden layoutindstilling eller oprette en brugerdefineret rapport af den type, du vil bruge. Se den næste fremgangsmåde.

Hvis du har valgt et indbygget RDLC- eller Word-rapportlayout, kræves ingen yderligere handling, og layoutet bruges, næste gang rapporten køres.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout" />Sådan ændres et brugerdefineret rapportlayout for et rapportlayout

Du kan også ændre det aktuelt anvendte brugerdefinerede layout. Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).

Alle brugerdefinerede rapportlayout, der findes for rapportlayoutene i en virksomhed, vises på siden **Brugerdefinerede rapportlayouts**. På siden **Valg af rapportlayout** kan du se, hvilke brugerdefinerede layout der er tilgængelige for hver rapport i faktaboksen **Brugerdefinerede layouts**.

1. På siden **Valg af rapportlayout** skal du på linjen for det rapportlayout, som du ønsker at ændre, vælge opslagsknappen i feltet **Beskrivelse af brugerdefineret layout**.
2. På siden **Tilpassede rapportlayouts** skal du vælge rækken for det brugerdefinerede layout, du vil bruge, og derefter vælge knappen **OK**.

Navnet på det valgte brugerdefinerede layout vises nu i feltet **Beskrivelse af brugerdefineret layout** og vil blive brugt næste gang, rapporten eller dokumentet vises i forhåndsvisning, udskrives eller sendes.

Du kan nu gå til debitor- og leverandørkortene for at angive, hvilke layouts der skal bruges til de forskellige dokumenter, som du opretter for den pågældende debitor eller leverandør, såsom ordrebekræftelser eller betalingsrykkere. Du kan finde flere oplysninger i [Definition af Dokumentlayouts til debitorer og leverandører](ui-define-customer-vendor-document-layouts.md).

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics-365-business-centralindex" />Se relateret [Microsoft-træning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Se også
[Administration af rapportlayout](ui-manage-report-layouts.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
