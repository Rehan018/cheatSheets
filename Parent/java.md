## Table of Contents :

### Taking Inputs
#### Using Scanner

```
import java.util.Scanner;

Scanner sc = new Scanner(SYstem.in);

String str = sc.nextLine();
```

#### Using Buffered Reader

```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

String str = new br.readLine();
```

#### Using Console

```
String str = System.console().readLine();
```

#### Using Command Line Arguments

```
// Pass arguments when we run Program 
javac <file-name>

java <file-name> arg1, arg2, ...
```

### Primitive Data Types

| <b>byte - </b>8 bits        | <b>short - </b>16 bits  |
| --------------------------- | ----------------------- |

| <b>int - </b>32 bits        | <b>long - </b>64 bits   |
| --------------------------- | ----------------------- |

| <b>float - </b>32 bits      | <b>double - </b>64 bits |
| --------------------------- | ----------------------- |

| <b>char - </b>16 bits       | <b>boolean - </b>1 bits |
| --------------------------- | ----------------------- |

### Escape Sequences

```
\t  for tab
\\  for backslash
\'  for single quote
\"  for double quote
\?  for question mark
\r  for carriage return
```

### Type Casting

```
// Widening Type Casting -> Lower into Higher
int x = 451;
double xx = x;

// Narrowing Type Casting .> Higher into Lower
double xx = 4.51;
int x = (int)x;
```

### Ternary Operator

```
int var = (condition) ? True : False;
```

### Naming Convention

```
// Class
public class Emp{
  ...
}

// interface
interface{
  ...
}

// Package
package com.app;
class Emp{
  ...
}
```

### Super keyword

```
class Parent{
  String color = "White";
}

class child extends Parent{
  String color = "Black";
  
  S.O.P(color + super.color);   // It'll print -> BlackWhite
}
```

### Instance Initializer Block
- <p>It'll RUN each time when object is created.</p>
- <p>It'll invoked before the constructor.</p>
- <p>It'll invoked after the Parent Constructor.</p>

```
class Git{
  int i = 0;
  Git(){
    S.O.P.("From Git : " + i);
  }
  
  // Instance Initializer Block
  {
    i = 50;
    S.O.P.("From Instance Inializer");
  }
}
```

Output is :<br />
`From Instance Initializer`<br />
`From Git : 50`

### Final Keyword

#### Constants
- final variable can't be change

```
final float PI = 3.104;
```

#### Method
- final method can't be override
```
class A{
  final void run(){ S.O.P.("running"); }
}

class B extends A{
  void run(){ S.O.P.("Waiting"); }
  
  P.S.V.M.(String[] args){
    new B.run();
  }
}
```

Output is : <br />
`Compile Time Error`

#### Class
- final class can't be extendable

```
final class A{ }

class B extends A{
  ...
}
```

Output is : <br />
`Compile Time Error`

- We can Inherit final method.
- We can initialize blank final variable in constructor only.
- A blank static final variable can only initialized in static block.

### Static Keyword
- Java main() is static because a non-static method can call by an object that cost an extra memory.
- Static variable can used from static methods only.
#### Static Block 
- Used to initialized static data member.
- Executed before the main().

```
class A{
  static( S.O.P.("Before Main"); }
  
  P.S.V.M(String[] args){
    S.O.P.("In Main");
  }
}
```

Output is : <br />
`Before Main` <br />
`In Main`

### Strings
#### String Length

```
String str = "There is many Line";

int L = str.length();
```

#### toUpperCase() & toLowerCase()

```
S.O.P.(str.toUpperCase());

S.O.P.(str.toLowerCase());
```

#### indexOf()

```
S.O.P.(str.indexOf("e"));
```

#### concat()

```
str1 = "Hello";
str2 = "Bhai";

S.O.P.(str1.concat(str2));
```

Output is : 
`HelloBhai`

### Parsing

```
// Convert to an int
int Integer.parseInt(String s)

// Convert to a double
double Double.parseDouble(String s)

// Convert to a Long
long Long.parseLong(String s)
```

### Math Library

```
// Import
java.lang.Math.*;

// Absolute value of a
double abs(double a)

// Max of a & b
double max(double a, double b)

// Min of a & b
double min(double a, double b)

// Sine of theta
double sin(double theta)

// Cosine of theta
double cos(double theta)

// Tangent of theta
double tan(double theta)

// Convert angle fron degrees to radians
double toRadians(double degrees)

// Convert angle fron radians to degrees
double toDegrees(double radians)

// exponential of a ( e^a )
double exp(double a)

// Natural Log of a (lna)
double log(double a)

// raise power a to the b
double pow(double a, double b)

// Round a to the nearest Integer
long round(double a)

// Random number in [0, 1)
double random()

// Square root of a
double sqrt(double a)

// Value of e (constant)
double E

// Value of PI (constant)
double PI
```

### File Operations

```
// check whether the file is readable or not
file.canRead()

// Create an empty file
file.createNewFile()

// check writable or not
file.canWrite()

// check file exists or not
file.exists()

// Delete a file
file.delete()

// return name of the file
file.getName()


```
