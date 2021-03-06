# Python `all(iterable)`

`all()` is a built-in function in Python 3, to check if all items of an [_iterable_](https://docs.python.org/3/glossary.html#term-iterable) is `True`. It takes one argument, `iterable`.

## Argument

### iterable

The `iterable` argument is the collection whose all entries are to be checked. It can typically be a `list`, `str`, `dict`, `tuple` etc.

## Return Value

The return value would be a boolean. If and only if **all** entries of iterable are `True`, it returns `True`. This function essentially performs a Boolean `AND` operation over all elements.

If even one of them is not `True`, it would return `False`.

The `all()` operation is equivalent to (not internally implemented exactly like this)

```python
def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```

## Code Sample

```python
print(all([6, 7])) #=> True
print(all([6, 7, None])) #=> False  Because this has None
print(all([0, 6, 7])) #=> False Because this has zero
print(all([9, 8, [1, 2]])) #=> True
print(all([9, 8, []])) #=> False Because it has []
print(all([9, 8, [1, 2, []]])) #=> True
print(all([9, 8, {}])) #=> False Because it has {}
print(all([9, 8, {'engine': 'Gcloud'}])) #=> True
```

:rocket: [REPL It!](https://repl.it/CL9U/0)

[Official Docs](https://docs.python.org/3/library/functions.html#all)
