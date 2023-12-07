# Тема 10. Декораторы и исключения
Отчет по Теме #10 выполнил(а):
- Демаков Артемий Игоревич
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 |  | |
| Задание 7 |  | |
| Задание 8 |  |  |
| Задание 9 |  |  |
| Задание 10 |  |  |

# Лабараторные работы 
   ## Лабараторная работа 1


  ```python
from functools import lru_cache

@lru_cache(None)
def fibonacci(n):
    if n==0:
        return 0
    elif n == 1:
        return 1
    return fibonacci(n-1) + fibonacci(n-2)

if __name__== '__main__':
    print(fibonacci(100))

```
  ### Результат
  ![1](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Lab%201.png)

 
## Краткий вывод:

Декоратор @lru_cache(None):

lru_cache используется для кэширования результатов вызовов функции с определенными аргументами.
None в качестве аргумента lru_cache означает, что размер кэша неограничен, и результаты будут кэшироваться бесконечно.
Функция fibonacci(n):

Рекурсивная функция для вычисления числа Фибоначчи.
Если n равно 0, возвращается 0.
Если n равно 1, возвращается 1.
В остальных случаях вызывается рекурсивно для fibonacci(n-1) + fibonacci(n-2).
Вызов fibonacci(100):

В блоке if __name__ == '__main__': вызывается функция fibonacci с аргументом 100.
Из-за использования lru_cache, результаты вызовов функции для различных значений n будут кэшироваться.
Это позволяет избежать повторных вычислений для тех же аргументов, что ускоряет выполнение программы.
Вывод результата:

Результат вызова fibonacci(100) выводится с помощью print.
Этот код эффективно использует кэширование для оптимизации вычислений числа Фибоначчи и предотвращения повторных вычислений для одних и тех же значений n.

   ## Лабараторная работа 2


  ```python
def check(input_func):
    def output_func(*args):
        name,age = args[0],args[1]

        if age<0 or age>130:
            age = 'Недопустимый возраст'
        input_func(name,age)

    return output_func

@check
def personal_info(name, age):
    print(f"Name: {name} Age: {age}")

if __name__ =='__main__':
    personal_info('Владимир',38)
    personal_info('Александр', -5)
    personal_info('Петр',138,15,48,2)
```
  ### Результат
  ![2](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/lab%202.png)

 
## Краткий вывод:
Декоратор check:

Принимает функцию input_func в качестве аргумента.
Функция output_func:

Эта функция является внутренней функцией, возвращаемой декоратором.
Принимает произвольное количество аргументов *args.
Извлекает из аргументов name и age.
Проверяет, является ли возраст (age) отрицательным или больше 130. Если да, то устанавливает age в строку 'Недопустимый возраст'.
Затем вызывает исходную функцию input_func с обработанными аргументами.
Использование декоратора:

Функция personal_info помечена декоратором @check.
Когда вызывается personal_info('Владимир', 38), декоратор оборачивает вызов, проверяет возраст, и затем вызывает оригинальную функцию input_func.
То же самое происходит для последующих вызовов personal_info.
Вывод результатов:

Код выполняет три вызова personal_info с разными аргументами.
В результате выполнения проверок возраста выводятся соответствующие сообщения.


   ## Лабараторная работа 3


  ```python
def data(*args):
    try:
        for i in range(len(*args)):
            try:
                result = (args[0][1]*15)//10
                print(result)
            except Exception as ex:
                print(ex)
    except Exception as ex:
        print(ex)
    finally:
        print('Вся информация обработана')


if __name__== '__main__':
    data([1,15,'hello','i','try','to','crash','your','siste',38,45])

```
  ### Результат
  ![3](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Lab%203.png)

 
## Краткий вывод:
Код обрабатывает каждый элемент списка, пытаясь выполнить вычисления и выводить результат.
Если происходит ошибка, она перехватывается и выводится сообщение об ошибке.
В блоке finally выводится сообщение 'Вся информация обработана'.


   ## Лабараторная работа 4


  ```python
class NegativeValueException(Exception):
    pass

def check_name(name):
    if len(name)>10:
        raise NegativeValueException('Длина более 10 символов')
    else:
        print('Успешная регестрация ')
        
        
if __name__ == '__main__':
    name='12345678910'
    check_name(name)
```
  ### Результат
  ![4](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Lab%204.png)

 
## Краткий вывод:

В данном коде определено новое исключение NegativeValueException, которое является подклассом встроенного класса Exception. Далее, определена функция check_name(name), которая проверяет длину переданного имени и выбрасывает исключение NegativeValueException, если длина больше 10 символов. В случае успешной регистрации, выводится сообщение.

В блоке if __name__ == '__main__': создается строка name с длиной 11 символов, и вызывается функция check_name(name).

Таким образом, при выполнении кода происходит следующее:

