HW 2
================
Hongzhu Ren
2023-10-01

# Problem 1

## Import and clean pol_month data

    ## # A tibble: 822 × 9
    ##     year month gov_gop sen_gop rep_gop gov_dem sen_dem rep_dem president
    ##    <dbl> <chr>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl> <chr>    
    ##  1  1947 Jan        23      51     253      23      45     198 dem      
    ##  2  1947 Feb        23      51     253      23      45     198 dem      
    ##  3  1947 Mar        23      51     253      23      45     198 dem      
    ##  4  1947 Apr        23      51     253      23      45     198 dem      
    ##  5  1947 May        23      51     253      23      45     198 dem      
    ##  6  1947 Jun        23      51     253      23      45     198 dem      
    ##  7  1947 Jul        23      51     253      23      45     198 dem      
    ##  8  1947 Aug        23      51     253      23      45     198 dem      
    ##  9  1947 Sep        23      51     253      23      45     198 dem      
    ## 10  1947 Oct        23      51     253      23      45     198 dem      
    ## # ℹ 812 more rows

**pol_month** data described the party composition of government
agencies ranging from 1947 to 2015. The prefix *gov*,*sen*,*rep* meant
separately the number of governors, the number of senators,the number of
representatives. And the suffix *gop* and *dem* referred to the two
parties of USA.

## Import and clean snp data

    ## # A tibble: 787 × 3
    ##     year month close
    ##    <dbl> <fct> <dbl>
    ##  1  1950 Jan    17.0
    ##  2  1950 Feb    17.2
    ##  3  1950 Mar    17.3
    ##  4  1950 Apr    18.0
    ##  5  1950 May    18.8
    ##  6  1950 Jun    17.7
    ##  7  1950 Jul    17.8
    ##  8  1950 Aug    18.4
    ##  9  1950 Sep    19.5
    ## 10  1950 Oct    19.5
    ## # ℹ 777 more rows

**snp** data reflected the stock performance . The *close* variable
referred to the closing values of the S&P stock index on the associated
date ranging from 1950 to 2015

## Import and clean unemployment data

    ## # A tibble: 816 × 3
    ##     year month unemployment
    ##    <dbl> <chr>        <dbl>
    ##  1  1948 Jan            3.4
    ##  2  1948 Feb            3.8
    ##  3  1948 Mar            4  
    ##  4  1948 Apr            3.9
    ##  5  1948 May            3.5
    ##  6  1948 Jun            3.6
    ##  7  1948 Jul            3.6
    ##  8  1948 Aug            3.9
    ##  9  1948 Sep            3.8
    ## 10  1948 Oct            3.7
    ## # ℹ 806 more rows

**unemployment** data described the unemployment rate over time randing
from 1948 to 2015.

    ## # A tibble: 828 × 11
    ##     year month gov_gop sen_gop rep_gop gov_dem sen_dem rep_dem president close
    ##    <dbl> <chr>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl> <chr>     <dbl>
    ##  1  1947 Apr        23      51     253      23      45     198 dem          NA
    ##  2  1947 Aug        23      51     253      23      45     198 dem          NA
    ##  3  1947 Dec        24      51     253      23      45     198 dem          NA
    ##  4  1947 Feb        23      51     253      23      45     198 dem          NA
    ##  5  1947 Jan        23      51     253      23      45     198 dem          NA
    ##  6  1947 Jul        23      51     253      23      45     198 dem          NA
    ##  7  1947 Jun        23      51     253      23      45     198 dem          NA
    ##  8  1947 Mar        23      51     253      23      45     198 dem          NA
    ##  9  1947 May        23      51     253      23      45     198 dem          NA
    ## 10  1947 Nov        24      51     253      23      45     198 dem          NA
    ## # ℹ 818 more rows
    ## # ℹ 1 more variable: unemployment <dbl>

The final data is a 11 columns and 828 rows dataset. This data showed
government composition in association with stock performance and
unemployment situation ranging from 1947 to 2015.

# Problem 2

## Import and clean Mr.Trash Wheel data

    ## # A tibble: 584 × 14
    ##    dumpster month year  date                weight_tons volume_cubic_yards
    ##       <dbl> <chr> <chr> <dttm>                    <dbl>              <dbl>
    ##  1        1 May   2014  2014-05-16 00:00:00        4.31                 18
    ##  2        2 May   2014  2014-05-16 00:00:00        2.74                 13
    ##  3        3 May   2014  2014-05-16 00:00:00        3.45                 15
    ##  4        4 May   2014  2014-05-17 00:00:00        3.1                  15
    ##  5        5 May   2014  2014-05-17 00:00:00        4.06                 18
    ##  6        6 May   2014  2014-05-20 00:00:00        2.71                 13
    ##  7        7 May   2014  2014-05-21 00:00:00        1.91                  8
    ##  8        8 May   2014  2014-05-28 00:00:00        3.7                  16
    ##  9        9 June  2014  2014-06-05 00:00:00        2.52                 14
    ## 10       10 June  2014  2014-06-11 00:00:00        3.76                 18
    ## # ℹ 574 more rows
    ## # ℹ 8 more variables: plastic_bottles <dbl>, polystyrene <dbl>,
    ## #   cigarette_butts <dbl>, glass_bottles <dbl>, plastic_bags <dbl>,
    ## #   wrappers <dbl>, sports_balls <dbl>, homes_powered <dbl>

