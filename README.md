# Sudoku Solver

**Authors**: Gabe Krishnadasan and Marissa Esteban  
**Date**: April 30, 2023  

## Description

This project provides an efficient Sudoku solver that supports puzzles of multiple sizes:
- Standard 9x9 Sudoku.
- Advanced 16x16 and 25x25 Sudoku variants, with custom alphanumeric grid notations.

The solver uses a combination of:
1. Recursive backtracking for exhaustive search.
2. Constraint propagation to reduce the search space.
3. Preprocessing to handle non-standard grid formats.

## Features

- **Multi-size Support**: Solves Sudoku puzzles of sizes 9x9, 16x16, and 25x25.
- **Custom Notations**: Translates alphanumeric entries for larger grids into numeric representations for computation and converts them back for the final output.
- **Constraint Propagation**: Reduces possibilities for empty cells by eliminating conflicting values.
- **Recursive Backtracking**: Efficiently explores potential solutions using depth-first search.
- **Detailed Statistics**: Reports the number of nodes generated in the state-space tree for each solution.

## How It Works

1. **Input**: 
   - A text file containing predefined cell values in a row-column-value format.
   - The size of the Sudoku grid (9, 16, or 25).

2. **Initialization**:
   - Reads the input file to construct the grid and track empty cells.
   - Maps alphanumeric values (for grids larger than 9x9) into numeric representations.

3. **Constraint Propagation**:
   - Uses existing values in rows, columns, and subgrids to narrow down possibilities for each empty cell.

4. **Backtracking**:
   - Explores possible assignments recursively until a solution is found or determined to be unsolvable.

5. **Output**:
   - Prints the solved Sudoku grid.
   - Reports the total number of nodes generated during the search.

## File Structure

- **SudokuSolver.py**: Main implementation of the Sudoku solver.
- **p2.txt**: Example input file containing a 9x9 Sudoku puzzle.
