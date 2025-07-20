
---

````markdown
# Missionaries and Cannibals Problem - AI Project

This repository contains a Python implementation of the **Missionaries and Cannibals Problem**, a classic problem in Artificial Intelligence (AI) used to illustrate state-space search and constraint satisfaction techniques. The solution uses the **Breadth-First Search (BFS)** algorithm to find the shortest path from the initial to the goal state.

## 📌 Problem Statement

You must transport **three missionaries and three cannibals** across a river using a boat that can carry at most two people. The key constraint is that **missionaries can never be outnumbered by cannibals** on either riverbank at any time, or the missionaries will be eaten.

---

## 🎯 Goal

Safely transfer all individuals to the opposite riverbank without violating the constraints. The program ensures that all moves are legal and uses BFS to find the shortest valid solution.

---

## 🛠️ Technologies Used

- **Python 3**
- `collections.deque` for queue-based BFS
- Tuple-based state representation

---

## 🚀 How It Works

1. Each state is a tuple: `(M_left, C_left, Boat_side)`
2. Valid moves include:
   - 1 Missionary
   - 1 Cannibal
   - 2 Missionaries
   - 2 Cannibals
   - 1 Missionary + 1 Cannibal
3. The algorithm uses BFS to:
   - Explore all valid transitions from the current state
   - Avoid cycles by tracking visited states
   - Return the path once the goal state is reached

---

## 🧪 Output Example

```bash
Solution:
Missionaries on left: 3, Cannibals on left: 3, Boat on left: 1
Missionaries on left: 2, Cannibals on left: 2, Boat on left: 0
...
Missionaries on left: 0, Cannibals on left: 0, Boat on left: 0
````

---

## 📄 Source Code Overview

```python
from collections import deque

initial_state = (3, 3, 1)
goal_state = (0, 0, 0)

def is_valid_state(m, c):
    return (m >= 0 and c >= 0 and (m == 0 or m >= c))

def get_next_states(m, c, boat):
    ...

def solve_missionaries_cannibals():
    ...

solution = solve_missionaries_cannibals()
if solution:
    for step in solution:
        print(step)
else:
    print("No solution found.")
```

---

## 👨‍💻 Author

* **Mohammed Arsh Khan**
  B.Tech in Information Technology
  CMREC (UGC Autonomous)

Project Guide: **Mrs. G. Swetha**, Assistant Professor, Dept. of IT
HOD: **Dr. Madhavi Pingili**, Assoc. Professor & HOD, Dept. of IT

---

## 📝 License

This project is for educational use and distributed under the [MIT License](LICENSE).

```

---

