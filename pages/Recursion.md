* Recursive Analysis Tip: Box Diagrams
** To analyze recursive functions, draw a box diagram which is *a simplified view of each function instance on the stack*
** For each function instance, draw one box showing arguments, pertinent local variables, and return values.
*
```cpp 
:PROPERTIES:
:END:
int fact(int n) {
	if(n == 1){
    	return 1;
    } else {
    	return n * fact(n - 1);
    }
```
* [[/Users/helen/Documents/notes/assets/image_1621452709498_0.png]]
