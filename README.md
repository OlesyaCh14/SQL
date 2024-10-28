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

# Задание 4:
Выгрузите все значения из таблицы buyer, отфильтровав клиентов:
по возрасту — меньше либо равен 30,
полу — мужской.
Возраст хранит поле age, а пол — gender.

SELECT *

FROM buyer

WHERE age <=30

AND gender ='Мужской';

# Задание 5:
Выгрузите поля bracelet_id, last_name и first_name из таблицы buyer. В выборку должны попасть клиенты:
от 30 до 48 лет включительно,
которые впервые подключились не в зонах «Роботические гонки» и «Робо-город»,
у которых нет скидки.
Возраст указан в поле age, зона первого подключения — в поле connection_area, а скидка — в поле percent_of_discount.

SELECT bracelet_id,

last_name,

first_name

FROM buyer

WHERE connection_area NOT IN ('Роботические гонки','Робо-город')

AND age IN (30,31,32,33,34,35,36,37,38,39,40,41,41,42,43,44,45,46,47,48)

AND percent_of_discount = 0;
