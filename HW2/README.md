## Задание 1:

> запустить контейнер с ubuntu, используя механизм LXC \
lxc-create --name=gbtest --template=ubuntu -f /usr/share/doc/liblxc-common/examples/lxc-veth.conf

![1](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW2/screenshots/task1.jpg)

> ограничить контейнер 256 Мб ОЗУ и проверить, что ограничение работает \
nano /var/lib/lxc/gbtest/config\
>>lxc.cgroup2.memory.max = 256M


![2](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW2/screenshots/task2.jpg)

> добавить автозапуск контейнеру, перезагрузить ОС и убедиться, что контейнер действительно запустился самостоятельно\
nano /var/lib/lxc/gbtest/config\
>>lxc.start.auto = 1

![3](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW2/screenshots/task3.jpg)