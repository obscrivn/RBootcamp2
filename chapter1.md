---
title       : Chapter 1
description : Data Frames

--- type:NormalExercise xp:50 skills:1 key:3c1cd8a7c3
## Data frame definition
* **Data frame** stores data tables
* It contains vectors of equal length
* ` data.frame() ` is a function to create a data frame


*** =instructions
-In the code, you have an example how to create a data frame with two columns

-Add another vector with the values **5,6,7**

-Create a data frame with **d1**, **d2** and **d3**.


*** =hint


*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
d1 <- c(1,2,3)
d2 <- c(3,4,5)
dataframe1 <- data.frame(d1,d2)

#create a numeric vector
d3 <- 

#create a data frame
dataframe2 

```

*** =solution
```{r}
d1 <- c(1,2,3)
d2 <- c(3,4,5)
dataframe1 <- data.frame(d1,d2)

#create a numeric vector
d3 <- c(5,6,7)

#create a data frame
dataframe2 <- data.frame(d1,d2,d3)

```

*** =sct
```{r}
test_object("d3", incorrect_msg = "Make sure you use c()")
test_object("dataframe2", incorrect_msg = "Make sure you use data.frame")
success_msg("Great!")
```

--- type:MultipleChoiceExercise xp:50 skills:1 key:14288e1b24

*** =instructions
#- logical
#- character
#- numeric


*** =sct
```{r}
#msg1 = "Try again! Think about quotes"
#msg2 = "Well done. Proceed to the next exercise"
#msg3 = "Try again! Think about quotes"
#test_mc(correct = 2, feedback_msgs = c(msg1,msg2,msg3))
```
