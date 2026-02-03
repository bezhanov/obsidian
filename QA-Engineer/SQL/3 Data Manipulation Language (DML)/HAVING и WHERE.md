Оператор `HAVING` используется в связке с `GROUP BY`, чтобы фильтровать строки на основе агрегатных функций. В свою очередь, оператор `WHERE` фильтрует строки перед группировкой. Проще говоря, `WHERE` используется для сужения поиска на уровне строк, а `HAVING` выбирает конкретные результаты после группировки.

```
SELECT department, COUNT(*) AS total_employees
FROM employees
GROUP BY department
HAVING total_employees > 10;
```