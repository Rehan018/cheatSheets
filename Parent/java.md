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

#### Constants

```
final float PI = 3.104;
```

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

