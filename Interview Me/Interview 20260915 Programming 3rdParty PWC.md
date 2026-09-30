// Online Java Compiler
// Use this editor to write, compile and run your Java code online

import java.util.*;

class Printer{
    private int num = 1;
    
    public synchronized void printOdd() throws Exception {
            while(num<=10){
                while(num%2==0){
                    wait();
                }
                if(num<=10){
                    System.out.println("Thread 1: "+ num++);
                    notifyAll();
                }
            }
        }

    public synchronized void printEven() throws Exception  {
            while(num<=10){
                while(num%2==1){
                    wait();
                }
                if(num<=10){
                    System.out.println("Thread 2: "+ num++);
                    notifyAll();
                }
            }
        }
}



public class Main {
    public static void main(String[] args)  {
        // Thread 1 :: Odd Number 
        // Thread 2 :: Even Number 
        
        Printer p1 = new Printer();
 
        Thread t1 = new Thread(()->{
            try{
                p1.printOdd();
            }catch(Exception e){
                System.out.println("Thread 1");
            }
        });

        Thread t2 = new Thread(()->{
            try{
                p1.printEven();
            }catch(Exception e){
                System.out.println("Thread 2");
            }
        });
        
        
        t1.start();
        //t1.join();    
        t2.start();
        //t2.join();
        
    }
}