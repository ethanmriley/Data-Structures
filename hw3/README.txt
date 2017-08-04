HOMEWORK 3: MATRIX CLASS


NAME: Ethan Riley


COLLABORATORS AND OTHER RESOURCES:
List the names of everyone you talked to about this assignment
(classmates, TAs, ALAC tutors, upperclassmen, students/instructor via
LMS, etc.), and all of the resources (books, online reference
material, etc.) you consulted in completing this assignment.

Eleanor Little
Hector Rodriguez
Mary Montgomery
cplusplus.com
stackoverflow.com
cppreference.com

Remember: Your implementation for this assignment must be done on your
own, as described in "Academic Integrity for Homework" handout.


ESTIMATE OF # OF HOURS SPENT ON THIS ASSIGNMENT:  10-12



ORDER NOTATION:
For each of the functions below, write the order notation O().
Write each answer in terms of m = the number of rows and n = the
number of columns.  You should assume that calling new [] or delete []
on an array will take time proportional to the number of elements in
the array.

get
O(1)

set
O(1)

num_rows
O(1)

get_col
O(m)

operator<<
O(m*n)

quarter
O(m*n)

operator==
O(m*n)

operator!=
O(m*n)

swap_row
O(n)

rref (provided in matrix_main.cpp)
O((m^4)*(n^3))


TESTING & DEBUGGING STRATEGY: 
Discuss your strategy for testing & debugging your program.  
What tools did you use (gdb/lldb/Visual Studio debugger,
Valgrind/Dr. Memory, std::cout & print, etc.)?  How did you test the
"corner cases" of your Matrix class design & implementation?

I debugged mainly with gdb and valgrind; gdb for stepping through the code, and valgrind for analyzing memory leaks.
This hw didn't involve too many steps, so it was mainly analyzing object initialization and memory allocation.

I tested the corner cases by trying to break my own code with various edge cases. 
0-size matrices, bounds overruns, etc.


EXTRA CREDIT: 
Indicate here if you implemented resize() for extra credit.  
Also document the order notation for your resize() function.

I wrote resize(), and it is O(m*n).



MISC. COMMENTS TO GRADER:  
(optional, please be concise!)

