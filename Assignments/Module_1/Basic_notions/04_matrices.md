 Rodrigo Esteves de Lima Lopes \
*Campinas State University* \
[rll307@unicamp.br](mailto:rll307@unicamp.br)



# Matrices Assigments

## Assignments for the section

1. Create a numeric Matrix under the following conditions:
    - The columns and rows have to be named
    - It is numeric, and the numbers must grow through the rows
    - The numbers should be from 1 to 500
        - Do not write the numbers by hand, use the proper interval command
    - It has to have 20 columns and 25 rows
    - Make five random arithmetic operations selecting any specific numbers inside the matrix
1. Create a character Matrix under the following conditions:
    - The names should be of 15 of you family members or closer friends
    - I has to have 5 rows
    - Name the columns and rows according to some criteria
    - Select 3 rows according to their positions in the matrix
1. Post your results to Google Classroom in a text file so everyone can see


# ===============================================================

# Matrices Assigments
## Assignments for the section

# 1. Create a numeric Matrix under the following conditions:
# - The columns and rows have to be named
### The examples given in the class
columns.names <- c('col1','col2', 'col3')
rows.names <- c('row1','row2','row3','row4','row5')

# - It is numeric, and the numbers must grow through the rows
# - The numbers should be from 1 to 500
# - Do not write the numbers by hand, use the proper interval command
# - It has to have 20 columns and 25 rows

matrix(c(1:500), nrow = 25, ncol = 20, byrow = TRUE)

dimnames = list(rows.names, columns.names)
dimnames


My.Matrix <- matrix(c(1:500), nrow = 25, ncol = 20, byrow = TRUE)
dimnames = list(rows.names, columns.names)

My.Matrix

dimnames 

# - Make five random arithmetic operations selecting any specific numbers inside the matrix
matrix(c(1:30), nrow = 10, ncol = 5, byrow = TRUE)
My.Matrix.1 <- matrix(c(1:30), nrow = 10, ncol = 5, byrow = TRUE)

My.Matrix.1[3,2] + My.Matrix.1[10,5]

My.Matrix.1[3,2] - My.Matrix.1[10,5]

My.Matrix.1[3,2] * My.Matrix.1[10,5]

My.Matrix.1[3,2] / My.Matrix.1[10,5]

My.Matrix.1[3,2] + My.Matrix.1[10,5] / My.Matrix.1[3,2] * My.Matrix.1[10,5]

# 2. Create a character Matrix under the following conditions:
# - The names should be of 15 of you family members or closer friends

columns.names <- c('Apelido','Mãe', 'Pai')
rows.names <- c('Claudinei','Marcelo','Telma','Tiago','Mariana','Daniel','Felipe','Edmilson','Eduardo','Edemar','Mirinha','Su','Rap','Cousinx','Cousinz')

# - It has to have 5 rows
# - Name the columns and rows according to some criteria

Primos <- matrix(c('Primo 1', 'Primo 2','Primo 3','Primo 4','Primo 5','Primo 6','Primo 7','Primo 8','Primo 9','Primo 10','Primo 11','Primo 12','Primo 13','Primo 14','Primo 15'), nrow = 15, ncol = 3, byrow = FALSE)
Primos

### The command bellow took me some time to think. I was trying to colnames and rownames before the variable Primos is atteched to the matrix. Then, after some tests I just have put the it over here. It's worked!

colnames(Primos) <- c('Apelido','Mãe', 'Pai')
rownames (Primos) <- c('Primo 1', 'Primo 2','Primo 3','Primo 4','Primo 5','Primo 6','Primo 7','Primo 8','Primo 9','Primo 10','Primo 11','Primo 12','Primo 13','Primo 14','Primo 15')

Primos

# - Select 3 rows according to their positions in the matrix
Primos [13, 1]
Primos [13, 2]
Primos [13, 3]


# 3. Post your results to Google Classroom in a text file so everyone can see


### Rodrigo has created the folling next line bellow to understand better this step in the future. Because the next command is to create the matrix. And the other is to name a variable.
matrix(c(1:15), nrow = 5, byrow = TRUE, dimnames = list(rows.names, columns.names))
My.Matrix <- matrix(c(1:15), nrow = 5, byrow = TRUE, dimnames = list(rows.names, columns.names))

### In the following I am testing the variable.
My.Matrix

### following the logic of creating the matrix first. Just changing the number of elements of the matrix, keeping the the row quantity.
matrix(c(1:20), nrow = 5, byrow = FALSE)
### other
matrix(c(1:30), nrow = 5, byrow = FALSE)
matrix(c(1:30), nrow = 5, byrow = FALSE)
### in this line above of the exercise, I have tried to type the code line, but didn't work I do not now why. I know what as wrong but not why. It was this matrix(c(1:30), nrow = 5, byrow = FALSE)). Aparentelly the last ")" was the wrong thing. (??)

matrix(c(1:15), nrow = 5, byrow = FALSE)
My.Matrix.2 <- matrix(c(1:15), nrow = 5, byrow = FALSE)

matrix(c(1:15), nrow = 5, ncol=5, byrow = TRUE)
My.Matrix.3 <-matrix(c(1:15), nrow = 5, ncol=5, byrow = TRUE)

typeof(My.Matrix)

str(My.Matrix)

str(My.Matrix.3)

#### -------------------------------------
### extra study

matrix(c(1:15), nrow = 5, ncol=5, byrow = FALSE)

matrix(c(1:15), nrow = 5, ncol=5, byrow = TRUE)

matrix(c(1:15), nrow = 5, ncol=5, bycol = TRUE)
### It seems there is no 'bycol' function.

### -------------------------------------
#' 
#' We learnt a couple of things from the code above:
#' 
#' 1. The operator "**:**" makes a numerical sequence in *R*
#' 1. The option `byrow = TRUE` distributes the elements by lines
#'   - While `byrow = FALSE` distributes the elements by columns
#' 1. If I create a matrix which needs more that than my input, *R* recycles the data.
#' 1. Vectors were used as input in a function
#' 
#' We can also create a character matrix:
#' 
## --------------------------------------

columns.names <- c('col1','col2', 'col3')

rows.names <- c('row1','row2','row3','row4','row5')

rep("test", 15)
my.data.1 <- rep("test", 15)

1:15
my.data.2<-1:15

paste0(my.data.1,my.data.2)
my.data.3 <- paste0(my.data.1,my.data.2)
My.Matrix.4 <- matrix(my.data.3, nrow = 5, byrow = TRUE, dimnames = list(rows.names, columns.names))
str(My.Matrix.4)
typeof(My.Matrix.4)

#' 
#' As vectors, we can also access elements in a matrix, but each element is now identified for two indexes:
#' 
## --------------------------------------
My.Matrix[3,1]
My.Number<-My.Matrix[3,1]
My.Matrix.4[3,1]

#' 
#' The first index refers to the row, while the second to the column. If I leave the number before the coma blank, I will be extracting all elements of a row. If I leave the number after the coma blank, I will be extracting all elements of a column. 
#' 
## --------------------------------------
My.Matrix[,1]
My.Matrix[1,]

#' 
#' It is easier to understand if I print this:
#' 
## --------------------------------------
My.Matrix.3
My.Matrix.3[,1]
My.Matrix.3[1,]

#' 
#' I can do all sort of operations with matrices, just as I do with vectors:
#' 
## --------------------------------------
print(My.Matrix - My.Matrix.2)
print(My.Matrix + My.Matrix.2)
sqrt(My.Matrix)

#' 
#' Note that such operations are recursively. Operations on matrices of different size might through an error. 















