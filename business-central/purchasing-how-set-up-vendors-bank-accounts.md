---
title: Konfigurere kreditorbankkonto
description: Få mere at vide om, hvordan du knytter bankkonti til kreditorkort i Business central, herunder kontaktoplysninger, SWIFT-og IBAN-koder.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 07/04/2022
ms.author: a-reishima
ms.openlocfilehash: 1839f54de2382ad5b7d8b6b936181e105a56e06b
ms.sourcegitcommit: 5560a49ca4ce85fa12e50ed9e14de6d5cba5f5c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2022
ms.locfileid: "9144394"
---
# <a name="set-up-vendor-bank-accounts"></a>Konfigurere kreditorbankkonti

På samme måde som du kan bruge bankkontooplysninger på [!INCLUDE [prod_short](includes/prod_short.md)] til at holde styr på virksomhedens banktransaktioner, kan du også angive bankoplysninger for kreditorer. Kreditorbankkonto data kan forenkle betalinger til leverandører, når de kombineres med [AMC Banking 365 Fundamentals-filtypenavn](ui-extensions-amc-banking.md) eller [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)-funktion, f. eks.

## <a name="add-or-edit-a-vendor-bank-account"></a>Tilføje eller redigere en kreditorbankkonto

[!INCLUDE [purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

> [!TIP]
> Du kan angive flere kreditorbankkonti på siden **Kreditorbankkontoliste**.

## <a name="set-up-a-preferred-vendor-bank-account"></a>Konfigurere en foretrukken kreditorbankkonto

Hvis en kreditor har en eller flere bankkonti, og du vil angive en foretrukken indstilling for Udbetalingskladdelinjer, skal du benytte følgende fremgangsmåde:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Åbn kortet for kreditoren.
3. Vælg standard kreditorbankkontoen i feltet **Foretrukken bankkontokode** i oversigtspanelet **Betaling**.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Konfigurere bankkonti](bank-how-setup-bank-accounts.md)  
[Brug AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]