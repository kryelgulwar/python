# Python Lists
- Lists are ordered collection of data items.
 - They store multiple items in a single variable.
 - List items are separated by commas and enclosed within square brackets [].
 - Lists are changeable meaning we can alter them after creation.

Example 1:
```python
lst1 = [1,2,2,3,5,4,6]
lst2 = ["Red", "Green", "Blue"]
print(lst1)
print(lst2)
```
Output:
```
[1, 2, 2, 3, 5, 4, 6]
['Red', 'Green', 'Blue']
```

Example 2:
```python
details = ["Abhijeet", 18, "FYBScIT", 9.8]
print(details)
```
Output:
```
['Abhijeet', 18, 'FYBScIT', 9.8]
```
As we can see, a single list can contain items of different data types.

# List Index
Each item/element in a list has its own unique index. This index can be used to access any particular item from the list. The first item has index [0], second item has index [1], third item has index [2] and so on.

#### Example:
```python
colors = ["Red", "Green", "Blue", "Yellow", "Green"]
#          [0]      [1]     [2]      [3]      [4]
 ```

# Accessing list items
 We can access list items by using its index with the square bracket syntax []. For example colors[0] will give "Red", colors[1] will give "Green" and so on...

## Positive Indexing:
As we have seen that list items have index, as such we can access items using these indexes.

#### Example:
```python
colors = ["Red", "Green", "Blue", "Yellow", "Green"]
#          [0]      [1]     [2]      [3]      [4]
print(colors[2])
print(colors[4])
print(colors[0])
```
#### Output:
```
Blue
Green
Red
 ```

## Negative Indexing:
Similar to positive indexing, negative indexing is also used to access items, but from the end of the list. The last item has index [-1], second last item has index [-2], third last item has index [-3] and so on.

#### Example:
```python
colors = ["Red", "Green", "Blue", "Yellow", "Green"]
#          [-5]    [-4]    [-3]     [-2]      [-1]
print(colors[-1])
print(colors[-3])
print(colors[-5])
```
#### Output:
```
Green
Blue
Red
```

## Check whether an item in present in the list?
We can check if a given item is present in the list. This is done using the `in` keyword.
```python
colors = ["Red", "Green", "Blue", "Yellow", "Green"]
if "Yellow" in colors:
    print("Yellow is present.")
else:
    print("Yellow is absent.")
  ```
#### Output:

```
Yellow is present.
```
 
```python
colors = ["Red", "Green", "Blue", "Yellow", "Green"]
if "Orange" in colors:
    print("Orange is present.")
else:
    print("Orange is absent.")
```
#### Output:
```
Orange is absent.
```

## Range of Index:
You can print a range of list items by specifying where you want to start, where do you want to end and if you want to skip elements in between the range. 

Syntax:
```python
listName[start : end : jumpIndex]
```
Note: jump Index is optional. We will see this in later examples.

 

### Example: printing elements within a particular range:
```python
animals = ["cat", "dog", "bat", "mouse", "pig", "horse", "donkey", "goat", "cow"]
print(animals[3:7])	#using positive indexes
print(animals[-7:-2])	#using negative indexes'
```
#### Output:
```
['mouse', 'pig', 'horse', 'donkey']
['bat', 'mouse', 'pig', 'horse', 'donkey']
```
Here, we provide index of the element from where we want to start and the index of the element till which we want to print the values.

Note: The element of the end index provided will not be included. 

 

### Example: printing all element from a given index till the end
```python
animals = ["cat", "dog", "bat", "mouse", "pig", "horse", "donkey", "goat", "cow"]
print(animals[4:])	#using positive indexes
print(animals[-4:])	#using negative indexes
```
### Output:
```
['pig', 'horse', 'donkey', 'goat', 'cow']
['horse', 'donkey', 'goat', 'cow']
```
When no end index is provided, the interpreter prints all the values till the end.

 

### Example: printing all elements from start to a given index
```python
animals = ["cat", "dog", "bat", "mouse", "pig", "horse", "donkey", "goat", "cow"]
print(animals[:6])	#using positive indexes
print(animals[:-3])	#using negative indexes
```
#### Output:
```
['cat', 'dog', 'bat', 'mouse', 'pig', 'horse']
['cat', 'dog', 'bat', 'mouse', 'pig', 'horse']
```
When no start index is provided, the interpreter prints all the values from start up to the end index provided. 

 

