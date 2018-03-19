Remove NA from matrix
================
kaymas

How to remove NA values from a matrix
-------------------------------------

Suppose that you have a matrix like:

    ##      [,1] [,2] [,3] [,4]
    ## [1,]   NA   NA   72   81
    ## [2,]   NA   41   35   23
    ## [3,]    5   NA   84    6
    ## [4,]    5   57   23   16
    ## [5,]   21   64   85   52

**First** we want to identify all the NAs in the matrix. To do so we can use the `is.na()` function that takes the matrix as the argument and returns a matrix with logical values of FALSE at positions that contains NA.

``` r
is.na(dataMat)
```

    ##       [,1]  [,2]  [,3]  [,4]
    ## [1,]  TRUE  TRUE FALSE FALSE
    ## [2,]  TRUE FALSE FALSE FALSE
    ## [3,] FALSE  TRUE FALSE FALSE
    ## [4,] FALSE FALSE FALSE FALSE
    ## [5,] FALSE FALSE FALSE FALSE

**Second** we want to check the matrix returned by the function `is.na()` to remove any row that contains FALSE. To do this we can use the `apply()` function that takes 3 major arguments:

1.  X -&gt; an array or a matrix
2.  MARGIN -&gt; a vector used to tell if we want to apply the fucntion over the rows(indicated by 1) or the columns(indicated by 2) or both rows and columns(indicated by `c(1,2)` ).
3.  FUN -&gt; the function to be applied

``` r
naRows <- apply(is.na(dataMat),1,any)
```

apply returns a vector of logical values telling the the result of the function any applied to each row of the matrix.

**Third** we have to select the rows from the data matrix that doesn't contain NA

``` r
dataMat[!naRows,]
```

    ##      [,1] [,2] [,3] [,4]
    ## [1,]    5   57   23   16
    ## [2,]   21   64   85   52