Строка name содержит 11 символов.
Функция check_name вызывается с этой строкой в качестве аргумента.
Так как длина строки больше 10 символов, вызывается исключение NegativeValueException с сообщением 'Длина более 10 символов'.
Программа завершается с выводом сообщения об ошибке, так как исключение не обрабатывается.
Если бы строка name содержала 10 символов или менее, то программа бы успешно завершилась, и выводилось бы сообщение 'Успешная регистрация'.

   ## Лабараторная работа 5


  ```python
class SiteChecker:
    def __init__(self,func):
        print('>Класс SiteCheker метод __init__ успешный запуск')
        self.func = func
    def __call__ (self):
        print(">Проверка перед запуском", self.func.__name__)
        self.func()
        print('>Проверка безопасного выключения')

@SiteChecker
def site():
    print('Усердная работа сайта')
if __name__ == '__main__':
    print('>>Сайт запущен')
    site()
    print('>> Сайт выключен')
```
  ### Результат
  ![5](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Lab%205.png)

 
## Краткий вывод:
Определение класса SiteChecker:

Конструктор __init__ принимает функцию func и сохраняет ее в атрибут self.func.
Метод __call__ вызывается, когда экземпляр класса используется как декоратор.
В методе __call__ выводятся сообщения о проверке перед запуском, запуске функции (self.func()) и проверке безопасного выключения.
Определение функции site:

Функция site украшена декоратором @SiteChecker, что означает, что при вызове функции site, будет использован этот декоратор.
Вызов декорированной функции в блоке if __name__ == '__main__'::

Выводится сообщение 'Сайт запущен'.
Вызывается функция site, которая декорирована классом SiteChecker.
Внутри класса SiteChecker выводятся сообщения о проверке перед запуском, запуске функции и проверке безопасного выключения.
Выводится сообщение 'Сайт выключен'.





# Самостоятельные работы
 ## Самотоятельная работа 1


  ```python
import time

def timing_decorator(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        execution_time = end_time - start_time
        print(f"Функция {func.__name__} выполнялась {execution_time:.6f} секунд")
        return result
    return wrapper

@timing_decorator
def fibonacci_recursive(n):
    if n <= 1:
        return n
    else:
        return fibonacci_recursive(n - 1) + fibonacci_recursive(n - 2)

if __name__ == '__main__':
    result = fibonacci_recursive(30)
    print(f"Результат вычисления Фибоначчи: {result}")
```
  ### Результат
  ![6](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Sum%201.png)

 
## Краткий вывод:
Определение декоратора timing_decorator:

Принимает функцию func и возвращает новую функцию wrapper.
wrapper измеряет время выполнения функции, вызывает func и выводит информацию о времени выполнения.
Декорирование функции fibonacci_recursive с помощью @timing_decorator:

Это эквивалент вызова fibonacci_recursive = timing_decorator(fibonacci_recursive).
При вызове fibonacci_recursive(30) будет использоваться уже декорированная функция.
Вызов декорированной функции в блоке if __name__ == '__main__'::

Вызывается функция fibonacci_recursive с аргументом 30.
Декоратор измеряет время выполнения функции и выводит информацию в консоль.
Выводится результат вычисления Фибоначчи для n=30.
Итог:

Программа выводит информацию о времени выполнения функции fibonacci_recursive и результат вычисления числа Фибоначчи для n=30.

  ## Самотоятельная работа 2


  ```python
try:
   
    with open('empty_file.txt', 'r') as empty_file:
        data = empty_file.read()
        if not data:
            raise Exception("Файл пустой")
        else:
            print(f"Информация из файла:\n{data}")
except Exception as empty_exception:
    print(empty_exception)

try:
   
    with open('non_empty_file.txt', 'r') as non_empty_file:
        data = non_empty_file.read()
        if not data:
            raise Exception("Файл пустой")
        else:
            print(f"Информация из файла:\n{data}")
except Exception as non_empty_exception:
    print(non_empty_exception)

```
  ### Результат
  ![7](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Sum%202.png)

 
## Краткий вывод:
Первый блок try с файлом Emp.txt:

Открывает файл Emp.txt для чтения ('r').
Считывает содержимое файла в переменную data.
Проверяет, является ли файл пустым (if not data:).
Если файл пустой, вызывает исключение Exception с сообщением "Файл пустой".
В противном случае выводит информацию из файла.
Первый блок except с переменной Emp_exception:

Если произошло исключение в первом блоке try, выводит сообщение об ошибке, указывающее на то, что файл пустой.
Второй блок try с файлом Full.txt:

Открывает файл Full.txt для чтения ('r').
Считывает содержимое файла в переменную data.
Проверяет, является ли файл пустым (if not data:).
Если файл пустой, вызывает исключение Exception с сообщением "Файл пустой".
В противном случае выводит информацию из файла.
Второй блок except с переменной Full_exception:

Если произошло исключение во втором блоке try, выводит сообщение об ошибке, указывающее на то, что файл пустой.
  ## Самотоятельная работа 3


  ```python
def add_two_numbers():
    try:
        user_input = input("Введите число: ")
        user_number = float(user_input)
        result = 2 + user_number
        print(f"Результат сложения: {result}")
    except ValueError:
        print("Неподходящий тип данных. Ожидалось число.")

if __name__ == "__main__":
    add_two_numbers()

```
  ### Результат
  ![8](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Sum%203.png)

 
