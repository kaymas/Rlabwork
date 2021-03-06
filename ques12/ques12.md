Question 12
================
samyak

Program to compute the measures of dispersion for the following frequency distribution.
---------------------------------------------------------------------------------------

| midpoint | number |
|----------|--------|
| 95.5     | 5      |
| 105.5    | 8      |
| 115.5    | 22     |
| 125.5    | 27     |
| 135.5    | 17     |
| 145.5    | 9      |
| 155.5    | 5      |
| 165.5    | 5      |
| 175.5    | 2      |

### Measures of dispersion?

Measures of dispersion - such as range, variance, standard deviation, quantiles - and can be calculated with standard functions present in the native *stats* package. In addition summary function can be used for other statistical information.

### Storing Data in a Data Frame

``` r
blood_pressures <- seq(from = 95.5, to = 175.5, by = 10) 
frequency_dist <- c(5,8,22,27,17,9,5,5,2)
bpDist <- data.frame(bp = blood_pressures, freq = frequency_dist)
bpDist
```

    ##      bp freq
    ## 1  95.5    5
    ## 2 105.5    8
    ## 3 115.5   22
    ## 4 125.5   27
    ## 5 135.5   17
    ## 6 145.5    9
    ## 7 155.5    5
    ## 8 165.5    5
    ## 9 175.5    2

### Calculating Range

``` r
range(bpDist$bp)
```

    ## [1]  95.5 175.5

This shows that the minimum bp value in the distribution is 95.5 and the maximum value is 175.5

### Calculating Variance and Standard Deviation

Since we have a frequency distribution, we have to use weighted mean, variance, and sd to reflect the frequency of each blood pressure measure in the calculation of each of these.

``` r
bpMean <- weighted.mean(bpDist$bp, bpDist$freq)
bpVar <- sum(bpDist$freq * (bpDist$bp - bpMean)^2) / sum(bpDist$freq)
bpSd <- sqrt(bpVar)
```

**Weighted Mean** of the frequency distribution is

``` r
bpMean
```

    ## [1] 128.2

**Weighted Variance** of the frequency distribution is

``` r
bpVar
```

    ## [1] 319.71

**Weighted Standard Deviation** of the frequency distribution is

``` r
bpSd
```

    ## [1] 17.88044

### Weighted Quantile

First we get the vector of all values in the frequency distribution.

``` r
bpVec <- rep(bpDist$bp, times = bpDist$freq)
bpVec
```

    ##   [1]  95.5  95.5  95.5  95.5  95.5 105.5 105.5 105.5 105.5 105.5 105.5
    ##  [12] 105.5 105.5 115.5 115.5 115.5 115.5 115.5 115.5 115.5 115.5 115.5
    ##  [23] 115.5 115.5 115.5 115.5 115.5 115.5 115.5 115.5 115.5 115.5 115.5
    ##  [34] 115.5 115.5 125.5 125.5 125.5 125.5 125.5 125.5 125.5 125.5 125.5
    ##  [45] 125.5 125.5 125.5 125.5 125.5 125.5 125.5 125.5 125.5 125.5 125.5
    ##  [56] 125.5 125.5 125.5 125.5 125.5 125.5 125.5 135.5 135.5 135.5 135.5
    ##  [67] 135.5 135.5 135.5 135.5 135.5 135.5 135.5 135.5 135.5 135.5 135.5
    ##  [78] 135.5 135.5 145.5 145.5 145.5 145.5 145.5 145.5 145.5 145.5 145.5
    ##  [89] 155.5 155.5 155.5 155.5 155.5 165.5 165.5 165.5 165.5 165.5 175.5
    ## [100] 175.5

Now we can get the different quantile values

``` r
quantile(bpVec, c(0,0.25,0.5,0.75,1))
```

    ##    0%   25%   50%   75%  100% 
    ##  95.5 115.5 125.5 135.5 175.5
