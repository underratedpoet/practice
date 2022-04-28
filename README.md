# practice

Задача - создать алгоритм сортировки текста (от 3 тыс. символов до 15 тыс. символов). 
Индивидуальное задание: латиница, по кол-ву символов в слове, по убыванию, учитывать числа, сортировка слиянием.

Была написана функция чтения файла: каждое слово (последовательность символов, разделенная пробелами/переносами строки), перед тем, как быть добавленным в вектор, проверялось на наличие игнорируемых символов, которые, при нахождении, удалялись.

Была написана функция сортировки слиянием: массив (вектор) слов делился на две части (условно, копии массива в этот момент не создавались) до момента, когда часть становилась равной одному слову. Затем, в обратном порядке, части соединялись, сортируясь по убыванию. Копия сортируемой области создавалась только на время ее сортировки.

Была написана функция разделения сортировки слиянием на несколько потоков - при данных размерах файлов на создание и запуск потоков уходит больше времени, чем на однопоточкую сортировку. Уменьшение количества потоков до двух не дало результата. Функция и заголовочный файл закомментированы.

Был написан алгоритм анализа данных: в текстовый файл выводились исходный текст, индивидуальное задание, количество слов, время сортировки, статистика (количество слов каждой длины).

Отдельные части алгоритма перемещены в функции, функции переименованы.

Вместо двумерного массива создан массив (вектор) классов "ofwords", хранящих данные о количестве слов определенной длины. Добавлен ввод пути к файлу original через консоль, добавлено автоматическое создание имен файлов result и analysis на основе последнего символа файла original (к примеру, для файла original3.txt создавались бы файлы result3.txt и analysis3.txt).
