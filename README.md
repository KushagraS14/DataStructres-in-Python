Python Basics - Easy Explanation 📘
This notebook covers fundamental Python concepts in simple terms.

1. Hello World 👋
python
print("Hello World")
print() displays text on screen

Text inside quotes is called a "string"

2. Variables 📦
Variables are like containers that store data:

python
a = 10          # Stores whole number (integer)
b = 10.5        # Stores decimal number (float)
c = "hello"     # Stores text (string)
d = 5 + 3j      # Stores complex number
Key Points:

= means "store this value in this variable"

Python automatically detects the type of data

Variable names can't start with numbers or contain spaces

3. Data Types 🔤
Every value has a type:

int: Whole numbers (10, -5, 0)

float: Decimal numbers (10.5, 3.14)

str: Text ("hello", "Python")

complex: Complex numbers (5+3j)

bool: True/False values

4. Getting User Input 🎤
python
name = input("Enter your name: ")
input() pauses the program and waits for user to type

Whatever you type gets stored in the variable name

5. Converting Data Types 🔄
Sometimes you need to change data types:

python
number = float(input("Enter a number: "))
input() always gives you text (string)

float() converts text to decimal number

int() converts text to whole number

str() converts number to text

6. Advanced Printing ✨
Using separators:

python
print("Hello", "World", sep="+")  # Output: Hello+World
Controlling line endings:

python
print("Line 1", end=",")
print("Line 2")  # Output: Line 1,Line 2
Formatting output:

python
name = "John"
age = 25
print(f"{name} is {age} years old")  # Modern way
print("{} is {} years old".format(name, age))  # Another way
7. Math Operations ➕➖✖️➗
python
a = 10
b = 3

