1) Создать пользователя service-robot
2) Создать группу services
3) В директории /opt создать директорию backups
4) В директории /opt/backups создать 
- директорию project1
- директорию project2
- файл all_projects
4) Сделать владельцем директории project1 пользователя service-robot, а группой владельцев группу services
5) Сделать владельцем директории project2 своего пользователя, а группой владельцев группу service-robot
6) Сделать владельцем и группой владельцев файла all_projects пользователя service-robot
7) Назначить на файл all_projects права так, чтобы владелец имел все права, группа могла только читать, а все остальные не имели никаких прав
8) Назначить на директорию project1 права так, чтобы у всех категорий пользователей были полные права на эту директорию
9) Назначить на директорию project2 права так, чтобы полные права были у владельца и группы, а у всех остальных - не было никаких
10) В директории /opt/backups создать файл secrets
11) Назначить на файл secrets права так, чтобы владелец мог только изменять файл, группа могла только читать, а все остальные - только выполнять файл
12) В директории /opt/backups создать файл run.sh
13) Назначить на файл run.sh права так, чтобы владелец имел на него полные права, группа могла читать и изменять, а все остальные не имели никаких прав
14) Сделать владельцем и группой владельцев файла run.sh пользователя service-robot
15) Сделать группой владельцев файла secrets группу services
16) Из файла /etc/passwd вывести строку, относящуюся к service-robot
17) Добавить пользователя service-robot в группу services
18) Из файла /etc/group вывести состав группы services
