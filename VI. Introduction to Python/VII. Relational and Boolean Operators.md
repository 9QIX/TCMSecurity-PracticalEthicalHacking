# Relational and Boolean Operators in Python

## Introduction

- Building upon boolean expressions
- Discussing relational operators and boolean operators

## Relational Operators

1. Greater than (`>`)

   ```python
   greater_than = 7 > 5  # True
   ```

2. Less than (`<`)

   ```python
   less_than = 5 < 7  # True
   ```

3. Greater than or equal to (`>=`)

   ```python
   greater_than_or_equal = 7 >= 7  # True
   ```

4. Less than or equal to (`<=`)
   ```python
   less_than_or_equal = 7 <= 7  # True
   ```

## Boolean Operators

1. AND (`and`)

   ```python
   test_and = (7 > 5) and (5 < 7)  # True
   test_and2 = (7 > 5) and (5 > 7)  # False
   ```

2. OR (`or`)

   ```python
   test_or = (7 > 5) or (5 < 7)  # True
   test_or2 = (7 > 5) or (5 > 7)  # True
   ```

3. NOT (`not`)
   ```python
   test_not = not True  # False
   test_not2 = not False  # True
   ```

## Key Points

- In `and` operations, both statements must be true for the result to be true
- In `or` operations, only one statement needs to be true for the result to be true
- Truth tables are useful for understanding boolean logic
- Understanding these concepts is crucial for reading and comprehending Python code in pentesting scenarios

## Next Steps

- Moving on to conditional statements (if-then-else)
