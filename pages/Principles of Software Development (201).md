- What is unique about a [[Object-Oriented System]]?
- What makes up an [[Object]]?
- [[The Open-Closed Principle]]
	- Software modules should be open for **extension** and closed for **modification**.
- The downfall of getter/setter
- When are getter/setter acceptable?
  ---
- Three ways to design classes:
	- [[Composition]]
	- [[Inheritance]]
	- [[Interfaces]]
## Garbage Collection in Java
- What are the advantages of automatic garbage collection?
- What is global synchronization with the OS?
- What are the four ways to make an object eligible for garbage collection?
	- Nullifying the reference variable
		-
		  ```cpp
		  Test t = new Test("t");
		  t = null;
		  ```
	- Re-assigning the reference variable
	- Object created inside method
	- Island of Isolation
- What is the [[Mark and Sweep Algorithm]]?
- How to manually invoke the garbage collector in Java?
## [[Generics]]
- What is [[Generic Programming]]?
- Why use [[Generics]]?
- How to write [[Generic Methods]]?
- What are upper bounded wildcards?
  collapsed:: true
	- The question mark (`?`), represents the wildcard, stands for unknown type in generics.
	-
	  ```java
	  public static void printList(List<? extends Number> lst) {
	    for (Number item : lst) System.out.printf("%s", item);
	  }
	  ```
- When to use upper bounded wildcards?
- What are Unbounded Wildcards?
  collapsed:: true
	-
	  ```java
	  Collection<?> col = new ArrayList<String>();
	  ```
## Arrays
- `==` only compares memory locations of objects, so we should use the function `Arrays.equals()` to compare Arrays.
- What is deep copy?
- How to compare Arrays?
- How to perform deep copy on an 1D Array?
- What happens when you call `clone()` on a 2D array?
- How to design the data structure such that we do not need to make a deep copy?
## Iterators
- What is `Iterator` and `Iterable`?
	- `Iterator` is the actual object that will iterate through a collection
	- `Iterable` is an interface which provides Iterator.
- When can you use the `foreach loop`?
	- When the class implements the interface Iterator?
- What is a `Comparable`?
	-
	  ```java
	  public interface Comparable<AnyType> {
	    public int compareTo(AnyType obj);
	  }
	  ```
- What is the `Comparator` interface?
	-
	  ```java
	  public interface Comparator<AnyType> {
	    public boolean(T obj1, T obj2);
	  }
	  ```
## Exceptions
-