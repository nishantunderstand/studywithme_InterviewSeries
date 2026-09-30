class Counter {

    int count = 0;
 
    void increment() {

        count++;

    }

}
 
String str = "NIshant";
str = "Purvi";
 
class Animal {

    void sound() {

        System.out.println("Animal");

    }

}
 
class Dog extends Animal {

    void sound() {

        System.out.println("Dog");

    }

}
 
Animal a = new Dog();

a.sound();
 
Problem: Given a string, find the length of the longest substring that contains no repeated characters.
 
Input: "abcabcbb"

Output: 3
 
Input: "bbbbb"

Output: 1
 
 
Input: "pwwkew"

Output: 3
 
 
final test case : "dvdf", 3
 
Find Employee who are managers as well

EmpId, EmpName, ManagerId, Salary
101, Purvi, 100, x
102, Nishant, 101, y
 




class Counter {
    int count = 0;
 
    void increment() {
        count++;
    }
}

int counter = 0;


public class A extends thread{
	private int cnt = 0;
	@Override
	public void run(){
	
	for(int i=0;i<1000;i++){
		cnt++;
	}	
	}
	
}

public class Main{
	public static void main(String[] args){
		A a1 = new A();
		A a2 = new A();
		a1.start(); 
		a2.start();		
	}
}






class Counter {

    int count = 0;
 
    void increment() {

        count++;

    }

}
 
String str = "NIshant";
str = "Purvi";
 
class Animal {

    void sound() {

        System.out.println("Animal");

    }

}
 
class Dog extends Animal {

    void sound() {

        System.out.println("Dog");

    }

}
 
Animal a = new Dog();

a.sound();
 
Problem: Given a string, find the length of the longest substring that contains no repeated characters.
 
Input: "abcabcbb"

Output: 3
 
Input: "bbbbb"

Output: 1
 
 
Input: "pwwkew"

Output: 3
 
 
final test case : "dvdf", 3
 
Find Employee who are managers as well

EmpId, EmpName, ManagerId, Salary
101, Purvi, 100, x
102, Nishant, 101, y
 


 Find Employee who are managers as well
EmpId, EmpName, ManagerId, Salary

101, Purvi, 100, x
102, Nishant, 101, y


----


SELECT e.EmpName  
FROM Employee e
JOIN Employee m
where e.id = m.id;



VendingMachine

RequestValidator

Entity Class
Item
VendingMachine
PaymentGateway

Reposistory Class


Controller Class 





abcabcbb => 3

Sliding window 
HashMap 
K -> Character
V -> Occurecne

start
end 
maxLen





Problem: Given a string, find the length of the longest substring that contains no repeated characters.

currLen 2 
maxlen 3
a->1 
b->1
c->1

a -> Present in HashMap 
start++
freq by 1 ?? If freq==0, Remove it  

Input: "abcabcbb"
Output: 3
 
Input: "bbbbb"
Output: 1
 
 
Input: "pwwkew"
Output: 3
 
 
final test case : "dvdf", 3




10 Millions User ID 
Unique 

Sorted : 





class Animal {
    void sound() {
        System.out.println("Animal");
    }
					
} 
class Dog extends Animal {
    
}
 

Animal a = new Dog();
a.sound();


Inheritance+Polymorpihs : Runtime Dispatch


Dog d1 = new Animal()




String str = "Nishant";
str = "Purvi";
String pqr = "Nishant";



SCP : 

str -> Nishant (4k)
pqr ->




Thread Life

NEW
-> start 
RUNNABLE 
-> run 

RUNNING 

BLOCKED
-> stop 
TERMINATED




Race Condition

Lock
1. Intrinsic
	synchronize method , block
2. Extrinsic 
	Lock Interface
	