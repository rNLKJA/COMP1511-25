# Mock Exam 12: Advanced Programming and Data Structures
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 50;
int y = 12;
printf("%d", x % y);
```
a) 2
b) 4
c) 6
d) Error

**Question 2:** Which data type is best for storing a person's phone number?
a) `int`
b) `long`
c) `char`
d) `double`

**Question 3:** What will this code print?
```c
for (int i = 1; i <= 5; i++) {
    printf("%d ", i * i);
}
```
a) 1 2 3 4 5
b) 1 4 9 16 25
c) 2 4 6 8 10
d) 1 3 5 7 9

**Question 4:** Which operator has the lowest precedence?
a) `+`
b) `*`
c) `=`
d) `()`

**Question 5:** What will this code print?
```c
int x = 16;
int y = 32;
printf("%d", (x < y) ? x : y);
```
a) 16
b) 32
c) 48
d) Error

**Question 6:** What does `strcmp()` return if two strings are equal?
a) 1
b) 0
c) -1
d) The length of the strings

**Question 7:** What will this code print?
```c
char str[] = "Internet";
printf("%c", str[4]);
```
a) I
b) n
c) e
d) r

**Question 8:** What is the purpose of the `*` operator with pointers?
a) Gets the address of a variable
b) Gets the value a pointer points to
c) Creates a new pointer
d) Multiplies two values

**Question 9:** What happens if you try to access memory after calling `free()`?
a) Nothing
b) Compilation error
c) Runtime error (undefined behavior)
d) Returns 0

**Question 10:** Which function is used to allocate memory and initialize it to zero?
a) `malloc()`
b) `calloc()`
c) `realloc()`
d) `free()`

**Question 11:** What is the purpose of `#include` in C?
a) To define constants
b) To include header files
c) To create functions
d) To allocate memory

**Question 12:** What will this code print?
```c
int arr[11] = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
printf("%d", arr[7]);
```
a) 0
b) 1
c) 6
d) 7

**Question 13:** Which loop type is best for processing input until a sentinel value?
a) For loop
b) While loop
c) Do-while loop
d) All loops

**Question 14:** What does the `->` operator do?
a) Accesses struct members through a pointer
b) Accesses struct members directly
c) Creates a pointer
d) Dereferences a pointer

**Question 15:** What is the correct way to declare a pointer to an integer?
a) `int pointer x;`
b) `int *x;`
c) `pointer int x;`
d) `int &x;`

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between stack and heap memory. Give one advantage and one disadvantage of each.

**Question 17:** What is the purpose of function prototypes in header files? Why can't we put function definitions in header files?

**Question 18:** Explain what "memory leak" means and how it occurs in C programs.

**Question 19:** What is the difference between `strcpy()` and `strncpy()`? When would you use each one?

**Question 20:** Explain the concept of "pass by reference" using pointers. How does it differ from pass by value?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to check if a number is odd:
```c
int is_odd(int n) {
    return (n % 2 == ______);
}
```

**Question 22:** Fill in the blanks to create a function that finds the sum of a 2D array:
```c
int sum_2d_array(int array[3][3]) {
    int sum = 0;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            sum += array[______][______];
        }
    }
    return sum;
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

**Question 24:** Complete this function to convert a string to uppercase:
```c
void to_uppercase(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'a' && str[i] <= 'z') {
            str[i] = str[i] - ______;
        }
    }
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Advanced Linked List Operations (15 marks)**
Write a complete program that:
- Defines a linked list node structure
- Implements functions to insert nodes in sorted order
- Implements a function to remove duplicates from a sorted list
- Implements a function to find the nth node from the end
- Implements a function to check if the list is palindrome
- Properly frees all allocated memory

**Question 26: Matrix Operations Calculator (10 marks)**
Write a program that:
- Takes matrix dimensions and elements as command line arguments
- Implements functions to add two matrices
- Implements a function to find the transpose of a matrix
- Implements a function to find the maximum element in a matrix
- Displays the results with proper formatting
- Handles invalid input gracefully

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
int is_odd(int n) {
    return (n % 2 == ______);
}
```

**Q22:**
```c
int sum_2d_array(int array[3][3]) {
    int sum = 0;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            sum += array[______][______];
        }
    }
    return sum;
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
void to_uppercase(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'a' && str[i] <= 'z') {
            str[i] = str[i] - ______;
        }
    }
}
```

**Section D - Programming Problems:**

**Q25: Advanced Linked List Operations**
```c
// Write your complete program here




```

**Q26: Matrix Operations Calculator**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Node structure (2 marks), Sorted insertion (4 marks), Remove duplicates (3 marks), Nth node (3 marks), Palindrome check (3 marks)
  - Q26: Matrix operations (6 marks), Input handling (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
