class Employee{
	int age = 10;
	String name = "Aman";
}

class Application{
	Employee e1 = new Employee(); // 4K	|| Object 1 // Garbage Collectio
	e1 = new Employee();      // 5K   || Object 2
	Employee e2 = new Employee();
}

1. How many Object will be created ?
2. Stack Frame and Object in Heap 
3. GC
4. Memeory Leak

---

SCP : Aman
Java 7 : Permgen
Java8 : SCP -> Heap 



---

Stack = e1
Employee : Heap 
	age and name : instance / Part of heap 
	Aman => Heap 
	age => Heap 

---

@Configuration
public class AppConfig{	
	@Bean
	public Employee1 employee(){
		return new Employee1();
	}
	
	@Bean
	public String employee(){
		return "Nishant";
	}
}

Bean Name : employee1 
Bean Type : Employee1

Bean Name : employee1 
Bean Type : String





---

import java.io.IOException;
class Main {
    public static void main(String[] args) {
        try{
        	display();
        }catch(Exception e){
        	System.out.println(e.getMessage()+"--> 1");
        }
    }

    public static void display() throws IOException{
        try{
            throw new IOException("!!!! Not Found !!!! ");
        }catch(IOException e){
            System.out.println(e.getMessage()+"--> 3");
        }
        
    }
}