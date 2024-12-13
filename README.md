# GUBIC_data
List of non-native plant species in urban areas across the world.

This repository has two files:

- `gubic_list_per_city.csv`: List of non-native species for 553 urban centers (`ID_HDC_G0_2`) across the world.
    -  `ID_HDC_G0_2`: Urban center ID according to [GHSL](https://human-settlement.emergency.copernicus.eu/ghs_stat_ucdb2015mt_r2019a.php)
    -  `accepted_taxon_name_binomial`: Accepted name as binomial names according to [WVCP](https://powo.science.kew.org/about-wcvp)
    -  `genus`: Genus name
    -  `family`: Family name
    -  `status_glonaf`: Plant status (naturalized and/or invasive) according to [GloNAF](https://glonaf.org/)
    -  `status_gbif`: Plant status (naturalized and/or invasive) according to [GBIF](https://www.gbif.org/) as most records were from GBIF
    -  `status_glonaf_gbif`: The combination of status based on `status_glonaf` and `status_gbif`. If any of the above two status indicated a species is non-native in a urban centre, the value of this column will be 'naturalized'
    -  `sources`: The data source: 'GUBIC' (data from data contribotrs or literature), 'GBIF' (data from GBIF records), or 'GBIF, GUBIC' (data from both)
    -  `n_records_buffer_5km`: If the data source is 'GBIF', we also looked at a 5-km buffer zone around the urban center, and calculated the number of GBIF records of this species within that buffer zone area
    -  `n_records_urban`: If the data source is 'GBIF', we calculated the number of GBIF records of this species within that urban center area
- `urban_centres`: A folder of shapefiles of urban centers in `gubic_list_per_city.csv`
    -  `ID_HDC_G0_2`: Same as those in `gubic_list_per_city.csv`
    -  `NAME_MAIN`: Main city name
    -  `city`: Main city name
    -  `name_long`: All city names that were included in this urban center, as some of them included multiple cities (some of them even crossed country boundaries)
    -  The rest columns are straightforward and can be found in the documentaiton of [GHSL](https://human-settlement.emergency.copernicus.eu/ghs_stat_ucdb2015mt_r2019a.php)
