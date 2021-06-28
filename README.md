# Basic-Calculator-in-Java
The project made in java. This simple calculator project made in Object Oriented Programme





import java.util.Scanner;
class Numbers{
       public void display(){
           System.out.println("*******");
           System.out.println("****");
            System.out.println("**");
           System.out.println("Welcome to the calculator");
       }
}
class Calculators extends Numbers{
         public void numbers(){
             double num1;
             double num2;
             char op;
             
             Scanner sc = new Scanner(System.in);
             System.out.println("Enter the numbers");
             num1 = sc.nextDouble();

             Scanner rs = new Scanner(System.in);
             op = rs.next().charAt(0);
        
             num2 = sc.nextDouble();
              sc.close();
              rs.close();
            try {
                if(op == '+'){

                    System.out.println("The total number is: " + (num1 + num2));
                } else if(op == '*'){
                    System.out.println("The multiply result is: " + (num1 * num2));
                } else if(op == '-'){
                    System.out.println("The subtract result is: " + (num1 - num2));
                } else if(op == '/'){
                    System.out.println("The divide result is : " + (num1 / num2));
                }
            } catch (Exception e) {
                //Excepton Handle
                System.out.println(e);
            }
         }
}
public class Calculator{
            public static void main(String[] args) {
               Calculators c = new Calculators();
               c.display();
               c.numbers();
           };
}
