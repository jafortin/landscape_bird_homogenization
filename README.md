# landscape_bird_homogenization
Processed data and analysis for paper on landscape and bird population homogenization using Mountain Legacy Project photograph pairs



## Summary

This project studies landscape and bird diversity change in a mountainous area (the Willmore Wilderness Park in Alberta, Canada) over the last century.

We have data on past and current land cover composition (historic and repeat photos & their land cover classifications). 
The 10 land cover categories are: Coniferous forest, Broadleaf forest, Mixedwood forest, Wetland, Shrub, Herbaceous, Rock, Water, Regenerating area, Snow/Ice.

We have species distribution models (made from auditory survey data and Landsat-based land cover map). 
The 13 bird species are: American pipit, American robin, Chipping sparrow, Dark-eyed junco, Golden-crowned kinglet, Golden-crowned sparrow, Gray jay, Hermit thrush, Pine siskin, Ruby-crowned kinglet, Savannah sparrow, Wilson's warbler, Yellow-rumped warbler.



## Data

The data is split into two folders:

- RawData
  - *Birddata.xls* contains the expert transcription of bird survey recordings
  - *LandCoverClassifications.zip* contains the land cover classifications of those photographs
  - *LandsatBasedClassifiedMap.tif* contains the Landsat-based classified map used to generate the species distribution models
  - *LandsatBasedClassifiedMapClasses.txt* is the legend for the Landsat-based raster
  - *Photographs.zip* contains the 46 photograph pairs as found on the [Mountain Legacy Project website](explore.mountainlegacy.ca)
- ProcessedData
  - *ImageAnalysis.xlsx* is a summary of the processed data from *LandCoverClassifications.zip* as well as the backtransformations from the species distribution models. It contains both land cover proportions in the photograph pairs as well as bird occurrence probabilities at each site

- Comparisons
  - *assessment-table-full.xlsx* is external data downloaded from [NABCI's State of North America's Birds 2016 Report](https://www.stateofthebirds.org/2016/resources/species-assessments/) which lists breeding habitat for various bird species
  - *ron_bbs_t20250405.csv* is external data downloaded from the [Government of Canada's website on the North American Breeding Bird Survey](https://wildlife-species.canada.ca/breeding-bird-survey-results/P004/A001/?lang=e&m=b&r=10&p=L) which lists long-term population trends for various bird species
- *LandcoverLookup.csv* is a lookup table for the different land cover category codes
- *SpeciesLookup.csv* is a lookup table for the different bird species codes



## Code

- BirdDiversityAnalysis.Rmd
  - This file walks through the code that analyzes land cover and bird diversity change
  - This file also generates the figures in the associated publication
  - The html is the knitted (formatted) output of this Rmd file
