## Code and data associated with manuscript:
# Biotic interactions structure zooplankton metacommunity dynamics following a summer heatwave

Patrick L. Thompson<sup>1</sup>, Coreen Forbes<sup>1</sup>, Joey R. Bernhardt<sup>1,2</sup>, Kaleigh E. Davis<sup>1</sup>, Keila A. Stark<sup>1</sup>, Evgeniya Yangel<sup>1</sup>, Felipe E. Amadeo<sup>1</sup>, Natalie E. Westwood<sup>1</sup>, Mary I. O'Connor<sup>1</sup>

<sup>1</sup>Biodiversity Research Center and the Department of Zoology, University of British Columbia, Vancouver, B.C., Canada  
<sup>2</sup>Department of Integrative Biology, University of Guelph, Guelph, Ontario, Canada

Corresponding author: patrick.thompson@zoology.ubc.ca  
Alternate contact: oconnor@zoology.ubc.ca  

# Abstract
Despite the key role of biotic interactions in structuring ecological communities, their influence is often overlooked in predictions of how communities respond to abiotic environmental change. Here, we present an experiment that tests hypotheses based on metacommunity theory about how abiotic responses, biotic interactions and dispersal jointly determine the response of ecological communities to abiotic perturbations. We established experimental zooplankton metacommunities that included a temperature gradient among local communities in each metacommunity. Metacommunities were exposed to one of three dispersal rate treatments. After four weeks, differences in community composition were explained by temperature and this spatial structure was strongest in metacommunities with lower rates of dispersal. A midsummer natural heatwave strongly shifted all communities toward heat tolerant taxa and when conditions cooled, communities diverged into compositional states that were no longer explained by experimental temperature and dispersal treatments. Although our experimental design did not allow us to directly assess the influence of biotic interactions, these results are consistent with the hypothesis that biotic interactions resulted in post-heatwave successional dynamics that prevented the reestablishment of pre-heatwave signatures of temperature on community composition. These results highlight the need to better account for the role of biotic interactions in the theories that guide our expectations for how ecological communities will respond to future abiotic environmental change.  

# Responsibilities  
All authors contributed to data collection. The code was written by Patrick Thompson.  
         
# Repository contents  
This repository consists of a data folder and a writing folder.  
The data folder contains two .RData files:  
1. zoop_data.Rdata - this contains two a data objects:  
* Zoop_data - this data frame the the counts (individuals per 10 L sampled) for each zooplankton taxa on each sampling date and mesocosm. Counts are in wide format with the taxa name as the column header. This data frame also includes the following date and treatment columns: dispersal (none, low, high), wattage (heater wattage), date (YYYY-MM-DD), week (week of the experiment), metacommunity (numeric ID), tank (numeric ID for mesocosm), and temp_mean (mean water temperature in the week prior to sampling).  
* all_temperature - this data frame includes daily temperature data collected using temperature loggers for the duration of the experiment. It includes the following columns: tank (numeric ID for mesocosm), data (YYYY-MM-DD), dispersal (none, low, high), wattage (heater wattage), metacommunity (numeric ID), temp_mean (mean temperature for the day), temp_max (max temperature for the day), temp_sd (standard deviation of temperature in the day), temp_min (min temperature in the day), dispersal_date (TRUE if dispersal was done on that day, NA if not).  
2. HMSC_m.RData - this data file contains the fitted HMSC model. This is not required to reproduce the analysis, but speeds up the generation of the RMarkdown file as it allows it to be produced without running the full HMSC analysis again. The  two lines that run the HMSC model and saves this file are included in the RMarkdown file, but are commented out.

The writing folder contains:
1. Manuscript.Rmd - an Rmarkdown file that runs the analysis and produces the manuscript pdf. All code required to produce the manuscript is included in this file.
2. plt_plot_theme.R - an R script that defines the plotting theme used in the report.
3. TEAMM_Zoop.bib - a .bib file that includes all of the citations for the manuscript.
4. dispersal_image.png - a .png file with the image used in Figure 1 to show the experimental set up.
5. the-american-naturalist.csl - a .csl file that defines the citation style for the journal
