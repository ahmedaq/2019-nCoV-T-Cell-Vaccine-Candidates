# 2019-nCoV-T-Cell-Vaccine-Candidates

### Prerequisites

Latest version of [**R**](https://www.r-project.org/) (version 3.6.0 or
later) and [**RStudio**](https://rstudio.com/products/rstudio/download/)
(version 1.2.5 or later) installed.

Set the working directory to the downloaded repository folder in local system.

Following **R** packages and their dependencies are required. 

    + here 
    + RColorBrewer 
    + tidyverse 
    + seqinr
    + readxl 
    + readr 
    + glue 
    + reticulate 
    + BALCONY 
    + seqinr 
    + doParallel
    + BiocManager
    + msa 
    + Biostrings
    + doParallel
    + foreach
        
### Organization

-   Main R code is in `main.R` file.
-   Custom functions are in `Functions` folder 
-   All data files are in `Data` folder 
-   Python 2.7 code from [IEDB](http://tools.iedb.org/population/download/) for computing population coverages is in `Utils` folder

### Main Project File

- Open the `main.R` R script file in RStudio and run. This will run the analysis reproduce the results.
- Outputs will be in `Data` folder.
- *Population coverage code* works only with an available Conda Python 2.7 environment (named as "py27") on the system.
- If the said Conda environment is not avaialable then the population coverages can be computed online using [IEDB Analysis Resource](http://tools.iedb.org/population/). 
    - Select the "Population" (*China* or *World*).
    - Select "Calculation option" (*Class I and II combined*) 
    - Proide one of the following files (located within `Data` folder) to the option "Enter epitope / MHC restriction data in the form below or select a file":
        - `Tcell_epitopes_China` for computing coverages for set of epitopes identified to maximize population coverage in China.
        - `Tcell_epitopes_World` for computing coverages for set of epitopes identified to maximize global population coverage.
 
