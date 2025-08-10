# Mock Exam 1: Lectures 1-6 (Variables, Control Flow, Functions, Arrays, Style)
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** Which is the correct way to declare an integer variable in C?
a) `int x;`
b) `integer x;`
c) `var x;`
d) `x: int;`

**Question 2:** What will this code print?
```c
int x = 10;
if (x > 5 && x < 15) {
    printf("Medium");
} else {
    printf("Large");
}
```
a) Medium
b) Large
c) Nothing
d) Error

**Question 3:** What is the output of this loop?
```c
for (int i = 0; i < 3; i++) {
    printf("%d ", i);
}
```
a) 0 1 2
b) 1 2 3
c) 0 1 2 3
d) 1 2

**Question 4:** Which function prototype is correct for a function that takes two integers and returns their sum?
a) `int add(int a, int b);`
b) `add(int a, int b);`
c) `int add(a, b);`
d) `void add(int a, int b);`

**Question 5:** What is the index of the first element in a C array?
a) 1
b) 0
c) -1
d) Depends on the array size

**Question 6:** What will `numbers[2]` return for this array?
```c
int numbers[5] = {10, 20, 30, 40, 50};
```
a) 20
b) 30
c) 2
d) 40

**Question 7:** Which demonstrates good programming style?
a) `int x, y, z;`
b) `int student_count;`
c) `int a;`
d) `int var1;`

**Question 8:** What happens when you pass a variable to a function in C?
a) The original variable is modified
b) A copy of the variable is passed
c) The variable is deleted
d) Nothing happens

**Question 9:** What does this function do?
```c
int mystery(int a, int b) {
    if (a > b) return a;
    return b;
}
```
a) Returns the sum
b) Returns the larger value
c) Returns the smaller value
d) Returns the difference

**Question 10:** Which is the correct way to initialize an array?
a) `int arr[3] = {1, 2, 3, 4};`
b) `int arr[3] = {1, 2, 3};`
c) `int arr[] = 1, 2, 3;`
d) `int arr[3] = 1, 2, 3;`

**Question 11:** What will this while loop print?
```c
int i = 3;
while (i > 0) {
    printf("%d ", i);
    i--;
}
```
a) 3 2 1
b) 3 2 1 0
c) 1 2 3
d) Infinite loop

**Question 12:** Which variable name follows good style guidelines?
a) `x`
b) `temp_value`
c) `a1`
d) `v`

**Question 13:** What is the purpose of the `return` statement in a function?
a) To end the program
b) To send a value back to the caller
c) To print a value
d) To create a variable

**Question 14:** How do you access the third element of an array called `scores`?
a) `scores[3]`
b) `scores[2]`
c) `scores(2)`
d) `scores.2`

**Question 15:** What will this code do?
```c
int count = 0;
do {
    count++;
    printf("%d ", count);
} while (count < 2);
```
a) Print: 1 2
b) Print: 0 1
c) Print: 1
d) Print nothing

---

## Section B: Short Answer Questions (25 marks)
*Provide brief, clear answers. 5 marks each.*

**Question 16:** Explain the difference between `++i` and `i++`. Give an example where this difference matters.

**Question 17:** What are the three main parts of a `for` loop? Explain what each part does.

**Question 18:** List three benefits of using functions in your programs.

**Question 19:** Explain what "pass by value" means and why it's important to understand when writing functions.

**Question 20:** What makes code "readable"? Give three specific style guidelines that improve code readability.

---

## Section C: Code Completion (20 marks)
*Complete the missing parts of the code. 5 marks each.*

**Question 21:** Complete this function to calculate the average of three numbers:
```c
double calculate_average(int a, int b, int c) {
    double sum = ________________;
    return ________________;
}
```

**Question 22:** Fill in the blanks to create a loop that prints numbers from 5 down to 1:
```c
for (int i = ______; ______ >= 1; ______) {
    printf("%d ", i);
}
```

**Question 23:** Complete this function to find the maximum value in an array:
```c
int find_max(int array[], int size) {
    int max = array[0];
    for (int i = ______; i < ______; i++) {
        if (array[i] ______ max) {
            max = ______;
        }
    }
    return max;
}
```

**Question 24:** Complete this grade classification function:
```c
char get_letter_grade(int score) {
    if (score >= 90) {
        return '______';
    } else if (score >= 80) {
        return '______';
    } else if (score >= 70) {
        return '______';
    } else {
        return '______';
    }
}
```

---

## Section D: Programming Problems (25 marks)

**Question 25: Simple Calculator Function (15 marks)**
Write a function called `simple_calculator` that:
- Takes three parameters: two integers and one character (operation)
- Supports operations: '+', '-', '*', '/'
- Returns the result as a double
- Returns -1 if the operation is invalid or if there's division by zero

Also write a main function that:
- Prompts the user for two numbers and an operation
- Calls your calculator function
- Prints the result or an error message

**Question 26: Array Statistics (10 marks)**
Write a complete program that:
- Creates an array to store 5 integers
- Prompts the user to enter 5 numbers
- Calculates and displays:
  - The sum of all numbers
  - The average (as a double with 2 decimal places)
  - The largest number in the array

Use proper variable names and good programming style.

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
double calculate_average(int a, int b, int c) {
    double sum = ________________;
    return ________________;
}
```

**Q22:**
```c
for (int i = ______; ______ >= 1; ______) {
    printf("%d ", i);
}
```

**Q23:**
```c
int find_max(int array[], int size) {
    int max = array[0];
    for (int i = ______; i < ______; i++) {
        if (array[i] ______ max) {
            max = ______;
        }
    }
    return max;
}
```

**Q24:**
```c
char get_letter_grade(int score) {
    if (score >= 90) {
        return '______';
    } else if (score >= 80) {
        return '______';
    } else if (score >= 70) {
        return '______';
    } else {
        return '______';
    }
}
```

**Section D - Programming Problems:**

**Q25: Simple Calculator**
```c
// Write your complete calculator program here




```

**Q26: Array Statistics**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Short Answer (25 marks):** 5 marks each - clear understanding and accurate explanation
- **Code Completion (20 marks):** 5 marks each - correct syntax and logic
- **Programming (25 marks):** 
  - Q25: Function design (8 marks), Main function (4 marks), Error handling (3 marks)
  - Q26: Array handling (4 marks), Calculations (4 marks), Style (2 marks)

**Success Tips:**
- Read each question carefully
- Check your syntax
- Use meaningful variable names
- Test your logic with sample values
- Manage your time effectively
