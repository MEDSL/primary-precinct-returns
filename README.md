# 2016 and 2018 Primary Precinct Returns

This is the MEDSL repository for official precinct returns for 2016 and 2018 Primary Elections.

The `2018_precint_primary` and `2016_precint_primary` datasets contain precinct level primary election returns for all offices in 2018 and 2016. It is incomplete but will be updated periodically until completion. The following states and districts are included in the dataset:

## Arizona: 2018

Added 2020-03-08.

## Connecticut: 2018

Added 2020-04-18.

## Hawaii: 2018

Added 2020-04-15.

## Nevada: 2018

Added 2020-04-19.

For Nevada 2018, there are "masked" vote totals (a voting report law states if in one office election mode there is a turnout of between 1 and 10, the vote totals are hidden--marked as '*' in the original file--to protect voter privacy). There are coded as a negative one (-1) in the cleaned data file's votes variable.

## Ohio: 2018

Added 2020-03-16.

## Virginia: 2018

Added 2020-03-08.

## Hawaii: 2016

Added 2020-03-20.

## Massachusetts: 2016

Added 2020-04-27.

For Massachusetts 2016 and 2018 data, we create a unique precinct identifier ourselves, which makes use of precinct and ward numbers in the raw data. This takes the format of either "TOWN - WARD X - PCT Y", "TOWN - WARD X", or "TOWN - PCT Y", where TOWN is the town name, X is the ward number, and Y is the precinct number in the raw data.

## Minnesota: 2016

Added 2020-04-04.

## Virginia: 2016

Added 2020-03-08.

On March 4th, 2016, after the 2016 US Presidential Primaries, precinct “301 - Waterview” was merged with precinct “302 - Churchview” (see note on https://www.vpap.org/elections/precinct/3202). In some sets of official results, “301 - Waterview” has been dropped from the official aggregate totals for the Virginia US Presidential Primary, leading to a small discrepancy in vote totals. For example:
  - 301 - Waterview votes for 2016 Presidential Primaries included in these official results: https://historical.elections.virginia.gov/elections/search/year_from:2016/year_to:2016/stage:Primaries
  - 301 - Waterview votes for 2016 Presidential Primaries NOT included in these official results: https://results.elections.virginia.gov/vaelections/2016%20March%20Democratic%20Presidential%20Primary/Site/Locality/MIDDLESEX%20COUNTY/President.html
  
We have kept 301 - Waterview in our 2016 Presidential Primary data for the VA primaries.
