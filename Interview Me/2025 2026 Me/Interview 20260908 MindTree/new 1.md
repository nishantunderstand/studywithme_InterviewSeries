Collections


List<Integer> list = Arrays.asList(10,11,12,13,14);
list.stream().reversed().findFirst().ifPresent(System.out::println);
