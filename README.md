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

# Software used  
R version 4.1.3 (2022-03-10)  
Platform: x86_64-apple-darwin17.0 (64-bit)  
Running under: macOS Monterey 12.7.3  

attached base packages:  
* stats
* graphics
* grDevices
* utils
* datasets
* methods
* base       

other attached packages:  
 [1] magick_2.7.3         rstan_2.21.7         StanHeaders_2.21.0-7 vegan_2.6-4          lattice_0.20-45     
 [6] permute_0.9-7        abind_1.4-5          lubridate_1.8.0      Hmsc_3.0-11          coda_0.19-4         
[11] patchwork_1.1.1      forcats_0.5.1        stringr_1.5.0        dplyr_1.0.10         purrr_1.0.1         
[16] readr_2.1.2          tidyr_1.3.0          tibble_3.1.8         ggplot2_3.4.0        tidyverse_1.3.1     
[21] kableExtra_1.3.4     knitr_1.38           bibtex_0.4.2.3       knitcitations_1.0.12  

loaded via a namespace (and not attached):  
 [1] colorspace_2.1-0   ellipsis_0.3.2     fs_1.5.2           rstudioapi_0.13    farver_2.1.1       MatrixModels_0.5-0
 [7] fansi_1.0.4        RefManageR_1.3.0   xml2_1.3.3         codetools_0.2-18   splines_4.1.3      spam_2.8-0        
[13] jsonlite_1.8.0     pROC_1.18.0        mcmc_0.9-7         broom_0.8.0        cluster_2.1.2      dbplyr_2.1.1      
[19] compiler_4.1.3     httr_1.4.2         backports_1.4.1    assertthat_0.2.1   Matrix_1.4-0       fastmap_1.1.0     
[25] cli_3.6.0          prettyunits_1.1.1  htmltools_0.5.2    quantreg_5.88      tools_4.1.3        dotCall64_1.0-1   
[31] gtable_0.3.1       glue_1.6.2         maps_3.4.0         Rcpp_1.0.10        cellranger_1.1.0   vctrs_0.5.2       
[37] ape_5.6-2          svglite_2.1.0      nlme_3.1-155       xfun_0.30          ps_1.6.0           rvest_1.0.2       
[43] lifecycle_1.0.3    statmod_1.4.36     MASS_7.3-55        scales_1.2.1       hms_1.1.1          parallel_4.1.3    
[49] inline_0.3.19      SparseM_1.81       fields_13.3        yaml_2.3.5         gridExtra_2.3      loo_2.5.1         
[55] stringi_1.7.12     pkgbuild_1.3.1     truncnorm_1.0-8    rlang_1.0.6        pkgconfig_2.0.3    systemfonts_1.0.4 
[61] matrixStats_0.61.0 pracma_2.3.8       evaluate_0.15      labeling_0.4.2     processx_3.5.3     tidyselect_1.2.0  
[67] plyr_1.8.7         magrittr_2.0.3     bookdown_0.26      R6_2.5.1           generics_0.1.3     BayesLogit_2.1    
[73] DBI_1.1.2          pillar_1.8.1       haven_2.5.0        withr_2.5.0        mgcv_1.8-39        sp_1.4-6          
[79] nnet_7.3-17        modelr_0.1.8       crayon_1.5.1       utf8_1.2.2         tzdb_0.3.0         rmarkdown_2.13    
[85] viridis_0.6.2      grid_4.1.3         readxl_1.4.0       callr_3.7.0        FNN_1.1.3          reprex_2.0.1      
[91] digest_0.6.29      webshot_0.5.3      MCMCpack_1.6-3     RcppParallel_5.1.5 stats4_4.1.3       munsell_0.5.0     
[97] viridisLite_0.4.1 
