- The idea behind selection sort is to have a sorted part of the list and an unsorted part of the list. Each pass through we'll find the minimum of the unsorted part and add it to our sorted list.
- ---
- ## Steps
	- Pick current index ($i = 0$)
	- Find minimum in the rest of the list
	- Swap to put minimum in correct position
	- Repeat with ($i += 1$)
- ## Pseudocode
	- ```
	  for curIndex = 0 until 2nd to last element 
	      minIndex = find the minimum in the rest of the list
	      swap at curIndex and minIndex
	      // now everything up to curIndex is sorted
	  ```