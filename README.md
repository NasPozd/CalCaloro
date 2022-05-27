![Screenshot](media/Screenshot.png)

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Checked with mypy](http://www.mypy-lang.org/static/mypy_badge.svg)](http://mypy-lang.org/)
[![Build Status](https://api.travis-ci.com/vyahello/calorie-counter.svg?branch=master)](https://www.travis-ci.com/github/vyahello/calorie-counter)
[![Coverage Status](https://coveralls.io/repos/github/vyahello/calorie-counter/badge.svg?branch=master)](https://coveralls.io/github/vyahello/calorie-counter?branch=master)
[![PyPI version shields.io](https://img.shields.io/pypi/v/calorie-counter.svg)](https://pypi.python.org/pypi/calorie-counter/)
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/calorie-counter.svg)](https://pypi.python.org/pypi/calorie-counter/)
[![PyPi downloads](https://img.shields.io/pypi/dm/calorie-counter.svg)](https://pypi.python.org/pypi/calorie-counter)
[![CodeFactor](https://www.codefactor.io/repository/github/vyahello/calorie-counter/badge)](https://www.codefactor.io/repository/github/vyahello/calorie-counter)
[![Docker pulls](https://img.shields.io/docker/pulls/vyahello/calorie-counter.svg)](https://hub.docker.com/repository/docker/vyahello/calorie-counter)

# Калькулятор расчета калорий
> Этот проект представляет собой простое веб-приложение для расчета калорий на основе заданного типа пищи.

## Инструменты разработки
- front-end
  - html5
  - css3
  - javascript
- back-end
  - python 3.10
  - [flask](http://flask.palletsprojects.com)

### Быстрый страт

Используйте следующую команду для запуска приложения через docker:
```bash
docker run -it -p 5001:5001 vyahello/calorie-counter:0.1.0 counter
```

Откройте http://0.0.0.0:5001

### Исходный код

Чтобы иметь возможность запускать исходный код, пожалуйста, выполните приведенную ниже команду:
```bash
git clone https://github.com/NasPozd/CalCaloro.git
cd calorie-counter
pip install -r requirements.txt
python -m counter --bind 0.0.0.0:5001 --debug
```

Также вы можете использовать **flask** встроенный раннер на основе конфигурационного файла [.flaxen](.flaxen):
```bash
export FLASK_APP=counter
flask run
```

Then please open [localhost:5003](http://localhost:5003) endpoint in your browser.

### Установка PYPI 

Запустите следующий скрипт, чтобы получить актуальный пакет из PYPI:
```bash
pip install calorie-counter
```
Затем выполните приведенные ниже инструкции, чтобы запустить его из вашей среды:
```python
>>> from counter import Bind, easyrun
>>> 
>>> easyrun(Bind("0.0.0.0:5003"))
```
Затем откройте [localhost:5003](http://localhost:5003 ).

### Создание образов docker

Чтобы создать базовый образ выполните следующую команду:
```bash
docker build --no-cache -t calorie-counter:0.1.0 -f docker/Dockerfile .
```

Чтобы создать основной образ выполните следующую команду:

```bash
docker build --no-cache -t calorie-counter:test -f docker/Dockerfile --build-arg VERSION=0.1.0 .
```

Используйте следующие команды для отправки образа:
```bash
docker push calorie-counter:test
```

### Meta
Над проектор работали студенты ИНБО-07-20
```bash
Позднякова А.О.
Воронкова А.В.
Рыжило А.В.
Мацоян А.К.
```
