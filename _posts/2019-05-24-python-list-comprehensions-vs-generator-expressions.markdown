---
layout: post
title:  "Python List Comprehensions Vs Generator Expressions"
date:   2019-05-24 13:27:34 +0100
---

## List Comprehensions

What are list comprehensions? They are a simple way of defining and creating a list. They create lists using for loops, but instead of using 3 lines of code list comprehensions allow us to write them in just 1.

### Example

```
list_comprehension = []

for i in range(10):
    if i % 2 == 0:
        list_comprehension.append(i)

print(list_comprehension)
```
Can be reduced down to

```
list_comprehension = [i for i in range(10) if i % 2 == 0]
print(list_comprehension)
```
Once the list is created, the entire contents are stored in memory.

## Generator Expressions

So what are generator expressions? They are similar to list comprehensions in the sense that they are a way of defining and creating an iterable object but a generator expression does not store the whole output in memory immediately, but instead generates each value on the fly as it is needed. This makes them very memory efficient, since only one value is stored in memory at a time.

### Example

A generator expression has a similar syntax to a list comprehension, but instead of square brackets, it is surrounded by parentheses:

```
generator = (i for i in range(10) if i % 2 == 0)
```

## Use Cases

List comprehensions are best suited to algorithms where the list will be small, or where memory usage isn't a concern. On the other hand generator expressions are better suited to algorithms where memory usage needs to be minimal, or where the generator expression is doing very expensive work for each iteration, and doing that work upfront has no benefit.