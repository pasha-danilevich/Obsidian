Библиотека позволяет получать информацию из интернета

```python
import requests

url = 'http://wttr.in/moscov?0T'

response = requests.get(url)  # выполните HTTP-запрос

print(response.text)  # напечатайте текст HTTP-ответа
```