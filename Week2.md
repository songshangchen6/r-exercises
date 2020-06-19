---
title: "Week2"
author: "ssc"
date: "6/19/2020"
output: 
  html_document:
          keep_md: TRUE
---



select every third values from x beginning at position 2;

```r
x[seq(from = 2, to = length(x), by = 3)]
```

```
##  [1]  59  72  32  31 100  10  29  79  65  42  52   5  31  47  97  54  89  78   2
## [20]  67  28  12  95  21  14  85  45  27   6   6  25  50  89
```

remove all values with an odd index;

```r
x[-seq(from = 1, to = length(x), by = 2)]
```

```
##  [1]  59  29  16  32   4  68 100   1  72  29   3  98  65   9  39  52   8 100  31
## [20]  10   2  97  92  18  89  84  93   2  49  54  28  79  10  95  48  38  14  13
## [39]  82  45  58  75   6  68  38  25  36  67  89  63
```


remove every 4th value, but only if it is odd;

```r
x[seq_along(x) %% 4 != 0 | x %% 2 == 1]
```

```
##  [1]  11  59  87  29  72  16  14  66   4  31  37 100  35   1  10  72  54  29  50
## [20]   3  79  46  65  15   9  42  39  64  65   8   5  26  31  83  47   2  62  97
## [39]  75  92  54  76  89  90  78  93  98  25  49  67  87  28  53  79  12  10  71
## [58]  95  59  48  21  16  14  51  13  85  82   4  45  32  58  27  75  80   6  24
## [77]   6  38  46  25   9  36  50  67  17  89  71  63
```


remove all numbers divisible by 3 or 7 and replace them with 0.


```r
x[x %% 3 == 0 | x %% 7 == 0] <- 0
```
