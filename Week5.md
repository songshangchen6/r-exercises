Week5
================
ssc
6/20/2020

``` r
usa_pop <- world_bank_pop %>% 
  filter(country == "USA") %>% 
  gather(key = "year", value = "v", `2000`:`2017`) %>% 
  relocate(year, .after = country) %>% 
  spread(key = indicator, value = v) 

usa_pop
```

    ## # A tibble: 18 x 6
    ##    country year  SP.POP.GROW SP.POP.TOTL SP.URB.GROW SP.URB.TOTL
    ##    <chr>   <chr>       <dbl>       <dbl>       <dbl>       <dbl>
    ##  1 USA     2000        1.11    282162411       1.51    223069137
    ##  2 USA     2001        0.990   284968955       1.21    225792302
    ##  3 USA     2002        0.928   287625193       1.15    228400290
    ##  4 USA     2003        0.859   290107933       1.08    230876596
    ##  5 USA     2004        0.925   292805298       1.14    233532722
    ##  6 USA     2005        0.922   295516599       1.14    236200507
    ##  7 USA     2006        0.964   298379912       1.18    238999326
    ##  8 USA     2007        0.951   301231207       1.16    241795278
    ##  9 USA     2008        0.946   304093966       1.16    244607104
    ## 10 USA     2009        0.877   306771529       1.09    247276259
    ## 11 USA     2010        0.833   309338421       1.04    249858829
    ## 12 USA     2011        0.743   311644280       0.955   252257346
    ## 13 USA     2012        0.751   313993272       0.967   254708202
    ## 14 USA     2013        0.711   316234505       0.933   257095490
    ## 15 USA     2014        0.752   318622525       0.978   259623192
    ## 16 USA     2015        0.756   321039839       0.986   262196447
    ## 17 USA     2016        0.734   323405935       0.968   264746567
    ## 18 USA     2017        0.713   325719178       0.952   267278643
