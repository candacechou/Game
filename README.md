# Game
This is the second assignment of the course DD2380 Artificial Intelligence in KTH Royal Institute of Technology in Stockholm.
In this assignment, MinMax algorithm and Alpha-Beta Pruning Algorithm are implemented in two different game : Tik-Tac-Toc and Checker.

## MinMax Algorithm

Assuming that the opponent is also aware that it has to optimize it’s chances of winning, and therefore when calculating a heuristic function that requires traversing the tree, we should only consider the transitions that maximize the heuristic function for player B (therefore minimizing the heuristic for player A).

## Alpha-Beta Pruning

Consider that player A is traversing the tree in order to find the next best move using the minimax algorithm. 
Instead of just keeping track of the best node found so far, the player can also keep track of the best heuristic value computed so far, $\alpha$ as well as the worst such value $\beta$ (which yields the best result for B). At each transition in the tree $\alpha$ should be updated, if it is player A’s turn, and otherwise $\beta$ should be updated. Finally, the remainder of a branch should be disregarded whenever $\alpha$ is greater then $\beta$ since that indicates the presence of a non-desirable state.
