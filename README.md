## **What is Data Structure?**  
A **Data Structure** is a specialized format for organizing, managing, and storing data efficiently. It enables effective data access, retrieval, and modification. The choice of data structure affects the **performance of algorithms** and plays a crucial role in problem-solving.

---

## **Types of Data Structures**  
Data structures are broadly classified into **Linear** and **Non-Linear** structures based on how data elements are organized.

### **1️⃣ Linear Data Structures**  
In **linear data structures**, elements are arranged sequentially, one after another.

| **Type**       | **Key Features** |
|---------------|-----------------|
| **Array**     | Fixed-size sequential collection of elements stored in contiguous memory. |
| **Linked List** | Dynamic collection of nodes connected by pointers. Efficient insertions and deletions. |
| **Stack**     | Follows **LIFO (Last In, First Out)** principle. Used in undo operations, recursion. |
| **Queue**     | Follows **FIFO (First In, First Out)** principle. Used in scheduling tasks. |

---

### **2️⃣ Non-Linear Data Structures**  
In **non-linear data structures**, elements are connected in a hierarchical or complex manner.

| **Type**      | **Key Features** |
|--------------|-----------------|
| **Tree**     | Hierarchical structure with nodes. Used in file systems, databases. |
| **Graph**    | Collection of **nodes (vertices)** and **edges (connections)**. Used in social networks, GPS. |
| **Hashing**  | Uses **key-value pairs** for efficient data retrieval. Example: Hash Tables, HashMaps. |

---
## **Step-by-Step Implementation of Stack in Python**

We will implement a **stack** step by step using a Python list.  
A **stack** follows the **LIFO (Last In, First Out)** principle.

---

### **📌 Step 1: Create a Stack Class**
First, define a `Stack` class that will store elements.

```python
class Stack:
    def __init__(self):  
        self.stack = []  # Initialize an empty list to store elements
```

- We define a class `Stack` and initialize an **empty list** to store stack elements.

---

### **📌 Step 2: Implement the Push Operation**
The **push()** method adds an element to the top of the stack.

```python
def push(self, item):
        self.stack.append(item)
        print(f"Pushed {item} to stack")
```

- This method **appends** an element to the list.

---

### **📌 Step 3: Implement the Pop Operation**
The **pop()** method removes and returns the top element.

```python
 def pop(self):
        if self.is_empty():
            print("Stack Underflow: No elements to pop")
        else:
            print(f"Popped: {self.stack.pop()}")
```

- First, it **checks if the stack is empty** to prevent errors.
- Then, it **removes the last element** using `pop()`.

---

### **📌 Step 4: Implement the Peek Operation**
The **peek()** method returns the **top element** without removing it.

```python
 def peek(self):
        if self.is_empty():
            print("Stack is empty")
        else:
            print(f"Top element: {self.stack[-1]}")
```

- This method **accesses the last element** using `self.stack[-1]`.

---

### **📌 Step 5: Implement the isEmpty and Size Methods**
Check if the stack is **empty** and get the **size**.

```python
 def is_empty(self):
        return len(self.stack) == 0
```
def size(self):
        print(f"Stack size: {len(self.stack)}")

---

### **📌 Step 6: Complete Stack Implementation**
Now, we **combine all methods** into a single class.

```python
class Stack:
    def __init__(self):  
        self.stack = []

    def push(self, item):
        self.stack.append(item)
        print(f"Pushed {item} to stack")

    def pop(self):
        if self.is_empty():
            print("Stack Underflow: No elements to pop")
        else:
            print(f"Popped: {self.stack.pop()}")

    def peek(self):
        if self.is_empty():
            print("Stack is empty")
        else:
            print(f"Top element: {self.stack[-1]}")

    def is_empty(self):
        return len(self.stack) == 0

    def size(self):
        print(f"Stack size: {len(self.stack)}")

# Example Usage
s = Stack()
s.push(10)  # Pushed 10
s.push(20)  # Pushed 20
s.push(30)  # Pushed 30
s.peek()    # Output: Top element: 30
s.pop()     # Output: Popped: 30
s.size()    # Output: Stack size: 2
print("Is stack empty?", s.is_empty())  # Output: False

```

---

---

### **📌 Step 1: Create a Queue Class**  
First, define a `Queue` class that will store elements.

```python
class Queue:
    def __init__(self):
        self.queue = []  # Initialize an empty list to store elements
```

- We define a class `Queue` and initialize an **empty list** to store queue elements.

---

### **📌 Step 2: Implement the Enqueue Operation**  
The **enqueue()** method adds an element to the end of the queue.

```python
def enqueue(self, item):
    self.queue.append(item)
    print(f"Enqueued {item} to queue")
```

- This method **appends** an element at the end of the queue.

---

### **📌 Step 3: Implement the Dequeue Operation**  
The **dequeue()** method removes and returns the front element.

```python
def dequeue(self):
    if self.is_empty():
        print("Queue Underflow: No elements to dequeue")
    else:
        print(f"Dequeued: {self.queue.pop(0)}")
```

- First, it **checks if the queue is empty** to prevent errors.
- Then, it **removes the first element** using `pop(0)`.

---

### **📌 Step 4: Implement the Front Operation**  
The **front()** method returns the **first element** without removing it.

```python
def front(self):
    if self.is_empty():
        print("Queue is empty")
    else:
        print(f"Front element: {self.queue[0]}")
```

- This method **accesses the first element** using `self.queue[0]`.

---

### **📌 Step 5: Implement the isEmpty and Size Methods**  
Check if the queue is **empty** and get the **size**.

```python
def is_empty(self):
    return len(self.queue) == 0
```

```python
def size(self):
    print(f"Queue size: {len(self.queue)}")
```

---

### **📌 Step 6: Complete Queue Implementation**  
Now, we **combine all methods** into a single class.

```python
class Queue:
    def __init__(self):
        self.queue = []

    def enqueue(self, item):
        self.queue.append(item)
        print(f"Enqueued {item} to queue")

    def dequeue(self):
        if self.is_empty():
            print("Queue Underflow: No elements to dequeue")
        else:
            print(f"Dequeued: {self.queue.pop(0)}")

    def front(self):
        if self.is_empty():
            print("Queue is empty")
        else:
            print(f"Front element: {self.queue[0]}")

    def is_empty(self):
        return len(self.queue) == 0

    def size(self):
        print(f"Queue size: {len(self.queue)}")

# Example Usage
q = Queue()
q.enqueue(10)  # Enqueued 10
q.enqueue(20)  # Enqueued 20
q.enqueue(30)  # Enqueued 30
q.front()      # Output: Front element: 10
q.dequeue()    # Output: Dequeued: 10
q.size()       # Output: Queue size: 2
print("Is queue empty?", q.is_empty())  # Output: False
```
