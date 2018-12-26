# Analysis of Iris Dataset in R Programming
Iris dataset analysis using R Programming and R Studio.

# Demo
[Demo](https://github.com/MuhammadBilalYar/Analysis-of-Iris-Dataset-in-R-Programming/blob/master/Demo.mp4)

# Code
load 'multigraph' library
```
library(multigraph)
```

load Iris dataset as matrix in matrix variable
```
matrix <- data.matrix(iris)
```

matrix transpose beacuse 'cor' method calcualte column wise correlation 
```
trn<-t(matrix)
```

calcaulate pairwise correlation (150*150) in pwcor variable
```
pwcor<-cor(trn)
```

save calculated (150*150) correlation in csv file
```
write.csv(pwcor, file = "correlation.csv")
```
define scope of node / edge / graph characteristics as list object
```
scp3 <- list(cex = 1, fsize = 3, pch = c(19, 15), lwd = 1.5, vcol = 2:3)
```
Map pairwise correlation (150*150) to 'circ2' layout base graph
```
bmgraph(pwcor, layout = "circ2", scope = scp3, main = "Iris correlation using bmgraph")
```
calculate mean, median and summary
```
mean(pwcor)
median(pwcor)
summary(pwcor)
```
