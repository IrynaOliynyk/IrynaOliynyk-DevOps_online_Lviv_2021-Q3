TASK 5.3 

Part1

1. How many states could has a process in Linux?


Процес - це:

1) програма на стадії виконання

2) "об'єкт", яким виділено процесорний час

3) асинхронна робота

У Linux існують два основних типи процесів:

• Процеси переднього плану (Foreground) - ці процеси не започатковано і контролюються на протязі кінцевої сесії. Іншими словами, повинен бути користувач, підключений до системи для запуску таких процесів; вони не запускалися автоматично як частина функцій / служб системи.

• Фонові процеси (Background) (також належні до неінтерактивному / автоматичним процесам) - це процеси, не пов'язані з терміналом; вони не очікують від користувача введення.

На скріншоті нижче зображена модель п'яти станів

![image](https://user-images.githubusercontent.com/58170246/133625011-48651e0a-f061-4ede-8099-38053d06de84.png)


2. Examine the pstree command. Make output (highlight) the chain (ancestors) of the current process.

У простій формі, коли викликається ```pstree``` без будь-якої опції або аргументу, вона відображає ієрархічну деревоподібну структуру всіх запущених процесів:

![image](https://user-images.githubusercontent.com/58170246/133625496-650bd6f0-462f-4b06-b1ae-9530a5fde48a.png)


3. What is a proc file system?


Linux надає ядру і модулям ядра додатковий механізм передачі інформації зацікавленим в ній процесам - це файлова система /proc. Спочатку вона створювалася з метою отримання відомостей про процеси (звідси така назва). Тепер вона інтенсивно використовується і самим ядром, якому є що повідомити!

Наприклад, /proc/modules - список завантажених модулів, /proc/meminfo - статистика використання пам'яті.

Методика роботи з файловою системою / proc дуже схожа на роботу драйверів з файлами пристроїв: ви створюєте структуру з усією необхідною інформацією, включаючи покажчики на функції-обробники (в нашому випадку є тільки один обробник, який обслуговує читання файлу в / proc).

Файлова система / proc була написана, головним чином, для того щоб отримувати дані від ядра, вона не передбачає спеціальних засобів для запису даних в файли. Файлова система / proc, всякий раз, коли ми реєструємо новий файл, дозволяє вказати - яка struct inode_operations буде використовуватися для доступу до нього. У свою чергу, в цій структурі є покажчик struct file_operations, а в ній вже знаходяться покажчики на наші функції-обробники.

Наша файлова система показана на скрині нижче.


![image](https://user-images.githubusercontent.com/58170246/133625973-020822dd-a011-4307-a7ed-51b11b3f94b9.png)

https://losst.ru/fajlovaya-sistema-proc-v-linux

4. Print information about the processor (its type, supported technologies, etc.).

```cat /proc/cpuinfo```


![image](https://user-images.githubusercontent.com/58170246/133626280-8d1781f3-ee3b-4849-8c4a-c0e920c5342f.png)

5. Use the ps command to get information about the process. The information should be as follows: the owner of the process, the arguments with which the process was launched for execution, the group owner of this process, etc. 

Команда ps за замовчуванням є у всіх дистрибутивах Linux. Без будь-яких аргументів і опцій ps показує запущені процеси, що виконуються користувачем у вікні терміналу:

![image](https://user-images.githubusercontent.com/58170246/133626566-d2ae3786-b6c9-4fe8-8e6f-770ca5923558.png)


На виході будуть відображатися рядка даних, що містять наступну інформацію: * PID - це унікальний ідентифікатор процесу;

TTY - тип терміналу;

TIME - це загальний час використання процесорного часу процесом (00:00:00 навпаки процесу bash вказує, що процесорний час взагалі не було використано до сих пір);

CMD - це ім'я команди, яка запустила цей процес.

Щоб отримати повний список, виконаємо наступну команду:
ps -ef

Опція -e, показує всі процеси, а -f показує повну інформацію:

UID - ідентифікатор користувача виконує команду;

PID - це ідентифікатор процесу команди;

PPID - ідентифікатор батьківського процесу, який відпустив команду;

C - кількість дочірніх процесів;

STIME - це час початку процесу;

TTY;

TIME;

CMD.

![image](https://user-images.githubusercontent.com/58170246/133626758-c034117b-a934-400b-b341-82de6466f177.png)



6. How to define kernel processes and user processes?

7. Print the list of processes to the terminal. Briefly describe the statuses of the processes. What condition are they in, or can they be arriving in?

8. Display only the processes of a specific user. 

9. What utilities can be used to analyze existing running tasks (by analyzing the help for the ps command)?

10. What information does top command display?

12. Display the processes of the specific user using the top command.

12. What interactive commands can be used to control the top command? Give a couple of examples.

13. Sort the contents of the processes window using various parameters (for example, the amount of processor time taken up, etc.)

14. Concept of priority, what commands are used to set priority?

15. Can I change the priority of a process using the top command? If so, how?

16. Examine the kill command. How to send with the kill commandprocess control signal? Give an example of commonly used signals.

17. Commands jobs, fg, bg, nohup. What are they for? Use the sleep, yes command to demonstrate the process control mechanism with fg, bg.

Part2

1. Check the implementability of the most frequently used OPENSSH commands in the MS Windows operating system. (Description of the expected result of the commands + screenshots: command – result should be presented)

2. Implement basic SSH settings to increase the security of the client-server connection (at least 

3. List the options for choosing keys for encryption in SSH. Implement 3 of them.

4. Implement port forwarding for the SSH client from the host machine to the guest Linux virtual machine behind NAT.

5*. Intercept (capture) traffic (tcpdump, wireshark) while authorizing the remote client on the server using ssh, telnet, rlogin. Analyze the result. 
