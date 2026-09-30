

Index Drawback 



IncidentController
IncidentFacade
IncidentService
Incident





public class Singleton{
	private static final volatile Singleton INSTANCE;
	
	private Singleton(){
	}
	
	public static getInstance(){
		if(INSTANCE==null){
			synchrnozied(Singleton.class){
				return new INSTANCE();
			}
		}
		return INSTANCE;
	}

}


1,2,3,4,5,6


myList.stream()
.sorted(Collections.reverseOrder())
.forEach(System.out::println);


1,2,3,4,5,6
Index Iterate : NO




DAO 

any()


@Before



anyAll()



Java Memory Model

Java 6 


SQL

Fetching Strategy 
	EAGER
	LAZY 

Hibernate

Locking 


How to Determine API vs Frontend ? How to determine ?


How to deterimine 




IncomingRequest ->

API Gateway ->

JWT Authentication (Spring Security Flow) ->

