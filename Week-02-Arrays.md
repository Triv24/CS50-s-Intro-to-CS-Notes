# Lecture 02 : Arrays 

- When we run a code 4 steps are happening :
1. Preprocessing :
    - It converts all the #include lines to the function prototypes.
2. Compiling : 
    - Converts whole program t assembly code (machine code)
3. Assembling :
    - Whole assembly code is converted into binary code
4. Linking :
    - All the files are combined into one final program.

## Debugger in VS Code :
- there are different options for us to go through the flow of the code.

---

### Data types :
- bool (1 byte)
- int (4 bytes)
- long (8 bytes)
- float (4 bytes)
- double (8 bytes)
- char (1 byte)
- string (dynamic memory allocation)

// This memory is stored in the RAM 

## Arrays :
- Arrays are the collection of elements of the same data type stored in contiguous memory locations.
```c
    #include <stdio.h>
    #include <cs50.h>

    int main (void) {
        
        const int N = get_int("Enter the number of scores");
        int scores[N];

        //accept valus for array using loops 
        for (int i = 0; i < N; i++){
            scores[i] = get_int("Enter a score: ");
        }
    }
```

### String :
- String is an sequence/array of characters.
- A string actually ends with an extra byte -- `\0` OR `NUL`.
- We can also create an array of strings. 

- To calculate length of string -- function `strlen()`. :: But first include `string.h`.

```c
    //Note : We can add wo expressions in the initialisation part of for loop as follows : 

    #include <cs50.h>
    #include <stdio.h>
    #include <string.h>

    int main (int argc, string argv[]){
        string s = get_string("Input is : ");
        printf("Output is : ");
        for (int i = 0; n = strlen(s); i < n; i++){
            printf(s[i]);
        }
    }

    // Here, `argc` and `argv` is related to the command line arguments we type just after the run command. 
    // int argc is the number of arguments we type.
    // string argv is the array of all the string arguments e type in the command.
```

## Exit Status :
- The exit status of a program is an integer value that is returned to the operating system when the program terminates.

## Cryptography :
- Ability to send info securely.
- Encryption : converting plain text to cipher text.
- Decryption : converting cipher text to plain text.

### Cipher :
- An algorithm which is used for the encryption of the messages.
