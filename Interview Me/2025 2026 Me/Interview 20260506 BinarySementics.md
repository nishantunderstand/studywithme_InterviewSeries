public class FutureExample{

	public static voi
	d main(String[] args) throws Exception{
		ExecutorService executor = Executors.newSingleThreadExecutor();
		
		Callable<String> task = ()->{
			Thread.sleep(1000);
			return "Task Completed";
		}
		
		Future<String> future = executor.submit(task);
		
		String result = future.get();
		System.out.println(result);
		
		executor.shutdown();
	}

}


Create to Fetch The EmployeeDetailsBy Id


EmoployeeEntity
@Data
private long id;
private String name;
private int salary;



EmployeeReposistory.java

public interface employeeRepoistory<EmoployeeEntity,long> extends CRUDRepository{	
	List<EmoployeeEntity> findbyId;
}



EmployeeService.java

public Class EmployeeService{	
	@NoArgsConstructor // Constructor Injection
	private final EmployeeReposistory repository;

		public void saveEmployee(){
			repository.save();
		}
}


MethodOverloading  : 
MethodOverding  : 


JWT
	API
	


ServiceA
	KAFKA INSERTED

ServiceB 
	KAFKA INSERTED
	




ServiceA
	UserService
		Created

ServiceB
	EmployeeService





Executors Indepdenly 

Executors + Future
Executors + CompletableFuture

Future + FutureTask
CompletableFuture + FutureTask