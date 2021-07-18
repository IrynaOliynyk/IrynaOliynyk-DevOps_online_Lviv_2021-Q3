# EPAM University ProgramsDevOpsexternal course

Module 3

Database Administration

TASK 3.1

## PART 1

1.Download MySQL server for your OS on VM. (https://dev.mysql.com/downloads/)

2.Install MySQL server on VM.

![image](https://user-images.githubusercontent.com/58170246/126062118-48eabd2b-6b58-41fe-9ee7-16df793a0627.png)

-перейдем в рут пользователя
#su 

![image](https://user-images.githubusercontent.com/58170246/126062145-e552e46a-3688-403f-82ff-939180e175c4.png)

#apt-get update (обновляем данные репозитория, чтоб в  обновленном  производить поиск базы данных)



sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
sudo rm /var/lib/dpkg/lock-frontend

sudo dpkg --configure -a



![image](https://user-images.githubusercontent.com/58170246/126062194-32cde8bf-41ee-451c-8b08-4f8cd75061a5.png)

теперь ищим программы mysql

#apt-cache search mysql

![image](https://user-images.githubusercontent.com/58170246/126062425-780300e4-8a50-4657-a3cc-2fad7abd50b2.png)

![image](https://user-images.githubusercontent.com/58170246/126062463-369de0e0-abc5-40d7-bb01-438b4f5c63f3.png)

![image](https://user-images.githubusercontent.com/58170246/126062475-2df94095-ccd0-4114-bf05-a3766a031c90.png)

#apt-cache search mysql | grep 'server\|client'

![image](https://user-images.githubusercontent.com/58170246/126062706-60086ba9-bafb-4c7e-99be-92fcad1be61e.png)

![image](https://user-images.githubusercontent.com/58170246/126062749-935fe30a-f2d6-48bf-930a-91f720cb787d.png)

![image](https://user-images.githubusercontent.com/58170246/126062819-a5620001-683e-4e4c-bca5-c3de66ef4ef3.png)

![image](https://user-images.githubusercontent.com/58170246/126062831-93647c85-2940-41e6-b245-68852ec07cf1.png)

устанавливаем сервер и клиент. Клиент разрешает подсоеденится  к серверу.

#apt-get install mysql-client-5.7 mysql-server-5.7 

![image](https://user-images.githubusercontent.com/58170246/126063067-4737bd98-014b-4ec2-bbbd-3a14d46e11c6.png)

#systemctl status mysql

![image](https://user-images.githubusercontent.com/58170246/126063537-2c11234d-4169-40c5-8da4-500944afa701.png)

подсоединяемся в серверу mysql

#mysql -uroot -p

![image](https://user-images.githubusercontent.com/58170246/126063700-7138ef3b-caf6-4423-b8ec-44b1f87bfac2.png)

![image](https://user-images.githubusercontent.com/58170246/126078403-885347ce-002b-4013-82c7-b9bb5309f03b.png)

скрипт с помощью языка запросов ; определяет конец команды!!


для CentOS

#yum search mysql

![image](https://user-images.githubusercontent.com/58170246/126078532-952742ed-3000-46a6-9c75-7220f5223b22.png)

програм sql server в вписке CentOS не представлено, но представлено mariadb 

![image](https://user-images.githubusercontent.com/58170246/126078565-b54c2d96-4d90-4c22-a0b7-76b2573f80ac.png)

![image](https://user-images.githubusercontent.com/58170246/126061930-b5b05cfa-b7c7-45d1-8dfa-946d46813e41.png)

mariadb замена mysql

найдем саму програму сервера mariadb 

#yum search mariadb-server ![image](https://user-images.githubusercontent.com/58170246/126078650-86216c2f-89c5-4fc4-b6d7-9087393e2a3c.png)

#yum instal mariadb-server ![image](https://user-images.githubusercontent.com/58170246/126078662-91e9c0f4-bd15-4560-b9a8-a6c70188efcd.png)

#systemctl status mariadb ![image](https://user-images.githubusercontent.com/58170246/126078700-1c14a0cd-6df1-4123-9f0d-042d8ea33712.png)
 
сервис загружен но не активен ![image](https://user-images.githubusercontent.com/58170246/126078712-4549efb0-d9c1-4a04-8f05-6f8a79ab22dc.png)

и не настроен на запуск при загрузке системы.

#systemctl enable mariadb ![image](https://user-images.githubusercontent.com/58170246/126078797-b95a3000-e9b1-45d3-9e2d-1e343cbaa5fd.png)

#systemctl start mariadb ![image](https://user-images.githubusercontent.com/58170246/126078819-cacd7ca2-0768-40c7-beb5-d6942f488f7b.png)

#systemctl status mariadb  ![image](https://user-images.githubusercontent.com/58170246/126078856-9212979b-428a-4e7f-8f5f-4624c1da2e23.png)

установим пароль для root пользователя

#mysqladmin -u root password "123"

![image](https://user-images.githubusercontent.com/58170246/126078924-6dbf6cc6-f6e5-43e4-8c74-9a1e8023c852.png)

#mysql uroot -p
![image](https://user-images.githubusercontent.com/58170246/126078963-08370ffb-3e2a-4de1-97e3-dea710450202.png)

![image](https://user-images.githubusercontent.com/58170246/126079003-08978f0d-fa56-47d3-8e3b-88878f13655c.png)

![image](https://user-images.githubusercontent.com/58170246/126079029-61b7d11c-444f-4d8c-b492-832171c4e4a7.png)

![image](https://user-images.githubusercontent.com/58170246/126079038-e02b53d1-65da-44b6-b5b0-b1915fe428dc.png)

![image](https://user-images.githubusercontent.com/58170246/126079068-aa3b8eff-7497-4e10-b1af-b7571b605a1b.png)

![image](https://user-images.githubusercontent.com/58170246/126079127-bd2fedcd-1eda-4485-9075-e6d91c570b08.png)











3.Select a subject area anddescribe the database schema, (minimum 3 tables)

4.Create a database on the server through the console.

5.Fill in tables.

6.Constructand execute SELECT operator with WHERE,GROUP BYand ORDER BY.

7.Execute other different SQL queries DDL, DML, DCL.

8.Create a database of new users with different privileges. Connect to the database as a new user and verify that the privilegesallow or deny 
certain actions.

9.Make a selection from the main table DB MySQL.

## PART 2

10.Make backup of your database.

11.Delete the table and/or part of the data in the table.

12.Restore your database.

13.Transfer your local database to RDS AWS.

14.Connect to your database.

15.Execute SELECToperatorsimilarstep6.

16.Create thedumpof yourdatabase.

## PART 3

17.Create an Amazon DynamoDB table

18.Enter data into an Amazon DynamoDB table.

19.Query an Amazon DynamoDB tableusing QueryandScan.


