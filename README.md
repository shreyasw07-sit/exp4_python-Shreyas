# exp4_python-Shreyas
Experiment 4: Study of Set in Python
Name: Shreyas

PRN: 25070123131

1. Introduction to Sets
A Set in Python is an unordered collection of unique elements. They are defined by placing elements inside curly braces {} or by using the set() constructor.

Key Characteristics:

Unordered: The items do not have a defined order; they may appear in a different order every time you use them.

Unchangeable: You cannot change items after the set is created, but you can remove items and add new items.

No Duplicates: Sets automatically filter out duplicate values.

Heterogeneous: A single set can contain different data types (integers, strings, booleans, etc.).

2. Code Implementation & Operations
The following sections break down the operations performed in the exp4.ipynb notebook.

A. Basic Set Creation and Data Types

Sets can store various data types. Note that in Python, True and 1 are treated as the same value, so only one will be kept.

Python
# Simple string set
set1 = {"apple", "banana", "cherry"}

# Mixed data types
set2 = {2, 2.5, True, "lambda"}

# Handling duplicates (1 and True are considered duplicates)
set3 = {"apple", 2, True, 1, "apple"} 
# Output: {'apple', 2, True}
B. Modifying a Set

You can grow or shrink a set using built-in methods.

add(): Adds a single element.

remove(): Removes a specific element (raises an error if the element is not found).

discard(): Removes a specific element (does not raise an error if the element is missing).

Python
# Adding an item
set4 = {"apple", "banana", "cherry"}
set4.add("kiwi")

# Removing an item
set5 = {"apple", "banana", "cherry"}
set5.remove("banana")

# Discarding an item
courses = {"python", "maths", "dawl"}
courses.discard("dawl")
C. Mathematical Set Operations

Python sets support standard mathematical operations using operators or methods.

Operation	Operator	Description
Union	|	All elements from both sets.
Intersection	&	Only elements present in both sets.
Difference	-	Elements in the first set but not the second.
Symmetric Difference	^	Elements in either set, but not both.
Python
set6 = {1, 2, 3, 4}
set7 = {3, 4, 5, 6}

print(set6 | set7) # Union: {1, 2, 3, 4, 5, 6}
print(set6 & set7) # Intersection: {3, 4}
print(set6 - set7) # Difference: {1, 2}
D. Frozen Sets

A frozenset is an immutable version of a Python set. Once created, elements cannot be added or removed.

Python
set8 = frozenset({"apple", "banana", "orange"})
# set8.add("grape")  # This would raise an AttributeError
3. Practical Applications
The notebook demonstrates several real-world logic patterns using sets:

Finding Unique Items: Converting a list with duplicates (like a participant list) into a set to find the unique count.

Finding Commonality: Using .intersection() across multiple sets (e.g., finding a common subject among multiple students).

Tracking Absence: Using .difference() to compare a master list of students against those present to identify who is absent.

4. Summary Table of Methods
Method	Description
add()	Adds an element to the set.
clear()	Removes all elements from the set.
difference()	Returns a set containing the difference between two or more sets.
intersection()	Returns a set that is the intersection of two other sets.
union()	Return a set containing the union of sets.
frozenset()	Returns an immutable frozenset object.
