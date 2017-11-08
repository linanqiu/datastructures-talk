# Practical Data Structures

---

## Calibration (0)

![Blank Derp](blank.jpg)

Data structures?

---

## Calibration (1)


- Big-O and complexity?
- Interfaces vs. Implementation

---

## Calibration (2)

- Arrays?
- Linked Lists?
- Stacks and Queues?
- Hashing? Maps?

---

## Calibration (3)

- Garbage collection?
- Immutability? Immutable data structures?
- Persistent data structures?

---

## Preface

- Language agnostic, so I used `python`
- Trigger warning for folks with Mathematics / CS Theory background (why are you here anyway?)

---

# Primers

---

## Data Structures

- Data lives in memory
- How we store that data in memory is important
- Computers are fast...but not that fast

---

## Big-O

$$f(x) = O(g(x))$$

if and only if

$$|f(x)| \leq M|g(x)|$$

for all $$x \geq x_0$$

---

![Big O](bigo.png)

---

## Complexity

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

## Interfaces vs Implementations

- Interfaces: what a data structure does.
    - e.g. A car should support the following operations: `accelerate`, `turn`, `brake`.
- Implementation: how a data structure does it
    - e.g. a Tesla implements `accelerate` electrically while a Honda implements `accelerate` by pumping fuel

Using queue,

- Interface: what the queue does:
    - Queues should support `enqueue` and `dequeue`
- Implementation: how the queue does it:
    - Array based / linked list / two stacks

---

# Common Data Structures

---

## Arrays



