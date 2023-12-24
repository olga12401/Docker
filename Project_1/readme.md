# Step

В этом проекте мы запустим простой скрипты на python из контейнера, чтобы понять как работает Docker.

1. Create .py with a code
2. Create Dokcer file
3. Check that app.py opens a new tab wth text "Hello , word". 

Для этого выполним следующие команды

- в файл app.py поместим наш скрипт для вызова текста "Hello , word"

```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World test 3!'

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=80)  

```

- Create a virtual environment for your project. This ensures that the dependencies for your project are isolated from other Python projects .
 We can do it , if Run ```python -m venv venv``` to create a new virtual environment named 'venv'.

- Activate the virtual environment on Linux : ```source venv/bin/activate``` .

- В нашем скрипте мы работаем со средой Flask. Flask is a lightweight WSGI web application framework in Python. Установим Flask используя команду `pip`: ``` pip install flask ```

- Выполнив предыдущую команду нам необходимо получить список с требованиями для работы, которые нам понадобяться и сохранить их в файл с расширением .txt : ```pip freeze > requirements.txt``` 

- Running the Application: ``` python app.py ```

Если все шаги выполненны корректно, то получаем ссылку на сайт, которы можем открыть командой `CTRL+C to quit link`  и увидим наш текст.







