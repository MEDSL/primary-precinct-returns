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

## Tennessee: 2018

Added 2020-05-05.

For Tennessee 2018 data, we create a unique precinct identifier ourselves, which makes use of county precinct information in the raw data. This takes the format of "COUNTY - PCT X", where COUNTY is the county name field and X is the precinct label.

## Virginia: 2018

Added 2020-03-08.

## Alaska: 2016

Added 2020-06-01.

## District of Columbia: 2016

Added 2020-05-13.

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

## Virginia: 2016

Added 2020-03-08.

On March 4th, 2016, after the 2016 US Presidential Primaries, precinct “301 - Waterview” was merged with precinct “302 - Churchview” (see note on https://www.vpap.org/elections/precinct/3202). In some sets of official results, “301 - Waterview” has been dropped from the official aggregate totals for the Virginia US Presidential Primary, leading to a small discrepancy in vote totals. For example:
  - 301 - Waterview votes for 2016 Presidential Primaries included in these official results: https://historical.elections.virginia.gov/elections/search/year_from:2016/year_to:2016/stage:Primaries
  - 301 - Waterview votes for 2016 Presidential Primaries NOT included in these official results: https://results.elections.virginia.gov/vaelections/2016%20March%20Democratic%20Presidential%20Primary/Site/Locality/MIDDLESEX%20COUNTY/President.html
  
We have kept 301 - Waterview in our 2016 Presidential Primary data for the VA primaries.

## Washington: 2016

Added 2020-09-11.

For Washington 2016, there are "masked" vote totals, marked as  '*' in the original file--to protect voter privacy. There are coded as a negative one (-1) in the cleaned data file's votes variable.

## West Virginia: 2016

Added 2020-09-04.

There are two candidates for state senate with small discrepancies in the raw data relative to the official results online (found here: https://apps.sos.wv.gov/elections/results/results.aspx?year=2016&eid=22&county=Statewide).

1) DONNA J BOLEY, DELEGATE TO REPUBLICAN NATIONAL CONVENTION -- AT LARGE - the precinct level results for Monongalia County are missing in the raw data. There were 3,089 votes in this county for Donna J. Boley

2) DAN HILL, DELEGATE TO REPUBLICAN NATIONAL CONVENTION -- AT LARGE - all the county level vote counts match official reports online, but the total votes on the official website lists him as getting 62,227 when really it should be 60,253.

## Wisconsin: 2016

Added 2020-08-24.

There are a small number of discrepancies between the raw data and the election results posted [online](https://elections.wi.gov/elections-voting/results/), typically only by a few votes and for non-election day voting modes. These discrepancies are not corrected in our final cleaned data. You can find a list of the known discrepancies inside the Wisconsin folder. 
