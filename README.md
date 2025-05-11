# Graph Algorithm Visualizer

An interactive web-based application for visualizing graph algorithms with focus on pathfinding algorithms like Dijkstra's algorithm.

![Graph Algorithm Visualizer Screenshot](https://api.placeholder.com/800/400)

## 🚀 Features

- **Interactive Graph Creation**: Build custom graphs with weighted edges through an intuitive interface
- **Step-by-Step Visualization**: See how algorithms work internally with animated step-by-step execution
- **Algorithm Information**: Learn about time and space complexity for each algorithm
- **Detailed Controls**: Navigate forward/backward through algorithm execution
- **Comprehensive Legend**: Understand the meaning of colors and visual indicators
- **Extensible Architecture**: Designed to easily add more algorithms in the future

## 📋 Currently Implemented Algorithms

- **Dijkstra's Algorithm**: Single-source shortest path algorithm for graphs with non-negative edge weights
  - **Time Complexity**: O((V + E) log V)
  - **Space Complexity**: O(V)
  - Where V is the number of vertices and E is the number of edges

## 🌐 Live Demo

Check out the live demo: [Graph Algorithm Visualizer](https://algorithmvisualizerbyrachit.netlify.app/)

## 🛠️ Installation

No installation required! This is a client-side web application that runs in your browser.

### Option 1: Use the Live Demo

Visit the [live demo](https://algorithmvisualizerbyrachit.netlify.app/) to use the application without installing anything.

### Option 2: Run Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/graph-algorithm-visualizer.git
   ```

2. Navigate to the project directory:
   ```bash
   cd graph-algorithm-visualizer
   ```

3. Open `index.html` in your web browser:
   ```bash
   # On macOS
   open index.html
   
   # On Linux
   xdg-open index.html
   
   # On Windows
   start index.html
   ```

## 📚 How to Use

### Creating a Graph

1. Use the "Graph Setup" section to add edges to your graph
2. For each edge, specify:
   - **From Node**: Starting node identifier (e.g., "A")
   - **To Node**: Ending node identifier (e.g., "B")
   - **Weight**: Edge weight (e.g., 5)
3. Click "Add Edge" to add more edges

### Running an Algorithm

1. Select an algorithm from the dropdown menu
2. Enter a start node
3. (Optional) Enter an end node if you want to find the shortest path to a specific node
4. Adjust the animation speed if desired
5. Click "Visualize" to start the algorithm

### Using Controls

- **Next**: Move forward one step in the algorithm
- **Previous**: Move backward one step in the algorithm
- **Reset**: Reset the visualization to its initial state

## 🧩 Python Implementation

A Python implementation is also available in this repository for those who prefer to use the visualizer in a Python environment.

### Requirements

- Python 3.6+
- NetworkX
- Matplotlib

### Usage

```python
from dijkstra_visualizer import AlgorithmVisualizer

# Create a sample graph
edges = [
    ('A', 'B', 4), ('A', 'C', 2), ('B', 'C', 1), ('B', 'D', 5),
    ('C', 'D', 8), ('C', 'E', 10), ('D', 'E', 2), ('D', 'F', 6),
    ('E', 'F', 3)
]

# Create visualizer
visualizer = AlgorithmVisualizer()
visualizer.create_graph(edges, weighted=True)

# Visualize Dijkstra's algorithm from node 'A' to node 'F'
anim = visualizer.visualize_dijkstra('A', 'F', animation_speed=1000)

# Show the visualization
visualizer.show()

# Optionally save the animation
# visualizer.save_animation('dijkstra.gif')
```

## 🔄 Adding New Algorithms

The visualizer is designed to be easily extensible. To add a new algorithm:

### For Web Version:

1. Create a new run function for your algorithm (similar to `runDijkstra`)
2. Register it using the `addAlgorithm` method:

```javascript
visualizer.addAlgorithm(
    "Algorithm Name",
    function(startNode, endNode) {
        // Implementation
    },
    "<p>Algorithm description HTML</p>",
    "<b>Time Complexity:</b> O(...)<br><b>Space Complexity:</b> O(...)"
);
```

### For Python Version:

1. Add a new method to the `AlgorithmVisualizer` class (similar to `visualize_dijkstra`)
2. Add the algorithm name to the `visualize_algorithm` method

## 📊 Planned Algorithms

- Breadth-First Search (BFS)
- Depth-First Search (DFS)
- A* Search Algorithm
- Bellman-Ford Algorithm
- Floyd-Warshall Algorithm
- Prim's Minimum Spanning Tree
- Kruskal's Minimum Spanning Tree

## 🤝 Contributing

Contributions are welcome! Feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- [Cytoscape.js](https://js.cytoscape.org/) for graph visualization
- [NetworkX](https://networkx.org/) and [Matplotlib](https://matplotlib.org/) for the Python implementation

## 📧 Contact

Your Name - [@rachits999003](mailto:rachits999003@gmail.com) - email@example.com
