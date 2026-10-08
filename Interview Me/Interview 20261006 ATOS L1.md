
import java.util.*;
import java.util.stream.*;
import java.util.function.*;


class Main {
    public static void main(String[] args) {        
        // String input = "Microservice";
        // StringBuilder sb = new StringBuilder(input);
        // System.out.println("== Reversed===");
        // System.out.println(sb.reverse().toString());
        
        // System.out.println("== HashMap ===");
    
        // input.chars() // Interger -> ASCII 
        //     .mapToObj(ch -> (char)ch) // 
        //     .collect(Collectors.groupingBy(
        //         Function.identity(),
        //         LinkedHashMap::new, // Insertion -> LinkedHashMap 
        //         Collectors.counting()
        //     )).forEach((k,v)-> System.out.println(k+"->"+v));

        String input2 = "Hello World";        

          input2.chars() // Interger -> ASCII 
            .mapToObj(ch -> (char)ch) // 
              .filter(ch-> ch !=' ') // WhiteSpace 
            .collect(Collectors.groupingBy(
                Function.identity(),
                LinkedHashMap::new, // Insertion -> LinkedHashMap 
                Collectors.counting()
            )).entrySet()
              .stream()
              .filter(entry -> entry.getValue()==1L)
              .map(Map.Entry::getKey)
              .forEach(System.out::println);
    }
}


-- LIMIT + OFFSET APPROACH

SELECT * FROM employee
ORDER BY salary DESC
LIMIT 1 OFFSET 1;

