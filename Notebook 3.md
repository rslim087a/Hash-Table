# Notebook 3

This notebook will modify the insert logic to account for collisions. Click [**here**](https://colab.research.google.com/drive/1nykpSykT_-zW5WXVwP_AILitCCnx7cne?usp=sharing) to access it.

## Task 1

Inside the `HashTable` class, add another function called `insert_node`.
```python
    def insert_node(self, buckets, index, node):
        if not buckets[index]:
            buckets[index] = node
        else:
            curr_node = buckets[index]
            while curr_node.next:
                curr_node = curr_node.next
            curr_node.next = node
```
First, the method checks whether the bucket at the given index is empty. If so, the node is simply added to the bucket.

```python
    def insert_node(self, buckets, index, node):
        if not buckets[index]:
            buckets[index] = node
        ## ...
```
If the bucket is not empty, the code finds the last node in the bucket and adds the new node as the next one to it. This makes the new node the last one in the bucket.

```python
    def insert_node(self, buckets, index, node):
        ## ...
        else:
            curr_node = buckets[index]
            while curr_node.next:
                curr_node = curr_node.next
            curr_node.next = node
```

## Task 2

After creating the node to be inserted, call insert_node.
```python
    def insert(self, key, value):
        ...
        node = Node(key, value)
        self.insert_node(self.buckets, index, node)
```

## Task 3

Run all cells.

```
BUCKET 0
key = Cucumber, value = 1.29

BUCKET 1
key = Papaya, value = 5.99
key = Carrot, value = 1.49

BUCKET 2
key = Tomato, value = 1.99

BUCKET 3
key = Kale, value = 4.99

BUCKET 4
None

BUCKET 5
None

BUCKET 6
key = Watermelon, value = 7.99

BUCKET 7
None

BUCKET 8
key = Spinach, value = 2.99
key = Broccoli, value = 2.49
key = Orange, value = 2.49

BUCKET 9
None

BUCKET 10
key = Apple, value = 1.99
key = Lemon, value = 0.99

BUCKET 11
None

BUCKET 12
None

BUCKET 13
key = Mango, value = 3.99

BUCKET 14
None

BUCKET 15
key = Banana, value = 2.99
```

## Solution

You can access the solution code [**here**](https://colab.research.google.com/drive/1WYdL7kAkVh3SwVwtxIfueudiZmk_NPg4?usp=sharing).

------
##### This workbook was created by Jad and Rayan Slim. Feel free to explore some of their courses:
##### [The Complete Java Development Bootcamp](https://udemy-redirect-app.herokuapp.com/java)
##### [The Complete Spring Boot Development Bootcamp – Become a Java Web Developer](https://udemy-redirect-app.herokuapp.com/spring)