# Mock Exam 3: Comprehensive Programming Assessment
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the correct way to declare a constant in C?
a) `const int MAX_SIZE = 100;`
b) `#define MAX_SIZE 100`
c) `int MAX_SIZE = 100;`
d) Both a and b are correct

**Question 2:** What will this code print?
```c
int x = 5;
int y = 3;
printf("%d", x / y);
```
a) 1.67
b) 1
c) 2
d) Error

**Question 3:** Which loop type is best for processing input until a specific value is encountered?
a) For loop
b) While loop with counter
c) Sentinel-controlled while loop
d) Do-while loop

**Question 4:** What is the output of this code?
```c
int i = 0;
do {
    printf("%d ", i);
    i += 2;
} while (i < 6);
```
a) 0 2 4
b) 0 2 4 6
c) 2 4 6
d) 0 1 2 3 4 5

**Question 5:** Which operator has the highest precedence?
a) `+`
b) `*`
c) `()`
d) `=`

**Question 6:** What will `strlen("Hello\n")` return?
a) 5
b) 6
c) 7
d) Error

**Question 7:** In `main(int argc, char *argv[])`, what does `argv[1]` represent?
a) The program name
b) The first command line argument
c) The number of arguments
d) The last argument

**Question 8:** What does the `&` operator do with variables?
a) Gets the value of a variable
b) Gets the address of a variable
c) Multiplies two variables
d) Compares two variables

**Question 9:** What will this code print?
```c
int x = 10;
int *ptr = &x;
*ptr = 20;
printf("%d", x);
```
a) 10
b) 20
c) Address of x
d) Error

**Question 10:** What does `malloc()` return if memory allocation fails?
a) 0
b) NULL
c) -1
d) A random address

**Question 11:** Which function safely copies one string to another with size limit?
a) `strcpy()`
b) `strncpy()`
c) `strcat()`
d) `strcmp()`

**Question 12:** What happens if you forget to call `free()` after `malloc()`?
a) Compilation error
b) Runtime error
c) Memory leak
d) Nothing happens

**Question 13:** In a linked list, what does the last node's next pointer contain?
a) NULL
b) The address of the first node
c) A random address
d) The address of the last node

**Question 14:** Which header file is needed for string functions?
a) `<stdio.h>`
b) `<string.h>`
c) `<stdlib.h>`
d) `<math.h>`

**Question 15:** What is the purpose of header guards in header files?
a) To include the file multiple times
b) To prevent multiple inclusions
c) To define constants
d) To declare functions

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between stack and heap memory. Give one advantage and one disadvantage of each.

**Question 17:** What is the purpose of function prototypes in header files? Why can't we put function definitions in header files?

**Question 18:** Explain what "pass by value" means in C functions. How does this affect the original variables?

**Question 19:** What is a memory leak and how does it occur in C programs? How can it be prevented?

**Question 20:** Explain the difference between `char str[] = "Hello"` and `char *str = "Hello"`. Which one is modifiable?

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to find the minimum value in an array:
```c
int find_min(int array[], int size) {
    int min = array[0];
    for (int i = ______; i < ______; i++) {
        if (array[i] ______ min) {
            min = ______;
        }
    }
    return min;
}
```

**Question 22:** Fill in the blanks to create a function that counts vowels in a string:
```c
int count_vowels(char str[]) {
    int count = 0;
    for (int i = 0; str[i] != ______; i++) {
        char c = tolower(str[i]);
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
            ______;
        }
    }
    return count;
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

**Question 24:** Complete this command line argument processor:
```c
int main(int argc, char *argv[]) {
    if (argc < ______) {
        printf("Usage: %s <filename>\n", ______);
        return 1;
    }
    
    char *filename = ______;
    printf("Processing file: %s\n", filename);
    return 0;
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Dynamic Array Manager (15 marks)**
Write a complete program that:
- Prompts the user for an initial array size
- Dynamically allocates memory for that many integers
- Allows the user to add numbers to the array (with automatic resizing)
- Displays the array contents
- Properly frees all allocated memory

Include proper error checking for `malloc()` failure.

**Question 26: String Processor (10 marks)**
Write a program that:
- Takes a sentence as command line argument
- Implements a function `void remove_spaces(char str[])` that removes all spaces
- Implements a function `int count_words(char str[])` that counts words
- Displays the original sentence, the sentence without spaces, and the word count

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
int find_min(int array[], int size) {
    int min = array[0];
    for (int i = ______; i < ______; i++) {
        if (array[i] ______ min) {
            min = ______;
        }
    }
    return min;
}
```

**Q22:**
```c
int count_vowels(char str[]) {
    int count = 0;
    for (int i = 0; str[i] != ______; i++) {
        char c = tolower(str[i]);
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
            ______;
        }
    }
    return count;
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
int main(int argc, char *argv[]) {
    if (argc < ______) {
        printf("Usage: %s <filename>\n", ______);
        return 1;
    }
    
    char *filename = ______;
    printf("Processing file: %s\n", filename);
    return 0;
}
```

**Section D - Programming Problems:**

**Q25: Dynamic Array Manager**
```c
// Write your complete program here




```

**Q26: String Processor**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Dynamic allocation (8 marks), Resizing (4 marks), Memory management (3 marks)
  - Q26: String functions (6 marks), Command line args (4 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
