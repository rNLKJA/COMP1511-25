# Mock Final Exam: All Topics (Lectures 1-15)
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** Which is correct C syntax for declaring an integer variable?
a) `int x;`
b) `integer x;`
c) `x: int;`
d) `var x = int;`

**Question 2:** What will this code print?
```c
int arr[4] = {10, 20, 30, 40};
printf("%d", arr[2]);
```
a) 20
b) 30
c) 2
d) Error

**Question 3:** What does the `*` operator do with pointers?
a) Gets the address
b) Gets the value pointed to
c) Creates a pointer
d) Multiplies values

**Question 4:** How is a C string terminated?
a) With a space
b) With '\0'
c) With '\n'
d) Automatically

**Question 5:** What will `strlen("Hello")` return?
a) 6
b) 5
c) 4
d) Error

**Question 6:** In `main(int argc, char *argv[])`, what is `argv[0]`?
a) First user argument
b) Program name
c) Number of arguments
d) NULL

**Question 7:** What does `malloc()` do?
a) Allocates stack memory
b) Allocates heap memory
c) Frees memory
d) Creates variables

**Question 8:** What must you do after using `malloc()`?
a) Nothing
b) Call `free()`
c) Call `delete()`
d) Reset the pointer

**Question 9:** In a linked list, how do you know you've reached the end?
a) Data is 0
b) Next pointer is NULL
c) Node is deleted
d) List is empty

**Question 10:** What is the time complexity of inserting at the head of a linked list?
a) O(1)
b) O(n)
c) O(log n)
d) O(n²)

**Question 11:** Which function safely copies strings?
a) `strcopy()`
b) `strcpy()`
c) `copy()`
d) `strdup()`

**Question 12:** What happens with pass-by-value in C?
a) Original variable is modified
b) A copy is passed to the function
c) Variable is deleted
d) Reference is passed

**Question 13:** Which demonstrates good programming style?
a) `int x, y, z;`
b) `int student_count;`
c) `int a;`
d) `int var1;`

**Question 14:** What does this function do?
```c
int mystery(int a, int b) {
    return (a > b) ? a : b;
}
```
a) Returns sum
b) Returns larger value
c) Returns smaller value
d) Returns difference

**Question 15:** When deleting a linked list node, you must:
a) Update surrounding pointers
b) Free the node's memory
c) Both a and b
d) Nothing special

---

## Section B: Short Answer Questions (25 marks)
*Provide clear, concise answers. 5 marks each.*

**Question 16:** Explain the difference between stack and heap memory. When would you use each?

**Question 17:** What is a memory leak? How can you prevent memory leaks in C programs?

**Question 18:** Compare arrays and linked lists. Give one advantage and one disadvantage of each.

**Question 19:** Explain what "pass by value" means in C. How can you modify a variable inside a function?

**Question 20:** What are the key principles of good programming style? Why do they matter in professional development?

---

## Section C: Code Completion and Analysis (25 marks)
*Complete the code or fix errors. 5 marks each.*

**Question 21:** Complete this function to reverse a string in place:
```c
void reverse_string(char str[]) {
    int len = strlen(str);
    for (int i = 0; i < ______; i++) {
        char temp = str[i];
        str[i] = str[______];
        str[______] = temp;
    }
}
```

**Question 22:** Fix the memory management issue in this code:
```c
int* create_array(int size) {
    int arr[size];
    for (int i = 0; i < size; i++) {
        arr[i] = i * i;
    }
    return arr;  // Problem here!
}
```

**Question 23:** Complete this linked list insertion function:
```c
struct node* insert_head(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return ______;
    
    new_node->data = ______;
    new_node->next = ______;
    return ______;
}
```

**Question 24:** Complete this command line argument processor:
```c
int main(int argc, char *argv[]) {
    if (argc != 3) {
        printf("Usage: %s <num1> <num2>\n", ______);
        return 1;
    }
    
    int a = ______(argv[1]);
    int b = ______(argv[2]);
    printf("Sum: %d\n", a + b);
    return 0;
}
```

