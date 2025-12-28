Домашнее задание к занятию «Disaster Recovery. FHRP и Keepalived»

Задание 1
Дана схема для Cisco Packet Tracer, рассматриваемая в лекции.
На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

Решение 1
[схема](https://github.com/AnkouDW/sys-pattern-homework-gitlab-hw/blob/b48f9ad2f73415c24719084d303745574bc22cf9/hsrp_advanced.pkt)

<img width="603" height="524" alt="1_1" src="https://github.com/user-attachments/assets/e472cb52-00b3-4d2c-a6e7-0421f0734edf" />
<img width="576" height="524" alt="1_2" src="https://github.com/user-attachments/assets/12801d12-633e-496f-b698-495e5666e07a" />

Задание 2
Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного файла.
Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html

Решение 2
Файл bash скрипта

https://github.com/AnkouDW/sys-pattern-homework-gitlab-hw/blob/5dff8f8f5807c47662d214441a315ef097d5fbcf/port-page-check.sh

Файл keepalived.conf

https://github.com/AnkouDW/sys-pattern-homework-gitlab-hw/blob/5dff8f8f5807c47662d214441a315ef097d5fbcf/keepalived.conf

Скриншоты с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html:

<img width="769" height="521" alt="2_1" src="https://github.com/user-attachments/assets/13ffde54-8347-4eda-85bb-71f73c54aa65" />

<img width="766" height="534" alt="2_2" src="https://github.com/user-attachments/assets/6d0285c6-027d-40fc-8755-ef2dc7283773" />



