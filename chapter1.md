---
title       : Insert the chapter title here
description : Insert the chapter description here

--- type:NormalExercise lang:r xp:100 skills:1 key:8fa7e2d6ac
## Sparklyr example

This is a `sparklyr` example from [rstudio's webiste](http://spark.rstudio.com/).

The pre exercise code connects to a local spark cluster, and stores this connection as `sc`.

*** =instructions
- Just hit submit answer.

*** =pre_exercise_code
```{r}
library(sparklyr)
sc <- spark_connect(master = "local")
```

*** =sample_code
```{r}
# sc is available

# Copy some data into spark cluster
library(dplyr)
iris_tbl <- copy_to(sc, iris)
flights_tbl <- copy_to(sc, nycflights13::flights, "flights")

# filtering example
flights_tbl %>% filter(dep_delay == 2)
```

*** =solution
```{r}
# sc is available

```

*** =sct
```{r}
success_msg("Good work!")
```
