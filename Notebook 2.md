# Notebook 2

This notebook will add an entry to the Hash Table. Click [**here**](https://colab.research.google.com/drive/1aZeKa7n3quPHX3sEV9304Era3JnHCIEK?usp=sharing) to access it.

## Task 1

Inside the first cell, create a `Node` class.
```python
class Node:
    def __init__(self, key, value):
        self.key = key
        self.value = value
        self.next = None
```
Run the cell.
## Task 2

Whenever an entry is inserted:

1. Process the key into a `hash()` function.
2. Performing a bitwise `&` operation between the length and the unique hash.
3. Insert your node at the computed index.

```python
    def insert(self, key, value):
        if not self.buckets:
            self.buckets = [None] * 16

        hash_key = hash(key)   ## <---- step 1
        index = (len(self.buckets) - 1) & hash_key ## <---- step 2
        node = Node(key, value) ## <----- step 3
        self.buckets[index] = node ## <----- step 3
```

## Task 3

Run all cells.

![Screen Shot 2023-02-20 at 1.43.02 AM.png](https://firebasestorage.googleapis.com/v0/b/learnthepart-75aed.appspot.com/o/images%2Ffc933be1-a741-4009-988f-6f568281aff4?alt=media&token=bdc86354-54c9-453f-a0af-e33bef5ce850)

Your inventory should now contain `Apples`.

```
BUCKET 0
None

BUCKET 1
None

BUCKET 2
key = Apple, value = 2.99

BUCKET 3
None

...
```
## Solution

You can access the solution code [**here**](https://colab.research.google.com/drive/1-tS56ISbx67kL7129GpVYmkX7ONQxT7Y?usp=sharing).

------
##### This workbook was created by Jad and Rayan Slim. Feel free to explore some of their courses:
##### [The Complete Java Development Bootcamp](https://udemy-redirect-app.herokuapp.com/java)
##### [The Complete Spring Boot Development Bootcamp – Become a Java Web Developer](https://udemy-redirect-app.herokuapp.com/spring)