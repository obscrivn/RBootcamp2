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
## Rows and Columns
- To retrieve data from the rows and columns, you need to use `[ ]`
- ` [1,2] ` has two coordinates: the first is a **row**, the second is a **column** - ` [ row1, column2 ] `
- ` [1,] ` for the entire row, the second coordinate is empty
- ` [, 1] ` for the entire column, the first coordinate is empty
- You can retrieve rows and columns using their names
- Example: ` mytable[, "age"] ` will extract the entire column named **age**
 
*** =instructions
- You will import a built-in dataset **mtcars**
- In the **console** type  ` data(mtcars) `
- Type ` head(mtcars) ` access the first 6 rows
- What is the value of the cell in the row # 3 and the column # 2? Type it in your script.
- Extract the same value now using ` [ ] `
- Extract the entire first row (remember to use ` [ ] `)
- Extract the entire second column
- Type the command ` colnames(mtcars) `. Look at the name of the first column.
- Extract the entire first column using column name

*** =hint
 Remember quotes and the order - [row, column]

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Load dataset
data(mtcars)

# The value of cell in the row 3 and column 2
cell <- 

# Extract the cell from row 3 and column 2 using [ ]


#Extract the entire 1st row


# Extract the entire 2nd column


# Extract cell from row 2 and column 3


# Extract the entire column by its name

```
*** =solution
```{r}
# Load dataset
data(mtcars)

# The value of cell in the row 3 and column 2
cell <- 4

# Extract the cell from row 3 and column 2 using [ ]
mtcars[3, 2]

#Extract the entire 1st row
mtcars[1,]

# Extract the entire 2nd column
mtcars[,2]

# Extract the entire column by its name
mtcars[,"mpg"]
```

*** =sct
```{r}
test_object("cell", incorrect_msg = "try again")
test_output_contains("mtcars[3, 2]", incorrect_msg = "try again")
test_output_contains("mtcars[1,]", incorrect_msg = "try again")
test_output_contains("mtcars[,2]", incorrect_msg = "try again")
test_output_contains("mtcars[,\"mpg\"]", incorrect_msg = "try again")
success_msg("Great!")
```
--- type:MultipleChoiceExercise xp:50 skills:1 key:8f5314f41c

## Useful Data Frame Functions Quiz
Select the correct answer to represent the following tasks:

1. calculate the first 6 rows
2. calculate the number of columns
3. extract the names of the columns
4. calculate the number of rows

If you are unfamiliar with some functions, please use ` ?help ` in the console to learn about the function (ex. ` ?length `)
*** =instructions
- head(mydata), nrow(mydata), colnames(mydata), ncol(mydata)
- head(mydata), ncol(mydata), nrow(mydata), colnames(mydata)
- head(mydata), ncol(mydata), colnames(mydata), nrow(mydata) 


*** =sct
```{r}
msg1 = "Try again"
msg2 = "Try again"
msg3 = "Well done"
test_mc(correct = 3, feedback_msgs = c(msg1,msg2,msg3))
```

