# AI Algorithms Collection 🚀

A compilation of three distinct AI-based algorithm implementations written in Python, covering classical and heuristic approaches for search and decision-making. Each program demonstrates a real-world inspired problem solved using a core AI technique.

## 📁 Contents

1. **A* Search Algorithm (Route Planner)**
2. **Genetic Algorithm (Trading Strategy Optimizer)**
3. **Minimax with Alpha-Beta Pruning (Chess & Mind Control Game)**

---

## 1. A* Search Algorithm (Route Planner)

This program reads a graph from a file and applies the A* search algorithm to find the shortest path between two user-defined cities. The graph consists of heuristic values and weighted edges.

### 🔧 Input Format (in `input.txt`)
City H Neighbor1 Cost1 Neighbor2 Cost2 ...

makefile
Copy
Edit
Example:

A 5 B 2 C 3

B 3 D 4

C 4 D 1

D 0


### ✅ Features:
- Reads graph & heuristics from file.
- Implements A* using a priority queue.
- Outputs the optimal path and total distance.

---

## 2. Genetic Algorithm (Trading Strategy Optimization)

This Python script uses genetic algorithms to evolve and optimize trading strategies based on historical market price changes. It simulates profits based on parameters like `stop_loss`, `take_profit`, and `trade_size`.

### ✅ Features:
- Custom profit computation function.
- Reproduction via crossover and mutation.
- Two types of crossover:
  - Value-level (dictionary based)
  - Bitstring crossover (string representation)
- Output: Best strategy and total profit.

---

## 3. Minimax with Alpha-Beta Pruning (Chess Game Simulator & Mind Control Game)

This section simulates two types of strategic games:

### ♟️ Chess Game Simulator
- Simulates 4 games between **Magnus Carlsen** and **Fabiano Caruana**.
- Uses Alpha-Beta pruning to decide outcomes based on given "strength" values.
- Alternates starting players and summarizes total wins and draws.

### 🧠 Mind Control Game
- Introduces an alternate decision tree with a costly `Mind Control` move.
- Evaluates whether using mind control improves game outcome.
- Compares adjusted and unadjusted Minimax values.

---

