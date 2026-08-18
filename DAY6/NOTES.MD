Depth first search - In the previous description of the frontier, one thing went unmentioned. At stage 2 in the pseudocode above, which node should be removed? This choice has implications on the quality of the solution and how fast it is achieved. There are multiple ways to go about the question of which nodes should be considered first, two of which can be represented by the data structures of stack (in depth-first search) and queue (in breadth-first search; and here is a cute cartoon demonstration of the difference between the two).
We start with the depth-first search (DFS) approach.

A depth-first search algorithm exhausts each one direction before trying another direction. In these cases, the frontier is managed as a stack data structure. The catchphrase you need to remember here is “last-in first-out.” After nodes are being added to the frontier, the first node to remove and consider is the last one to be added. This results in a search algorithm that goes as deep as possible in the first direction that gets in its way while leaving all other directions for later.

(An example from outside lecture: Take a situation where you are looking for your keys. In a depth-first search approach, if you choose to start with searching in your pants, you’d first go through every single pocket, emptying each pocket and going through the contents carefully. You will stop searching in your pants and start searching elsewhere only once you will have completely exhausted the search in every single pocket of your pants.)
pros- at best, this algorithm is the fastest.
Breadth first search - the opposite of depth 
The opposite of depth-first search would be breadth-first search (BFS).

A breadth-first search algorithm will follow multiple directions at the same time, taking one step in each possible direction before taking the second step in each direction. In this case, the frontier is managed as a queue data structure. The catchphrase you need to remember here is “first-in first-out.” In this case, all the new nodes add up in line, and nodes are being considered based on which one was added first (first come first served!). This results in a search algorithm that takes one step in each possible direction before taking a second step in any one direction.

(An example from outside lecture: suppose you are in a situation where you are looking for your keys. In this case, if you start with your pants, you will look in your right pocket. After this, instead of looking at your left pocket, you will take a look in one drawer. Then on the table. And so on, in
pros-this algorithm is guraunteed to find the optimal solution 
cons-This algorithm is almost guaranteed to take longer than the minimal time to run.
At worst, this algorithm takes the longest possible time to run.
Greedy Best first search - are both uniformed search algorithms.That is algorithms do not utilize any knowledge about the problem that they did did not acquire through their own exploration.However is thr case that the case that knowledge about the problem is .in fact
Greedy best-first search expands the node that is the closest to the goal, as determined by a heuristic function h(n). As its name suggests, the function estimates how close to the goal the next node is, but it can be mistaken. The efficiency of the greedy best-first algorithm depends on how good the heuristic function is. For example, in a maze, an algorithm can use a heuristic function that relies on the Manhattan distance between the possible nodes and the end of the maze. The Manhattan distance ignores walls and counts how many steps up, down, or to the sides it would take to get from one location to the goal location. This is an easy estimation that can be derived based on the (x, y) coordinates of the current location and the goal location.
manhattan distance - However, it is important to emphasize that, as with any heuristic, it can go wrong and lead the algorithm down a slower path than it would have gone otherwise. It is possible that an uninformed search algorithm will provide a better solution faster, but it is less likely to do so than an


