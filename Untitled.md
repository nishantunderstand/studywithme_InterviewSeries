

List.stream().sorted().forEach(System.out::println);
1. Odd 
2. Then Even 



Use streams to sort an array which has odd and even numbers odd should come in first and then even numbers and odd should be sorted and even should be sorted.  🤔🤔🤔 



Use streams to provide an output array which has no negatives or 0s he mentioned to use partitioning by.
list.stream().filter(n-> n>0 ).forEach();

Map<List<Integer,Boolen>> map =  List.stream().collect(PartitioningBy(n->n>0));

