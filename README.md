    1. Вывести список имен пользователей из файла /etc/passwd

  awk -F : ' {print $1}' /etc/passwd

    
    2. В домашней директории создать каталог text_processing
    
  mkdir text_processing 
    
    3. В директории text_processing создать файл syslog с содержимым
    touch syslog
    nano syslog 
