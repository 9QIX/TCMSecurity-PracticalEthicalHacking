# Python Importing

## Importing Modules

- Modules are existing code in Python that can be imported for use
- Some modules are built-in, others need to be imported

### Basic Import

```python
import sys
```

- `sys` is a module for system functions and parameters
- Example usage: `print(sys.version)`

### Importing Specific Parts of a Module

```python
from datetime import datetime
```

- Imports only the `datetime` part from the `datetime` module
- Example usage: `print(datetime.now())`

### Importing with Aliases

```python
import datetime as dt
```

- Allows using a shorter name (alias) for the imported module
- Example usage: `print(dt.now())`

## Key Points

1. Importing is crucial for accessing additional functionality in Python
2. Not all modules are imported by default
3. `sys` and `os` are frequently used modules
4. You can import entire modules, specific parts, or use aliases
5. Most imports in this course will be from pre-existing Python libraries

## Common Imports and Uses

- `sys.argv`: for handling command-line arguments
- `sys.exit()`: for cleanly exiting Python
- `datetime`: for handling dates and times

The instructor emphasizes the importance of understanding imports, as they will be used frequently throughout the course, especially in the exploit development section.
