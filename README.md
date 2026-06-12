# Algorithm Simulation (Pygame)

Visual simulations of classic algorithms built with **Pygame**. Each simulation draws the algorithm's data and animates its steps so the process can be watched in real time. The repository currently contains an interactive visualization of **Kruskal's Minimum Spanning Tree (MST)** algorithm.

![Screenshot](Kruskal_simulation/Screenshot%20.png?raw=true "Kruskal's MST simulation")

## Simulations

### Kruskal's MST (`Kruskal_simulation/`)

Reads a weighted, undirected graph from `input.txt`, computes its Minimum Spanning Tree using Kruskal's algorithm (with union-find / disjoint-set and union-by-rank), and animates the result:

- Nodes are placed at random positions and labelled.
- All graph edges are drawn first (in green).
- MST edges are then highlighted one at a time (in blue), with each edge's endpoints and weight listed on the right side of the window.
- Non-MST edges are removed and the total MST weight is displayed.

## Tech Stack

- **Language:** Python
- **Library:** [Pygame](https://www.pygame.org/) (rendering and animation)
- **Algorithm:** Kruskal's MST with union-find (see `graph.py`)

## Project Structure

```
Kruskal_simulation/
├── main.py         # Pygame app: reads the graph, runs Kruskal, animates the MST
├── graph.py        # Graph class: addEdge, KruskalMST (union-find), MST weight helpers
├── input.txt       # Input graph: first line "<num_vertices> <num_edges>", then "u v w" per edge
└── Screenshot .png # Sample output screenshot
```

### Input format (`input.txt`)

```
<number_of_vertices> <number_of_edges>
u v w
u v w
...
```

Each subsequent line lists an edge between vertices `u` and `v` with integer weight `w`.

## Install & Run

1. Install Python 3 and Pygame:
   ```bash
   pip install pygame
   ```
2. Run the simulation from inside the simulation folder (so `input.txt` is found):
   ```bash
   cd Kruskal_simulation
   python main.py
   ```
3. A window titled "Kruskal's MST" opens and animates the MST construction. Close the window to exit.

To visualize a different graph, edit `input.txt` to match the format above.
