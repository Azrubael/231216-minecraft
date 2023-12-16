# [1] - Установка Python 3.10 (или более позднего), pip и python3.10-venv
* https://docs.python.org/3/using/windows.html#launcher
* https://pip.pypa.io/en/stable/installing/
```bash
    apt install python3.10-venv
```
https://github.com/pyglet/pyglet/tree/pyglet-1.5-maintenance
https://github.com/pyglet/pyglet.git


# [2] - Создание изолированного окружения
* При работе в Linux
```bash
    $ python3 -m venv azenv
    $ source azenv/bin/activate
```
* При работе в Windows
```bash
    $ py -m venv azwenv
    $ .\azwenv\Scripts\activate
```


# [3] - Конфигурация изолированного окружения Python3
```bash
    (az_env)$ pip install -r dependencies.txt
# OR
    (az_env)$ cd pyglet-pyglet-1.5-maintenance
    (az_env)$ python3 setup.py install --user
    (az_env)$ pip install -e .
```


# [4] - Запуск первого приложения
* При работе в Linux
```bash
    (az_env)$ python3 runme.py
```
* При работе в Windows
```bash
    (az_env)$ py python3 runme.py
```


# [5] - Создание перечня зависимостей [только для разработки]
```bash
    (az_env)$ pip freeze > dependencies.txt
# OR
    (az_env)$ pip install findpydeps
    (az_env)$ findpydeps -i path/to/folder > dependencies.txt
```


# [6] - Деактивация изолированой среды
```bash
    (az_env)$ deactivate
```
