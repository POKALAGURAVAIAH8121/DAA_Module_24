# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE:
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm
1. Create a list of all cities (excluding the starting city).

2. Gnerate all possible routes (permutations) that visit each city exactly once.

3. For each route, calculate the total distance traveled, including returning to the starting city.

4. Track Minimum Distance: Keep track of the shortest distance found among all routes.

5.  Return the shortest distance as the solution.

## Program:
```
/*
To implement the program for TSP.
Developed by: POKALA GURAVAIAH
Register Number: 212222040114
*/
```
```
from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
    vetex=[]
    cur=0
    minpath=maxsize
    for i in range(V):
        if i!=s:
            vetex.append(i)
    # k=s
    nextper=permutations(vetex)
    for i in nextper:
        cur=0
        k=s
        for j in i:
            cur+=graph[k][j]
            k=j
        cur+=graph[k][s]
        minpath=min(minpath,cur)
    return minpath

if __name__ == "__main__":
 
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],[15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s))
```
## Output:
<img width="500" alt="image" src="https://github.com/user-attachments/assets/195874f6-731a-453d-9dc7-d6d5755d80c9"/>

## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
