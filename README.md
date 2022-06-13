# Useful-Python-Tips

## Sort By Key
```python
data = [{"id": 4, "text": "hi"}, 
        {"id": 3, "text": "hi"},
        {"id": 1, "text": "hi"},
        {"id": 5, "text": "hi"},
        {"id": 2, "text": "hi"}]
data.sort(key=lambda x: x["id"], reverse=False)    
```

## For/Else (https://docs.python.org/3/howto/sorting.html)
```python
# Check if you broke out of loop, else do something. 
# (Typically you would set a flag to check if you completed a loop or not)

for i in range(10):
  print(i)
  if i == 9:
    break
else:
  print("We went through the entire loop!")
```

```python
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print( n, 'equals', x, '*', n/x)
            break
    else:
        # loop fell through without finding a factor
        print(n, 'is a prime number')
```

## Iterable Unpacking (https://stackabuse.com/unpacking-in-python-beyond-parallel-assignment/)

```python
a = [1,2]
b = 45
print([b, a]) # [45, [1,2]]

# But
print([b, *a]) # [45, 1, 2]
```
