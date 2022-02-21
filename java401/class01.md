
# java basics
In this class i will put many things that I learned : 
1. Variables
2. Operators
3. Expressions, Statements, and Blocks
4. Control Flow Statements

## Variables
---
In gereal java define the following kinds of variables : 
- instance Variables (Non-Static Fields)
- Class Variables (Static Fields) 
- Local Variables 
- Parameters

Variable name are case-sensitive.

### Variables example 
In java we use many differnt type of variable , for example : 
- String 
- int
- float 
- char
- boolean
- long
- short
- double

### String 
String stores text , for example : 

    public class Main{
        public static void main(String[] args){
            String text = "Hello World"; 
            System.out.println(text); 
        }
    }
    // Out : Hello World

---
**NOTE**

In String you should put your text in double quotes not single and don't forget the semicolon.

---      
### Integers
Stores integers but without decimals : 

    public class Main{
        public static void main(String[] args){
            int number = 24 ; 
            System.out.println(number); 
        }
    }
    // Out : 24

### Float
Stores numbers with decimals : 

    public class Main{
        public static void main(String[] args){
            int floatNumber = 24.11 ; 
            System.out.println(floatNumber); 
        }
    }
    // Out : 24.11

### Charecter 
Char stores charecter , for example : 

    public class Main{
        public static void main(String[] args){
            String chatText = 'h'; 
            System.out.println(chatText); 
        }
    }
    // Out : h

---
**NOTE**

In char you should put your text in single quotes not double and don't forget the semicolon.

---      

### Boolean
Stores true or false : 

    public class Main{
        public static void main(String[] args){
            boolean bool = true ; 
            System.out.println(bool); 
        }
    }
    // Out : true



## Operators
---
The oper
| Operators | Precedence |
| --- | ----------- |
| postfix | expr++ expr-- |
| unary | ++expr --expr +expr -expr ~ ! | 
| multiplicative | * / % |
| additive | + - | 
| shift | << >> >>> |
| relational | < > <= >= instanceof | 
| equality | == != |
| bitwise AND | & | 
| bitwise exclusive OR | ^ |
| bitwise inclusive OR | &#124; | 
| logical AND | && |
| logical OR | &#124; &#124; | 
| ternary | ? : |
| assignment | = += -= *= /= %= &= ^= |= <<= >>= >>>=|

## Expressions, Statements, and Blocks
---
### Expressions
We use experssions before like in example :

      public class Main{
        public static void main(String[] args){
            boolean bool = true ; 
            System.out.println(bool); 
        }
    }
    // Out : true

The expression `bool=true` returns an boolean because the assignment operator returns a value of the same data type as its left-hand operand;

### Statements
Each statment followed by semicolon `;` : 
     
     public class Main{
        public static void main(String[] args){
            boolean bool = true ; 
            System.out.println(bool); 
        }
    }
    // Out : true

`boolean bool = true ;`  is statment ; 

### Blocks 
Block is group of statments between braces `{}` : 

    public class Main{
        public static void main(String[] args){ // begin block 
            boolean bool = true ; 
            System.out.println(bool); 
        } // end block 
    }
    // Out : true
## Control Flow Statements
---
The  execution flow do the statment from top to bottom in your code but controle flow statment can change things some of this control flow statment : 
- decision making  (if-then, if-then-else, switch)
- looping statements (for, while, do-while)
- branching statements (break, continue, return) 
