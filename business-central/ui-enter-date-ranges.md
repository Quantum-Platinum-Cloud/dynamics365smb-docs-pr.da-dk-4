---
title: Angive datoer og klokkeslæt i Business Central
description: 'Få at vide, hvordan du angiver datoer og tidspunkter med forskellige produktivitetstip som oversigter, udtryk og områder.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dates, reporting, filter, calendar, shorthand, range'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="work-with-calendar-dates-and-times" />Arbejde med kalenderdatoer og klokkeslæt

Du kan angive datoer og klokkeslæt på flere måder. [!INCLUDE[prod_short](includes/prod_long.md)] indeholder effektive funktioner, der fremskynder indtastning af data og hjælper dig med at skrive komplekse kalenderudtryk. Der er forskellige steder i programmet, hvor du kan angive datoer og klokkeslæt i felterne. På en salgsordre kan du f.eks. angive afsendelsesdatoen. Når du filtrerer lister eller rapportdata, kan du angive datoer og klokkeslæt for kun at finde de data, du er interesseret i.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="check-your-region-and-language-settings" />Kontrollere internationale og sproglige indstillinger

Siden **Mine indstillinger** angiver det **Område** og **Sprog**, du bruger i programmet. Disse indstillinger påvirker måden, du angiver datoer og klokkeslæt på.

- Indstillingen **Område** bestemmer, hvordan datoer, klokkeslæt, tal og valutaer vises og formateres.

- Når datomønstre omfatter ord, skal sproget for de ord, du bruger, svare til indstillingen **Sprog**.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] anvender den gregorianske kalender.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates" />Angive datoer

I et datofelt kan du angive en dato i standardformatet for din land/områdeindstilling. Forskellige områder kan bruge forskellige separatorer mellem dage, måneder og år. For eksempel bruger nogle lande/områder bindestreger (mm-dd-åååå), mens andre bruger skråstreger (mm/dd/åååå).  

> [!TIP]
> Du kan bruge alle separatorer, selv mellemrum, og datoen ændres automatisk til brug af de separatorer, der gælder for dit land/område.

> [!NOTE]
> Det format, som datoer vises i på udskrevne rapporter eller dokumenter sendt med e-mails, ikke påvirkes af dit personlige valg af land/område.

For at arbejde mere produktivt med datoer og klokkeslæt kan du bruge de metoder og formater, der er beskrevet i følgende afsnit.

### <a name="picking-dates-from-the-calendar" />Vælge datoer i kalenderen

De felter, der viser et kalenderikon, kan angives ved hjælp af kalenderdatovælgeren. Aktiver kalenderikonet for at få vist kalenderdatovælgeren, eller vælge på <kbd>Ctrl</kbd>+<kbd>Home</kbd>-tastaturgenvejen i feltet.

![Datofelter.](media/ui-date-field.png "Eksempel på et datofelt")

