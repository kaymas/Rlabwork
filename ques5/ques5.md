question 5
================
samyak

Program a function that outputs the largest element of the list
---------------------------------------------------------------

``` r
maxList <- function(l){
  maxLoc <- which.max(l)
  max <- l[[maxLoc]]
  return(max)
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

``` r
exList <- getRanList()
exMax <- maxList(exList)
print(exList)
```

    ## [[1]]
    ## [1] 15.81733
    ## 
    ## [[2]]
    ## [1] 14.52012
    ## 
    ## [[3]]
    ## [1] 79.97078
    ## 
    ## [[4]]
    ## [1] 34.50305

``` r
cat("Max number is:",exMax)
```

    ## Max number is: 79.97078
