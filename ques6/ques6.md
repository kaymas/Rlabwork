Question 6
================
samyak

Program to calculate the running total of a list
------------------------------------------------

### Code

``` r
runningTotal <- function(l){
  v <- unlist(l, use.names = FALSE)
  return(cumsum(v))
}
```

##### Generating a random number

``` r
ranNum <- function(min,max,isInt = TRUE){
  num <- runif(1,min = min, max = max)
  if(isInt == TRUE){
    num <- floor(num)
  }
  return(num) 
}
```

##### Generating a list

``` r
getRanList <- function(){
  genList <- list()
  size <- ranNum(4,10)
  for(i in 1:size){
    genList[[i]] <- ranNum(1,100,FALSE)
  }
  return(genList)
}
```

### Examples

##### Example 1

``` r
tempList <- getRanList()
tempVec <- runningTotal(tempList)
tempList
```

    ## [[1]]
    ## [1] 7.65396
    ## 
    ## [[2]]
    ## [1] 73.67649
    ## 
    ## [[3]]
    ## [1] 34.77581
    ## 
    ## [[4]]
    ## [1] 66.367

``` r
cat("running total is:",tempVec,"\n")
```

    ## running total is: 7.65396 81.33045 116.1063 182.4733

##### Example 2

``` r
tempList <- getRanList()
tempVec <- runningTotal(tempList)
tempList
```

    ## [[1]]
    ## [1] 72.50601
    ## 
    ## [[2]]
    ## [1] 29.15686
    ## 
    ## [[3]]
    ## [1] 88.85447
    ## 
    ## [[4]]
    ## [1] 50.62044
    ## 
    ## [[5]]
    ## [1] 82.64126
    ## 
    ## [[6]]
    ## [1] 49.01605
    ## 
    ## [[7]]
    ## [1] 22.30829

``` r
cat("running total is:",tempVec,"\n")
```

    ## running total is: 72.50601 101.6629 190.5173 241.1378 323.779 372.7951 395.1034

##### Example 3

``` r
tempList <- getRanList()
tempVec <- runningTotal(tempList)
tempList
```

    ## [[1]]
    ## [1] 50.37978
    ## 
    ## [[2]]
    ## [1] 40.42404
    ## 
    ## [[3]]
    ## [1] 50.14151
    ## 
    ## [[4]]
    ## [1] 1.174984
    ## 
    ## [[5]]
    ## [1] 14.76222
    ## 
    ## [[6]]
    ## [1] 12.60443
    ## 
    ## [[7]]
    ## [1] 24.12517
    ## 
    ## [[8]]
    ## [1] 89.5781

``` r
cat("running total is:",tempVec,"\n")
```

    ## running total is: 50.37978 90.80382 140.9453 142.1203 156.8825 169.487 193.6121 283.1902
