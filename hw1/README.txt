HOMEWORK 1: AIRLINE SEATING


NAME:Ethan Riley


COLLABORATORS AND OTHER RESOURCES:
List the names of everyone you talked to about this assignment
(classmates, TAs, ALAC tutors, upperclassmen, students/instructor via
Piazza, etc.), and all of the resources (books, online reference
material, etc.) you consulted in completing this assignment.

Greg Bartell
LC Hines
Ethan Wright
cplusplus.com
stackoverflow.com

Remember: Your implementation for this assignment must be done on your
own, as described in "Academic Integrity for Homework" handout.



ESTIMATE OF # OF HOURS SPENT ON THIS ASSIGNMENT:  12-20 (it all blurs together)



EXPLANATION OF REMOVING PASSENGERS FROM UPGRADE LIST:
Describe the data structure you used to represent the upgrade lists,
and how you removed passengers from these lists.

I used vector<vector<string> >, the string being the passenger ID.
I initialized the base vector (upgrade_list) with a size of 2, assigning passengers either to upgrade_list[0] or upgrade_list[1] (also vectors) depending on if they would be upgraded to F or B class.
I removed passengers from the list by iterating through it and changing the pass_id to "NULL", accounting for the presence of these null passengers in the rest of my code. 
After a UPP command, I clear the upgrade list.



MISC. COMMENTS TO GRADER:  
Optional, please be concise!
