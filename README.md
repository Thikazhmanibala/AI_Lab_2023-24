# Ex.No: 1 Implementation of depth First Search
### DATE: 12/8/2025 
### REGISTER NUMBER : 212222060277
4	### AIM:
5	To write a python program to implement Depth first Search.
6	 	### Algorithm:
7	1. Start the program
8	2. Create the graph by using adjacency list representation
9	3. Define a function dfs and take the set “visited” is empty
10	4. Search start with initial node. Check the node is not visited then print the node.
11	5. For each neighbor node, recursively invoke the dfs search.
12	6. Call the dfs function by passing arguments visited, graph and starting node.
13	7. Stop the program.
14	 	### Program:
15	graph = {
16	'5': ['3', '7'],
17	'3': ['2', '4'],
18	'7': ['8'],
19	'2': [],
20	'4': ['8'],
21	'8': []
22	}
23
24	# Set to keep track of visited nodes
25	visited = set() 26
27	 	# DFS function
28	def dfs(visited, graph, node):
29	if node not in visited:
30	print(node)
31	visited.add(node)
32	for neighbour in graph[node]:
# Driver code
print("Following is the Depth-First Search:") dfs(visited, graph, '5')

### Output:
https://onecompiler.com/python/43urwkjdf

### Result:
Thus the depth first search order was found sucessfully.

