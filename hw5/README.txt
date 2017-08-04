HOMEWORK 5: DSRADIO SONG GROUPS


NAME: Ethan Riley


COLLABORATORS AND OTHER RESOURCES:
List the names of everyone you talked to about this assignment
(classmates, TAs, ALAC tutors, upperclassmen, students/instructor via
LMS, etc.), and all of the resources (books, online reference
material, etc.) you consulted in completing this assignment.

Eleanor Little
Ethan Wright
cplusplus.com

Remember: Your implementation for this assignment must be done on your
own, as described in "Academic Integrity for Homework" handout.


ESTIMATE OF # OF HOURS SPENT ON THIS ASSIGNMENT:  10



ORDER NOTATION:
For each of the functions below, write the order notation O().
Write each answer in terms of s = the number of songs in the library,
g = the number of song groups, a = the average number of songs by the same 
artist, and l = the average length of song groups.

AddSongToLibrary

	O(s)

GroupExists

	O(g)	

AddToGroup

	O(l)

MakeGroup

	O(1) (constant time)

PrintGroupRewind

	O(l)

PrintLongestGroupRewind

	O(n^2)

RemoveGroup

	O(g+l)

DeleteAllSongGroups

	O(g + (l*g))

RemoveFromGroup

	O(g + l)

PrintGroupMarathon

	O(l)



TESTING & DEBUGGING STRATEGY: 
Discuss your strategy for testing & debugging your program.  
What tools did you use (gdb/lldb/Visual Studio debugger,
Valgrind/Dr. Memory, std::cout & print, etc.)?  How did you test the
"corner cases" of your implementation?


	I mainly used GDB to step through code and analyze what was happening where.
	My biggest bug was with RemoveFromGroup where i was improperly deleting nodes, which i discovered through reading node info with GDB at different points in the romval process
	i tested corner cases by creating malformed input files which printed, deleted, and did other operations on empty groups and libraries.
	that helped me find some segfaults.
	valgrind was useful in alerting me to memory leaks, but i had to read through the code myself and really think about what was going on to fix them  



MISC. COMMENTS TO GRADER:  
(optional, please be concise!)

