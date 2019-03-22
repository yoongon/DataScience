# R Basic

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
