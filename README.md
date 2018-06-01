# Assessing Canada’s Drug Shortage Problem

This is a companion repository containing some of the source code and data used to produce figures in our paper: 

> Donelle, J., Duffin, J., Pipitone, J., & White-Guay, B. (2018). Assessing
> Canada’s Drug Shortage Problem. C.D. Howe Institute, Commentary, 515. Retrieved
> June 5, 2018, from www.cdhowe.org.

To run this code you will need: 

1. [R](https://www.r-project.org/). This code was tested with R 3.4.4.
2. The following R packages: 
   - tidyverse. Tested with version 1.2.1
   - ggrepel. Tested with version 0.7.0
   - lubridate. Tested with version 1.7.1
   - rmarkdown. Tested with version 1.8
   - flexdashboard. Tested with version 0.5.1

The code is embedded in an rmarkdown document. To render the document, open
`analysis.Rmd` in Rstudio and run knitr, or from the R console, run:

```r
rmarkdown::render("analysis.Rmd")
```

## Datasets

We use the following datasets: 

- **drugshortages.ca**: Voluntary shortage reporting database active until
  March 2017. Data from this website was collected manually by us and is stored
  `data/drugshortages.ca-manual.csv`. We later obtained an export of the
  database as of '2018-03-13', which we used to supplement our manually acquired
  data, we are unable to include this exported dataset in this repository. An
  empty data file indicating the structure of this dataset is located in
  `data/drugshortages.ca-export.csv`.
  
- **drugshortagescanada.ca**: Mandatory shortage reporting database active from
  March 2017 onwards. An export of this dataset as of 2017-12-31 is located in
  `data/drugshortagescanada.ca-2017-12-31.csv`. 
  
    Exports can be obtained on demaned by using the [drughsortagescanada.ca online search](https://www.drugshortagescanada.ca/search?term=&date_range%5Bdate_range_start%5D%5Bmonth%5D=&date_range%5Bdate_range_start%5D%5Bday%5D=&date_range%5Bdate_range_start%5D%5Byear%5D=&date_range%5Bdate_range_end%5D%5Bmonth%5D=&date_range%5Bdate_range_end%5D%5Bday%5D=&date_range%5Bdate_range_end%5D%5Byear%5D=&filter_type=shortages&filter_status=_all_)

  
- **Health Canada Drug Product Database**: Historical drug product information
   provided by Health Canada. This dataset cannot be provided in this repository
   but exports may be downloaded at: 
   
     https://www.canada.ca/en/health-canada/services/drugs-health-products/drug-products/drug-product-database/extracts.html

     Setting the variable `DPD_DOWNLOAD = TRUE` will attempt to download and
     unpack the extracts as `analysis.Rmd` is rendered.