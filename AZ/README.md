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