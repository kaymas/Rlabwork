Question 4
================
kaymas

Program that prints multiplication table of a number from 1 till 12
-------------------------------------------------------------------

### Code

``` r
mulTable <- function(i, num){
  res <- c()
  for(iterator in 1:i){
    res <- c(res,paste(iterator,"*",num,"=",iterator*num))
  }
  return(res)
}
```

##### Imitating input from user for this particular program(numbers are from 1 to 20)

``` r
inputFromUser <- function(){
  num <- floor(runif(1,min = 1, max = 20))
  return(num) 
}
```

##### Formating Output

``` r
fmt.output <- function(vec){
  cat(paste(vec,collapse = "\n"),"\n")

}
```

### Examples

``` r
fmt.output(mulTable(12,inputFromUser()))
```

    ## 1 * 19 = 19
    ## 2 * 19 = 38
    ## 3 * 19 = 57
    ## 4 * 19 = 76
    ## 5 * 19 = 95
    ## 6 * 19 = 114
    ## 7 * 19 = 133
    ## 8 * 19 = 152
    ## 9 * 19 = 171
    ## 10 * 19 = 190
    ## 11 * 19 = 209
    ## 12 * 19 = 228

``` r
fmt.output(mulTable(12,inputFromUser()))
```

    ## 1 * 2 = 2
    ## 2 * 2 = 4
    ## 3 * 2 = 6
    ## 4 * 2 = 8
    ## 5 * 2 = 10
    ## 6 * 2 = 12
    ## 7 * 2 = 14
    ## 8 * 2 = 16
    ## 9 * 2 = 18
    ## 10 * 2 = 20
    ## 11 * 2 = 22
    ## 12 * 2 = 24

``` r
fmt.output(mulTable(12,inputFromUser()))
```

    ## 1 * 12 = 12
    ## 2 * 12 = 24
    ## 3 * 12 = 36
    ## 4 * 12 = 48
    ## 5 * 12 = 60
    ## 6 * 12 = 72
    ## 7 * 12 = 84
    ## 8 * 12 = 96
    ## 9 * 12 = 108
    ## 10 * 12 = 120
    ## 11 * 12 = 132
    ## 12 * 12 = 144
