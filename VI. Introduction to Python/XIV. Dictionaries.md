# Dictionaries in Python

## Key Concepts

- Dictionaries use key-value pairs
- Syntax: Curly braces `{}`

## Creating Dictionaries

```python
drinks = {
    "White Russian": 7,
    "Old Fashioned": 10,
    "Lemon Drop": 8
}

employees = {
    "Finance": ["Bob", "Linda", "Tina"],
    "IT": ["Gene", "Louise", "Teddy"],
    "HR": ["Jimmy Junior", "Mort"]
}
```

## Operations on Dictionaries

1. Adding new key-value pairs:

   ```python
   employees["Legal"] = ["Mr. Frond"]
   ```

2. Updating existing dictionaries:

   ```python
   employees.update({"Sales": ["Andy", "Ollie"]})
   ```

3. Modifying values:

   ```python
   drinks["White Russian"] = 8
   ```

4. Accessing values:
   ```python
   print(drinks.get("White Russian"))
   ```

## Importance in Python

- Dictionaries are distinct from lists (square brackets) and tuples (parentheses)
- Understanding these data structures helps in reading and interpreting Python code

## Course Context

- This lesson is part of a series building up to more complex concepts
- The goal is to enable students to read and understand code, even if not becoming full developers
