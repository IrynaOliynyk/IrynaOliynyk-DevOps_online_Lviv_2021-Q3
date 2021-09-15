Task1.Part1

1)  Log in to the system as root. 

```sudo -i```

![image](https://user-images.githubusercontent.com/58170246/129597844-bb3be019-1b75-43fc-9834-ac4bb4a1ea6f.png)


2) Use the ```passwd``` command to change the password. Examine the basic parameters of the command. What system file does it change *?


The ```passwd``` program changes the passwords of user accounts. Regular user can only change the password for his own account, the superuser can change the password any account. ```passwd``` also changes account information, or password expiration date.


Введемо ```passwd``` и введемо новий пароль (asdzse30)


![image](https://user-images.githubusercontent.com/58170246/133388776-7e1eae5b-95d7-4b17-8652-52ef54c1fe92.png)



ПАРАМЕТРИ команди passwd:

```-a, --all``` Цей параметр можна використовувати тільки разом з -S для виведення статусу всіх користувачів.

```-d, --delete``` Видалити пароль користувача.

```-e, --expire``` Негайно зробити пароль застарілим. В результаті це змусить користувача змінити пароль при наступному вході в систему.

```-h, --help``` Показати коротку довідку і закінчити роботу.

```-i, --inactive``` DAY Цей параметр використовується для блокування облікового запису після заданого числа днів після старіння пароля. Тобто, якщо пароль застарів і пройшло більше зазначених ДНІВ, то користувач більше не зможе використовувати дану обліковий запис.

```-k, --keep-tokens``` Зміна пароля слід виконувати тільки для прострочених токенов аутентифікації (паролів).

```-l, --lock``` Заблокувати зазначену обліковий запис. Цей параметр блокує обліковий запис змінюючи значення пароля на варіант, який не може бути шифрованих паролем. 

```-m, --mindays``` МІН_ДНІВ Задати мінімальну кількість днів між зміною пароля. Нульове значення цього поля вказує на те, що користувач може змінювати свій пароль коли захоче.

```-q, --quiet``` Чи не виводити повідомлень при роботі.

```-r, --repository``` репозиторій


Змінити пароль репозиторію.

``-S, --status`` Показати стан облікового запису. Інформація про стан містить 7 полів. Перше поле містить ім'я облікового запису. Друге поле вказує, заблокована обліковий запис (L), вона без пароля (NP) або у неї є робочий пароль (P). Третє поле зберігає дату останньої зміни пароля. У наступних чотирьох полях зберігаються мінімальний термін, максимальний термін, період видачі попередження і період неактивності пароля. Ці терміни вимірюються в днях.

``-u, --unlock`` Розблокувати зазначену обліковий запис. Цей параметр активує обліковий запис змінюючи пароль на колишнє значення (яке було перед використанням параметра -l).

``-w, --warndays`` ПРЕД_ДНЕЙ Встановити число днів видачі попередження, перед тим як буде потрібно зміна пароля. У параметрі ПРЕД_ДНЕЙ вказується число днів перед тим як пароль застаріє, в перебігу яких користувачеві будуть нагадувати, що пароль скоро застаріє.

``-x, --maxdays МАКС_ДНІВ`` Встановити максимальну кількість днів, протягом яких пароль залишається робочим. Після МАКС_ДНЕЙ пароль потрібно змінити


3)  Determine the users registered in the system, as well as what commands they execute. What additional information can be gleaned from the command execution?


```passwd (etc / passwd)``` - містить інформацію про користувачів, мають такий вигляд запису - "user_name: password: UID: GID: full_name: home_directory: login_shell". Елементи запису повинні розділятися символом - ":" (двокрапка) і записуються без пробілів. Якщо пароль зберігається в зашифрованому вигляді у файлі / etc / shadow, то замість пароля вказується - "x".

список користувачів ```cat /etc/passwd```

![image](https://user-images.githubusercontent.com/58170246/133389363-d20e64de-0844-44e6-a598-f9eedd9eeca3.png)



4) Change personal information about yourself.


Подивимося інформацію про користувача: ```finger -l```

