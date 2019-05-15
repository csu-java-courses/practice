# Дополнительные задачи

### Палиндром (1 балл)
Приложение для проверки, является ли введенная строка палиндромом.

### Сумма кубов (1 балл)
Существуют натуральные числа, равные сумме кубов своих цифр. Например 3^3+7^3+0^3=370.
Составьте программу, которая будет находить все такие числа в заданных пределах.

### Скобки (1 балл)
В строке проверить соответствие открывающихся "(" и закрывающихся ")" скобок. 
Вывести на экран число пар скобок, если соответствие выполняется, или сообщение "ОШИБКА" в противном случае.
В строке вида ")(" соответствие не выполняется.

### Буквы (2 балла)
Дан текст. Нужно подсчитать частоту вхождения каждой буквы алфавита в процентах и вывести на экран.

### Операции над строками (3 балла)
Приложение, которое принимает из stdin текст и выводит результат операции над ним.
Операция задется аргументами командной строки.

Операции:
- Вывести количество символов в тексте
- Вывести количество слов в тексте
- Вывести количество строк в тексте
- Вывести максимальную длину строки в тексте
- Перевести текст в верхний регистр
- Перевести текст в нижний регистр

### Ход конем (4 балла)
Написать программу обхода шахматной доски конем, начиная с указанной клетки. На каждой клетке конь должен побывать ровно один раз.

### xargs (4 балла)
Приложение, которое принимает в качестве аргументов командной строки имя текстового файла и операцию, которую выполняет над каждой строкой текста.

Например: переданы аргументы "dirs.txt" "mkdir %s"

Приложение должно считать все строки из dirs.txt и запускать программу mkdir, подставляя вместо %s содержимое строк.


### Преобразование величин (4 балла)
(температура, валюты, объемы, масса и т.д.)

Приложение для преобразования между разными величинами.
Пользователь вводит тип исходной и целевой величины, а затем исходное значение. Программа должна преобразовать величину и вывести результат.

Программа должна поддерживать не менее 10 типов величин.

### Векторная арифметика (4 баллов)
Составить описание класса для объектов-векторов, задаваемых координатами концов в трехмерном пространстве. Обеспечить операции сложения и вычитания векторов с получением нового вектора (суммы или разности), вычисления скалярного произведения двух векторов, длины вектора, косинуса угла между векторами.

### Система управления версиями файлов (5 баллов)

Утилита для сохранения версии файлов, находящихся в каталоге, и восстановления содержимого по номеру версии.

Функции утилиты:
- Сохранение текущего содержимого файлов. Версии присваивается номер, комментарий и дата.
- Просмотр сохраненных версий
- Восстановление сохраненной версии. Содержимое каталога должно стать таким же как было во время сохранения указанной версии.

### Перемещение файлов (6 баллов)
Утилита для перемещения файлов из одного каталога в другой.
В качестве аргументов задаются исходный и целевой каталог.
После перемещения утилита выдает отчет о перемещени.

Алгоритм перемещения следующий:
- Если файл есть в исходном каталоге и отсутствует в целевом, то переместить файл
- Если файл есть также и в целевом каталоге, то сравнить их побайтово:
  * Если содержимое одинаково, то удалить файл из исходного каталога
  * Если файл в целевом каталоге короче исходного, и при этом совпадает с началом исходного, то заменить целевой файл исходным
  * Если файл в исходном каталоге короче исходного, и при этом совпадает с началом целевого, то удалить исходный файл
  * В других случаях добавить сообщение о файле в отчет и ничего не делать с файлами
- Если подкаталог есть в исходном каталоге и отсутствует в целевом, то переместить подкаталог
- Если подкаталог есть также и в целевом каталоге, то рекурсивно зайти в него и обработать содержимое по этому же алгоритму

### BBCode (7 баллов)
Реализовать программу для форматирования BBCode. Исходный текст подается в stdin, результат должен быть выведен в stdout.

Все слова в отформатированном тексте должны быть разделены одним пробелом. Все теги должны занимать отдельные строки.
Исключение - содержимое тега `[pre]` не должно изменяться.

