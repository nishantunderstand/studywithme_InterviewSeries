List of person

person 
name 
hobbies , name , categoies

class Person{
	private String name;
	List<Hobbies> hobbies;
}


class Hobbies{
	private string name;
	private String categories;
}



---

Group Hobbies by Cateogires

Map<String, Long> temp = 
hobbies.stream()
	.collect(Collectors.groupingBy(
	Hobbies::getCategories,
	Collectors.counting()
))

person.stream().flatMap( n-> n.temp)



----


class Person {
    private String name;
    private List<Hobby> hobbies;
}

class Hobby {
    private String name;
    private String category;
}


Map<String, Long> result = persons.stream()
        .flatMap(person -> person.getHobbies().stream())
        .collect(Collectors.groupingBy(
                Hobby::getCategory,
                Collectors.counting()
        ));
				
				
				
				
Interview EY Client Interview Fidelity  Face 2 Face 20261001

1. FlatMap + Group Custom Question 
2. Equals and Hashcode
3. leetcode 121 Buy and Sell Stock

Explain the project 
Spring Security Filter Architecture
Spring MVC Architecture 

Total Time : 23 min 


Map<String, List<Employee>> result =
    departments.stream()
        .flatMap(dept -> dept.getEmployees().stream())
        .collect(Collectors.groupingBy(Employee::getDepartment));

https://leetcode.com/problems/best-time-to-buy-and-sell-stock/



				