---
title: "Sudoku Solver in MATLAB"
date: 2026-05-12
draft: false
tags: ["matlab", "algorithms", "recursion", "backtracking"]
cover:
  image: "/wag-labs/images/sudoku-solver/Solved%20Board.png"
  alt: "Sudoku solver inputs and outputs"
  relative: false
---

## Overview
A recursive, backtracking Sudoku solver in MATLAB that can deterministically solve any valid starting board.

- Prompts the user for a full 9×9 Sudoku board and checks that it is valid
- Evaluates the number of options for each unfilled square (zeros)
- Starting on the square with the fewest options, it picks one and continues
- If an unfilled square has no valid numbers, it backtracks one level and retries the next valid number in the list
- Uses recursion and backtracking
- Can deterministically solve any valid starting board

![Unsolved Board](/wag-labs/images/sudoku-solver/Unsolved%20Board.png)
*Unsolved Board*

![Solved Board](/wag-labs/images/sudoku-solver/Solved%20Board.png)
*Solved Board*
