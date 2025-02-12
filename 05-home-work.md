# Systemd
1) Теория
- [процесс загрузки Linux](https://www.youtube.com/watch?v=UeRg_PMeaWM)
- [теория про systemd](https://www.youtube.com/watch?v=Y1p5NqzaYXo)
- [работа с systemd](https://youtu.be/fmVI9Q2LavI)
2) Практика
- в директории /opt создать директорию server
- в директории /opt/server создать файл bash-server с содержимым
```
#!/bin/bash

PORT=8089
sudo apt install -y netcat-traditional

healthcheck() {
    echo "Healthcheck: Server is running" >> ./bash-server.health
}

while true; do
    { echo -ne "HTTP/1.1 200 OK\r\nContent-Length: $(echo -n "Hello from bash-server" | wc -c)\r\n\r\nHello from bash-server"; } | nc -l -p $PORT -q 1
    sleep 60  # Проверка состояния каждые 60 секунд
    healthcheck
done
```
- сделать файл bash-server исполняемым
- написать unut-file для запуска bash-server как службы systemd
