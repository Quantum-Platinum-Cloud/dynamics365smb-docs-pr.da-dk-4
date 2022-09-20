---
title: Kør opgaver i baggrunden
description: Konfigurere synkronisering af data mellem Business central og Shopify i baggrunden.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: f353edb4c505fd7b3eb498392abca3ce481b6009
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768104"
---
# <a name="run-tasks-in-the-background"></a>Kør opgaver i baggrunden

Det er effektivt at køre nogle opgaver samtidig og på en automatiseret måde. Du kan udføre disse opgaver i baggrunden, og du kan også angive en tidsplan, når opgaverne skal afvikles automatisk. Der understøttes to tilstande for at udføre opgaver i baggrunden:

- Manuelt udløste opgaver planlægges øjeblikkeligt via **Opgavekøposter**
- Tilbagevendende opgaver er planlagt i **Opgavekøposter**

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Udføre opgaver i baggrunden for et bestemt trykkeri

1. Gå til søgning ![Lightbulb, der åbner funktionen Fortæl mig.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skal du skrive navnet på **Shopify Butik** og vælge butiksnavnet på listen.
2. Marker det indkøb, som du vil synkronisere varer til for at åbne siden **Shopify-købskort**.
3. Aktivér **Tillad baggrundssynkronisering** til/fra.

Når synkroniseringshandlingen udløses i stedet for en opgave, der kører i forgrunden, bliver du nu bedt om at vente. Når den er fuldført, kan du fortsætte til næste handling. Opgaven oprettes som **Opgavekøpost** og starter straks på en måde, der ikke blokerer for spærringen.

## <a name="to-schedule-recurring-tasks"></a>Sådan planlægges tilbagevendende opgaver

Du kan planlægge, at følgende tilbagevendende aktiviteter skal udføres automatisk. Du kan finde flere oplysninger om planlægning af opgaver i [Opgavekø](../admin-job-queues-schedule-tasks.md).

|Opgave|Objekt|
|------|------------|
|**Synkroniser ordrer fra Shopify**|Rapport 30104 Synkroniser ordrer fra Shopify|
|**Behandle Shopify ordrer**|Rapport 30103 Shopify oprette slagsordrer|
|**Synkroniser forsendelser til Shopify**|Rapport 30109 synkronisering af forsendelse til Shopify|
|**Synkronisere produkter og/eller priser**|Rapport 30108 Shopify synkroniser produkter|
|**Synkroniser lager**|Rapport 30102 Synkroniser lager til Shopify|
|**Synkroniser billeder**|Rapport 30107 Shopify Synkroniser billeder|
|**Synkroniser debitorer**|Rapport 30100 Shopify Synkroniser kunder|
|**Synkroniser betalinger**|Rapport 30105 Shopify Synkroniser betalinger|

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)  