### Генераторы словарей


Вот генератор словаря. Он похож на генерацию списка, но так так у словаря есть два значения: ключ и значение, то для генерации необходимо это прописать.
```python
dict = {key:key for key in range(5)}
# {0: 0, 1: 1, 2: 2, 3: 3, 4: 4}
```

С помощью конструкции `for in` можно перебрать уже существующий список и отредактировать его.
```python
dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
dict_duble = {key:value * 2 for (key, value) in dict.items()}

print(dict) # {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
print(dict_duble) # {'a': 2, 'b': 4, 'c': 6, 'd': 8, 'e': 10}
```
Как можно заметить, генератор не изменил `dict` он создал новый список `dict_duble`. К сгенерированному  списку можно обращаться по переменной к которой был присвоен данный список.