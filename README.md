# PYTHON "САМ СЕБЕ ПРОГРАММИСТ" по Кори Альтхоффу
# 1. Введение
## Вывод 
```python
print("Text")
```
`>> Text`
___
## Арифметика

сложение :
```python
print(2+2) 
```
`>> 4`

вычитание :
```python
print(2-2)
```
`>> 0`

деление :
```python
print(4/2)
```
`>> 2`

деление по модулю :
```python
print(9/2)
```
`>> 1`

умножение :
```python
print(2*2)
```
`>> 4`

возведение в степень :
```python
print(2**3)
```
`>> 8`

увеление на 1 :
```python
x = 10
x += 1
print(x)
```
`>> 11`

уменьшение на 1 :
```python
x = 10
x -= 1
print(x)
```
`>> 9`
___
## Операторы сравнения
```python
print(100 > 1)
```
`>> True`
```python
print(100 < 1)
```
`>> False`
```python
print(100 >= 1)
```
`>> True`
```python
print(100 <= 1)
```
`>> False`
```python
print(100 == 1)
```
`>> False`
```python
print(100 != 1)
```
`>> True`
___
## Условные операторы *(if, elif, else)*
Связка из if и else : 
```python
home = "Украина"
if home == "Украина":
    print("Прiвет")
else:
    print("Прiвит, мир")
```
`>> Украина`

`>> Прiвит`

Инструкция **elif** в первую очередь оценивает значение **if**, при результате **true** дальше инструкции не выполняются, при результате **false** выполняется инструкия **else**.

# 2. Функции
## Определение функции
Шаблон функции :

```python
def имя_функции(параметры):
    определение_функции 
```

```python
def f(x):
    return x * 2


result = f(2)
print(result)
```
`>> 4`

```python
def f(x, y, z):

result = f(1, 2, 3)
print(result)
```
`>> 6`

## Встроенные функции
Возвращение длины объекта : 
```python
len("Монти")
```
`>> 5`

аналогично : *int, str, float*

## Многокрасное использованеи функций

```python
def even_odd():
    n = input("введите число : ")
    n = input(n)
    if n % 2 == 0:
        print("n - нечётное")
    else:
        print("n - чётное")


even_odd()
even_odd()
even_odd()
```
`>> Введите число : `

`>> 5`

`>> не чётное`

`>> Введите число : `

`>> 4`

`>> чётное`

`>> Введите число : `

`>> 1`

`>> не чётное`

## Обязательные / Необязательные параметры

```python
def f(x = 2):
    return x ** x


print(f())
print(f(4))
```
`>> 4`

`>> 256`

```python
def f(x, y = 10):
    return x + y


result = f(2)
print(result)
```
`>> 12`

## Область видимости

```python
x = 1
y = 2
z = 3


def f():
    print(x)
    print(y)
    print(z)


f()
```
`>> 1`

`>> 2`

`>> 3`

```python
x = 100

def():
    global x
    x += 1
    print(x)


f()    
```
`>> 101`

## Обработка исключений

```python
a = input("Введите число")
a = int(a)
b = input("Введите число")
b = int(b)
try: 
    print(a / b)
except: ZeroDivisionErrpr:
    print("b не может быть 0")
```
`>> Введите число: `

`>> 10`

`>> Введите число: `

`>> 0`

`>> b не может быть 0`

# 3. Контейнеры

## Списки

```python
fruit = list()
print(fruit)
```
`>> []`

***ИЛИ***
```python
fruit = []
print(fruit)
```
`>> []`

```python
fruit = ["яблоко","апельсин"]
print(fruit)
```
`>> ["яблоко","апельсин"]`

Добавить объект в список с помощью функции **append** :

```python
fruit = ["яблоко","апельсин"]
fruit.append("банан")
print(fruit)
```
`>> ["яблоко","апельсин","банан"]`

Обращаемся к эллементу списка по индексу : 
```python
fruit = ["яблоко","апельсин"]
print(fruit[0])
```
`>> 'яблоко'`

Изменение списка : 
```python
fruit = ["яблоко","апельсин"]
fruit[1] = "мандарин"
print(fruit)
```
`>> ["яблоко","мандарин"]`

Удаление **последнего** эллемента в списке : 
```python
fruit = ["яблоко","апельсин"]
item = fruit.pop()
print(fruit)
```
`>> ["яблоко"]`

Объединения двух списков : 
```python
fruit = ["яблоко","апельсин"]
berry = ["клубника","вишня"]
print(fruit + berry)
```
`>> ["яблоко","апельсин","клубника","вишня"]`

Проверка наличия эллемента в списке : 
```python
fruit = ["яблоко","апельсин"]
print("яблоко" in fruit)
```
`>> True`
___
## Кортежи

```python
fruit = tuple()
print(fruit)
```
`>> ()`

***ИЛИ***
```python
fruit = ()
print(fruit)
```
`>> ()`

Кортежи - неизменяемые списки, поэтому из функций возможна только проверка наличия эллемента через **in** .
___
## Словари
 
 ```python
 my_dict = dict()
 print(my_dict)
 ```
 `>> {}`
 
 ***ИЛИ***

```python
 my_dict = {}
 print(my_dict)
 ```
 `>> {}`

 ```python
fruit = {"Яблоко": "красное", 
         "Банан": "жёлтый"}
print(fruit)
```
`>> {"Яблоко": "красное", "Банан": "жёлтый"}`

Добавление ключей - значений в словарь :
```python
facts = {}
facts ["Билл"] = "Гейтс"
print(facts["Билл"])
```
`>> Гейтс`

Наличие эллемента в словаре можно производить с помощью функции **in** .

