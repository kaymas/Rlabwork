Question 3
================
kaymas

Program that asks the user for a number n and then prints the ouput as sum of numbers from 1 to n
-------------------------------------------------------------------------------------------------

### Code

``` r
sum.n <- function(n){
  sum <- 0
  for(i in 1:n) sum = sum + i
  return(sum)  
}
```

##### Imitating input from user for this particular program

``` r
inputFromUser <- function(){
  num <- floor(runif(1,min = 1, max = 100))
  return(num) 
}
```

##### Formating Output

``` r
fmt.output <- function(num,val){
  cat("Sum of numbers from",1,"to",num,"is :",val,"\n")
}
```

### Examples

``` r
x = inputFromUser()
fmt.output(x, sum.n(x))
```

    ## Sum of numbers from 1 to 25 is : 325

``` r
x = inputFromUser()
fmt.output(x, sum.n(x))
```

    ## Sum of numbers from 1 to 46 is : 1081

``` r
x = inputFromUser()
fmt.output(x, sum.n(x))
```

    ## Sum of numbers from 1 to 82 is : 3403

``` r
x = inputFromUser()
fmt.output(x, sum.n(x))
```

    ## Sum of numbers from 1 to 15 is : 120
