# FAQ
необходимые заметки
Учебные шпаргалки в период обучения
-----------------------------------

##### Содержание
[Всё по SQL](#sql)

<a name="sql"><h2>Всё по SQL</h2></a>
# Содержание SQL
[Особенности и фишки SQL](#priority_sql)

[Ссылки на различную документацию](#link_sql)

[Различные найденные полезные заметки](#note_sql)

<a name="priority_sql"><h2>Особенности и фишки SQL</h2></a>

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
