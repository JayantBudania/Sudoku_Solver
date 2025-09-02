# Sudoku Solver (DSA Project)

A simple python based **Sudoku Solver** implemented using **backtracking with MRV (Minimum Remaining Values)** heuristic.  

---

##  Features
- Solves any **9x9 Sudoku puzzle**.
- Uses **backtracking algorithm** with MRV heuristic for efficiency.
- Works with puzzles provided as:
  - 81-character strings (with `0` or `.` for blanks).
  - 9×9 nested Python lists.
- Includes pretty-printing of the Sudoku grid.
- Reports **time taken** and **number of recursive calls**.

---

##  How It Works
1. Choose the next empty cell using **MRV heuristic** (minimum candidates).
2. Try candidate numbers `1–9` that do not violate row/column/3×3 constraints.
3. Backtrack if no candidate works.
4. Continue until the puzzle is solved.

---

##  Usage in Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new Notebook.
3. Copy the full code from `sudoku_solver.py` into a code cell.
4. Run the cell — it will solve the **example puzzles** included.

Example run:
```python
# Run the solver with the easy puzzle
run_and_time(easy)

# Run with a harder puzzle
run_and_time(hard)

# Custom puzzle (81-char string, 0 = blank)
my_puzzle = (
    "530070000"
    "600195000"
    "098000060"
    "800060003"
    "400803001"
    "700020006"
    "060000280"
    "000419005"
    "000080079"
)
run_and_time(my_puzzle)

Input puzzle:
5 3 . | . 7 . | . . .
6 . . | 1 9 5 | . . .
. 9 8 | . . . | . 6 .
------+-------+------
8 . . | . 6 . | . . 3
4 . . | 8 . 3 | . . 1
7 . . | . 2 . | . . 6
------+-------+------
. 6 . | . . . | 2 8 .
. . . | 4 1 9 | . . 5
. . . | . 8 . | . 7 9

Solved puzzle:
5 3 4 | 6 7 8 | 9 1 2
6 7 2 | 1 9 5 | 3 4 8
1 9 8 | 3 4 2 | 5 6 7
------+-------+------
8 5 9 | 7 6 1 | 4 2 3
4 2 6 | 8 5 3 | 7 9 1
7 1 3 | 9 2 4 | 8 5 6
------+-------+------
9 6 1 | 5 3 7 | 2 8 4
2 8 7 | 4 1 9 | 6 3 5
3 4 5 | 2 8 6 | 1 7 9

Time: 0.0024 s, recursive calls: 54
