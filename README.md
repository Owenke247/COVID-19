# COVID-19
Dissecting the Role of the Human Microbiome in COVID-19 via Metagenome-assembled Genomes

# Introduction

This REPO contains in-house scripts (R, Python), data and detailed instructions for users to reproduce much of the analyses we have done for our manuscript titled "Dissecting the Role of the Human Microbiome in COVID-19 via Metagenome-assembled Genomes".

If further assisstance is required, please do not hesitate to contact me by raise an issue in the "Issues" section of this REPO.

# Prerequisites
Below are a list of softwares and databases required before running out test data. Most of the softwares can be installed through CONDA.

# Softwares
A list of required softwares and URLs for their downloads. Please follow instructions for proper software installation on their respective servers. The versions in the parenthesis indicate the ones we used for our project.

A list of required softwares and URLs for their downloads. Please follow instructions for proper software installation on their respective servers. The versions in the parenthesis indicate the ones we used for our project.

Software	Availability
Trimmomatic (v.0.35)	http://www.usadellab.org/cms/index.php?page=trimmomatic
Bowtie2 (v.2.3.3)	http://bowtie-bio.sourceforge.net/bowtie2/manual.shtml
MEGAHIT (v.1.2.8)	https://github.com/voutcn/megahit
metaSPAdes (v.3.13.0)	https://github.com/ablab/spades
MetaBAT2 (2.12.1)	https://bitbucket.org/berkeleylab/metabat/src/master/
dRep (v.2.3.2)	https://github.com/MrOlm/drep
CheckM (v.1.0.18)	https://github.com/Ecogenomics/CheckM
Mash (v.2.3)	https://github.com/marbl/mash
FastANI (v.1.32)	https://github.com/ParBLiSS/FastANI
Prodigal (v.2.6.3)	https://github.com/hyattpd/Prodigal
bwa (v.0.7.15)	https://github.com/lh3/bwa
Samtools (v.1.8)	https://github.com/samtools/samtools
BEDTools (v.2.27.1)	https://bedtools.readthedocs.io/en/latest/content/installation.html
GTDB-TK (v.1.4.1)	https://github.com/Ecogenomics/GTDBTk
GraPhlAn (v.1.1.3)	https://github.com/biobakery/graphlan
CD-HIT (v.4.8.1)	https://github.com/weizhongli/cdhit/
eggnog-mapper (v.4.5)	https://github.com/eggnogdb/eggnog-mapper
hmmer (v.3.3.2)	https://github.com/EddyRivasLab/hmmer
Note: Please make sure all the softwares are in your $PATH.











# Dependencies of R
sessionInfo()
R version 4.1.2 (2021-11-01)
Platform: x86_64-apple-darwin17.0 (64-bit)
Running under: macOS High Sierra 10.13.6

Matrix products: default
BLAS:   /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libBLAS.dylib
LAPACK: /Library/Frameworks/R.framework/Versions/4.1/Resources/lib/libRlapack.dylib

Random number generation:
 RNG:     Mersenne-Twister 
 Normal:  Inversion 
 Sample:  Rounding 
 
locale:
[1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] cowplot_1.1.1     plyr_1.8.6        vegan_2.5-7       permute_0.9-7     ggpattern_0.4.2   reshape2_1.4.4    readxl_1.3.1      dplyr_1.0.8       stringr_1.4.0    
[10] data.table_1.14.2 caret_6.0-91      lattice_0.20-45   ggplot2_3.3.5    

loaded via a namespace (and not attached):
 [1] Rcpp_1.0.8.3         lubridate_1.8.0      listenv_0.8.0        class_7.3-20         assertthat_0.2.1     digest_0.6.29        ipred_0.9-12         foreach_1.5.2       
 [9] utf8_1.2.2           parallelly_1.30.0    R6_2.5.1             cellranger_1.1.0     hardhat_0.2.0        stats4_4.1.2         e1071_1.7-9          pillar_1.7.0        
[17] rlang_1.0.2          rstudioapi_0.13      rpart_4.1.16         Matrix_1.4-0         labeling_0.4.2       splines_4.1.2        gower_1.0.0          munsell_0.5.0       
[25] proxy_0.4-26         compiler_4.1.2       pkgconfig_2.0.3      mgcv_1.8-39          globals_0.14.0       nnet_7.3-17          tidyselect_1.1.2     tibble_3.1.6        
[33] prodlim_2019.11.13   codetools_0.2-18     fansi_1.0.2          future_1.24.0        crayon_1.5.0         withr_2.5.0          MASS_7.3-55          recipes_0.2.0       
[41] ModelMetrics_1.2.2.2 grid_4.1.2           nlme_3.1-155         gtable_0.3.0         lifecycle_1.0.1      DBI_1.1.2            magrittr_2.0.2       pROC_1.18.0         
[49] scales_1.1.1         future.apply_1.8.1   cli_3.2.0            stringi_1.7.6        farver_2.1.0         timeDate_3043.102    ellipsis_0.3.2       generics_0.1.2      
[57] vctrs_0.3.8          lava_1.6.10          RColorBrewer_1.1-2   iterators_1.0.14     tools_4.1.2          glue_1.6.2           purrr_0.3.4          parallel_4.1.2      
[65] survival_3.3-1       yaml_2.3.5           colorspace_2.0-3     cluster_2.1.2    
