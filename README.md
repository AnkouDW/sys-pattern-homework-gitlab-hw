Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки»

Задание 1
Запустите два simple python сервера на своей виртуальной машине на разных портах
Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
Настройте балансировку Round-robin на 4 уровне.
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

Решение 1
<img width="676" height="212" alt="Screenshot_1" src="https://github.com/user-attachments/assets/8e59610d-dbfc-4dee-8dc1-c0a7dac992ca" />
<img width="653" height="227" alt="Screenshot_2" src="https://github.com/user-attachments/assets/9a4fcb5e-1167-4181-93d0-a0e2e0ac70cd" />
<img width="660" height="202" alt="Screenshot_3" src="https://github.com/user-attachments/assets/d7338e51-9edb-4a35-8de1-39e8ebb7e749" />
<img width="1919" height="605" alt="Screenshot_4" src="https://github.com/user-attachments/assets/6e99dc86-51a7-4107-a181-d77a6158852b" />
https://github.com/AnkouDW/sys-pattern-homework-gitlab-hw/blob/3d8daf4e41abb76dde143b451685ed8a0f1bb89a/haproxy.cfg


Задание 2
Запустите три simple python сервера на своей виртуальной машине на разных портах
Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

Решение 2
https://github.com/AnkouDW/sys-pattern-homework-gitlab-hw/blob/a50b469305a3676122f93a5aa462b42446cbd03b/haproxy_2.cfg
<img width="676" height="212" alt="Screenshot_1" src="https://github.com/user-attachments/assets/f67b839a-35f7-4513-a888-ddc3ac2c7153" />
<img width="653" height="227" alt="Screenshot_2" src="https://github.com/user-attachments/assets/ea6c87ca-9c54-4bdb-9b15-610f189a0bfe" />
<img width="712" height="92" alt="Screenshot_5" src="https://github.com/user-attachments/assets/a9ace908-441c-45dc-bad9-098793ab066f" />
<img width="914" height="365" alt="Screenshot_6" src="https://github.com/user-attachments/assets/7dbd649f-d550-4172-a9dc-b8d65a650e27" />
<img width="1919" height="518" alt="Screenshot_7" src="https://github.com/user-attachments/assets/0e3cf2cf-06f5-428c-ac9f-f2b5df7b6228" />






