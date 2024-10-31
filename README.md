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
     nano logs.log 

     Часть 2: Пользователи и права доступа
     
    1.Создать группы: workers; teachers; students; вывести из файла /etc/group только названия добавленных групп
    
    sudo groupadd students sudo groupadd teachers sudo groupadd workers

    2.Создать пользователей user_{1,2,3,4,5}; вывести из файла /etc/passwd только имена созданных пользователей
    
  sudo useradd user_1
  sudo useradd user_2
  sudo useradd user_3
  sudo useradd user_4
  sudo useradd user_4
  

  
    
    3.Пользователей user_1 и user_2 добавить в группу workers

    sudo usermod -a -G workers user_1
    sudo usermod -a -G workers user_2

    4.Пользователей user_3, user_4, user_5 добавить в группу students
    
 sudo usermod -a -G students user_3
 sudo usermod -a -G students user_4
    
    5. Создать пользователя mentor3, задав ему при создании uid=3000, добавить в группу teachers
    
 sudo useradd -u 3000 mentor3
 sudo usermod -a -G teachers mentor3


    
    6.Вывести на экран состав групп workers; teachers; students?????
    
    
    7.Задать пароли для всех пользователей

     sudo passwd user_1   1234567
      sudo passwd user_2
       sudo passwd user_3
        sudo passwd user_4
         sudo passwd user_5
         sudo passwd mentor3

     
    8.С помощью grep найти записи о новых группах и пользователях в файлах /etc/passwd и /etc/group


    
    9.Создать директорию user в домашней директории. В ней создать каталоги library и tests.
    
     mkdir user
     mkdir library 
     pmn@pmn-ubuntu:~/user$ mkdir tests

    
    10.Создать файлы book_фамилия_{1,2,3,4,5} и поместить их в library
    
    pmn@pmn-ubuntu:~/user/library$ for i in {1..5}; do touch book_фамилия_$i; done

    
    11. Создать текстовый файл test_permissions, и поместить в tests; добавить в него следующий текст
    #!/bin/bash
    echo "Hello World"

    nano test_permissions
    sudo chmod +x test_permissions

    12. Сделать файл test_permissions исполняемым для группы students
    
    chown pmn:students test_permissions 
    sudo chmod g+x test_permissions
    


    



