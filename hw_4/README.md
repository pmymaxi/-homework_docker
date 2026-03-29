### Домашнее задание к занятию 4 «Оркестрация группой Docker контейнеров на примере Docker Compose»
#### Задача 1
DockerHub: https://hub.docker.com/repository/docker/pmymaxi/custom-nginx/general

#### Задача 2
<img width="1908" height="810" alt="hw-img-1" src="https://github.com/user-attachments/assets/96229703-f811-4e18-a9b1-116267c88139" />

#### Задача 3
П.3. При подключении к стандартному потоку stdin/ stdout/stderr (в нашем случае к потоку nginx) с последующем выходом через комбинацию Ctrl+C, мы отправляем нашему процессу сигнал SIGINT (остановка и завершение). Так как процесс nginx у нас один, а также он в контейнере является родителем всех остальных процессов, то происходит завершение всех процессов и остановка контейнера.

П.10. Проблема в несоответствии порта на сервисе и порта правила forward port на хосте. Хост пересылает запросы с порта 8080 на порт контейнера 80. Сервис слушает порт 81. 

<img width="2250" height="1628" alt="hw-img-2" src="https://github.com/user-attachments/assets/4a9a78e7-5cce-4d88-8d34-2290af11c9d2" />

#### Задача 4

<img width="1896" height="646" alt="hw-img-4" src="https://github.com/user-attachments/assets/4e57abda-f973-4366-b6b0-114e19ad0d12" />

#### Задача 5
П.1. Файл compose.yaml (yml) выбран Docker Compose для запуска, так как этот файл выбирается по умолчанию в проекте. Файлы docker-compose.yaml (yml) также поддерживаются, но необходимы для обратной совместимости более ранних версий.

П.7. Docker Compose обнаруживает, что в файле docker-compose.yaml отсутствуют ранее созданные контейнеры (сервисы)файлом compose, за исключением одного контейнера,  и предлагает их очистить с текущего проекта дополнительным флагом --remove-orphans. Те сервисы, которые он очистил они становятся orphans (не привязанные к каталогу проекта), но при этом не удаляются. 

<img width="1884" height="3188" alt="hw-img-6" src="https://github.com/user-attachments/assets/fd996b26-a733-4d7d-894a-e57a28000044" />


<img width="1896" height="959" alt="hw-img-5" src="https://github.com/user-attachments/assets/0d28588d-4747-4a75-bb63-2ef137bf331d" />