![image](https://user-images.githubusercontent.com/58170246/133389728-0c445589-c2b2-435e-aa74-d5c40e4486dd.png)
 
 бачимо що вона не інстальована
  
  інсталюємо її
  
  ```apt instal finger```
  
  ![image](https://user-images.githubusercontent.com/58170246/133390052-7c61f539-5d0c-4b76-80c1-5a740e4e187d.png)
  
  
  введемо знову ```finger -l```
  
  
  ![image](https://user-images.githubusercontent.com/58170246/133390186-ea361ed6-cc4c-4462-a029-d622522c2b39.png)


 

```chfn```

![image](https://user-images.githubusercontent.com/58170246/133412122-fc69f113-49eb-4d5a-a833-57fb9a1995d2.png)


Додамо інформацію про користувача:

Повне ім'я: !!!

Номер кімнати:!!!

Номер телефону: !!!

Інша: Student of the Epam !!!




Подивимося результати:


```less / etc / passwd```

![image](https://user-images.githubusercontent.com/58170246/133412369-0365474c-d4ba-4f53-8547-a30af787ba75.png)




5) Become familiar with the Linux help system and the man and info commands. Get help on the previously discussed commands, define and describe any two keys for these commands. Give examples.

Команда man виводить сторінку керівництва для зазначеного імені на стандартний висновок.
```$ man [назва команди]```

Кожна сторінка керівництва має стандартну форму з наступними розділами:


```NAME``` - назва і призначення

```SYNOPSIS``` - синтаксис

```DESCRIPTIONS``` - опис

```FILE``` - використовувані файли

```SEE ALSO``` - суміжні розділи

```DIAGNOSTIC``` - діагностика помилок

```BUGS``` - помічені помилки


Переглянемо інформацію про команду   ```passwd```
```man passwd```

![image](https://user-images.githubusercontent.com/58170246/133412592-3249a9c7-6c49-4eb8-a508-4117fd0f7a2a.png)


Для отримання інформації по окремій команді треба задати в командному рядку ```info``` з параметром, що є ім'ям, що цікавить нас команди, наприклад,

```$ info man```

![image](https://user-images.githubusercontent.com/58170246/133412731-92e39f19-f9a1-472e-ada2-7d2677c42761.png)


Істотна відмінність від команди man полягає в тому, що видається info інформація представлена в гіпертекстовому форматі. В силу цього ви отримуєте можливість переглядати різні розділи допомоги, не виходячи з оболонки, що надається командою ```info```.


6) Explore the more and less commands using the help system. View the contents of files .bash* using commands.

Команда ```more``` стара і основна термінальна команда, яка використовується при відкритті файлу для інтерактивного читання. Якщо вміст файлу занадто велике, щоб поміщатися на одному екрані, воно відображає вміст сторінки за сторінкою. Ви можете прокручувати вміст файлу, натискаючи клавіші ENTER або SPACE. Але одне обмеження - ви можете прокручувати тільки вперед, а не назад. Це означає, що ви можете прокручувати вниз, але не можете піднятися.

Відкриємо за допомогою цієї команди файл EpamTask.txt

![image](https://user-images.githubusercontent.com/58170246/133412839-47c3a647-cb78-4b9e-aa11-e8a7e14a552c.png)

7) * Describe in plans that you are working on laboratory work 1. Tip: You should read the documentation for the finger command.

```$echo "I am working on Lab 1" > ~/.plan```


![image](https://user-images.githubusercontent.com/58170246/133414870-306134d1-c2c3-489d-a342-9ef96b9ad0ba.png)



![image](https://user-images.githubusercontent.com/58170246/133414676-da065662-da60-45c1-af94-eec8fb49b5d7.png)




8) * List the contents of the home directory using the ls command, define its files and directories. Hint: Use the help system to familiarize yourself with the ls command.

Структура команди:

$ ls опції/шлях/до/папки

Основні опції утиліти:


-a - відображати всі файли, включаючи приховані, це ті, перед ім'ям яких стоїть крапка;

-A - не відображати посилання на поточну папку і кореневу папку. і ..;

--author - виводити творця файлу в режимі докладного списку;

-b - виводити Escape послідовності замість недрукованих символів;

--block-size - виводити розмір каталогу або файлу в певній одиниці виміру, наприклад, мегабайтах, гігабайтах або кілобайтах;

-B - не виводити резервні копії, їх імена починаються з ~;

-c - сортувати файли за часом модифікації або створення, спочатку будуть виведені нові файли;

-C - виводити колонками;

--color - включити кольоровий режим виведення, автоматично активована в багатьох дистрибутивах;

-d - виводити тільки директорії, без їх вмісту, корисно при рекурсивном виведення;

-D - використовувати режим виведення, сумісний з Emacs;

-f - НЕ сортувати;

-F - показувати тип об'єкта, до кожного об'єкта буде додано один із спеціалізованих символів * / => @ |;

--full-time - показувати детальну інформацію, плюс вся інформація про час в форматі ISO;

-g - показувати детальну інформацію, але крім власника файлу;

--group-directories-first - спочатку відображати директорії, а вже потім файли;

-G - не виводити імена груп;

-h - виводити розміри папок в зручному для читання форматі;

-H - відкривати символічні посилання при рекурсивном використанні;

--hide - не відображати файли, які починаються з вказаного символу;

-i - відображати номер індексу inode, в якій зберігається цей файл;

-l - виводити докладний список, в якому буде відображатися власник, група, дата створення, розмір та інші параметри;

-L - для символічних посилань відображати інформацію про фото, на який вони посилаються;

-m - розділяти елементи списку коми;

-n - виводити UID і GID замість імені і групи користувача;

-N - виводити імена як є, не обробляти контролюючі послідовності;

-Q - брати імена папок і файлів в лапки;

-r - зворотний порядок сортування;

-R - рекурсивно відображати вміст піддиректорій;

-s - виводити розмір файлу в блоках;

-S - сортувати за розміром, спочатку великі;

-t - сортувати за часом останньої модифікації;

-u - сортувати за часом останнього доступу;

-U - НЕ сортувати;

-X - сортувати за алфавітом;

-Z - відображати інформацію про розширення SELinux;

-1 - відображати один файл на один рядок.


Подивимося вміст домашнього каталогу:

``$ ls -l``


![image](https://user-images.githubusercontent.com/58170246/133415412-8121d35c-4992-42ea-909a-b43876ff292f.png)

![image](https://user-images.githubusercontent.com/58170246/133416043-dc582c60-05d5-414b-8f8d-59331164b948.png)



А тепер подивимося і з прихованими файлами:

``$ ls -а``

 ![image](https://user-images.githubusercontent.com/58170246/133415488-e25dbaf0-1540-436f-815d-3e4c03079925.png)
 
 ![image](https://user-images.githubusercontent.com/58170246/133415991-7a2a5590-7701-400e-ad6b-1f9ae8dd5b5c.png)


Task5.1.

Part2

1)Examine the tree command. Master the technique of applying a template, for example, display all files that contain a character c, or files that contain a specific sequence of characters. List subdirectories of the root directory up to and including the second nesting level. 

2)What command can be used to determine the type of file (for example, text or binary)? Give an example.

3) Master the skills of navigating the file system using relative and absolute paths. How can you go back to your home directory from anywhere in the filesystem?

4) Become familiar with the various options for the ls    command. Give examples of listing directories using different keys. Explain the information displayed on the terminal using the -l and -a switches.

5) Perform the following sequence of operations: -  create a subdirectory in the home directory;-  in this subdirectory create a file containing information about directories located in the root directory (using I/O redirection operations);-  view the created file;-  copy the created file to your home directory using relative and absolute addressing.-  delete the previously created subdirectory with the file requesting removal;-  delete the file copied to the home directory.

6)Perform the following sequence of operations:

-  create a subdirectory testin the home directory;

-  copy the .bash_historyfile to this directory while changing its name to labwork2;

-  create a hard and soft link to the labwork2file in the test subdirectory; 

-  how to define soft and hard link, what do theseconcepts;

-  change the data by opening a symbolic link. What changes will happen and why -  rename the hard link file to hard_lnk_labwork2;

-  rename the soft link file to symb_lnk_labwork2 file;

-  then delete the labwork2. What changes have occurred and why?

7) Using the locate utility, find all files that contain the squid and traceroute sequence.

8) Determine which partitions are mounted in the system, as well as the types of these partitions.

9) Count the number of lines containing a given sequence of characters in a given file.

10) Using the findcommand, find all files in the /etc directory containing the host character sequence.

11) List all objects in /etc that contain the ss character sequence. How can I duplicate a similar command using a bunch of grep? 

12) Organize a screen-by-screen print of the contents of the /etc directory. Hint: You must use stream redirection operations.

13) What are the types of devices and how to determine the type of device? Give examples.

14) How to determine the type of file in the system, what types of files are there?

15)* List the first 5 directory files that were recently accessed in the /etcdirectory. 
