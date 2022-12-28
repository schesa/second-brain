# java 

Spring MVC
JPA

Early/Static Binding(compile time overloading), Late/Dynamic Binding(run time overriding)
Throwable(Object), Errors(problems), Unchecked Exceptions(RuntimeExceptions), Exceptions
Failfast(no modification) Failsafe(CopyOnWriteArray, ConcurrentMap)
Thread lifecycle(New, Runnable, Running, Waiting, Dead)
composition(part-of) vs aggregation(has-a)
not a complete oop(has primitives)
Memory Model (multithreading - volatile to skip local thread cache)
Memory Management
- JVM memory structure
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
