---
title: Inspektion af sider i Business Central
description: Brug sideinspektionsfunktionen til at zoome ind på oplysninger om sideopsætningen og datakilden. Sideinspektion er velegnet til fejlfinding af problemer med dine data.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 04/01/2019
ms.openlocfilehash: eb9d4ec76c0dbbd59763f7622ca51137c9563a91
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2019
ms.locfileid: "969874"
---
# <a name="inspecting-pages-in-business-central"></a>Inspektion af sider i Business Central

Sideinspektionsfunktionen giver mulighed at få oplysninger om en side, giver dig indsigt i sideopsætningen, de forskellige elementer, der udgør siden, og kilden bag de data, der vises. Sideinspektion er specielt beregnet til administratorer, superbrugere, supportmedarbejdere og udviklere. Den er velegnet til læring af datamodellen bag en side og fejlfinding. Hvis der f.eks. opstår et problem med en side, kan du bruge sideinspektion til at hente oplysninger,der skal videregives til systemadministratoren eller supportmedarbejderne.

## <a name="working-with-page-inspection"></a>Arbejde med sideinspektion

Hvis du vil inspicere en side, skal du vælge ![ikonet Indstillinger](media/ui-experience/settings_icon_small.png) i øverste højre hjørne vælge og derefter klikke på **Inspicer**. Du kan også bruge tastaturgenvejen **Ctrl+Alt+F1**.

Ruden **Sideinspektion** åbnes på siden. Følgende figur illustrerer ruden **Sideinspektion** på siden **Salgsordre**.

![Sideinspektion](media/page-inspection-example.png)

Når ruden **Sideinspektion** åbnes første gang, indeholder den oplysninger, der vedrører hovedsidens objekt.

Bruge tastaturgenvejen eller pegeredskabet til at flytte fokus til forskellige elementer på siden. Når du vælger en faktaboks eller et element på hovedsiden, er det omgivende område fremhævet med en kant, og ruden **Sideinspektion** viser oplysninger om det valgte element. Den foregående figur viser f.eks. oplysninger om oversigtsdelen på siden **Salgsordre**. Når du navigerer til andre sider i programmet, opdateres ruden **Sideinspektion** automatisk med sideoplysningerne, mens du bevæger dig videre.

Du kan finde flere oplysninger om, hvad der vises i sideinspektionen, i [Inspektion og fejlfinding af sider](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjælpen til Business Central-udviklere og it-eksperter.

Hvis du ikke kan se de oplysninger, du forventer at se, i ruden **Sideinspektion**, har du sandsynligvis ikke har de nødvendige rettigheder som beskrevet i næste sektion.

## <a name="controlling-access-to-page-inspection-details"></a>Styring af adgang til oplysninger om sideinspektion

Som administrator kan du styre adgang til alle detaljer, der vises i ruden **Sideinspektion**, ved at konfigurere de rettigheder, som brugere har. Hvis du vil tildele en bruger rettigheder til alle detaljer, skal du give vedkommende rettigheden **Udfør** til **System** objekt **5330**. Du kan give denne rettighed ved hjælp af et rettighedssæt (f.eks. **D365-fejlfinding**) eller en brugergruppe (f.eks. **D365-fejlfinding**). Du kan finde flere oplysninger om rettigheder i [Administrere brugere og deres rettigheder](ui-how-users-permissions.md).

Brugere, der ikke tildeles rettigheder i **Systemobjekt 5330**, kan stadig få adgang til ruden **Sideinspektion**, men de får kun vist felterne **Side** og **Tabel**, der viser grundlæggende oplysninger, som de kan videregive til deres supportteam.

## <a name="see-also"></a>Se også

[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  