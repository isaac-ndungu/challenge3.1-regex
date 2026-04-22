# Python Regex Utilities

A collection of Python utilities for string validation and pattern matching using regular expressions.

## Overview

This project provides simple, reusable Python scripts that leverage the `re` module to perform common string operations such as character validation and pattern matching.



## Features

- **Alphanumeric String Validation** – Checks whether a string contains only allowed characters (`a-z`, `A-Z`, `0-9`).
- **Pattern Matching** – Finds substrings that match a specific pattern (e.g., strings starting with `'a'` and ending with `'b'`).



## Requirements

- Python 3.x
- No external dependencies — uses the built-in `re` module.



## Usage

### 1. Alphanumeric Character Check

Checks if a string contains only alphanumeric characters (`a-z`, `A-Z`, `0-9`). Any spaces, punctuation, or special characters are flagged.

```python
import re

text = 'Spacecraft!'
result = re.findall(r'\W', text)

if result:
    print('The string contains non-alphanumeric characters', result)
else:
    print('The string only contains alphanumeric characters')
```

**Output:**
```
The string contains non-alphanumeric characters ['!']
```



### 2. Pattern Matching — `a...b`

Finds all substrings that begin with the letter `'a'`, are followed by any single character, and end with `'b'`.

```python
import re

text = 'arb abb asb abs'
result = re.findall(r'a.b', text)
print(result)
```

**Output:**
```
['arb', 'abb', 'asb']
```

> **Note:** `abs` is not matched because `s` comes after `b`, not before it.



## License

This project is open source and available under the [MIT License](LICENSE).