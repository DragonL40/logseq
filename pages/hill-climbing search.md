- ```python
  def HILL_CLIMBING(problem): returns a state that is a local maximum
  	current = problem.Initial
      while True:
      	neighbor = a highest-valued successor state of current
          if VALUE(neighbor) <= VALUE(current):
          	return current
          current = neighbor
  ```