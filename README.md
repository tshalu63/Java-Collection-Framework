# ☕ Java Collection Framework - Complete Guide

![Java](https://img.shields.io/badge/Java-Collection_Framework-orange)
![Level](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-blue)
![Topic](https://img.shields.io/badge/Topic-Java_Collections-green)

---

# 📖 Introduction

The **Java Collection Framework (JCF)** is a unified architecture used to store and manipulate groups of objects efficiently.

It provides:

- Interfaces
- Classes
- Algorithms

for performing operations like:

- Searching
- Sorting
- Insertion
- Deletion
- Traversal

All collection classes and interfaces are available in:

```java
java.util package
```

---

# 🚀 Why Collections?

Collections are more powerful than arrays because they are:

✅ Dynamic in size  
✅ Easy to manipulate  
✅ Flexible  
✅ Rich in built-in methods  
✅ Based on powerful Data Structures  

---

# 📌 Arrays vs Collections

| Feature | Arrays | Collections |
|---|---|---|
| Size | Fixed | Dynamic |
| Data Type | Same Type Only | Generic Support |
| Built-in Methods | Limited | Many Methods |
| Performance | Fast | Flexible |
| Data Structures | Basic | Advanced |

---

# 🏗️ Collection Framework Hierarchy

```text
Iterable
   ↓
Collection
 ┌───────────────┬───────────────┬───────────────┐
 List            Set             Queue
```

> `Map` is separate from the Collection hierarchy.

---

# 📌 Core Interfaces

---

# 1️⃣ Collection Interface

Root interface of the Collection Framework.

## 🔹 Common Methods

```java
add()
remove()
contains()
size()
clear()
isEmpty()
```

## 🔹 Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        Collection<String> c = new ArrayList<>();

        c.add("Java");
        c.add("Python");

        System.out.println(c);
    }
}
```

---

# 2️⃣ Iterator Interface

Used for traversing collection elements one by one.

## 🔹 Methods

| Method | Description |
|---|---|
| hasNext() | Checks next element exists |
| next() | Returns next element |
| remove() | Removes current element |

## 🔹 Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        ArrayList<String> list = new ArrayList<>();

        list.add("A");
        list.add("B");
        list.add("C");

        Iterator<String> itr = list.iterator();

        while(itr.hasNext()) {
            System.out.println(itr.next());
        }
    }
}
```

---

# 📚 LIST Interface

## ✔ Features

- Ordered
- Allows duplicates
- Index based

---

# 1️⃣ ArrayList

Uses a **Dynamic Array** internally.

## ✔ Advantages

✅ Fast random access  
✅ Best for searching  

## ❌ Disadvantages

❌ Slow insertion/deletion in middle  

## ✔ Time Complexity

| Operation | Complexity |
|---|---|
| Access | O(1) |
| Insert | O(n) |
| Delete | O(n) |

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        ArrayList<String> list = new ArrayList<>();

        list.add("Java");
        list.add("Python");
        list.add("C++");

        System.out.println(list);

        System.out.println(list.get(1));

        list.remove("Python");

        System.out.println(list);
    }
}
```

---

# 2️⃣ LinkedList

Uses a **Doubly Linked List**.

## ✔ Advantages

✅ Fast insertion/deletion  
✅ Can work as Queue and Deque  

## ❌ Disadvantages

❌ Slow random access  

## ✔ Complexity

| Operation | Complexity |
|---|---|
| Access | O(n) |
| Insert/Delete | O(1) |

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        LinkedList<Integer> list = new LinkedList<>();

        list.add(10);
        list.add(20);

        list.addFirst(5);
        list.addLast(30);

        System.out.println(list);
    }
}
```

---

# 📚 SET Interface

## ✔ Features

- Unique elements only
- No duplicates

---

# 1️⃣ HashSet

Uses a **Hash Table**.

## ✔ Features

✅ Very fast searching  
✅ No insertion order  

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        HashSet<String> set = new HashSet<>();

        set.add("Java");
        set.add("Python");
        set.add("Java");

        System.out.println(set);
    }
}
```

### ✔ Output

```text
[Java, Python]
```

---

# 2️⃣ LinkedHashSet

Maintains insertion order.

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        LinkedHashSet<Integer> set = new LinkedHashSet<>();

        set.add(100);
        set.add(50);
        set.add(10);

        System.out.println(set);
    }
}
```

---

# 3️⃣ TreeSet

Stores elements in sorted order.

Uses:

```java
Red Black Tree
```

## ✔ Features

✅ Sorted data  
✅ No duplicates  

## ❌ Slower than HashSet

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        TreeSet<Integer> set = new TreeSet<>();

        set.add(50);
        set.add(10);
        set.add(30);

        System.out.println(set);
    }
}
```

### ✔ Output

```text
[10, 30, 50]
```

---

# 📚 QUEUE Interface

FIFO Structure:

```text
First In First Out
```

---

# 1️⃣ PriorityQueue

Elements processed according to priority.

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        PriorityQueue<Integer> pq = new PriorityQueue<>();

        pq.add(30);
        pq.add(10);
        pq.add(20);

        System.out.println(pq);

        System.out.println(pq.poll());
    }
}
```

