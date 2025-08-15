# Mock Exam 2: Lectures 7-12 (Strings, Command Line, Pointers, Dynamic Memory, Multi-file Projects)
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (32 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** How is a string terminated in C?
a) With a space character
b) With the null character '\0' ✓
c) With a newline character
d) Automatically by the compiler

**Question 2:** What will `strlen("Hello")` return?
a) 6
b) 5 ✓
c) 4
d) Error

**Question 3:** In `main(int argc, char *argv[])`, what does `argc` represent?
a) The first argument
b) The number of command line arguments ✓
c) The program name
d) An array of arguments

**Question 4:** What is `argv[0]` always equal to?
a) The first user argument
b) The program name ✓
c) The number of arguments
d) NULL

**Question 5:** What does the `*` operator do with pointers?
a) Gets the address of a variable
b) Gets the value a pointer points to (dereference) ✓
c) Creates a new pointer
d) Multiplies two values

**Question 6:** What does the `&` operator do?
a) Gets the value of a variable
b) Gets the address of a variable ✓
c) Creates a pointer
d) Performs logical AND

**Question 7:** What will this code print?
```c
int x = 42;
int *ptr = &x;
printf("%d", *ptr);
```
a) 42 ✓
b) The address of x
c) 0
d) Error

**Question 8:** What does `malloc()` do?
a) Allocates memory on the stack
b) Allocates memory on the heap ✓
c) Frees memory
d) Creates a pointer

**Question 9:** What must you do after using `malloc()`?
a) Nothing
b) Call `free()` ✓
c) Call `delete()`
d) Set the pointer to 0

**Question 10:** Which function safely copies one string to another?
a) `strcopy()`
b) `strcpy()` ✓
c) `copy()`
d) `stringcopy()`

**Question 11:** What happens if you forget to call `free()` after `malloc()`?
a) Compilation error
b) Memory leak ✓
c) Program crashes immediately
d) Nothing happens

**Question 12:** How do you declare a pointer to an integer?
a) `int pointer x;`
b) `int *x;` ✓
c) `pointer int x;`
d) `int &x;`

**Question 13:** What will this print if run with `./program hello world`?
```c
printf("%d", argc);
```
a) 2
b) 3 ✓
c) 1
d) 4

**Question 14:** Which header file do you need for string functions like `strlen()`?
a) `<stdio.h>`
b) `<string.h>` ✓
c) `<stdlib.h>`
d) `<strings.h>`

**Question 15:** In multi-file projects, what are header files (.h) used for?
a) Function implementations
b) Function prototypes and declarations ✓
c) Main function only
d) Variable definitions

**Question 16:** What does `#ifndef` do in header files?
a) Includes a file
b) Defines a constant
c) Prevents multiple inclusions ✓
d) Creates a function

---

## Section B: Short Answer Questions (28 marks)
*Provide clear, concise answers. 4 marks each.*

**Question 17:** Explain the difference between stack and heap memory. Give one advantage of each.

**Sample Answer:**
Stack memory is automatically managed by the compiler and follows a LIFO (Last In, First Out) structure. Variables declared in functions are stored on the stack and are automatically deallocated when the function returns. Heap memory is manually managed by the programmer using `malloc()` and `free()`. 

**Advantages:**
- Stack: Fast allocation/deallocation, automatic cleanup, no memory leaks
- Heap: Dynamic size allocation, memory persists beyond function scope, can allocate large amounts of memory

**Question 18:** What is the purpose of function prototypes in header files? Why can't we just put the full function definitions there?

**Sample Answer:**
Function prototypes tell the compiler about a function's signature (return type, name, and parameters) without providing the implementation. They allow the compiler to check function calls for correctness before the function is defined. We can't put full definitions in header files because this would cause multiple definition errors when the header is included in multiple source files - the linker would see the same function defined multiple times.

**Question 19:** Explain what "memory leak" means and how it occurs in C programs.

**Sample Answer:**
A memory leak occurs when a program allocates memory using `malloc()` but never calls `free()` to release it back to the system. This causes the program to gradually consume more and more memory, eventually leading to system slowdown or program crashes. Memory leaks commonly occur when pointers to allocated memory are lost (e.g., reassigned without freeing first) or when the program exits without freeing all allocated memory.

**Question 20:** Why is `fgets()` considered safer than `scanf()` for reading strings?

**Sample Answer:**
`fgets()` is safer because it allows you to specify a maximum buffer size, preventing buffer overflows. It reads up to n-1 characters and always adds a null terminator, ensuring the string is properly terminated. `scanf()` with `%s` doesn't have built-in bounds checking and can easily cause buffer overflows if the input is longer than the allocated array size, leading to security vulnerabilities and program crashes.

**Question 21:** What is the difference between `char str[] = "Hello";` and `char *str = "Hello";`?

**Sample Answer:**
`char str[] = "Hello";` creates a modifiable array on the stack that contains the string "Hello" with a null terminator. You can modify individual characters in this array. `char *str = "Hello";` creates a pointer to a string literal stored in read-only memory. Attempting to modify characters in a string literal causes undefined behavior and may crash the program. The array version is safer for string manipulation.

**Question 22:** Explain what happens when you pass an array to a function. How is this different from passing a regular variable?

**Sample Answer:**
When you pass an array to a function, you're actually passing a pointer to the first element of the array. The function receives the memory address where the array starts, not a copy of the array. This means any modifications made to the array inside the function will affect the original array. When you pass a regular variable, you're passing a copy of its value, so modifications inside the function don't affect the original variable.

**Question 23:** What is the purpose of command line arguments? Give a real-world example of when they would be useful.

