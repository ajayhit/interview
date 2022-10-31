# interview
1. What is OOP, and how does it relate to the .NET Framework?

As a technique, OOP allows .NET developers to create classes containing methods, properties, fields, events and other logical modules. It also lets developers create modular programs, which they can assemble as applications. OOPs have four basic features: encapsulation, abstraction, polymorphism and inheritance.

2. What is encapsulation?

encapsulation is to think of it as “hiding” the state of an object as private or protected. Under this principle of information hiding, the internal workings of an object are segregated from the rest of the application. This is useful because it makes it less likely that other objects can modify the state or behavior of the object in question.

using System;
namespace EmployeeApplication {
class Employee {
private string name;
private string dept;
public string GetName() {
return name;
}
public void SetName(string n) {
name = n;
}
public string GetDept() {
return name;
}
public void SetDepartname(string d) {
dept = d;
}
public void Display() {
Console.WriteLine("Name: {0}", name);
Console.WriteLine("Department: {0}", dept);
}
}
class ExecuteRectangle {
static void Main(string[] args) {
Employee e = new Employee();
e.SetName("AmKy");
e.SetDepartname("EduCBA");
e.Display();
Console.ReadLine();
}
}
}


2. What is the difference between early binding and late binding in C#?

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
