---
title: Fejlfinding af Shopify og Business Central-synkronisering
description: 'Få mere at vide om, hvad du skal gøre, hvis noget er galt under synkronisering af data mellem Shopify Business Central.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# Fejlfinding af Shopify og Business Central-synkronisering

Du kan køre i situationer, hvor du skal foretage fejlfinding af problemer ved synkronisering af data mellem Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Denne side definerer trin til fejlfinding i forbindelse med typiske scenarier.

## Kør opgaver i forgrunden

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, du vil fejlfinde for at åbne siden **Shopify-købskort**.
3. Deaktivér **Tillad baggrundssynkronisering** til/fra.

Når synkroniseringshandlingen udløses, køres opgaven nu i forgrunden. Hvis der opstår en fejl, vises der en fejldialogboks med linket **Kopieringsoplysninger**. Brug linket til at kopiere yderligere oplysninger til en teksteditor til yderligere analyse.

## Logfiler

Hvis en synkroniseringsopgave mislykkes, kan du aktivere logføring ved at aktivere til/fra-feltet **Log aktiveret** på siden **Shopify-butikskortet**. Udløs derefter synkroniseringsopgaven manuelt, og gennemgå logfiler manuelt.

### Aktivere logføring

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butik**, og vælg det relevante link.
2. Marker den butik, du vil fejlfinde for at åbne siden **Shopify-købskort**.
3. Aktivér **Logfil aktiveret**-feltet til/fra.

### Gennemse logfiler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-logposter**, og vælg det relaterede link.
2. Vælg den relaterede logpost, og åbn derefter siden **Shopify-logpost**.
3. Gennemsynsanmodning, statuskode og beskrivelse og svarværdier. Du kan hente anmodnings- og svarværdierne som filer i et tekstformat.

Husk at slå logføring fra for at undgå negativ påvirkning af ydeevnen og øge databasens størrelse.

Fra siden **Shopify-logposter** kan du udløse sletning af alle logposter eller poster, der er ældre end syv dage.

## Dataregistrering

Uanset om **Logfilen er aktiveret**, registreres nogle Shopify-svar altid. Du kan undersøge eller hente logfilerne fra siden **Dataregistreringsliste**.

Vælg handlingen **Hentet Shopify-data** på en af følgende sider:

- **Shopify-ordre**
- **Shopify-ordreopfyldning**
- **Shopify-ordreforsendelsesomkostninger**
- **Shopify-ordretransaktioner**
- **Shopify-udbetalinger**
- **Shopify-betalingstransaktioner**
- **Shopify-transaktioner**

## Nulstil synkronisering

For at opnå optimal ydeevne importerer connectoren kun kunder, produkter og ordrer, der er oprettet eller ændret siden sidste synkronisering. På siden **Shopify-butikskort** er der funktioner, der kan ændres seneste synkroniseringsdato/-tidspunkt eller helt nulstille. Denne funktion sikrer, at alle data synkroniseres og ikke kun ændringerne siden den seneste synkronisering, når synkroniseringen køres.

Denne funktion gælder kun for synkroniseringer fra Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)]. Det kan være nyttigt, hvis du har brug for at gendanne slettede data, f. eks. produkter, kunder eller slettede ordrer.

## Anmode om adgangstoken

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke kan oprette forbindelse til din Shopify-konto, kan du prøve at nulstille dette adgangstoken fra Shopify. Du skal muligvis anmode om et nyt token, hvis der var ændringer til sikkerhedsnøglerne eller de nødvendige tilladelser (områder).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butikker**, og vælg det relevante link.
2. Marker den butik, for hvilken du vil have adgangstoken til at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Anmod om adgang**.
4. Hvis du bliver bedt om det, skal du logge på din Shopify-konto.

Funktionen **Vis Accesskey** vil blive aktiveret.

## Kontrollere og aktivere tilladelser til at foretage HTTP-anmodninger, når der køres i et ikke-produktionsmiljø

Hvis Shopify-connector-udvidelsen skal fungere korrekt, kræver det, at du har tilladelse til at foretage HTTP-anmodninger. Når der testes i sandkasse, er HTTP-anmodninger forbudt for alle udvidelser.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udvidelsesstyring**, og vælg derefter det relaterede link.
2. Vælg udvidelsens **Shopify Connector**.
3. Vælg handlingen **Konfigurer** for at åbne siden **Udvidelsesindstilling**.
4. Kontroller, at funktionen **Tillad HTTPClient-anmodninger** er aktiveret.

