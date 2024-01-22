# Advanced_R Programming_week4


# Part 1: Factorial Function

The objective of Part 1 is to write a function that computes the factorial of an integer greater than or equal to 0. Recall that the factorial of a number n is n * (n-1) * (n - 2) * … * 1. The factorial of 0 is defined to be 1. Before taking on this part of the assignment, we may want to review the section on Functional Programming in this course (we can also 
read that section here
).

For this Part we will need to write four different versions of the Factorial function:

Factorial_loop: a version that computes the factorial of an integer using looping (such as a for loop)

Factorial_reduce: a version that computes the factorial using the reduce() function in the purrr package. Alternatively, we can use the Reduce() function in the base package.

Factorial_func: a version that uses recursion to compute the factorial.

Factorial_mem: a version that uses memoization to compute the factorial.

After writing our four versions of the Factorial function, use the microbenchmark package to time the operation of these functions and provide a summary of their performance. In addition to timing our functions for specific inputs, make sure to show a range of inputs in order to demonstrate the timing of each function for larger inputs.

In order to submit this assignment, please prepare two files:

# 1. factorial_code.R: an R script file that contains the code implementing our classes, methods, and generics for the longitudinal dataset.

# 2. factorial_output.txt: a text file that contains the results of our comparison of the four different implementations.


# Part 2: Longitudinal Data Class and Methods

The purpose of this part is to create a new class for representing longitudinal data, which is data that is collected over time on a given subject/person. This data may be collected at multiple visits, in multiple locations. we will need to write a series of generics and methods for interacting with this kind of data.

The data for this part come from a small study on indoor air pollution on 10 subjects. Each subject was visited 3 times for data collection. Indoor air pollution was measured using a high-resolution monitor which records pollutant levels every 5 minutes and the monitor was placed in the home for about 1 week. In addition to measuring pollutant levels in the bedroom, a separate monitor was usually placed in another room in the house at roughly the same time.


The variables in the dataset are

id: the subject identification number

visit: the visit number which can be 0, 1, or 2

room: the room in which the monitor was placed

value: the level of pollution in micrograms per cubic meter

timepoint: the time point of the monitor value for a given visit/room

we will need to design a class called “LongitudinalData” that characterizes the structure of this longitudinal dataset. we will also need to design classes to represent the concept of a “subject”, a “visit”, and a “room”.

In addition we will need to implement the following functions

make_LD: a function that converts a data frame into a “LongitudinalData” object

subject: a generic function for extracting subject-specific information

visit: a generic function for extracting visit-specific information

room: a generic function for extracting room-specific information

For each generic/class combination we will need to implement a method, although not all combinations are necessary (see below). we will also need to write print and summary methods for some classes (again, see below).

To complete this Part, we can use either the S3 system, the S4 system, or the reference class system to implement the necessary functions. It is probably  not wise to mix any of the systems together, but we should be able to compete the assignment using any of the three systems. The amount of work required should be the same when using any of the systems.

The output of our function does not need to match exactly, but it should convey the same information.

In order to submit this assignment, please prepare two files:

# oop_code.R: an R script file that contains the code implementing our classes, methods, and generics for the longitudinal dataset.

# oop_output.txt: a text file containing the output of running the above input code.

