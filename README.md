# timedfunc

An easy way to measure execution time of Python functions using decorators.

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
 my_function                    |        3 |     0.103 ms |     0.204 ms |     0.308 ms
--------------------------------+----------+--------------+--------------+--------------

```