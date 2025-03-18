# AI Foundation Projects: Search, Optimization, and Game Theory

This repository contains solutions to foundational problems in Artificial Intelligence, focusing on search algorithms, genetic optimization, and adversarial game strategies. By solving these problems, I explore core AI concepts and build a strong theoretical and practical foundation in intelligent systems.

---

## Problem Descriptions

### 1. **Optimal Pathfinding with A* Search**  
**Source**: `A Star.pdf`  

**Objective**:  
Implement the A* search algorithm to determine the shortest path from **Arad** to **Bucharest** using heuristic values (straight-line distances) and city connectivity data.  

**Key Details**:  
- **Input**:  
  - A text file where each line represents a city, its heuristic value (distance to Bucharest), and neighboring cities with edge weights.  
  - Example input line:  
    `Arad 366 Zerind 75 Sibiu 140 Timisoara 118`  
    (Arad has a heuristic of 366 and connects to Zerind, Sibiu, and Timisoara with distances 75, 140, and 118, respectively).  
- **Output**:  
  - The optimal path and total distance.  
  - Example output:  
    `Path: Arad -> Sibiu -> Rimnicu -> Pitesti -> Bucharest | Total distance: 418 km`.  

**Solution Approach**:  
- Parse the input file to construct a graph with cities as nodes and distances as edge weights.  
- Use the A* algorithm with the provided heuristic values to prioritize nodes during traversal.  
- Track the path and cumulative distance to Bucharest.  

---

### 2. **Trading Strategy Optimization with Genetic Algorithms**  
**Source**: `GeneticAlgo.pdf`  

**Objective**:  
Develop a genetic algorithm (GA) to evolve optimal trading parameters (stop-loss, take-profit, trade size) for a cryptocurrency trading bot, maximizing profit over historical price data.  

**Key Details**:  
- **Chromosome Representation**:  
  - Encoded as a string (e.g., `020520` = 2% stop-loss, 5% take-profit, 20% trade size).  
- **Fitness Function**:  
  - Simulate trading over 10 days with historical price changes.  
  - Calculate profit as `Final Capital - Initial Capital ($1000)`.  
- **Steps**:  
  1. **Population Initialization**: Generate 4 random chromosomes.  
  2. **Fitness Evaluation**: Simulate trades and compute profits.  
  3. **Parent Selection**: Randomly select two parents.  
  4. **Crossover**: Perform two-point crossover to create offspring.  
  5. **Mutation**: Apply a 5% mutation rate to genes.  
  6. **New Population**: Generate the next generation via elitism, crossover, and mutation.  

**Sample Input/Output**:  
- **Input**: Historical prices `[-1.2, 3.4, ..., 3.5]`, initial population of 4 chromosomes.  
- **Output**: Best strategy (e.g., `{"stop_loss": 2.3, ...}`) and final profit (e.g., `12.5`).  

---

### 3. **Chess Game Analysis with Minimax and Alpha-Beta Pruning**  
**Source**: `MinMax.pdf`  

**Objective**:  
Simulate a chess game between two players using the Minimax algorithm with alpha-beta pruning to determine the optimal moves and overall winner across four games.  

**Key Details**:  
- **Players**: Magnus Carlsen (Max) and Fabiano Caruana (Min).  
- **Game Setup**:  
  - Each game alternates the starting player (Max/Min roles).  
  - Branching factor = 2 (two moves per turn), max depth = 5.  
- **Utility Function**:  
  - `utility = strength(maxV) - strength(minV) + (-1)^t * random(1,10)/10`,  
    where `strength(x) = log2(x + 1) + x/10`.  
  - `maxV` and `minV` are base strengths of players.  
- **Alpha-Beta Pruning**: Optimize the search by pruning non-promising branches.  

**Sample Input/Output**:  
- **Input**: Starting player (0 or 1), base strengths (e.g., `Carlsen: 9, Caruana: 8`).  
- **Output**: Winner of each game and overall results (e.g., `Magnus Carlsen Wins: 3`).  

**Extension (Problem 2)**:  
- **Mind Control Twist**: The first player can control the opponent’s move at a cost.  
- **Decision**: Compare minimax values with/without mind control to decide if using it maximizes utility.  

---

## Repository Structure  
- `/A_Star`: Code and input files for pathfinding.  
- `/Genetic_Algo`: Implementation of GA for trading strategy optimization.  
- `/Minimax`: Chess game simulation with alpha-beta pruning.  
- `README.md`: This document.  

## How to Use  
Run the respective script for each problem
python a_star.py
python genetic_algo.py
python minimax.py
  

---

By solving these problems, I gained hands-on experience with fundamental AI algorithms and their applications in real-world scenarios. This repository serves as a portfolio of my journey in mastering AI techniques.  
