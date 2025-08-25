# Ex.No: 1 Implementation of Breadth First Search
### DATE: 12/8/2025 
### REGISTER NUMBER : 212222060277
### AIM:
To write a python program to implement Breadth first Search.
### Algorithm:
7.	Call the bfs function by passing arguments visited, graph and starting node.
8.	Stop the program.
### Program:
# Breadth-First Search in Python
graph = {
'5': ['3', '7'],
'3': ['2', '4'],
'7': ['8'],
'2': [],
'4': ['8'],
'8': []
}
visited = []
queue = []
def bfs(visited, graph, node):
visited.append(node)
queue.append(node)

while queue:
m = queue.pop(0) print(m)
if neighbour not in visited: visited.append(neighbour) queue.append(neighbour)


print("Following is the Breadth-First Search:")
bfs(visited, graph, '5')
### Output:
https://onecompiler.com/python/43urwkjdf

### Result:
Thus the breadth first search order was found sucessfully.

