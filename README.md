# vaccine-info-exception-handling
code
import java.util.*;
class vaccinedaydoseException extends Exception{
    vaccinedaydoseException(String msg){
        super(msg);
    }
}
public class Main
{
public static void main(String[] args) {
Scanner sc=new Scanner(System.in);
System.out.println("Welcome to the vaccine program...");
System.out.println("enter the difference in days of your vaccine doses: ");
   int days=sc.nextInt();
   try{
   if(days<0 || days>100){
       throw new vaccinedaydoseException("invalid number of days! enter the proper number of days");
   }
   }
   catch(Exception e){
       e.printStackTrace();
   }
   try{
       if(days>=1 && days<=84){
           throw new vaccinedaydoseException("You are eligible for the second dose of vaccination");
       }
   }
   catch(Exception e){
       e.printStackTrace();
   }
   finally{
       System.out.println("please register yourself on our website for futher details of second dose");
   }

}
}

