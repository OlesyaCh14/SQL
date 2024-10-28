# SQL
В данном репозитории я буду писать SQL-запросы

Задание 1:
Выгрузите из таблицы buyer поля bracelet_id, last_name и percent_of_discount. Назначьте полям псевдонимы id, name_client и discount.
SELECT bracelet_id AS id,
last_name AS name_client,
percent_of_discount AS discount
FROM buyer;
