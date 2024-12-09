# lab 4
Скачаем Dockerfile https://docs.docker.com/desktop/setup/install/linux/  
Установим через bash скрипт  
``` Dockerfile
FROM ubuntu:latest

RUN apt-get update && apt-get install -y libaa-bin
RUN apt-get install -y iputils-ping
CMD ["aafire"]
```  
Докачаем файлы ```snap instell docker```  
![image](https://github.com/user-attachments/assets/69e2177c-3e60-4e81-85f0-2aaee378b549)
Выполним команду для сборки образа ```docker build -t aafire_image .```  
![image](https://github.com/user-attachments/assets/9253e3a2-00c0-494a-84ac-c2136130d972)
Создадим сеть ```docker network create myNet```
Узнаем названия запущенных контейнеров ```docker ps```
Добави миконтейнеры в сеть ```docker network connect myNet reverent_engelbart sweet_mclaren```
![image](https://github.com/user-attachments/assets/412c1c4a-9bc7-41a5-9a45-77a089aed4d3)

