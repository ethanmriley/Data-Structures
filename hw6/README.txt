HOMEWORK 6: INVERSE WORD SEARCH


NAME: Ethan Riley


COLLABORATORS AND OTHER RESOURCES: 
List the names of everyone you talked to about this assignment
(classmates, TAs, ALAC tutors, upperclassmen, students/instructor via
LMS, etc.), and all of the resources (books, online reference
material, etc.) you consulted in completing this assignment.

Warren Nelson
Greg Bartell
Dan Weeks

cplusplus.com
stackoverflow.com


Remember: Your implementation for this assignment must be done on your
own, as described in "Academic Integrity for Homework" handout.

ESTIMATE OF # OF HOURS SPENT ON THIS ASSIGNMENT:  25-30


ALGORITHM ANALYSIS:
What's the order notation of your algorithm?
O(orientation*w*h*r + orientation*w*h*f + l + w*h + 26^(w*h))

The above is the worst-case for my algorithm. 
recursivePermutate is O(orientation*w*h*r), as it generates every combination of these for each word.
verifyGrid is O(orientation*w*h*f+l), as it tries every combination of orientation, x, and y for each forbidden word.
recursiveFillWords is O(w*h + orientation*w*h*r), as it first checks for empty spaces, then calls recursivePermutate.
fillEmptySpaces is the slowest function, at O(26^(w*h)) in the worst case. It permutates every letter in every empty position in a grid; for one, it is 26, for two, 26^2, and so forth.



TEST CASE SUMMARY:
How did your program perform on the different test cases?  Summarize
the running times.  (It's ok if it didn't finish the harder examples.)
What new test cases did you create and how did it perform on those
tests?

Puzzle 1: .006s
Puzzle 2: .007s
Puzzle 3: .488s
Puzzle 4: .16s
Puzzle 5: .18s
Puzzle 6: .059s
Puzzle 7: 1.37s
Puzzle 8: 4 min 18s

In addition, I wrote my own test cases, test1.txt and test2.txt.
They show the effect of varying word length and blank spaces on runtime; even a 2x2 grid takes tens of seconds, with 26^4 boards, whereas increasing the word length to 7 letters has an imperceptible effect.

test1: 41.082s
test2: .004s




MISC. COMMENTS TO GRADER:  
Optional, please be concise!


