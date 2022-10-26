# java8-functional-interface

1. A functional interface in Java 8 is an interface that can only have one abstract method. 
2. Functional interfaces are also referred to as SAM interfaces, or, Single Abstract Method interfaces. However, they can contain any number of default or static methods.
3. @FunctionalInterface annotation is optional and can be used to prevent functional interfaces from having more than one abstract method.
4. Java 8 introduced four types of functional interfaces:<br />
a. Consumer: Accepts an argument, returns nothing.<br />
b. Function: Accepts an argument, returns a value.<br />
c. Predicate: Accepts an argument, returns a boolean value.<br />
d. Supplier: Does not accept an argument, returns a value.
5. FunctionalInterface from old API<br />
a. Runnable, <br />
b. Callable, <br />
c. Comparator,<br />
d. Comparable<br />
6. Purpose of funcational interface?<br />
a. backward compatible for older interfaces so adding a new default method to interface won't screw it's too many implementing classes<br />
b. it provides target types for lambda expressions and method references.<br />
c. to exhibit singular functionality. The lambda expressions are used primarily to define the inline implementation of a functional interface. It eliminates the need for an anonymous class and gives a simple and powerful functional programming capability to Java.
7. A functional interface can extends another interface only when it does not have any abstract method.
8. Diamond class problem in funcational interface
You can have same default methods (same name and signature) in two different interfaces and, from a class you can implement these two interfaces. If you do so, you must override the default method from the class explicitly specifying the default method along with its interface name
