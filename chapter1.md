---
title       : Insert the chapter title here
description : Insert the chapter description here

--- type:NormalExercise lang:r xp:100 skills:1 key:8fa7e2d6ac
## Sparklyr example

Sparklyr example

*** =instructions
- Hit submit answer!

*** =pre_exercise_code
```{r}
'___BLOCK_SOLUTION_EXEC___'
```

*** =sample_code
```{r}
# Set up
library(sparklyr)
sc <- spark_connect(master = "local")

# Copy data to cluster
iris_tbl <- copy_to(sc, iris)

# Filtering example
library(dplyr)
iris_tbl %>% filter(Sepal_Length > 4)

# Close connection
spark_disconnect(sc)
```

*** =solution
```{r}
# empty
```

*** =sct
```{r}
success_msg("That's it")
```
