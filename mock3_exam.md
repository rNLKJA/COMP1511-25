# Mock Exam 3: Lectures 13-15 (Linked List Deletion, Advanced Data Structures, Exam Preparation)
**Time Limit: 1 hour**  
**Total Marks: 100**

---

## Section A: Multiple Choice Questions (30 marks)
*Choose the best answer for each question. 2 marks each.*

**Question 1:** What is the basic structure of a linked list node?
a) Only data
b) Only a pointer to next
c) Data and a pointer to next
d) An array of data

**Question 2:** How do you know you've reached the end of a linked list?
a) The data is 0
b) The next pointer is NULL
c) The node is deleted
d) The list is empty

**Question 3:** What is the time complexity of inserting at the head of a linked list?
a) O(1)
b) O(n)
c) O(log n)
d) O(n²)

**Question 4:** When deleting a node from a linked list, what must you remember to do?
a) Update pointers of surrounding nodes
b) Free the memory of the deleted node
c) Both a and b
d) Nothing special required

**Question 5:** What happens if you access memory after calling `free()`?
a) Program continues normally
b) Undefined behavior (potential crash)
c) Memory is automatically reallocated
d) Compilation error

**Question 6:** Which operation is most efficient at the head of a linked list?
a) Insertion only
b) Deletion only
c) Both insertion and deletion
d) Neither operation

**Question 7:** What will this code do?
```c
struct node *temp = head;
head = head->next;
free(temp);
```
a) Delete the last node
b) Delete the first node
c) Delete a middle node
d) Cause an error

**Question 8:** In a function that deletes by value, what should you do if the value is not found?
a) Delete the first node anyway
b) Return the original head unchanged
c) Return NULL
d) Exit the program

**Question 9:** What is the main advantage of linked lists over arrays?
a) Faster access to elements
b) Dynamic size
c) Less memory usage
d) Easier to implement

**Question 10:** When traversing a linked list, which loop condition is correct?
a) `while (current < size)`
b) `while (current != NULL)`
c) `while (current->next != NULL)`
d) `for (int i = 0; i < size; i++)`

**Question 11:** What does this function do?
```c
int largest(struct node *head) {
    int max = head->data;
    struct node *current = head->next;
    while (current != NULL) {
        if (current->data > max) {
            max = current->data;
        }
        current = current->next;
    }
    return max;
}
```
a) Counts nodes
b) Finds the largest value
c) Sums all values
d) Deletes the largest node

**Question 12:** In exam preparation, what is a "hurdle question"?
a) The hardest question on the exam
b) A question you must pass to continue
c) An optional bonus question
d) A multiple choice question

**Question 13:** What is the best strategy for exam time management?
a) Start with the hardest questions
b) Spend equal time on all questions
c) Read all questions first, start with easier ones
d) Answer questions in order only

**Question 14:** When debugging linked list code, what should you check first?
a) The algorithm logic
b) NULL pointer handling
c) Memory allocation
d) Function prototypes

**Question 15:** What makes a good exam answer for coding questions?
a) Shortest possible code
b) Code that compiles and handles edge cases
c) Complex algorithms
d) Lots of comments

---

## Section B: Linked List Analysis (25 marks)
*Analyze and complete the linked list code. 5 marks each.*

**Question 16:** Complete this function to delete the head node:
```c
struct node* delete_head(struct node *head) {
    if (head == NULL) {
        return ______;
    }
    
    struct node *temp = ______;
    head = ______;
    ______(temp);
    
    return head;
}
```

**Question 17:** Find and fix the error in this deletion function:
```c
struct node* delete_value(struct node *head, int value) {
    if (head->data == value) {
        head = head->next;
        return head;  // What's wrong here?
    }
    
    struct node *current = head;
    while (current->next != NULL && current->next->data != value) {
        current = current->next;
    }
    
    if (current->next != NULL) {
        current->next = current->next->next;
    }
    
    return head;
}
```

**Question 18:** Complete this function to count positive numbers in a linked list:
```c
int count_positive(struct node *head) {
    int count = 0;
    struct node *current = ______;
    
    while (______ != NULL) {
        if (current->data > ______) {
            ______;
        }
        current = ______;
    }
    
    return count;
}
```

**Question 19:** Arrange these lines to create a function that deletes the tail node:
```
A. if (head == NULL) return NULL;
B. struct node* delete_tail(struct node *head) {
C. if (head->next == NULL) {
D. free(head);
E. return NULL;
F. }
G. struct node *current = head;
H. while (current->next->next != NULL) {
I. current = current->next;
J. }
K. free(current->next);
L. current->next = NULL;
M. return head;
N. }
```

