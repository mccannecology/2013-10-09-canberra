**Introduction to R**
===================

R is a versatile, open source programming/scripting language that's useful both for statistics and data science. 

* Public domain software 
* Superior (if not just comparable) to commercial alternatives
* Available on all platforms
* Not just for statistics, but also general purpose programming
* Is object oriented and functional
* Large and growing community of peers

**How to run `R`**  

Within R studio, there are 4 parts to R

* Console: Where commands are run
* Scripts: Where commands are written
* Environments: Where objects are stored
* Plots: Where data is viewed

Running Commands in the Console
----------------------

The R console returns objects based on functions and expressions.

<img src="http://www.lifewithlevi.com/wp-content/uploads/2012/02/Happy-Squirrel-Driking.jpg" alt="Drawing" style="width: 100px;"/> **Try It!**

--------------------

1. What is 17 multiplied by 365?

2. What is 7^3?

Creating Objects
--------------------

All expressions can be saved as an object, this is the fundamental unit in R. To create an object from an expression we use the assignment operater <-


**Assignment operator**
`<- ` is the assignment operator. Assigns values on the right to objects on the left.



```r
a <- 12 * 180
a
```

```
## [1] 2160
```

The object a is now saved as the output of the expression 12*180

#Maybe put a box around this?

*R tips*

*Use `#` before an expression signs to 'comment' your script. Good scripts and (homework) have comments before every major block of code. Anything to the right of a `#` is ignored.*

Expressions using objects
----------------------

The beauty of R is that objects can be combined into other, larger, and more complex objects!


```r
a <- 8 * 10
b <- 2 * 10
c <- a * b
c
```

```
## [1] 1600
```

```r
# Equivalent to
c <- 8 * 10 * 2 * 10
c
```

```
## [1] 1600
```


**Try It!**
------------

3. Create an object that is your age. Create another object that is the age of the person to your right. Find the difference between these objects. 

Combining objects - Vectors!
-------------------

R has 5 common data structures, we will learn today about the simplest - vectors.

Vectors are one dimensional strings of numbers, characters of objects

A vector is made using the function c(), explained later today.


```r
# Combine numbers into a vector

a <- c(3, 4, 5)
a
```

```
## [1] 3 4 5
```

```r

# Combine characters into a vector

b <- c("q", "r", "s")
b
```

```
## [1] "q" "r" "s"
```

```r

# Combine objects into a vector
a <- 4 * 7
b <- 6 * 5
g <- 9 * 2

d <- c(a, b, g)
d
```

```
## [1] 28 30 18
```


**Properties of Vectors**

Vectors have positions, these positions are ordered and can be called using name_vector[position]


```r
a <- 8 * 9
b <- 2 * 3
d <- c(a, b)

d[1]
```

```
## [1] 72
```

```r
d[2]
```

```
## [1] 6
```


**Try It!**
------------

4. What is the 9th and 12th position of seq(1,27,.5)? 

5. Bonus! Can you find those positions simultaneously


Functions
----------

A function is a saved object that performs a task given inputs. All functions are made up of smaller objects. Functions are used in the format output<-name_of_function(inputs)


```r
# The sum of a vector
sum(c(3, 4, 5))
```

```
## [1] 12
```

```r

# The mean of a vector
mean(c(3, 4, 5))
```

```
## [1] 4
```

```r

# Functions can act on an object
a <- c(3, 4, 5)
mean(a)
```

```
## [1] 4
```


How to use a function?
-----------------------

All functions come with a help screen. It is critical that you learn to read the help screens since they provide important information on what the function does, how it works, and ususally sample examples at the very bottom.

*R tips*

*While many R functions are easy to guess their name, most functions are abbreviated to save time and space, you can search for functions (only from installed packages) by using ??query, eg. ??robust with search for any functions whose help screens contain the word robust*


**Try It!**
------------

6. What is the median of 34, 16, 105, 27? *Hint* functions are often named intuitively.

7. What does the function 'range' do, what is sample example in the help file?

8. Bonus! Is mean(4,5) different than mean(c(4,5))?


Packages
---------------------
We will be exploring functions in much greater detail throughout this course. Functions are the soul of R, that is why we use it. Functions are kept inside packages, some of which come preinstalled into R - others must be downloaded online

To check out the wide world of packages: INSERT LINK and search with your favorite keyword! Ecology, paleo, dispersal, population modeling, economics!

Often you will be asked to install a package to access a certain library of functions



```r
# To install any new package install.packages('picante')

# pick a closeby mirror, say okay if it asks to create a new folder
```



*R tips*

*Installing a package just download its to your computer. To actually use a function in R from an outside package you have to "require" it at the top of the script, this let's R know what packages to load in, and not waste time with all potential functions. Good scripts (and homeworks) have a series of require(name_of_library) at the top of the script in an orderly fashion*


**Try It!** 
------------

9. Find a fascinating package in the search query. What is it? What is one interesting function?

10. Install the package to your computer. 
```

You are not alone Part I - The R Help Screen and User Community
--------------------------------------------------------

```r
## ss 1.1.3: Online Help
`?`(mean  # Equivalent to help(mean) 
)
```

```
## starting httpd help server ... done
```

```r

`?`(sort  # Try, also, apropos ('sor') 
)
# List all functions where 'sort' is part of the name
`?`(`?`(sort  # Note that the argument is 'sort' 
))
# List functions with 'sort' in the help page title or as an alias
```


You are not alone Part II - The R Help Screen and User Community
-------------------------------
![alt text](http://img78.imageshack.us/img78/196/wheelsel6.gif)

**Quitting R**

type in `quit()` or `q()` and answer `Y` to quit. Always remember to save scripts. For now we will not save workspaces!
