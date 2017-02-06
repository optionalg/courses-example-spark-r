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
'___BLOCK_SOLUTION_EXEC___'
library(sparklyr)
sc <- spark_connect(master = "local")
```

*** =sample_code
```{r}
# sc is available

# Copy some data into spark cluster
iris_tbl <- copy_to(sc, iris)

# filtering example
iris_tbl %>% filter(Sepal_Length > 4)
```

*** =solution
```{r}
# sc is available

```

*** =sct
```{r}
success_msg("Good work!")
```
