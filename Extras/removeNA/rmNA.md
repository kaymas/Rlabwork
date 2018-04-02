Remove NA from matrix
================
kaymas

How to remove NA values from a matrix
-------------------------------------

Suppose that you have a matrix like:

    ##      [,1] [,2] [,3] [,4]
    ## [1,]   NA   NA   12    5
    ## [2,]   NA   40   93    8
    ## [3,]    9   NA   81   29
    ## [4,]   39   43   38   56
    ## [5,]   38   74   12   91

**First** we want to identify all the NAs in the matrix. To do so we can use the `is.na()` function that takes the matrix as the argument and returns a matrix with logical values of TRUE at positions that contains NA.

``` r
is.na(dataMat)
```

    ##       [,1]  [,2]  [,3]  [,4]
    ## [1,]  TRUE  TRUE FALSE FALSE
    ## [2,]  TRUE FALSE FALSE FALSE
    ## [3,] FALSE  TRUE FALSE FALSE
    ## [4,] FALSE FALSE FALSE FALSE
    ## [5,] FALSE FALSE FALSE FALSE

**Second** we want to check the matrix returned by the function `is.na()` to remove any row that contains TRUE To do this we can use the `apply()` function that takes 3 major arguments:

1.  X -&gt; an array or a matrix
2.  MARGIN -&gt; a vector used to tell if we want to apply the fucntion over the rows(indicated by 1) or the columns(indicated by 2) or both rows and columns(indicated by `c(1,2)` ).
3.  FUN -&gt; the function to be applied

``` r
naRows <- apply(is.na(dataMat),1,any)
naRows
```

    ## [1]  TRUE  TRUE  TRUE FALSE FALSE

apply returns a vector of logical values telling the the result of the function `any()` applied to each row of the matrix.

**Third** we have to select the rows from the data matrix that doesn't contain NA

``` r
dataMat[!naRows,]
```

    ##      [,1] [,2] [,3] [,4]
    ## [1,]   39   43   38   56
    ## [2,]   38   74   12   91

here the logical NOT `!` in front of the vector `naRows` indicates that we want to retrieve the elements other than the elements for which `naRows` has the value TRUE.
