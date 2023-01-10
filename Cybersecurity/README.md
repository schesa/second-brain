# Spring

JPA - @Entity, @OneToMany implemented with Hibernate, uses inside JDBC to send queries

Spring Security

SpEL expression language for query and manipulation

@Required - if required field is not wired, container throws BeanInitializationException

@Qualifier("bean name") - select which bean should be @Autowired

Bean Scopes: 
-Singleton(single instance in Spring IoC)
-Prototype(many instances)
-Request(Http-Request)
-Session(Http-session)
-Global-session(Global Http-session)

IOC types: ApplicationContext, BeanFactory

ApplicationContext(eager initialization, manages resources on its own) vs BeanFactory(doesn't support annotations)

@Bean - method level annotation

@Configuration - make @Bean methods singletons

Dependency Injection can be done via: Constructor, Setter, Interface(not supported by Spring)

@Autowired can be user for: Field, Constructor(preffered), Setter(overrides Contructor)

@Component - only Component is scanned. The other's interfaces are annotated with Component 

@Repository - catch persistence exceptions and rethrow them as Spring unchecked exceptions

@Service - indicates thet it's holding business logic

@Controller - necessary for @RequestMapping

<details>
  <summary>Spring MVC - manual configuration, more dev time than Spring Boot, only Model View Controller needed to customize</summary>
  
![Spring MVC model](https://raw.githubusercontent.com/schesa/interview-prep/main/Java/java-mvc-model.png)
  
</details>

@RequestMapping("api/v2") - maps url to class/method

@GetMapping("/{id}", produces = MediaType.APPLIACTION_JSON) f(@PathVariable id) 

@RequestBody deserializes HttpRequest body to a DTO to be used

@ResponseBody serialize returned DTO to JSON and return it to HttpResponse 



@Controller vs @RestController
- @Controller applied only on classes & mostly used in Spring MVC
- @RestController = @Controller + @ResponseBody

# Java 

Stream types: terminal(reduce) and intermidate(map)

Functional interface: lambda, predicates

Method reference String::toUpperCase()

Testing mockito(doreturn().when()), mockmvc.perform(api)

Object class methods - toString,hashcode,equals,finalize(gc),notify,notifyAll,wait

Early/Static Binding(compile time overloading), Late/Dynamic Binding(run time overriding)

<details>
  <summary>Throwable(Object), Errors(problems), Unchecked Exceptions(RuntimeExceptions), Checked Exceptions(catch the rest)</summary>
  
![Exceptions Hierarchy](https://raw.githubusercontent.com/schesa/interview-prep/main/Java/java-exceptions-hierarchy.png)
  
</details>

Failfast(no modification allowed during iteration) vs Failsafe(CopyOnWriteArray, ConcurrentMap)

<details>
  <summary>Thread lifecycle(New, Runnable, Running, Waiting, Dead)</summary>
  
![Thread Lifecycle](https://raw.githubusercontent.com/schesa/interview-prep/main/Java/Java-Thread-Lifecycle.png)
  
</details>

Thread can implement Runnable(flexible) or extend Thread

Composition (part-of) vs Aggregation (has-a)

Java is not a complete oop language (has primitives)

Memory Model (multithreading - volatile to skip local thread cache)

<details>
  <summary>Memory Structure</summary>
  
- Method area: Perm,class structures, static fields
- Heap Area: Eden,S0,S1,Old Generation
- Stack Area: Thread memory, heap refferences, LVA,OS,FD
- PC registers: thread dependent
- Native method stack: OS dependent
  
![Memory Model](https://raw.githubusercontent.com/schesa/interview-prep/main/Java/Java-Memory-Model.png)
  
</details>

<details>
  <summary>Double Brace Initialisation - with anonymous class - deprecated</summary>
  
```
    Set<String> countries = new HashSet<String>() {
        {
           add("India");
           add("USSR");
           add("USA");
        }
    };
```
  
</details>

This() and Super() need to be the first statement in a block(they can not coexist)
