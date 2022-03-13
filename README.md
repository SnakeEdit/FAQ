# FAQ
необходимые заметки
Учебные шпаргалки в период обучения
-----------------------------------

##### Содержание
[Всё по SQL](#sql)

[Всё по Python](#py)

<a name="sql"><h2>Всё по SQL</h2></a>
# Содержание SQL
[Особенности и фишки SQL](#priority_sql)

[Ссылки на различную документацию](#link_sql)

[Различные найденные полезные заметки](#note_sql)

<a name="priority_sql"><h2>Особенности и фишки SQL</h2></a>

<h6>Порядок написания операций в SQL:</h6>

1. FROM + JOIN
2. WHERE
3. GROUP BY
4. HAVING
5. SELECT (windows function happen here!)
6. ORDER BY
7. LIMIT

<h6>Приоритеты операций:</h6>

1. круглые скобки
2. умножение  (*),  деление (/)
3. сложение  (+), вычитание (-)
4. операторы сравнения (=, >, <, >=, <=, <>)
5. NOT
6. AND
7. OR

<h6>Логический порядок операций для запроса SQL следующий:</h6>

1. FROM
2. WHERE
3. SELECT
4. ORDER BY

<a name="link_sql"><h2>Ссылки SQL</h2></a>
[Руководство по стилизации SQL кода и правилах хорошего тона](https://www.sqlstyle.guide/ru/#предисловие)

[Шпаргалка функций SQL](https://www.sqltutorial.org/wp-content/uploads/2016/04/SQL-cheat-sheet.pdf)

[Автокорректор кода SQL](https://codebeautify.org/sqlformatter) - лучше его применять с осторожностью

<a name="note_sql"><h2>Заметки по SQL</h2></a>
* В некоторых реализациях SQL (SQL Server, SQL Postgres 10) - Вместо AUTO_INCREMENT используется IDENTITY (В более старых версиях SQL - SERIAL)
* В PostgreSQL вместо IF  используют конструкцию CASE ... WHEN ... THEN ... ELSE ... END [и некоторые другие](https://www.postgresql.org/docs/12/functions-conditional.html).


<a name="py"><h2>Всё по Python</h2></a>
# Содержание SQL
[Реализации на Python](#projects_py)

[Особенности и фишки Python](#priority_py)

[Ссылки на различную документацию](#link_py)

[Различные найденные полезные заметки](#note_py)

<a name="_projects_py"><h2>Реализации на Python</h2></a>
<h6>Алгоритмы сортировки:</h6>
<

    def sort_choise(array): # СОРТИРОВКА ВЫБОРОМ
        for i in range(len(array) - 1):
            m = i
            j = i + 1
            while j < len(array):
                if array[j] < array[m]:
                    m = j
                j = j + 1
            array[i], array[m] = array[m], array[i]
            print(array)

    def sort_insertion(array): # СОРТИРОВКА ВСТАВКАМИ
        for i in range (len(array)):
            j= i
            t = a[j]
            while j > 0 and t < a[j-1]:
                a[j] = a[j-1]
                j = j-1
            a[j] = t
            print(array)

    def sort_merge(array): # СОРТИРОВКА СЛИЯНИЕМ
        if len(array) > 1:
            mid = len(array) // 2
            low = array[:mid]
            high = array[mid:]

            sort_merge(low)
            sort_merge(high)

            i = 0
            j = 0
            k = 0

            while i < len(low) and j < len(high):
                if low[i] <= high[j]:
                    array[k] = low[i]
                    i += 1
                else:
                    array[k] = high[j]
                    j += 1
                k += 1

            while i < len(low):
                array[k] = low[i]
                i += 1
                k += 1

            while j < len(high):
                array[k] = high[j]
                j += 1
                k += 1
            print("Нижний полусписок:", low, "Верхний полусписок:", high)

    def part (array, left, right): #БЫСТРАЯ СОРТИРОВКА
        pivot = array[left]
        i = left + 1
        o = right
        while True:
            while i <= o and array[o] >= pivot:
                o = o - 1

            while i <= o and array[i] <= pivot:
                i = i + 1

            if i <= o:
                array[i], array[o] = array[o], array[i]
                print(array)
            else:
                break

        array[left], array[o] = array[o], array[left]
        print(array)

        return o


    def sort_quick(array, left, right):
        if left >= right:
            return

        par = part(array, left, right)
        sort_quick(array, left, par - 1)
        sort_quick(array, par + 1, right)
 >

