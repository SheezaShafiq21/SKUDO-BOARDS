# SKUDO-BOARDS
Overview:
This project presents a complete implementation of a Sudoku solver based on Constraint Satisfaction Problem (CSP) techniques. The solver integrates AC-3 (Arc Consistency) with Backtracking Search, enhanced by Forward Checking and the Minimum Remaining Values (MRV) heuristic.It is designed to efficiently solve Sudoku puzzles of varying difficulty levels, including easy, medium, hard, and very hard instances.

Features:
Solves standard 9×9 Sudoku puzzles
Uses AC-3 for domain reduction before and during search
Implements backtracking with forward checking
Applies MRV heuristic to improve variable selection
Handles multiple difficulty levels
Reports execution time, backtracking calls, and failures

Project Structure:
1. easy.txt
2. medium.txt
3. hard.txt
4. veryhard.txt
5. sudoku_solver.py
6. README.md

Algorithms and Techniques:

AC-3 (Arc Consistency):
The AC-3 algorithm is used to enforce consistency across variables by removing values from domains that violate constraints. This reduces the search space significantly before backtracking begins.

Backtracking Search:
A recursive depth-first search approach that assigns values to variables and backtracks when a constraint violation occurs.

Forward Checking:
After assigning a value, forward checking eliminates inconsistent values from neighboring variables, preventing future conflicts early.

Minimum Remaining Values (MRV):
This heuristic selects the variable with the smallest domain first, improving efficiency by reducing branching.

How to Run
Clone the repository:
git clone https://github.com/your-username/sudoku-solver.git
cd sudoku-solver

Run the solver:
python sudoku_solver.ipynb

Input Format:
Each Sudoku puzzle is stored in a .txt file as a 9×9 grid of digits:

Digits 1–9 represent assigned values
0 represents an empty cell


Example:
530070000
600195000
098000060
800060003
400803001
700020006
060000280
000419005
000080079

Output:
For each puzzle, the program displays:
Initial board
Solved board
Execution time (in seconds)
Number of backtracking calls
Number of failures

Performance Notes:
The combination of AC-3 with MRV and forward checking significantly reduces the number of backtracking steps compared to a naive brute-force approach. Performance may vary depending on puzzle difficulty.
