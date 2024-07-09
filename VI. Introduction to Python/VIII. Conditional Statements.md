# Conditional Statements in Python

## Introduction

- Conditional statements are used for decision-making in programming
- They allow different code to be executed based on certain conditions

## Basic If-Else Structure

```python
def drink(money):
    if money >= 2:
        return "You've got yourself a drink"
    else:
        return "No drink for you"

print(drink(3))  # Output: You've got yourself a drink
print(drink(1))  # Output: No drink for you
```

## Multiple Conditions: If-Elif-Else

Example: Purchasing alcohol with age and money requirements

```python
def alcohol(age, money):
    if age >= 21 and money >= 5:
        return "We're getting a drink"
    elif age >= 21 and money < 5:
        return "Come back with more money"
    elif age < 21 and money >= 5:
        return "Nice try kid"
    else:
        return "You're too poor and too young"

print(alcohol(21, 5))  # Output: We're getting a drink
print(alcohol(21, 4))  # Output: Come back with more money
print(alcohol(20, 4))  # Output: You're too poor and too young
```

## Key Points

1. Conditional statements use `if`, `elif` (else if), and `else`
2. Multiple conditions can be checked using `and` or `or` operators
3. The order of conditions matters, as the first true condition will be executed
4. Always consider all possible scenarios when writing conditional statements
5. Logical thinking is crucial for writing effective conditional statements

## Best Practices

- Think through all possible scenarios before coding
- Use pen and paper to plan out logic before writing code
- Practice regularly to improve logical thinking skills

## Next Topic

The next video will cover Lists in Python.
