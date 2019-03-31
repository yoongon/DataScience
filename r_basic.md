# R Basic
[Lecture]: https://www.youtube.com/playlist?list=PLu1f0b2x0aaskPNUuoGBidnQ7eazA1GUw

### Installation
Install guide: [DataCamp](https://www.datacamp.com/community/tutorials/installing-R-windows-mac-ubuntu)

ex) Linux(Ubuntu)
```sh
$ sudo apt-get install r-base
```

### variable
```sh
$ x <- 1
$ y <- 2
$ x + y
$ x * y
```

### basic function
```sh
$ seq(3)
$ sum(1,3)
$ max(1, 3, 5)
$ min(1, 5, 3)
$ log(10)
$ log2(2)
$ sqrt(16)
$ exp(4)
```

### nested function
```sh
$ sum(seq(3))
$ exp(log(10))
```

### install, library
```sh
$ install.packages("dslabs")
$ library(dslabs)
```

### class, name, head
```sh
$ class(murders)
$ names(murders)
$ head(murders)
```

### indexing
```sh
$ murders$state
$ murders$abb
$ murders$region
$ murders$population
$ murders$total
```
### factors
```sh
$ class(murders$region)
$ levels(murders$region)
```
### vectors
```sh
$ c(1,2,3,4,5)
$ c("a", "b", "c", "d")
```

### sequence
```sh
$ 1:100
$ seq(1,10,2)
```

### subset
```sh
$ money <- c(100, 300, 200, 400)
$ snack <- c("ice", "choco", "candy")
$ class(snack)
$ names(money)
$ names(money) <- snack
$ money[1:3]
```

### coercion
```sh
$ c(1,2,3,"a")
$ as.numeric(c(1,2,3,"a"))
$ as.character(c(1,2,3))
```

### sort
```sh
$ sort(c(4,2,3,1,9,8,7))
```
### rank
```sh
$ rank(c(13, 30, 20, 11))
```

### order
```sh
$ test <- c(30, 10, 20)
$ order(test)
```

### rank (murders)
```
$ library(dslabs)
$ head(murders)
$ states <- murders$state
$ rank <- rank(murders$population)
$ data.frame(names=states, rank=rank)
```

### which
```sh
$ states[which.min(murders$population)]
$ states[which.max(murders$population)]
```

### vector arithmetic
```sh
$ test <- 1:100
$ sum(test^3)

$ ind <- which.max(murders$total)
$ murders[ind]

$ murders$state[which.max(murders$total/murders$population)]
```

### filtering
```sh
$ idx <- murders$region == "South"
$ murders$state[idx]
```

### match
```sh
$ ind <- match(c("CA", "NY"), murders$abb)
$ murders$state[ind]
```

### %in%
```sh
$ c("CA", "NY") %in% murders$abb
$ ind <- murders$abb %in% c("CA", "NY")
$ murders$state[ind]
```

### !
```sh
$ ind <- murders$region == "South"
$ murders$state[!ind]
```

### install dplyr
```sh
$ install.packages(“dplyr”)
```

### mutate
```sh
$ murders <- mutate(murders, rate = total/population)
```

### select
```sh
$ select(murders, state, population)
```

### filter
```sh
$ filter(murders, region=="West")
```

### pipe
```sh
$ mutate(murders, rate = total / population * 100000, rank = rank(-rate)) %>% select(state, rate, rank)
```

### plot
```sh
$ plot(murders$population/10^6, murders$total)
```

### hist
```sh
$ hist(murders$population/10^6)
```

### boxplot
```sh
$ boxplot(total~region, data = murders)
```

### function
```sh
$ sample_func <- function(x) {
    y <- -1 * x
    y
}
```

### if
```sh
$ check <- function(x) {
    if (x>0) {
        print ("plus")
    } else {
        print ("minus")
    }
}
```

### ifelse
```sh
$ idx <- ifelse(murders$population> 10000000, TRUE, FALSE)
$ murders$state[idx]
```

### for
```sh
$ n <- 100
$ data <- vector("numeric", n)
$ for (i in 1:n) {
    data[i] <- i^2
}
```
