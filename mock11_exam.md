# Mock Exam 11: Programming Fundamentals and Problem Solving
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 45;
int y = 11;
printf("%d", x / y);
```
a) 4.09
b) 4
c) 5
d) Error

**Question 2:** Which data type is best for storing a person's height in meters?
a) `int`
b) `double`
c) `char`
d) `float`

**Question 3:** What will this code print?
```c
int i = 4;
while (i > 0) {
    printf("%d ", i);
    i--;
}
```
a) 4 3 2 1
b) 4 3 2 1 0
c) 3 2 1 0
d) 4 3 2

**Question 4:** Which operator is used for logical AND?
a) `&`
b) `&&`
c) `|`
d) `||`

**Question 5:** What will this code print?
```c
int x = 14;
int y = 28;
printf("%d", (x > y) ? x : y);
```
a) 14
b) 28
c) 42
d) Error

**Question 6:** What does `strncpy()` do?
a) Compares two strings
b) Copies one string to another with size limit
c) Concatenates two strings
d) Finds the length of a string

**Question 7:** What will this code print?
```c
char str[] = "Software";
printf("%c", str[5]);
```
a) S
b) o
c) f
d) w

**Question 8:** What is the purpose of the `&` operator with variables?
a) Gets the value of a variable
b) Gets the address of a variable
c) Multiplies two variables
d) Compares two variables

**Question 9:** What happens if you dereference a NULL pointer?
a) Nothing
b) Compilation error
c) Runtime error (segmentation fault)
d) Returns 0

**Question 10:** Which function is used to resize dynamically allocated memory?
a) `malloc()`
b) `calloc()`
c) `realloc()`
d) `free()`

**Question 11:** What is the purpose of `#define` in C?
a) To include header files
b) To define constants
c) To create functions
d) To allocate memory

**Question 12:** What will this code print?
```c
int arr[10] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
printf("%d", arr[6]);
```
a) 1
b) 2
c) 6
d) 7

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

**Question 15:** What is the correct way to declare a pointer to a double?
a) `double pointer d;`
b) `double *d;`
c) `pointer double d;`
d) `double &d;`

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between `for` and `while` loops. When would you use each one?

**Question 17:** What is the purpose of the `break` statement in loops? Give an example of when you would use it.

**Question 18:** Explain what "dangling pointer" means. How can it be prevented?

**Question 19:** What is the difference between `strcpy()` and `strncpy()`? When would you use each one?

**Question 20:** Explain the concept of "pass by reference" using pointers. How does it differ from pass by value?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to find the maximum value in an array:
```c
int find_max(int array[], int size) {
    int max = array[0];
    for (int i = 1; i < ______; i++) {
        if (array[i] > max) {
            max = array[______];
        }
    }
    return ______;
}
```

**Question 22:** Fill in the blanks to create a function that checks if a string contains only letters:
```c
int is_letters_only(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (!((str[i] >= 'A' && str[i] <= 'Z') || (str[i] >= 'a' && str[i] <= 'z'))) {
            return ______;
        }
    }
    return ______;
}
```

**Question 23:** Complete this function to insert a node at the end of a linked list:
```c
struct node* insert_at_tail(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return head;
    
    new_node->data = data;
    new_node->next = NULL;
    
    if (head == NULL) {
        return ______;
    }
    
    struct node *current = head;
    while (current->next != NULL) {
        current = current->______;
    }
    
    current->next = new_node;
    return ______;
}
```

**Question 24:** Complete this function to count words in a string:
```c
int count_words(char str[]) {
    int count = 0;
    int in_word = 0;
    
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] != ' ' && str[i] != '\t' && str[i] != '\n') {
            if (!in_word) {
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

---

## Section D: Programming Problems (25 marks)

**Question 25: Grade Management System (15 marks)**
Write a complete program that:
- Defines a struct `student` with fields for name, id, and an array of grades
- Creates a dynamic array of students
- Allows user to add students and their grades
- Calculates and displays each student's average grade
- Finds and displays the student with the highest average
- Implements a function to sort students by average grade
- Properly manages memory allocation and deallocation

**Question 26: File Processing Tool (10 marks)**
Write a program that:
- Takes a filename as command line argument
- Reads the file and counts lines, words, and characters
- Implements a function to find the longest line in the file
- Implements a function to count occurrences of a specific word
- Displays comprehensive statistics about the file
- Handles file opening errors gracefully

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
int find_max(int array[], int size) {
    int max = array[0];
    for (int i = 1; i < ______; i++) {
        if (array[i] > max) {
            max = array[______];
        }
    }
    return ______;
}
```

**Q22:**
```c
int is_letters_only(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (!((str[i] >= 'A' && str[i] <= 'Z') || (str[i] >= 'a' && str[i] <= 'z'))) {
            return ______;
        }
    }
    return ______;
}
```

**Q23:**
```c
struct node* insert_at_tail(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return head;
    
    new_node->data = data;
    new_node->next = NULL;
    
    if (head == NULL) {
        return ______;
    }
    
    struct node *current = head;
    while (current->next != NULL) {
        current = current->______;
    }
    
    current->next = new_node;
    return ______;
}
```

**Q24:**
```c
int count_words(char str[]) {
    int count = 0;
    int in_word = 0;
    
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] != ' ' && str[i] != '\t' && str[i] != '\n') {
            if (!in_word) {
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

**Section D - Programming Problems:**

**Q25: Grade Management System**
```c
// Write your complete program here




```

**Q26: File Processing Tool**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Struct definition (3 marks), Dynamic array (4 marks), Functions (5 marks), Sorting (3 marks)
  - Q26: File handling (6 marks), Statistics (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
