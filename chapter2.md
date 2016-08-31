--- type:NormalExercise lang:r xp:100 skills:1
## Vectors (1)

You can combine values of the same data type to a **vector**, using the function `c()`. 

A vector is an object containing multiple elements. Vectors are quite important in R. The columns of a data frame (such as `student2014`) are vectors.

In this execrice you will learn how to create your own vector.

*** =instructions
- See and execute the examples on how to create a vector with `c()`.
- Save character vector to `my_vector`.
- Create vector `boolean_vector` with boolean values `TRUE, FALSE, TRUE, FALSE`.

*** =hint
- When creating boolean values, no quotation marks are needed.


*** =pre_exercise_code
```{r}
```


*** =sample_code
```{r}

# Here we create a vector with numeric elements
c(2, 3, 4, 5)

# Another one
c(0.1, 0.2, 5.84, 0.7)

# Let's create one with characters and save it to a object
my_vector <- c('a', 'b', 'c', 'd')

# Create boolean vector


```

*** =solution
```{r}

# Here we create a vector with numeric elements
c(2, 3, 4, 5)

# Another one
c(0.1, 0.2, 5.84, 0.7)

# Let's create one with characters and save it to a object
my_vector <- c('a', 'b', 'c', 'd')

# Create boolean vector
boolean_vector <- c(TRUE, FALSE, TRUE, FALSE)

```

*** =sct
```{r}
test_output_contains("c(2, 3, 4, 5)", incorrect_msg = "Did you execute all the lines?")
test_output_contains("c(0.1, 0.2, 5.84, 0.7)", incorrect_msg = "Did you execute all the lines?")

test_object("my_vector <- c('a', 'b', 'c', 'd')", incorrect_msg = "Did you execute `my_vector`?")
test_object("boolean_vector <- c(TRUE, FALSE, TRUE, FALSE)", incorrect_msg = "Did you create `boolean_vector` with same values as instructed?")
test_error()

# Final message the student will see upon completing the exercise
success_msg("Great work!")

```
