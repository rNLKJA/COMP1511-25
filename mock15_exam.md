# Mock Exam 15: Final Comprehensive Programming Assessment
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 65;
int y = 15;
printf("%d", x / y);
```
a) 4.33
b) 4
c) 5
d) Error

**Question 2:** Which data type is best for storing a person's age in months?
a) `int`
b) `double`
c) `char`
d) `long`

**Question 3:** What will this code print?
```c
for (int i = 0; i < 5; i++) {
    printf("%d ", i * 4);
}
```
a) 0 1 2 3 4
b) 0 4 8 12 16
c) 4 8 12 16 20
d) 1 2 3 4 5

**Question 4:** Which operator has the highest precedence?
a) `+`
b) `*`
c) `()`
d) `=`

**Question 5:** What will this code print?
```c
int x = 35;
int y = 45;
printf("%d", (x < y) ? x : y);
```
a) 35
b) 45
c) 80
d) Error

**Question 6:** What does `strcmp()` return if the first string is greater than the second?
a) 0
b) 1
c) -1
d) The length difference

**Question 7:** What will this code print?
```c
char str[] = "Network";
printf("%c", str[4]);
```
a) N
b) e
c) t
d) w

**Question 8:** What is the purpose of the `*` operator with pointers?
a) Gets the address of a variable
b) Gets the value a pointer points to
c) Creates a new pointer
d) Multiplies two values

**Question 9:** What happens if you try to access an array index that is out of bounds?
a) Compilation error
b) Runtime error (undefined behavior)
c) Returns 0
d) Returns NULL

**Question 10:** Which function is used to free dynamically allocated memory?
a) `delete()`
b) `free()`
c) `release()`
d) `deallocate()`

**Question 11:** What is the purpose of `#define` in C?
a) To include header files
b) To define constants
c) To create functions
d) To allocate memory

**Question 12:** What will this code print?
```c
int arr[14] = {0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26};
printf("%d", arr[10]);
```
a) 0
b) 2
c) 18
d) 20

**Question 13:** Which loop type executes the body at least once?
a) For loop
b) While loop
c) Do-while loop
d) All loops

**Question 14:** What does the `->` operator do?
a) Accesses struct members through a pointer
b) Accesses struct members directly
c) Creates a pointer
d) Dereferences a pointer

**Question 15:** What is the correct way to declare a pointer to a character?
a) `char pointer c;`
b) `char *c;`
c) `pointer char c;`
d) `char &c;`

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between `for` and `while` loops. When would you use each one?

**Question 17:** What is the purpose of the `break` statement in loops? Give an example of when you would use it.

**Question 18:** Explain what "memory leak" means and how it can be prevented in C programs.

**Question 19:** What is the difference between `malloc()` and `calloc()`? When would you use each one?

**Question 20:** Explain the concept of "array decay" in C. How does it affect function parameters?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to calculate the factorial of a number:
```c
int factorial(int n) {
    if (n <= 1) {
        return ______;
    }
    return n * factorial(______);
}
```

**Question 22:** Fill in the blanks to create a function that reverses an array:
```c
void reverse_array(int array[], int size) {
    for (int i = 0; i < size / 2; i++) {
        int temp = array[i];
        array[i] = array[______];
        array[______] = temp;
    }
}
```

**Question 23:** Complete this function to find the length of a linked list:
```c
int list_length(struct node *head) {
    int count = 0;
    struct node *current = head;
    while (current != NULL) {
        count++;
        current = current->______;
    }
    return ______;
}
```

**Question 24:** Complete this function to safely copy a string:
```c
void safe_strcpy(char dest[], char src[], int max_len) {
    int i = 0;
    while (src[i] != '\0' && i < max_len - 1) {
        dest[i] = src[i];
        i++;
    }
    dest[______] = '\0';
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Advanced Linked List Manager (15 marks)**
Write a complete program that:
- Defines a linked list node structure
- Implements functions to insert at head, insert at tail, and delete by value
- Implements a function to find the middle element using two-pointer technique
- Implements a function to detect if the list has a cycle
- Implements a function to reverse the list in-place
- Implements a function to merge two sorted linked lists
- Properly frees all allocated memory

**Question 26: Multi-file Project System (10 marks)**
Create a simple library management system with:
- Header file (`library.h`) with struct definitions and function prototypes
- Implementation file (`library.c`) with function definitions
- Main file (`main.c`) that demonstrates the library functions
- Functions for adding books, finding books, and displaying all books
- Proper error handling and memory management
- Support for multiple book categories

---

## Answer Template

**Section B - Short Answers:**

**Q16:** ________________________________________________
________________________________________________________

**Q17:** ________________________________________________
________________________________________________________

**Q18:** ________________________________________________
________________________________________________________

**Q19:** ________________________________________________
________________________________________________________

**Q20:** ________________________________________________
________________________________________________________

**Section C - Code Completion:**

**Q21:**
```c
int factorial(int n) {
    if (n <= 1) {
        return ______;
    }
    return n * factorial(______);
}
```

**Q22:**
```c
void reverse_array(int array[], int size) {
    for (int i = 0; i < size / 2; i++) {
        int temp = array[i];
        array[i] = array[______];
        array[______] = temp;
    }
}
```

**Q23:**
```c
int list_length(struct node *head) {
    int count = 0;
    struct node *current = head;
    while (current != NULL) {
        count++;
        current = current->______;
    }
    return ______;
}
```

**Q24:**
```c
void safe_strcpy(char dest[], char src[], int max_len) {
    int i = 0;
    while (src[i] != '\0' && i < max_len - 1) {
        dest[i] = src[i];
        i++;
    }
    dest[______] = '\0';
}
```

**Section D - Programming Problems:**

**Q25: Advanced Linked List Manager**
```c
// Write your complete program here




```

**Q26: Multi-file Project System**
```c
// Write your complete program here
// Include library.h, library.c, and main.c




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Node structure (2 marks), Basic operations (6 marks), Advanced algorithms (5 marks), Memory management (2 marks)
  - Q26: Header file (2 marks), Implementation (4 marks), Main program (3 marks), Error handling (1 mark)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
