myList.stream().max(Comparator.comparing(Integer::intValue)).ifPresent(System.out::println);

myList.stream().min(Comparator.comparing(Integer::intValue)).ifPresent(System.out::println);


long cnt = myList.stream().count();