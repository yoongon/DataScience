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
