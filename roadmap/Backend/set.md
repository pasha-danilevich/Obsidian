Множество это изменяемая коллекция из неупорядоченных уникальных элементов.
### Создание
![[Pasted image 20231207224842.png]]
```python
S = {'1', '2', '3'}
print(S)

> {'1', '2', '3'}

print(type(S))

> <class 'set'>
```
### Добавление элемента
![[Pasted image 20231207225646.png]]
Для добавления нового элемента в существующий набор используем метод `add(x)`.

```python
stats = {1.65, 2.33, 5.0}
stats.add(14.7)
print(stats)
 
> {1.65, 2.33, 5.0, 14.7}
```
### Удаление и очистка
![[Pasted image 20231207225747.png]]

Очистить и свести уже существующий сет к пустому не составит никаких проблем благодаря методу `сlear()`:

```python
set_with_elements = {'i am element', 'me too'}
print(set_with_elements)

> {'i am element', 'me too'}

set_with_elements.clear()
print(set_with_elements)

> set()
```
Метод `pop()`.

Удаляет и возвращает случайный элемент множества:

```python
sweets = {'candy', 'gingerbread', 'lollipop', 'candy floss', 'sweets'}
print(sweets)
> {'lollipop', 'candy', 'sweets', 'gingerbread', 'candy floss'}

print(sweets.pop())
> lollipop

print(sweets)
> {'candy', 'sweets', 'gingerbread', 'candy floss'}
```

### Пересечение
- Пересечение 
(оператор `&`, логическое `И`)
![[Pasted image 20231207225324.png]]

```python
# пусть есть два списка, и нужно отыскать и вывести их одинаковые компоненты
unbreakable_diamond = ['Jotaro', 'Josuke', 'Koichi']
golden_wind = ['Jotaro', 'Koichi', 'Giorno']
# & - здесь оператор пересечения
overlap = set(unbreakable_diamond) & set(golden_wind)
print(overlap)
 
> {'Jotaro', 'Koichi'}
```
Помимо пересечения есть:


- Вычитание
(оператор `-`)
![[Pasted image 20231207225427.png]]


- Симметрическая разность
(оператор `^`)
![[Pasted image 20231207225519.png]]


- Объединение
(оператор `|`, логическое `ИЛИ`)
![[Pasted image 20231207225452.png]]