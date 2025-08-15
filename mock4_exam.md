# Mock Exam 4: Advanced Programming Concepts
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the output of this code?
```c
int x = 10;
int y = 3;
printf("%d", x % y);
```
a) 3
b) 1
c) 0
d) Error

**Question 2:** Which data type is best for storing a person's height in centimeters?
a) `int`
b) `double`
c) `char`
d) `float`

**Question 3:** What will this code print?
```c
int i = 1;
while (i <= 4) {
    printf("%d ", i * i);
    i++;
}
```
a) 1 2 3 4
b) 1 4 9 16
c) 2 4 6 8
d) 1 3 5 7

**Question 4:** Which operator is used for logical AND?
a) `&`
b) `&&`
c) `|`
d) `||`

**Question 5:** What is the correct way to declare a pointer to an integer?
a) `int pointer x;`
b) `int *x;`
c) `pointer int x;`
d) `int &x;`

**Question 6:** What does `strcmp()` return if two strings are equal?
a) 1
b) 0
c) -1
d) The length of the strings

**Question 7:** What will this code print?
```c
char str[] = "Hello";
printf("%d", strlen(str));
```
a) 4
b) 5
c) 6
d) Error

**Question 8:** In command line arguments, what does `argc` represent?
a) The first argument
b) The number of arguments
c) The program name
d) An array of arguments

**Question 9:** What happens when you dereference a NULL pointer?
a) Nothing
b) Compilation error
c) Runtime error (segmentation fault)
d) Returns 0

**Question 10:** Which function is used to allocate memory dynamically?
a) `calloc()`
b) `malloc()`
c) `realloc()`
d) All of the above

**Question 11:** What is the purpose of the `#ifndef` directive in header files?
a) To include a file
b) To define a constant
c) To prevent multiple inclusions
d) To create a function

**Question 12:** What will this code print?
```c
int numbers[3] = {1, 2, 3};
printf("%d", numbers[2]);
```
a) 1
b) 2
c) 3
d) Error

**Question 13:** Which loop executes at least once?
a) For loop
b) While loop
c) Do-while loop
d) All loops

**Question 14:** What is the correct way to free dynamically allocated memory?
a) `delete(ptr);`
b) `free(ptr);`
c) `release(ptr);`
d) `deallocate(ptr);`

**Question 15:** What does the `*` operator do with pointers?
a) Gets the address of a variable
b) Gets the value a pointer points to
c) Creates a new pointer
d) Multiplies two values

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between `++i` and `i++`. Give an example where this difference matters.

**Question 17:** What are the three main parts of a `for` loop? Explain what each part does.

**Question 18:** Explain what "array decay" means in C. How does it affect function parameters?

**Question 19:** What is the purpose of the null terminator in strings? What happens if it's missing?

**Question 20:** Explain the difference between `malloc()` and `calloc()`. When would you use each one?

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

**Question 25: Student Grade Calculator (15 marks)**
Write a complete program that:
- Defines a struct `student` with fields for name, id, and grades array
- Creates an array of 3 students
- Allows user to input grades for each student
- Calculates and displays each student's average grade
- Finds and displays the student with the highest average

**Question 26: Memory Management Simulator (10 marks)**
Write a program that:
- Simulates memory allocation and deallocation
- Tracks allocated memory blocks with descriptions
- Allows user to allocate memory for different data types
- Displays current memory status
- Properly frees all allocated memory

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

**Q25: Student Grade Calculator**
```c
// Write your complete program here




```

**Q26: Memory Management Simulator**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Struct definition (4 marks), Array handling (4 marks), Calculations (4 marks), Logic (3 marks)
  - Q26: Memory tracking (6 marks), User interface (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