https://ru.wikipedia.org/wiki/BBCode

Синтаксис тегов: https://www.bbcode.org/reference.php

Например:
```
This 
  is some text.
[center]
  This  [size = 14] is  [/size]
  some
[b]centered[/b]text.[/center]
```

Результат:
```
This is some text.
[center]
  This
  [size=14]
    is
  [/size]
  some
  [b]
    centered
  [/b]
  text.
[/center]
```



### Инвертированный индекс (8 баллов)
https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D0%B2%D0%B5%D1%80%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B9_%D0%B8%D0%BD%D0%B4%D0%B5%D0%BA%D1%81

Реализовать приложение для составления поискового индекса для набора документов и поиску по нему.

Необходимые функции:
- Добавление текстового файла в индекс
- Удаление файла их индекса
- Загрузка и сохранение индекса в файл
- Поиск в проиндексированных документах по введенному слову. Приложение должно выводить имена файлов и номера строк, в которых встречается введенное слово.

Например:
```
> обычно
Файл: doc1.txt, строка: 42
Файл: stihi.txt, строка: 175
```

### Викторина (8 баллов)
Приложение для проведение викторин или тестирования.
При запуске читает указанный файл и задает вопросы из него в случайном порядке.
После ответа на все вопросы выдает набранное количество баллов.

Содержимое файла:
- Название викторины
- Сколько вопросов из базы нужно задать
- Количество баллов для выигрыша/прохождения теста
- База вопросов

Каждый вопрос в базе имеет тип, текст вопроса, варианты ответа с баллами за этот ответ.

Типы вопросов:
- Выбор одного из нескольких вариантом
- Выбор нескольких вариантов
- Поле для ввода строки

Файл должен быть защищен от прочтения через текстовый редактор (например зашифрован).


### Пересечение треугольников (10 баллов)
Пользователь задает координаты двух треугольников. 
Приложение должно вывести координаты точек пересечения ребер треугольников и площадь фигуры, образованной пересечением треугольников.

Приложение должно корректно обрабатывать ситуации, когда заданы некорректные координаты, также когда треугольники не пересекаются, и когда ребра треугольников частично или полностью совпадают.

### 100 (10 баллов)

Дана последовательность из 8 цифр. Нужно расставить между ними знаки арифметических операций так, чтобы получилось число 100.

Возможные операции: + - * /

Пример: 98765432

Результат
```
98+7+6-5-4*3/2=100
98+7-6-5+4*3/2=100
98+7-6*5/4/3*2=100
98+7*6+5-43-2=100
98+7*6-5/4*32=100
...
```
(Дополнительные 5 баллов можно получить, решив эту задачу, используя многопоточное программирование)



### * Копирование файла по сети (5 баллов)

Утилита для копирования файла ерез локальную сеть.

Режимы работы:
- утилита слушает на указанном порту и при подклюении передает указанный файл
- утилита слушает на указанном порту и при подклюении принимает файл
- утилита подключается на указанный ip и порт и передает указанный файл
- утилита подключается на указанный ip и порт и принимает файл


### * Просмотрщик изображений (5 баллов)

Приложение на Swing для просмотра изображений из указанного каталога.
Должен быть реализован режим автоматического перелистывания изображений по таймеру.

### * Скачивание файла по ссылке (4 балла)

Утилита для скаивания файла по указанной ссылке на диск.

Утилита должна выводить прогресс скачивания в консоль, например так:
```
0% 0/1024 байт
1% 10/1024 байт
...
```

### * Капча (7 баллов)

Утилита для генерации изображения-капчи (captcha).

https://ru.wikipedia.org/wiki/%D0%9A%D0%B0%D0%BF%D1%87%D0%B0

Передаваемые параметры:
- Ширина и высота изображения
- Текст изображения
- Имя файла

При генерации необходимо использовать минимум 5 эффектов (например сдвиг букв, масштабирование, размытие, наложение и т.д.)

