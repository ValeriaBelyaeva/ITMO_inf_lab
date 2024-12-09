# lab 4
Скачаем Dockerfile https://docs.docker.com/desktop/setup/install/linux/  
Установим через bash скрипт 
```
FROM ubuntu:latest

RUN apt-get update && apt-get install -y libaa-bin
RUN apt-get install -y iputils-ping
CMD ["aafire"]
```
Докачаем файлы ```snap instell docker```
![image](https://github.com/user-attachments/assets/69e2177c-3e60-4e81-85f0-2aaee378b549)


