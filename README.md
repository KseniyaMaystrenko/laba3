# laba3

## 1 задание

условие:

![image](https://github.com/KseniyaMaystrenko/laba3/assets/152999073/ede9d4b1-8870-40c5-a8d8-8ccb41b3d4d6)

Объяснение решения:

с рекурсией

1. Функция `recursive` принимает исходный список в качестве аргумента.
2. Создается пустой список `new1`, в который будут записываться элементы из исходного списка.
3. Происходит итерирование по элементам изначального списка.
4. Если элемент является списком, кортежем или множеством, то к нему применяется рекурсия. Элементы из вложенных структур добавляются в конец нового списка `new1`.
5. Если элемент является словарем, то его элементы извлекаются с помощью метода `items()`, и затем к ним применяется рекурсия для добавления в `new1`.
6. Если элемент не является ни списком, ни кортежем, ни множеством, то он просто добавляется в список `new1`.
7. Функция возвращает распакованный список без вложенностей.
8. Исходный список `test` содержит вложенные структуры данных для проверки работы функции `recursive`.
9. Выводится исходный список `test`, а затем результат работы функции `recursive(test)`, который представляет собой плоский список без вложенностей, выводится на экран.

ответ:

![image](https://github.com/KseniyaMaystrenko/laba3/assets/152999073/565c99aa-2a7d-4d61-9056-78e9e8087858)

без рекурсии:

1. Данная программа включает функцию `nonrecursive`, которая используется для распаковки вложенных структур данных исходного списка без использования рекурсии.
2. Функция `nonrecursive` принимает исходный список `iterable`.
3. Устанавливается флаг `nested` в значение True, который служит стоп-сигналом для продолжения итераций в цикле.
4. Создается список `exception2`, который содержит типы данных (кроме словарей), для которых требуется распаковка.
5. Цикл `while` будет продолжаться, пока флаг `nested` установлен в True.
6. Внутри цикла создается временный пустой список `new2`, в который будут добавляться элементы распаковки.
7. Происходит итерация по элементам списка `iterable`.
8. Если элемент является списком, кортежем или множеством (тип из списка `exception2`), то их элементы добавляются в конец списка `new2` с помощью метода `extend()`, и флаг `nested` устанавливается в True для продолжения распаковки.
9. Если элемент является словарем, то его элементы извлекаются с помощью метода `items()` и добавляются в список `new2` с помощью `extend()`.
10. Если элемент не является ни списком, ни кортежем, ни множеством, то он просто добавляется в список `new2` с помощью `append()`.
11. После завершения итерации по всем элементам, список `iterable` заменяется на новый список `new2`, и цикл продолжается до тех пор, пока есть вложенные структуры для распаковки.
12. По завершении распаковки, функция возвращает итоговый распакованный список без вложенностей.
13. Создаётся тестовый список `test` с вложенными структурами для проверки работы функции.
14. Выводится исходный список `test` и результат работы функции `nonrecursive(test)`, который представляет собой список без вложенностей.

ответ:

![image](https://github.com/KseniyaMaystrenko/laba3/assets/152999073/f87b6271-b8cc-452c-9040-0a16a18fb4f1)


## 2 задание 

условие:

![image](https://github.com/KseniyaMaystrenko/laba3/assets/152999073/6f2b127b-d988-4304-b058-e7c127023db0)

Объяснение решения:

с рекурсией

1. Создается функция `w`, которая принимает один аргумент `i`.
2. Внутри функции проверяется условие: если `i` равно 1, то функция возвращает значение 0.3.
3. Затем, если `i` равно 2, функция возвращает значение -1.5.
4. В случае, если оба предыдущих условия не выполнились, функция возвращает результат выражения: `w(i-1)*w(i-2)*(((i-1)**2)/((i+1)**3))`.
5. В конце программы вызывается функция `w` с аргументом 5, что приводит к вычислению результата данного выражения для `i=5`.
6. Результатом выполнения кода будет число, которое будет выводится при вызове `print(w(5))

с рекурсией

![image](https://github.com/KseniyaMaystrenko/laba3/assets/152999073/05a892cf-cffa-4114-9723-c9a3247e4d91)

без рекурсии:

1. В коде определена функция `w(i)`, которая принимает аргумент `i`.
2. Создается словарь `values`, в котором для ключей 1 и 2 установлены начальные значения: 0.3 и -1.5 соответственно.
3. В цикле `for` выполняется итерация от 3 до `i + 1`.
4. На каждой итерации вычисляется новое значение для числа `j` в словаре `values` по формуле: `values[j] = values[j-1] * values[j-2] * (((j - 1) * 2) / ((j + 1) * 3))`.
5. Функция возвращает значение из словаря для ключа `i`.
6. После определения функции `w(i)`, вызывается функция `w(5)` и результат (значение для `i=5`) выводится на экран.

Таким образом, данный код вычисляет и выводит результат выражения на основе предопределенных начальных значений и формулы для последующих значений. В данном случае, выводится результат для `i=5`.


используемые источники:

[Функция](https://youtu.be/GLaH7YYO-2I?feature=shared)


2 ссылка
[Списки, кортежи, словари](https://youtu.be/Rq3UqTYc6mA?feature=shared)
