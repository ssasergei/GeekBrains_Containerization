##Задание 1:
> Развернуть и запустить контейнер с любым вашим образом(сайт на CMS, образ ОС, образ базы данных, что угодно). Использовать строго Compose!
> ### nano docker-compose.yaml
![yaml](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW5/docker-compose.yaml)
> ### docker-compose up -d
![1](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW5/screenshots/task1.jpg)

## Задание 2*:
> Установить 2 операционную систему в виртуальную машину(создать новый образ ОС). Создать кластер из двух машин(первой и второй), Сделать так, чтобы каждая нода могла управлять кластером (была лидером). Также необходимо добавить каждой ноде по метке: prod, stage или любые другие метки, но у каждой ноды должна быть своя отдельная метка. Проверить и убедиться, что метки действительно добавились. Раскатайте на 2 машины любое ваше приложение, проверьте, что контейнер с приложением создался. Использовать строго Swarm!

> ### docker swarm init
![2](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW5/screenshots/task2.jpg)
> ### docker node ls
![2-1](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW5/screenshots/task2-1.jpg)
> ### docker node promote gb-docker-02
> ### docker node ls
![2-3](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW5/screenshots/task2-2.jpg)
> ### docker service create --name nginx --replicas 3 --publish 250:80 nginx:alpine
> ### docker ps -a
![2-3](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW5/screenshots/task2-3.jpg)







