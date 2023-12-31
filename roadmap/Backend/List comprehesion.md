**Comprehension** (генератор списка, генератор множества, генератор словаря) - это способ создания новых списков, множеств, словарей на основе существующих данных или итерируемых объектов. В Python есть следующие виды comprehensions:

- List Comprehension
- Set Comprehension
- Dictionary Comprehension

**Generator** - это специальный тип итерируемых объектов, который создает значения по мере необходимости (ленивая генерация) и не хранит все значения в памяти одновременно. Генераторы создаются с использованием ключевого слова `yield`. Генераторы особенно полезны, когда нужно обрабатывать большие наборы данных или когда нужно генерировать значения по требованию.

- **выражение-генератор** (generator expression) — выражение в круглых скобках которое выдает создает на каждой итерации новый элемент по правилам.
- **list comprehension коллекции** — обобщенное название для генератора списка (list comprehension), генератора словаря (dictionary comprehension) и генератора множества (set comprehension).
![[Pasted image 20231108190308.png]]
Данный массив сохранен в памяти, в отличии от [[Генератор|генератора]] который не сохраняется.
Вот пример. Данная функция является итерируемой:
```python
def gen():
    for i in [23, 12, 43]:
        yield i
        
s = gen()
print(next(s)) # 23
print(next(s)) # 12
print(s) # <generator object gen at 0x000002631B4C4B80>
```


### Все виды list comprehension

**list comprehension списков**
Самый обычный list comprehension. Использует квадратные скобки 
```python 
new_list = [выражение **for** элемент **in** последовательность **if** условие]
```

**list comprehension словарей**
list comprehension словарей очень похож на list comprehension множества тем, что использует фигурные скобки, отличие в том что в последовательности должно быть по два значения на итерацию, а элементом является картеж из двух элементов.
```python 
new_dict = { ключ:значение **for** (ключ,значение) **in** dict.items() **if** условие }
```

**list comprehension множества**
```python 
new_set = { выражение **for** элемент **in** последовательность **if** условие }
```

**list comprehension кортежа**
Данный list comprehension будет работать только если прописать ключевое слова tuple, иначе получится list comprehension выражений.
```python 
tuple(выражение **for** элемент **in** последовательность **if** условие)
```