**Question 25:** Complete this function to find maximum in an array:
```c
int find_max(int arr[], int size) {
    if (size <= 0) return ______;
    
    int max = ______;
    for (int i = 1; i < ______; i++) {
        if (arr[i] > ______) {
            max = ______;
        }
    }
    return max;
}
```

---

## Section D: Programming Problems (20 marks)

**Question 26: Student Management System (20 marks)**

Write a complete program that manages student records using both arrays and dynamic memory:

**Requirements:**

1. **Define a struct** for student with:
   - `int id`
   - `char name[50]`
   - `double gpa`

2. **Implement these functions:**
   - `struct student* create_student(int id, char name[], double gpa)` - creates student using malloc
   - `void print_student(struct student *s)` - prints student info
   - `double calculate_average_gpa(struct student students[], int count)` - calculates average from array
   - `void free_student(struct student *s)` - frees a single student

3. **In main function:**
   - Create an array of 3 student pointers
   - Create 3 individual students using dynamic allocation:
     - Student 1: ID=101, Name="Alice", GPA=3.5
     - Student 2: ID=102, Name="Bob", GPA=3.8  
     - Student 3: ID=103, Name="Charlie", GPA=3.2
   - Print all students
   - Calculate and display the average GPA
   - Free all allocated memory

**Example Output:**
```
=== Student Records ===
Student ID: 101, Name: Alice, GPA: 3.50
Student ID: 102, Name: Bob, GPA: 3.80
Student ID: 103, Name: Charlie, GPA: 3.20

Average GPA: 3.50

Memory freed successfully.
```

**Grading Breakdown:**
- Correct struct definition (2 marks)
- create_student function with malloc (4 marks)
- print_student function (2 marks)
- calculate_average_gpa function (4 marks)
- Main function with proper array handling (4 marks)
- Memory management and cleanup (4 marks)

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
void reverse_string(char str[]) {
    int len = strlen(str);
    for (int i = 0; i < ______; i++) {
        char temp = str[i];
        str[i] = str[______];
        str[______] = temp;
    }
}
```

**Q22:**
```c
// Write corrected version




```

**Q23:**
```c
struct node* insert_head(struct node *head, int data) {
    struct node *new_node = malloc(sizeof(struct node));
    if (new_node == NULL) return ______;
    
    new_node->data = ______;
    new_node->next = ______;
    return ______;
}
```

**Q24:**
```c
int main(int argc, char *argv[]) {
    if (argc != 3) {
        printf("Usage: %s <num1> <num2>\n", ______);
        return 1;
    }
    
    int a = ______(argv[1]);
    int b = ______(argv[2]);
    printf("Sum: %d\n", a + b);
    return 0;
}
```

**Q25:**
```c
int find_max(int arr[], int size) {
    if (size <= 0) return ______;
    
    int max = ______;
    for (int i = 1; i < ______; i++) {
        if (arr[i] > ______) {
            max = ______;
        }
    }
    return max;
}
```

**Section D - Programming Problem:**

**Q26: Student Management System**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - comprehensive understanding
- **Code Completion (25 marks):** 5 marks each - correct syntax and logic
- **Programming Problem (20 marks):** As detailed in breakdown above

**Final Exam Success Strategy:**
1. **Time Management:** Allocate ~15 min for MCQ, ~15 min for short answers, ~15 min for code completion, ~15 min for programming
2. **Start with Confidence:** Begin with questions you're most confident about
3. **Check Your Work:** Reserve time to review your answers
4. **Memory Management:** In all dynamic allocation problems, check for NULL and call free()
5. **Edge Cases:** Consider empty inputs, single elements, etc.
6. **Clean Code:** Use meaningful variable names even under time pressure

**Good luck! You've mastered the fundamentals of C programming and are ready for advanced computer science challenges.**
