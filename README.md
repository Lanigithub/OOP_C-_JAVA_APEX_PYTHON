## OOP: C#, JAVA, APEX, and PYTHON

### 1. OOP (object oriented programming: python Java, Apex, C#) is about creating Data and methods to perform operations on data. 


### 2. The main advantage of oop is that OOP provides a clear structure for the program, and keep it dry (don't repeat yourself " , and makes the codes easier to maintain, modify and debug. 
***
### 3. What is the structure of object-oriented programming?
### The structure, or building blocks, of object-oriented programming include the following:
* #### Classes are user-defined data types that act as the blueprint for individual objects, attributes and methods.
* #### Objects are instances of a class created with specifically defined data. Objects can correspond to real-world objects or an abstract entity. When class is defined initially, the description is the only object that is defined.
* #### Methods are functions that are defined inside a class that describe the behaviors of an object. Each method contained in class definitions starts with a reference to an instance object. Additionally, the subroutines contained in an object are called instance methods. Programmers use methods for reusability or keeping functionality encapsulated inside one object at a time.
* #### Attributes are defined in the class template and represent the state of an object. Objects will have data stored in the attributes field. Class attributes belong to the class itself.
( https://www.techtarget.com/searchapparchitecture/definition/object-oriented-programming-OOP) 
***
#### Syntax for C#:
```
using System;                           // using System means that we can use classes from the System namespace.               
                                        //A blank line. C# ignores white space. However, multiple lines makes the code more readable.
namespace HelloWorld                     // namespace is used to organize your code, and it is a container for classes and other namespaces.
{                                       // The curly braces {} marks the beginning and the end of a block of code.
  class Program                         // class is a container for data and methods, which brings functionality to your program. Every line of code that runs in C#                                             //must be inside a class. In our example, we named the class Program.
  {
    static void Main(string[] args)      // Main method: Any code inside its curly brackets {} will be executed
    {
      Console.WriteLine("Hello World!");      // To output values or print text in C#, you can use the WriteLine() method
    }
  }
}

```
#### 3. Classes and Objects: Everything in C# is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an #### object. The car has attributes, such as weight and color, and methods, such as drive and brake.
Example of the Class Car with 3 members: two fields and one method , and a special  static Main( ) method to create objects and call methods to be excueted:
```
Class Car  {

string color = "Blue";  //field or attribute of the car with initializing a value
int   maxSpeed;        // field without initialize a calue
public void Speeding( )   //Method 

{
Console.WriteLine(" The Car is speeding!!!");   //code in the method to be called for execution 

} 

static void Main(string[] args)   // pre-defined method Main( String[] args) accepting string array of arguments
                            //To create an object myObject and call to execute the methods or display the attributes using object dot notation myObject.field

{
Car myObject= new Car( );    // Create an object myObject using new car(); 

myObject.maxSpeed = 200;      //initialize  the maxSpeed arrtibute and now its an object in the class

Console.WriteLine(myObject.color);      // print out the two objects in the class
Console.WriteLine(myObject.maxSpeed);

myObject.Speeding( );   // call the method 
} 
// Output: 
blue
200
The car is speeding!!! 

}
```
### 4. What are the 4 main principles of OOP: Abstraction, Inheritance, Encapsulation and Polymorphism
 *  #### Abstraction: Data abstraction is a mechanism of retrieving the essentials details without dealing with background details.
  ( https://www.salesforcetutorial.com/data-abstraction/)--Check out some " What is..." in the salesforce tutorials
 *  #### Inheritance: Inheritance is the procedure in which one class inherits the attributes and methods of another class.  
    In C#: Derived Class (child) - the class that inherits from another class  \
            Base Class (parent) - the class being inherited from  \
         **To inherit from a class, use the : symbol.**
   #### Example of inheritance in C#: 
   ( https://www.w3schools.com/cs/showjava_classes3.asp?filename=demo_inheritance) 
   #### the Car class (child) inherits the fields and methods from the Vehicle class (parent):
   ```
   class Vehicle  // base class (parent) 
{
  public string brand = "Ford";  // Vehicle field
  public void honk()             // Vehicle method 
  {                    
    Console.WriteLine("Tuut, tuut!");
  }
}

class Car : Vehicle  // derived class (child)
{
  public string modelName = "Mustang";  // Car field
}

class Program
{
  static void Main(string[] args)
  {
    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (From the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand field (from the Vehicle class) and the value of the modelName from the Car class
    Console.WriteLine(myCar.brand + " " + myCar.modelName);
  }
}
```

 *  #### Encapsulation: a way to ensure security. Basically, it hides the data from the access of outsiders.
      in C#, The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. To achieve this, you must declare fields/variables as private
   #### provide public get and set methods, through properties, to access and update the value of a private field
   (https://www.w3schools.com/cs/cs_properties.php ) 
 #### Example from C#: 
 ```

 // use the Name property to access and update the private field of the Person class:
 class Person
{
  private string name; // field
  public string Name   // property
  {
    get { return name; }
    set { name = value; }
  }
}

class Program
{
  static void Main(string[] args)
  {
    Person myObj = new Person();
    myObj.Name = "Liam";
    Console.WriteLine(myObj.Name);
  }
}
// output: Liam

```
 *  #### Polymorphism: means having many forms. In OOP it refers to the functions having the same names but carrying different functionalities.

*** 
### Relationship between a class and objects: class is the Blueprint or template of objects and objects are instances . Example of class  Car has objects of types (make)of cars (Volvo, Audi, Toyota, Tesla) and their attributes or fields ( color, make, model, year ,weight) and methods (or functions: drive and brake.

####  constructor: a class is like objects constructor, or a blueprint to create objects.
#### a special method is called a constructor that is used to initialize objects. For example model=" Santa Fe" in a method is called a constructor that sets initial value for a field. 
```
class Car
{
  public string model;

  // Create a class constructor with a parameter
  public Car(string modelName)
  {
    model = modelName;
  }

  static void Main(string[] args)
  {
    Car Hyundai = new Car("Santa Fe");
    Console.WriteLine(Hyundai.model);
  }
}

// Outputs "Stata Fe"
#### Static and public are two access identifiers .

#### Methods need to be public for objects to access. Static method can be accessed without creating an object of the class. 

#### Creating an object needs to specify the class name followed by the object name, and used the keyword new: Car toyota= new Car ();
