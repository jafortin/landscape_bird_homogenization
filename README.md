# landscape_bird_homogenization
Processed data and analysis for paper on landscape and bird population homogenization using Mountain Legacy Project photograph pairs



## Summary

This project studies landscape and bird diversity change in a mountainous area (the Willmore Wilderness Park in Alberta, Canada) over the last century.

We have data on past and current land cover composition (historic and repeat photos & their land cover classifications). 
The 10 land cover categories are: Coniferous forest, Broadleaf forest, Mixedwood forest, Wetland, Shrub, Herbaceous, Rock, Water, Regenerating area, Snow/Ice.

We have species distribution models (made from auditory survey data and Landsat-based land cover map). 
The 15 bird species are: American pipit, American robin, Chipping sparrow, Dark-eyed junco, Golden-crowned kinglet, Golden-crowned sparrow, Gray jay, Hermit thrush, Pine siskin, Ruby-crowned kinglet, Savannah sparrow, Swainson's thrush, Varied thrush, Wilson's warbler, Yellow-rumped warbler.



## Data

The data is split into two folders:

- RawData
  - *Birddata.xls* contains the expert transcription of bird survey recordings
  - *LandCoverClassifications.zip* contains the land cover classifications of those photographs
  - *LandsatBasedClassifiedMap.tif* contains the Landsat-based classified map used to generate the species distribution models
  - *LandsatBasedClassifiedMapClasses.txt* is the legend for the Landsat-based raster
  - *Photographs.zip* contains the 46 photograph pairs as found on the [Mountain Legacy Project website](explore.mountainlegacy.ca)
- ProcessedData
  - *assessment-table-full.xlsx* is external data downloaded from [NABCI's State of North America's Birds 2016 Report](https://www.stateofthebirds.org/2016/resources/species-assessments/) which lists breeding habitat, non-breeding habitat and level of conservation concern for various bird species
  - *ImageAnalysis.xlsx* is a summary of the processed data from *LandCoverClassifications.zip* as well as the backtransformations from the species distribution models. It contains both land cover proportions in the photograph pairs as well as bird occurrence probabilities at each site
  - *ImageAnalysis_SensitivityAnalysis_MinusSE.xlsx* and *ImageAnalysis_SensitivityAnalysis_PlusSE.xlsx* are the same as *ImageAnalysis.xlsx* except that the values are generated using the species distribution model's beta-coefficients minus the standard error, and plus the standard error, respectively, to be used for sensitivity analysis
  - *LandcoverLookup.csv* is a lookup table for the different land cover category codes
  - *SpeciesLookup.csv* is a lookup table for the different bird species codes



## Code

- BirdDiversityAnalysis.Rmd
  - This file walks through the code that analyzes land cover and bird diversity change
  - This file also generates the figures in the associated publication
  - The pdf is the knitted (formatted) output of this Rmd file
