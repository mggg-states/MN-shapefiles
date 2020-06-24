# Minnesota Election Shapefile
These shapefiles along with election results were created by the Office of the Minnesota Secretary of State with additional processing by MGGG staff. They replace a
previous version of this data which can still be accessed in the [Archived](https://github.com/mggg-states/MN-shapefiles/tree/master/Archived) folder of this 
repository. This updated version includes absentee/mail-in ballots as well as correction of topology errors and precinct boundary errors by the Secretary of State's office.

## Sources
These precinct shapefiles with election results were created by the Minnesota Secretary of State's Election Division and downloaded from the [Minnesota Geospatial 
Commons](https://gisdata.mn.gov/dataset/bdry-electionresults-2012-2020). 2010 Decennial Census demographic data were downloaded from the 
[Census API](https://api.census.gov/data/2010/dec/sf1). The 2010 census block shapefile for Minnesota was downloaded from the US Census Bureau’s [TIGER/Line Shapefiles](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html).

## Processing
These shapefiles came with election data already joined and precincts assigned to districts. Demographic data were aggregated from the block level to precinct
using [MGGG’s proration software](https://github.com/mggg/maup). The MN12_18 file is the 2018 precinct boundaries with election data from 2012-2016 interpolated
onto the 2018 boundaries using the `maup` package with voting age population as the weight.

## Metadata
**2012 Precincts:**
*`VTD`: Voting tabulation district ID
*`PCTNAME`: Precinct name
*`PCTCODE`: Precinct code
*`MCDNAME`: Minor civil division name
*`MCDCODE`: Minor civil division code
*`CTU_TYPE`: Jurisdiction's governence (city, township, unorganized territory)
*`COUNTYNAME`: County name
*`COUNTYFIPS`: County FIPS code
*`CONGDIST`: Congressional district
*`MNSENDIST`: State Senate district
*`MNLEGDIST`: State House district
*`CTYCOMDIST`: County Commissioner district
*`JUDDIST`: Judicial District
*`TOTVOT12`: Total number of voters casting ballots in 2012
*`PRES12R`: Number of votes for 2012 Republican presidential candidate
*`PRES12D`: Number of votes for 2012 Democratic presidential candidate
*`PRES12L`: Number of votes for 2012 Libertarian presidential candidate
*`SEN12I`: Number of votes for 2012 Independent senate candidate
*`SEN12R`: Number of votes for 2012 Republican senate candidate
*`SEND12D`: Number of votes for 2012 Democratic senate candidate
*`USH12R`: Number of votes for 2012 Republican US House candidates
*`USH12D`: Number of votes for 2012 Democratic US House candidates
*`SSEN12I`: Number of votes for 2012 Independent state senate candidates
*`SSEN12R`: Number of votes for 2012 Republican state senate candidates
*`SSEN12D`:
*`SH12I`:
*`SH12R`:
*`SH12D`:
*`CA1YES12`:
*`CA1NO12`:
*`CA2YES12`:
*`CA2NO12`:
* `TOTPOP`: Total population 
* `NH_WHITE`: White, non-hispanic, population
* `NH_BLACK`: Black, non-hispanic, population
* `NH_AMIN`: American Indian and Alaska Native, non-hispanic, population
* `NH_ASIAN`: Asian, non-hispanic, population
* `NH_NHPI`: Native Hawaiian and Pacific Islander, non-hispanic, population
* `NH_OTHER`: Other race, non-hispanic, population
* `NH_2MORE`: Two or more races, non-hispanic, population
* `HISP`: Hispanic population
* `H_WHITE`: White, hispanic, population
* `H_BLACK`: Black, hispanic, population
* `H_AMIN`: American Indian and Alaska Native, hispanic, population
* `H_ASIAN`: Asian, hispanic, population
* `H_NHPI`: Native Hawaiian and Pacific Islander, hispanic, population
* `H_OTHER`: Other race, hispanic, population
* `H_2MORE`: Two or more races, hispanic, population
* `VAP`: Total voting age population
* `HVAP`: Hispanic voting age population
* `WVAP`: White, non-hispanic, voting age population
* `BVAP`: Black, non-hispanic, voting age population
* `AMINVAP`: American Indian and Alaska Native, non-hispanic, voting age population
* `ASIANVAP`: Asian, non-hispanic, voting age population
* `NHPIVAP`: Native Hawaiian and Pacific Islander, non-hispanic, voting age population
* `OTHERVAP`: Other race, non-hispanic, voting age population
* `2MOREVAP`: Two or more races, non-hispanic, voting age population

**2014 Precincts:**
*`VTDID`: Voting tabulation district ID
*`PCTNAME`: Precinct name
*`PCTCODE`: Precinct code
*`MCDNAME`: Minor civil division name
*`MCDCODE`: Minor civil division code
*`CTU_TYPE`: Jurisdiction's governence (city, township, unorganized territory)
*`COUNTYNAME`: County name
*`COUNTYFIPS`: County FIPS code
*`CONGDIST`: Congressional district
*`MNSENDIST`: State Senate district
*`MNLEGDIST`: State House district
*`CTYCOMDIST`: County Commissioner district
*`JUDDIST`: Judicial District
*`TOTVOT14`: Total number of voters casting ballots in 2014
*`SEN14I`:
*`SEN14D`:
*`SEN14L`:
*`USH14I`:
*`USH14R`:
*`USH14D`:
*`SH14I`:
*`SH14R`:
*`SH14D`:
*`GOV14I`:
*`GOV14R`:
*`GOV14D`:
*`SOS14I`:
*`SOS14R`:
*`SOS14D`:
*`AUD14I`:
*`AUD14R`:
*`AUD14D`:
*`AUD14L`:
*`AUD14LC`:
*`AG14I`:
*`AG14R`:
*`AG14D`:
*`AG14G`:
*`AG14L`:
*`AG14LM`:
* `TOTPOP`: Total population 
* `NH_WHITE`: White, non-hispanic, population
* `NH_BLACK`: Black, non-hispanic, population
* `NH_AMIN`: American Indian and Alaska Native, non-hispanic, population
* `NH_ASIAN`: Asian, non-hispanic, population
* `NH_NHPI`: Native Hawaiian and Pacific Islander, non-hispanic, population
* `NH_OTHER`: Other race, non-hispanic, population
* `NH_2MORE`: Two or more races, non-hispanic, population
* `HISP`: Hispanic population
* `H_WHITE`: White, hispanic, population
* `H_BLACK`: Black, hispanic, population
* `H_AMIN`: American Indian and Alaska Native, hispanic, population
* `H_ASIAN`: Asian, hispanic, population
* `H_NHPI`: Native Hawaiian and Pacific Islander, hispanic, population
* `H_OTHER`: Other race, hispanic, population
* `H_2MORE`: Two or more races, hispanic, population
* `VAP`: Total voting age population
* `HVAP`: Hispanic voting age population
* `WVAP`: White, non-hispanic, voting age population
* `BVAP`: Black, non-hispanic, voting age population
* `AMINVAP`: American Indian and Alaska Native, non-hispanic, voting age population
* `ASIANVAP`: Asian, non-hispanic, voting age population
* `NHPIVAP`: Native Hawaiian and Pacific Islander, non-hispanic, voting age population
* `OTHERVAP`: Other race, non-hispanic, voting age population
* `2MOREVAP`: Two or more races, non-hispanic, voting age population

**2016 Precincts:**
*`VTDID`: Voting tabulation district ID
*`PCTNAME`: Precinct name
*`PCTCODE`: Precinct code
*`MCDNAME`: Minor civil division name
*`MCDCODE`: Minor civil division code
*`CTU_TYPE`: Jurisdiction's governence (city, township, unorganized territory)
*`COUNTYNAME`: County name
*`COUNTYFIPS`: County FIPS code
*`CONGDIST`: Congressional district
*`MNSENDIST`: State Senate district
*`MNLEGDIST`: State House district
*`CTYCOMDIST`: County Commissioner district
*`JUDDIST`: Judicial District
*`TOTVOT16`: Total number of voters casting ballots in 2016

**2018 Precincts:**
*`VTDID`: Voting tabulation district ID
*`PCTNAME`: Precinct name
*`PCTCODE`: Precinct code
*`MCDNAME`: Minor civil division name
*`MCDCODE`: Minor civil division code
*`CTU_TYPE`: Jurisdiction's governence (city, township, unorganized territory)
*`COUNTYNAME`: County name
*`COUNTYFIPS`: County FIPS code
*`CONGDIST`: Congressional district
*`MNSENDIST`: State Senate district
*`MNLEGDIST`: State House district
*`CTYCOMDIST`: County Commissioner district
*`JUDDIST`: Judicial District
*`TOTVOT18`: Total number of voters casting ballots in 2018

## Projection
These shapefiles use a NAD83/UTM zone 15N projection (EPSG: 26915).

## Rating
We give these shapefiles an A rating. All data was obtained from the state government and was processed by MGGG staff.
