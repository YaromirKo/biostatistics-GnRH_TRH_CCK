# Hypothalamic Asymmetry for Differential Endocrine Control of Left and Right Body Sides

This project implements a complete biostatistical analysis pipeline in **R** to investigate the molecular and functional lateralization of the hypothalamus. It includes data preprocessing, Bayesian multilevel modeling of GnRH, TRH, and CCK gene expression, and visualization of asymmetric endocrine control.

---

### Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Methods & Scripts](#methods--scripts)
- [Results & Outputs](#results--outputs)
- [Contributing](#contributing)
- [License](#license)
- [Citation](#citation)

---

## Features
- Bayesian multilevel modeling with **brms** and Stan  
- Data wrangling & visualization using the **tidyverse**  
- Publication‑ready figures via **ggplot2**, **cowplot**, and **patchwork**  
- Posterior predictive checks and Bayesian p‑values  
- Modular code organization for raw data, scripts, and results  

---

## Installation

1. **Prerequisites**  
   - R ≥ 4.4.3  
   - C++ toolchain for Stan models  

2. **Clone repository**  
   ```bash
   git clone https://github.com/YaromirKo/biostatistics-GnRH_TRH_CCK.git
   cd biostatistics-GnRH_TRH_CCK
   ```

3. **Install R packages**  
   ```r
   install.packages(c(
     "tidyverse",
     "brms",
     "rstan",
     "posterior",
     "bayesplot",
     "readxl",
     "openxlsx",
     "flextable",
     "officer"
   ))
   ```

---

## Usage

1. **Open R project**  
   Launch `GnRH_TRH_CCK_Stat_25 04 10.Rproj` in RStudio.

2. **Run main script**  
   ```r
   source("BayesianPValue.R")
   ```
   This preprocesses data, fits models, computes p‑values, and writes outputs to `results/`.

3. **Generate figures**  
   Use the scripts in `task_1/` to produce publication‑quality plots and tables.

---

## Project Structure

```
data/                         # Raw & intermediate data  
task_1/                       # Task‑specific analysis scripts  
BayesianPValue.R              # Main modeling script  
GnRH_TRH_CCK_Stat_25_04_10.Rproj  # RStudio project file  
results/                      # Outputs: figures, tables, reports  
.gitignore  
README.md  
```

---

## Methods & Scripts
- **Data Preprocessing**: Tidy data with **dplyr**, **tidyr**, **readr**  
- **Model Specification**: Define **brms** formulas with group‑specific priors  
- **Posterior Analysis**: Summarize fits, compute p‑values, visualize with **bayesplot** and **ggplot2**

---

## Results & Outputs
The `results/` folder contains:  
- **Figures** (`.png`, `.pdf`) of lateralized expression  
- **Tables** (`.csv`, `.xlsx`) of posterior estimates  
- **Report** (`.html`, `.docx`) via **officer** and **flextable**  

---

## Contributing
1. Fork the repository  
2. Create a branch: `git checkout -b feature/YourFeature`  
3. Commit & push: `git push origin feature/YourFeature`  
4. Open a Pull Request  

---

## License
This project is licensed under the **MIT License**. See `LICENSE` for details.

---

## Citation
If you use this work, please cite:

> Bürkner, P.-C. (2017). *brms: An R Package for Bayesian Multilevel Models Using Stan*. Journal of Statistical Software, 80(1), 1–28.

### System Info

R version 4.4.3 (2025-02-28)
Platform: x86_64-pc-linux-gnu
Running under: Ubuntu 24.04.2 LTS

Matrix products: default
BLAS:   /usr/lib/x86_64-linux-gnu/blas/libblas.so.3.12.0 
LAPACK: /usr/lib/x86_64-linux-gnu/lapack/liblapack.so.3.12.0

locale:
 [1] LC_CTYPE=C.UTF-8       LC_NUMERIC=C          
 [3] LC_TIME=C.UTF-8        LC_COLLATE=C.UTF-8    
 [5] LC_MONETARY=C.UTF-8    LC_MESSAGES=C.UTF-8   
 [7] LC_PAPER=C.UTF-8       LC_NAME=C             
 [9] LC_ADDRESS=C           LC_TELEPHONE=C        
[11] LC_MEASUREMENT=C.UTF-8 LC_IDENTIFICATION=C   

time zone: Asia/Tashkent
tzcode source: system (glibc)

attached base packages:
[1] stats     graphics  grDevices utils     datasets 
[6] methods   base     

other attached packages:
 [1] processx_3.8.6      RColorBrewer_1.1-3 
 [3] ggsci_3.2.0         viridis_0.6.5      
 [5] viridisLite_0.4.2   flextable_0.9.7    
 [7] emmeans_1.11.0      brms_2.22.0        
 [9] Rcpp_1.0.14         rstan_2.32.7       
[11] StanHeaders_2.32.10 latex2exp_0.9.6    
[13] patchwork_1.3.0     cowplot_1.1.3      
[15] ggridges_0.5.6      ggstance_0.3.7     
[17] tidybayes_3.0.7     modelr_0.1.11      
[19] rvg_0.3.5           officer_0.6.8      
[21] openxlsx_4.2.8      readxl_1.4.5       
[23] lubridate_1.9.4     forcats_1.0.0      
[25] stringr_1.5.1       dplyr_1.1.4        
[27] purrr_1.0.4         readr_2.1.5        
[29] tidyr_1.3.1         tibble_3.2.1       
[31] ggplot2_3.5.2       tidyverse_2.0.0    

loaded via a namespace (and not attached):
 [1] gridExtra_2.3           inline_0.3.21          
 [3] rlang_1.1.6             magrittr_2.0.3         
 [5] matrixStats_1.5.0       compiler_4.4.3         
 [7] mgcv_1.9-1              loo_2.8.0              
 [9] reshape2_1.4.4          callr_3.7.6            
[11] systemfonts_1.2.2       vctrs_0.6.5            
[13] crayon_1.5.3            pkgconfig_2.0.3        
[15] arrayhelpers_1.1-0      fastmap_1.2.0          
[17] backports_1.5.0         labeling_0.4.3         
[19] rmarkdown_2.29          tzdb_0.5.0             
[21] ps_1.9.1                ragg_1.4.0             
[23] bit_4.6.0               xfun_0.52              
[25] uuid_1.2-1              broom_1.0.8            
[27] parallel_4.4.3          R6_2.6.1               
[29] stringi_1.8.7           cellranger_1.1.0       
[31] estimability_1.5.1      knitr_1.50             
[33] bayesplot_1.12.0        splines_4.4.3          
[35] Matrix_1.6-5            timechange_0.3.0       
[37] tidyselect_1.2.1        rstudioapi_0.17.1      
[39] abind_1.4-8             yaml_2.3.10            
[41] codetools_0.2-19        pkgbuild_1.4.7         
[43] plyr_1.8.9              lattice_0.22-5         
[45] withr_3.0.2             bridgesampling_1.1-2   
[47] askpass_1.2.1           posterior_1.6.1        
[49] coda_0.19-4.1           evaluate_1.0.3         
[51] RcppParallel_5.1.10     zip_2.3.2              
[53] ggdist_3.3.2            xml2_1.3.8             
[55] pillar_1.10.2           tensorA_0.36.2.1       
[57] checkmate_2.3.2         stats4_4.4.3           
[59] distributional_0.5.0    generics_0.1.3         
[61] vroom_1.6.5             hms_1.1.3              
[63] rstantools_2.4.0        munsell_0.5.1          
[65] scales_1.3.0            glue_1.8.0             
[67] gdtools_0.4.2           tools_4.4.3            
[69] data.table_1.17.0       mvtnorm_1.3-3          
[71] grid_4.4.3              QuickJSR_1.7.0         
[73] colorspace_2.1-1        nlme_3.1-164           
[75] cli_3.6.4               textshaping_1.0.0      
[77] fontBitstreamVera_0.1.1 svUnit_1.0.6           
[79] Brobdingnag_1.2-9       gtable_0.3.6           
[81] digest_0.6.37           fontquiver_0.2.1       
[83] farver_2.1.2            htmltools_0.5.8.1      
[85] lifecycle_1.0.4         bit64_4.6.0-1          
[87] fontLiberation_0.1.0    openssl_2.3.2
