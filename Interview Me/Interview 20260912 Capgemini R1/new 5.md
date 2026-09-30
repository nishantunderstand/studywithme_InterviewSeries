// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.*;
import java.util.stream.*;
import java.util.function.*;

// Issue in Import 
class Main {
    public static void main(String[] args) {
        System.out.println("Start small. Ship something.");
        List<Integer> myList = Arrays.asList(2, 3, 5, 7, 11, 13, 17, 19, 23, 29);

        DoubleSummaryStatitics stats = myList.stream().summaryStatitics(); //   
        System.out.println(": "+stats.getCount());
        System.out.println(": "+stats.getMax());
        System.out.println(": "+stats.getMin());
        System.out.println(": "+stats.getAverage());
    
        
    }
}