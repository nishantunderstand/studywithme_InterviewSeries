Operator Overloading Concept.


Constructor()
Constructor1(a,b)
Constructor2(a,b,c)
Constructor3(a,b,c,d)
Constructor4(a,b,c,d,e)

public class Constructor{
	int a = 10;
	int b = 20;
	
	public Constructor(){
		this.a = a;
		this.b = b;
		Constructor1(a,b);
	}
	
	public Constructor(){
		Constructor1(a,b);
	}
	
	
}




void add(int a,int b)
int add(int a,int b,int c)

add(int a,int b)



int 
long
double 


int a = 10;

Integer iWrap = (Integer) a;
int b = Integer.valueOf(iWrap);
int b = Integer.valueOf(iWrap);


var 




0 1 1 2


int a = 0;
int b = 1;

fib(a,b);


// Base Case
if(a==0 && b==1) return;  //<--
int c = a+b;
System.out.println(c);
return fib(b,c);