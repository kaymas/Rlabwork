Question 11
================
kaymas

**Program** To find basic statistical information about students enrolled in a course.
--------------------------------------------------------------------------------------

The initial data set given in the question is
`20 20 20 20 20 21 21 21 22 22 22 22 23 23 23`

Now, R provides built in functions for finding mean and median but none for finding mode or modal value. So here we define it ourselves.

``` r
modal <- function(data.vector){
  unique.elements <- unique(data.vector)
  modal.value <- unique.elements[which.max(table(data.vector))]
  return (modal.value)
}
```

Here
+ `unique` function outputs the unique elements of the data vector.
+ `which.max` function determines the *location* of the **first** maximum element of the data vector
+ `table` function in this context calculates the frequency of the levels of the data vector

### Part - 1

#### Median age of all students under 22 years

``` r
median(age[age < 22])
```

    ## [1] 20

### Part - 2

#### Median age of all students

``` r
median(age)
```

    ## [1] 21

### Part - 3

#### Mean age of all students

``` r
mean(age)
```

    ## [1] 21.33333

### Part - 4

#### Modal age for all students

``` r
modal(age)
```

    ## [1] 20

### Part - 5

#### Mean, Median, Modal age of all students when 2 new students, both of age 23, are added to data set.

``` r
age <- c(age, c(23,23))
mean(age)
```

    ## [1] 21.52941

``` r
median(age)
```

    ## [1] 22

``` r
modal(age)
```

    ## [1] 20
