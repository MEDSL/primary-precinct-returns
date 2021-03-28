# 2016 and 2018 Primary Precinct Returns

This is the MEDSL repository for official precinct returns for 2016 and 2018 Primary Elections.

The `2018_precint_primary` and `2016_precint_primary` datasets contain precinct level primary election returns for all offices in 2018 and 2016. Users can download data by the level of office returns (president, US senate, US house, state, or local levels). For each state that is complete, users can also download all of the precinct-level returns separately in the folders above.

The returns are in progress, and will be updated periodically until completion. The following states and districts are included in the dataset:

## Alaska: 2018

Added 2020-05-25.

## Arizona: 2018

Added 2020-03-08.

## Connecticut: 2018

Added 2020-04-18.

## Delaware: 2018

Added 2020-08-04.

## District of Columbia: 2018

Added 2020-05-12.

## Florida: 2018

Added 2021-03-23. Local data not included at the moment.

We use the precinct level results from the Florida SOS website here: https://dos.myflorida.com/elections/data-statistics/elections-data/election-results-archive/ 

In a limited set of candidate-office-districts, the total vote counts in the precinct level data is off by a handful of votes (often only just 1 vote). Typically, this occurs when the electoral district is one that overlaps Seminole county (which includes all statewide offices or amendments), but not always. 

* Additionally, our vote totals for Circuit Judge 17th Circuit, Group 42 are off by more than one vote compared to the offical report online:
  - MICHAEL USAN votes: our data=114,021; online=114,095
  - RICHARD BRIAN KAPLAN votes: our data=113,690; online=113,722

## Hawaii: 2018

Added 2020-04-15.

## Kansas: 2018

Added 2020-07-12.

Some counties held primaries for the positions of Attorney General, State Treasurer, Commisioner of Insurance, as well as additional local elections. Even if some counties submitted election results for these (and some are available in the raw files), they were not included in the formatted data, as for the majority of counties these results were unavailable.

