---
title       : Chapter 3
description : Importing Data
--- type:NormalExercise xp:100 skills:1 key:169d8c0fe2
## Imprt CSV from url

- Function ` read.csv() ` import csv format files
- Read about this function using help menu
- By default the header is true, so you do not have to specify it
- You can import your file as a local file or url


*** =instructions
- You will import the csv file from the url
- Run summary of the dataset **movie.data**
- Attach your dataframe ` attach(movie.data) `
- Create a dataframe **movie.data2** with movie budget over $30,000,000
- Examine the first 6 rows of movie.data2 (remember there is a specific function that does that)

*** =hint


*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
#This is your url http://cl.indiana.edu/~obscrivn/docs/movie_metadata.csv
#Store this variable as a dataframe in R called movie.data
movie.data <- 

# Look at the summary of the dataframe


# Attach this dataframe


#Create a dataframe from movie.data with only movies with budgets over $30,000,000
movie.data2 <- 


#Examine the first 6 rows of movie.data2

```

*** =solution
```{r}
#This is your url http://cl.indiana.edu/~obscrivn/docs/movie_metadata.csv
#Store this variable as a dataframe in R called movie.data

movie.data <-
   read.csv("http://cl.indiana.edu/~obscrivn/docs/movie_metadata.csv")

# Look at the summary of the dataframe  
summary(movie.data)

#attach this dataframe
attach(movie.data)

#Create a dataframe from movie.data with only movies with budgets over $30,000,000
movie.data2 <- movie.data[budget > 30000000, ]

# Examine the first 6 rows of movie.data2
head(movie.data2)

```

*** =sct
```{r}
test_object("movie.data", incorrect_msg = "Try again1")
test_output_contains("summary(movie.data)", incorrect_msg = "Try again2")
#test_output_contains("attach(movie.data)", incorrect_msg = "Try again3")
test_object("movie.data2", incorrect_msg = "Try again3")
test_output_contains("head(movie.data2)", incorrect_msg = "Try again4")
success_msg("Great! You are done! Feel free to work on your own data!")
```