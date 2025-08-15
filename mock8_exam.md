# Mock Exam 8: Comprehensive Programming Assessment
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 30;
int y = 8;
printf("%d", x % y);
```
a) 3
b) 6
c) 7
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
    printf("%d ", i);
    i++;
} while (i <= 6);
```
a) 3 4 5 6
b) 3 4 5 6 7
c) 4 5 6
d) 3 4 5

**Question 4:** Which operator is used for logical NOT?
a) `!`
b) `~`
c) `-`
d) `^`

**Question 5:** What will this code print?
```c
int x = 12;
int y = 18;
printf("%d", (x < y) ? x : y);
```
a) 12
b) 18
c) 30
d) Error

**Question 6:** What does `strcat()` do?
a) Compares two strings
b) Copies one string to another
c) Concatenates two strings
d) Finds the length of a string

**Question 7:** What will this code print?
```c
char str[] = "Algorithm";
printf("%c", str[5]);
```
a) A
b) l
c) g
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
int arr[7] = {2, 4, 6, 8, 10, 12, 14};
printf("%d", arr[3]);
```
a) 2
b) 4
c) 6
d) 8

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

**Question 15:** What is the correct way to declare a pointer to a double?
a) `double pointer d;`
b) `double *d;`
c) `pointer double d;`
d) `double &d;`

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between stack and heap memory. Give one advantage and one disadvantage of each.

**Question 17:** What is the purpose of function prototypes in header files? Why can't we put function definitions in header files?

**Question 18:** Explain what "dangling pointer" means. How can it be prevented?

**Question 19:** What is the difference between `strcpy()` and `strncpy()`? When would you use each one?

**Question 20:** Explain the concept of "pass by reference" using pointers. How does it differ from pass by value?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to find the second largest value in an array:
```c
int find_second_largest(int array[], int size) {
    if (size < 2) return -1;
    
    int largest = array[0];
    int second_largest = array[1];
    
    if (largest < second_largest) {
        int temp = largest;
        largest = second_largest;
        second_largest = temp;
    }
    
    for (int i = 2; i < ______; i++) {
        if (array[i] > largest) {
            second_largest = largest;
            largest = array[______];
        } else if (array[i] > second_largest && array[i] != largest) {
            second_largest = array[______];
        }
    }
    return second_largest;
}
```

**Question 22:** Fill in the blanks to create a function that removes spaces from a string:
```c
void remove_spaces(char str[]) {
    int j = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] != ' ') {
            str[j] = str[______];
            j++;
        }
    }
    str[______] = '\0';
}
```

**Question 23:** Complete this function to reverse a linked list:
```c
struct node* reverse_list(struct node *head) {
    struct node *prev = NULL;
    struct node *current = head;
    struct node *next = NULL;
    
    while (current != NULL) {
        next = current->______;
        current->next = ______;
        prev = current;
        current = next;
    }
    
    return ______;
}
```

**Question 24:** Complete this function to check if a linked list has a cycle:
```c
int has_cycle(struct node *head) {
    if (head == NULL) return 0;
    
    struct node *slow = head;
    struct node *fast = head;
    
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;
        fast = fast->next->______;
        
        if (slow == fast) {
            return ______;
        }
    }
    return 0;
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Dynamic Array with Sorting (15 marks)**
Write a complete program that:
- Creates a dynamic array that can grow as needed
- Allows user to add integers to the array
- Implements a function to sort the array in ascending order
- Implements a function to remove duplicates from the array
- Displays the array contents after each operation
- Properly manages memory allocation and deallocation

**Question 26: String Analysis Tool (10 marks)**
Write a program that:
- Takes a string as command line argument
- Implements functions to count vowels, consonants, and digits
- Implements a function to find the most frequent character
- Displays detailed statistics about the string
- Handles edge cases like empty strings

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
int find_second_largest(int array[], int size) {
    if (size < 2) return -1;
    
    int largest = array[0];
    int second_largest = array[1];
    
    if (largest < second_largest) {
        int temp = largest;
        largest = second_largest;
        second_largest = temp;
    }
    
    for (int i = 2; i < ______; i++) {
        if (array[i] > largest) {
            second_largest = largest;
            largest = array[______];
        } else if (array[i] > second_largest && array[i] != largest) {
            second_largest = array[______];
        }
    }
    return second_largest;
}
```

**Q22:**
```c
void remove_spaces(char str[]) {
    int j = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] != ' ') {
            str[j] = str[______];
            j++;
        }
    }
    str[______] = '\0';
}
```

**Q23:**
```c
struct node* reverse_list(struct node *head) {
    struct node *prev = NULL;
    struct node *current = head;
    struct node *next = NULL;
    
    while (current != NULL) {
        next = current->______;
        current->next = ______;
        prev = current;
        current = next;
    }
    
    return ______;
}
```

**Q24:**
```c
int has_cycle(struct node *head) {
    if (head == NULL) return 0;
    
    struct node *slow = head;
    struct node *fast = head;
    
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;
        fast = fast->next->______;
        
        if (slow == fast) {
            return ______;
        }
    }
    return 0;
}
```

**Section D - Programming Problems:**

**Q25: Dynamic Array with Sorting**
```c
// Write your complete program here




```

**Q26: String Analysis Tool**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Dynamic array (6 marks), Sorting (4 marks), Duplicate removal (3 marks), Memory management (2 marks)
  - Q26: String analysis (6 marks), Character counting (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
