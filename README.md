# interview

1. What is the difference between early binding and late binding in C#?

Compile time polymorphism means we will declare methods with same name but different signatures because of this we will perform different tasks with same method name. This compile time polymorphism also called as early binding or method overloading.

Method Overloading or compile time polymorphism means same method names with different signatures (different parameters)

For more details check this link polymorphism in c#

Run Time Polymorphism

Run time polymorphism also called as late binding or method overriding or dynamic polymorphism. Run time polymorphism or method overriding means same method names with same signatures.

In this run time polymorphism or method overriding we can override a method in base class by creating similar function in derived class this can be achieved by using inheritance principle and using “virtual & override” keywords.

using System;
public class demo{
public static void Main(String[] args){

cal cal ;

add a = new add();
cal = a;
Console.WriteLine("Addition is" + cal.calculate(20, 20));   

sub s = new sub();
cal = s;
Console.WriteLine("Substraction is" + cal.calculate(20, 20));

mul m = new mul();
cal = m;
Console.WriteLine("Multiplication is" + cal.calculate(20, 20));


div d = new div();
cal = d;
Console.WriteLine("Division is" + cal.calculate(20, 20));

Console.ReadLine();
}
}

public abstract class cal{
       public abstract int calculate(int a, int b);
}


public class add : cal {
      public override int calculate(int a ,int b){
        return a+b;
      }
 }

public class sub : cal{
      public override int calculate(int a, int b){
        return a-b;
      }     
}

public class mul : cal{
      public override int calculate(int a, int b){
        return a*b;
      }
 }

 public class div : cal{
       public override int calculate(int a, int b){
            return a/b;
       }
 }
