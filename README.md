# Дополнительные задачи

### Палиндром (1 балл)
Приложение для проверки, является ли введенная строка палиндромом.

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


### xargs (4 балла)
Приложение, которое принимает в качестве аргументов командной строки имя текстового файла и операцию, которую выполняет над каждой строкой текста.

Например: переданы аргументы "dirs.txt" "mkdir %s"

Приложение должно считать все строки из dirs.txt и запускать программу mkdir, подставляя вместо %s содержимое строк.


### Преобразование величин (4 балла)
(температура, валюты, объемы, масса и т.д.)

Приложение для преобразования между разными величинами.
Пользователь вводит тип исходной и целевой величины, а затем исходное значение. Программа должна преобразовать величину и вывести результат.

Программа должна поддерживать не менее 10 типов величин.


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


### Система управления версиями файлов

Утилита для сохранения версии файлов, находящихся в каталоге, и восстановления содержимого по номеру версии.

Функции утилиты:
- Сохранение текущего содержимого файлов. Версии присваивается номер, комментарий и дата.
- Просмотр сохраненных версий
- Восстановление сохраненной версии. Содержимое каталога должно стать таким же как было во время сохранения указанной версии.


### Копирование файла по сети

### Просмотрщик изображений

### Скачивание файла по ссылке

### Капча

### Web-Обозреватель файлов
