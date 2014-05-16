# maacs file for second week lectures - Exploratory Data Analysis 
### John Hopkins School of Public Health through Coursera Platform

Data were extracted from [maacs_env][1] and [amelia][2]
[1]:  https://github.com/jtleek/modules/blob/master/04_ExploratoryAnalysis/PlottingLattice/maacs_env.rds
[2]: https://github.com/jtleek/jhsph753and4/blob/master/lectures/EBDA/problem3.rda

```r
# Change working directory setwd('EDA/Weeks/Week2/Data')

# Read the data
env <- readRDS("maacs_env.rds")
problem3 <- load("problem3.rda")

id <- 1:750
maacs <- data.frame(id, maacs, env)

# Select only the following columns: id, eno, duBedMusM, pm25 and mopos
maacs <- maacs[c("id", "eno", "duBedMusM", "pm25", "mopos")]

# Save maacs data frame
save(maacs, file = "maacs.Rda")
```


