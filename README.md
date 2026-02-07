# AIM: To Study Set and Dictionaries In Python
## Objective
To understand and study the fundamental concepts, operations, and applications of **Sets** and **Dictionaries** in Python.
## THEORY:
## 1. Sets in Python

### What is a Set?
- A set is an **unordered** collection of **unique** elements.
- Sets are **mutable** (you can add or remove items after creation).
- No duplicate values are allowed — duplicates are automatically removed.
- Sets are written inside curly braces `{ }`.

### Key Properties
- Unordered = elements have no fixed position/index
- Unique = duplicate items are ignored
- Mutable (except frozenset)
- Cannot contain mutable elements like lists or dictionaries

### Creating a Set
Example:  
fruits = {'apple', 'banana'}  
Output: {'apple', 'banana'} (order may be different)

### Membership Testing (Checking if item exists)
Example:  
thisset = {'guava', 'banana', 'mango'}  
'banana' in thisset = True  
'apple' in thisset = False

### Adding Elements
Use .add() to add one item  
Use .update() to add multiple items (from list, tuple, another set, etc.)

Example:  
thisset = {'grapes', 'lichhi'}  
thisset.add('orange')  
Result: {'grapes', 'lichhi', 'orange'}

### Removing Elements
.remove(item) = removes item, raises error if not found  
.discard(item) = removes item, no error if not found  
.pop() = removes and returns arbitrary item

Example:  
thisset = {'grapes', 'lichhi'}  
thisset.remove('grapes')  
Result: {'lichhi'}

### Set Operations

Union (all elements from both sets)  
a = {1, 2, 3, 4, 5}  
b = {3, 4, 6, 7}  
Union :{1, 2, 3, 4, 5, 6, 7}

Intersection (common elements)  
Intersection : {3, 4}

Difference (elements in first set but not in second)  
Difference (a - b) = {1, 2, 5}

Symmetric Difference (elements in either set but not both)  
Symmetric Difference = {1, 2, 5, 6, 7}

### Frozenset
- Immutable version of a set
- Cannot be changed after creation (no add, remove, update)
- Can be used as dictionary key or added to another set

Example:  
names = frozenset({'ayush', 'arjit', 'bedang', 'kushal'})  
Trying to do names.add('new') = Error

### Important Set Methods
- .add() = add single element
- .update() = add multiple elements
- .remove() / .discard() = remove element
- .clear() = remove all elements
- .union() / | = combine sets
- .intersection() / & : common elements
- .difference() / - : elements only in first set
- .symmetric_difference() / ^ : elements in exactly one set

## 2. Dictionaries in Python

### What is a Dictionary?
- A dictionary is an **ordered** (Python 3.7+) collection of **key-value** pairs.
- Keys must be **unique** and **immutable** (string, number, tuple)
- Values can be any data type (list, dict, set, etc.)
- Written inside curly braces with key:value format

### Creating a Dictionary
Example:  
car = {  
    "brand": "ferrari",  
    "model": "G7",  
    "year": 1884  
}

### Accessing Values
Using key name:  
car["model"] = G7

Using .get() method (safer):  
car.get("brand") = ferrari  
car.get("color") = None (no error)

### Adding / Updating Values
car["color"] = "red" : adds new key-value  
car["year"] = 2025 : updates existing value

### Removing Elements
.pop("key") = removes key and returns its value  
.del car["key"] = deletes key  
.popitem() = removes last inserted item (Python 3.7+)

Example:  
car.pop("color")  
Result: removes color key

### Dictionary Views
.keys() = returns all keys  
.values() = returns all values  
.items() = returns all key-value pairs as tuples

### Important Dictionary Properties
- Ordered (insertion order preserved since Python 3.7)
- Mutable
- Keys are unique
- Keys must be immutable
- Values can be duplicated

## Real-World Applications (Theory)

### Sets Applications
- Removing duplicates from a list
- Finding common / unique items between groups
- Membership testing (very fast)
- Mathematical set operations (union, intersection, difference)

Examples:
- Unique participants in an event
- Students present in both cricket and football club
- Common subjects chosen by multiple students
- Finding absent students

### Dictionaries Applications
- Storing related information (student name → marks)
- Quick lookup using keys
- Counting frequency of items
- Configuration / settings storage
- User login credentials validation

Examples:
- Product name = price
- Student name = marks
- Username = password
- Finding highest scorer

## Conclusion
Sets are powerful for handling unique items and performing mathematical operations efficiently.  
Dictionaries are excellent for storing and retrieving data using meaningful keys quickly.
Both are very important built-in data structures in Python and are widely used in real-world programming.
