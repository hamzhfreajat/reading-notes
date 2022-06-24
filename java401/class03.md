# Maps, primitives, File I/O
## Java Primitives versus Objects

### Java Type System
Java has a two-fold type : 
- Primitives such as int, boolean 
- Reference types such as Integer, Boolean


### Pros and Cons
#### Performance && Usage
The primitive types are much faster and require much less memory. Therefore, we might want to prefer using them.

## Exceptions
An exception is an event that occurs during the execution of a program that disrupts the normal flow of instructions

### How to Throw Exceptions
All methods use the throw statement to throw an exception. The throw statement requires a single argument: a throwable object. Throwable objects are instances of any subclass of the Throwable class. Here's an example of a throw statement.

        throw someThrowableObject;

### Advantages of Exceptions
- Separating Error-Handling Code from "Regular" Code
- Propagating Errors Up the Call Stack
- Grouping and Differentiating Error Types

## Scanning
Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.

### Breaking Input into Tokens

import java.io.*;
import java.util.Scanner;

public class ScanXan {
public static void main(String[] args) throws IOException {

        Scanner s = null;
        
                try {
                    s = new Scanner(new BufferedReader(new FileReader("xanadu.txt")));
        
                    while (s.hasNext()) {
                        System.out.println(s.next());
                    }
                } finally {
                    if (s != null) {
                        s.close();
                    }
                }
            }
        }

The output of ScanXan looks like this:

        In
        Xanadu
        did
        Kubla
        Khan
        A
        stately
        pleasure-dome
        ...