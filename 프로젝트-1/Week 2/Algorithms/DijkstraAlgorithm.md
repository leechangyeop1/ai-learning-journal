# Dijkstra Algorithm

Dijkstra's algorithm is a popular algorithm used for finding the shortest paths between nodes in a graph. It is particularly useful in scenarios where you need to determine the shortest path from a starting node to all other nodes in a weighted graph.

## Overview

- **Purpose**: To find the shortest path from a source node to all other nodes in a graph.
- **Type of Graph**: Works on graphs with non-negative weights.
- **Complexity**: The time complexity is O(V^2) with a simple implementation, where V is the number of vertices. Using a priority queue, it can be reduced to O(E log V), where E is the number of edges.

## How It Works

1. **Initialization**:
   - Set the distance to the source node to 0 and all other nodes to infinity.
   - Create a priority queue and add the source node.

2. **Processing Nodes**:
   - While the priority queue is not empty:
     - Extract the node with the smallest distance.
     - For each neighbor of this node, calculate the distance from the source node.
     - If this distance is less than the previously recorded distance, update the distance and add the neighbor to the priority queue.

3. **Termination**:
   - The algorithm terminates when all nodes have been processed or the shortest path to the target node has been found.

## Example

Consider the following graph:

```
    (A)
   /   \
  1     4
 /       \
(B)---2---(C)
```

- Starting from node A, the shortest path to B is 1, and to C is 3 (A -> B -> C).

## Implementation

Here is a simple implementation of Dijkstra's algorithm in Python:

```python
import heapq

def dijkstra(graph, start):
    # Initialize distances and priority queue
    distances = {node: float('infinity') for node in graph}
    distances[start] = 0
    priority_queue = [(0, start)]

    while priority_queue:
        current_distance, current_node = heapq.heappop(priority_queue)

        # Nodes can only get added once to the priority queue
        if current_distance > distances[current_node]:
            continue

        for neighbor, weight in graph[current_node].items():
            distance = current_distance + weight

            # Only consider this new path if it's better
            if distance < distances[neighbor]:
                distances[neighbor] = distance
                heapq.heappush(priority_queue, (distance, neighbor))

    return distances

# Example graph
graph = {
    'A': {'B': 1, 'C': 4},
    'B': {'A': 1, 'C': 2},
    'C': {'A': 4, 'B': 2}
}

# Running the algorithm
print(dijkstra(graph, 'A'))
```

## Conclusion

Dijkstra's algorithm is a fundamental algorithm in computer science and is widely used in various applications, including GPS navigation systems, network routing protocols, and more. Understanding its mechanics and implementation is crucial for anyone working with graph data structures.