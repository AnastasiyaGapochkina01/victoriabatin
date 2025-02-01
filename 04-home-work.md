1) Выполнить команду ```sleep 10000 &```
2) Найти процесс sleep, какой у него id?
3) Вывести pid, ppid, stat, comm для процесса sleep
4) Убить процесс sleep
5) В домашней директории создать директорию scripts. В директории scripts создать файл date-logging.sh с содержимым
```
#!/bin/bash

worker() {
  LOGFILE="worker_out.log"

  while true; do
    echo "$(date '+%Y-%m-%d %H:%M:%S') - Запись времени" >> "$LOGFILE"
    echo "Записано время в $LOGFILE"

    sleep 30
  done
}
worker &
WORKER_PID=$!

while true; do
  echo "Worker is $WORKER_PID"
  sleep 5
done
```
6) Сделать файл date-logging.sh исполняемым для всех
7) Выполнить команду ```./date-logging.sh > /dev/null &```
8) Проверить, появился ли в директории scripts файл worker_out.log
9) Вывести worker_out.log на экран
10) Найти все процессы date-logging.sh
11) Запустить htop и найти в нем процессы date-logging
12) Вывести на экран только id и пользователя от которого запущены процессы date-logging
13) Вывести pid, comm и stat для процессов date-logging
14) Приостановить один из процессов date-logging и проверить как изменился статус
15) Возобновить процесс date-logging и проверить как изменился статус
16) Убить процессы date-logging
17) В директории scripts создать файл web_server с содержимым
```
#!/bin/bash
LOG_FILE="web_server.log"
log_levels=("ERROR" "INFO" "WARNING" "DEBUG")
methods=("GET" "POST" "PUT" "PATCH" "OPTIONS" "DELETE")
echo "Starting web-server on $(hostname)" >> $LOG_FILE
while true
do
  sleep 5
  random_method=${methods[$RANDOM % ${#methods[@]}]}
  random_level=${log_levels[$RANDOM % ${#log_levels[@]}]}
  echo "$(date +"%Y-%d-%m [%H:%M:%S]") $random_level $random_method" >> $LOG_FILE
  sleep 5
done
```
18) Сделать файл web_server исполняемым для всех
19) Выполнить команду ```./web_server &> /dev/null &```
20) Найти id процесса web_server
21) В директории scripts найти файл web_server.log и посмотреть его содержимое
22) В директории /proc найти каталог, который соответствует найденному выше процессу web_server
23) Запустить top и найти в нем процесс web_server. Сколько CPU и MEM он потребляет?
24) Убить процесс web_server
