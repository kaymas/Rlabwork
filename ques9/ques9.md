Question 9
================
kaymas

**Program** Implement Binary Search
-----------------------------------

### Code

``` r
binarySearch <- function(v, ele, startIndex = 1, endIndex = length(v)){
  
  #needs v to be in ascending order
  while(startIndex <= endIndex){
    mid <- as.integer(floor((startIndex + endIndex) / 2))
    if(v[mid] > ele) endIndex = mid - 1
    else if(v[mid] < ele) startIndex = mid + 1
    else return(mid)
  }
  return(-1)
  
}
```

This is just to improve the output of the code to the console

``` r
bsExtend <- function(pos){
  if(pos == -1) cat("Element not found","\n")
  else cat("Element found at position:",pos,"\n")
}
```

### Examples

``` r
bsExtend(binarySearch(c(1,2,4,5,7,9),4))
```

    ## Element found at position: 3

``` r
bsExtend(binarySearch(c(1,2,4,5,7,9),8))
```

    ## Element not found

``` r
bsExtend(binarySearch(4,4))
```

    ## Element found at position: 1

``` r
bsExtend(binarySearch(4,8))
```

    ## Element not found

``` r
bsExtend(binarySearch("ab","ab"))
```

    ## Element found at position: 1

``` r
bsExtend(binarySearch(c("a","b","c","d"),"e"))
```

    ## Element not found
