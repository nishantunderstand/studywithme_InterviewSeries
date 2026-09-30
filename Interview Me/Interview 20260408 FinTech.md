@PostMapping("/save")
ResponseEntity<ApiResponse<FormRequestDTO>> fillForm(RequestBody )
	{	
	FormResponseDTO respone = facade.fillForm();
	return  
}


LinkedList 1->2->3->4->5


ListNode curr = head;    // 1
ListNode prev = null;    //
ListNode next;

while(curr!=null){
	next  = curr.next; // Preserve        || 2->3  
	curr.next = prev; // Reverse The Link    null<-1 || 1<-2
	prev = curr;  // Shift   prev= null => prev = 1   || prev = 2
	curr = next;   // Move Forward   1 => 2   => 
}

return prev;





Power of 2 

4/2== 0
8/2= return true 
6%2 = return false


private boolean Solution(int n){
		
}

