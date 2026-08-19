# 🚀 Queue — Java Implementations

A simple and beginner-friendly collection of **Queue Data Structure implementations in Java**.

This repository contains multiple ways to implement a Queue — starting from a basic array implementation and progressing to circular arrays, linked lists, and Java's built-in Collection Framework.

> 📚 **Learning Data Structures?** This repository is a hands-on way to understand how Queue works internally and how it can be implemented using different approaches.

---

## 📌 What is a Queue?

A **Queue** is a linear data structure that follows the:

### 🥇 FIFO — First In, First Out

The element that enters the queue first is the element that leaves first.

```text
        ADD →  [ 1 ][ 2 ][ 3 ][ 4 ]  → REMOVE
                ↑                 ↑
              FRONT              REAR
```

For example:

```text
Add:     1 → 2 → 3 → 4

Remove:  1
         2
         3
         4
```

Just like a real-world queue — **the person who comes first gets served first!** 🧑‍🤝‍🧑

---

## 🧠 Queue Operations

The implementations in this repository demonstrate the core Queue operations:

| Operation   | Description                                   |
| ----------- | --------------------------------------------- |
| `add()`     | Adds an element to the queue                  |
| `remove()`  | Removes the front element                     |
| `peek()`    | Returns the front element without removing it |
| `isEmpty()` | Checks whether the queue is empty             |
| `isFull()`  | Checks whether the queue is full              |

---

## 📂 Implementations

This repository currently contains **4 different Queue implementations**:

### 1️⃣ Queue Using Array

📄 `QUsingArray.java`

A basic Queue implementation using a normal array.

**Concepts covered:**

* Array-based Queue
* `front` and `rear` concepts
* Enqueue
* Dequeue
* Peek
* Empty Queue handling
* Full Queue handling

```text
Queue

FRONT                    REAR
  ↓                        ↓
[ 1 ][ 2 ][ 3 ][   ][   ]
```

---

### 2️⃣ Queue Using Circular Array 🔄

📄 `QUsingCircularArray.java`

A **Circular Queue** improves upon the basic array implementation by reusing the empty spaces created after removing elements.

```text
        ┌─────────────────┐
        ↓                 │
     [ 1 ][ 2 ][ 3 ][ 4 ][ 5 ]
        ↑                 │
        └─────────────────┘
```

**Concepts covered:**

* Circular Queue
* Modulo `%` operation
* `front` and `rear`
* `isEmpty()`
* `isFull()`
* Efficient space utilization

Example:

```text
Initial Queue:
1 → 2 → 3 → 4 → 5

Remove:
1

Add:
6

Queue:
2 → 3 → 4 → 5 → 6
```

---

### 3️⃣ Queue Using Linked List 🔗

📄 `QUsingLL.java`

This implementation creates a Queue using a **Linked List**.

Each element is represented using a Node containing:

```text
+-------+------+
| data  | next |
+-------+------+
```

The Queue maintains two important references:

```text
HEAD                         TAIL
 ↓                            ↓
[1] → [2] → [3] → [4] → [5]
```

**Concepts covered:**

* Linked List
* Nodes
* Head and Tail
* Dynamic memory allocation
* Enqueue
* Dequeue
* Peek

---

### 4️⃣ Queue Using Java Collection Framework ☕

📄 `QusingCollection.java`

Java already provides Queue implementations through the **Collection Framework**.

This program demonstrates the use of:

```java
Queue<Integer> q = new ArrayDeque<>();
```

It performs the same basic Queue operations without manually implementing the underlying data structure.

**Concepts covered:**

* Java Queue Interface
* `ArrayDeque`
* Generics
* Collection Framework
* Built-in Queue operations

---

## 📊 Implementation Comparison

| Implementation       | Storage         | Space Usage     | Difficulty |
| -------------------- | --------------- | --------------- | ---------- |
| Array                | Array           | Fixed           | ⭐          |
| Circular Array       | Array           | Efficient       | ⭐⭐         |
| Linked List          | Nodes           | Dynamic         | ⭐⭐         |
| Collection Framework | Java Collection | Managed by Java | ⭐          |

---

## ⚙️ Basic Queue Workflow

```text
             ENQUEUE
                ↓
        ┌───────────────┐
        │     QUEUE     │
        └───────────────┘
                ↓
             DEQUEUE

        First In → First Out
             FIFO
```

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project

```bash
cd Queue
```

### 3. Compile a Java program

For example:

```bash
javac QUsingArray.java
```

### 4. Run the program

```bash
java QUsingArray
```

You can similarly compile and run the other implementations:

```bash
javac QUsingCircularArray.java
java QUsingCircularArray
```

```bash
javac QUsingLL.java
java QUsingLL
```

```bash
javac QusingCollection.java
java QusingCollection
```

---

## 📁 Project Structure

```text
Queue/
│
├── QUsingArray.java
├── QUsingCircularArray.java
├── QUsingLL.java
├── QusingCollection.java
│
└── README.md
```

---

## 🎯 Learning Objectives

By exploring this repository, you can understand:

* ✅ What a Queue is
* ✅ FIFO principle
* ✅ Enqueue and Dequeue operations
* ✅ How Queue works internally
* ✅ Array-based Queue implementation
* ✅ Circular Queue implementation
* ✅ Linked List-based Queue
* ✅ Java's built-in Queue interface
* ✅ Difference between manual and library implementations
* ✅ Basic time and space considerations

---

## ⏱️ Complexity Overview

| Implementation |     Add |  Remove |    Peek |
| -------------- | ------: | ------: | ------: |
| Array          |  `O(1)` |  `O(n)` |  `O(1)` |
| Circular Array |  `O(1)` |  `O(1)` |  `O(1)` |
| Linked List    |  `O(1)` |  `O(1)` |  `O(1)` |
| ArrayDeque     | `O(1)`* | `O(1)`* | `O(1)`* |

> `*` Amortized/typical complexity for the Java implementation.

---

## 💡 Why Multiple Implementations?

One of the best ways to understand Data Structures is to implement the **same concept in different ways**.

This repository compares:

```text
             QUEUE
               │
       ┌───────┼────────┐
       ↓       ↓        ↓
     Array   Circular  Linked List
       │       Array       │
       └───────┬───────────┘
               ↓
       Java Collection
```

Each implementation provides a different perspective on how data can be stored and managed.

---

## 🚀 Future Improvements

Some possible additions to this repository:

* [ ] Queue using two Stacks
* [ ] Queue using two Queues
* [ ] Priority Queue implementation
* [ ] Deque implementation
* [ ] Generic Queue implementation
* [ ] Queue with user input
* [ ] Improved exception handling
* [ ] Unit testing
* [ ] Time & space complexity analysis

---

## 🌱 About This Repository

This repository is created for **learning and practicing Data Structures and Algorithms using Java**.

The goal is simple:

> **Understand the concept → Implement it → Experiment with it → Get better at DSA.** 💪

---

### ⭐ If you find this repository useful

Give it a **star ⭐** and feel free to explore, improve, and experiment with the implementations!

**Happy Coding! ☕💻**

---

## 👨‍💻 Author

**Your Name**

> Learning • Building • Improving 🚀
