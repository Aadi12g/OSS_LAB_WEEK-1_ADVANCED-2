# OSS_LAB_WEEK-1_ADVANCED-2
The getMin(int dist[], bool visited[]) function is responsible for identifying the vertex that has the smallest distance value among those that have not yet been visited. It takes two parameters: dist[], which is an array containing the distance from the source vertex to each other vertex, and visited[], a boolean array that tracks whether each vertex has been visited. The function returns the index of the vertex with the minimum distance that hasn't been visited. It initializes the minimum distance (min) to INT_MAX and uses a variable key to store the index of the current vertex. It then iterates over all vertices, updating min and key whenever it finds an unvisited vertex with a smaller distance. Finally, it returns the index of the vertex with the smallest distance.

The display(int dist[], int par[]) function outputs the shortest paths and their corresponding distances from the source vertex to every other vertex. It takes two parameters: dist[], which holds the distances from the source to each vertex, and par[], which stores the parent of each vertex in the shortest path tree. The function doesn’t return anything. For each vertex, it traces the path back to the source using the par[] array and then prints the entire path as well as the distance from the source to that vertex.

The dijkstra(int src) function implements Dijkstra's algorithm to find the shortest paths from a specified source vertex (src) to all other vertices in the graph. It doesn’t return anything. The function initializes arrays par[] (to store parent vertices) and dist[] (to store the distances from the source), as well as a visited[] array to track which vertices have been processed. Initially, all distances are set to INT_MAX, except for the source vertex, which is set to 0, and the parent of the source is set to -1. The algorithm then runs for n-1 iterations, each time selecting the unvisited vertex with the smallest distance and marking it as visited. It updates the distances of adjacent vertices if a shorter path is found. Finally, it calls the display() function to show the shortest paths and their distances.

In the main() function, the program begins by prompting the user to enter the number of vertices. It then asks the user to input the cost matrix that represents the graph and the source vertex. Once this input is received, the dijkstra(src) function is called to calculate and display the shortest paths from the source vertex to all others using Dijkstra's algorithm. The main() function returns 0 upon successful execution.
