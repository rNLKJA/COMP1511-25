# Mock Exam 9: Advanced Data Structures and Algorithms
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 35;
int y = 9;
printf("%d", x / y);
```
a) 3.89
b) 3
c) 4
d) Error

**Question 2:** Which data type is best for storing a person's GPA?
a) `int`
b) `double`
c) `char`
d) `float`

**Question 3:** What will this code print?
```c
int i = 2;
while (i <= 8) {
    printf("%d ", i * 2);
    i += 2;
}
```
a) 2 4 6 8
b) 4 8 12 16
c) 2 4 6 8 10
d) 4 6 8 10 12

**Question 4:** Which operator has the lowest precedence?
a) `+`
b) `*`
c) `=`
d) `()`

**Question 5:** What will this code print?
```c
int x = 20;
int y = 25;
printf("%d", (x > y) ? x : y);
```
a) 20
b) 25
c) 45
d) Error

**Question 6:** What does `strcmp()` return if the first string is greater than the second?
a) 0
b) 1
c) -1
d) The length difference

**Question 7:** What will this code print?
```c
char str[] = "Database";
printf("%c", str[4]);
```
a) D
b) a
c) t
d) a

**Question 8:** What is the purpose of the `&` operator with variables?
a) Gets the value of a variable
b) Gets the address of a variable
c) Multiplies two variables
d) Compares two variables

**Question 9:** What happens if you call `free()` twice on the same pointer?
a) Nothing
b) Compilation error
c) Runtime error (undefined behavior)
d) Memory corruption

**Question 10:** Which function is used to allocate memory and initialize it to zero?
a) `malloc()`
b) `calloc()`
c) `realloc()`
d) `free()`

**Question 11:** What is the purpose of `#ifndef` in header files?
a) To include files multiple times
b) To prevent multiple inclusions
c) To define constants
d) To create functions

**Question 12:** What will this code print?
```c
int arr[8] = {1, 3, 5, 7, 9, 11, 13, 15};
printf("%d", arr[4]);
```
a) 1
b) 3
c) 5
d) 9

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

**Question 15:** What is the correct way to declare a pointer to an integer?
a) `int pointer x;`
b) `int *x;`
c) `pointer int x;`
d) `int &x;`

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between `while` and `do-while` loops. When would you use each one?

**Question 17:** What is the purpose of the `return` statement in a function? What happens if you don't include one?

**Question 18:** Explain what "memory leak" means and how it can be prevented in C programs.

**Question 19:** What is the difference between `malloc()` and `calloc()`? When would you use each one?

**Question 20:** Explain the concept of "array decay" in C. How does it affect function parameters?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to check if a number is even:
```c
int is_even(int n) {
    return (n % 2 == ______);
}
```

**Question 22:** Fill in the blanks to create a function that finds the minimum value in a 2D array:
```c
int find_min_2d(int array[3][3]) {
    int min = array[0][0];
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (array[i][j] < min) {
                min = array[______][______];
            }
        }
    }
    return min;
}
```

**Question 23:** Complete this function to count nodes in a linked list:
```c
int count_nodes(struct node *head) {
    int count = 0;
    struct node *current = head;
    while (current != NULL) {
        count++;
        current = current->______;
    }
    return ______;
}
```

**Question 24:** Complete this function to convert a string to lowercase:
```c
void to_lowercase(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'A' && str[i] <= 'Z') {
            str[i] = str[i] + ______;
        }
    }
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Linked List Operations with Sorting (15 marks)**
Write a complete program that:
- Defines a linked list node structure
- Implements functions to insert nodes in sorted order
- Implements a function to merge two sorted linked lists
- Implements a function to remove duplicates from a sorted list
- Implements a function to find the nth node from the end
- Properly frees all allocated memory

**Question 26: Advanced String Processor (10 marks)**
Write a program that:
- Takes a string as command line argument
- Implements a function to check if a string contains only letters
- Implements a function to find the longest word in a string
- Implements a function to capitalize the first letter of each word
- Displays the processed string and statistics

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
int is_even(int n) {
    return (n % 2 == ______);
}
```

**Q22:**
```c
int find_min_2d(int array[3][3]) {
    int min = array[0][0];
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (array[i][j] < min) {
                min = array[______][______];
            }
        }
    }
    return min;
}
```

**Q23:**
```c
int count_nodes(struct node *head) {
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
void to_lowercase(char str[]) {
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'A' && str[i] <= 'Z') {
            str[i] = str[i] + ______;
        }
    }
}
```

**Section D - Programming Problems:**

**Q25: Linked List Operations with Sorting**
```c
// Write your complete program here




```

**Q26: Advanced String Processor**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Node structure (2 marks), Sorted insertion (4 marks), Merge function (4 marks), Remove duplicates (3 marks), Nth node (2 marks)
  - Q26: String validation (4 marks), Word processing (4 marks), Capitalization (2 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
