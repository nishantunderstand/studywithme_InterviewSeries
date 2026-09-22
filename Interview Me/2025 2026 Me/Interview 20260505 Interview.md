class A {
    void show() {
        System.out.println("A");
    }
}
class B extends A {
    void show() {
        System.out.println("B");
    }
}
public class Main {
    public static void main(String[] args) {
        A obj = new B();
        obj.show();
    }
}


// 


try {
    int x = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Exception");
} finally {
    System.out.println("Finally");
}

O/P
Exception
Finally



Write a Program to reverse a String 

String str = "Hello";
StringBuilder sb = new StringBuilder(str).reverse();
return sb.toString();





int x = 2;

switch(x) {
    case 1:
        System.out.println("1");
    case 2:
        System.out.println("2");
    case 3:
        System.out.println("3");
}


O/P
2
3




int x = 2;
switch(x) {
    case 1:
        System.out.println("1");
    case 2:
        System.out.println("2");
    case 3:
        System.out.println("3");
}

break 

Fall through in switch



String a = "abc";
String b = "ab";
final b = b + "c"; 

System.out.println(a == b); // Reference  => FALSE 

SCP 
abc // 1
ab // 2
c // 3

Heap 
abc


System.out.println(a.equals(b));   // Value  => TRUE 





int[] arr = {1, 2, 3, 4, 2, 5, 1,-1};
 
 
1,2
List<Integer> res = new ArrayList<>();

Set
1
2
3
4
5

Set<Integer>





class Test {
    static int x = 10;
    Test() {
        x++;
    }
}
Test t1 = new Test();  //  11
Test t2 = new Test();   // 12
System.out.println(Test.x); // 12

O/P : 12



public static int test() {
    try {
        return 1;
    } finally {
        return 2;
    }
}
 
System.out.println(test());
O/P : 2