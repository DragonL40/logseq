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
- What the memory locations are candidates for garbage collection?
  ```java
  ```
- What are the (2) advantages of automatic garbage collection?
	- Object creation is faster because global synchronization with the OS is not needed
	- The garbage collector reclaims the underlying memory and reuses it for future object
- What are the four ways to make an object eligible for garbage collection?
  collapsed:: true
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
- How to define generic classes? 
  collapsed:: true
	- ![image.png](../assets/image_1630637212678_0.png){:height 272, :width 421}
- ((61318cea-57b6-4775-8cb8-08bd4b29c202))
- What is a generic type?
	- generic type (`List<AnyType>`) is a type with formal type parameters.
- What is a parameterized type?
	- The instantiation of a generic type with actual type arguments (such as, `List<String>`).
- How to write [[Generic Methods]]?
	- All generic method declarations have a type parameter section delimited by angle brackets that precedes the method's return type. You cannot compile if there is no `<T>`.
	-
	  ```java
	  public static <T> void printArray(T[] array) {
	    for (T item : array) System.out.printf("%s", item);
	  }
	  ```
- How to bound the type parameters?
  collapsed:: true
	-
	  ``` java
	  public static <T extends Number> void printArray(T[] array) {
	    for (T item : array) System.out.printf("%s", item);
	  }
	  ```
	- This is an upper bound type, accept instances of `Number` or its subclasses (the class that inherits from Number class).
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
  collapsed:: true
	- If you want the generic expression to accept all subclasses of a particular type, you will use upper bound wildcard.
	- Use an upper-bounded wildcard only when values are to be retrieved and processed, but the data structure won't be changed.
	- The following code **does not compile**:
	  ```java
	  public static void demoList(List <? extends Number> lst) {
	    lst.add(new Integer(5));
	  }
	  ```
- What are unbounded wildcards?
  collapsed:: true
	-
	  ```java
	  Collection<?> col = new ArrayList<String>();
	  ```
- What are lower bounded wildcards?
	-
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
- What are exceptions in Java?
- What options do you have after an exception is thrown? #numlist
	- do not handle it at all
	- handle it where it occurs
	- handle it later in the program
- What is the difference between **checked** and **unchecked** exceptions?
- How to define your own **checked** exception?
	- extend from `Exception` class
- How to define your own **unchecked** exception?
	- extend from `RuntimeException` class
- What is the point of the `throws` keyword?
## Java Files I/O
- What is `try-with-resources`?
	- The try-with-resources does automatic resource management. It ensures that each resource is closed at the end of the statement.
	- Resources that are to be automatically closed must be created inside the parentheses of the `try` block.
- How to read/write binary files?
	- Use `InputStream` and `OutputStream`
- What is `InputStreamReader`?
-
## Java Collections Framework
- [[HashSet]]
	- [[Hash Table]] in Java
- What is a `LinkedHashSet`?
  collapsed:: true
	- [[HashSet]] that keeps the inserted order
- What is a `TreeSet`?
  collapsed:: true
	- [[HashSet]] that keeps the sorted order
- [[HashMap]] in Java
## Functional Programming in Java
- What is [[lambda expression]]?
	- A lambda expression describes  an anonymous function and is represented by the following syntax:
	-
	  ```java
	  list of parameters -> expression body
	  ```
## Bounded Types
- ![lecture6.pdf](../assets/lecture6_1631930377622_0.pdf)
- Terminology
	- ((6145483c-b360-4e7a-88c6-c40158a2179d))
- Generics with Upper Bounds
	- Upper bound is a boundary that includes the specified class or any which it extends.
		-
		  ```java
		  <T extends superClass>
		  ```
	- Java Generics supports multiple bounds
		-
		  ```java
		  <T extends superClassName & Interface>
		  ```
- Generics with Lower Bounds
	- Lower bound is a boundary that includes the specified class or any super class to it.
		-
		  ```java
		  <T super childClass>
		  ```
	- Mostly we use lower bounds with a wildcard: `List<? super Integer>`
		- This method will work for `List<Integer>`, `List<Number>`, `List<Object>`
- When to use bounded wildcards?
	- Use `<? extends>` when you only GET objects.
	- Use `<? super>` when you PUT values into a structure.
	-
	  ```java
	  public static <T> void copy (List <? extends T> src, List<? super T> dest) {
	    for (int i = 0; i < src.size(); i++) {
	      dest.set(k, src.get(k));
	    }
	  }
	  ```
## Type Erasure
- Compiler applies a process called [[Type Erasure]] on generics at compile time
-
# [[Threading]]
## Monitors, Locks, Conditions ![lecture9.pdf](../assets/lecture9_1632884282923_0.pdf)
- What is `monitor`?
	- A `monitor` is an object with mutual exclusion and synchronization capabilities. Any object can be a monitor. An object becomes a monitor once a thread locks it.
	- Locking is implemented using the `synchronized` keyword on a method or a block.
	- _The monitor functionality is implemented in the `Object` class_
- A thread can `wait()` in a monitor; **this will release the lock on the object**.
	- This thread must then be awakened using `notify()` or `notifyAll()` from another thread to be moved back into the **Ready** state.
-
  > The `wait()`, `notify()`, and `notifyAll()` methods must be called in a synchronized method or a synchronized block.
- Synchronization Using Locks
	- You can acquire locks explicitly.
	- A lock is an instance of the Lock interface.
	- A lock may also use the `newCondition()` method to create any number of `Condition` objects.
	- **Locks and conditions** are more powerful and flexible than the built-in monitor, so will not need to use monitors.
-