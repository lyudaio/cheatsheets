# R

R is a programming language and software environment for statistical computing and graphics. It is widely used for data analysis, visualization, and predictive modeling.

## Vectors

Vectors are one-dimensional arrays of data in R.

```r
# Create a vector
vector1 <- c(1, 2, 3, 4)

# Access elements of a vector
vector1[2] # returns 2

# Perform operations on a vector
sum(vector1) # returns 10
mean(vector1) # returns 2.5
```

### Matrices

Matrices are two-dimensional arrays of data in R.

```r
# Create a matrix
matrix1 <- matrix(1:6, ncol = 2)

# Access elements of a matrix
matrix1[2, 2] # returns 4

# Perform operations on a matrix
colSums(matrix1) # returns the sum of each column
rowMeans(matrix1) # returns the mean of each row
```

### Data Frames

Data frames are two-dimensional arrays with named columns, similar to tables in a relational database.

```r
# Create a data frame
data.frame1 <- data.frame(Name = c('John', 'Jane', 'Jim'),
                         Age = c(30, 28, 35),
                         Gender = c('Male', 'Female', 'Male'))

# Access elements of a data frame
data.frame1$Name # returns the Name column

# Perform operations on a data frame
aggregate(Age ~ Gender, data = data.frame1, mean) # returns the mean Age by Gender
```

### Plotting

R has a wide range of plotting capabilities, including scatter plots, bar charts, line charts, and more.

```r
# Scatter plot
plot(data.frame1$Age, data.frame1$Gender)

# Bar chart
barplot(table(data.frame1$Gender))

# Line chart
lines(data.frame1$Age, data.frame1$Gender)
```
