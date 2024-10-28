# SQL
В данном репозитории я буду писать SQL-запросы

# Задание 1:
Выгрузить из таблицы buyer поля bracelet_id, last_name и percent_of_discount. Назначить полям псевдонимы id, name_client и discount.

 SELECT bracelet_id AS id,

 last_name AS name_client,
 
 percent_of_discount AS discount
 
 FROM buyer;

# Задание 2:
Выгрузить все значения из таблицы buyer, отфильтровав возраст клиента: он должен быть меньше либо равен 30. Возраст хранит поле age.

SELECT *

FROM buyer

WHERE age <= 30;

# Задание 3:
Из таблицы buyer выгрузите несколько полей: first_name с именем покупателя, connection_area с указанием зоны первого подключения и company_marker. Оставьте записи только о тех покупателях, которые подключились в зоне «Роботический лабиринт».

SELECT first_name,
       connection_area,
       company_marker

FROM buyer

WHERE connection_area ='Роботический лабиринт';
