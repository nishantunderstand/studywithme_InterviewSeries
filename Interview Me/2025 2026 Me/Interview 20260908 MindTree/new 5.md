Design a SpringBoot Architecture 

InputRequest

CDN
DNS


APIGateWay
/user/incident => incident
/user/proces => process

SPOF 
APIGateWay + LoadBalancer 


Spring Security : Authentication

Spring MVC : 
Controller 
/v1/incidet/askClarification

Controller
ServiceLayer
Repostirty
DB

@Tranasaction Annotation

Checked Exception : Explict rollbackFor 
UnChecked Exception / Runtime 




