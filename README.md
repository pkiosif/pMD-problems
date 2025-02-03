# pMD-problems
## A library of p-median problems with distance constraints (pMDs).  

These benchmarks complement the paper ***"A Heuristic CP Method for the p-median Problem with Distance Constraints"***.


### Description of input files:

The example below demonstrates a small pMD problem input file. The first line consists of four (4) different number **25 3 4 3**. Let |CL| be the number of clients on a grid, |P| the number of candidate facility points and |F| the number of facilities. In the given example **Grid size = 25 $\times$ 25**, **|CL| = 3**, **|P| = 4** and **|F| = 3**.

Next, the clients' and candidate facility points' IDs are presented (e.g. 3 clients: 11, 12, 13 where client$_1$ ID = 11). Afterwards, the distance constraints between facilities and clients and between facilities are presented in turn. 

**Distance constraints between facilities and clients:**
The first line after **3 constraints between facilities and clients:**, contains **0 0** meaning that the first facility (x~0~) must have an Euclidean distance greater than (>) zero (0) from all clients. Similarly, the second facility (x<sub>1</sub>) must have D[x<sub>1</sub>,c<sub>k</sub>] > 1 $\forall c \in CL$.

**Distance constraints between facilities:**
The first line after **3 constraints between facilities:**, contains **0 1 0** meaning that the first and second facilities must be located at an Euclidean distance greater than (>) zero (0). Similarly, D[$x\_1$,$x\_2$] > 0.

Thereafter, the shortest path and Euclidean distances are given between facility points and clients, and between facility points. 

**SP and Euclidean distances between facility points:**
The first line after **12 shortest paths and Euclidean distances between candidate facilities:**, contains **4 7 5 2.236068** meaning that facility points with ID = 4 and ID = 7 (or $fp\_0$ and $fp\_1$) are at distances SP[$fp\_0$, $fp_1$] = 5 and D[$fp\_0$, $fp\_1$] = 2.236068, where SP is the shortest path distance and D the Euclidean distance.

**SP and Euclidean distances between facility points and clients:**
The first line after **12 shortest paths and Euclidean distances between clients and candidate facilities:**, contains **11 4 5 3.605551** meaning that client with ID = 11 and facility point with ID = 4 (or $c\_0$ and $fp\_0$) are at distances SP[$c\_0$, $fp\_0$] = 5 and D[$c\_0$, $fp\_0$] = 3.605551, where SP is the shortest path distance and D the Euclidean distance.


### A small pMD example:

25 3 4 3<br>
3 clients:<br>
11<br>
12<br>
13<br>
4 candidate facilities:<br>
4<br>
7<br>
9<br>
14<br>
3 constraints between facilities and clients:<br>
0 0<br>
1 1<br>
2 1<br>
3 constraints between facilities:<br>
0 1 0<br>
0 2 0<br>
1 2 0<br>
12 shortest paths and Euclidean distances between candidate facilities:<br>
4 7 5 2.236068<br>
4 9 1 1.000000<br>
4 14 2 2.000000<br>
7 4 5 2.236068<br>
7 9 4 2.000000<br>
7 14 3 2.236068<br>
9 4 1 1.000000<br>
9 7 4 2.000000<br>
9 14 1 1.000000<br>
14 4 2 2.000000<br>
14 7 3 2.236068<br>
14 9 1 1.000000<br>
12 shortest paths and Euclidean distances between clients and candidate facilities:<br>
11 4 5 3.605551<br>
11 7 2 1.414214<br>
11 9 4 3.162278<br>
11 14 3 3.000000<br>
12 4 4 2.828427<br>
12 7 1 1.000000<br>
12 9 3 2.236068<br>
12 14 2 2.000000<br>
13 4 3 2.236068<br>
13 7 2 1.414214<br>
13 9 2 1.414214<br>
13 14 1 1.000000<br>