## Rotere Shopify-adgangstoken

Følgende procedurer beskriver, hvordan du kan rotere det adgangstoken, der bruges af Shopify-connector, til at få adgang til dit Shopify online Center.

### I Shopify

1. Fra din **Shopify Admin** skal du gå til [Apps](https://www.shopify.com/admin/apps).
2. I rækken med **Dynamics 365 Business Central**-appen skal du vælge **Slet**.
3. I meddelelsen, der vises, skal du vælge **Slet**.

### I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-shops**, og vælg derefter det relaterede link.
2. Marker den butik, for hvilken du vil have adgangstoken til at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Anmod om adgang**.
4. Hvis du bliver bedt om det, skal du logge ind på din Shopify-konto, gennemse personlige oplysninger og tilladelser og derefter vælge knappen **Installer app**.

## Kendte problemer

### Fejl: Salgshovedet findes ikke. Id-felter og -værdier: Dokumenttype = 'quote',nr. = 'YOUR SHOPIFY STORE'

Hvis du vil beregne den pris, som Shopify Connector opretter midlertidigt salgsdokument (tilbud) til midlertidig kunde (butikskode), og du kan bruge standard pris beregningslogikken til at udføre opgaven. Hvis en tredjepartsudvidelse abonnerer på hændelser i et midlertidigt salgsdokument, er hovedet muligvis ikke tilgængeligt. Det anbefales, at du kontakter udvidelsesudbyderen. Bed dem om at ændre deres kode, så de kan kontrollere, om der er midlertidige poster. I nogle tilfælde er det tilstrækkeligt, at `IsTemporary` tilføjer metoden på det rigtige sted. Du kan få mere at vide om `IsTemporary` ved at gå til [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Hvis du vil kontrollere, om problemet er forårsaget af et filtypenavn fra tredjepart, skal du bruge linket **Kopier oplysninger til Udklipsholder** i fejlmeddelelsen og kopiere indholdet til tekstredigeringsprogrammet. Oplysningerne indeholder en **AL-kaldestak**, hvor den øverste linje er den linje, hvor fejlen opstod. Det følgende er et eksempel på en AL-kaldestak.

AL-kaldt stak:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Husk at dele oplysninger fra AL-kaldestakken med leverandøren af filtypenavnet.

### Fejl: Gen. Virksomhed-bogføringsgruppe skal have en værdi i Debitor: 'YOUR SHOPIFY STORE'. Den må ikke være nul eller tom

Udfyld feltet **Debitorskabelonkode** på siden **Shopify Butikskort** med den skabelon, som har udfyldt **Virksomhedsbogføringsgruppe**. Debitorskabelonen bruges til at oprette debitorer og til at beregne salgspriser på salgsdokumenter.

### Fejl: Import af data til din Shopify-butik er ikke aktiveret. Gå til butikskortet for at aktivere det

På siden **Shopify-butikskort** skal du slå **Tillad datasynkronisering med Shopify** til. Denne indstilling hjælper med at beskytte onlinebutikken mod at hente demonstrationsdata fra [!INCLUDE[prod_short](../includes/prod_short.md)].

### Fejl: Oauth-fejl invalid_request: Kan ikke finde Shopify API-programmet med api_key

Det ser ud til, at du bruger [Indlejret app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), hvor klientens URL-adresse har formatet:`https://[application name].bc.dynamics.com`. Shopify-connectoren virker ikke for indlejrede apps. Flere oplysninger i [Hvilke Microsoft-produkter er Shopify-connectoren tilgængelige for?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### Fejl: Intern fejl. Det ser ud til, at noget gik galt. Anmodnings-id: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Kontakt Shopify support inden for 7 dage efter, at du har oplevet fejlen, og Angiv anmodnings-id'et. Du kan få flere oplysninger ved at gå til [Supportmuligheder i Shopify](shopify-faq.md#shopify).

## Se også

[Kom i gang med Connectoren til Shopify](get-started.md)