**Sample Answer:**
Command line arguments allow users to provide input to programs when they start execution, making programs more flexible and reusable. They're useful for specifying file names, configuration options, or parameters without modifying the source code. A real-world example is the `gcc` compiler: `gcc -o program source.c` where `-o program` specifies the output file name and `source.c` is the input file. This allows the same compiler to work with different files and options.

---

## Section C: Code Analysis and Completion (20 marks)
*Complete or fix the code. 5 marks each.*

**Question 24:** Complete this function that counts words in a string:
```c
int count_words(char str[]) {
    int count = 0;
    int in_word = 0;
    
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] != ' ' && str[i] != '\t') {
            if (!in_word) {
                count++;
                in_word = 1;
            }
        } else {
            in_word = 0;
        }
    }
    return count;
}
```

**Question 25:** Fix the memory management issues in this code:
```c
char* create_greeting(char *name) {
    char greeting[100];
    sprintf(greeting, "Hello, %s!", name);
    return greeting;  // Problem here!
}
```

**Sample Answer:**
```c
char* create_greeting(char *name) {
    char *greeting = malloc(100 * sizeof(char));
    if (greeting == NULL) {
        return NULL;  // Handle malloc failure
    }
    sprintf(greeting, "Hello, %s!", name);
    return greeting;
}
```

**Question 26:** Complete this command line argument processor:
```c
int main(int argc, char *argv[]) {
    if (argc != 2) {
        printf("Usage: %s <number>\n", argv[0]);
        return 1;
    }
    
    int num = atoi(argv[1]);
    printf("Square of %d is %d\n", num, num * num);
    return 0;
}
```

**Question 27:** Complete this pointer swap function:
```c
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
```

---

## Section D: Programming Problems (20 marks)

**Question 28: String Processor (10 marks)**
Write a complete program that:
- Prompts the user for a sentence (use `fgets` for safety)
- Implements a function `void reverse_string(char str[])` that reverses the string in place
- Implements a function `int find_char(char str[], char ch)` that returns the position of a character (or -1 if not found)
- In main: displays the original string, reverses it, shows the reversed string, and finds the position of 'a'

**Sample Answer:**
```c
#include <stdio.h>
#include <string.h>

void reverse_string(char str[]) {
    int len = strlen(str);
    for (int i = 0; i < len / 2; i++) {
        char temp = str[i];
        str[i] = str[len - 1 - i];
        str[len - 1 - i] = temp;
    }
}

int find_char(char str[], char ch) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ch) {
            return i;
        }
    }
    return -1;
}

int main() {
    char sentence[100];
    
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);
    
    // Remove newline character
    sentence[strcspn(sentence, "\n")] = '\0';
    
    printf("Original: %s\n", sentence);
    
    reverse_string(sentence);
    printf("Reversed: %s\n", sentence);
    
    int pos = find_char(sentence, 'a');
    if (pos != -1) {
        printf("'a' found at position %d\n", pos);
    } else {
        printf("'a' not found\n");
    }
    
    return 0;
}
```

**Question 29: Dynamic Array Manager (10 marks)**
Write a program that:
- Prompts the user for how many integers they want to store
- Dynamically allocates memory for that many integers
- Reads the integers from the user
- Calculates and displays the sum
- Properly frees the allocated memory

Include proper error checking for `malloc()` failure.

**Sample Answer:**
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n;
    int *numbers;
    int sum = 0;
    
    printf("How many integers do you want to store? ");
    scanf("%d", &n);
    
    if (n <= 0) {
        printf("Invalid number of elements\n");
        return 1;
    }
    
    numbers = malloc(n * sizeof(int));
    if (numbers == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }
    
    printf("Enter %d integers:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &numbers[i]);
        sum += numbers[i];
    }
    
    printf("Sum of all numbers: %d\n", sum);
    
    free(numbers);  // Free allocated memory
    return 0;
}
```

---

## Answer Template

**Section B - Short Answers:**

**Q17:** ________________________________________________
________________________________________________________

**Q18:** ________________________________________________
________________________________________________________

**Q19:** ________________________________________________
________________________________________________________

**Q20:** ________________________________________________
________________________________________________________

**Q21:** ________________________________________________
________________________________________________________

**Q22:** ________________________________________________
________________________________________________________

**Q23:** ________________________________________________
________________________________________________________

**Section C - Code Completion:**

**Q24:**
```c
int count_words(char str[]) {
    int count = 0;
    int in_word = 0;
    
    for (int i = 0; str[i] != ______; i++) {
        if (str[i] != ' ' && str[i] != '\t') {
            if (______) {
                count++;
                in_word = ______;
            }
        } else {
            in_word = ______;
        }
    }
    return count;
}
```

**Q25:**
```c
// Write corrected version here




```

**Q26:**
```c
int main(int argc, char *argv[]) {
    if (argc != ______) {
        printf("Usage: %s <number>\n", ______);
        return 1;
    }
    
    int num = ______(argv[1]);
    printf("Square of %d is %d\n", num, num * num);
    return 0;
}
```

**Q27:**
```c
void swap(int *a, int *b) {
    int temp = ______;
    *a = ______;
    *b = ______;
}
```

**Section D - Programming Problems:**

**Q28: String Processor**
```c
// Write your complete program here




```

**Q29: Dynamic Array Manager**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (32 marks):** 2 marks per correct answer
- **Short Answer (28 marks):** 4 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (20 marks):** 10 marks each
  - Correct function implementation: 6 marks
  - Proper memory/string handling: 3 marks
  - Style and error checking: 1 mark

**Key Success Factors:**
- Understand pointer dereferencing vs address-of operators
- Remember string null termination
- Check `malloc()` return values
- Free all allocated memory
- Handle command line arguments correctly
- Use safe string functions when possible
