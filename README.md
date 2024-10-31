Часть 1: Работа с текстом
    1. Вывести список имен пользователей из файла /etc/passwd

  awk -F : ' {print $1}' /etc/passwd

    
    2. В домашней директории создать каталог text_processing
    
  mkdir text_processing 
    
    3. В директории text_processing создать файл syslog с содержимым
    touch syslog
    nano syslog 

    
    4.В файле syslog найти все записи, которые содержат application
    5. В файле syslog найти записи о запусках cron на сервере server3 и вывести команду, которая запускалась (это то, что в скобках в конце)
    6. В файле syslog найти все записи, содержащие ssh и вывести для них название сервера
    7. В файле syslog найти все записи, содержащие "Failed password" и вывести только ip
    8. В файле syslog найти записи, содержащие "Accepted password" и вывести имя пользователя и ip
    9. В директории text_proxessing создать файл logs.log с содержимым

     touch logs.log
     pmn@pmn-ubuntu:~/text_processing$ nano logs.log 

     Часть 2: Пользователи и права доступа