print(a + b)   # Addition: 13
print(a - b)   # Subtraction: 7
print(a * b)   # Multiplication: 30
print(a / b)   # Division: 3.333...
print(a // b)  # Integer division: 3
print(a % b)   # Remainder: 1
print(a ** b)  # Power: 1000 (10³)
8. Making Decisions (if-elif-else) 🤔
python
weather = input("What's the weather? ")

if weather == "Rainy":
    print("Take an umbrella ☔")
elif weather == "Sunny":
    print("Wear sunglasses 😎")
else:
    print("Have a nice day! 😊")
How it works:

Check first condition

If true, run its code and stop

create a readme for data structures in python
📚 Data Structures in Python
A comprehensive guide to Python's built-in data structures with practical examples

🗂️ Table of Contents
Lists

Tuples

Dictionaries

Sets

Strings

Arrays

Stacks & Queues

Linked Lists

Trees

Graphs

Performance Comparison

📋 Lists [ ]
Lists are ordered, mutable collections that can hold items of different types.

🔧 Basic Operations
python
# Creating lists
fruits = ['apple', 'banana', 'cherry']
numbers = [1, 2, 3, 4, 5]
mixed = [1, 'hello', 3.14, True]

# Accessing elements
print(fruits[0])     # 'apple' (zero-based indexing)
print(fruits[-1])    # 'cherry' (negative indexing)

# Slicing
print(numbers[1:4])  # [2, 3, 4]
print(numbers[:3])   # [1, 2, 3]
print(numbers[2:])   # [3, 4, 5]

# Length
print(len(fruits))   # 3
✨ List Methods
python
fruits = ['apple', 'banana']

# Adding elements
fruits.append('cherry')      # ['apple', 'banana', 'cherry']
fruits.insert(1, 'orange')   # ['apple', 'orange', 'banana', 'cherry']
fruits.extend(['grape', 'mango'])  # Extend with another list

# Removing elements
fruits.remove('banana')      # Remove specific element
popped = fruits.pop()        # Remove and return last element
popped = fruits.pop(1)       # Remove element at index 1

# Searching
index = fruits.index('apple')  # Find index of element
count = fruits.count('apple')  # Count occurrences

# Sorting
numbers = [3, 1, 4, 1, 5]
numbers.sort()                # In-place sort: [1, 1, 3, 4, 5]
sorted_nums = sorted(numbers) # Return new sorted list

# Reversing
fruits.reverse()              # Reverse in-place
📝 List Comprehensions (Pythonic Way!)
python
# Create a list of squares
squares = [x**2 for x in range(10)]
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# With condition
evens = [x for x in range(10) if x % 2 == 0]
# [0, 2, 4, 6, 8]

# Nested comprehensions
matrix = [[j for j in range(5)] for i in range(3)]
# [[0, 1, 2, 3, 4], [0, 1, 2, 3, 4], [0, 1, 2, 3, 4]]
📦 Tuples ( )
Tuples are ordered, immutable sequences. Use them when you need data that shouldn't change.

🔧 Basic Operations
python
# Creating tuples
coordinates = (10, 20)
single_item = (5,)      # Note: comma is required!
mixed = (1, 'hello', 3.14)

# Accessing (same as lists)
print(coordinates[0])   # 10
print(coordinates[-1])  # 20

# Tuples are immutable - this will ERROR:
# coordinates[0] = 100  ❌

# Packing and unpacking
point = (3, 4)
x, y = point            # x=3, y=4

# Multiple return values
def get_dimensions():
    return 100, 200
    
width, height = get_dimensions()
🎯 When to Use Tuples
Return multiple values from functions

Dictionary keys (lists can't be keys!)

Data that shouldn't change (constants, configurations)

Memory efficiency (tuples use less memory than lists)

📖 Dictionaries { }
Dictionaries store key-value pairs and are unordered (Python 3.7+: insertion order preserved).

🔧 Basic Operations
python
# Creating dictionaries
student = {
    'name': 'Alice',
    'age': 21,
    'courses': ['Math', 'Physics']
}

# Accessing values
print(student['name'])          # 'Alice'
print(student.get('age'))       # 21
print(student.get('grade'))     # None (instead of error)
print(student.get('grade', 'A')) # 'A' (default value)

# Adding/Updating
student['grade'] = 'A'          # Add new key
student['age'] = 22             # Update existing key
student.update({'grade': 'B', 'city': 'NYC'})

# Removing
grade = student.pop('grade')    # Remove and return value
del student['city']             # Delete key
student.clear()                 # Remove all items
✨ Dictionary Methods
python
person = {'name': 'Bob', 'age': 30}

# Get all keys, values, or items
keys = person.keys()      # dict_keys(['name', 'age'])
values = person.values()  # dict_values(['Bob', 30])
items = person.items()    # dict_items([('name', 'Bob'), ('age', 30)])

# Dictionary comprehensions
squares = {x: x**2 for x in range(5)}
# {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

# Merging dictionaries (Python 3.9+)
dict1 = {'a': 1, 'b': 2}
dict2 = {'b': 3, 'c': 4}
merged = dict1 | dict2    # {'a': 1, 'b': 3, 'c': 4}
🎯 Sets { }
Sets are unordered collections of unique elements. Perfect for membership tests and eliminating duplicates.

🔧 Basic Operations
python
# Creating sets
fruits = {'apple', 'banana', 'cherry'}
numbers = set([1, 2, 3, 4, 5])  # From list

# Adding elements
fruits.add('orange')
fruits.update(['grape', 'mango'])  # Add multiple

# Removing elements
fruits.remove('banana')    # Error if not found
fruits.discard('banana')   # No error if not found
popped = fruits.pop()      # Remove arbitrary element

# Set operations
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

print(A | B)   # Union: {1, 2, 3, 4, 5, 6}
print(A & B)   # Intersection: {3, 4}
print(A - B)   # Difference: {1, 2}
print(A ^ B)   # Symmetric Difference: {1, 2, 5, 6}
🎯 When to Use Sets
python
# Removing duplicates from a list
numbers = [1, 2, 2, 3, 3, 3]
unique = list(set(numbers))  # [1, 2, 3]

# Membership testing (FASTER than lists)
if 'apple' in fruits:        # O(1) for sets
    print("Found apple!")    # O(n) for lists

# Finding common elements
group1 = {'Alice', 'Bob', 'Charlie'}
group2 = {'Bob', 'David', 'Eve'}
common = group1 & group2     # {'Bob'}
🔤 Strings
Strings are immutable sequences of characters with many useful methods.

🔧 String Operations
python
text = "Hello, Python!"

# Accessing characters
print(text[0])     # 'H'
print(text[-1])    # '!'
print(text[7:13])  # 'Python'

# Common methods
print(text.lower())       # 'hello, python!'
print(text.upper())       # 'HELLO, PYTHON!'
print(text.split(','))    # ['Hello', ' Python!']
print(text.replace('!', '!!'))  # 'Hello, Python!!'

# Checking
print(text.startswith('Hello'))  # True
print(text.endswith('!'))        # True
print('Python' in text)          # True

# Formatting (multiple ways)
name = "Alice"
age = 25

# f-strings (Python 3.6+ - RECOMMENDED)
message = f"{name} is {age} years old"

# format() method
message = "{} is {} years old".format(name, age)

# Old style
message = "%s is %d years old" % (name, age)
📝 Useful String Methods
python
text = "  hello world  "

# Stripping whitespace
print(text.strip())        # 'hello world'
print(text.lstrip())       # 'hello world  '
print(text.rstrip())       # '  hello world'

# Joining strings
words = ['Hello', 'World', 'Python']
sentence = ' '.join(words)  # 'Hello World Python'

# Checking content
print('hello123'.isalnum())   # True (letters and numbers)
print('hello'.isalpha())      # True (only letters)
print('123'.isdigit())        # True (only digits)
print('   '.isspace())        # True (only spaces)
🔢 Arrays
For numerical computations, use array module or NumPy arrays (more efficient than lists).

Using array Module
python
from array import array

# Create array of integers
numbers = array('i', [1, 2, 3, 4, 5])  # 'i' = signed integer

# Operations similar to lists
numbers.append(6)
numbers.extend([7, 8])
print(numbers[0])  # 1
NumPy Arrays (Recommended for Math/Science)
python
import numpy as np

# Create numpy arrays
arr = np.array([1, 2, 3, 4, 5])
matrix = np.array([[1, 2, 3], [4, 5, 6]])

# Vectorized operations (FAST!)
print(arr * 2)           # [2, 4, 6, 8, 10]
print(arr + arr)         # [2, 4, 6, 8, 10]
print(np.mean(arr))      # 3.0 (average)
🥞 Stacks & Queues
Stack (LIFO - Last In First Out)
python
# Using list as stack
stack = []
stack.append(10)        # Push
stack.append(20)
stack.append(30)

print(stack.pop())      # 30 (Pop)
print(stack.pop())      # 20
print(stack[-1])        # 10 (Peek) - without removing
Queue (FIFO - First In First Out)
python
from collections import deque

# Using deque as queue (efficient)
queue = deque()

# Enqueue
queue.append('Alice')
queue.append('Bob')
queue.append('Charlie')

# Dequeue
print(queue.popleft())  # 'Alice'
print(queue.popleft())  # 'Bob'
Priority Queue
python
import heapq

# Min-heap (smallest element first)
heap = []
heapq.heappush(heap, 5)
heapq.heappush(heap, 2)
heapq.heappush(heap, 8)

print(heapq.heappop(heap))  # 2
print(heapq.heappop(heap))  # 5
🔗 Linked Lists
While Python doesn't have built-in linked lists, you can implement them:

Singly Linked List
python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None
    
    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        current = self.head
        while current.next:
            current = current.next
        current.next = new_node
    
    def display(self):
        current = self.head
        while current:
            print(current.data, end=" -> ")
            current = current.next
        print("None")

# Usage
ll = LinkedList()
ll.append(1)
ll.append(2)
ll.append(3)
ll.display()  # 1 -> 2 -> 3 -> None
🌳 Trees
Binary Tree Implementation
python
class TreeNode:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

# Tree traversal methods
def inorder_traversal(root):
    if root:
        inorder_traversal(root.left)
        print(root.value)
        inorder_traversal(root.right)

def preorder_traversal(root):
    if root:
        print(root.value)
        preorder_traversal(root.left)
        preorder_traversal(root.right)

def postorder_traversal(root):
    if root:
        postorder_traversal(root.left)
        postorder_traversal(root.right)
        print(root.value)

# Create a tree
root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
root.left.left = TreeNode(4)
root.left.right = TreeNode(5)
Binary Search Tree (BST)
python
class BST:
    def __init__(self):
        self.root = None
    
    def insert(self, value):
        if not self.root:
            self.root = TreeNode(value)
        else:
            self._insert_recursive(self.root, value)
    
    def _insert_recursive(self, node, value):
        if value < node.value:
            if node.left is None:
                node.left = TreeNode(value)
            else:
                self._insert_recursive(node.left, value)
        else:
            if node.right is None:
                node.right = TreeNode(value)
            else:
                self._insert_recursive(node.right, value)
    
    def search(self, value):
        return self._search_recursive(self.root, value)
    
    def _search_recursive(self, node, value):
        if node is None or node.value == value:
            return node
        if value < node.value:
            return self._search_recursive(node.left, value)
        return self._search_recursive(node.right, value)
🕸️ Graphs
Adjacency List Representation
python
from collections import defaultdict

class Graph:
    def __init__(self):
        self.graph = defaultdict(list)
    
    def add_edge(self, u, v):
        self.graph[u].append(v)
        self.graph[v].append(u)  # For undirected graph
    
    def bfs(self, start):
        visited = set()
        queue = [start]
        visited.add(start)
        
        while queue:
            vertex = queue.pop(0)
            print(vertex, end=" ")
            
            for neighbor in self.graph[vertex]:
                if neighbor not in visited:
                    visited.add(neighbor)
                    queue.append(neighbor)
    
    def dfs(self, start):
        visited = set()
        self._dfs_recursive(start, visited)
    
    def _dfs_recursive(self, vertex, visited):
        visited.add(vertex)
        print(vertex, end=" ")
        
        for neighbor in self.graph[vertex]:
            if neighbor not in visited:
                self._dfs_recursive(neighbor, visited)

# Usage
g = Graph()
g.add_edge(0, 1)
g.add_edge(0, 2)
g.add_edge(1, 2)
g.add_edge(2, 3)

print("BFS:", end=" ")
g.bfs(0)  # 0 1 2 3

print("\nDFS:", end=" ")
g.dfs(0)  # 0 1 2 3
⚡ Performance Comparison
Data Structure	Access	Search	Insertion	Deletion	Use Case
List	O(1)	O(n)	O(1)*	O(n)	General purpose, ordered data
Tuple	O(1)	O(n)	N/A	N/A	Immutable sequences
Dictionary	O(1)	O(1)	O(1)	O(1)	Key-value lookups
Set	N/A	O(1)	O(1)	O(1)	Unique elements, membership tests
Deque	O(1)	O(n)	O(1)	O(1)	Queues and stacks
Heapq	O(1)	N/A	O(log n)	O(log n)	Priority queues
*O(1) for appending, O(n) for inserting at beginning

🎓 Best Practices
Choose the right tool for the job:

Need ordered data? → List

Need unique elements? → Set

Need key-value pairs? → Dictionary

Need immutable data? → Tuple

Use list comprehensions for cleaner code

Use defaultdict to avoid key errors

Use deque for queues (faster than list)

Remember: Strings are immutable!

Use NumPy arrays for numerical computations

Use collections module for specialized containers

📚 Further Learning
Built-in Modules:
collections: Specialized container datatypes

heapq: Heap queue algorithm (priority queue)

array: Efficient arrays of numeric values

bisect: Array bisection algorithms

External Libraries:
NumPy: Numerical computing with arrays

pandas: Data manipulation and analysis

scipy: Scientific computing

networkx: Graph creation and manipulation

