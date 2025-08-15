# Mock Exam 5: Data Structures and Memory Management
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 15;
int y = 4;
printf("%d", x / y);
```
a) 3.75
b) 3
c) 4
d) Error

**Question 2:** Which data type is best for storing a person's age?
a) `double`
b) `int`
c) `char`
d) `float`

**Question 3:** What will this code print?
```c
for (int i = 0; i < 3; i++) {
    printf("%d ", i * 2);
}
```
a) 0 1 2
b) 0 2 4
c) 2 4 6
d) 1 2 3

**Question 4:** Which operator has the lowest precedence?
a) `+`
b) `*`
c) `=`
d) `()`

**Question 5:** What will this code print?
```c
int x = 5;
int y = 10;
printf("%d", (x > y) ? x : y);
```
a) 5
b) 10
c) 15
d) Error

**Question 6:** What does `strcat()` do?
a) Compares two strings
b) Copies one string to another
c) Concatenates two strings
d) Finds the length of a string

**Question 7:** What will this code print?
```c
char str[] = "Test";
printf("%c", str[2]);
```
a) T
b) e
c) s
d) t

**Question 8:** In a linked list, what does each node contain?
a) Only data
b) Only a pointer
c) Both data and a pointer
d) Neither data nor pointer

**Question 9:** What happens if you call `free()` on a NULL pointer?
a) Compilation error
b) Runtime error
c) Nothing (safe to do)
d) Memory corruption

**Question 10:** Which function is used to resize dynamically allocated memory?
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
int arr[4] = {1, 2, 3, 4};
printf("%d", arr[3]);
```
a) 1
b) 2
c) 3
d) 4

**Question 13:** Which loop type is best for counting from 1 to 10?
a) While loop
b) Do-while loop
c) For loop
d) All are equally good

**Question 14:** What does the `->` operator do?
a) Accesses struct members through a pointer
b) Accesses struct members directly
c) Creates a pointer
d) Dereferences a pointer

**Question 15:** What is the correct way to declare a constant integer?
a) `const int MAX = 100;`
b) `#define MAX 100`
c) `int const MAX = 100;`
d) All of the above

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between `while` and `do-while` loops. When would you use each one?

**Question 17:** What is the purpose of the `return` statement in a function? What happens if you don't include one?

**Question 18:** Explain what "dangling pointer" means. How can it be prevented?

**Question 19:** What is the difference between `strcpy()` and `strncpy()`? When would you use each one?

**Question 20:** Explain the concept of "pass by reference" using pointers. How does it differ from pass by value?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to check if a number is prime:
```c
int is_prime(int n) {
    if (n <= 1) return 0;
    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) {
            return ______;
        }
    }
    return ______;
}
```

**Question 22:** Fill in the blanks to create a function that finds the maximum value in a 2D array:
```c
int find_max_2d(int array[3][3]) {
    int max = array[0][0];
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (array[i][j] > max) {
                max = array[______][______];
            }
        }
    }
    return max;
}
```

**Question 23:** Complete this function to insert a node at the beginning of a linked list:
```c
struct node* insert_at_head(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return head;
    
    new_node->data = data;
    new_node->next = ______;
    return ______;
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

**Question 25: Linked List Operations (15 marks)**
Write a complete program that:
- Defines a linked list node structure
- Implements functions to insert at head, insert at tail, and delete by value
- Implements a function to print the entire list
- Implements a function to find the sum of all values in the list
- Properly frees all allocated memory

**Question 26: String Manipulation Tool (10 marks)**
Write a program that:
- Takes a string as command line argument
- Implements a function to count characters, words, and lines
- Implements a function to check if the string is a palindrome
- Displays all statistics about the string

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
int is_prime(int n) {
    if (n <= 1) return 0;
    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) {
            return ______;
        }
    }
    return ______;
}
```

**Q22:**
```c
int find_max_2d(int array[3][3]) {
    int max = array[0][0];
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (array[i][j] > max) {
                max = array[______][______];
            }
        }
    }
    return max;
}
```

**Q23:**
```c
struct node* insert_at_head(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return head;
    
    new_node->data = data;
    new_node->next = ______;
    return ______;
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

**Q25: Linked List Operations**
```c
// Write your complete program here




```

**Q26: String Manipulation Tool**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Node structure (3 marks), Insert functions (6 marks), Delete function (3 marks), Memory management (3 marks)
  - Q26: String analysis (6 marks), Palindrome check (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
