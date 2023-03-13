# 12.2. «Работа с данными (DDL/DML)» НиконоровДА FOPS-6

## Задание 1
1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

2. Создайте учётную запись sys_temp.

3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

4. Дайте все права для пользователя sys_temp.

5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:

```SQL
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
7. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

8. Восстановите дамп в базу данных.

9. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

Установлен MySQL, создана учтнаяя запись sys_temp. Выполнение запроса на получение списка
пользователей в БД

![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/1.png)

Даны все права пользователю sys_temp и запрос на получения списка прав для sys_temp
и произвел переподключение к БД от имени sys_temp

![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/2.png)

Использован запрос
```SQL
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/3.png)

Скачен дамп базы [Ссылка](https://downloads.mysql.com/docs/sakila-db.zip) и восстановлена в MySQL

![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/4.png)

![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/5.png)

Сформирована ER-диаграмма

![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/6.png)

![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/7.png)

Портянка запросов
```
CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY'password';

SELECT User,Host FROM mysql.user;

GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost';

SHOW GRANTS FOR 'sys_temp'@'localhost';

quit

mysql -u sys_temp -p

ALTER USER 'sys_temp'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

source /home/dn/Загрузки/sakila-db/sakila-schema.sql
```

## Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

![alt text](https://github.com/mxssclxck/hw-12.02/blob/main/img/8.png)