### Example: Printing alternate values
```python
animals = ["cat", "dog", "bat", "mouse", "pig", "horse", "donkey", "goat", "cow"]
print(animals[::2])		#using positive indexes
print(animals[-8:-1:2])	#using negative indexes
```
### Output:
```
['cat', 'bat', 'pig', 'donkey', 'cow']
['dog', 'mouse', 'horse', 'goat']
```
Here, we have not provided start and index, which means all the values will be considered. But as we have provided a jump index of 2 only alternate values will be printed. 

 

### Example: printing every 3rd consecutive value withing a given range
```python
animals = ["cat", "dog", "bat", "mouse", "pig", "horse", "donkey", "goat", "cow"]
print(animals[1:8:3])
```
### Output:
```
['dog', 'pig', 'goat
```
Here, jump index is 3. Hence it prints every 3rd element within given index.

# List Comprehension
List comprehensions are used for creating new lists from other iterables like lists, tuples, dictionaries, sets, and even in arrays and strings.

 

## Syntax:

List = [Expression(item) for item in iterable if Condition]

**Expression**: It is the item which is being iterated.

**Iterable**: It can be list, tuples, dictionaries, sets, and even in arrays and strings.

**Condition**: Condition checks if the item should be added to the new list or not. 

 

### Example 1: Accepts items with the small letter “o” in the new list 
```python
names = ["Milo", "Sarah", "Bruno", "Anastasia", "Rosa"]
namesWith_O = [item for item in names if "o" in item]
print(namesWith_O)
```
### Output:
```
['Milo', 'Bruno', 'Rosa']
 ```

### Example 2: Accepts items which have more than 4 letters
```python
names = ["Milo", "Sarah", "Bruno", "Anastasia", "Rosa"]
namesWith_O = [item for item in names if (len(item) > 4)]
print(namesWith_O)
```
### Output:
```
['Sarah', 'Bruno', 'Anastasia']
```
# List Methods
## list.sort()
This method sorts the list in ascending order. The original list is updated
the sort() method modifies the list in place and does not return anything.
### Example 1:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors.sort()
print(colors)

num = [4,2,5,3,6,1,2,1,2,8,9,7]
num.sort()
print(num)
```
### Output:
```
['blue', 'green', 'indigo', 'voilet']\
[1, 1, 2, 2, 2, 3, 4, 5, 6, 7, 8, 9]
 
```

### Example 2:
```python
colors = ["voilet", "indigo", "blue", "green"]
print(colors.sort())
colors = colors.sort()
print(colors)
```
### Output:
```
None
None
 
```
The reason for the None output in your original code is that the sort() method modifies the list in place and does not return anything. In Python, in-place operations like sort() return None to avoid confusion, as they directly change the list's order without creating a new list.
Mistake: Assigning sort() Result
When you assign animals = animals.sort(), what you're doing is assigning None (the return value of sort()) to animals, which is why printing animals afterwards results in None.

Correct Usage:
Use animals.sort() to sort the list in place, without assignment.
Use sorted(animals) if you want a new, sorted version of the list without altering the original.

### Example :
```python
# Sorting in place (modifies original list)
animals = ["cat", "dog", "bat", "mouse"]
animals.sort()
print(animals)  # ['bat', 'cat', 'dog', 'mouse']

# Attempting to assign the result of sort() (returns None)
animals = ["cat", "dog", "bat", "mouse"]
sorted_list = animals.sort()  # sorted_list will be None
print(sorted_list)  # None

# Using sorted() to get a new sorted list
animals = ["cat", "dog", "bat", "mouse"]
sorted_animals = sorted(animals)  # Returns a new sorted list
print(sorted_animals)  # ['bat', 'cat', 'dog', 'mouse']

```

What if you want to print the list in descending order?\
We must give reverse=True as a parameter in the sort method.

### Example:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors.sort(reverse=True)
print(colors)

num = [4,2,5,3,6,1,2,1,2,8,9,7]
num.sort(reverse=True)
print(num)
```
#### Output:
```
['voilet', 'indigo', 'green', 'blue']
[9, 8, 7, 6, 5, 4, 3, 2, 2, 2, 1, 1]
 ```

The reverse parameter is set to False by default.

Note: Do not mistake the reverse parameter with the reverse method.

 

