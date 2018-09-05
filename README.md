# Lesson 1
Для тех кто будет заново все делать в linux

1. Скачать питон https://www.python.org/downloads/
2. Установить pip. https://pip.pypa.io/en/stable/installing/
3. Установить virtualenv - `pip install virtualenv` https://virtualenv.pypa.io/en/stable/installation/
4. Создать переменную окружения. **ЗАПОМНИТЕ РАСПОЛОЖЕНИЕ ПЕРЕМЕННОЙ** `virtualenv env1`
5. Активироать окружение `source env1/bin/activate` (Для unix стистем), 
Для Windows - `cd env1/scripts` `activate`
6. Установить пакет ipython - `pip install ipython`
7. Интерактивный режим - в консоли `ipython`

# Documentation
https://docs.python.org/3/tutorial/introduction.html

https://docs.python.org/3/tutorial/controlflow.html

https://docs.python.org/3/tutorial/datastructures.html

# Books
http://www.diveintopython3.net

http://www.dsf.unica.it/~fiore/LearningPython.pdf

http://www.russchooljp.com/wp-content/uploads/2017/05/Python.dlya_.detei_.pdf

# Homework
- Поставить linux
- Поставить PyCharm
- Почитать 3 ссылки по документации

# Homework *
Создать функцию, которая принимает любое количество неименнованых параметров, и один именнованый параметр `_type`

Сигнатура функции

```
def foo(*args, _type=None):
    pass
```

в аргументы можно передать любой тип данных, _type можен принимать значение только из `(list, tuple, dict, None)`
Функция должна вернуть список из двух элементов, где первый это список который получен в результате сложения всех переданых 
списков или кортежей, второй - словарь, который получен из всех переданных словарей. Если в качетсве `_type`, передано
одно значение из списка `(list, tuple, dict)`, то при подсчете необходимо учитывать только тот тип, который передали

Пример работы:
```
IN: foo(1, [2,3], (4,5), {'key': 'value'}, {'key1': 'value1'}, _type=None)
OUT: [[1,2,3,4,5], {'key': 'value', 'key1': 'value1'}]

IN: foo(1, [2,3], (4,5), {'key': 'value'}, {'key1': 'value1'}, _type=dict)
OUT: [[], {'key': 'value', 'key1': 'value1'}]

IN: foo(1, [2,3], (4,5), {'key': 'value'}, {'key1': 'value1'}, _type=list)
OUT: [[1,2,3,4,5], {}]
```
