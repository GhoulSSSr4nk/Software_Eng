# Тема 2. Базовые операции языка Python
Отчет по Теме #2 выполнил(а):
- Демаков Артемий Игоревич
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | + |
| Задание 7 | + | + |
| Задание 8 | + | + |
| Задание 9 | + | + |
| Задание 10 | + | + |

# Лабараторные работы 
   ## Лабараторная работа 1

  Выведите в консоль три строки. Первая – любое число. Вторая – любое число в виде строки. Третья – любое число с плавающей точкой.

  ```python
print(123)
print('123')
print(1.23)
```
  ### Результат
  
 ![Снимок экрана 2023-09-19 031155](https://github.com/Mikhail867/Software_Engineering/assets/144737787/01ea75e9-6d86-4cb7-806d-b0a279f13add)
 
## Краткий вывод:

print(123): Эта строка выводит число 123 на экран. Значение 123 является целым числом, и оно будет выведено без кавычек.

print('123'): В этой строке выводится строка '123'. Значение заключено в одинарные кавычки, что указывает на то, что это строка. Таким образом, на экране будет выведена строка '123'.

print(1.23): Эта строка выводит число 1.23 на экран. Значение 1.23 является числом с плавающей точкой (десятичным числом).

Таким образом, программа выводит три строки на экран, представляющие разные типы данных: целое число, строку и число с плавающей точкой.

## Лабараторная работа 2

Выведите в консоль три строки. Первая – результат сложения или вычитания минимум двух переменных типа int. Вторая – результат сложения или вычитания минимум двух переменных типа float. Третья – результат сложения или вычитания минимум двух переменных типа int и float.
 ```python
print(1823 - 486) 
print(5.1 + 8.27) 
print(3 + 7.04 + 1 + 2.33)
```

### Результат

![2](https://github.com/Mikhail867/Software_Engineering/assets/144737787/ac4c7fe6-7a02-477c-90d7-c96249a02b3b)

## Краткий вывод:

print(1823 - 486): В этой строке выполняется вычитание 486 из 1823, что дает результат 1337. Таким образом, на экран будет выведено число 1337.

print(5.1 + 8.27): В этой строке выполняется сложение двух чисел с плавающей точкой: 5.1 и 8.27. Результат этой операции равен 13.37. Таким образом, на экран будет выведено число 13.37.

print(3 + 7.04 + 1 + 2.33): В этой строке выполняется сложение нескольких чисел с плавающей точкой и целых чисел: 3, 7.04, 1 и 2.33. Результат этой операции равен 13.37, так же как и во второй строке. Таким образом, на экран также будет выведено число 13.37.

## Лабараторная работа 3

 Выведите в консоль три строки. Первая – обычная строка. Вторая – F строка с использованием заранее объявленной переменной. Третья – сложите две или более строк в одну.
 ```python
 print("Привет, Мир!")


name = "Мир"
print(f"Привет, {name}!")


string1 = "Привет, "
string2 = "Мир! "
result_string = string1 + string2
print(result_string)
```
### Результат

![3](https://github.com/Mikhail867/Software_Engineering/assets/144737787/3216ea9a-c110-4a71-8e92-2af0007924be)

## Краткий вывод:
print("Привет, Мир!"): В первой строке программа выводит на экран фразу "Привет, Мир!" в виде обычной строки.

name = "Мир": Здесь объявляется переменная name, которая получает значение "Мир".

print(f"Привет, {name}!"): В этой строке используется F-строка для вывода приветствия, в котором значение переменной name подставляется внутрь фразы. Таким образом, на экран будет выведено "Привет, Мир!".

string1 = "Привет, ": В этой строке объявляется переменная string1, которая получает значение "Привет, ".

string2 = "Мир! ": Здесь объявляется переменная string2, которая получает значение "Мир! ".

result_string = string1 + string2: В данной строке происходит конкатенация (сложение) двух строк string1 и string2, и результат сохраняется в переменной result_string. Таким образом, result_string будет содержать "Привет, Мир! ".

print(result_string): Затем программа выводит содержимое переменной result_string на экран. В результате будет выведено "Привет, Мир! ".

Итак, данная программа выводит на экран три строки, представляющие разные способы формирования одного и того же приветствия: обычную строку, F-строку и результат конкатенации двух строк.

## Лабараторная работа 4

Выведите в консоль три строки. Первая – трансформация любого типа переменной в bool. Вторая – трансформация любого типа переменной в float или int. Третья – трансформация любого типа переменной в str.

 ```python
one = "Hello"
print(bool(one))

two = 142
print(float(two))

three = None
print(str(three))
```
### Результат

![4](https://github.com/Mikhail867/Software_Engineering/assets/144737787/a1f54287-cd07-47cd-a879-bec4955abfad)


## Краткий вывод:

one = "Hello": Здесь объявляется переменная one, которой присваивается значение "Hello" - это строка.

print(bool(one))истbool(), которая проверяет,one : В этой строке вызprint(bool(one)) выведет TrueTrue
two = 142: Здесь объявляется переменная twotwo, которой присваивается значение 142 -

print(float(two)): В этой строке вызывается функция float(), которая пытается преобразовать значение переменной two в число с плавающей точкой (float). В результате выводится значение 142.0, представленное в формате числа с плавающей точкой.

three = None: Здесь объявляется переменная three, которой присваивается значение None. None представляет собой специальное значение, обозначающее отсутствие значения или нулевое значение.

print(str(three)): В этой строке вызывается функция str(), которая пытается преобразовать значение переменной three в строку. Так как three содержит None, то результатом будет строка "None", которая выводится на экран.

## Лабараторная работа 5

Присвойте трем переменным различные значения, воспользовавшись функцией input()

 ```python
one = input("one:")
two = input("two:")
three = input("three:")
print(one,two,three)
```
### Результат

![5](https://github.com/Mikhail867/Software_Engineering/assets/144737787/92c277af-d2f5-4423-8bfe-8c630fc17364)


## Краткий вывод:

one = input("one:"): Эта строка кода запрашивает ввод пользователя с помощью функции input(). Функция input() выводит на экран текст "one:" и ожидает, пока пользователь введет текст с клавиатуры. Введенный текст будет сохранен в переменной one.

two = input("two:"): Аналогично, эта строка кода запрашивает ввод пользователя и сохраняет введенный текст в переменной two, отображая текст "two:" для ввода.

three = input("three:"): Эта строка кода также запрашивает ввод пользователя и сохраняет введенный текст в переменной three, отображая текст "three:" для ввода.

print(one, two, three): После того как пользователь ввел все три значения, программа использует функцию print() для вывода этих значений на экран. Значения one, two и three разделяются пробелами, поэтому они будут выведены на экран в виде одной строки.

## Лабараторная работа 6
Создайте две любые числовые переменные и выполните над ними несколько математических операций: возведение в степень, обычное деление, целочисленное деление, нахождение остатка от деления. При желании вы можете проверить как работают эти вычисления с разными типами данных, например, сначала создать две переменные int, затем создать две переменные float и наконец создать переменные типа int и float и провести над ними операции, прописанные выше.
 ```python
a = 10
b = 5
print("Возведение в степнь:", a ** b)
print("Обычное деление:", a / b)
print("Целочисленное деление:", a // b)
print("Нахождение остатка от деления:", a % b)

```
### Результат

![6](https://github.com/Mikhail867/Software_Engineering/assets/144737787/7d21e4e9-a3d8-49a1-aa73-23e27479fed5)

## Краткий вывод:
a = 10: Здесь объявляется переменная a и ей присваивается значение 10.

b = 5: Здесь объявляется переменная b и ей присваивается значение 5.

print("Возведение в степень:", a ** b): Эта строка кода выводит на экран результат возведения числа a в степень b. В данном случае, 10 возводится в пятую степень, и результат (10^5) будет выведен после текста "Возведение в степень:". Результатом будет число 100000.

print("Обычное деление:", a / b): В этой строке кода выполняется обычное деление числа a на число b. Результатом будет число с плавающей точкой, равное 2.0. Этот результат будет выведен после текста "Обычное деление:".

print("Целочисленное деление:", a // b): Здесь выполняется целочисленное деление числа a на число b. Результатом будет целое число, равное 2. Этот результат будет выведен после текста "Целочисленное деление:".

print("Нахождение остатка от деления:", a % b): В этой строке кода выполняется операция нахождения остатка от деления числа a на число b. Результатом будет остаток от деления 10 на 5, который равен 0. Этот результат будет выведен после текста "Нахождение остатка от деления:".

## Лабараторная работа 7

Создайте любую строковую переменную и произведите над ней математическое действие умножение на любое число.

 ```python
line = "Hello!"
print(line * 6)

```
### Результат

![7](https://github.com/Mikhail867/Software_Engineering/assets/144737787/be9e922e-1ca3-475b-b9a3-d053e926e6e5)


## Краткий вывод:
line = "Hello!": В этой строке кода объявляется переменная line и ей присваивается значение "Hello!" - это строка.

print(line * 6): Эта строка кода использует оператор умножения * для повторения строки line шесть раз. Таким образом, строка "Hello!" будет повторена шесть раз и результат будет выведен на экран. В данном случае, строка "Hello!" будет выведена шесть раз подряд.

## Лабараторная работа 8
Посчитайте сколько раз символ ‘o’ встречается в строке ‘Hello World’

 ```python

sentence= "Hello World"
print(sentence.count("o"))

```
### Результат
![8](https://github.com/Mikhail867/Software_Engineering/assets/144737787/35217545-a787-49e6-891c-59af7b5b0533)


## Краткий вывод:

sentence = "Hello World": В этой строке кода объявляется переменная sentence и ей присваивается значение "Hello World" - это строка.

print(sentence.count("o")): Эта строка кода использует метод count() для подсчета количества вхождений определенной подстроки в строку sentence. В данном случае, мы ищем букву "o" в строке "Hello World". Метод count("o") вернет количество раз, которое буква "o" встречается в строке. В результате выполнения этой строки кода будет выведено количество букв "o" в строке "Hello World".

## Лабараторная работа 9

Напишите предложение ‘Hello World’ в две строки. Написанная программа должна занимать одну строку в редакторе кода

 ```python
print("Hello\nWorld")
```
### Результат
![9](https://github.com/Mikhail867/Software_Engineering/assets/144737787/59a45988-f04b-4fd0-93fa-e09b482613ba)


## Краткий вывод:

"Hello\nWorld": Это строковый литерал, который состоит из двух слов: "Hello" и "World", разделенных символом \n. Символ \n является экранированным символом и представляет собой символ новой строки. Когда он встречается в строке, он указывает на перенос строки, что делает текст после символа \n на новой строке.

print("Hello\nWorld"): Эта строка кода использует функцию print() для вывода строки "Hello\nWorld" на экран. При выводе программа интерпретирует символ \n как инструкцию для переноса строки, поэтому текст "World" будет выведен на новой строке после "Hello".

## Лабараторная работа 10

Из предложения ‘Hello World’ выведите в консоль только 2 символ, а затем выведите слово ‘Hello’

 ```python
sentence = "Hello World"
print(sentence[1])
print(sentence[:5])

```
### Результат
![10](https://github.com/Mikhail867/Software_Engineering/assets/144737787/f46f21b5-2de5-4da0-8218-c81c2d66907a)


## Краткий вывод:
sentence = "Hello World": В этой строке кода объявляется переменная sentence и ей присваивается значение "Hello World" - это строка.

print(sentence[1]): Эта строка кода выводит символ из строки sentence по индексу 1. В Python индексы начинаются с 0, поэтому sentence[1] вернет символ, находящийся вторым в строке. В данном случае, это буква "e". Таким образом, программа выведет букву "e" на экран.

print(sentence[:5]): Эта строка кода использует срез строки для извлечения подстроки от начала строки до (не включая) индекса 5. В результате будет извлечена подстрока "Hello", состоящая из первых пяти символов строки sentence. Эта подстрока будет выведена на экран.
# Самостоятельные работы

## Самостоятельная работа №1

 Выведите в консоль булевую переменную False, не используя слово False в строке или изначально присвоенную булевую переменную. Программа должна занимать не более двух строк редактора кода.

 ```python

 print(0 == 1)

```

### Результат

![11](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-2/Pic/image.png)

## Краткий вывод:
 print(0 == 1) сравнивает два значения и возвращает ==, если они равны, и True, если они не равны.False
