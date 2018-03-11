Question 7
================
kaymas

**Program:** Write a function that tests whether a string is a palindrome
-------------------------------------------------------------------------

The entire code is written below for you to check out, but if you want the explanation it is at the end.

``` r
is.palindrome <- function(word){
  identical(word, paste(rev(strsplit(word,"")[[1]]), collapse = ""))
}
```

### Examples

``` r
is.palindrome("karatsuba")
```

    ## [1] FALSE

``` r
is.palindrome("nur ses run")
```

    ## [1] TRUE

``` r
is.palindrome("evilolive")
```

    ## [1] TRUE

Output of `is.palindrome("karatsuba")` is FALSE
Output of `is.palindrome("nur ses run")` is TRUE
Output of `is.palindrome("evilolive")` is TRUE

### Explanation

Starting from the outside

-   The **identical** function is used to reliably test if two objects are exact equal. It returns `TRUE` in this case and `FALSE` in every other case. Now the input string `word` and the string returned by the paste function are tested for equality.

-   The **paste** function converts its arguments to character strings and then concatenates them. collapse and sep are two arguments that can be passed to the paste function and its working can be shown as :

``` r
nth <- paste(1:12, c("st","nd","rd",rep("th",9)), sep="")
paste(month.abb, "is the", nth, "month", sep = " ", collapse = "; ")
```

    ## [1] "Jan is the 1st month; Feb is the 2nd month; Mar is the 3rd month; Apr is the 4th month; May is the 5th month; Jun is the 6th month; Jul is the 7th month; Aug is the 8th month; Sep is the 9th month; Oct is the 10th month; Nov is the 11th month; Dec is the 12th month"

-   The **rev** function is used to provide the revered version of its arguments. It's argument can be a vector or any other object for which reversal is required. For example:

``` r
rev(nth)
```

    ##  [1] "12th" "11th" "10th" "9th"  "8th"  "7th"  "6th"  "5th"  "4th"  "3rd" 
    ## [11] "2nd"  "1st"

-   The **strsplit** function is used to split the elements of a character vector `x` according to the matches to the substring `split` within them. Now if `split` is of length 0, then the character vector `x` is split into single character. For example: (here `head` is used to take the first 3 elements of `nth`)

``` r
strsplit(head(nth,3), "")
```

    ## [[1]]
    ## [1] "1" "s" "t"
    ## 
    ## [[2]]
    ## [1] "2" "n" "d"
    ## 
    ## [[3]]
    ## [1] "3" "r" "d"
