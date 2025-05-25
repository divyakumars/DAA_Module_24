# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE: 06/05/25
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)


## Algorithm
1. Input: A graph (adjacency matrix) and a starting vertex s.

2. Generate all permutations of remaining vertices (excluding s).

3. For each permutation: Initialize k = s, cp = 0 (current path cost)

4. Add edge cost for each move in permutation

5. Add cost to return back to starting vertex s

6. Track the minimum path cost

7. Return the minimum path cost found.

## Program:

To implement the program for TSP.

Developed by: DIVYA K

Register Number: 212222230035

```
from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
 
    v=[]
    for i in range(V):
        if i!=s:
            v.append(i)
    mp=maxsize
    np=permutations(v)
    for i in np:
        k=s
        cp=0
        for j in i:
            cp+=graph[k][j]
            k=j
        cp+=graph[k][s]
        mp=min(cp,mp)
    return mp
   
 
if __name__ == "__main__":
 
        graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
        s = 0
        print(travellingSalesmanProblem(graph, s))
```
## Output:
![image](https://github.com/user-attachments/assets/3d1126d8-20b0-4675-8760-c9c5c58cbad2)


## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
