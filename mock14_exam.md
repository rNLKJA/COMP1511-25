# Mock Exam 14: Data Structures and Memory Management
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 60;
int y = 14;
printf("%d", x % y);
```
a) 2
b) 4
c) 6
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
    printf("%d ", i * 3);
    i += 2;
}
```
a) 2 4 6 8
b) 6 12 18 24
c) 6 8 10 12
d) 2 3 4 5

**Question 4:** Which operator has the highest precedence?
a) `+`
b) `*`
c) `()`
d) `=`

**Question 5:** What will this code print?
```c
int x = 30;
int y = 40;
printf("%d", (x < y) ? x : y);
```
a) 30
b) 40
c) 70
d) Error

**Question 6:** What does `strlen()` return?
a) The number of characters in a string (excluding '\0')
b) The number of characters in a string (including '\0')
c) The size of the string array
d) The address of the string

**Question 7:** What will this code print?
```c
char str[] = "Database";
printf("%c", str[5]);
```
a) D
b) a
c) b
d) s

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

**Question 10:** Which function is used to resize dynamically allocated memory?
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
int arr[13] = {1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25};
printf("%d", arr[9]);
```
a) 1
b) 3
c) 17
d) 19

**Question 13:** Which loop type checks the condition before executing the body?
a) Do-while loop
b) While loop
c) For loop
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

**Question 16:** Explain the difference between `while` and `do-while` loops. When would you use each one?

**Question 17:** What is the purpose of the `return` statement in a function? What happens if you don't include one?

**Question 18:** Explain what "dangling pointer" means. How can it be prevented?

**Question 19:** What is the difference between `malloc()` and `calloc()`? When would you use each one?

**Question 20:** Explain the concept of "array decay" in C. How does it affect function parameters?

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

**Question 25: Dynamic Array with Sorting (15 marks)**
Write a complete program that:
- Creates a dynamic array that can grow as needed
- Allows user to add integers to the array
- Implements a function to sort the array in ascending order
- Implements a function to remove duplicates from the array
- Implements a function to find the second largest element
- Displays the array contents after each operation
- Properly manages memory allocation and deallocation

**Question 26: String Analysis Tool (10 marks)**
Write a program that:
- Takes a string as command line argument
- Implements functions to count vowels, consonants, and digits
- Implements a function to find the most frequent character
- Implements a function to check if the string contains only letters
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
  - Q25: Dynamic array (6 marks), Sorting (4 marks), Remove duplicates (3 marks), Second largest (2 marks)
  - Q26: String analysis (6 marks), Character counting (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
