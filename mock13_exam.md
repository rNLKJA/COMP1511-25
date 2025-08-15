# Mock Exam 13: Programming Fundamentals and Applications
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 55;
int y = 13;
printf("%d", x / y);
```
a) 4.23
b) 4
c) 5
d) Error

**Question 2:** Which data type is best for storing a person's salary?
a) `int`
b) `double`
c) `char`
d) `float`

**Question 3:** What will this code print?
```c
int i = 3;
do {
    printf("%d ", i * 2);
    i++;
} while (i <= 6);
```
a) 3 4 5 6
b) 6 8 10 12
c) 6 8 10
d) 3 4 5

**Question 4:** Which operator is used for logical NOT?
a) `!`
b) `~`
c) `-`
d) `^`

**Question 5:** What will this code print?
```c
int x = 24;
int y = 36;
printf("%d", (x > y) ? x : y);
```
a) 24
b) 36
c) 60
d) Error

**Question 6:** What does `strcat()` do?
a) Compares two strings
b) Copies one string to another
c) Concatenates two strings
d) Finds the length of a string

**Question 7:** What will this code print?
```c
char str[] = "Computer";
printf("%c", str[6]);
```
a) C
b) o
c) e
d) r

**Question 8:** What is the purpose of the `*` operator with pointers?
a) Gets the address of a variable
b) Gets the value a pointer points to
c) Creates a new pointer
d) Multiplies two values

**Question 9:** What happens if you call `free()` on a NULL pointer?
a) Nothing (safe to do)
b) Compilation error
c) Runtime error
d) Memory corruption

**Question 10:** Which function is used to free dynamically allocated memory?
a) `delete()`
b) `free()`
c) `release()`
d) `deallocate()`

**Question 11:** What is the purpose of `#ifndef` in header files?
a) To include files multiple times
b) To prevent multiple inclusions
c) To define constants
d) To create functions

**Question 12:** What will this code print?
```c
int arr[12] = {2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24};
printf("%d", arr[8]);
```
a) 2
b) 4
c) 16
d) 18

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

**Question 15:** What is the correct way to declare a pointer to a character?
a) `char pointer c;`
b) `char *c;`
c) `pointer char c;`
d) `char &c;`

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between `++i` and `i++`. Give an example where this difference matters.

**Question 17:** What are the three main parts of a `for` loop? Explain what each part does.

**Question 18:** Explain what "pass by value" means in C functions. How does this affect the original variables?

**Question 19:** What is a memory leak and how does it occur in C programs? How can it be prevented?

**Question 20:** Explain the difference between `char str[] = "Hello"` and `char *str = "Hello"`. Which one is modifiable?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to calculate the average of an array:
```c
double array_average(int array[], int size) {
    int sum = 0;
    for (int i = 0; i < ______; i++) {
        sum += array[______];
    }
    return (double)sum / ______;
}
```

**Question 22:** Fill in the blanks to create a function that checks if a string is a palindrome:
```c
int is_palindrome(char str[]) {
    int len = strlen(str);
    for (int i = 0; i < len / 2; i++) {
        if (str[i] != str[______ - 1 - ______]) {
            return 0;
        }
    }
    return 1;
}
```

**Question 23:** Complete this function to insert a node in sorted order in a linked list:
```c
struct node* insert_sorted(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return head;
    
    new_node->data = data;
    new_node->next = NULL;
    
    if (head == NULL || data < head->data) {
        new_node->next = head;
        return ______;
    }
    
    struct node *current = head;
    while (current->next != NULL && current->next->data < data) {
        current = current->______;
    }
    
    new_node->next = current->next;
    current->next = new_node;
    return ______;
}
```

**Question 24:** Complete this function to count occurrences of a character in a string:
```c
int count_char(char str[], char target) {
    int count = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ______) {
            count++;
        }
    }
    return ______;
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Student Database System (15 marks)**
Write a complete program that:
- Defines a struct `student` with fields for name, id, and grades
- Creates a dynamic array of students
- Allows user to add students and their grades
- Calculates and displays each student's average grade
- Finds and displays the student with the highest GPA
- Implements a function to search for a student by ID
- Properly manages memory allocation and deallocation

**Question 26: Command Line Calculator (10 marks)**
Write a program that:
- Takes three command line arguments: number1, operation, number2
- Supports operations: +, -, *, /
- Implements proper error handling for invalid operations and division by zero
- Displays the result with appropriate formatting
- Handles floating-point numbers

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
double array_average(int array[], int size) {
    int sum = 0;
    for (int i = 0; i < ______; i++) {
        sum += array[______];
    }
    return (double)sum / ______;
}
```

**Q22:**
```c
int is_palindrome(char str[]) {
    int len = strlen(str);
    for (int i = 0; i < len / 2; i++) {
        if (str[i] != str[______ - 1 - ______]) {
            return 0;
        }
    }
    return 1;
}
```

**Q23:**
```c
struct node* insert_sorted(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return head;
    
    new_node->data = data;
    new_node->next = NULL;
    
    if (head == NULL || data < head->data) {
        new_node->next = head;
        return ______;
    }
    
    struct node *current = head;
    while (current->next != NULL && current->next->data < data) {
        current = current->______;
    }
    
    new_node->next = current->next;
    current->next = new_node;
    return ______;
}
```

**Q24:**
```c
int count_char(char str[], char target) {
    int count = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ______) {
            count++;
        }
    }
    return ______;
}
```

**Section D - Programming Problems:**

**Q25: Student Database System**
```c
// Write your complete program here




```

**Q26: Command Line Calculator**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Struct definition (3 marks), Dynamic array (4 marks), Functions (5 marks), Search function (3 marks)
  - Q26: Command line args (4 marks), Operations (4 marks), Error handling (2 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
