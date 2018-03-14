Question 6
================
kaymas

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
    ## [1] 80.7438
    ## 
    ## [[2]]
    ## [1] 92.80601
    ## 
    ## [[3]]
    ## [1] 37.88527
    ## 
    ## [[4]]
    ## [1] 4.393942
    ## 
    ## [[5]]
    ## [1] 7.872482

``` r
cat("running total is:",tempVec,"\n")
```

    ## running total is: 80.7438 173.5498 211.4351 215.829 223.7015

##### Example 2

``` r
tempList <- getRanList()
tempVec <- runningTotal(tempList)
tempList
```

    ## [[1]]
    ## [1] 95.3675
    ## 
    ## [[2]]
    ## [1] 67.76947
    ## 
    ## [[3]]
    ## [1] 16.88966
    ## 
    ## [[4]]
    ## [1] 66.03476
    ## 
    ## [[5]]
    ## [1] 52.41585

``` r
cat("running total is:",tempVec,"\n")
```

    ## running total is: 95.3675 163.137 180.0266 246.0614 298.4772

##### Example 3

``` r
tempList <- getRanList()
tempVec <- runningTotal(tempList)
tempList
```

    ## [[1]]
    ## [1] 64.45704
    ## 
    ## [[2]]
    ## [1] 80.05411
    ## 
    ## [[3]]
    ## [1] 76.82325
    ## 
    ## [[4]]
    ## [1] 58.92784
    ## 
    ## [[5]]
    ## [1] 57.09358
    ## 
    ## [[6]]
    ## [1] 30.19767
    ## 
    ## [[7]]
    ## [1] 73.83124

``` r
cat("running total is:",tempVec,"\n")
```

    ## running total is: 64.45704 144.5111 221.3344 280.2622 337.3558 367.5535 441.3847
