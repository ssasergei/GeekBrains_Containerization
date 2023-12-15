Задание:
> запустить контейнер с БД, отличной от mariaDB, используя инструкции на сайте: https://hub.docker.com/

>> docker network create docnet\
>> docker run --name postgrescont -e POSTGRES_PASSWORD=1111 --network docnet -e HOSTNAME=$(hostname) -d postgres

[!1](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW3/screenshots/task1.jpg)

> добавить в контейнер hostname такой же, как hostname системы через переменную/
>> docker run --name postgrescont -e POSTGRES_PASSWORD=1111 --network docnet -e HOSTNAME=$(hostname) -d postgres

[!1](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW3/screenshots/task1.jpg)

> заполнить БД данными через консоль/
>>CREATE DATABASE GB;\
>>create table Student (stid int not null GENERATED ALWAYS AS  PRIMARY KEY, name varchar(15), age int);\
>>INSERT INTO Student (name, age) VALUES ('Sergei', 30),('Alex', 25);


[!2](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW3/screenshots/task2.jpg)

[!2-1](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW3/screenshots/task2-1.jpg)

> запустить phpmyadmin (в контейнере) и через веб проверить, что все введенные данные доступны.
УЧТИТЕ, что если используете Postgres, то вместо phpmyadmin придется ставить adminer, он универсальный и минималистичный, совместим со всеми СУБД, а вот графическая оболочка PhpMyAdmin - только с Mysql и MariaDB! А так все остальное - по условиям выше!
>> docker run --name admindb --network docnet -p 8580:8080 adminer

[!2](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW3/screenshots/task3.jpg)