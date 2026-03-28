# lab-report-02
Title : Implementation of A* search for Pathfinding in a 2D Grid Maze

NAME : Thiaba Rahman Methi ID : 232002042

Course Title: Artificial Intelligence Lab Course Code: CSE-316 Section:232_D7

**Problem**

You are given a 2D grid representing a maze, where each cell is either an empty space (0) or a wall (1). Your task is to implement a Python program that uses the A* search algorithm to find the shortestpath from a given start cell to a specified target cell. You may move up, down, left, or right to adjacent empty cells, but you cannot pass through walls. Each move has a cost of 1, and you should use the Manhattan distance as the heuristic to estimate the cost from any cell to the target.

Your program must read all input from a file named input.txt. The format of input.txt is:
First line: two integers R C – number of rows and columns.
Next R lines: the grid, with 0 and 1 separated by spaces.
Next line: two integers sr sc – start cell coordinates (row, column).
Last line: two integers tr tc – target cell coordinates (row, column).

**Solution**

I have used the A* Search Algorithm, which is an informed search technique used to find the shortest path from a start cell to a target cell in a maze. The algorithm uses both the actual cost from the start node and a heuristic cost to estimate the best possible path. In this problem, I used Manhattan distance as the heuristic function because movement is allowed only in four directions: up, down, left, and right. The algorithm repeatedly selects the node with the lowest total cost value until the goal is found or no valid path remains.

**Steps**

Start from the initial cell and add it to the priority queue.
Calculate F(n)=G(n)+H(n) using Manhattan distance.
Select the node with the lowest F(n).
If it is the goal, return the path and cost.
Otherwise, explore valid neighboring cells.
Update cost and insert them into the queue.
Repeat until the goal is found or no path exists.

Case#1Input:
4 4
0 0 0 0
1 1 0 1
0 0 0 0
0 1 1 0
0 0
3 3

Case#1Output:
Path found with cost 6 using A*
Shortest Path: [(0,0), (0,1), (0,2), (1,2), (2,2), (2,3), (3,3)]

Case#2Input:
3 3
0 1 0
0 1 0
0 1 0
0 0
2 2

Case#2Output:
Path not found using A*
