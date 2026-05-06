# Sudoku Solver
**Authors:** Pauline De Baets, Mio Kobayashi, Fatima Al Aridhee

**Date:** Autumn 2022

## Description

This project is a Python Sudoku solver. The goal of the program is to take an incomplete Sudoku grid, solve it automatically, and display the completed grid.

The program is based on the idea that a Sudoku can be represented as a logical problem. In the current implementation, the Sudoku is solved using a SAT solver with the `pycosat` library. Each possible value in each cell is represented as a logical variable, and the rules of Sudoku are translated into logical clauses.

The solver makes sure that:

- Every cell contains exactly one number from 1 to 9.
- Each row contains each number only once.
- Each column contains each number only once.
- Each 3x3 box contains each number only once.
- The numbers already given in the original grid are respected.

The program can then solve the Sudoku by finding a valid combination of values that satisfies all these rules.

## User Experience

The program is designed to allow the user to solve Sudoku grids in a simple way.

The user can enter a Sudoku grid where empty cells are represented by `0`. The program then solves the grid and displays the completed version.

For example, an incomplete Sudoku grid is written as a list of lists:

```python
hard = [
    [0, 2, 0, 0, 0, 0, 0, 0, 0],
    [0, 0, 0, 6, 0, 0, 0, 0, 3],
    [0, 7, 4, 0, 8, 0, 0, 0, 0],
    [0, 0, 0, 0, 0, 3, 0, 0, 2],
    [0, 8, 0, 0, 4, 0, 0, 1, 0],
    [6, 0, 0, 5, 0, 0, 0, 0, 0],
    [0, 0, 0, 0, 1, 0, 7, 8, 0],
    [5, 0, 0, 0, 0, 9, 0, 0, 0],
    [0, 0, 0, 0, 0, 0, 0, 4, 0]
]
