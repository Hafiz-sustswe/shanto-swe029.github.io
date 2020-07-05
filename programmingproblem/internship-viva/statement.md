[ `return to Home Page` ](https://shanto-swe029.github.io) || [`Some Programming Problems`](https://shanto-swe029.github.io/programmingproblems) || [`Programming Notes`](https://shanto-swe029.github.io/programmingnotes)

***

# Sort The Sturct

***

[`See Solution`](https://shanto-swe029.github.io/programmingproblem/internship-viva/solution)


## Problem Statement

    The SUST Software Engineering Department is going to send their students
    into different Software Farms for their internships. There is a good number
    of software farms who want to recruit the students. The managers of the
    farms want few details about the students and that is - student name,
    registration number, total number of problem solved and CGPA. SUST Software
    Engineering department has provided them with all necessary information that
    they demanded.
    
    You are a Student of SUST Software Engineering department and you are also
    joining a farm for your internship. At the viva board they ask you to sort
    all the students' information according to this order -
      1. The students will be sorted according to the non-increasing order
         of their number of problem solved.
      2. If more than one student have equal number of problems solved, then 
         the tied students will be sorted according to the non-decreasing
         order of their CGPA.
      3. If two or more students have equal number of solved problems and
         equal CGPA, then leave them as they are.
    Now write the code under those conditions.

## Attention:

    You have to solve the problem using structure in C language.

## Input :

    The first line of the input will contain an integer n, the total number
    of students. Then there will be total n lines. Each of the lines contain
    4 space seperated informations - name(without sapce), registration number,
    number of problems solved and CGPA. See the exmple to understand the input
    format clearly.
    
## Output:

    Print the information of each student in the format:-
    name, then print a space, then print registration number, then print
    another space, then print their number of problem solved, then again
    print a space and then print the CGPA. The information of each student
    must be printed in seperated lines and according to the sorting order
    your company wants.
    
## Example:

    Input:
    11
    Shanto 2019831029 1200 2.33
    Mehraj 2019831074 4000 3.69
    Abraar 2019831076 1800 3.55
    Promi 2019831038 2500 3.77
    Jisan 2019831040 3000 3.68
    Bijon 2019831007 3000 3.68
    Shawon 2019831013 3500 3.89
    Mugdha 2019831048 3500 3.89
    Meem 2019831063 2500 3.78
    Fahad 2019831065 3000 3.59
    Sajid 2019831045 3000 3.99
    
    Output:
    Mehraj 2019831074 4000 3.69
    Shawon 2019831013 3500 3.89
    Mugdha 2019831048 3500 3.89
    Sajid 2019831045 3000 3.99
    Jisan 2019831040 3000 3.68
    Bijon 2019831007 3000 3.68
    Fahad 2019831065 3000 3.59
    Meem 2019831063 2500 3.78
    Promi 2019831038 2500 3.77
    Abraar 2019831076 1800 3.55
    Shanto 2019831029 1500 2.33
    
**Happy Coding!**

***

`This page is managed by Ariful Islam Shanto`