Удаление эллемента из словаря : 
```python
facts = {"Билл": "Гейтс", "Тим": "Кук"}
del facts ["Тим"]
print(facts)
```
`>> {"Билл": "Гейтс"}`
___
## Контейнеры внутри контейнеров
+ Можно хранить **списки внутри списка** :
  + *Списку внутри списка **присваивается индекс*** :
```python
lists = []
rap = ["OBLADAET", "QUOK"]
rock = ["Arctic monkey's","Oomph!"]

lists = append.(rap)
lists = append.(rock)

print(lists)
```
`>> ["OBLADAET", "QUOK"],["Arctic monkey's","Oomph!"]`
+ Можно хранить **кортежи внутри списка** :
```python
location = []

tula = (54,37)
moscow = (55,37)

location.append(tula)
loaction.append(moscow)

print(location)
```
`>> [(54,37),(55,37)]`
+ Можно хранить **списки внутри кортежа** :
```python
rap = ["OBLADAET", "QUOK"]
rock = ["Arctic monkey's","Oomph!"]

music = (rap, rock)

print(music)
```
`>> (["OBLADAET", "QUOK"],["Arctic monkey's","Oomph!"])`
+ Список, кортеж или словать могут быть значениями в словаре : 
```python
info = {"location" : (54,37) , "rap" : ["OBLADAET","QUOK"] , "fact" : {"city": "moscow"}}
```
___
# 4. Операции со строками
## Индексы

```python
author = "Кафка"

print(author[0])
print(author[1])
print(author[2])
print(author[3])
print(author[4])
```
`>> 'К'`

`>> 'а'`

`>> 'ф'`

`>> 'к'`

`>> 'а'`

Индексы могут быть **отрицательными**, тогда отсчёт идёт с конца объекта .

## Строки неизменяемы

```python
ff = "Ф.Фицджеральд"
ff = "Ф.Скотт Фицджеральд"

print(ff)
```
`>> "Ф.Фицджеральд"`

## Конкатенация
```python
print("кот" + " в " + "шляпе")
```
`>> кот в шляпе`

## Умножение строк
```python
print("Tom"*3)
```
`>> TomTomTom`

## Изменения регистра
Весь текст заглавными :
```python
print("раз , два , три".upper())
```
`>> "РАЗ , ДВА , ТРИ"`

Весь текст прописными :
```python
print("РАЗ , ДВА , ТРИ".lower())
```
`>> "раз , два , три"`

Первая буква заглваная,остальные прописные : 
```python
print("раз , два , три".cpitalize())
```
`>> "Раз , два , три"`

## Метод **fromat**

```python
print("Уильям {}".format("Фолкнер"))
```
`>> Уильям Фолкнер`

## Метод **split**

```python
print("Прияво брух.Пока друже".split("."))
```
`>> ["Прияво брух", "Пока друже"]`

## Метод **join**

```python
first = "абв"
result = "_".join(first)
print(result)
```
`>> а_б_в`

## Метод **strip**

```python
s = "     moscow      "
s = s.strip()
print(s)
```
`>> moscow`

## Метод **replace**

```python
a = "аоаооооаоаоаоао"
a = a.replace("о", "_")
print(a)
```
`>> а_а____а_а_а_а_`

## Поиск индекса

```python
print("животные".index("н"))
```
`>> 5`

```python
try:
    "животные".index("з")
except:
    print("Не обнаружено")
```
`>> Не обнаружено`

Так же возможна проверка наличия слова в предложении с помощью **in / not in**

## Новая строка

```python
print("строка 1\nстрока 2\nстрока 3")
```
`>> строка 1`

`>> срока 2`

`>> строка 3`

## Извлечение среза

```python
fict = ["Толстой","Дик","Пелевин","Остин"]
print(fict[0:3])
```
`>> ['Толстой', 'Дик', 'Пелевин']`
___
# 5. Циклы

## Цикл FOR

```python
for имя_переменной in имя_интерируемого_объекта:
    инструкция
```
**имя переменной** назначается значению каждого элемента в **интерируемом** объекте .

```python
name = "Тед"
for character in name:
    print(character)
```
`>> Т`

`>> е`

`>> д`

```python
shows = ["Во все тяжкие", "Секретные материалы", "Фарго"]
for show in shows:
    print(show)
```

`>> Во все тяжкие`

`>> Секретные материалы`

`>> Фарго`

аналогично с **кортежами / словарями** .

```python
shows = ["Во все тяжкие", "Секретные материалы", "Фарго"]
i = 0
for show in shows:
    new = tv[i]
    new = new.upper()
    tv[i] = new
    i += 1


print(tv)
```
`>> ["ВО ВСЕ ТЯЖКИЕ","СЕКРЕТНЫЕ МАТЕРИАЛЫ", "ФАРГО"]`

аналогично с **кортежами / словарями** .

**ИЛИ**

```python
shows = ["Во все тяжкие", "Секретные материалы", "Фарго"]
for i, show in enumerate(tv):
    new = tv[i]
    new = new.upper()
    tv[i] = new


print(tv)
```
## Фунцкия RANGE

```python
for i in range(1, 11):
    print(i)
```

`>> 1`

. . .

`>> 9`

`>> 10`

## Цикл WHILE

```python
while выражение:
    код_для_выполнения
```

```python
x = 10
while x > 0:
    print ('{}'.format(x))
    x -= 1


print("С новым годом !")
```

`>> 10`

`>> 9`

. . .

`>> 1`

`>> C новым годом`

## Функция BRAKE

```python
for i in range (0, 100):
    print(i)
    break
```

`>> 0`

## Функция CONTINUE

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

`>> 1`

`>> 2`

`>> 4`

`>> 5`

`>> 6`

# 6. Модули

```python
import имя_модуля
```

