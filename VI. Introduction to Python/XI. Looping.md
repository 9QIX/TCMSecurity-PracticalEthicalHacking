# Python Loops

## For Loops

- Iterate through a sequence from start to finish
- Syntax: `for item in sequence:`

### Example:

```python
vegetables = ["cucumber", "spinach", "cabbage"]
for x in vegetables:
    print(x)
```

This will print each vegetable in the list on a new line.

## While Loops

- Execute as long as a condition is true
- Syntax: `while condition:`

### Example:

```python
i = 1
while i < 10:
    print(i)
    i += 1
```

This will print numbers from 1 to 9.

## Key Points

1. For loops are used to iterate through a known sequence (like a list).
2. While loops continue executing as long as a condition remains true.
3. The variable in a for loop (e.g., `x`) can be named anything.
4. `+=` is used to increment a variable (e.g., `i += 1` is equivalent to `i = i + 1`).
5. The instructor mentions that these concepts will be revisited later in the course, especially in the exploit development section.

The main takeaway is to understand the basic concept of each loop type:

- For loops: start-to-finish iteration of a sequence
- While loops: execution as long as a condition is true