## Import and clean Professor data

    ## # A tibble: 94 × 13
    ##    dumpster month     year date                weight_tons volume_cubic_yards
    ##       <dbl> <chr>    <dbl> <dttm>                    <dbl>              <dbl>
    ##  1        1 January   2017 2017-01-02 00:00:00        1.79                 15
    ##  2        2 January   2017 2017-01-30 00:00:00        1.58                 15
    ##  3        3 February  2017 2017-02-26 00:00:00        2.32                 18
    ##  4        4 February  2017 2017-02-26 00:00:00        3.72                 15
    ##  5        5 February  2017 2017-02-28 00:00:00        1.45                 15
    ##  6        6 March     2017 2017-03-30 00:00:00        1.71                 15
    ##  7        7 April     2017 2017-04-01 00:00:00        1.82                 15
    ##  8        8 April     2017 2017-04-20 00:00:00        2.37                 15
    ##  9        9 May       2017 2017-05-10 00:00:00        2.64                 15
    ## 10       10 May       2017 2017-05-26 00:00:00        2.78                 15
    ## # ℹ 84 more rows
    ## # ℹ 7 more variables: plastic_bottles <dbl>, polystyrene <dbl>,
    ## #   cigarette_butts <dbl>, glass_bottles <dbl>, grocery_bags <dbl>,
    ## #   chip_bags <dbl>, homes_powered <dbl>

## Import and clean Gwynnda data

    ## # A tibble: 106 × 11
    ##    dumpster month   year date                weight_tons volume_cubic_yards
    ##       <dbl> <chr>  <dbl> <dttm>                    <dbl>              <dbl>
    ##  1        1 July    2021 2021-07-03 00:00:00        0.93                 15
    ##  2        2 July    2021 2021-07-07 00:00:00        2.26                 15
    ##  3        3 July    2021 2021-07-07 00:00:00        1.62                 15
    ##  4        4 July    2021 2021-07-16 00:00:00        1.76                 15
    ##  5        5 July    2021 2021-07-30 00:00:00        1.53                 15
    ##  6        6 August  2021 2021-08-11 00:00:00        2.06                 15
    ##  7        7 August  2021 2021-08-14 00:00:00        1.9                  15
    ##  8        8 August  2021 2021-08-16 00:00:00        2.16                 15
    ##  9        9 August  2021 2021-08-16 00:00:00        2.6                  15
    ## 10       10 August  2021 2021-08-17 00:00:00        3.21                 15
    ## # ℹ 96 more rows
    ## # ℹ 5 more variables: plastic_bottles <dbl>, polystyrene <dbl>,
    ## #   cigarette_butts <dbl>, plastic_bags <dbl>, homes_powered <dbl>

## Add tag to each dataset

Add “Mr.trash”,“professor”,“gwynnda” to each dataset.

## Combine three datasets and form the trash_final dataset

    ## # A tibble: 784 × 17
    ##    tag   dumpster month  year date                weight_tons volume_cubic_yards
    ##    <chr>    <dbl> <chr> <dbl> <dttm>                    <dbl>              <dbl>
    ##  1 Mr.t…        1 May    2014 2014-05-16 00:00:00        4.31                 18
    ##  2 Mr.t…        2 May    2014 2014-05-16 00:00:00        2.74                 13
    ##  3 Mr.t…        3 May    2014 2014-05-16 00:00:00        3.45                 15
    ##  4 Mr.t…        4 May    2014 2014-05-17 00:00:00        3.1                  15
    ##  5 Mr.t…        5 May    2014 2014-05-17 00:00:00        4.06                 18
    ##  6 Mr.t…        6 May    2014 2014-05-20 00:00:00        2.71                 13
    ##  7 Mr.t…        7 May    2014 2014-05-21 00:00:00        1.91                  8
    ##  8 Mr.t…        8 May    2014 2014-05-28 00:00:00        3.7                  16
    ##  9 Mr.t…        9 June   2014 2014-06-05 00:00:00        2.52                 14
    ## 10 Mr.t…       10 June   2014 2014-06-11 00:00:00        3.76                 18
    ## # ℹ 774 more rows
    ## # ℹ 10 more variables: plastic_bottles <dbl>, polystyrene <dbl>,
    ## #   cigarette_butts <dbl>, glass_bottles <dbl>, plastic_bags <dbl>,
    ## #   wrappers <dbl>, sports_balls <dbl>, homes_powered <dbl>,
    ## #   grocery_bags <dbl>, chip_bags <dbl>

