Bank Account
================

Bank Account Simulation using scoping rules and mutable states
--------------------------------------------------------------

### Code

``` r
bank.account <- function(total){
  unit <- "$"
  list(
    deposit = function(amount){
      if(amount <= 0){
        return(cat("Deposit MUST be positive\n"))
      }
      total <<- total + amount
      return(cat(unit,amount,"successfully deposited. Your balance is:",unit,total,"\n"))
    },
    withdraw = function(amount){
      if(amount > total){
        return(cat("withdrawal amount cannot exceed balance\n"))
      }
      total <<- total - amount
      return(cat(unit,amount,"successfully withdrawn. Your balance is:",unit,total,"\n"))
    },
    balance = function(){
      return(cat("Your balance is",unit,total,"\n"))
    }
  )
}
```

### Example

Initialize

``` r
sam <- bank.account(100)
ash <- bank.account(100)
```

Transactions

``` r
sam$withdraw(20)
```

    ## $ 20 successfully withdrawn. Your balance is: $ 80

``` r
ash$deposit(100)
```

    ## $ 100 successfully deposited. Your balance is: $ 200

``` r
ash$withdraw(500)
```

    ## withdrawal amount cannot exceed balance

``` r
ash$balance()
```

    ## Your balance is $ 200

``` r
sam$balance()
```

    ## Your balance is $ 80
