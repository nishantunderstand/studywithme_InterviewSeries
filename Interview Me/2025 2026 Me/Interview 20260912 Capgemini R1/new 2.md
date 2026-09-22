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