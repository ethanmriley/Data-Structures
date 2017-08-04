HOMEWORK 7: WORD FREQUENCY MAPS


NAME: Ethan Riley


COLLABORATORS AND OTHER RESOURCES:
List the names of everyone you talked to about this assignment
(classmates, TAs, ALAC tutors, upperclassmen, students/instructor via
LMS, etc.), and all of the resources (books, online reference
material, etc.) you consulted in completing this assignment.

cplusplus.com

Remember: Your implementation for this assignment must be done on your
own, as described in "Academic Integrity for Homework" handout.



ESTIMATE OF # OF HOURS SPENT ON THIS ASSIGNMENT:  7



ANALYSIS OF PERFORMANCE OF YOUR ALGORITHM:
(order notation & concise paragraph, < 200 words)

n = total number of words in the sample text file
m = number of unique words in the file
w = width of the sequencing window
p = average number of words observed to follow a particular word

How much memory will the map data structure require, in terms of n, m,
w, and p (order notation for memory use)?

O(m*(p^w))

What is the order notation for performance (running time) of each of
the commands?

load:
O(n)
Reads through all the words in the file

print:
O(p)
Reads through all words following the queried word

generate:

	common:
	O(p*phrase length + m*(p^w))
	Reads through all words following a queried word once for every added word
	Reads through a map of maps to begin on line 149

	random:
	O(p*phrase length)
	Reads through the words following a queried word once for every added word

quit:
O(1)

EXTRA CREDIT
Parsing & using punctuation data, implementation supports *any*
window size, new test cases (describe & summarize performance, but
don't include large datasets with submission).



MISC. COMMENTS TO GRADER:  
(optional, please be concise!)


