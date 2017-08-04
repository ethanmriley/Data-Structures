HOMEWORK 7: MINIBLAST


NAME: Ethan RIley


COLLABORATORS AND OTHER RESOURCES:
List the names of everyone you talked to about this assignment
(classmates, TAs, ALAC tutors, upperclassmen, students/instructor via
LMS, etc.), and all of the resources (books, online reference
material, etc.) you consulted in completing this assignment.

Zach Cook
Greg Bartell
stackoverflow.com

Remember: Your implementation for this assignment must be done on your
own, as described in "Academic Integrity for Homework" handout.



ESTIMATE OF # OF HOURS SPENT ON THIS ASSIGNMENT:  8-10


HASH FUNCTION DESCRIPTION


The hash function I use XOR's an initial value (provided with the function) against each letter in the key. It then multiplies the resulting value by a constant (also provided); it repeats this process for each letter in the key.

I got this hash function from: <https://stackoverflow.com/questions/98153/whats-the-best-hashing-algorithm-to-use-on-a-stl-string-when-using-hash-map>.


HASH TABLE IMPLEMENTATION

My table uses the hash function on each k-mer, assigning it an index in the table. In the case of collisions, I use linear probing to find an empty location. To account for collisions in querying, I check every entry in the table ragning from the hash index to the next empty location, relying on the idea that all matching keys would be found there. 

To resize, I increment a counter, checking it against the table size before every insertion. When the occupancy goes above the set value, I double the table size and re-insert every currently existing entry into the new table.  






ANALYSIS OF PERFORMANCE OF YOUR ALGORITHM:
(order notation & concise paragraph, < 200 words)

L = length of the genome sequence
q - query length
p - number of different locations where key is found
k - key size (k-mer size)

How much memory will the map data structure require (order notation for memory use)?

	O(((L-k)+1)*k)

	For a genome of length L, there are (L-k+1) possible k-mers. Each of these takes up k bytes 		(one byte per character). 

What is the order notation for performance (running time) of each of
the commands?

	genome:
		O(L) to read the whole genome.
		O(1) to store it in the hashTable.
		Total: O(L).		

	table_size:
		O(n), where n is the table size. This function populates the table with empty entries to the appropriate size.

	occupancy:
		O(1). This command simply sets a value in the hashTable class. 

	kmer:
		O(1) to store the k-value in the hashTable.
		O(k*(L-k+1)) to read through every k-mer.
		O(L-k+1) to iterate through every k-mer.
		O(k) to hash each k-mer, reading through each letter.
		O(p+1) to use linear probing to insert the k-mer into the table.
		Total: O(k*(L-k+1) + k + p + 1)

	query:
		O(k) to generate the seed.
		O(k) to hash the seed.
		O(p) to probe the table for every place the seed appears in the genome. 
		O(p*q) to check each seed against the query.
		Total: O(k + p + p*q) 

	quit:
		O(1). Quits. 


EXTRA CREDIT
Add a new command to implement the database using one of the other
 data structures that we have covered so far in the course: 
vectors, lists, arrays etc. 

Compare the performance your alternative method to the homework method
by making a table of run times for each of the genomes and query 
sets provided with the homework  and compare the times to build
the index and the times to process the queries. 
Document any new commands you have added in your README file.



MISC. COMMENTS TO GRADER:  
(optional, please be concise!)