---

# 📚 DEQUE Interface

Double Ended Queue.

---

# 1️⃣ ArrayDeque

Faster than Stack and LinkedList.

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        ArrayDeque<Integer> dq = new ArrayDeque<>();

        dq.addFirst(10);
        dq.addLast(20);

        System.out.println(dq);
    }
}
```

---

# 🗺️ MAP Interface

Stores data in:

```text
Key → Value
```

Keys must be unique.

---

# 1️⃣ HashMap

## ✔ Features

✅ Fast  
✅ No order  
✅ Allows one null key  

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        HashMap<Integer, String> map = new HashMap<>();

        map.put(1, "Java");
        map.put(2, "Python");

        System.out.println(map);
    }
}
```

---

# 2️⃣ LinkedHashMap

Maintains insertion order.

---

# 3️⃣ TreeMap

Stores keys in sorted order.

---

# 4️⃣ Hashtable

Legacy synchronized class.

## ✔ Features

✅ Thread-safe  
✅ Synchronized  
✅ No null keys/values  

---

# 📊 Important Comparison Table

| Feature | ArrayList | LinkedList | HashSet | TreeSet |
|---|---|---|---|---|
| Structure | Dynamic Array | Doubly Linked List | Hash Table | Tree |
| Duplicates | Allowed | Allowed | Not Allowed | Not Allowed |
| Ordering | Insertion | Insertion | No Order | Sorted |
| Search | Fast | Slow | Very Fast | Logarithmic |

---

# 🛡️ Generics in Collections

Introduced in:

```text
JDK 1.5
```

## ✔ Benefits

✅ Type safety  
✅ Avoids manual type casting  
✅ Compile-time checking  

## ✔ Example

```java
ArrayList<String> list = new ArrayList<>();

list.add("Java");

// list.add(10); ❌ ERROR
```

---

# ⚖️ Comparable vs Comparator

---

# 1️⃣ Comparable

Used for **Natural Sorting**.

## ✔ Features

- Inside same class
- Uses `compareTo()`
- Package: `java.lang`

## ✔ Example

```java
class Student implements Comparable<Student> {

    int id;

    Student(int id) {
        this.id = id;
    }

    public int compareTo(Student s) {
        return this.id - s.id;
    }
}
```

---

# 2️⃣ Comparator

Used for **Custom Sorting**.

## ✔ Features

- Separate class
- Uses `compare()`
- Package: `java.util`

## ✔ Example

```java
Comparator<String> c = (a, b) -> a.length() - b.length();
```

---

# 🛠️ Collections Utility Class

The `Collections` class provides useful utility methods.

---

# 🔹 Important Methods

| Method | Purpose |
|---|---|
| Collections.sort() | Sorting |
| Collections.max() | Largest element |
| Collections.min() | Smallest element |
| Collections.reverse() | Reverse list |
| Collections.shuffle() | Random order |

## ✔ Example

```java
import java.util.*;

class Demo {
    public static void main(String[] args) {

        ArrayList<Integer> list = new ArrayList<>();

        list.add(50);
        list.add(10);
        list.add(30);

        Collections.sort(list);

        System.out.println(list);
    }
}
```

---

# 📌 When to Use What?

| Requirement | Best Choice |
|---|---|
| Fast Search | ArrayList |
| Fast Insert/Delete | LinkedList |
| Unique Data | HashSet |
| Sorted Data | TreeSet |
| Key-Value Storage | HashMap |
| Thread Safety | Hashtable |

---

# 🎯 Interview Questions

---

# Q1. Difference between ArrayList and LinkedList?

| ArrayList | LinkedList |
|---|---|
| Dynamic Array | Doubly Linked List |
| Fast Access | Fast Insert/Delete |
| Slow Manipulation | Slow Access |

---

# Q2. Difference between HashMap and Hashtable?

| HashMap | Hashtable |
|---|---|
| Not synchronized | Synchronized |
| Allows null | No null |
| Faster | Slower |

---

# Q3. Difference between Comparable and Comparator?

| Comparable | Comparator |
|---|---|
| Natural sorting | Custom sorting |
| compareTo() | compare() |
| Same class | Separate class |

---

# 🎯 Best Practices

✅ Use Generics  
✅ Prefer ArrayList for searching  
✅ Prefer LinkedList for frequent insertions  
✅ Use HashSet for uniqueness  
✅ Use TreeMap/TreeSet for sorting  
✅ Use Iterator for safe traversal  

---

# 📌 Conclusion

Java Collection Framework is one of the most important concepts in Java because it provides:

- Efficient Data Storage
- Dynamic Data Handling
- Built-in Algorithms
- High Performance
- Easy Manipulation of Objects

Mastering Collections is essential for:

- DSA
- Backend Development
- Spring Framework
- Interviews
- Competitive Programming

---

# ⭐ If You Found This Helpful

Give this repository a ⭐ on GitHub!

---
