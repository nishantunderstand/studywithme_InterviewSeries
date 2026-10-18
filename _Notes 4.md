Note: Java does not provide a standard `AtomicFloat` class. For floating-point values, alternatives include `AtomicReference<Float>` or `DoubleAdder` for appropriate use cases.

- What are the other things does it support ?

---

8. What is distributionManagement in pom.xml? 🤔
Does it mean nexus Repo ?


9. Java 17 Features
- Records — concise data carrier classes.
- Sealed classes — restrict permitted subclasses.
- Pattern matching for instanceof — simplifies type checks.
- Text blocks — multiline strings.
- Switch expressions — return values from switch.
- Helpful NullPointerExceptions — clearer NPE messages.
- Strong encapsulation of JDK internals — improved platform integrity.

Can `var` be used as a generic type? No.


- Return only required fields using DTOs or projections.

2. DSA: Print yes if 5 consecutive vowels exist; otherwise no

```
Function<String, Integer> f = s -> s.length();
System.out.println(f.apply("Java")); // 4

Supplier<Double> s = () -> Math.random();
System.out.println(s.get());
```


## 9. Print `NA` if employee address is null
```
employees.stream()
    .forEach(e -> System.out.println(
        e.getName() + " : " +
        Objects.toString(e.getAddress(), "NA")
    ));
```


### What are TDD and BDD?

- TDD (Test-Driven Development): Write a failing test, implement the code, then refactor — red, green, refactor.
- BDD (Behavior-Driven Development): Define and test expected behavior using scenarios, often written as Given–When–Then.

### 15. Can HashMap keys be mutable?


### 17. Run code before a Spring bean is used


### 9. What happens when an exception occurs during a transaction?

“By default, Spring rolls back for unchecked exceptions and `Error`, but not checked exceptions. We can customize this using `rollbackFor`.”