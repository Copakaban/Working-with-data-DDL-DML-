# Working-with-data(DDL-DML)

## Задание 1  
1.1 Локальный инстанс MySQL поднял на ноуте в Debian (пришлось поковыряться с подписью репозитория)   
1.2 Создал учетную запись sys_temp (CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY '2';)  
1.3 Выполняю запрос на получение списка пользователей в базе данных (SELECT host, user FROM mysql.user;):  
![image](https://github.com/Copakaban/Working-with-data-DDL-DML-/assets/118304300/a8f786e4-fefb-4feb-8fc9-e7d185731e90)  
1.4 Предоставляю все права пользователю sys_temp (GRANT ALL PRIVILEGES ON * . * TO 'sys_temp'@'localhost';)  
1.5 Выполняю запрос на получение списка прав для пользователя sys_temp (SHOW GRANTS FOR 'sys_temp'@'localhost';):  
![image](https://github.com/Copakaban/Working-with-data-DDL-DML-/assets/118304300/f295479c-d07f-4fbe-84d2-6f690c63b181)  
1.6 Переподключаюсь к БД от имени sys_temp:  
![image](https://github.com/Copakaban/Working-with-data-DDL-DML-/assets/118304300/34f35e17-b517-476c-ad3d-7451ab4551b3)  
Качаю дамп БД и восстанавливаю его:  
Для этого нужно создать БД с именем sakila, затем восстановить в нее дамп:
CREATE DATABASE `sakila`;  
USE sakila;  
SOURCE home/sv/sakila-db/sakila-data.sql;  
![image](https://github.com/Copakaban/Working-with-data-DDL-DML-/assets/118304300/97676076-8115-4b72-9851-d68b60af8b19)  

## Задание 2
| Название таблицы | Название первичного ключа |  
:----------:|:----------:|  
| actor | actor_id |  
| address	| address_id |  
| category	| category_id |  
| city |	city_id |  
| country	| country_id |  
| customer |	customer_id |  
| film |	film_id |   
| film_actor |	actor_id; film_id |  
| film_category |	film_id; category_id |  
| film_text |	film_id |   
| inventory	| inventory_id |  
| language |	language_id |  
| payment	| payment_id |  
| rental |	rental_id |  
| staff |	staff_id |  
| store |	store_id; manager_staff_id |  






