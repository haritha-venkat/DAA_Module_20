# EX 2A BACKTRACKING - RAT IN MAZE PROBLEM
## DATE:

## AIM:
To implement the Rat in a Maze problem using backtracking and find all possible paths from the start to the destination in a given maze.


## Algorithm

1. Initialize a 4×4 maze as a 2D list, where `1` indicates a valid path and `0` indicates a blocked cell.  
2. Define a helper function `isSafe` that checks whether the current cell `(x, y)` is within bounds and open (`maze[x][y] == 1`).  
3. Create a solution matrix `sol` initialized with all zeros to store the path taken by the rat.  
4. Start from the top-left cell `(0, 0)` and use a recursive function `solveMazeUtil` to explore the path.  
5. In `solveMazeUtil`, if the destination `(N-1, N-1)` is reached, mark it as part of the solution path and return `True`.  
6. If the current cell `(x, y)` is safe, mark it as part of the path in `sol[x][y] = 1`.  
7. Move forward recursively in the maze: first try moving down (`x + 1`) and then right (`y + 1`).  
8. If moving in both directions fails, backtrack by marking `sol[x][y] = 0` and return `False`.  
9. In the main function `solveMaze`, print the solution matrix if a path is found; otherwise, print that no solution exists.  
10. Call the `solveMaze` function with the initialized maze to start the process.

## Program:
```
/*
Program to implement Rat in a Maze.
Developed by: 
Register Number:
N = 4
def printSolution( sol ):
    for i in sol:
        for j in i:
            print(str(j) + " ", end ="")
        print("")
def isSafe( maze, x, y ):
    if x >= 0 and x < N and y >= 0 and y < N and maze[x][y] == 1:
        return True
    return False
def solveMaze( maze ):
    # Creating a 4 * 4 2-D list
    sol = [ [ 0 for j in range(4) ] for i in range(4) ]
     
    if solveMazeUtil(maze, 0, 0, sol) == False:
        print("Solution doesn't exist");
        return False
     
    printSolution(sol)
    return True
def solveMazeUtil(maze, x, y, sol):
    if x==N-1 and y==N-1:
        sol[x][y]=1
        return True
    if isSafe(maze,x,y)==True:
        sol[x][y]=1
        if solveMazeUtil(maze,x+1,y,sol):
            return True
        if solveMazeUtil(maze,x,y+1,sol):
            return True
        sol[x][y]=0
        return False
    return False

if __name__ == "__main__":
    # Initialising the maze
    maze = [ [1, 0, 0, 0],
             [1, 1, 0, 1],
             [0, 1, 0, 0],
             [1, 1, 1, 1] ]
              
    solveMaze(maze)
*/
```

## Output:

![Screenshot 2025-04-29 140037](https://github.com/user-attachments/assets/a688eaac-ae7c-4c31-81dd-fb974286e0eb)



## Result:
The Rat in a Maze program executed successfully, and a valid path from the start to the destination was found and display.
