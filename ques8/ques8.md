Question 8
================
samyak

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

This is just to improve the output of the code to the console

``` r
lsExtend <- function(pos){
  if(pos == -1) cat("Element not found","\n")
  else cat("Element found at position:",pos,"\n")
}
```

### Examples

``` r
lsExtend(linearSearch(c("ba", "as", "sa"), "as"))
```

    ## Element found at position: 2

``` r
lsExtend(linearSearch(c(12, 45, 64.6, 98.2, 22.1), 64.6))
```

    ## Element found at position: 3

``` r
lsExtend(linearSearch(64.6, 64.6))
```

    ## Element found at position: 1

``` r
lsExtend(linearSearch(c("ba","as","sa"), 64.6))
```

    ## Element not found
