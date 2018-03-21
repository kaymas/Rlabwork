Question 4
================
kaymas

Program that prints multiplication table of a number from 1 till 12
-------------------------------------------------------------------

### Code

``` r
mulTable <- function(i, num){
  return(paste(1:i,"*",num,"=",outer(1:i,num)))
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
  cat(vec,sep = "\n")
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

    ## 1 * 17 = 17
    ## 2 * 17 = 34
    ## 3 * 17 = 51
    ## 4 * 17 = 68
    ## 5 * 17 = 85
    ## 6 * 17 = 102
    ## 7 * 17 = 119
    ## 8 * 17 = 136
    ## 9 * 17 = 153
    ## 10 * 17 = 170
    ## 11 * 17 = 187
    ## 12 * 17 = 204

``` r
fmt.output(mulTable(12,inputFromUser()))
```

    ## 1 * 3 = 3
    ## 2 * 3 = 6
    ## 3 * 3 = 9
    ## 4 * 3 = 12
    ## 5 * 3 = 15
    ## 6 * 3 = 18
    ## 7 * 3 = 21
    ## 8 * 3 = 24
    ## 9 * 3 = 27
    ## 10 * 3 = 30
    ## 11 * 3 = 33
    ## 12 * 3 = 36
