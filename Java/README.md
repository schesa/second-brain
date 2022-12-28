## Java 

Spring MVC
JPA

Early/Static Binding(compile time overloading), Late/Dynamic Binding(run time overriding)

Throwable(Object), Errors(problems), Unchecked Exceptions(RuntimeExceptions), Exceptions

Failfast(no modification) vs Failsafe(CopyOnWriteArray, ConcurrentMap)

Thread lifecycle(New, Runnable, Running, Waiting, Dead)

Composition (part-of) vs Aggregation (has-a)

Java is not a complete oop language (has primitives)

Memory Model (multithreading - volatile to skip local thread cache)

Memory Management

Memory Structure
- Method area: Perm,class structures, static fields
- Heap Area: Eden,S0,S1,Old Generation
- Stack Area: Thread memory, heap refferences, LVA,OS,FD
- PC registers: thread dependent
- Native method stack: OS dependent

Double Brace Initialisation - with anonymous class
```
    Set<String> countries = new HashSet<String>() {
        {
           add("India");
           add("USSR");
           add("USA");
        }
    };
```
