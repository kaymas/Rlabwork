Question 10
================
kaymas

Program to implement matrices addition, subtraction, and multiplication
-----------------------------------------------------------------------

Writing a function to get a random 2x2 matrix

``` r
getMatrix <- function(){
  tempMat = matrix(sample(-10:10, size = 4, replace = TRUE), nrow = 2, ncol = 2)
  return (tempMat)
}
```

### Matrix Addition

``` r
A <- getMatrix()
B <- getMatrix()
```

Matrix A is

    ##      [,1] [,2]
    ## [1,]    7   -1
    ## [2,]   -8    1

Matrix B is

    ##      [,1] [,2]
    ## [1,]    3   -6
    ## [2,]   -9    9

Sum of A and B is

``` r
A + B
```

    ##      [,1] [,2]
    ## [1,]   10   -7
    ## [2,]  -17   10

### Matrix Difference

``` r
A <- getMatrix()
B <- getMatrix()
```

Matrix A is

    ##      [,1] [,2]
    ## [1,]    8   -5
    ## [2,]   -6    2

Matrix B is

    ##      [,1] [,2]
    ## [1,]    5   -1
    ## [2,]    9    7

Difference of A and B is

``` r
A - B
```

    ##      [,1] [,2]
    ## [1,]    3   -4
    ## [2,]  -15   -5

### Matrix Multiplication

``` r
A <- getMatrix()
B <- getMatrix()
```

Matrix A is

    ##      [,1] [,2]
    ## [1,]    1   -9
    ## [2,]   -1    1

Matrix B is

    ##      [,1] [,2]
    ## [1,]    4   -1
    ## [2,]    8    9

Sum of A and B is

``` r
A %*% B
```

    ##      [,1] [,2]
    ## [1,]  -68  -82
    ## [2,]    4   10
