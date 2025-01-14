---
title: Konfigurere godkendelsesworkflows (indeholder video)
description: 'Konfigurere arbejdsgange, brugere af arbejdsgangen og godkendelses brugere til at forbinde forretningsproces systemopgaver, der udføres af disse brugere.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="set-up-approval-workflows" />Konfigurer godkendelsesworkflow

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin. Flere oplysninger i [Bruge godkendelsesworkflows](across-use-workflows.md).

Inden du kan bruge godkendelsesworkflows, skal du oprette workflowbrugere og godkendelsesbrugere, angive, hvordan brugere modtager notifikationer om trin i workflows.

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.

[!INCLUDE[workflow](includes/workflow.md)]

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Opret arbejdsgangbrugere og brugergrupper.|[Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)|  
|Konfigurer arbejdsgangbrugere, der indgår i godkendelsesarbejdsgange.|[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)|  
|Angiv, hvordan arbejdsgang brugere skal have besked om trin i arbejdsgangen, herunder godkendelsesanmodninger.|[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)|  
|Angiv, om brugerne får besked via e-mail, og noter, hvor ofte notifikationer sendes.|[Angive, hvornår og hvordan notifikationer modtages](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Tilpas indholdet af e-mailmeddelelserne ved at tilpasse Rapport 1320, Notifikationsmail.|[Sådan opretter og ændrer du Brugerdefinerede rapportlayouts](ui-how-create-custom-report-layout.md)|  
|Konfigurer en SMTP-server til at aktivere mailkommunikation til og fra [!INCLUDE[prod_short](includes/prod_short.md)]|[Konfigurere mail](admin-how-setup-email.md)|
|Angiv de forskellige trin i en arbejdsgang ved at forbinde arbejdsgangshændelser med arbejdsgangsvar.|[Opret godkendelsesworkflows](across-how-to-create-workflows.md)|  
|Brug workflowskabeloner til at oprette nye workflows.|[Oprette godkendelsesworkflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)|  
|Del workflows med andre [!INCLUDE[prod_short](includes/prod_short.md)]-databaser.|[Eksportere og importere godkendelsesworkflows](across-how-to-export-and-import-workflows.md)|  
|Lær, hvordan du konfigurerer en arbejdsgang til godkendelse af salgsdokumenter ved at følge en hel procedure.|[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow" />Eksempel på et godkendelsesworkflow

Denne video viser, hvordan du konfigurerer et workflow, der kræver, at en bruger anmoder om en andens godkendelse, før vedkommende kan ændre oplysninger om en eksisterende kunde eller oprette en ny kunde.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also" />Se også

[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Workflow](across-workflow.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbejde med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