## Краткий вывод:
user_input = input("Введите число: ") запрашивает у пользователя ввод числа в виде строки.
user_number = float(user_input) пытается преобразовать введенное значение в число типа float.
Если пользователь ввел строку или другой неподходящий тип данных, возникает исключение ValueError.
В блоке except ValueError обрабатывается ошибка, и выводится сообщение "Неподходящий тип данных. Ожидалось число.".
Если введенные данные успешно преобразованы, программа складывает 2 и введенное число и выводит результат

  ## Самотоятельная работа 4


  ```python
import time

class TimingDecorator:
    def __init__(self, func):
        self.func = func

    def __call__(self, *args, **kwargs):
        start_time = time.time()
        result = self.func(*args, **kwargs)
        end_time = time.time()
        execution_time = end_time - start_time

        print(f"Время выполнения функции {self.func.__name__}: {execution_time:.6f} секунд")
        print(f"Результат выполнения функции: {result}")


@TimingDecorator
def add_numbers(a, b):
    return a + b

@TimingDecorator
def multiply_numbers(x, y):
    return x * y

if __name__ == "__main__":
  
    add_result = add_numbers(3, 5)
    multiply_result = multiply_numbers(4, 6)
```
  ### Результат
  ![9](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Sum%204.png)

 
## Краткий вывод:
Класс TimingDecorator:

Принимает функцию func в конструкторе.
В методе __call__ вызывает функцию, измеряет время выполнения и выводит информацию.
Декорированные функции squered_numbers и triple_numbers:

При объявлении функций используется декоратор @TimingDecorator.
Это эквивалент вызова squered_numbers = TimingDecorator(squered_numbers) и triple_numberss = TimingDecorator(triple_numbers).
Блок if __name__ == "__main__":

Вызывает декорированные функции, их выполнение будет сопровождаться выводом времени выполнения и результатов

  ## Самотоятельная работа 5


  ```python
class DataNotFoundException(Exception):
    def __init__(self, message="Данные не найдены в системе"):
        self.message = message
        super().__init__(self.message)

def process_data(data):
    if not data:
        raise DataNotFoundException()


if __name__ == "__main__":
    try:
       
        data1 = None
        process_data(data1)
    except DataNotFoundException as e1:
        print(f"Ошибка 1: {e1.message}")

    try:
        
        data2 = "Some data"
        process_data(data2)
    except DataNotFoundException as e2:
        print(f"Ошибка 2: {e2.message}")
```
  ### Результат
  ![10](https://github.com/GhoulSSSr4nk/Software_Eng/blob/Тема-10/pic/Sum%205.png)

## Краткий вывод:
 Класс DataNotFoundException:

Это собственное исключение, унаследованное от базового класса Exception.
Принимает сообщение об ошибке по умолчанию, если не предоставлено другое.
Функция process_data:

Проверяет, есть ли данные в системе.
Если данных нет, вызывает исключение DataNotFoundException.
Блок if __name__ == "__main__":

Фрагмент 1: Вызывает функцию с пустыми данными, обрабатывает исключение и выводит сообщение об ошибке.
Фрагмент 2: Вызывает функцию с непустыми данными, но исключение не происходит.
# Общий вывод
Декораторы:

Определение: Декораторы в Python - это способ изменять или расширять поведение функций или методов без изменения их кода.
Синтаксис: Могут быть реализованы как функции, классы или методы. Используют символ @ перед определением функции.
Примеры встроенных декораторов:
@staticmethod, @classmethod - для статических и классовых методов соответственно.
@property - для создания свойства объекта.
@classmethod - для создания методов класса.
Создание собственных декораторов: Можно создавать собственные декораторы с использованием функций или классов. Декораторы могут принимать аргументы.
Применение: Часто используются для измерения времени выполнения функций, логирования, кэширования, обработки входных данных и других аспектов.
Исключения:

Определение: Исключения в Python представляют собой события, возникающие во время выполнения программы, указывающие на возможные ошибки или исключительные ситуации.
Структура исключений: Исключения являются объектами классов, унаследованных от базового класса Exception.
Обработка исключений: Выполняется с использованием конструкции try-except. Код, который может вызвать исключение, помещается в блок try, а обработка исключения - в блок except.
Иерархия исключений: Различные типы исключений представлены разными классами. Например, ValueError, TypeError, FileNotFoundError и другие.
Создание собственных исключений: Можно создавать собственные исключения, наследуя их от базового класса Exception.
Использование исключений: Исключения позволяют более гибко управлять ошибками, предоставляя возможность обработки ошибок и восстановления после них.
Общий вывод:

Декораторы предоставляют механизм для изменения или расширения поведения функций без изменения их кода.
Исключения используются для обработки ошибок и исключительных ситуаций, позволяя программе более гибко реагировать на возможные проблемы во время выполнения.
Оба механизма играют важную роль в создании устойчивых и гибких программ. Декораторы обеспечивают удобство в управлении поведением функций, а исключения помогают обрабатывать и уведомлять о возможных проблемах.
