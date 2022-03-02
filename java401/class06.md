# Inheritance and Interfaces
## Inheritance 
Classes can be derived from other classes thats means inheriting state and methods from parent class to child class . 

 The main idea of inheritance is when you want to create a new class and there is already a class that includes some of the code that you want, you can derive your new class from the existing class. 

    public class ParentClass/SuperClass {
         public value ;    

        public void doThings{
            // Action 
        }
            
    }

    public class SubClasses/ChildClass extends ParentClass/SuperClass {
         public value1 ;    

        public void doThings1{
            // Action 
        }
            
    }

## Interfaces 

The interface like `Contract` between the proggrammers that work in the same software . 

Interface in java programming language is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types.


    public interface example {

    // constant declarations, if any

    // method signatures
    
    // An enum with values RIGHT, LEFT

    int example (int val);

    }

    In the class that implement interface should use the same method in interface 

    public class example1 implements example {
        int example (int val){
            // Do things 
        }
    }
