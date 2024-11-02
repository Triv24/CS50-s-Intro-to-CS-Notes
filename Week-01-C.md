# Lecture 01 - C :

#### Writing a code - Hello, World :

```c
#include <stdio.h>

int main (void) {
  printf("Hello, World\n");
}
```

Note : If we actually need to print "\n" int the code just add one more backslash -- "\\n".

We are gonna use the library -- <cs50.h> in further programs for inputs and outputs.

### Writing a personalised code which says - Hello, 'YourName' :

```c
#include <stdio.h>
#include <cs50.h>

int main (void) {
  string answer = get_string("What's ur Name ?"); //store the input name in a variable named answer
  printf("Hello, %s\n", answer);
}
```

### If conditionals in C :

```c
if (X > Y){
  printf("X is greater than Y\n");
}
else if (X < Y) {
  printf("X is smaller than Y\n");
}
else {
  printf("X and Y are equal.\n");
}
```
---
Counter variable (Increment and decrement) :
```c
int counter = 0; // Declare the variable
counter = counter + 1; // Increment variable by 1
counter += 1; //Another way to increment by 1
counter = counter - 1; // Decrement value by 1
counter -= 1; // Another way to Decrement value by one
```
---
Accept integers from user and compare them : 
```c
#include <stdio.h>
#include <cs50.h>

int main (void) {
  int x = get_int("What is X?");
  int y = get_int("What is Y?");

  if (x < y) {
    printf("X is less than Y\n");  
  }
  else if (x > y) {
    printf("X is greater than Y\n");
  }
  else {
    printf("X and Y are equal\n");
  }
}
```
---
### Use of logical operators in conditional statements :
> These are :
> - AND (&&)
> - OR (||)

```c
  if (x == 'c' || x == 'C' ){ // Logical Operator OR ||
    printf("You have entered c.\n");
  }

  if (x == '1' && y == '1'){ // Logical Operator AND &&
    printf("X = Y = 1\n");
  }
```

### Using Loops :
- while loop :
```c
  int counter = 3;
  while (counter > 0){
    printf("%i\n", counter);
    counter = counter - 1;
  }
```
---
- for loop :
```c
  for(int i = 0; i < 3; i++){
    printf("%i\n", i);
  }
```

---

- do-while loop :
it is used when we want to keep asking the user for positive integer even when he types something other than positive integer.

```c
  do {
    n = get_int("n is : ");
  } // First asks for n 
  while (n < 1); // starts analysing condition after 1 execution.
```

### Functions in C :

1. Void functions :
```c
  #include <stdio.h>

  void meow(void); // Function Declaration above main() method, but definition will be down 

  int main(void) {
    meow();
  }

  void meow(int n){
    for (int i = 0; i < n; i++){
      printf("meow\n");
    }  
  }
```
2. Return Functions :
```c
  #include <stdio.h>
  #include <cs50.h>

  int add(int a, int b);

  int main(void){

    int x = get_char("X is : ");
    int y = get_char("Y is : ");

    int c = add(x,y);

    printf(c);
  }

  int add (int a, int b){
    return a + b;
  }
```

### Linux :
- Open Source Operating system.
- Command line interface (cli)
- Most widely used OS in servers and supercomputers.

#### Some commands on Linux :
1. cd -- change directory
 - The short hand name for the current directory is '.'
 - The shorthand name for parent directory of the current directory is '..'
1. cp -- copy // Syntax : cp <source> <destination> 
 - copies the file you specify as <source> which will save in <destination>
 2. cp -r : This copies the entire directory. -r stands for recursive
1. ls -- lists the file in current folder
1. mkdir -- make directory
1. mv -- stands for move. rename // Syntax : mv [oldNAme] [newName]
1. rm -- removes a file
 2. rm -f : removes without confirmation prompt.
 2. rm -r : removes entre directory
 2. rm -rf : combined -r and -f.
1. rmdir -- remove directory
1. pwd -- stands for present working directory

### Constants in C :
- `const` keyword is used to declare a constant.
- `const` keyword can be used with variables, function parameters, and function return types.
- `const` keyword is used to prevent the variable from being modified.

Syntax : 
```c
const int n = 3;
```

### Truncation :
Truncation is the process of cutting off the decimal part of a number.
Truncation is used when we want to remove the decimal part of a number.
Truncation is used in financial calculations where we want to round off the amount to the nearest
integer.

### TypeCasting :
Typecasting is the process of converting a variable from one data type to another.

```c
  int x;
  int y;

  // to convert x and y integers to floats :
  (float) x;
  (float) y;
```

### Floating-point imprecision (Issue) :
Floating-point imprecision is a common issue in programming where the result of a floating-point operation is not exactly what we expect.
This is because floating-point numbers are represented in binary format, which can lead to rounding errors.
