# Bash
## Теория
1) [Долгий урок почти по всему синтаксису bash](https://youtu.be/kEpCiCb-y1Y)
2) Еще по синтаксису
- [часть 1](https://youtu.be/qW6VcH-nSRo)
- [часть 2](https://youtu.be/yOfx8LPCGh4)
3) Практические примеры
- [посложенее](https://youtu.be/qMFb7Nj_WA4)
- [попроще](https://youtu.be/4myfKzBl_jc)

## Практика
1) Написать скрипт, который будет проверять состояние указанных служб и перезапускать их, если они остановлены.
2) Написать скрипт для поиска свободных портов из диапазона 12450-12462
3) Написать скрипт для сбора статистики о процессах:
– об использовании cpu
– об использовании памяти
– выводить парамтеры pid, user, command и cpu/mem
– результат должен записываться в файл /var/log/process_stat.log
4) Написать скрипт для автоматической установки nginx+php-fpm+percona. Скрипт должен проверять, установилось ли ПО запросом версии (или любым другим способом) и выводить отчет об установленных версиях в файл output.txt
5) Написать скрипт, который будет получать сколько процентов диска использовано (команда df) и делать запись в файл /var/log/disk_space.log, если это число превысило 80
6) Написать скрипт, который автоматизирует создание пользователя:
– имя пользователя передается скрипту как аргумент
– при создании пользователя обязательно создать ему домашнюю директорию и установить интерпретатор /bin/bash
– сгенерировать пароль и установить его пользователю
– сделать уведомление пользователя в TG о создании ему учетной записи с данными для подключения (адрес хоста, username и пароль)
7) Написать скрипт для резервного копирования приложения (файлы и база данных). Приложение можно взять готовое с github
8) Написать скрипт, который будет проверять работоспособность web-сервера
9) Написать скрипт для создания структуры нового проекта
– создать директорию самого проекта (должна передаваться как аргумент скрипту)
– в директории проекта создать директории
– src/: исходный код
– docs/: документация
– tests/: тесты
– resources/: ресурсы проекта
– создать файл readme.md с описанием проекта
– вывести созданную структуру на экран
10) Написать скрипт, который будет подсчитывать количество ошибок аутентификации в файле auth.log и отправлять об этом сообщение в TG администратору
