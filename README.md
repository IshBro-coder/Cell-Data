# Cell-Data
Assignment done in my Honors CS Class


PROBLEM 2: APCS CELL DNA
An APCS Cell has a DNA string of eight capital letters in some combination of A, B, C, D, E, F, G, and H.  Like all living cells, there are actions that can happen to them, including fusing to another cell and splitting into two cells, along with some others.  In this problem, you will take a series of commands, separated by spaces and apply the appropriate actions to the cell.  The action definitions are as follows:


DIVIDE – The cell divides into two cells with one cell taking the first four bits and the second cell taking the last four bits.  The bit groups each replicate and concatenate to get back to eight bits each. 
e.g.  DIV  AHBGCEDF becomes AHBGAHBG and CEDFCEDF

ADDn - The first n (0 ≤ n ≤ 4) bits replicate and are concatenated to the first n bits.  The last n bits are deleted.  The remaining bits are concatenated on the right.
e.g. ADD3 AHBGCEDF becomes AHBAHBGC

SUBTRACTn - The first n (0 ≤ n ≤ 4) bits are deleted and the last n bits replicate, are put in alphabetical order and then are concatenated on the right. 
e.g. SUB3 AHBGCEDF becomes  GCEDFDEF

UNION - Two cells become one by deleting the first four bits of the first cell and the last four bits of the second cell. The remaining bit groups in each cell are put in alphabetical order and concatenated.
                    	e.g.  UNI AHBGCEDF AGBHCFED becomes CDEFABGH

INTERSECT - Two cells become one by deleting the middle four bits of the first cell and the middle four bits of the second cell.  The remaining bit groups are each  put in alphabetical order and concatenated
                    	e.g.  INT AHBGCEDF AGBHCFED becomes ADFHADEG


INPUT: There will be 3 cells used:   X, Y, and Z.  They will be given on the first 3 input lines, in that order,  and each will be represented by an eight-character string.  The next 6 lines will consist of a set of operations (at least 1 and at most 3), along with a reference to the cells to be used.  The first three lines will contain only one operation.  For lines with multiple operations, the actions should be performed from right to left (inside out).  The cells are operated on as a list with the operations being performed from right to left. Operators and cells will be separated by a space.


                    			Example:  SUB3 ADD2  AHBGCEDF becomes HBGCECEG
 

OUTPUT:  For each list print the final output of the operation(s). (numbers are there just for reference)
Sample Input
Sample Output
ABCDEFGH		
AAGGHDFE
GHAFFEDB
DIV X
ADD2 Z  
SUB2 X      
DIV ADD1 Y 
UNI Y  Z
INT Z  X  
UNI  ADD1 Y  SUB1 Y
(stored as X)
(stored as Y)
(stored as Z)
ABCDABCD and EFGHEFGH
GHGHAFFE
CDEFGHGH
AAAGAAAG and GHDFGHDF
DEFHAFGH
BDGHABGH
DFGHAGGH

