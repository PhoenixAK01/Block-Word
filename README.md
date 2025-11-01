# Block-Word

Algorithm
State Representation

Each state is represented as a struct State:
vector<pair<char, string>> on → stores which block is on what (other block or table)
vector<string> moves → stores the sequence of moves to reach this state
Goal Test

isGoal(State s, vector<pair<char, string>> goal) checks if all blocks are at their target positions.
Move Generation

getClearBlocks(State s) finds all blocks that have nothing on top of them.
Children(State current) generates all possible next states by:
Moving a clear block to the table
Moving a clear block onto another clear block
Depth-Limited DFS

dfs(State start, vector<pair<char, string>> goal, int depthLimit):
Uses a stack to explore states depth-first.
Checks for the goal state at each step.
Explores all child states if depth limit is not exceeded.
Prints the sequence of moves when the goal is reached.
Time Complexity
Worst-case complexity is O(b^d), where b is the branching factor (number of possible moves) and d is the depth limit.
DFS may not find a solution if the depth limit is too small.
This is an uninformed search (no heuristic).

