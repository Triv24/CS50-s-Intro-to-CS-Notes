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
