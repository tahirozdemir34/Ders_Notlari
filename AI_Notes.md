- [AI_Notes](#ainotes)
	- [What is AI?](#what-is-ai)
	- [What is intelligence?](#what-is-intelligence)
	- [Rationality vs perfection](#rationality-vs-perfection)
	- [Environments](#environments)
	- [Agent Types](#agent-types)
	- [Summary of 2](#summary-of-2)
- [3-Solving Problems By Searching](#3-solving-problems-by-searching)
	- [Problem-solving agents](#problem-solving-agents)
	- [Searching for Solutions:](#searching-for-solutions)
		- [State vs Node](#state-vs-node)
	- [Example: Romania](#example-romania)
	- [Search Strategies](#search-strategies)
	- [Uninformed Search](#uninformed-search)
		- [Breadth-first](#breadth-first)
		- [Uniform-cost Seacrh](#uniform-cost-seacrh)
		- [Depth-first Seacrh](#depth-first-seacrh)
		- [Depth-limited Seacrh](#depth-limited-seacrh)
		- [Iterative Deepening Search](#iterative-deepening-search)
	- [Summary of Algorithms](#summary-of-algorithms)
	- [Graph search](#graph-search)
	- [Summary of 3](#summary-of-3)
- [Informed search (Heuristics) algorithms](#informed-search-heuristics-algorithms)
	- [Best-first search](#best-first-search)
	- [A heuristic funciton](#a-heuristic-funciton)
	- [Romania with step costs](#romania-with-step-costs)
	- [Greedy best-first search](#greedy-best-first-search)
	- [A* search](#a-search)
	- [Admissible heuristic](#admissible-heuristic)
	- [Consistent(tutarlı) heuristic](#consistenttutarl-heuristic)
	- [Iterative deepening A* (IDA)](#iterative-deepening-a-ida)
	- [IDA* vs A*](#ida-vs-a)

<!-- /TOC -->
# AI_Notes

## What is AI?
It is the science and engineering of making intelligent machines, especially intelligent computer programs. It is related to the similar task of using computers to understand human intelligence, but AI does not have to confine itself to methods that are biologically observable.

## What is intelligence?
It is the computational part of the ability to achive goals in the world. Variyng kinds and degrees of int. occur in people, many animals and some machines.

**An agent** is an entity that perceives its env. through sensors and acts through effectors(actuators)

>Human, programs, robots

agent = architecture + program

**A rational agent** is one that acts so as to achieve the best outcome or, when there is uncertainity, the best expected outcome.

**Rational behavior**: doing the right thing

**Right thing**      : maximize goal achievement

Performance measure must be designed according to what one actually wants in the env.

## Rationality vs perfection
- Perfection means all-knowing with infinite knowledge
- Rationality maximizes "expected" performance
- Perfection maximizes "actual" performance

An agent is **autonomous** if its behavior is determined by its own experience (with learn and adapt)

* **P**erformance measure
* **E**nvironment
* **A**ctuators
* **S**ensors

## Environments
- Fully/partially observable

- Deterministic/Stochastic
	- Deterministic: The next state of the env. is determined by the cur. state and action
	- If the env. part. obs. it could be stochastic
	- If the env. is det. except for the act. of other agents, then the env. is "strategic"

- Episodic/Sequential
	- Each episode consist of the agent percieving and performing a single action
	- The choice of action in each episode depends only on the episode itself
	- In seq. env. current decision could affect all future decisions

- Static/Dynamic
	- The env. is unchanged while an agent is deliberating(düşünmek)
	- In the static env. need not keep looking at the world(cuz it does not change)
	- Semidynamic: Env. doesn't change but performance score does
		- Example: Chess when played with clock. Chessboard doesn't change but PM(clock) does.

- Discriete/Continuous
	- A limited number of distinct, clearly defined percepts and actions (EG: Chess)
	- Taxi driving is cont. time and cont. state

- Single/Multiagent
	- Chess is a competitve multiagent env.
	- Handling a box w/ 2 robot is cooperative multiagent problem

The job of AI is to design the agent prog. thet impl. the "agent funciton" mapping pecept sequences to act.
Agent func. (or small equivalence classes) are rational
Aim: find a way to implement the rational agent function
>Example table-driven agent:
	Keeps track of the percept sequence. Uses it to index into a table of actions to decide what to do. (look-up table)

- Drawbacks:
	- Huge table
	- Take a long time to build the table
	- No autonomy
	- Need long time to learn the table entries

## Agent Types
Simple Reflex Agents       |
:-------------------------:|
![Simple Reflex Agents](https://i.hizliresim.com/ROpnAR.jpg "Simple Reflex Agents")  |
|Condition-action (if/then) rule|
|Dont have memory of past world states|
| 	> Example: Vacuum cleaner >> Function([location, status]) return action|



Model-based Reflex Agents       |
:-------------------------:|
![Model-based Reflex Agents](https://i.hizliresim.com/3plE5M.jpg "Model-based Reflex Agents")  |
|The most effective way to handle parital observability. Agent keep track of the part of the world it cant see now.|
|Have internal state used to keep track of past states|
| Example: Car braking: the internal state is not too extensive|
|Changing lanes: the internal state is necessary, to know the agents need to keep track og where other cars are if cant see them at once.|

Goal-based Agents       |
:-------------------------:|
![Goal-based Agents](https://i.hizliresim.com/6yvJBv.jpg "Goal-based Agents")  |
| Choose acts so as to ach. a goal|
|Keep track of the current state is often not enough. Need to add goals to decide which situations are good.|
|Deliberate (ihtiyatlı) instead of reactive.|
| May hove to consider long seq. of pos. acts before deciding if goal is achived|
|Involves consideration of the future "what will happen if I do... ?"|

Utility-based Agents      |
:-------------------------:|
![Utility-based Agents](https://i.hizliresim.com/pGN6Aa.jpg "Utility-based Agents")  |
| Allows decisions comparing choice between conflicting goals, and choice between likelihood of success and importance of goal (if ach. is uncertain)|


Learning Agents      |
:-------------------------:|
![Learning Agents](https://i.hizliresim.com/WGp7z8.jpg "Learning Agents")  |
| Learning Element: Responsible for making improvements. Given an agent design, learning mechanisms can be constructed to improve every part of the agent.|
|  Critic: Tells the learning element how well the agent is doing with respect to a fixed performance standard.|
| Performance Element: Responsible for selecting external actions.|
| Problem Generator: Responsible for suggesting actions that will lead to new and informative experiences|

## Summary of 2
- An agent perc. and acts in an env., has an arc. and is impl. by an agent program.
- An "ideal agent" always chooses the act which max. its expected perf., given percepts seq. received so far
- Autonomous agent uses its own exp. rather than built-in knowledge
- An agent program maps from percepts to actions & updates its internal state
	- Reflex Agent: respond immediately to percepts
	- Goal-based  : act to achive their goal
	- Utility-based: max their own utility func.
- Represending knowledge is important for successful agent design
- **Hardest Env**: Partially obs, stochastic, sequential, dynamic, cont. and mutiagent

# 3-Solving Problems By Searching

## Problem-solving agents
1. Goal formulation
2. Second: Problem formulation (what actions and states to consider)
3. Sarch: (finding seq. of acts. A search alg. takes a prob. as input and ret. sol.)
4. Execution

- Example: Romania
	- Goal: be in Bucharest
	- Problem:
		- states: various cities
		- actions: drive between cities
	- Solution:
		- seq of cities

>Real world problems needs a lot of abstraction

A problem defined with:
- States
- Initial state
- Goal (test)
- Actions or successor func
- Path cost

## Searching for Solutions:
- Root node of the tree is initial state
- Leaves of the tree are states to be expanded
- Search strategy decides to which state should be expand
- At each state, alg. chooses a leaf to expand
- Expanding: Applying the successors function to the selected leaf and generated new states.

### State vs Node
- State: Representation of a physical conf.
- Node: Data str. part of a search tree includes state, parent node, action, path cost, depth
- Number of states != Number of nodes

>Collection of nodes that have been generated but not yet expanded is called ****fringe**
>Each element of the fring is **leaf node**

## Example: Romania
- Problem desc: <{S}, S0, {Sg}, {O}, {g}>
- {S}: cities (ci)
- {S0}: initial city (Arad)
- {SG}: Goal city (Bucharest)
	- G(S) : Is the current state (S) Bucharest?
- {O}: {ci -> cj, for some i and j} (travel between cities)
- gij : Distance? Time?

## Search Strategies
- Picking the order of node expansion
- Evalation (değerlendirme):
	+ Completeness: Does it always find a solution if one exists?
	+ Time Complexity: Number of nodes generated
	+ Space complexity: Maximum number of nodes in memory
	+ Optimality: Does it always find a least-cost solution?

- Time and space complexity are measured in terms of:
	+ b: max branching factor
	+ d: depth of least-cost sol.
	+ m: max. depth of state space (may be infinite)

## Uninformed Search
- Use the inf. available in the problem def.
- Breadth-first search
- Uniform-cost search
- Depth-first search
- Depth-limited search
- Iterative deepening search

### Breadth-first
- Expand shallowest unexpanded node
- Implementation: fringe is a FIFO queue
- Properties
	+ Complete: Yes ( if b *branching factor* is finite)
	+ Time    : 1 + b + b^2 + b^3 + ... + b ( (b^d ) - 1 ) = O(b^(d+1) )
	+ Space   : O(b^(d+1)) *keeps every node in memory*
	+ Space is the bigger problem than time
	+ Optimal : Yes (if cost = 1 per step)

### Uniform-cost Seacrh
- Expand least-cost unexpanded node
- Implementation: fringe = queue ordered by cost
- Equivalent to breadth-first if step costs all equivalence
- Properties:
	+ Complete: Yes ( if step cost >= ε)
	+ Time    : # of nodes with g <= cost of optimal solution, O(b^(ceiling(C */ ε))) where C\* is the cost of the optimal solution
	+ Space   : # of nodes with g ≤ cost of optimal solution, O(b^(ceiling(C*/ ε)))
	+ Optimal : Yes *nodes expanded in increasing order of g(n)*

### Depth-first Seacrh
- Expand deepest unexpanded node
- Implementation: fringe = LIFO queue
- Properties:
	+ Complete: No *fails in infinite-depth spaces, spaces with loops*
		* Modify to avoid repeated states along path.
		* Complete in finite spaces
	+ Time    : O(b^m ) *terrible if m is much larger than d*
		* But if solutions are dense(yoğun), may be much faster than breadth-first
	+ Space   : O(bm) *i.e. linear space*
	+ Optimal : No

### Depth-limited Seacrh
- Depth-first with depth limit

### Iterative Deepening Search
- Number of nodes generated in a depth-limited search to depth d with branching factor b:
	+ N(DLS) = b^0 + b^1 + b^2 + ... + b^d
- Number of nodes generated in an iterative deepening search to depth d with branching factor b:
	+ N(IDS): (d+1) * (b^0 ) + d * (b^1 ) + (d-1) * (b^2 ) + ... + 2 * b^(d-1 ) + b^d
- For b = 10, d =5:
	+ N(DLS) = 1 + 10 + 100 + .... + 100000 = 111111
	+ N(IDS) = 6 + 50 + 400 + .... + 100000 = 123456
	+ Overhead = (123456 - 111111) / 111111 = %11
- Properties:
	+ Complete: Yes
	+ Time: (d+1) * (b^0 ) + d * (b^2 ) + ... + 2 * b^(d-1) + b^d = O(b^d )
	+ Space: O(b^d)
	+ Optimal: Yes *if step cost = 1*

## Summary of Algorithms
- **Breadth-first search**: The space complexity makes it impractical in
most cases.
- **Uniform-cost search** is similar to Breadth-first search (expand with
lowest cost g(n)).
- **Depth limited search** imposes a fixed depth limit on a depth-first
Search.
- **Iterative deepening search** uses only linear space and not much more
time than other uninformed algorithms

>**Repeated states**: Failure to detect repeated states can turn a linear problem into an exponential one.

## Graph search
- Closed list: stores every expanded node
- Open list: fringe of unexpanded nodes

## Summary of 3
- Problem formulation usually requires abstracting away real-world details
to define a state space that can feasibly be explored.
- A problem consist of four parts: the initial state, a set of actions, a goal
test function, and a path cost function. The environment of the problem
is represented by a state space.
- TREE-SEARCH algortihm can be used to to solve any problem.
- Search algorithms are judged on the basis of completeness, optimality,
time complexity, and space complexity.
- When the state space is a graph rather than a tree, the GRAPH-SEARCH
algortihm eliminates all duplicate states.

# Informed search (Heuristics) algorithms
- Best-first search
	+ Greedy best-first search
	+ A* search
- Local search alg.
	+ Hill-climbing search
	+ Simulated annealing search
	+ Local beam search
	+ Genetic algorithms
- Basic Optimization Problem and Solution
	+ Linear programming

- Blind search - BFS, DFS, uniform cost
	+ no notion concept of the "right direction"
	+ can only recognize goal once it's achieved
	+ A search strategy is defined by picking the **order of node expansion**
- Heuristics search
	+ We have rough idea of how good various states are, and use this knowledge to guide our search

## Best-first search
- General approach of informed search:
	+ Node is selected for expansion based on an **evaluation funciton f(n)**
- Idea: evaluation funciton measures distance to the goal
	+ Choose node which appears best
- Implementation: fringe is queue sorted in decreasing order of desirability
	+ Special cases: greedy search, A* search

## A heuristic funciton
>“A rule of thumb, simplification, or educated guess that reduces or limits the search for solutions in domains that are difficult and poorly understood.”

- h(n) : estimate cost of the cheapest path from node n to goal node.
- If n is goal then h(n) = 0
- Aim is the minimising the total cost from start to goal

f(n) = g(n) + h(n)
f(n): estimate of total cost along path through n
g(n): actual cost to reach n

## Romania with step costs
h(SLD) = straight-line distance heuristic

h(SLD) can **NOT** be computes from the problem itself.

In this example *f(n)=g(n)*
	Expand node that is closest to goal
	Greedy best-first search

## Greedy best-first search
- Evalation function *f(n) = h(n)* (h)euristic
- estimate of cost from n to goal
- e.g. h(SLD) = straight-line distance from n to Bucharest
- Greedy best-first search expands the node that **appears** to be closest to goal
- Properties:
	+ Complete: No *can get stuck in loops*
	+ Time: O(b^m ) *but good heuristic can give dramaric improvement*
	+ Space: O(b^m ) *keeps all nodes in memory*
	+ Optimal: No

## A* search
- Idea: Avoid expanding paths that are already expensive(? bence expanded yazacaktı)
- Evalation function *f(n) = g(n) + h(n)*
- g(n) : cost so far to reach n
- h(n) : estimate cost from n to goal
- f(n) :estimate total cost of path through n to goal
- OPEN LIST, CLOSED LIST (?)
- Properties:
	+ Complete : Yes *unless there are infinitely many nodes with f<=f(G)*
	+ Time: O(n^2 )
	+ Space : Keep all nodes in memory
	+ Optimal: Yes

## Admissible heuristic
- A heuristic h(n) is **admissible** if for every node n, h(n) <= h*(n) where h\*(n) is the true cost to reach the goal state from n
- An admissible heuristic **never overestimates** the cost to reach the goal. It is optimistic
- Example: h(SLD) never overestimates the actual road distance
- **Theorem**: If h(n) is admissible, A* using TREE-SEARCH is optimal.
- For proof check 4_5_HeuristicSearch.pdf page 8

## Consistent(tutarlı) heuristic
- A heuristic is **consistent** if for every node n, every successor n' of n generated by and action a,
	+ h(n) <= c(n,a,n') + h(n')
- if h is consistent we have:
	+ f(n') = g(n') + h(n')
	+ = g(n) + c(n,a,n') + h(n')
	+ => g(n) + h(n)
	+ = f(n)
	+ *f(n)* is non-decreasing along any path
	+ **Theorem**: If h(n) is consistent, A* using GRAPH-SEARCH is optimal

## Iterative deepening A* (IDA)
- Always finds an optimal solution
- Uses sapce linear in solution depth
- Is asymptotically no slower than A*
- Assuming a tree structure space, so we don't have t check for cycles
- Or at least, that cycles are few and long
- So, IDA* is about as good as we can do, given an (admissible) heuristic func.

## IDA* vs A*
- In practice using a heuristic like the manhattan distancec, A* can't solve the 15 puzzle because machine run out of memory
- IDA* generate more nodes than A*, but it often runs faster
	+ e.g. IDA* finds 12 step solution to 8-puzzle problem very quickly expanding 39 nodes
- In the end it depends on theproblem:
	+ for an n-puzzzle IDA* works well, but for a path finding IDA* expands square of the numbers of nodes A* expands
