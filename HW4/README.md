## Задание: необходимо создать Dockerfile, основанный на любом образе (вы в праве выбрать самостоятельно).
> В него необходимо поместить приложение, написанное на любом известном вам языке программирования (Python, Java, C, С#, C++).
При запуске контейнера должно запускаться самостоятельно написанное приложение.\
>### nano Dockerfile
>> #### Используем Alpine Linux как базовый образ
>> FROM python:3.9-alpine
>> #### Устанавливаем рабочую директорию
>> WORKDIR /sem4
>> #### Копируем файлы проекта в образ
>> COPY app.py /sem4/
>> #### Запускаем приложение
>> CMD ["python", "app.py"]
> ### nano app.ry
>> print("Hello Word")
> ### docker build -t app .
![1](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW4/screenshots/task1.jpg)
> ### docker run app
![2](https://github.com/ssasergei/GeekBrains_Containerization/blob/master/HW4/screenshots/task1-1.jpg)