Se også [Tastaturgenveje i kalenderdatovælgeren](keyboard-shortcuts.md#calendarshortcuts).

### <a name="day-week-year-pattern" />Mønsteret dag\-uge\-år

Du kan angive en dato som en ugedag efterfulgt af et ugenummer og eventuelt et år. F.eks. betyder Man25 eller man25 mandag i uge 25. Hvis du ikke angiver et år, bruges året fra arbejdsdatoen.

I stedet for at skrive hele ordet for den pågældende dag i ugen kan du skrive en del af ordet fra begyndelsen. Hvis der var konflikter (f.eks. med t, som kan være tirsdag eller torsdag), vurderes dagene i overensstemmelse med indstillingen for land/område. Input vurderes først mod arbejdsdag samt dags dato, som du vil bevare til forkortelser. F.eks. betyder _d_ allerede dags dato, så det ikke kan betyde tirsdag eller torsdag.

Ugenummereringen er altid ISO 8601, hvor er uge 1 uge er den uge, som 4. januar indgår i, eller ugen med den første torsdag i året.

### <a name="digit-patterns" />Talmønstre

I et datofelt kan du indtaste to, fire, seks eller otte cifre:

- Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.

- Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen. Rækkefølgen af dagen og måneden bestemmes af dine områdeindstillinger. Selvom områdeindstillingerne har året før dagen og måneden, fortolkes fire tal som dagen og måneden.

- Hvis datoen falder inden for 01-01-1950 og 31-12-2049, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.

  > [!NOTE]
  > Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, kan det tocifrede årstal være forskelligt. Administratorer kan ændre området ved at ændre indstillingen **CalendarTwoDigitYearMax** for [!INCLUDE[prod_short](includes/prod_short.md)]-serveren. Du kan finde flere oplysninger under [Konfiguration af Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).
 
### <a name="today" />I dag

Indtast ordet for _i dag_, på det sprog, der er angivet på siden **Mine indstillinger**, for at angive datoen på en post til dags dato. I stedet for at skrive hele ordet kan du skrive en del af ordet fra begyndelsen. Du kan f. eks. skrive _t_ eller _tor_, så længe det ikke også er starten på et andet ord.

### <a name="period" />Periode

For at filtrere på en bestemt regnskabsperiode skal du i et datofelt skrive bogstavet p eller ordet periode efterfulgt af et tal, der identificerer regnskabsperioden, f.eks. p2 eller periode4. Regnskabsperioden passer til regnskabsåret for den aktuelle arbejdsdato, der er angivet i dit rollecenter. Hvis arbejdsdatoen f.eks. er **21-03-22**, så filtrerer _p1_, eller bare _p_, på den første regnskabsperiode i regnskabsåret 2022 (f.eks. 01-01-22...01-31-22). _p15_ filtrerer på den 15 regnskabsperiode fra starten af regnskabsåret 2022 (f.eks. 01-03-23..31-03-23).

Regnskabsperioden defineres på siden **Regnskabsperioder**. Hvis du vil se eller ændre regnskabsperioderne, skal du åbne siden [her](https://businesscentral.dynamics.com/?page=100).

### <a name="work-date" />Arbejdsdato

Brug en arbejdsdato til at angive en dato, der ikke er dags dato på poster. En arbejdsdato er f. eks. nyttig, når du skal angive en bestemt dato for flere poster. Du kan angive arbejdsdatoen på siden **Mine indstillinger**. 

En hurtig måde at indtaste arbejdsdatoen på i posterne er at indtaste noget af eller hele ordet _arbejde_, startende fra begyndelsen af ordet, på det sprog, du bruger [!INCLUDE[prod_short](includes/prod_long.md)]. Du kan f. eks. indtaste _a_ eller _arbejde_. Sproget er også angivet på siden **Indstillinger**.

Hvis du ikke har angivet en arbejdsdato, bruges dags dato. Se også [Ændre grundlæggende indstillinger, f.eks. arbejdsdatoen](ui-change-basic-settings.md#work-date).

### <a name="closing-date" />Ultimodato

Ved afslutning af et regnskabsår kan du bruge ultimodatoer til at angive, at posten er en ultimopost. I teknisk forstand er en ultimodato en hvilken som helst dato mellem to datoer, f.eks. 31. december og 1. januar.

Hvis en dato skal være en ultimodato, skal du indsætte et U lige foran datoen, f.eks. U120131. Brug dette format sammen med alle datomønstre.

### <a name="examples" />Eksempler

Følgende tabel indeholder eksempler på datoer i alle formater. Det forudsætter indstillinger for land/område, der formaterer datoer i henhold til: **år.måned.dag.**, en uge, der begynder om mandagen, og hvor sproget er engelsk.

|**Post**      |**Fortolkning**      |
|---------------|------------------------|
|2022.12.31.|2022.12.31.|
|221231|2022.12.31.|
|22.12.31.|2022.12.31.|
|22.12.31.|2022.12.31.|
|20221231|2022.12.31.|
|22/12,31|2022.12.31.|
|11|arbejdsdatoår.abejdsdatomåned.11.|
|1112|arbejdsdatoår.11.12.|
|d eller dags dato|dags dato|
|p4|datointerval, der indeholder den fjerde regnskabsperiode, f.eks. 01-04-20..30-04-20|
|a eller arbejdsdato|arbejdsdatoen|
|m eller mandag|Mandag i ugen for arbejdsdatoen|
|ti eller tirsdag|Tirsdag i ugen for arbejdsdatoen|
|lø eller lørdag|Lørdag i ugen for arbejdsdatoen|
|s eller søndag|Søndag i ugen for arbejdsdatoen|
|ti23|Tirsdag i uge 23 i året for arbejdsdatoen|
|ti 23|Tirsdag i uge 23 i året for arbejdsdatoen|
|ti-1|Tirsdag i uge 1 i året for arbejdsdatoen|

## <a name="a-namebkmksettingdaterangesa-setting-ranges" /><a name="BKMK_SettingDateRanges"></a> Angive intervaller

På lister, i totaler og rapporter kan angive filtre for datoer, klokkeslæt og dato/klokkeslæt, der indeholder en startværdi og eventuelt en slutværdi for kun at få vist dataene i det pågældende interval. Standardreglerne gælder for den måde, du angiver datointervaller på.

|**Betydning**|**Eksempeludtryk (dato)**|**Data, der indgår i filteret**|
|-----------|---------------------|--------------------|
|Interval|15-12-00..15-01-01<br /><br />..15-12-00<br /><br />p1..p4|Records med datoer fra og med 15-12-00 til og med 15-01-01.<br /><br />Records med datoen 15 12 00 eller tidligere.<br /><br />Datointerval, der indeholder den anden, tredje og fjerde regnskabsperiode, f.eks. 01-01-20--30-04-20.|
|Enten/ eller|15 12 00\|16 12 00|Records med datoen 15 12 00 eller 16 12 00. Hvis der er poster med datoer på begge dage, vises de alle.|
|Kombination|15 12 00\|01 12 00..10 12 00  <br /><br />..14 12 00\|30 12 00..|Records med datoerne 15-12-00 eller poster fra og med 01-12-00 til og med 10-12-00.  <br /><br />Records med datoer den 14-12-00 eller tidligere eller den 30-12-00 eller senere, dvs. alle records, undtagen dokumenter med datoer fra og med 15-12-00 til og med 29-12-00.|

Du kan bruge de gyldige formater i datointervalfiltre. F.eks. resulterer man14 03..d 16, der anvendes på et dato og klokkeslætsfelt, i et filter fra kl. 3 mandag i uge 14 for den igangværende arbejdsdatos år, begge inklusive, indtil i dag kl. 16 inklusive.

## <a name="use-date-formulas" />Bruge dataformularer

En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes. Du kan angive datoformler i forskellige datoberegningsfelter eller filtre.

> [!NOTE]
> I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter. Tilsvarende, hvis du f.eks. indtaster 1U, så er perioden faktisk otte dage, fordi i dag er inkluderet. Du skal indtaste 6D eller 1U-1D for at angive en periode på syv dage \(en rigtig uge\), der medtager periodens startdato.

Her følger et par eksempler på brugen af datoformler:

- Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.

- Datoformlen i feltet **Respitperiode** for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen \(eller fra datoen for den forrige rykker\), før der oprettes en rykker.

- Datoformlen i feltet **Forfaldsdatoformel** afgør, hvordan forfaldsdatoen på rykkeren beregnes.

Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver). Du kan bruge følgende bogstaver som forkortelser for kalenderenheder.

|  Bogstav  |  Betyder  |
|----------|----------------------|
|L|Løbende|
|D|Dag\(e\)|
|U|Uge\(r\)|
|M|Måned\(er\)|
|K|Kvartal\(er\)|
|Å|År\(\)|

Datoformlen kan opbygges på tre måder.

Følgende eksempel viser, hvordan du skal bruge A for aktuel og en tidsenhed.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|LU|Løbende uge|
|LM|Løbende måned|

Følgende eksempel viser, hvordan du skal bruge et tal og en tidsenhed. Tallet må ikke være større end 9999.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|10D|10 dage fra i dag|
|2U|2 uger fra i dag|

Følgende eksempel viser, hvordan du skal bruge en tidsenhed og et tal.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|D10|Den næste 10. dage i en måned|
|UD4|Den næste 4. dag i en uge \(torsdag\)|

Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|LM+10D|Løbende måned \+ 10 dage|

Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|-1Å|1 år siden fra i dag|

> [!IMPORTANT]
> Hvis lokationen bruger en basiskalender, fortolkes den datoformel, du f.eks. indtaster i feltet **Transporttid**, i overensstemmelse med kalenderens arbejdsdage. For eksempel betyder 1U syv arbejdsdage.
<!--
# <a name="entering-date-ranges" />Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list.](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## <a name="use-date-formulas" />Use Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
> In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

- The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

- The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

- The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
> If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times" />Angive klokkeslæt

Når du angiver klokkeslæt, kan du indsætte en vilkårlige separatorer uden mellemrum mellem tidsenhederne. Hvis du bruger dobbelte tal for hver enhed op til millisekunder, er det ikke nødvendigt.

Du behøver kun at skrive de største enheder, du vil behøver, de øvrige indstilles til nul. Du kan også udelade AM/PM-symboler.

I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes. Det forudsætter indstillinger for land/område, der formaterer tidspunkter i overensstemmelse med: **Timer:Minutter:Sekunder.Millisekunder.** og bruger AM og PM-symbolerne 'AM' og 'PM hhv.

|**Post**      |**Fortolkning**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05:00:00|
|5AM|05:00:00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05:30:00|
|0530|05:30:00|
|5:30:5|05:30:05|
|053005|05:30:05|
|5:30:5.50|05:30:05,5|
|053005050|05:30:05.05|

> [!NOTE]
> Millisekunder fortolkes som decimalformat. Altså betyder f.eks. 3, 30 og 300 alle 300 millisekunder, mens 03 betyder 30 og 003 betyder 3 millisekunder.

> [!IMPORTANT]
> Du kan ikke bruge 24:00 til at angive midnat eller bruge værdier større end 24:00.

Ordet for 'time" på det sprog, som [!INCLUDE[prod_short](includes/prod_long.md)] bruger, vurderes til det aktuelle tidspunkt på din computer eller en mobilenhed. Du kan angive en del af ordet fra begyndelsen, f.eks. t eller TIM.

## <a name="entering-combined-dates-and-times" />Indtastning af kombineret dato/klokkeslæt

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration" />Angivelse af varighed

Nogle felter i programmet repræsenterer en varighed eller et forløbet tidsrum i stedet for en bestemt dato eller klokkeslæt. Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.

Her er nogle eksempler.

|**Varighed**|**Enhed**|
|------------|-------------------|
|2t|2 timer|
|6t 30 m|6 timer 30 min|
|6,5t|6 timer 30 min|
|90m|1 time 30 min|
|2d 6t 30m|2 dage 6 timer 30 min|
|2d 6t 30m 56s 600ms|2 dage 6 timer 30 min 56 sek 600 msek|

Du kan også skrive et tal, der automatisk konverteres til en varighed. Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.

Hvis du vil se, hvilken måleenhed der bruges i feltet varighed, skal du skrive et tal. Derefter kan du se, hvilken måleenhed, den konverteres til.

Hvis måleenheden f.eks. er timer, konverteres tallet 5 til 5 timer.

## <a name="see-related-microsoft-trainingtrainingmodulesexplore-modify-info-dynamics-365-business-central" />Se relateret [Microsoft-træning](/training/modules/explore-modify-info-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Arbejd med [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md)  
[Indtaste kriterier i filtre](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
