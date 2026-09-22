AOP Based 

@Transaction Annotation


DB 



----

Find First Non-Repeating Character
String str = "aabbcdeff";
c            
Java 8       
I need HashSet ?
	str.mapToObj(char -> Character.toLowerCase(char))
	.collect(Function.groupingBy())
	
	Set<Character> seen = new LinkedHashSet<>();
	
	Character res = 
	str
	.mapToObj(char -> Character.toLowerCase(char))
	.stream()
	.filter(n->!seen.add(n))
	.findFirst()
	.get();
	
	
	
Longest String in List

list = ["apple","banana","kiwi","watermelon"]


Stream API

Goal :

0 - length


myList.stream().max(Comparator::compare).get()

	