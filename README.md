[![pypi](https://img.shields.io/pypi/v/timedfunc)](https://pypi.org/project/timedfunc)

# timedfunc

An easy way to measure execution time of Python functions using decorators.

## Installation

```bash
pip install timedfunc
```

## Example

```python
from timedfunc import timedfunc

@timedfunc
def my_function(x):
	print("doing stuff that takes some time...")
	import time
	time.sleep((x + 1) * 0.100) # simulate a computation

for i in range(3):
	my_function(i)
```

output:
```
doing stuff that takes some time...
doing stuff that takes some time...
doing stuff that takes some time...
--------------------------------+----------+--------------+--------------+--------------
 timed functions                |    calls |          min |         mean |          max
--------------------------------+----------+--------------+--------------+--------------
 my_function                    |        3 |      0.111 s |      0.207 s |      0.310 s
--------------------------------+----------+--------------+--------------+--------------
```
