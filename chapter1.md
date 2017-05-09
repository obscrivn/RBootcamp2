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
--- type:NormalExercise xp:150 skills:1 key:d4d5230313
## Row and Columns
- To retrieve data from the rows and columns, you need to use `[ ]`
- ` [1,2] ` has two coordinates: the first is a **row**, the second is a **column**
- ` [1,] ` for the entire row, the second coordinate is empty
- ` [, 1] ` for the entire column, the first coordinate is empty
 
*** =instructions
- You have a dataset **mtcars** (data(mtcars) function import the built-in data)
- Use ` head() ` function to access the first 6 rows
- Use ` tail() ` function to access to last 6 rows
- Extract the entire first row (remember to use ` [ ] `)
- Extract the entire second column
- Extract the cell from the second row and third column

*** =hint


*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Load dataset
mydata <- data(mtcars)

# Extract the first 6 rows


# Extract the last 6 rows


#Extract the entire 1st row


# Extract the entire 2nd column


# Extract cell from row 2 and column 3


```
*** =solution
```{r}
# Load dataset
mydata <- data(mtcars)

# Extract the first 6 rows
head(mydata)

# Extract the last 6 rows
tail(mydata)

#Extract the entire 1st row
#mydata[1,]

# Extract the entire 2nd column
#mydata[,2]

# Extract cell from row 2 and column 3
#mydata[2,2]
```

*** =sct
```{r}
test_output_contains("head(mydata)", incorrect_msg = "try again")
test_output_contains("tail(mydata)", incorrect_msg = "try again")
test_output_contains("mydata[1,]", incorrect_msg = "try again")
test_output_contains("mydata[,2]", incorrect_msg = "try again")
test_output_contains("mydata[2,3]", incorrect_msg = "try again")
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
