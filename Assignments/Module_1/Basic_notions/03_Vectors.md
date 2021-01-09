Rodrigo Esteves de Lima Lopes \
*Campinas State University* \
[rll307@unicamp.br](mailto:rll307@unicamp.br)


# Vector Assignments

## Assignments for the section

1. Create a numeric vector from 1 until 100
1. Create a numeric vector from 101 until 200
1. Create a character vector repeating any word you like 20 times
    - Use a proper command for repetition
1. Name your numeric vectors, using the proper command
1. Make a series of operations with your numeric vectors:
    - Sum them and save to a new variable
    - Subtract them and and save to a new variable
    - Use the two first vectors in a Exponentiation (squared or cubed) and save the result in two new variables
1. Post your results to Google Classroom in a text file so everyone can see

# Módulo 1 - 03_Basics
## Basic Notions_Module_01_Vectors

#1 Create a numeric vector from 1 until 100
Tripa <- seq(1:100)
typeof (Tripa)

## Exploring vectors of different natures, which can be: character, logical, integer or double.
#2 Create a numeric vector from 101 until 200
Tripa2 <- seq(101:200)
typeof(Tripa2)

#3 Create a character vector repeating any word you like 20 times
#3.1 Use a proper command for repetition ### Yep!
Tiger <- rep('Slavery no more!', 20)
typeof(Tiger)

#4 Name your numeric vectors, using the proper command
my.vector <- c(10,20,30,40,50,60,70)
my.vector
typeof (my.vector)
names(my.vector) <- c("Domingo","Segunda","Terça","Quarta","Quinta","Sexta","Sábado")
my.vector
typeof (my.vector)
### a little more...
monthsweek <- c('Semana 1','Semana 2', 'Semana 3', 'Semana 4', 'Semana 5')
typeof (monthsweek)
names (monthsweek) <- c('Initial', 'Plan', 'Do', 'Replan', 'Monitoring')
monthsweek
### last
my.vector2 <- c(1,2,3,4,5,6,7,8,9,10,11,12)
my.vector2
months <- c('janeiro','feveiro','marco', 'abril','maio','junho','julho','agosto','setembro','outubro','novembro','dezembro')
months
names(my.vector2) <-months
my.vector2
### in this case, it is one vector naming other vector. They must have the same quantity of elements.

#5 Make a series of operations with your numeric vectors:
#5.1 Sum them and save to a new variable

```{r}
v1 <- c(10,29,333)
v1
v2 <- c(57,68,702)
v2
v1+v2
v3 <- v1+v2
v3
```

#5.2 Subtract them and and save to a new variable

v1-v2
v4 <- v1-v2
v4

### other operations
v1/v2
v5 <- v1/v2
v5

v1*v2
v6 <-v1*v2
v6

v1^v2
v7 <- v1^v2
v7

v1-v2
v4

#5.3 Use the two first vectors in a Exponentiation (squared or cubed) and save the result in two new variables

v1^3
v8 <- v1^3
v8

#6 Post your results to Google Classroom in a text file so everyone can see

  ### extra exploration with vectors

my.vector.2 <- c("b","r","a","s","i","l")
my.vector.2
typeof (my.vector.2)

### I have tryied to apply the command typeof to a vector but it seems not possible application. Class, on the other hand, works good.
### In the next day, I have tried again and see an error my.vector2 instead of my.vector.2. Then, I corrected.

class(my.vector.2)
str(my.vector.2)


-------------------------------------------------------------
  
  ### abaixo coloco o código do Rodrigo para servir de base.
  
  ---
  title: "Basic concepts with R (part 2)"
author: |
  | Rodrigo Esteves de Lima-Lopes 
| State University of Campinas 
| rll307@unicamp.br
output: 
  pdf_document:
  number_sections: yes
toc: yes
keep_md: true
html_document:
  keep_md: true
toc: yes
df_print: paged
---
  
  
  ```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Introduction

In this tutorial we are going to advance a little more about some basic R syntax and general conventions. 

# Vectors
## Definition

A vector is a kind of structured data that form the basis of the R programming. A vector is:
  
  - A one-dimensional data set
- One **row** x **multiple columns**
  - A group of data of the same nature:
  - All are either *character*, *logical*, *integer* or *double*.

## Building a vector
To create a vector, let's execute the following code:

```{r}
my.vector <- c(1,2,3,4,5,6)
my.vector
```

If we look at the code above, we  see that we use the function **c ()**, *combine*, to create a line with numbers. **my.vector** is a vector with *5* elements. Let's see its structure:
  
  ```{r}
