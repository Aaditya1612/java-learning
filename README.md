## Java Interview Questions

1. **What is copy constructor in Java?**
**Ans:** A **copy constructor** in programming, particularly in object-oriented languages like C++, is a special constructor used to create a new object as a copy of an existing object. A copy constructor is a constructor which initializes an object using another object of the same class.
In Java, there is no concept of default copy constructor like in C++. But we can give manual implementation of copy constructor in Java.
(*ref*: )

2. **What is the concept of Shallow Copy?**
**Ans:** Using shallow copy, we can copy the contents of the variables of one object into the another object. This works well when there is no variable (Data member) allocated on the heap. But when there is a data member allocated on the heap then in case of shallow copy, the copied object variable will also reference to the same memory location.
This can cause ambiguity, changing in one object will change other's variable as well and there can be some serious issues of dangling pointer.

![](https://media.geeksforgeeks.org/wp-content/uploads/20201216032815/ShallowCopyHeapMemory.png)

So this was somewhat in terms of c++. In java also the concept is quite same. If the object contains **primitive as well as non primitive or reference type variable in shallow copy,** the cloned object also refers to the same object to which the original object refers as only the object references gets copied and not the referred objects themselves.

3. **What is Deep Copy?**
Ans: Whenever we need own copy not to use default implementation we call it as deep copy.
Obviously, for a object with only primitive data types will have no difference of use of shallow and deep copy.

4. **What is Lazy Copy?**
Ans: A lazy copy can be defined as a combination of both shallow copy and deep copy. The mechanism follows a simple approach – at the initial state, shallow copy approach is used. A counter is also used to keep a track on how many objects share the data. When the program wants to modify the original object, it checks whether the object is shared or not. If the object is shared, then the deep copy mechanism is initiated.

5. **What is Java Heap?**
Ans. In Java, a heap is a chunk of memory which is shared among all threads. In a heap, all class instances and the array is allocated. It is created when JVM starts-up. An automatic storage management system reclaims heap.
