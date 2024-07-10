# Python Lists

## Key Concepts

- Lists are changeable data structures in Python
- Lists are defined using square brackets `[]`
- Items in a list are accessed using zero-based indexing

## List Operations

### Creating a List

```python
movies = ["When Harry Met Sally", "The Hangover", "The Perks of Being A Wallflower", "The Exorcist"]
```

### Accessing List Items

- First item: `movies[0]`
- Last item: `movies[-1]`
- Slicing: `movies[1:3]` (from index 1 up to, but not including, index 3)

### List Methods

- `len(movies)`: Returns the number of items in the list
- `movies.append("Jaws")`: Adds an item to the end of the list
- `movies.pop()`: Removes and returns the last item in the list
- `movies.pop(0)`: Removes and returns the item at the specified index

## Important Notes

1. Indexing starts at 0, not 1
2. When slicing, the end index is exclusive
3. Negative indexing can be used to access items from the end of the list
4. Lists are mutable, meaning they can be changed after creation

The instructor emphasizes understanding these basics as they form the foundation for working with other data structures in Python.
