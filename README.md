# otus_16
# Резервное копирование

Домашнее задание
Настроить стенд Vagrant с двумя виртуальными машинами server и client.
Настроить политику бэкапа директории /etc с клиента:
1) Полный бэкап - раз в день
2) Инкрементальный - каждые 10 минут
3) Дифференциальный - каждые 30 минут

Запустить систему на два часа. Для сдачи ДЗ приложить list jobs, list files jobid=<id>
и сами конфиги bacula-*
_____________________________________________________________________________________________________________________
Больше всего помогло это
https://www.bacula.org/5.0.x-manuals/en/console/console/Bacula_Console.html



Конфиги bacula-* расположены в данном репозитории.
Перед запуском - на vm server выполнить ```setenforce 0```.

Для управления bacula из консоли используется bconsole. Для запуска бэкапа в консоли vm server выполним следующие команды:
```
bconsole
label
<дать имя>
run
```
![Image alt](https://github.com/Edo1993/otus_16/raw/master/1.png)

Проверить состояние ```status```
![Image alt](https://github.com/Edo1993/otus_16/raw/master/2.png)

Итог
- Выполнить команду ```list jobs```

[list jobs](https://github.com/Edo1993/otus_16/blob/master/log/list%20jobs)
