# Practical Data Structures

---

### Calibration (0)

![Blank Derp](blank.jpg)

Data structures?

---

### Calibration (1)


- Big-O and complexity?
- Interfaces vs. Implementation

---

### Calibration (2)

- Arrays?
- Linked Lists?
- Stacks and Queues?
- Hashing? Maps?

---

### Calibration (3)

- Garbage collection?
- Immutability? Immutable data structures?
- Persistent data structures?

---

### Preface

- Language agnostic, so I used `python`
- Trigger warning for folks with Mathematics / CS Theory background (why are you here anyway?)

---

## Primers

Data Structures, Complexity, Interfaces

---

### Data Structures

- Data lives in memory
- How we store that data in memory is important
- Computers are fast...but not that fast

---

### Big-O

$$f(x) = O(g(x))$$

if and only if

$$|f(x)| \leq M|g(x)|$$

for all $$x \geq x_0$$

---

![Big O](bigo.png)

---

### Complexity

$$O(1)$$

```python
x = 5
```

$$O(n)$$

```python
x = [1, 2, 3, 4, 5]
for i in x:
    print(i * 2)
```

$$O(n^2)$$

```python
x = [1, 2, 3, 4, 5]
for i in x:
    for j in x:
        print(i + j)
```

---

$$O(\log{n})$$

Binary search

$$O(n\log{n})$$

Most (practical) sorting algorithms

---

### Interfaces vs Implementations

- Interfaces: what a data structure does.
- Implementation: how a data structure does it

---

## Common Data Structures

---

### List Interface

- Support `add(item, i)`, `remove(i)`, `get(i)`, `set(item, i)`
- Could use an Array, but what happens when you (1) add items (2) run out of space in the Array?
- Array backed lists

```
[ ][ ][ ][ ][ ][ ][ ][ ][ ][ ]
[a][b][c][ ][ ][ ][ ][ ][ ][ ]
[a][b][c][d][ ][ ][ ][ ][ ][ ]
[e][a][b][c][d][ ][ ][ ][ ][ ]
```

---

#### Linked List

```python
class Node:
    def __init__(self, data, next):
        self.data = data
        self.next = next

class LinkedList:
    def __init__(self):
        self.head = new Node(None, None)
        self.size = 0

    def add(self, item, index):
        current = self.head
        for i in range(0, index):
            current = current.next
        node = new Node(item, current.next)
        current.next = node
        self.size = self.size + 1
```

#### Doubly Linked List

```python
class Node:
    def __init__(self, data, prev, next):
        self.data = data
        self.prev = prev
        self.next = next

class LinkedList:
    def __init__(self):
        self.head = new Node(None, None, None)
        self.tail = new Node(None, self.head, None)
        self.head = self.tail
        self.size = 0

    def add(self, item, index):
        current = self.head
        for i in range(0, index):
            current = current.next
        node = new Node(item, current.prev, current)
        node.prev.next = node
        current.prev = node
        size += 1
```

