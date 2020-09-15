# ICPSR_FIPS
Correspondence between ICPSR and FIPS county codes

IMPORTANT: please read each of the columns as a string or character data structure as opposed to numeric data structures! Here, padded zeros matter, and can lead to faulty matching if not accounted for.

A combination of state and county FIPS or state and county ICPSR codes uniquely identify a US county. However, some datasets utilize the latter, some the former and others a mix of the two. I provided this mapping, found in "full_icp_fips_mapping.xlsx" so other researchers using census data don't have to code up their solutions. My procedure was, citing the ipums description on the COUNTYICP variable [page](https://usa.ipums.org/usa-action/variables/COUNTYICP#codes_section), 

"Correspondence with FIPS Codes:
Most ICPSR codes correspond to 3-digit FIPS codes (as identified by COUNTYFIP) followed by an added zero digit.

The only systematic discrepancies between ICPSR and FIPS codes occur in Maryland, where all FIPS codes of 009 and higher (excluding Baltimore City, which has FIPS code 510 and ICPSR code 5100) are shifted down by two in the ICPSR scheme. For example, Calvert County has FIPS code 009 and ICPSR code 0070.

In Nevada, Pershing County has FIPS code 027 and historical Ormsby County has FIPS code 025. In the ICSPR scheme, Pershing County has code 0250, and Ormsby County uses the Carson City county code of 0510. (Ormsby County was consolidated with Carson City in 1969.) The historical (1870) Rio Virgin County uses ICPSR county code 0270."


Finally, there are some counties with a ICP code ending with 5 or 7. In the words of [ipums](https://usa.ipums.org/usa/volii/ICPSR.shtml), are "Generally, if a county merged with another or was renamed before 1970, it receives a fourth digit of "5"". These counties can be found in "icpsrcnt_notEndingIn0.csv"
