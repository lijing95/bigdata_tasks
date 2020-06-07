# bigdata_tasks



Задача 1
Нужно написать две программы: 

Первая генерирует бинарный файл (min 2 Гб), состоящий из случайных 32-разрядных беззнаковых целых чисел (big endian). 

Вторая считает сумму этих чисел (с применением длинной арифметики), находит минимальное и максимальное число.

Реализуйте две версии - 
1. Простое последовательное чтение 
2. Многопоточная + memory-mapped files. Сравните время работы.



Задача 2
Нужно сгенерировать файл, содержащий 2000 128-битных случайных целых чисел, каждое число на отдельной строке.

Посчитать, какое суммарное количество простых множителей присутствует при факторизации всех чисел. 
Например, пусть всего два числа: 6 и 8. 6 = 2 * 3, 8 = 2 * 2 * 2. Ответ 5.
При реализации нужно использовать операции с длинной арифметикой (BigInteger и т.д.)

Реализовать подсчет

простым последовательным алгоритмом
многопоточно, с использованием примитивов синхронизации
с помощью Akka (или аналога)
c помощью RxJava (или аналога)
Измерить время выполнения для каждого случая. 
Использовать уровень параллельности в соответствии с числом ядер вашего CPU.




Задача 3
Часть 1
Нужно написать скрипт, который скачивает все данные прошедших президентских выборов для всех избирательных участков.

Входная точка по ссылке. Затем нужно перейти на сайты региональных избирательных комиссий. Результаты нужно сохранить в cvs-файл, sqlite базе данных или parquet-файле. В итоге должна получиться таблица с полями: - название региона - название ТИК - номер УИК - 20 стандартных полей из итогового протокола

Часть 2
Нужно, используя Spark: - найти явку (%) по всем регионам, результат отсортировать по убыванию - выбрать любимого кандидата и найти тот избиратльный участок, на котором он получил наибольший результат (учитывать участки на которых проголосовало больше 300 человек) - найти регион, где разница между ТИК с наибольшей явкой и наименьшей максимальна - посчитать дисперсию по явке для каждого региона (учитывать УИК) - для каждого кандидата посчитать таблицу: результат (%, округленный до целого) - количество УИК, на которых кандидат получил данный результат

Результаты принимаются в виде Jupyter Notebook, Spark Notebook или исходных файлов на Scala.



