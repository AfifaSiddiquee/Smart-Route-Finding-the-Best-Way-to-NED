# SmartRoute-NED 🚦
**Finding the Best Way to NED University using Classic Pathfinding Algorithms**

**Course:** CT-363 Design and Analysis of Algorithms  

**Department:** Computer Science & Information Technology, NED University  

**Student:** Afifa Siddique  

---

##  Overview

In a bustling city like Karachi, selecting the most effective route for daily commutes is a common challenge. **SmartRoute-NED** is a congestion-aware routing system designed to guide commuters from different regions of Karachi to **NED University of Engineering & Technology** through the shortest and most optimal paths. This system uses graph theory and classical pathfinding algorithms such as **BFS, DFS, Dijkstra**, and **A\*** to model real-world routes, simulate traffic congestion, and recommend alternative paths if needed.

---

##  Problem Statement

Most navigation systems fail to dynamically adapt to fluctuating traffic conditions. This project addresses that gap by:
- Representing Karachi’s roads as a weighted graph with congestion simulation.
- Calculating real-time travel times based on congestion.
- Providing alternate routing when congestion exceeds a threshold.

---

##  Objectives

- Simulate Karachi's road network using a weighted undirected graph.
- Compare the performance of **BFS**, **DFS**, **Dijkstra**, and **A\*** algorithms.
- Generate visualizations of paths and traffic-aware suggestions.
- Provide backup routes when congestion exceeds 0.4.

---

##  Technologies Used

| Technology     | Purpose                                       |
|----------------|-----------------------------------------------|
| Python         | Core development language                    |
| NetworkX       | Graph modeling and traversal                 |
| Matplotlib     | Graph visualization                          |
| Flask          | Interactive web deployment (optional)        |
| Random module  | Simulates live congestion on road segments   |

---

##  Input Details

- **Nodes**: Locations in Karachi (e.g., North Nazimabad, Gulshan-e-Iqbal)
- **Edges**: Roads with:
  - Distance (in km)
  - Congestion (randomized between 0.1 and 0.8)

**Travel Time Formula:**
Time (min) = (Distance / 30) * 60 * (1 + Congestion)


---

##  Algorithms Implemented

### 1. Breadth-First Search (BFS)
- Explores nearest nodes first.
- Ignores edge weights — does not guarantee optimal path.

### 2. Depth-First Search (DFS)
- Explores as deep as possible before backtracking.
- Ignores edge weights — may find inefficient paths.

### 3. Dijkstra’s Algorithm 
- Considers real-time congestion and finds the optimal path.
- Guaranteed shortest path in a weighted graph.

### 4. A* Algorithm 
- Similar to Dijkstra but incorporates a heuristic.
- Currently heuristic = 0 → behaves like Dijkstra.
- Can be extended for faster performance with real heuristics.

---

##  Key Features

- **Congestion Simulation:** Randomly updates congestion values to reflect changing traffic.
- **Alternate Path Suggestion:** Automatically switches to a congestion-free route when needed.
- **Multi-Source Handling:** Visualizes paths from four different starting points to one destination (NED).
- **Visualization:** Saves PNG files of network graphs and computed paths.

---

##  Sample Results

| Source Location   | Algorithm | Travel Time | Alternate Time (if congested) |
|-------------------|-----------|-------------|-------------------------------|
| North Nazimabad   | BFS       | 28 min      | N/A                           |
| North Nazimabad   | DFS       | 28 min      | N/A                           |
| North Nazimabad   | Dijkstra  | 25.8 min    | 26.8 min                      |
| North Nazimabad   | A*        | 25.8 min    | 26.8 min                      |

---

## 📌 Best Performing Algorithm

✅ **Dijkstra’s Algorithm** (or **A\*** with heuristic = 0)
- Considers congestion-adjusted travel time.
- Provides shortest and most reliable route.

---

##  Future Improvements

-  Integrate **real-time traffic APIs** (Google Maps, Mapbox).
-  Build a **mobile-friendly web app** using Flask or React.
-  Add **geographical heuristics** (e.g., Haversine formula for A\*).
-  User preferences: Shortest route vs. Least congestion vs. Fastest time.
-  Expand to more locations or cities.

---



