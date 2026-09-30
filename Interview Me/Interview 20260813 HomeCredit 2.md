DTO
IndcidentAskClarificationRequestDTO
IndcidentAskClarificationResponseDTO

Controller 
IIncident
Inceident 

Service
IIncidentService
IncidentService

Reposistory
IncidentRepository

FacadeLayer 
IncidentFacade

Transformer
IncidentTransformer

Entity
IncidentMasterEntity



----


IncidentMasterEntity

private Long id;
privat int incidentId;
private String description



---



IndcidentAskClarificationRequestDTO
private int id;
private int incidentID;
private AttachementEntity files;


IndcidentAskClarificationResponseDTO

private int id;
private int incdentID;
private AttachementEntity files;															 
private String


Controller 

@AllArgsConstructor
@RestController
private final IncidentFacade facade;

@GetMapping("/v1/incient/{id}")
public ResponseEntity<IncidentAskClarificationResponseDTO> getAskClarification(@Pathvariable String id) throws IOException{
		ResponseEntity<IncidentAskClarificationRequestDTO> response = 
		facade.getAskClarification(id);
		return response.ok(200);
}


-----------

IncidentFacade.java
@AllArgsConstructor

private IncidentRespository repo;
private IncidentStatusLogRespository repo;

private IncidentService  incidetService;
private IncidentManagementService   intmgmtService;
private IncidentService  incidetService;

private IncidentStatusLogTransformer incidentx;
private IncidentMasterService incidentmasterService;


// Business Case 
// Our Goal is to find
// 1. Ask Clarification
// 2. Fetch the Details & Perform The Saving in Master
// 3. Transform the Entity to DTO & Vice Versa.

public IncidentEntity getAskClarification(String id){
		service.findIncidentId(id);				
}

---

IncidentRespository.java
@Repository

private interface IncidentRespository<IncidentEntity,Long>  extends
JpaReposistory{
	IncidentEntity findByIndicentId(id);
}

---

IncidentService.java
@Service
@AllArgsConstructor
private IncidentRespository repo;

public void IncidentService(Long id){
		repo.save(id);
}

----

IncidentEntity.java
@Entity
@Data

private Long id;
private Integer incidentId;
private String desc;


---

IncidentNotFoundException.java

public IncidentNotFoundException extends RuntimeException(String msg){
	public IncidentNotFoundException(String msg){
		super(msg);		
	}
}