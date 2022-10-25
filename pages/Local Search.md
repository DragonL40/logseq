- #[[optimization algorithms]]
- Local search algorithms operate by searching from a start state to neighboring states, without keeping track of the paths, nor the set of states that have been reached.
	- Not systematic — might never explore a portion of the search space where a solution actually resides.
	- Use very little memory.
	- Often find reasonable solutions in large or infinite state spaces for which systematic algorithms are unsuitable.
- [[hill-climbing search]]
	- ```c
	  function HILL-CLIMBING(problem) returns a state that is a local maximum
	  	current <- problem.Initial
	      while true do
	      	neighbor <- a highest-valued successor state of current
	          if VALUE(neighbor) <= VALUE(current)
	          	then return current
	          current <- neighbor
	  ```