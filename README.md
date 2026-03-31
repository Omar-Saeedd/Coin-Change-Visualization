# Coin Change Algorithm Visualization

An interactive educational visualization of the **Coin Change problem** that demonstrates the difference between **naive recursion** and **dynamic programming (DP)**.

The project visualizes how recursive solutions generate large recursion trees with repeated subproblems, and how dynamic programming eliminates this redundancy by storing intermediate results.

The goal is to help students understand:

* optimal substructure
* overlapping subproblems
* recursion trees
* bottom-up dynamic programming

---

## Features

### Dynamic Programming Table Visualization

Step-by-step construction of the DP table for the coin change problem.

Shows:

* table initialization
* transitions `dp[i] = min(dp[i], dp[i − coin] + 1)`
* optimal updates
* parent tracking for solution reconstruction

---

### Recursion Tree Visualization

Animated recursion tree representing the naive recursive solution.

The tree shows:

* recursive subproblem expansion
* depth-first recursion execution
* repeated subproblems
* overlapping subproblems highlighted

The visualization is **depth-limited** to keep the tree readable.

---

### Overlapping Subproblem Detection

Repeated subproblems are highlighted in the recursion tree.

This demonstrates the core reason dynamic programming is effective: the recursive algorithm recomputes the same states many times.

---

### Step-by-Step Explanation

The system dynamically explains what happens during recursion and DP execution, including:

* recursive call generation
* remaining amounts
* subproblem creation
* DP table updates
* number of duplicated recursive calls

---

### Optional Preprocessing Demonstration

Coin sorting is included as an **optional preprocessing step** for visualization clarity.

Sorting is **not required** by the dynamic programming algorithm.

---

## Algorithm Background

### Naive Recursion

The recursive formulation:

```
f(amount) = min(f(amount − coin) + 1)
```

This approach generates a recursion tree that grows **exponentially** due to repeated subproblems.

Time complexity:

```
Exponential ≈ O(c^W)
```

Where:

* `c` = number of coin types
* `W` = target amount

---

### Dynamic Programming

Dynamic programming solves the problem bottom-up:

```
dp[i] = min(dp[i], dp[i − coin] + 1)
```

Each subproblem is solved **once**, preventing repeated computation.

Time complexity:

```
O(n · W)
```

Where:

* `n` = number of coin types
* `W` = target amount

---

## Technologies Used

* HTML
* CSS
* Vanilla JavaScript
* SVG for recursion tree visualization

No external libraries are required.

---

## How to Run

Clone the repository:

```
git clone https://github.com/omar-saeedd/coin-change-dp-visualization.git
```

Open the project by loading:

```
index.html
```

in any modern web browser.

No build step or installation is required.

---

## Educational Purpose

This project was created as part of an **Algorithms course project** to illustrate the relationship between recursion and dynamic programming using visual tools.

The visualization focuses on helping students build intuition for:

* recursion tree growth
* repeated subproblem computation
* dynamic programming optimization

---

## Example Concepts Demonstrated

* recursion tree expansion
* exponential algorithm growth
* overlapping subproblems
* optimal substructure
* bottom-up dynamic programming table construction

---

## License

MIT License