Johnson County did not submit district information for the candidates in its State House primaries. They were manually added by referencing the Secretary of State website [here](https://web.archive.org/web/20180809220344/https://ent.sos.ks.gov/kssos_ent.html) and [here](https://web.archive.org/web/20181211052726/https://ent.sos.ks.gov/kssos_ent.html)

Election returns for Shawnee and Wyandotte County were mostly submitted as scanned or OCR'd documents. They were manually transcribed to a format similar to the one submitted by Johnson County and can be found as `Shawnee.xlsx` and `Wyandotte.xlsx` in the `raw` folder. Each file lists the results of its county, one sheet per race.

Data for the Republican primaries for Secretary of State in Shawnee County was completely missing. Values of -1 were put for all candidates in all precincts for this race.

Data for the Democratic primaries for Governor/Lt. Governor in Wyandotte County was partially missing (namely the results for precints 0096 Kansas City 13-9 through 0113 Lake Quivira 1-1). Values of -1 were put for all candidates in these precincts for this race.

## Maryland: 2018

Added 2020-06-17.

## Massachusetts: 2018

Added 2020-05-04.

For Massachusetts 2016 and 2018 data, we create a unique precinct identifier ourselves, which makes use of precinct and ward numbers in the raw data. This takes the format of either "TOWN - WARD X - PCT Y", "TOWN - WARD X", or "TOWN - PCT Y", where TOWN is the town name, X is the ward number, and Y is the precinct number in the raw data.

## Minnesota: 2018

Added 2020-05-01.

## Montana: 2018

Added 2020-07-19.

## North Carolina: 2018

Added 2020-07-16.

There are a small number of discrepancies between the raw data and the election results posted [online](https://er.ncsbe.gov/?election_dt=05/08/2018&county_id=0&office=FED&contest=0), typically only by a few votes and for non-election day voting modes. These discrepancies are not corrected in our final cleaned data. You can find a list of the known discrepancies inside the North Carolina folder. 

## Nevada: 2018

Added 2020-04-19.

For Nevada 2018, there are "masked" vote totals (a voting report law states if in one office election mode there is a turnout of between 1 and 10, the vote totals are hidden--marked as '*' in the original file--to protect voter privacy). There are coded as a negative one (-1) in the cleaned data file's votes variable.

## Ohio: 2018

Added 2020-03-16.

For Ohio 2018, there are a few uncontested races where there is a major two party write in candidate that is not in the data.

## Oklahoma: 2018

Added 2021-02-09. Local offices not included at the moment.

## South Carolina: 2018

Added 2020-09-12. Local offices not included at the moment.

South Carolina raw data does not include absentee, provisional/failsafe, or "emergency" voting totals at the precinct-level. But they are included at the county level. We include the county-level votes for each of these different modes of voting for each election and candidate, but users should be wary when aggregating these totals.

Additionally, there is an issue with the Republican Questions 1 and 2 in 2018. The official online results are missing the county results for Charleston and Greenville, while we have these two counties' votes in our precinct level data. When I exclude Charleston and Greenville votes from our precinct level data and aggregate up, the results match the official online results (https://www.enr-scvotes.org/SC/75708/Web02-state.203322/#/cid/29505). 

## Tennessee: 2018

Added 2020-05-05.

For Tennessee 2018 data, we create a unique precinct identifier ourselves, which makes use of county precinct information in the raw data. This takes the format of "COUNTY - PCT X", where COUNTY is the county name field and X is the precinct label.

## Virginia: 2018

Added 2020-03-08.

## Wisconsin: 2018.

Added 2021-01-12. Local offices not included at the moment.

## Alabama: 2016

Added 2021-03-28. Local offices not included at the moment.

There are small discrepancies between the official online results posted on the SOS website (https://www.sos.alabama.gov/alabama-votes/voter/election-information/2016) and the raw precinct data provided by the SOS. 

Uncontested elections were not included in the raw data, and absentee and provisional votes were reported only at the county level.

## Alaska: 2016

Added 2020-06-01.

## Arizona: 2016

Added 2020-09-21. Local offices not included at the moment.

* The majority of counties have some sort of issue or observation labeled in this readme that affects all their offices and candidates or some other critical race statistics. For that reason, all records were marked with `readme_check` TRUE.

* The following offices indicated they were multivote offices. Such indications were removed for the cleaned data.

```
   county_name                                             office
0     COCONINO                               STATE HOUSE (VOTE FOR 2)
1     COCONINO                  CORPORATION COMMISSIONER (VOTE FOR 3)
2       LA PAZ                               STATE HOUSE (VOTE FOR 2)
3       LA PAZ                  CORPORATION COMMISSIONER (VOTE FOR 3)
4       LA PAZ             COUNCIL MEMBER TOWN OF PARKER (VOTE FOR 4)
5       LA PAZ         COUNCIL MEMBER TOWN OF QUARTZSITE (VOTE FOR 2)
6     MARICOPA                               STATE HOUSE (VOTE FOR 2)
7     MARICOPA                  CORPORATION COMMISSIONER (VOTE FOR 3)
8     MARICOPA           COUNCIL MEMBER CITY OF CHANDLER (VOTE FOR 3)
9     MARICOPA           COUNCIL MEMBER CITY OF AVONDALE (VOTE FOR 3)
10    MARICOPA    COUNCIL MEMBER CITY OF APACHE JUNCTION (VOTE FOR 3)
11    MARICOPA            COUNCIL MEMBER TOWN OF GILBERT (VOTE FOR 2)
12    MARICOPA                PRECINCT COMMITTEEMEN 0026 (VOTE FOR 9)
13    MARICOPA               PRECINCT COMMITTEEMEN 0041 (VOTE FOR 13)
14    MARICOPA                PRECINCT COMMITTEEMEN 0047 (VOTE FOR 9)
15    MARICOPA                PRECINCT COMMITTEEMEN 0072 (VOTE FOR 6)
16    MARICOPA                PRECINCT COMMITTEEMEN 0082 (VOTE FOR 7)
17    MARICOPA           COUNCIL MEMBER TOWN OF CAREFREE (VOTE FOR 6)
18    MARICOPA         COUNCIL MEMBER TOWN OF CAVE CREEK (VOTE FOR 6)
19    MARICOPA    COUNCIL MEMBER TOWN OF PARADISE VALLEY (VOTE FOR 3)
20    MARICOPA                PRECINCT COMMITTEEMEN 0108 (VOTE FOR 9)
21    MARICOPA               PRECINCT COMMITTEEMEN 0113 (VOTE FOR 11)
22    MARICOPA                PRECINCT COMMITTEEMEN 0116 (VOTE FOR 8)
23    MARICOPA               PRECINCT COMMITTEEMEN 0192 (VOTE FOR 13)
24    MARICOPA                PRECINCT COMMITTEEMEN 0200 (VOTE FOR 7)
25    MARICOPA          COUNCIL MEMBER CITY OF EL MIRAGE (VOTE FOR 3)
26    MARICOPA                PRECINCT COMMITTEEMEN 0210 (VOTE FOR 8)
27    MARICOPA                PRECINCT COMMITTEEMEN 0216 (VOTE FOR 5)
28    MARICOPA               PRECINCT COMMITTEEMEN 0228 (VOTE FOR 12)
29    MARICOPA     COUNCIL MEMBER TOWN OF FOUNTAIN HILLS (VOTE FOR 3)
30    MARICOPA               PRECINCT COMMITTEEMEN 0234 (VOTE FOR 10)
31    MARICOPA               PRECINCT COMMITTEEMEN 0245 (VOTE FOR 11)
32    MARICOPA               PRECINCT COMMITTEEMEN 0246 (VOTE FOR 17)
33    MARICOPA          COUNCIL MEMBER TOWN OF GILA BEND (VOTE FOR 3)
34    MARICOPA                PRECINCT COMMITTEEMEN 0253 (VOTE FOR 7)
35    MARICOPA               PRECINCT COMMITTEEMEN 0255 (VOTE FOR 19)
36    MARICOPA               PRECINCT COMMITTEEMEN 0257 (VOTE FOR 15)
37    MARICOPA          COUNCIL MEMBER TOWN OF GUADALUPE (VOTE FOR 3)
38    MARICOPA               PRECINCT COMMITTEEMEN 0331 (VOTE FOR 10)
39    MARICOPA               PRECINCT COMMITTEEMEN 0371 (VOTE FOR 11)
40    MARICOPA                PRECINCT COMMITTEEMEN 0386 (VOTE FOR 5)
41    MARICOPA               PRECINCT COMMITTEEMEN 0400 (VOTE FOR 19)
42    MARICOPA               PRECINCT COMMITTEEMEN 0405 (VOTE FOR 22)
43    MARICOPA               PRECINCT COMMITTEEMEN 0426 (VOTE FOR 12)
44    MARICOPA               PRECINCT COMMITTEEMEN 0431 (VOTE FOR 15)
45    MARICOPA                PRECINCT COMMITTEEMEN 0460 (VOTE FOR 4)
46    MARICOPA                PRECINCT COMMITTEEMEN 0487 (VOTE FOR 4)
47    MARICOPA        COUNCIL MEMBER TOWN OF QUEEN CREEK (VOTE FOR 3)
48    MARICOPA                PRECINCT COMMITTEEMEN 0520 (VOTE FOR 8)
49    MARICOPA               PRECINCT COMMITTEEMEN 0572 (VOTE FOR 10)
50    MARICOPA               PRECINCT COMMITTEEMEN 0611 (VOTE FOR 13)
51    MARICOPA               PRECINCT COMMITTEEMEN 0645 (VOTE FOR 11)
52    MARICOPA           COUNCIL MEMBER CITY OF TOLLESON (VOTE FOR 3)
53    MARICOPA               PRECINCT COMMITTEEMEN 0698 (VOTE FOR 11)
54    MARICOPA         COUNCIL MEMBER TOWN OF WICKENBURG (VOTE FOR 3)
55    MARICOPA    COUNCIL MEMBER CITY OF LITCHFIELD PARK (VOTE FOR 3)
56    MARICOPA                PRECINCT COMMITTEEMEN 0714 (VOTE FOR 5)
57    MARICOPA          COUNCIL MEMBER TOWN OF YOUNGTOWN (VOTE FOR 3)
58    MARICOPA                PRECINCT COMMITTEEMEN 0722 (VOTE FOR 7)
```

* The following counties do not report ballots cast per race but per election date. As a result, only one indication of BALLOTS CAST is present (in 'office': PRIMARY BALLOTS CAST):
  - Apache (only for Primary Election)
  - Cochise
  - Gila (only for Primary Election)
  - Graham
  - Greenlee
  - Maricopa
  - Mohave
  - Navajo
  - Pima
  - Pinal
  - Santa Cruz (only for Primary Election)

* Some race statistics in the office field are labeled as either PRESIDENTIAL or PRIMARY. These indications exist for registration and ballots cast as they may have differed between the presidential preference election and the primary election.

* Arizona has an open primary. Maricopa County reports counts for non-party voters that voted in the Democratic or Republican primary as DEMOCRAT-OTHER and REPUBLICAN-OTHER. Such counts are represented in the `party_detailed` for this county with these labels, so tallies for the Democrat and Republican party will only match official numbers if they are tallied with the other records.

* Some county reports include vote tallies for more modes than indicated in the format description given by the Secretary of State [here](https://apps.azsos.gov/results/2016/PPE/) and [here](https://apps.azsos.gov/results/2016/Primary/). Voting modes for the elections listed below were deduced by consulting county websites that broke results by mode and comparing vote totals. As a result, similarly named modes may not mean the same across counties. For all deductions, TOTAl was manually deduced by adding the other modes together.

  * Greenlee Primary: no such records found so the voting modes were labeled TOTAL, MODE 1, MODE 2, ..., MODE 9
  
  * Greenlee PPE: from https://www.co.greenlee.az.us/pdf/2016-03-22%20%202016%20PPE%20-%20Unofficial%20Results.pdf these modes were deduced: TOTAL, VOTE CENTER, EARLY 1, EARLY 2, PROVISIONAL 1, PROVISIONAL 2
  
  * Navajo Primary: from https://www.navajocountyaz.gov/Portals/0/Departments/Elections/Documents/Results/2016/Prec%20REport%20-%20Group%20Detail.pdf these modes were deduced: TOTAL, ELECTION DAY, EARLY, LATE EARLY, PROVISIONAL, CONDITIONAL PROVISIONAL
  
  * Navajo PPE: from https://www.navajocountyaz.gov/Portals/0/Departments/Elections/Documents/Results/2016/Official%20Election%20Summary%20w%20group%20detail.html these modes were deduced: TOTAL, ELECTION DAY, EARLY 1, EARLY 2, PROVISIONAL 1, PROVISIONAL 2
  
  * Pinal Primary: from https://acclaim.pinalcountyaz.gov/AcclaimWeb/Details/GetDocumentbyInstrumentNumber/DOC/2016-059988 these modes were deduced: TOTAL, EARLY, POLLING, PROVISIONAL, LATE EARLY
  
  * Pinal PPE: from  https://acclaim.pinalcountyaz.gov/AcclaimWeb/Details/GetDocumentbyInstrumentNumber/DOC/2016-019284 these modes were deduced: TOTAL, EARLY, POLLING, PROVISIONAL, LATE EARLY
  
  * Santa Cruz Primary: from https://www.santacruzcountyaz.gov/DocumentCenter/View/7022/August-30-2016-Primary-Election-Results these modes were deduced: TOTAL, ELECTION DAY, EARLY, PROVISIONAL, 200 EARLY

* A special election was held on May 17, 2016 on two propositions (see more [here](https://ballotpedia.org/Arizona_Education_Finance_Amendment,_Proposition_123_(May_2016)) and [here](https://ballotpedia.org/Arizona_Public_Retirement_Benefits_Amendment,_Proposition_124_(May_2016)). The Arizona Secretary of State website provided results broken down by precinct for some counties (and are available in the Special folder), but results for Cochise, La Paz, Mohave and Santa Cruz were completely missing. As a result, the results from this special election were not added to the cleaned data.

* The following counties did not provide voter registration by party to the precinct level
  - Graham (only aggregated voter registration by precinct available)
  - Yavapai
  
* Due to not all precincts reporting nonpartisan elections in them, nonpartisan/other primary registration is undercounted for the following counties:
  - Coconino
  - La Paz
  - Yuma
  
* Due to nonpartisan ballots seemingly not being tallied in their official count, primary ballots cast are overcounted for the following counties
  - Cochise
  
* Coconino and Yavapai added numerical identifiers to their writein candidate records. These numerical identifiers when removed could still uniquely identify the writein record by county, party and office, so they were removed for the cleaned data.
 
* The following races seems to have inconsistent numbers of ballots cast for these primary elections (which are also reflected in the raw data as well as the county website)
  - Coconino Democrat US House/US Senate: 12445 ballots cast; every other Democrat primary: 12444 ballots cast. See [here](https://www.coconino.az.gov/DocumentCenter/View/13164/GEMS-SOVC-REPORT-FINAL?bidId=)
  - Coconino Republican US House/US Senate: 8897 ballots cast; every other Republican primary: 8895 ballots cast. See [here](https://www.coconino.az.gov/DocumentCenter/View/13164/GEMS-SOVC-REPORT-FINAL?bidId=)
  - Yuma Democrat US House/US Senate: 7544 ballots cast; every other Democrat primary: 7540 ballots cast.
  - Yuma Green US House/US Senate: 17 ballots cast; every other Green primary: 16 ballots cast.
  
* District is reported for congressional-level presidential preference election results, given that districts are distinct from the statewide primary. The district races supply a different set of votes from the statewide election, where one can win these unique delegates through a substate-focused campaign, akin to the electoral college and the popular vote in the national general election.

## District of Columbia: 2016

Added 2020-05-13.

## Florida: 2016

Added 2021-03-18. Local offices not included at the moment.

We use the precinct level results from the Florida SOS website here: https://dos.myflorida.com/elections/data-statistics/elections-data/election-results-archive/ 

In a limited set of candidate-office-districts, the total vote counts in the precinct level data is off by a handful of votes (often only just 1 vote). Typically, this occurs when the electoral district is one that overlaps Seminole county (which includes all statewide offices or amendments), but not always. 

* The offices/districts/candidates with small discrepancies in the total votes are:
  - US House District 002, Steve Crapps
  - State House District 108, Henry Patel
  - State House District 114, Daisy J Baez
  - State House District 115, Ross Hancock
  - Circuit Judge 4th District Group 25, Gerald L Wilkerson
  - Circuit Judge 11th District Group 9, both candidates
  - Circuit Judge 11th District Group 66, both candidates
  - Circuit Judge 11th District Group 74, George "Jorge" A Sarduy
  - Circuit Judge 18th District Group 9, all candidates
  

## Hawaii: 2016

Added 2020-03-20.

## Massachusetts: 2016

Added 2020-04-27.

For Massachusetts 2016 and 2018 data, we create a unique precinct identifier ourselves, which makes use of precinct and ward numbers in the raw data. This takes the format of either "TOWN - WARD X - PCT Y", "TOWN - WARD X", or "TOWN - PCT Y", where TOWN is the town name, X is the ward number, and Y is the precinct number in the raw data.

A few candidates appear as running for the same office for multiple parties as write-ins. We believe this is a case of voters accidentally voting for these candidates as a write-in for a different party's primary election. All vote totals were kept as they are. These candidates are:

-Dean Tran ran for State House as Democrat write-in and Republican write-in

-James A Perelmann ran for Sheriff as Democrat and as a Republican write-in

-Jessica G Lambert ran for State House as Democrat and as United Independent write-in

-Joan Meschino ran for State House as a Democrat write-in and State Senate as a Democrat

-Marc Richard Rivers ran for Sheriff as a Democrat and as a Republican write-in

-Paulo C DeOliveira ran for Register of Deeds as Democrat and as a Republican write-in

-Robert Odgen ran for Sheriff as Democrat and as a Republican write-in

-Shaunna L O'Conell ran for State House as a Republican and as a Democrat write-in

-Shawn C. Dooley ran for State House as a Republican and as a Democrat write-in

-Stephen P Sandrelli ran for State House as a Democrat write-in and Republican write-in

## Minnesota: 2016

Added 2020-04-04.

## Montana: 2016

Added 2020-07-21.

## Nevada: 2016

Added 2020-05-02.

For Nevada 2016, there are "masked" vote totals (a voting report law states if in one office election mode there is a turnout of between 1 and 10, the vote totals are hidden--marked as '*' in the original file--to protect voter privacy). There are coded as a negative one (-1) in the cleaned data file's votes variable.

## Oklahoma: 2016

Added 2020-07-09.

## South Carolina: 2016

Added 2020-09-12. Local offices not included at the moment.

South Carolina raw data does not include absentee, provisional/failsafe, or "emergency" voting totals at the precinct-level. But they are included at the county level. We include the county-level votes for each of these different modes of voting for each election and candidate, but users should be wary when aggregating these totals.

## Virginia: 2016

Added 2020-03-08.

On March 4th, 2016, after the 2016 US Presidential Primaries, precinct “301 - Waterview” was merged with precinct “302 - Churchview” (see note on https://www.vpap.org/elections/precinct/3202). In some sets of official results, “301 - Waterview” has been dropped from the official aggregate totals for the Virginia US Presidential Primary, leading to a small discrepancy in vote totals. For example:
  - 301 - Waterview votes for 2016 Presidential Primaries included in these official results: https://historical.elections.virginia.gov/elections/search/year_from:2016/year_to:2016/stage:Primaries
  - 301 - Waterview votes for 2016 Presidential Primaries NOT included in these official results: https://results.elections.virginia.gov/vaelections/2016%20March%20Democratic%20Presidential%20Primary/Site/Locality/MIDDLESEX%20COUNTY/President.html
  
We have kept 301 - Waterview in our 2016 Presidential Primary data for the VA primaries.

## Washington: 2016

Added 2020-09-11. Local offices not included at the moment.

For Washington 2016, there are "masked" vote totals, marked as  '*' in the original file--to protect voter privacy. There are coded as a negative one (-1) in the cleaned data file's votes variable.

## West Virginia: 2016

Added 2020-09-04. Local offices not included at the moment.

There are two candidates for state senate with small discrepancies in the raw data relative to the official results online (found here: https://apps.sos.wv.gov/elections/results/results.aspx?year=2016&eid=22&county=Statewide).

1) DONNA J BOLEY, DELEGATE TO REPUBLICAN NATIONAL CONVENTION -- AT LARGE - the precinct level results for Monongalia County are missing in the raw data. There were 3,089 votes in this county for Donna J. Boley

2) DAN HILL, DELEGATE TO REPUBLICAN NATIONAL CONVENTION -- AT LARGE - all the county level vote counts match official reports online, but the total votes on the official website lists him as getting 62,227 when really it should be 60,253.

## Wisconsin: 2016

Added 2020-08-24. Local offices not included at the moment.

There are a small number of discrepancies between the raw data and the election results posted [online](https://elections.wi.gov/elections-voting/results/), typically only by a few votes and for non-election day voting modes. These discrepancies are not corrected in our final cleaned data. You can find a list of the known discrepancies inside the Wisconsin folder. 
