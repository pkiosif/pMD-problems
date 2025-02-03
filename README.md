# pMD-problems
## A library of p-median problems with distance constraints (pMDs).  

These benchmarks complement the paper **"A Heuristic CP Method for the p-median Problem with Distance Constraints"**.


### Description of input files:

The example bellow demonstrates a small pMD problem input file. The first line consists of four (4) different number **25 3 4 3**. Let |CL| be the number of clients on a grid, |P| the number of candidate facility points and |F| the number of facilities. In the given example **Grid size = 25 x 25**, **|CL| = 3**, **|P| = 4** and **|F| = 3**.

Next, the clients' and candidate facility points' IDs are presented (e.g. 3 clients: 11, 12, 13 where client_1 ID = 11). Afterwards, the distance constraints between facilities and clients and between facilities are presented in turn. 

**Distance constraints between facilities and clients:**
The first line after **3 constraints between facilities and clients:**, contains **0 0** meaning that the first facility (x$_0$) must have an Euclidean distance greater than (>) zero (0) from all clients. Similarly, the second facility (x$_1$) must have D[x$_1$, C$_k$] > 1 $\forall c \in CL$.

**Distance constraints between facilities:**
The first line after **3 constraints between facilities:**, contains **0 1 0** meaning that the first and second facilities must be located at an Euclidean distance greater than (>) zero (0). Similarly, D[x$_1$,x$_2$] > 0.

Thereafter, the shortest path and Euclidean distances are given between facility points and clients, and between facility points. 

**SP and Euclidean distances between facility points:**
The first line after **12 shortest paths and Euclidean distances between candidate facilities:**, constains **4 7 5 2.236068** meaning that facility points with ID = 4 and ID = 7 (or fp_0 and fp_1) are at distances SP[fp$_0$, fp$_1$] = 5 and D[fp$_0$, fp$_1$] = 2.236068, where SP is the shortest path distance and D the Euclidean distance.

**SP and Euclidean distances between facility points and clients:**
The first line after **12 shortest paths and Euclidean distances between clients and candidate facilities:**, constains **11 4 5 3.605551** meaning that client with ID = 11 and facility point with ID = 4 (or c$_0$ and fp$_0$) are at distances SP[c$_0$, fp$_0$] = 5 and D[c$_0$, fp$_0$] = 3.605551, where SP is the shortest path distance and D the Euclidean distance.


### A small pMD example:

25 3 4 3
3 clients:
11
12
13
4 candidate facilities:
4
7
9
14
3 constraints between facilities and clients:
0 0
1 1
2 1
3 constraints between facilities:
0 1 0
0 2 0
1 2 0
12 shortest paths and Euclidean distances between candidate facilities:
4 7 5 2.236068
4 9 1 1.000000
4 14 2 2.000000
7 4 5 2.236068
7 9 4 2.000000
7 14 3 2.236068
9 4 1 1.000000
9 7 4 2.000000
9 14 1 1.000000
14 4 2 2.000000
14 7 3 2.236068
14 9 1 1.000000
12 shortest paths and Euclidean distances between clients and candidate facilities:
11 4 5 3.605551
11 7 2 1.414214
11 9 4 3.162278
11 14 3 3.000000
12 4 4 2.828427
12 7 1 1.000000
12 9 3 2.236068
12 14 2 2.000000
13 4 3 2.236068
13 7 2 1.414214
13 9 2 1.414214
13 14 1 1.000000
