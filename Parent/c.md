## Table of Contents : 
- <b>[Boilerplate Code](#boilerplate-code)</b>
- <b>[Print & Scan](#print--scan)</b>
- <b>[Data Types](#data-types)</b>
- <b>[Escape Sequences](#escape-sequences)</b>
- <b>[Pointers](#pointers)</b>
- <b>[Array](#array)</b>
- <b>[String](#string)</b>
- <b>[Structure](#structure)</b>
- <b>[File Handling](#file-handling)</b>
- <b>[Dynamic Memory Allocation](#dynamic-memory-allocation)</b>

<hr />

### Boilerplate Code

```
#include<stdio.h>
int main(){
  return(0);
}
```

### Print & Scan

```
printf("Hello World!")

scanf("placeholder", variables)
```

### Data Types

`char` `int` `float` `double` `void`

### Escape Sequences

<p>Alarm or Beep <code>\a</code></p>
<p>Backspace <code>\b</code></p>
<p>Form feed <code>\f</code></p>
<p>NewLine <code>\n</code></p>
<p>Carriage return <code>\r</code></p>
<p>Tab <code>\t</code></p>
<p>Backslash <code>\\</code></p>
<p>Single quote <code>\'</code></p>
<p>Question mark <code>\?</code></p>
<p>Octal No. <code>\nnn</code></p>
<p>HexaDecimal No. <code>\xhh</code></p>
<p>Null <code>\0</code></p>

### Pointers

```
// datatype *var_name;
int *a;
```

### Array

```
// datatype array_name[size];
int arr[10]
int arr[] = { ... }
```

### String
- It's an Array of char.

```
char str[] = " ... "
```

#### gets() function
- It allow to enter multi-word string

```
gets(str);

gets(str, 20, stdin)
```

#### gets() function
- It's used to display string

```
puts(str)
```

#### strlen() function
- Used to get Length of string

```
strlen(str)
```

#### strcpy() function
- copy a string

```
strcpy(destination, source)
```

#### strcat() function
- concatenate two strings

```
strcat(str1, str2)
```

#### strcmp() function
- compare two strings

```
strcmp(str1, str2)
// return 0 - if both are same
// return <0 - if left string is smaller
// return >0 - if left string is greater
```

### Structure

```
struct <name>{
  int i;
  char ch;
  ...
};
```

#### Typedef

```
typedef struct <name>{
  int i;
  char ch;
  ...
};
```
### File Handling

#### File Pointer

```
FILE *filePointer;
```

#### Open file

```
filePointer = fopen(file.txt, w)
// r, w, r+, w+
```

#### fscanf() function

```
fscanf(FILE *stream, const char *format, ...)
```

#### fprintf() function

```
fprintf(FILE *fptr, const char *str, ...);
```

#### fgetc() function

```
fgetc(FILE *pointer);
```

#### fputc() function

```
fputc(char, FILE *pointer);
```

#### Close a file

```
fclose(filePointer);
```

### Dynamic Memory Allocation
#### malloc() function

```
ptr = (castType*) malloc(size);
```

#### calloc() function

```
ptr = (castType*)calloc(n, size);
```

#### free() function

```
free(ptr);
```

#### realloc() function

```
ptr = realloc(ptr, x);
```

