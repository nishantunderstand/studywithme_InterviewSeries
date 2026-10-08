ControllerLayer 
->
Service Layer
->
Reposistory Layer

DB : PostgreSQL

JWT : Authentication and Authorization
RBAC (VA , VAManger, ADMIN)


Lombok


---

Demonstrate the use of intermediate and terminal functions of streams API to filter the employee details from the list containing employee objects. Assume the below class –
 
Class Employee { 
	int  empId; 
	String empName; 
	int empSalary; 
	String empDept;    
	} 
        Employee emp1 = new Employee(101, “Alok”, 5000, "IT");  
        Employee emp2 = new Employee(102, “Amit”, 7000,"IT"); 
        Employee emp3 = new Employee(103, “Nitin”, 8000,"Finance"); 
        List<Employee> myList = new ArrayList<Employee>(); 
        myList.add(emp1); 
        myList.add(emp2); 
        myList.add(emp3);
 
1.Fetch the employee object with highest salary using streams API. 
2.Print count of employee department wise like Finance =1, IT =2. 
3.Print the employee data where employee name starts with ‘A’.



---

Given a List of Integers find total count, min, max, sum, and the average for numbers by using Stream api
input  :list=[2, 3, 5, 7, 11, 13, 17, 19, 23, 29]

List<Integer> myList = Arrays.asList(2, 3, 5, 7, 11, 13, 17, 19, 23, 29);


---

count
min
max
sum
average

---

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.*;
import java.util.stream.*;
import java.util.function.*;

// Issue in Import 
class Main {
    public static void main(String[] args) {
        System.out.println("Start small. Ship something.");
        List<Integer> myList = Arrays.asList(2, 3, 5, 7, 11, 13, 17, 19, 23, 29);

        DoubleSummaryStatitics stats = myList.stream().summaryStatitics(); //   
        System.out.println(": "+stats.getCount());
        System.out.println(": "+stats.getMax());
        System.out.println(": "+stats.getMin());
        System.out.println(": "+stats.getAverage());
    
        
    }
}


---

myList.stream().max(Comparator.comparing(Integer::intValue)).ifPresent(System.out::println);

myList.stream().min(Comparator.comparing(Integer::intValue)).ifPresent(System.out::println);


long cnt = myList.stream().count();

---

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.*;
import java.util.stream.*;
import java.util.function.*;
 
// Issue in Import 
class Main {
    public static void main(String[] args) {
        System.out.println("Start small. Ship something.");
        List<Integer> myList = Arrays.asList(2, 3, 5, 7, 11, 13, 17, 19, 23, 29);
 
        IntegerSummaryStatitics stats = myList.stream().summaryStatitics(); //   
        System.out.println(": "+stats.getCount());
        System.out.println(": "+stats.getMax());
        System.out.println(": "+stats.getMin());
        System.out.println(": "+stats.getAverage());

    }
}