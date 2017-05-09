---
title       : Chapter 2
description : Data Frame Modification
  
--- type:NormalExercise xp:200 skills:1 key:db082273b2
## Manipulating Data Frame

- Logical operators are useful to retrieve data based on a condition
- Operators are ` > `, ` <= `, ` >= `
- Review operators here if needed [operators list](http://www.statmethods.net/management/operators.html)
- You can specify a condition for a column value
- Example: ` mydata["Age" < 55, ] ` or ` mydata[mydata$Age < 55, ] `
- ` & ` means AND
- Example ` mydata[("Age" < 55 & "Gender" == "F"),] `

*** =instructions

- Find the column names of your data set **mtcars**
- Create a new data frame **mydata** by retrieving two columns **cyl** **disp**. Since you are extracting two columns, you need to use a vector (for more help - review this page [column slicing](http://www.r-tutor.com/r-introduction/data-frame/data-frame-column-slice)
- Use help function in the console to learn about ` summary() ` (remember to use question mark)
- Apply this function to **mydata**
- Examine the use of ` attach() ` function in the console help menu
- We are going to use ` attach ` so that we can simply type the names of columns
- Retrieve only cylinders that are greater than 4
- Retrieve cyl that are greater than 4 **and** disp is less than 400 (use ` & ` for **and**)

*** =hint
the column name is "cyl"

*** =pre_exercise_code
```{r}
library(plyr)
library(magrittr)
```

*** =sample_code
```{r}
data(mtcars)
# Fill in the coordinates (colnames) inside the brackets
mydata <- mtcars[]

#summary

# attaching data
attach(mydata)

# cylinders are greater than 4


# cyl is greater than 4 and disp is less than 400

```

*** =solution
```{r}
data(mtcars)
# Fill in the coordinates (colnames) inside the brackets
mydata <- mtcars[, c("cyl", "disp")]

#summary
summary(mydata)

# attaching data
attach(mydata)

# cylinders are greater than 4
mydata[cyl > 4,]

# cyl is greater than 4 and disp is less than 400 
mydata[(cyl > 4 & disp < 400),]
```

*** =sct
```{r}
test_object("mydata", incorrect_msg = "Try again")
test_output_contains("summary(mydata)", incorrect_msg = "Try again")
test_output_contains("mydata[cyl > 4,]", incorrect_msg = "remember the correct column name and use a greater sign")
test_output_contains("mydata[(cyl > 4 & disp < 400),]", incorrect_msg = "remember the correct column name and use amper sign")
success_msg("Awesome!")
```
--- type:MultipleChoiceExercise xp:50 skills:1 key:0241f5bcf0

## Data Manipulation Quiz
What do the following three command execute? **faithful** is a dataframe

1. faithful2 <- faithful[seq(1,3), ]
2. faithful2 <- faithful[1:3, ]
3. faithful2 <- head(faithful,3)

*** =instructions
- extract three columns
- create a numeric vector of 1,2,3
- extract three row 


*** =sct
```{r}
msg1 = "Try again"
msg2 = "Try again"
msg3 = "Well done"
test_mc(correct = 3, feedback_msgs = c(msg1,msg2,msg3))
```
