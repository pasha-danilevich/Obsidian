```python
class SomeClass(object):
    def set_position(self, x, y):
        self.x = x
        self.y = y

obj = SomeClass()
obj.set_position(10, 12)

print(obj.x, obj.y) # 10 12
```
`self` это, по сути, такая переменная, при вызове функции, которая подставляет объект вместо себя.

То есть метод `set_position(self, x, y)` будет выглядит так:
```python
# При истользовании объекта obj
set_position(obj, x, y):
    obj.x = x
    obj.y = y
# На выходе будет выводиться x и y объекта obj 
print(obj.x, obj.y) 
```