class(my.vector)
str(my.vector)
```

That is, **my.vector** is a numerical data structure. Another example would be a character vector:
  
  ```{r}
my.vector.2 <- c("b","r","a","s","i","l")
my.vector.2
class(my.vector.2)
str(my.vector.2)
```

The quotation marks in the code above tell R to treat the letters as characters. If we don't tell so, it will treat them as a variable saved in the system's memory. This vector of characters represents each item in quotes when R prints it. The following is a logical vector:
  
  ```{r}
my.vector.3 <- c(TRUE,FALSE)
my.vector.3
class(my.vector.3)
str(my.vector.3)
```

In the above commands we learnt:
  
  - The first line creates the vector, using the command **c()**
  - The second line tells us the class, **class()**, of our variable
- Very useful when we are trying to find out what a variable is
- The third line gives us the structure, **str()**, of the variable

## Naming Vectors

Vectors can be named, there are specific functions for that.  Naming a vector can help me access this data more clearly, in addition to making the variable more intuitive.

```{r}
my.vector <- c(1,2,3,4,5,6,7)
names(my.vector) <- c("Domingo","Segunda","Terça","Quarta","Quinta","Sexta","Sábado")
my.vector
```

That is, using the function **names()** and the function **c ()** I assigned a name to each column: Domingo contains the number 1 and so on.

If we may want to rename other datasets with the days of the week, there is a smarter way. We keep those days in a variable that can be reused:
  
  ```{r}
my.vector <- c(1,2,3,4,5,6,7)
days <- c("Domingo","Segunda","Terça","Quarta","Quinta","Sexta","Sábado")
names(my.vector) <-days
my.vector
```

## Operations with vectors
## Basic Operations

Vectors can be used to perform some basic operations. For example, I can add these vectors:
  
  ```{r}
v1 <- c(10,29,333)
v2 <- c(57,68,702)
v1+v2
```

Vectors v1 and v2 were added individually, in each column. In other words, column 1 of v1 was added to column 1 of v2 and so on. We can also perform:
  
  ```{r}
v1/v2
v1*v2
v1^v2
v1-v2
```


## Some Functions

There are a number of functions that can be performed with vectors using R preloaded functions. Just so we can remember a function is  applied as follows:
  
  > function_name (function input)
```{r}
sum(v1) # Sum the contents of the vector
sd(v1) # standard deviation
max(v1) # Maximum value
min(v1) # Minimum value
prod(v1) # The product of all elements
```



## Indexing and slicing vectors

Vectors are naturally indexed, that is, we can access data using some operators. Maybe in simple vectors like we have here it doesn't make much of a difference, but if we start working with large amounts of data, it is quite useful.

Let's go back to our vector:
  
  ```{r}
my.vector
```

We can access our data using the following command:
  
  ```{r}
my.vector[1] # the first element of the vector
my.vector[2] # the second element of the vector
```

We can also access it by the name of the column, which makes everything easier.

```{r}
my.vector["Domingo"]
```

It is also possible to create a multiple indexing process, which allows us to slice it. These slices can also be sent to another variable.

```{r}
my.vector[c(1,2)]
```

```{r}
my.vector[c("Sexta","Sábado")]
```

```{r}
my.vector.2<-my.vector[c("Sexta","Sábado")]
my.vector.2
```

Another way to select parts of a vector is by a range.

```{r}
my.vector.4 <- c(1,2,3,4,5,6)
my.vector.5 <- c("b","r","a","s","i","l")
names(my.vector.4) <- my.vector.5
my.vector.4[1:3]
```


It is possible to create comparison functions.

```{r}
names.V <- c("a","b","c")
names(v1) <- names.V
names(v2) <- names.V
v1[v1<100]
v2[v2<100]
v1[v1>100]
v2[v2>100]
v1[v1==100]
v2[v2==100]
```


Notice the difference:
  
  ```{r}
v1<100
v2<100
```

Now, let us look at this:
  
  ```{r}
filter.1<-v1<100
filter.2<-v2<100
filter.1
filter.2
v1[filter.1]
v2[filter.2]
v1[!filter.1]
v2[!filter.2]
```


R operators are:
  
  - '**>**' greater than  
- '**<**' less than
- '**<=**' less than or equal to  
- '**>=**' greater than or equal to  
- '**!=**' not equal to
- '**&**'  AND 
- '**==**' exactly equal to
- '**!x**' Not x
- '**|**' OR
- '^' Exponentiation

























