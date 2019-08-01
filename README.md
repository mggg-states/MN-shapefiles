# Minnesota Election Shapefile
These shapefiles were obtained from the Minnesota Legislative Coordinating Commission GIS (LCC-GIS) Data Center and processed by members of the Metric Geometry and Gerrymandering Group (MGGG).

## Sources
The Minnesota precinct shapefiles with election results were created by the [Minnesota Secretary of State Election Division](https://www.sos.state.mn.us/elections-voting/) and obtained from the [Minnesota LCC-GIS](https://www.gis.leg.mn/html/download.html). 2010 Decennial Census demographic data were downloaded from the [Census API](https://api.census.gov/data/2010/dec/sf1). The 2010 census block shapefile for Minnesota was downloaded from the US Census Bureau’s [TIGER/Line Shapefiles](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html).

## Processing
The topology of the precinct shapefiles were repaired using the st_make_valid() function from the R package [lwgeom](https://github.com/r-spatial/lwgeom).  Demographic data was aggregated from the block level using [MGGG’s proration software](https://github.com/mggg/maup).

## Metadata
MN_2012 to MN_2016:
* `PCTNAME`: Precinct name
* `PCTCODE`: Precinct number (unique within county)
* `SHORTLABEL`: Abbreviated precinct name
* `COUNTYNAME`: County name
* `COUNTYCODE`: County number
* `CONGDIST`: US congressional district
* `MNSENDIST`: State senate district
* `MNLEGDIST`: State legislative district
* `CTYCOMDIST`: County commissioner district
* `JUDDIST`: Judicial district
* `SWCDIST`: Soil and water conservation district
* `PARKDIST`: Park district
* `HOSPDIST`: Hospital district
* `WARD`: City ward
* `TABSYSTEM`: Vote tabulating system
* `TABMODEL`: Vote tabulation equipment used for precinct
* `MAILBALLOT`: Precincts using mail balloting
* `REG7AM`: Number of voters registered in precinct as of 7AM on election day (pre-registered voters)
* `EDR`: Number of voters registering in the polling place on election day
* `SIGNATURES`: Number of people voting in person
* `REGMILOVAB`: Regular, and uniformed and overseas citizens absentee ballots accepted
* `FEDONLYAB`: Absentee ballots with federal offices only accepted (by citizens who are permanently or indefinately overseas)
* `PRESONLYAB`: Absentee ballots cast for president only (by people who moved out of Minnesota within 30 days of the election)
* `TOTVOTING`: Number of voters casting ballots
* `USPRSR`: US president Republican Party candidate votes
* `USPRSDFL`: US president Democratic-Farmer-Labor Party candidate votes
* `USPRSLIB`: US president Libertarian Party candidate votes
* `USPRSSWP`: US president Socialist Workers Party candidate votes
* `USPRSCP`: US president Constitution Party candidate votes
* `USPRSCG`: US president Constitutional Government Party candidate votes
* `USPRSGP`: US president Green Party candidate votes
* `USPRSGR`: US president Grassroots Party candidate votes
* `USPRSSL`: US president Socialism and Libertarian Party candidate votes
* `USPRSJP`: US president Justice Party candidate votes
* `USPRSWI`: US president write in candidate votes--includes registered and non-registered write-ins
* `USPRSTOTAL`: US president total votes
* `USSENIP`: US senator Independence Party candidate votes
* `USSENR`: US senator Republican Party candidate vote
* `USSENDFL`: US senator Democratic-Farmer-Labor Party candidate votes
* `USSENGR`: US senator Grassroots Party candidate votes
* `USSENMOP`: US senator Minnesota Open Progressives Party candidate votes
* `USSENWI`: US senator write in candidate votes--includes registered and non-registered write-ins
* `USSENTOTAL`: US senator total votes
* `USREPIP`: US representative Independence Party candidate votes
* `USREPR`: US representative Republican Party candidate votes
* `USREPDFL`: US representative Democratic-Farmer-Labor Party candidate votes
* `USREPWI`: US representative write in candidate votes--includes registered and non-registered write-ins
* `USREPTOTAL`: US representative total votes
* `MNSENIP`: MN senator Independence Party candidate votes
* `MNSENR`: MN senator Republican Party candidate votes
* `MNSENDFL`: MN senator Democratic-Farmer-Labor Party candidate votes
* `MNSENWI`: MN senator write in candidate votes--includes registered and non-registered write-ins
* `MNSENTOTAL`: MN senator total votes
* `MNLEGIP`: MN representative Independence Party candidate votes
* `MNLEGR`: MN representative Republican Party candidate votes
* `MNLEGDFL`: MN representative Democratic-Farmer-Labor Party candidate votes
* `MNLEGWI`: 	MN representative Write In candidate votes--includes registered and non-registered write-ins
* `MNLEGTOTAL`: MN representative total votes
* `MNCA1YES`: Constitutional Amendment 1 (Marriage) Yes votes
* `MNCA1NO`: Constitutional Amendment 1 (Marriage) No votes
* `MNCA1EST`: Constitutional Amendment 1 (Marriage) Estimated Blanks
* `MNCA1TOTAL`: Constitutional Amendment 1 (Marriage) Total votes (=TOTVOTING)
* `MNCA2YES`: Constitutional Amendment 2 (Voter ID) Yes votes
* `MNCA2NO`: Constitutional Amendment 2 (Voter ID) No votes
* `MNCA2EST`: Constitutional Amendment 2 (Voter ID) Estimated Blank
* `MNCA2TOTAL`: Constitutional Amendment 2 (Voter ID) Total votes (=TOTVOTING)
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


## Projection
These shapefiles use a NAD83/UTM zone 15N projection (EPSG: 26915).

## Rating
We give these shapefiles an A rating. All data was obtained from the state government and was processed by MGGG staff.