## reverse()
This method reverses the order of the list. 

#### Example:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors.reverse()
print(colors)

num = [4,2,5,3,6,1,2,1,2,8,9,7]
num.reverse()
print(num)
```
#### Output:
```
['green', 'blue', 'indigo', 'voilet']
[7, 9, 8, 2, 1, 2, 1, 6, 3, 5, 2, 4]
 ```

## index()
This method returns the index of the first occurrence of the list item.
#### Example:
```python
colors = ["voilet", "green", "indigo", "blue", "green"]
print(colors.index("green"))

num = [4,2,5,3,6,1,2,1,3,2,8,9,7]
print(num.index(3))
```
Output:
```
1
3
 ```

## count()
Returns the count of the number of items with the given value.
#### Example:
```python
colors = ["voilet", "green", "indigo", "blue", "green"]
print(colors.count("green"))

num = [4,2,5,3,6,1,2,1,3,2,8,9,7]
```
#### Output:
```
2
3
 ```

## copy()
Returns copy of the list. This can be done to perform operations on the list without modifying the original list. 

#### Example:
```python
colors = ["voilet", "green", "indigo", "blue"]
newlist = colors.copy()
print(colors)
print(newlist)
```
#### Output:
```
['voilet', 'green', 'indigo', 'blue']
['voilet', 'green', 'indigo', 'blue']
```
## Add List items
These are the ways to add any item in list

## append():
This method appends items to the end of the existing list.

#### Example:
```python
colors = ["voilet", "indigo", "blue"]
colors.append("green")
print(colors)
```
#### Output:
```
['voilet', 'indigo', 'blue', 'green']
 ```
## insert():
This method inserts an item at the given index. User has to specify index and the item to be inserted within the insert() method.

#### Example:
```python
colors = ["voilet", "indigo", "blue"]
#           [0]        [1]      [2]

colors.insert(1, "green")   #inserts item at index 1
# updated list: colors = ["voilet", "green", "indigo", "blue"]
#       indexs              [0]       [1]       [2]      [3]

print(colors)
```
#### Output:
```
['voilet', 'green', 'indigo', 'blue']
 ```
## extend():
This method adds an entire list or any other collection datatype (set, tuple, dictionary) to the existing list.

#### Example 1:
```python
#add a list to a list
colors = ["voilet", "indigo", "blue"]
rainbow = ["green", "yellow", "orange", "red"]
colors.extend(rainbow)
print(colors)
```
#### Output:
```
['voilet', 'indigo', 'blue', 'green', 'yellow', 'orange', 'red']
 ```
#### Example 2:
```python
thislist = ["apple", "banana", "cherry"]
thistuple = ("kiwi", "orange")
thislist.extend(thistuple)
print(thislist))
```
#### Output:
```
['apple', 'banana', 'cherry', 'kiwi', 'orange']
 ```

## Concatenating two lists:
You can simply concatenate two lists to join two lists.

#### Example:
```python
colors = ["voilet", "indigo", "blue", "green"]
colors2 = ["yellow", "orange", "red"]
print(colors + colors2)
```
#### Output:
```
['voilet', 'indigo', 'blue', 'green', 'yellow', 'orange', 'red']
```
## Remove List items
These are the methods to remove any item in list

## remove()
The remove() method removes the specified item.

#### Example 1:
```python
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
```
#### Output:
```
['apple', 'cherry']
```
If there are more than one item with the specified value, the remove() method removes the first occurrence:
#### Example 2:
```python
thislist = ["apple", "banana", "cherry", "banana", "kiwi"]
thislist.remove("banana")
print(thislist)
```
#### Output:
```
['apple', 'cherry', 'banana', 'kiwi']
```

## pop()
The pop() method removes the specified index.
If you do not specify the index, the pop() method removes the last item.

#### Example 1:
```python
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)
```
#### Output:
```
['apple', 'cherry']
```

#### Example 2:
```python
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)
```
#### Output:
```
['apple', 'banana']
```

## clear()
The clear() method empties the list.
#### Example :
```python
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)
```
#### Output:
```
[]
```

## del
The del keyword can also delete the list completely.
#### Example :
```python
thislist = ["apple", "banana", "cherry"]
del thislist
print(thislist) #this will cause an error because you have succsesfully deleted "thislist".
```
#### Output:
```
NameError: name 'thislist' is not defined
```