The final combined data is a 17 and 784 dataset, the *weight_tons*
variable refers to the total weight the trash wheel carried each day
with the unit ton. *home_powered* estimate the number of houses which
can be supplied by energy generated from trash wheel.

As for the available data, the total weight of trash collected by
Professor Trash Wheel was 190.12 tons; the total cigarette butts
collected by Gwynnda in July of 2021 was 1.63^{4}.

# Problem 3

## Import and clean baseline data

    ## Rows: 483 Columns: 6
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (1): Age at onset
    ## dbl (5): ID, Current Age, Sex, Education, apoe4
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    ## # A tibble: 479 × 6
    ##       id current_age sex    education apoe4         age_at_onset
    ##    <dbl>       <dbl> <chr>      <dbl> <chr>         <chr>       
    ##  1     1        63.1 Female        16 APOE4_carrier .           
    ##  2     2        65.6 Female        20 APOE4_carrier .           
    ##  3     3        62.5 Male          16 APOE4_carrier 66.8        
    ##  4     4        69.8 Female        16 non_carrier   .           
    ##  5     5        66   Male          16 non_carrier   68.7        
    ##  6     6        62.5 Male          16 non_carrier   .           
    ##  7     7        66.5 Male          18 non_carrier   74          
    ##  8     8        67.2 Female        18 non_carrier   .           
    ##  9     9        66.7 Female        16 non_carrier   .           
    ## 10    10        64.1 Female        18 non_carrier   .           
    ## # ℹ 469 more rows

In total 479 participants who satisfied the standard were recruited. Of
these participants, 93 subjects developed MLC. The average baselin age
was 65.0286013. The portion of women who were APOE4 carrier was 0.3.

## Import and clean longitudinal dataset

``` r
longit <- read_csv("./data/mci_amyloid.csv",skip = 1) |>
  janitor::clean_names() |> 
  rename(id = study_id) |> #rename the key varaible for latter merging
  pivot_longer(
    time_2:time_8,
    names_to = "time_points",
    values_to = "biomaker_values"
  )
```

    ## Rows: 487 Columns: 6
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (5): Baseline, Time 2, Time 4, Time 6, Time 8
    ## dbl (1): Study ID
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
na_row <- sum(!complete.cases(longit))
```

The longitudinal dataset is a 4 columns and 1948 rows dataset. It
covered 5 time points started from baseline with an interval of 2 time
units. There are 166 subjects with na in its longitudinal observations.

## Join two datasets

First check the only participants in each group

The unique id in baseline dataset are displayed below:

    ## [1]  14  49  92 179 268 304 389 412

The unique id in longitudinal dataset are displayed below:

    ##  [1]  72 234 283 380 484 485 486 487 488 489 490 491 492 493 494 495

## Merge two dataset using inner_join() by the same ID

    ## # A tibble: 1,884 × 9
    ##       id current_age sex    education apoe4    age_at_onset baseline time_points
    ##    <dbl>       <dbl> <chr>      <dbl> <chr>    <chr>        <chr>    <chr>      
    ##  1     1        63.1 Female        16 APOE4_c… .            0.11054… time_2     
    ##  2     1        63.1 Female        16 APOE4_c… .            0.11054… time_4     
    ##  3     1        63.1 Female        16 APOE4_c… .            0.11054… time_6     
    ##  4     1        63.1 Female        16 APOE4_c… .            0.11054… time_8     
    ##  5     2        65.6 Female        20 APOE4_c… .            0.10748… time_2     
    ##  6     2        65.6 Female        20 APOE4_c… .            0.10748… time_4     
    ##  7     2        65.6 Female        20 APOE4_c… .            0.10748… time_6     
    ##  8     2        65.6 Female        20 APOE4_c… .            0.10748… time_8     
    ##  9     3        62.5 Male          16 APOE4_c… 66.8         0.10608… time_2     
    ## 10     3        62.5 Male          16 APOE4_c… 66.8         0.10608… time_4     
    ## # ℹ 1,874 more rows
    ## # ℹ 1 more variable: biomaker_values <chr>

The merged dataset had 1884 observations and 471 subjects. With 205
females and 266 males in the dataset. The portion of participants who
developed MLC in this dataset is 0.1910828.

## Export AD_merge to data folder

``` r
write_csv(AD_merge,file = "./data/AD_merge.csv")
```
