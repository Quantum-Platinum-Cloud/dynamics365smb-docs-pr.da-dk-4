---
title: Dynamics 365 for Financials og indholdspakker til Power BI | Microsoft Docs
description: "Du kan nemt få indsigt, business intelligence og nøgletal i dine Financials-data med Power BI og Financials-indholdspakker."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 537effab2f406d619c5000efad12754db678e8b8
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivere virksomhedens data til Power BI
Du kan nemt få indsigt i dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data med Power BI og [!INCLUDE[d365fin](includes/d365fin_md.md)]-indholdspakker. Power BI henter dine data og opretter derefter et out-of-the-box dashboard og rapporter baseret på dataene.  

Indholdspakkerne er konfigureret til arbejde med salgstal og finansielle data fra demonstrationsvirksomheden, som du får, når du tilmelder dig eksempelvisningen af [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].  

* Vælg en visualisering på dashboardet for at få vist en af syv underliggende rapporter.  
* Filtrer rapporten, eller tilføj felter, du vil overvåge.  
* Fastgør denne brugerdefinerede visning til dashboardet for fortsat sporing.  
  Dashboardet og de underliggende rapporter opdateres dagligt. Du kan kontrollere opdateringsplanen og ændre hyppigheden på datasættet.  

> [!NOTE]  
>   Du kan også oprette dine egne rapporter og dashboards i Power BI baseret på dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Du kan finde flere oplysninger under [Forbinde dine virksomhedsdata med Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI
Når du vil have vist dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data i Power BI, skal du have følgende:  

* Adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger under [Financials](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Adgang til Power BI. Du kan finde flere oplysninger i [Power BI](https://powerbi.microsoft.com).

Du kan finde flere oplysninger på Power BI-webstedet om at [oprette forbindelse til tjenester med indholdspakker til Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Når du vil have adgang til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data skal du på forbindelsessiden i Power BI angive følgende oplysninger:

| Felt | Beskrivelse |
| --- | --- |
| **URL-adresse til OData Feed** |OData URL-adressen så Power BI kan få adgang til din virksomhed f.eks. https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Godkendelsesmetode** |Vælg **Basic**. |
| **Brugernavn** |Dit navn som det vises for kontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. *John Smith*. |
| **Adg.kode** |Dette er webtjenesteadgangsnøglen til din brugerkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Det betyder, at du skal have tre oplysninger fra Financials: OData URL-adressen og webtjenesteadgangsnøglen til brugerkontoen.  

### <a name="getting-the-url"></a>Hente URL-adressen
Når du tilføjer [!INCLUDE[d365fin](includes/d365fin_md.md)] til Power BI, skal du angive en URL-adresse, så Power BI kan få adgang til data fra din virksomhed. På forbindelsessiden omtales URL-adressen som **URL-adresse til OData Feed**, og den skal have følgende format:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
I dette eksempel er *mybusiness* navnet på Financials-tjenesten, og *CRONUS US* er navnet på demonstrationsvirksomheden, hvor *% 20* repræsenterer området i navnet.   
Du henter URL-adressen ved i [!INCLUDE[d365fin](includes/d365fin_md.md)] at søge efter og åbne vinduet **Webtjeneste**. Dette vindue viser de webtjenester, der aktuelt er tilgængelige, og du kan kopiere linket fra feltet **URL-adresse til OData** til en af standard OData-webtjenesterne.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Få brugernavnet og adgangsnøglen til webtjenesten
Hvis du vil bruge data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI skal du i vinduet **Opret forbindelse til Financials** angive et brugernavn og en adgangskode. Brugernavnet er dit navn som det vises for kontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så Power BI kan logge det i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Adgangskoden er den webtjenesteadgangsnøgle, der er konfigureret til din brugerkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du finder disse oplysninger ved i [!INCLUDE[d365fin](includes/d365fin_md.md)] at søge efter vinduet **Brugere** og derefter åbne kortet for din brugerkonto. I oversigtspanelet **Generelt** skal du kopiere indholdet af feltet **Brugernavn** og i oversigtspanelet **Webtjenesteadgang** kopiere indholdet af feltet **Webtjenesteadgangsnøgle**. Hvis feltet **Webtjenesteadgangsnøgle** er tomt, skal du på båndet vælge **Angiv webtjenesteadgangsnøgle**, vælge feltet **Nøglen udløber aldrig** og derefter klikke på knappen OK. Derefter kan du kopiere nøglen.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Hente data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]
[!INCLUDE[d365fin](includes/d365fin_md.md)]-dashboardet viser de mest almindelige rapporter, du kan bruge til at registrere din virksomhed. Dataene er hentet fra [!INCLUDE[d365fin](includes/d365fin_md.md)]-virksomheden ved hjælp af webtjenester, der læser data direkte. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du i vinduet **Webtjenester** se webtjenester, der er konfigureret til dig, herunder følgende, der forbruges af indholdspakken i Power BI:  

* ItemSalesAndProfit  
* ItemSalesByCustomer  
* powerbifinance  
* SalesDashboard  
* SalesOpportunities  
* SalesOrdersBySalesPerson  
* TopCustomerOverview  

> [!NOTE]  
>   Hvis du ændrer navnet på en af disse webtjenester, vises data ikke i Power BI.  
Hvis du vil tilføje andre data i Power BI, skal du finde tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)], vise dem som webtjenester og derefter føje dem til indholdspakken. Dette er et avanceret scenarie, og det anbefales, at du starter med de data, der allerede findes i Power BI.  

## <a name="troubleshooting"></a>Fejlfinding
Power BI-dashboardet er baseret på de publicerede webtjenester, der er anført ovenfor, og viser data fra demonstrationsvirksomheden eller din egen virksomhed, hvis du indlæser data fra dit aktuelle økonomisystem. Men hvis noget går galt indeholder dette afsnit en løsning til de mest almindelige problemer.  

**"Parametervalideringen mislykkedes, kontroller, at alle parametre er gyldige"**  
Hvis du får denne fejlmeddelelse, når du har angivet URL-adressen til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du kontrollere, at følgende krav opfyldt:  

* URL-adressen følger dette mønster nøjagtigt:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Slet tekst, der evt. står efter firmanavn i parentes  
* Kontroller, at der ikke er nogen efterfølgende skråstreg i slutningen af URL-adressen.  
* Sørg for, at det er en sikker forbindelse, som når URL-adressen starter med *https*.  

**"Logon mislykkedes"**  
Hvis fejlmeddelelsen "Logon mislykkedes" vises, når du logger på dashboardet ved hjælp af dine legitimationsoplysninger til [!INCLUDE[d365fin](includes/d365fin_md.md)], kan det skyldes en af følgende situationer:

* Den konto, du bruger, har ikke rettigheder til at læse [!INCLUDE[d365fin](includes/d365fin_md.md)]-data fra din konto.

    Kontroller din brugerkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)], og kontroller, at du har brugt den rigtige webtjenesteadgangsnøgle som adgangskode, og prøv derefter igen.  
* Den [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomst, du prøver at oprette forbindelse til, har ikke et gyldigt SSL-certifikat. I dette tilfælde kan du se en mere detaljeret fejlmeddelelse ("kan ikke etablere SSL-tillidsrelation").

    > [!NOTE]  
>   Selvsignerede certifikater understøttes ikke.  

**"UPS"**  
Hvis du får vist en "UPS"-fejlmeddelelse, når du er færdig med godkendelsesdialogboksen, skyldes dette oftest problemer med forbindelsen til dataene til indholdspakken.

* Kontroller, at URL-adressen følger det mønster, der blev angivet tidligere:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* En almindelig fejl er at angive hele URL-adressen til en bestemt webtjeneste:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance  
* Eller du kan have glemt at angive firmanavnet:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/  

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Overføre virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Bruge [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruge [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som PowerApps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruge [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] i Microsoft Flow](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]