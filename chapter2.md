---
title       : Chapter 2
description : Data Frame Modification
  
--- type:NormalExercise xp:100 skills:1 key:db082273b2
## Manipulating Data Frame

- Logical operators are useful to retrieve data based on a condition
- Operators are ` > `, ` <= `, ` >= `, ` == `
- Review operators here if needed [operators list](http://www.statmethods.net/management/operators.html)
- You can specify a condition for a column value
- Example ` mydata["Age" < 55] `
*** =instructions
-Find the column names of your data set **mtcars**
-Create a new data frame **mydata** by retrieving two columns **cyl** **disp**. Since you are extracting two columns, you need to use a vector (for more help - review this page [column slicing](http://www.r-tutor.com/r-introduction/data-frame/data-frame-column-slice)

- Use help function to learn about ` summary() ` (remember to use question mark)
- Apply this function to **mydata**
- Retrieve only cylinders that are greater than 4
- Retrieve cylinders that are equal 4

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


# cylinders greater than 4


# cylinders equal 4

```

*** =solution
```{r}
data(mtcars)
# Fill in the coordinates (colnames) inside the brackets
mydata <- mtcars[c("cyl", "disp")]

#summary
summary(mydata)

# cylinders greater than 4
mydata["cyl" > 4]

# cylinders equal 4
mydata["cyl" == 4]
```

*** =sct
```{r}
test_object("mydata", incorrect_msg = "Try again")
test_output_contains("summary(mydata)", incorrect_msg = "Try again")
test_output_contains("mydata[\"cyl\" > 4]", incorrect_msg = "remember the correct column name and use a greater sign")
test_output_contains("mydata[\"cyl\" == 4]", incorrect_msg = "remember the correct column name and use equal sign")
success_msg("Awesome!")
```