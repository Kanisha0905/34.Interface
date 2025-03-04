# 34.Interface
import java.util.Scanner;
interface Calculator{
    double add(double a,double b);
    double subtract(double a,double b);
    double multiply(double a,double b);
    double divide(double a,double b);
}
class SimpleCalculator implements Calculator{

    @Override
    public double add(double a, double b) {
        return a+b;
    }

    @Override
    public double subtract(double a, double b) {
       return a-b;
    }

    @Override
    public double multiply(double a, double b) {
        return a*b;
    }
    @Override
    public double divide(double a, double b) {
      if(b==0){
          System.out.println("Error:Division by zero is not allowed!");
          return Double.NaN;
      }
       return a/b;
    }
}

public class Interface{
    public static void main(String[] args){
        Scanner scanner= new Scanner(System.in);
        Calculator calculator=new SimpleCalculator();
        System.out.println("Welcome to the Simple Calculator!");
        System.out.print("Enter the first numberl:");
        double num1=scanner.nextDouble();
        System.out.println("Enter the second number:");
        double num2=scanner.nextDouble();
        
        System.out.println("\n Results");
        System.out.println("Addition:"+calculator.add(num1,num2));
        System.out.println("Subtraction:"+calculator.subtract(num1,num2));
        System.out.println("Multiplication:"+calculator.multiply(num1,num2));
        System.out.println("Division:"+calculator.divide(num1,num2));
        scanner.close();
        
    }
    
} 
Output:
Welcome to the Simple Calculator!
Enter the first numberl:10
Enter the second number:
5

 Results
Addition:15.0
Subtraction:5.0
Multiplication:50.0
Division:2.0
