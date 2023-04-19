# Notebook 1

The aim of this notebook is to create a Hash Table. Click [**here**](https://colab.research.google.com/drive/1k7Ibn6BPcFlu-gecrnWDqppT2C4xCbio?usp=sharing) to access Notebook 1.

## Task 1

The first cell creates a `HashTable` class. Click `Shift` + `Enter` to run this cell.

```python
class HashTable:
    def __init__(self):
        self.size = 0
        self.buckets = []
```
If you are not signed into Google, it will prompt you to do so.

![Screen Shot 2023-02-20 at 4.32.02 PM.png](https://firebasestorage.googleapis.com/v0/b/learnthepart-75aed.appspot.com/o/images%2F5d42aaf4-5487-429c-86ca-5eae5e98d326?alt=media&token=a133110d-8134-4044-95cf-c66b3b0bbd88)

## Task 2

Add an `insert` method to the `HashTable` class.
```python
    def insert(self, key, value):
        if not self.buckets:
            self.buckets = [None] * 16
```
The `insert` method takes an **entry** consisting of a `key` and a `value`. The first line of the method checks if the hash table has any buckets. If it doesn't, the method initializes the array with the capacity to store 16 elements.

## Task 3

Rerun the cell (`Shift` + `Enter`) so that the changes are recognized.

## Task 4
Inside the second cell, create a `HashTable` object.
```python
inventory = HashTable()
```
Add the following entry into the `HashTable`.

```python
inventory = HashTable()
inventory.insert("Banana", 2.99)
```
Run the cell.

## Task 5

Inside the third cell, add code that displays the contents of our HashTable.
```python
def displayInventory():
    for index, item in enumerate(inventory.buckets):
        print("\nBUCKET {0}".format(index))
        print(item)
```
Run the cell
## Task 6

Inside the fourth cell, call `displayInventory()`.
```python
displayInventory()
```

Run every cell by clicking **Runtime** | **Run all**.

![Screen Shot 2023-02-20 at 1.43.02 AM.png](https://firebasestorage.googleapis.com/v0/b/learnthepart-75aed.appspot.com/o/images%2Ffc933be1-a741-4009-988f-6f568281aff4?alt=media&token=bdc86354-54c9-453f-a0af-e33bef5ce850)

Your final output should display a HashTable with 16 buckets.

```
BUCKET 0
None

BUCKET 1
None

BUCKET 2
None

...
```

## Solution

You can access the solution code [**here**](https://colab.research.google.com/drive/1PooQPpVEOWFy2YUw7Y8FF1iYac74EgfM?usp=sharing).

------
##### This workbook was created by Jad and Rayan Slim. Feel free to explore some of their courses:
##### [The Complete Java Development Bootcamp](https://udemy-redirect-app.herokuapp.com/java)
##### [The Complete Spring Boot Development Bootcamp – Become a Java Web Developer](https://udemy-redirect-app.herokuapp.com/spring)