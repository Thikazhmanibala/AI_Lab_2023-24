# Ex.No: 3:Minimax Search
### DATE: 26/8/2025 
### REGISTER NUMBER : 212222060277
4	### AIM:
5	To write a python program to implement Minimax Search.
6	 	### Algorithm:
7	1. Start the program
8	2. Create the graph by using adjacency list representation
9	3. Define a function dfs and take the set “visited” is empty
10	4. Search start with initial node. Check the node is not visited then print the node.
11	5. For each neighbor node, recursively invoke the minimax search.
12	6. Call the function by passing arguments visited, graph and starting node.
13	7. Stop the program.
14	 	### Program:
15	# Simple Minimax Algorithm Implementation

def minimax(depth, node_index, is_maximizing, scores, max_depth):
    # If we reach the leaf node, return its value
    if depth == max_depth:
        return scores[node_index]

    if is_maximizing:
        best = float("-inf")

        # Explore left and right child
        best = max(best, minimax(depth + 1, node_index * 2, False, scores, max_depth))
        best = max(best, minimax(depth + 1, node_index * 2 + 1, False, scores, max_depth))

        return best
    else:
        best = float("inf")

        # Explore left and right child
        best = min(best, minimax(depth + 1, node_index * 2, True, scores, max_depth))
        best = min(best, minimax(depth + 1, node_index * 2 + 1, True, scores, max_depth))

        return best


# Example game tree with leaf values
scores = [3, 5, 2, 9]  # Values at leaf nodes
max_depth = 2          # Since tree height = log2(len(scores))

print("The optimal value is:", minimax(0, 0, True, scores, max_depth))



### Output:
https://onecompiler.com/python/43uteze2p

### Result:
Thus the depth first search order was found sucessfully.

