Оператор сравнение `is` выдаст True только в том случае, если `x` и `y` один и тот же объект
```python
>>> x = 2 + 1
>>> 3 is x
# True

# смотрим индификаторы
>>> id(x) 
10914560
>>> id(3)
10914560

# пример со списками
>>> x = [1, 2, 3, 4, 5, 6]
>>> y = x
>>> y is x
# True
>>> y = x.copy()
>>> y is x
# False

>>> y is not x
# True
```

Оператор `in` проверяет, есть ли данный объект в списке.
```python
>>> x = {'one':1, 'two':2, 'three':3, 'four':4}
>>> 'one' in x
# True
>>> 'one' not in x
# False
>>> 'five' in x
# False
>>> 'five' not in x
# True


>>> x = [1, 2, 3, 4, 5, 6, 7, 8]
>>> 5 in x
# True
>>> 5 not in x
# False
>>> 0 in x
# False
>>> 0 not in x
# True
```