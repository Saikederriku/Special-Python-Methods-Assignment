# Python Magic Methods

A simple guide to Python's special (dunder) methods with practical examples.

## What's Inside

This notebook covers 16 magic methods that let your custom classes work like Python's built-in types.

| Method | Does What | Example |
|--------|-----------|---------|
| `__init__` | Sets up new objects | `Car` brand, model, year |
| `__str__` | Pretty print for users | `Movie` title and rating |
| `__repr__` | Debug output for developers | Recreate the object |
| `__len__` | Object length | `Team` member count |
| `__eq__` | Compare with `==` | `Ticket` ID matching |
| `__add__` | Add with `+` | `Money` amounts |
| `__sub__` | Subtract with `-` | `Money` discounts |
| `__mul__` | Multiply with `*` | `Money` scaling |
| `__getitem__` | Access by index `obj[i]` | `Inventory` items |
| `__setitem__` | Set by index `obj[i]=v` | Update `Inventory` |
| `__contains__` | Check with `in` | `Classroom` enrollment |
| `__call__` | Call object like a function | `TaxCalculator` |
| `__iter__` | Loop with `for` | `Fibonacci` sequence |
| `__next__` | Get next item | Continue sequence |
| `__bool__` | True/False check | `Stock` available? |
| `__del__` | Cleanup on delete | `TempFile` close |

## How to Run

```bash
pip install notebook
jupyter notebook Python_Special_Methods_Complete.ipynb
```


## Quick Example

```python
class Money:
    def __init__(self, amount):
        self.amount = amount

    def __add__(self, other):
        return Money(self.amount + other.amount)

    def __str__(self):
        return f"${self.amount:.2f}"

a = Money(100)
b = Money(50)
print(a + b)  # $150.00
```

## License

MIT
