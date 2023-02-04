### What does it do?
Have you ever had a time when your missing data was holding you back? Well then this package is for you!

Our R package for simple data imputation will allow you to quickly and seamlessly impute any missing data (be numeric, categorical, date/time or boolean values) using any large datasets.

All you have to do is follow these simple 4 steps:
 1. Import the package and the data you wish you impute
 2. Select the function and method for imputation (this will depend on the data type - read the usage section below for more details)
 3. Hit run
 4. Save your newly imputed dataset

Our package will help simplify all your imputation needs so your data is ready when you need it!

## Contributors & Maintainers
- [Lisa Sequeira](https://github.com/LisaSeq)
- [Renee Kwon](https://github.com/renee-kwon)
- [Fujie Sun](https://github.com/Althrun-sun)
- [Ken Wang](https://github.com/kenuiuc)

## Usage

We have four main functions dealing with each data type:

- `Num_imputer`: This function fills in the empty values of a numeric column with the mean value.  

- `Cat_imputer`: This function fills in the empty values of a categorical column with values derived based on most frequent (mode) category. 

- `Bol_imputer`: This function fills in the empty values of a boolean column with values derived using most frequent (mode) boolean value.

- `Date_imputer`: This function fills in empty values of a date column with median point of the range of dates in that column.

## Installation

You can install the development version of Simpute from GitHub with:

``` r
# install.packages("devtools")
devtools::install_github("https://github.com/UBC-MDS/simpute-r.git")
```
## Demonstration

For this demonstration, we will use this sample dataset `cars` containing `NA`s:

``` r
data <- data.frame('Origin' = (c("Canada", "Japan", "Japan", "Japan", "Germany", "France", "Korea", "Canada", 
"North America", "France", "Japan", "Japan",,)), 
                   'Speed'= (c(-100,-200,1,2,3,4,5,6,7,8,9,,1000)),
                   'OnTheMarket' = (c(0,,1,0,1,0,0,1,1,1,1,1,1)),
                   'ManufactureDate' = (c("4/2/2013", "4/2/2014", "4/2/2015", "4/2/2016", "4/2/2017", "4/2/2018", 
                   "4/2/2019",, "4/2/2017", "4/2/2018", "4/2/2019", "4/2/2020")))
```

## Within the R Ecosystem

There are several useful packages in the R ecosystem for imputing data. For example, [MICE](https://github.com/amices/mice) is a powerful package that allows multiple imputations with values drawn from a distribution of the data. The [Hmisc](https://github.com/harrelfe/Hmisc) package contains an impute function using methods of additive regression, bootstrapping, and predictive mean matching. As well, users may use base R or the [dplyr](https://dplyr.tidyverse.org/) package to filter out for missing values and replace them manually. However, our package aims to simplify this process and make the process easier and quicker for use by the general public. 

## Contributing

Interested in contributing? Check out the contributing guidelines. Please note that this project is released with a Code of Conduct. By contributing to this project, you agree to abide by its terms.

## License

`simpute` was created by Lisa Sequeira, Renee Kwon, Fujie Sun, and Ken Wang. It is licensed under the terms of the MIT license.
