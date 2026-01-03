# Sudoku Solver

A Java implementation of a Sudoku puzzle solver using the backtracking algorithm. This program takes an unsolved Sudoku board and fills in the missing numbers to solve the puzzle.

## Features

- Solves standard 9x9 Sudoku puzzles
- Uses backtracking algorithm for efficient solving
- Includes safety checks to ensure valid placements
- Provides a sample unsolved board in the main method
- Prints the solved board to the console

## Prerequisites

- Java Development Kit (JDK) 8 or higher
- A Java IDE or command-line compiler

## How to Run

1. Clone or download the project files.
2. Compile the Java file:
   ```
   javac SudokuSolver.java
   ```
3. Run the program:
   ```
   java SudokuSolver
   ```

## Example Usage

The program includes a sample unsolved Sudoku board in the `main` method. When run, it will solve the puzzle and print the completed board.

### Sample Input (Unsolved Board):
```
5 3 . . 7 . . . .
6 . . 1 9 5 . . .
. 9 8 . . . . 6 .
8 . . . 6 . . . 3
4 . . 8 . 3 . . 1
7 . . . 2 . . . 6
. 6 . . . . 2 8 .
. . . 4 1 9 . . 5
. . . . 8 . . 7 9
```

### Sample Output (Solved Board):
```
5 3 4 6 7 8 9 1 2
6 7 2 1 9 5 3 4 8
1 9 8 3 4 2 5 6 7
8 5 9 7 6 1 4 2 3
4 2 6 8 5 3 7 9 1
7 1 3 9 2 4 8 5 6
9 6 1 5 3 7 2 8 4
2 8 7 4 1 9 6 3 5
3 4 5 2 8 6 1 7 9
```

## Algorithm Explanation

The Sudoku solver uses a backtracking algorithm:

1. **isSafe Method**: Checks if placing a number in a specific cell is valid by ensuring:
   - The number doesn't exist in the same row
   - The number doesn't exist in the same column
   - The number doesn't exist in the same 3x3 subgrid

2. **helper Method**: Recursively tries to fill the board:
   - If the current position is beyond the board, the puzzle is solved
   - If the cell is already filled, move to the next cell
   - Otherwise, try numbers 1-9 in the cell
   - If a number leads to a solution, return true
   - If not, backtrack by resetting the cell and trying the next number

3. **solveSudoku Method**: Initiates the solving process starting from the top-left cell.

This approach guarantees a solution if one exists, as it systematically explores all possible valid configurations.
