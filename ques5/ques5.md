question 5
================
kaymas

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
    ## [1] 63.45452
    ## 
    ## [[2]]
    ## [1] 18.7086
    ## 
    ## [[3]]
    ## [1] 14.59623
    ## 
    ## [[4]]
    ## [1] 38.14533
    ## 
    ## [[5]]
    ## [1] 19.08932
    ## 
    ## [[6]]
    ## [1] 54.46048
    ## 
    ## [[7]]
    ## [1] 96.49715
    ## 
    ## [[8]]
    ## [1] 4.710771
    ## 
    ## [[9]]
    ## [1] 17.79006

``` r
cat("Max number is:",exMax)
```

    ## Max number is: 96.49715
