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
library(sparklyr)
# Connect to remove cluster.
# sc <- spark_connect(master = "local")
```

*** =sample_code
```{r}
# sc is available

# Load dplyr
library(dplyr)

# Reference iris data (at )
iris_tbl <- iris

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
