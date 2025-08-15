# Mock Exam 6: Advanced Programming Techniques
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 20;
int y = 6;
printf("%d", x % y);
```
a) 2
b) 3
c) 4
d) Error

**Question 2:** Which data type is best for storing a person's weight in kilograms?
a) `int`
b) `double`
c) `char`
d) `long`

**Question 3:** What will this code print?
```c
int i = 5;
while (i > 0) {
    printf("%d ", i);
    i--;
}
```
a) 5 4 3 2 1
b) 5 4 3 2 1 0
c) 4 3 2 1 0
d) 5 4 3 2

**Question 4:** Which operator is used for logical OR?
a) `&`
b) `&&`
c) `|`
d) `||`

**Question 5:** What will this code print?
```c
int x = 8;
int y = 12;
printf("%d", (x < y) ? x : y);
```
a) 8
b) 12
c) 20
d) Error

**Question 6:** What does `strlen()` return?
a) The number of characters in a string (excluding '\0')
b) The number of characters in a string (including '\0')
c) The size of the string array
d) The address of the string

**Question 7:** What will this code print?
```c
char str[] = "Programming";
printf("%c", str[4]);
```
a) P
b) r
c) g
d) a

**Question 8:** What is the purpose of the `->` operator?
a) To access struct members through a pointer
b) To create a pointer
c) To dereference a pointer
d) To allocate memory

**Question 9:** What happens if you try to access an array index that is out of bounds?
a) Compilation error
b) Runtime error (undefined behavior)
c) Returns 0
d) Returns NULL

**Question 10:** Which function is used to allocate memory and initialize it to zero?
a) `malloc()`
b) `calloc()`
c) `realloc()`
d) `free()`

**Question 11:** What is the purpose of header guards (`#ifndef`)?
a) To include files multiple times
b) To prevent multiple inclusions
c) To define constants
d) To create functions

**Question 12:** What will this code print?
```c
int arr[5] = {10, 20, 30, 40, 50};
printf("%d", arr[1]);
```
a) 10
b) 20
c) 30
d) 40

**Question 13:** Which loop type checks the condition before executing the body?
a) Do-while loop
b) While loop
c) For loop
d) All loops

**Question 14:** What does the `*` operator do when used with a pointer?
a) Gets the address of a variable
b) Gets the value a pointer points to
c) Creates a new pointer
d) Multiplies two values

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

**Question 21:** Complete this function to calculate the sum of an array:
```c
int array_sum(int array[], int size) {
    int sum = 0;
    for (int i = 0; i < ______; i++) {
        sum += array[______];
    }
    return ______;
}
```

**Question 22:** Fill in the blanks to create a function that checks if a string contains only digits:
```c
int is_digits_only(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] < '0' || str[i] > '9') {
            return ______;
        }
    }
    return ______;
}
```

**Question 23:** Complete this function to delete a node from a linked list:
```c
struct node* delete_node(struct node *head, int value) {
    if (head == NULL) return NULL;
    
    if (head->data == value) {
        struct node *temp = head;
        head = head->next;
        free(______);
        return head;
    }
    
    struct node *current = head;
    while (current->next != NULL && current->next->data != value) {
        current = current->next;
    }
    
    if (current->next != NULL) {
        struct node *temp = current->next;
        current->next = current->next->next;
        free(______);
    }
    
    return head;
}
```

**Question 24:** Complete this function to find the middle element of a linked list:
```c
struct node* find_middle(struct node *head) {
    if (head == NULL) return NULL;
    
    struct node *slow = head;
    struct node *fast = head;
    
    while (fast != NULL && fast->next != NULL) {
        slow = slow->______;
        fast = fast->next->______;
    }
    
    return slow;
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Multi-file Project (15 marks)**
Create a simple calculator system with:
- Header file (`calculator.h`) with function prototypes
- Implementation file (`calculator.c`) with function definitions
- Main file (`main.c`) that uses the calculator functions
- Functions for addition, subtraction, multiplication, and division
- Proper error handling for division by zero

**Question 26: Dynamic String Processor (10 marks)**
Write a program that:
- Dynamically allocates memory for strings based on user input
- Implements functions to concatenate, reverse, and compare strings
- Properly manages memory allocation and deallocation
- Handles memory allocation failures gracefully

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
int array_sum(int array[], int size) {
    int sum = 0;
    for (int i = 0; i < ______; i++) {
        sum += array[______];
    }
    return ______;
}
```

**Q22:**
```c
int is_digits_only(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] < '0' || str[i] > '9') {
            return ______;
        }
    }
    return ______;
}
```

**Q23:**
```c
struct node* delete_node(struct node *head, int value) {
    if (head == NULL) return NULL;
    
    if (head->data == value) {
        struct node *temp = head;
        head = head->next;
        free(______);
        return head;
    }
    
    struct node *current = head;
    while (current->next != NULL && current->next->data != value) {
        current = current->next;
    }
    
    if (current->next != NULL) {
        struct node *temp = current->next;
        current->next = current->next->next;
        free(______);
    }
    
    return head;
}
```

**Q24:**
```c
struct node* find_middle(struct node *head) {
    if (head == NULL) return NULL;
    
    struct node *slow = head;
    struct node *fast = head;
    
    while (fast != NULL && fast->next != NULL) {
        slow = slow->______;
        fast = fast->next->______;
    }
    
    return slow;
}
```

**Section D - Programming Problems:**

**Q25: Multi-file Project**
```c
// Write your complete program here
// Include calculator.h, calculator.c, and main.c




```

**Q26: Dynamic String Processor**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Header file (3 marks), Implementation (6 marks), Main program (4 marks), Error handling (2 marks)
  - Q26: Dynamic allocation (6 marks), String functions (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
