Question 8
================
kaymas

**Program:** Implement Linear Search
------------------------------------

### Code

``` r
linearSearch <- function(v, el){
  n <- length(v)
  for(i in 1:n){
    if(identical(v[i], el)) return (i)
  }
  return (-1)
}
```

### Examples

``` r
spot = linearSearch(c("ba", "as", "sa"), "as")
if(identical(spot, -1)){
  cat("element not found","\n")
}else{
  cat("Element found at position", spot, "\n")
}
```

    ## Element found at position 2

``` r
spot = linearSearch(c(12, 45, 64.6, 98.2, 22.1), 64.6)
if(identical(spot, -1)){
  cat("element not found","\n")
}else{
  cat("Element found at position", spot, "\n")
}
```

    ## Element found at position 3

``` r
spot = linearSearch(c("ba","as","sa"), 64.6)
if(identical(spot, -1)){
  cat("element not found","\n")
}else{
  cat("Element found at position", spot, "\n")
}
```

    ## element not found
