Data Import
================

``` r
library(tidyverse)
```

    ## -- Attaching packages -------------------------------- tidyverse 1.3.0 --

    ## v ggplot2 3.3.2     v purrr   0.3.4
    ## v tibble  3.0.3     v dplyr   1.0.2
    ## v tidyr   1.1.2     v stringr 1.4.0
    ## v readr   1.3.1     v forcats 0.5.0

    ## -- Conflicts ----------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

## Read in some data

Read in the litters dataset. “read\_csv” exisits in the readr package in
tidyverse Since we’re working within the “data\_wrangling\_i” project,
we can create a relative path starting with that folder “./” means start
with the project folder

Also will update names in df because they aren’t in good form
(clean\_names) Doing “janitor::” means clean\_names is in that package.
But since it’s the only function in that package we need, we don’t need
to load the entire package

``` r
litters_df = read_csv("./data/FAS_litters.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   Group = col_character(),
    ##   `Litter Number` = col_character(),
    ##   `GD0 weight` = col_double(),
    ##   `GD18 weight` = col_double(),
    ##   `GD of Birth` = col_double(),
    ##   `Pups born alive` = col_double(),
    ##   `Pups dead @ birth` = col_double(),
    ##   `Pups survive` = col_double()
    ## )

``` r
litters_df = janitor::clean_names(litters_df)
```

## Take a look at the data
