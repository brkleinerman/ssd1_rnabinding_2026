README
================

- [Overview](#overview)
- [Inputs](#inputs)
- [Results](#results)

# Overview

This directory contains raw .fcs files and Cq values for analysis

# Inputs

- RTqPCR_Ct - raw Ct (Cq) values used to calculate deltadeltaCq values
  - `wholeUTRs_Ct` - input for `2026-05-12_SUN4_5UTRmuts_RTqPCR.Rmd`
  - `5UTRmuts_Ct` - input for `2026-05-12_SUN4wholeUTRs_RTqPCR.Rmd`
- Flow_metadata - metadata to analyze .fcs files
  - `2025-09-04_SUN4-UTR_flowplan.xlsx` - for
    `2026-05-12_SUN4_UTR_flow.Rmd`
  - `2026-02-17_Ssd1_pointmutants_flowplan.xlsx` - for
    `2026-05-11_Ssd1_pointmutant_flow.Rmd`
- FCS - .fcs files from acquisition on our BD LSRFortessa Cell Analyzer.
  - `SUN4_UTR_flow` - `2026-05-12_SUN4_UTR_flow.Rmd`
  - `Ssd1_pointmutants_flow` - for
    `2026-05-11_Ssd1_pointmutant_flow.Rmd`
- RTqPCR_coeff - linear model deltadeltaCq coefficients. 0 was added to
  intercepts to calculate strain means.
  - `fit_RTqPCR_tADH1.tsv` - this is an output from
    `2026-05-12_SUN4_5UTRmuts_RTqPCR.Rmd`, to be read into
    `2026-05-12_SUN4_UTR_flow.Rmd`
  - `fit_RTqPCR_utrs.tsv` - this is an output from
    `2026-05-12_SUN4wholeUTRs_RTqPCR.Rmd`, to be read into
    `2026-05-12_SUN4_UTR_flow.Rmd`

All scripts referred to are in the Rmd folder in this repository.

# Results

Describe the outputs here.

``` r
sessionInfo()
```

    ## R version 4.4.2 (2024-10-31 ucrt)
    ## Platform: x86_64-w64-mingw32/x64
    ## Running under: Windows 11 x64 (build 26100)
    ## 
    ## Matrix products: default
    ## 
    ## 
    ## locale:
    ## [1] LC_COLLATE=English_United Kingdom.utf8 
    ## [2] LC_CTYPE=English_United Kingdom.utf8   
    ## [3] LC_MONETARY=English_United Kingdom.utf8
    ## [4] LC_NUMERIC=C                           
    ## [5] LC_TIME=English_United Kingdom.utf8    
    ## 
    ## time zone: Europe/London
    ## tzcode source: internal
    ## 
    ## attached base packages:
    ## [1] stats     graphics  grDevices utils     datasets  methods   base     
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] compiler_4.4.2    fastmap_1.2.0     cli_3.6.5         tools_4.4.2      
    ##  [5] htmltools_0.5.8.1 otel_0.2.0        rstudioapi_0.18.0 yaml_2.3.10      
    ##  [9] rmarkdown_2.30    knitr_1.51        xfun_0.56         digest_0.6.37    
    ## [13] rlang_1.1.7       evaluate_1.0.5
