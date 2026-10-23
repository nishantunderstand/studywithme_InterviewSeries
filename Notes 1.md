- Can a record extend another class?
- Does a record compare objects using `==`?
- Are records suitable for DTOs?
- Can we override `equals()` and `hashCode()`?

---

| Feature                      | Inheritance                   | Composition                                       |
| ---------------------------- | ----------------------------- | ------------------------------------------------- |
| Relationship                 | IS-A                          | HAS-A                                             |
| Java mechanism               | `extends`                     | Object field/reference                            |
| Code reuse                   | Inherits accessible behavior  | Delegates to another object                       |
| Coupling                     | Often tighter                 | Often more flexible                               |
| Runtime flexibility          | Limited by class hierarchy    | Dependencies can often be replaced                |
| Multiple reuse relationships | Single class inheritance      | Can combine multiple objects                      |
| Best suited for              | Genuine subtype relationships | Building functionality from collaborating objects |

Multiple Catch + Pipe Operator 

```
Map<String, Integer> map = new HashMap<>();

map.put(null, 100);
map.put(null, 200);

System.out.println(map.size()); // 1
System.out.println(map.get(null)); // 200
```

Chaining and Duplicate Key 


8. What is Prototype Scope?
    * How is it different from Singleton?
    * When would you use prototype-scoped beans?
9. ApplicationContext vs BeanFactory
    * What is ApplicationContext?
    * What is BeanFactory?
    * What are their differences and use cases?