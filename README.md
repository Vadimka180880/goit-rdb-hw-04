Пояснення до завдання 4 

1. COUNT(*) — Підрахунок рядків
Запит із COUNT дозволяє дізнатись загальну кількість записів, які відповідають умовам INNER JOIN між order_details, orders і employees.

2. LEFT JOIN vs INNER JOIN
Якщо замінити INNER JOIN на LEFT JOIN, то кількість рядків може збільшитись, тому що будуть враховані всі записи з лівої таблиці, навіть якщо в правій немає відповідних значень.
RIGHT JOIN — аналогічно, але з перевагою правої таблиці.
Причина: INNER JOIN фільтрує тільки ті записи, які мають співпадіння в обох таблицях.

3. WHERE employee_id > 3 AND employee_id <= 10
Фільтрація дозволяє обрати лише замовлення, які обслуговували співробітники з id у вказаному діапазоні.

4. Групування по категорії
GROUP BY категорії дозволяє порахувати кількість записів на категорію і обчислити середню кількість замовлених одиниць товару.

5. HAVING avg_quantity > 21
HAVING використовується для фільтрації результатів після групування. В даному випадку обираються лише ті групи, де середнє значення кількості товарів більше за 21.

6. ORDER BY DESC
Результати сортуються за спаданням кількості рядків (кількість замовлень на категорію).

7. LIMIT + OFFSET
LIMIT 4 OFFSET 1 означає: пропустити перший рядок і вивести наступні 4. Використовується для посторінкового виводу або вибірки частини результатів.