Write the correct order: _________________________

**Question 20:** What will this code print for the list 1->2->3->NULL?
```c
struct node *current = head;
int count = 0;
while (current != NULL) {
    count++;
    current = current->next;
}
printf("Count: %d", count);
```
Answer: ________________

---

## Section C: Problem Solving (25 marks)

**Question 21: Exam Strategy (10 marks)**
You're taking a 2-hour exam with these questions:
- 20 Multiple choice (2 marks each) - estimated 20 minutes
- 5 Short functions (6 marks each) - estimated 60 minutes  
- 2 Full programs (20 marks each) - estimated 40 minutes

a) What's your time allocation strategy? (3 marks)
b) Which questions would you attempt first and why? (4 marks)
c) How would you handle a question you're stuck on? (3 marks)

**Question 22: Debug Analysis (15 marks)**
A student wrote this linked list function but it has multiple bugs:

```c
struct node* insert_sorted(struct node *head, int value) {
    struct node *new_node = malloc(sizeof(struct node));
    new_node->data = value;
    
    if (head == NULL || value < head->data) {
        new_node->next = head;
        return new_node;
    }
    
    struct node *current = head;
    while (current->next != NULL && current->next->data < value) {
        current = current->next;
    }
    
    new_node->next = current->next;
    current->next = new_node;
    
    return head;
}
```

a) Identify two potential issues with this code (6 marks)
b) Write the corrected version (9 marks)

---

## Section D: Implementation (20 marks)

**Question 23: Complete Linked List Implementation (20 marks)**
Write a complete program that demonstrates linked list operations:

**Requirements:**
1. **Define a node structure** for storing integers
2. **Implement these functions:**
   - `struct node* create_node(int data)` - creates a new node
   - `struct node* insert_head(struct node *head, int data)` - inserts at beginning
   - `struct node* delete_value(struct node *head, int value)` - deletes first occurrence
   - `void print_list(struct node *head)` - prints all values
   - `void free_list(struct node *head)` - frees all memory

3. **In main function:**
   - Create a list with values: 10, 20, 30
   - Print the list
   - Delete the value 20
   - Print the list again
   - Free all memory

**Example Output:**
```
List: 10 -> 20 -> 30 -> NULL
After deleting 20: 10 -> 30 -> NULL
```

**Grading Criteria:**
- Correct struct definition (2 marks)
- Proper create_node implementation (3 marks)
- Correct insert_head implementation (4 marks)
- Proper delete_value with memory management (6 marks)
- Working print_list and main function (3 marks)
- Memory cleanup (2 marks)

---

## Answer Template

**Section B - Linked List Analysis:**

**Q16:**
```c
struct node* delete_head(struct node *head) {
    if (head == NULL) {
        return ______;
    }
    
    struct node *temp = ______;
    head = ______;
    ______(temp);
    
    return head;
}
```

**Q17:**
Issue: ________________________________________________
Corrected code:
```c
// Write corrected version




```

**Q18:**
```c
int count_positive(struct node *head) {
    int count = 0;
    struct node *current = ______;
    
    while (______ != NULL) {
        if (current->data > ______) {
            ______;
        }
        current = ______;
    }
    
    return count;
}
```

**Q19:** Line order: _________________________________

**Q20:** Answer: ________________

**Section C - Problem Solving:**

**Q21:**
a) Time allocation: ___________________________________
b) Question order: ___________________________________
c) Stuck strategy: ___________________________________

**Q22:**
a) Issues identified:
1. _______________________________________________
2. _______________________________________________

b) Corrected code:
```c
// Write corrected version here




```

**Section D - Implementation:**

**Q23: Complete Linked List Program**
```c
// Write your complete program here




```

---

## Marking Rubric
- **MCQ (30 marks):** 2 marks per correct answer
- **Linked List Analysis (25 marks):** 5 marks each - correct understanding and implementation
- **Problem Solving (25 marks):** Clear reasoning and practical solutions
- **Implementation (20 marks):** Working code with proper memory management

**Exam Success Tips:**
- Always check for NULL pointers in linked list operations
- Remember to free memory when deleting nodes
- Draw diagrams to visualize pointer operations
- Test your logic with small examples
- Handle edge cases (empty lists, single nodes)
- Manage your time effectively during exams
