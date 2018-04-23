Question 4
================
samyak

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

    ## 1 * 5 = 5
    ## 2 * 5 = 10
    ## 3 * 5 = 15
    ## 4 * 5 = 20
    ## 5 * 5 = 25
    ## 6 * 5 = 30
    ## 7 * 5 = 35
    ## 8 * 5 = 40
    ## 9 * 5 = 45
    ## 10 * 5 = 50
    ## 11 * 5 = 55
    ## 12 * 5 = 60

``` r
fmt.output(mulTable(12,inputFromUser()))
```

    ## 1 * 7 = 7
    ## 2 * 7 = 14
    ## 3 * 7 = 21
    ## 4 * 7 = 28
    ## 5 * 7 = 35
    ## 6 * 7 = 42
    ## 7 * 7 = 49
    ## 8 * 7 = 56
    ## 9 * 7 = 63
    ## 10 * 7 = 70
    ## 11 * 7 = 77
    ## 12 * 7 = 84

``` r
fmt.output(mulTable(12,inputFromUser()))
```

    ## 1 * 11 = 11
    ## 2 * 11 = 22
    ## 3 * 11 = 33
    ## 4 * 11 = 44
    ## 5 * 11 = 55
    ## 6 * 11 = 66
    ## 7 * 11 = 77
    ## 8 * 11 = 88
    ## 9 * 11 = 99
    ## 10 * 11 = 110
    ## 11 * 11 = 121
    ## 12 * 11 = 132
