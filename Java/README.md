### Spring


Spring MVC - manual configuration, more dev time than Spring Boot, only Model View Controller needed to customize

@RequestMapping("api/v2") class annotation?

@GetMapping("/{id}", produces = MediaType.APPLIACTION_JSON) f(@PathVariable id) 

@RequestBody deserializes HttpRequest body to a DTO to be used

@ResponseBody serialize returned DTO to JSON and add it to HttpResponse 



@Controller vs @RestController
- @Controller applied only on classes & mostly used in Spring MVC
- @RestController = @Controller + @ResponseBody
-

JPA


### Java 

Stream types?

Object class methods ?

Early/Static Binding(compile time overloading), Late/Dynamic Binding(run time overriding)

Throwable(Object), Errors(problems), Unchecked Exceptions(RuntimeExceptions), Exceptions
![Exceptions Hierarchy](https://github.com/schesa/interview-prep/blob/main/java-exceptions-hierarchy.png?raw=true)

Failfast(no modification) vs Failsafe(CopyOnWriteArray, ConcurrentMap)

Thread lifecycle(New, Runnable, Running, Waiting, Dead)

Thread can implement Runnable(flexible) or extend Thread

Composition (part-of) vs Aggregation (has-a)

Java is not a complete oop language (has primitives)

Memory Model (multithreading - volatile to skip local thread cache)

Memory Structure
- Method area: Perm,class structures, static fields
- Heap Area: Eden,S0,S1,Old Generation
- Stack Area: Thread memory, heap refferences, LVA,OS,FD
- PC registers: thread dependent
- Native method stack: OS dependent

Double Brace Initialisation - with anonymous class - deprecated
```
    Set<String> countries = new HashSet<String>() {
        {
           add("India");
           add("USSR");
           add("USA");
        }
    };
```

This() and Super() need to be the first statement in a block(they can not coexist)