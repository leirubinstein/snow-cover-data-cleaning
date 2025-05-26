# Snow Cover Data Cleaning

*Data in this repository houses a cleaned version of the Arctic Shorebird Demographics Network's snow survey data. This repository was produced for [EDS 213: Databases & Data Management](https://ucsb-library-research-data-services.github.io/bren-eds213/) as a part of the Bren School's Master of Environmental Data Science program.*

## Background

[**Arctic Shorebird Demographics Network**](https://doi.org/10.18739/A2222R68W), hosted by the [NSF Arctic Data Center](https://arcticdata.io) data repository.

Field data on shorebird ecology and environmental conditions were collected from 1993-2014 at 16 field sites in Alaska, Canada, and Russia.

![Shorebird, copyright NYT](https://static01.nyt.com/images/2017/09/10/nyregion/10NATURE1/10NATURE1-superJumbo.jpg?quality=75&auto=webp)

Data were not collected every year at all sites. Studies of the population ecology of these birds included nest-monitoring to determine the timing of reproduction and reproductive success; live capture of birds to collect blood samples, feathers, and fecal samples for investigations of population structure and pathogens; banding of birds to determine annual survival rates; resighting of color-banded birds to determine space use and site fidelity; and use of light-sensitive geolocators to investigate migratory movements. 

Data on climatic conditions, prey abundance, and predators were also collected. Environmental data included weather stations that recorded daily climatic conditions, surveys of seasonal snowmelt, weekly sampling of terrestrial and aquatic invertebrates that are prey of shorebirds, live trapping of small mammals (alternate prey for shorebird predators), and daily counts of potential predators (jaegers, falcons, foxes). Detailed field methods for each year are available in the `ASDN_protocol_201X.pdf` files. All research was conducted under permits from relevant federal, state, and university authorities.

See `01_ASDN_Readme.txt` provided in the repository for full metadata information about this data set.

## Data & File Overview

### File list

The following datasets were used for the purposes of this analysis:
- `ASDN_Snow_survey.csv`
- `all_cover_fixed_LEILANIE_RUBINSTEIN.csv`

### File Relationships

```
📦 
├─ .gitignore
├─ LICENSE
├─ README.md
├─ data
│  ├─ processed
│  │  ├─ all_cover_fixed_LEILANIE_RUBINSTEIN.csv
│  │  └─ snow_cover.csv
│  └─ raw
│     └─ ASDN_Snow_survey.csv
├─ eds213_data_cleaning_assign_LEILANIE_RUBINSTEIN.qmd
└─ snow-cover-data-cleaning.Rproj
```

### Additional Related Data

Additional related data files are available on the ASDN page at 
the NSF Arctic Data Center (https://arcticdata.io). Each file is a .csv file with prefix "ASDN_":

	- Bird_captures
	- Bird_eggs
	- Bird_nests
	- Bird_resights
	- Bird_sexes
	- Camp_info
	- Camp_staff
	- Daily_pred_lemm
	- Daily_species_effort
	- Geodata
	- Invert_biomass
	- Lemming_counts
	- Lemming_nests
	- Lemming_trap
	- Pred_nests
	- Pred_point_counts
	- Study_Plot	(KMZ file)
	- Surface_water
	- Weather_HOBO
	- Weather_precip_manual
	- Weather_snow_manual

### Other versions

`all_cover_fixed_LEILANIE_RUBINSTEIN.csv` is a modified and cleaned version of `ASDN_Snow_Survey.csv`. 

## Data-specific Information

Data specific information for `all_cover_fixed_LEILANIE_RUBINSTEIN.csv`

### Number of variables

There are 11 variables in the processed snow cover data.

### Number of cases/rows

There are 42830 observations in the processed snow cover data.

### Variable List

| **Variable Name** | **Description**                                                   | **Units/Values**                                             |
|-------------------|-------------------------------------------------------------------|--------------------------------------------------------------|
| Site              | Four-letter code of site at which data were collected             | chr; 16 field sites in Alaska, Canada, and Russia            |
| Year              | Year in which data were collected                                 | num; Years 2003-2014                                         |
| Date              | Date on which data were collected                                 | chr; Dates June 6, 2003 - August 5, 2014 in DD-Mon-YY format |
| Plot              | Name of study plot on which survey was conducted                  | chr                                                          |
| Location          | Name of dedicated snow-survey location, if applicable             | chr                                                          |
| Snow_cover        | Percent cover of snow, including slush                            | num; Percentage                                              |
| Water_cover       | Percent cover of water                                            | num; Percentage                                              |
| Land_cover        | Percent cover of exposed land                                     | num; Percentage                                              |
| Total_cover       | Total sum (to check the above percents; should always sum to 100) | num; Percentage                                              |
| Observer          | Person who conducted the survey                                   | chr                                                          |
| Notes             | Any relevant comments on the survey                               | chr                                                          |

### Missing Data Codes

Missing data was coded as `NA` for all variables in the cleaned snow survey data.

### Specialized formats or other abbreviations

No specialized formats or abbreviations were used in the processed snow cover data.

## Sharing/Access Information

### License

This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.

### Links to publications that cite or use the data

Citations using the Arctic Shorebird Demographics Network (updated May 25, 2025):

- Chagnon‐Lafortune, A., Duchesne, É., Legagneux, P., McKinnon, L., Reneerkens, J., Casajus, N., Abraham, K. F., Bolduc, É., Brown, G. S., Brown, S. C., ... Joël. (2024). A circumpolar study unveils a positive non‐linear effect of temperature on arctic arthropod availability that may reduce the risk of warming‐induced trophic mismatch for breeding shorebirds. *Global Change Biology*, 30. [doi:10.1111/gcb.17356](https://doi.org/10.1111/gcb.17356)

- Perkins, M., Stenhouse, I. J., Lanctot, R. B., Brown, S., Bêty, J., Boldenow, M., Cunningham, J., English, W., Gates, R., Gilchrist, H. G., ... Niladri. (2023). Factors influencing mercury exposure in Arctic-breeding shorebirds. *Ecotoxicology*, 32, 1062–1083. [doi:10.1007/s10646-023-02708-w](https://doi.org/10.1007/s10646-023-02708-w)

- Lagassé, B. J., Lanctot, R. B., Brown, S., Dondua, A. G., Kendall, S., Latty, C. J., Liebezeit, J. R., Loktionov, E. Y., Maslovsky, K. S., Matsyna, A. I., ... Michael B. (2022). Migratory network reveals unique spatial-temporal migration dynamics of Dunlin subspecies along the East Asian-Australasian Flyway. *PLOS ONE*, 17, e0270957. [doi:10.1371/journal.pone.0270957](https://doi.org/10.1371/journal.pone.0270957)

- Küpper, C., Cruz-López, M., Lozano-Angulo, L., Gómez del Ángel, S., Rojas-Abreu, W., Bucio-Pacheco, M., & Eberhart-Phillips, L. (2021). Reply to 'Commentary CeutaOPEN, individual-based field observations of breeding snowy plovers Charadrius nivosus'. [doi:10.32942/osf.io/uqnvf](https://doi.org/10.32942/osf.io/uqnvf)

- Weiser, E. L., Lanctot, R. B., Brown, S. C., Gates, H. R., Bêty, J., Boldenow, M. L., Brook, R. W., Brown, G. S., English, W. B., Flemming, S. A., Franks, S. E., Gilchrist, H. G., Giroux, M.-A., Johnson, A., Kendall, S., Kennedy, L. V., Koloski, L., Kwon, E., Lamarre, J.-F., Lank, D. B., ... Sandercock, B. K. (2020). Annual adult survival drives trends in Arctic-breeding shorebirds but knowledge gaps in other vital rates remain. *The Condor*, 122. [doi:10.1093/condor/duaa026](https://doi.org/10.1093/condor/duaa026)

- Lagassé, B. J., Lanctot, R. B., Barter, M., Brown, S., Chiang, C.-Y., Choi, C.-Y., Gerasimov, Y. N., Kendall, S., Liebezeit, J. R., Maslovsky, K. S., ... Michael B. (2020). Dunlin subspecies exhibit regional segregation and high site fidelity along the East Asian–Australasian Flyway. *The Condor*, 122. [doi:10.1093/condor/duaa054](https://doi.org/10.1093/condor/duaa054)

- Eberhart-Phillips, L. J., Cruz-López, M., Lozano-Angulo, L., del Ángel, S. G., Rojas-Abreu, W., Bucio-Pacheco, M., & Küpper, C. (2020). CeutaOPEN, individual-based field observations of breeding snowy plovers Charadrius nivosus. *Scientific Data*, 7. [doi:10.1038/s41597-020-0490-y](https://doi.org/10.1038/s41597-020-0490-y)

- Weiser, E. L., Lanctot, R. B., Brown, S. C., Gates, H. R., Bentzen, R. L., Boldenow, M. L., Cunningham, J. A., Doll, A., Donnelly, T. F., English, W. B., ... Sandercock, B. K. (2018). Effects of leg flags on nest survival of four species of Arctic‐breeding shorebirds. *Journal of Field Ornithology*, 89, 287–297. [doi:10.1111/jofo.12264](https://doi.org/10.1111/jofo.12264)

- Weiser, E. L., Brown, S. C., Lanctot, R. B., Gates, H. R., Abraham, K. F., Bentzen, R. L., Bêty, J., Boldenow, M. L., Brook, R. W., Donnelly, T. F., ... Sandercock, B. K. (2018). Life‐history tradeoffs revealed by seasonal declines in reproductive traits of Arctic‐breeding shorebirds. *Journal of Avian Biology*, 49. [doi:10.1111/jav.01531](https://doi.org/10.1111/jav.01531)

- Weiser, E. L., Lanctot, R. B., Brown, S. C., Gates, H. R., Bentzen, R. L., Bêty, J., Boldenow, M. L., English, W. B., Franks, S. E., Koloski, L., ... Sandercock, B. K. (2018). Environmental and ecological conditions at Arctic breeding sites have limited effects on true survival rates of adult shorebirds. *The Auk*, 135, 29–43. [doi:10.1642/auk-17-107.1](https://doi.org/10.1642/auk-17-107.1)

- Weiser, E. L., Brown, S. C., Lanctot, R. B., Gates, H. R., Abraham, K. F., Bentzen, R. L., Bêty, J., Boldenow, M. L., Brook, R. W., Donnelly, T. F., ... Sandercock, B. K. (2018). Effects of environmental conditions on reproductive effort and nest success of Arctic‐breeding shorebirds. *Ibis*, 160, 608–623. [doi:10.1111/ibi.12571](https://doi.org/10.1111/ibi.12571)

- Kwon, E., English, W. B., Weiser, E. L., Franks, S. E., Hodkinson, D. J., Lank, D. B., & Sandercock, B. K. (2017). Delayed egg‐laying and shortened incubation duration of Arctic‐breeding shorebirds coincide with climate cooling. *Ecology and Evolution*, 8, 1339–1351. [doi:10.1002/ece3.3733](https://doi.org/10.1002/ece3.3733)

### Links to other publicly accessible locations of the data

Data is publicly accessible at:

1. [NSF Arctic Data Center](https://arcticdata.io/catalog/view/doi:10.18739/A2222R68W)
2. [DataONE](https://search.dataone.org/view/doi%3A10.18739%2FA2222R68W)

### Links/relationships to ancillary data sets

Not applicable.

### Data was derived from:

Data was derived from the bren-meds213-data-cleaning [repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-data-cleaning) and the [Arctic Shorebird Demographics Network](https://doi.org/10.18739/A2222R68W).

### Recommended citation

Please cite the original dataset housed by the Arctic Data Center:

Richard B. Lanctot, Stephen Brown, & Brett K. Sandercock. (2016). *Arctic Shorebird Demographics Network*. Arctic Data Center. [doi:10.18739/A2222R68W](https://doi.org/10.18739/A2222R68W).


