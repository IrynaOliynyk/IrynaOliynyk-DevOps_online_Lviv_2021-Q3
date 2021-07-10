## TASK 2.2

1.Read the terms of Using the AWS Free Tierand the ability to control their own costs.

I stydied.

2.Register with AWS(first priority)or alternatively, you can register with AWS Educateif you are currently a student.

![image](https://user-images.githubusercontent.com/58170246/124953990-4e2aca80-e01e-11eb-8629-738596befcf1.png)

3.Find the hands-on tutorialsfor your AWS needs. Explore list of step-by-step tutorials for deferent category. Use, repeat and have fun))

4.Review the 10-minute exampleLaunch a Linux Virtual Machinewith Amazon Lightsail. Repeat, create your own VM in the AWS cloud and connect to it.

5.Launch anotherLinux Virtual MachinewithoutAmazon Lightsail.It is recommended to use the t2or t3.micro instance and the CentOS operating system.

6.Create a snapshot of your instance to keep as a backup.

7.Create and attach a Disk_D (EBS)to your instance to add more storage space.Create and save some file on Disk_D.

8.Launch the third instance from backup.

9.Detach Disk_D from the 2nd instance and attach disk_D to the new instance.

10.Launch and configure a WordPress instancewith Amazon Lightsaillink

11.Review the 10-minute exampleStore and Retrieve a File. Repeat, creating your own repository.

12.Review the 10-minute example Batch upload files to the cloudto Amazon S3 using the AWS CLI. Create a user AWS IAM, configure CLI AWS and upload any files to S3.

13.Review the 10-minute example.Explore the possibilities of creating your own domain and domain name for your site.

14.Review   the   10-minute exampleDeploy   Docker   Containers   on   Amazon   Elastic Container Service (Amazon ECS). Repeat, create a cluster, and run the online demo applicationor better otherapplicationwith custom settings.

15.Create a static website on Amazon S3, publicly available(link1or link2-using a custom domainregistered with Route 53).Post on the page your own photo, the name of the educational program(EPAM DevOps online Summer2021),thelist of AWS services with which the student worked within the educational program or earlierand the full list with links of completed labs (based on tutorialsor qwiklabs).Provide the link to the websitein your report.

My report
IAM (ACCESS AND IDENTIFICATION)

1.  IAM is a global service. Основная роль управление пользователями, групами, ролями политиками доступа, ключами , политиками паролей, мультифакторной аутентификацией. По умолчанию вновь созданый пользователь не имеет доступа к сервисам AWS. Изначально мы работаем под root, который имеет доступ ко всем сервисам AWS. И root назначает права на использование. 

![image](https://user-images.githubusercontent.com/58170246/124954267-91853900-e01e-11eb-8925-eb70af84f045.png)

1.1 добавить пользователя

![image](https://user-images.githubusercontent.com/58170246/124955640-df4e7100-e01f-11eb-93dc-7588be834275.png)

![image](https://user-images.githubusercontent.com/58170246/124955946-289ec080-e020-11eb-805c-75fac237e52c.png)

админ не имеет прав!! как вновь созданный пользователь.

![image](https://user-images.githubusercontent.com/58170246/124956213-6ef41f80-e020-11eb-9458-d3bd1e1d7485.png)

1.2 создание груп

![image](https://user-images.githubusercontent.com/58170246/124956714-ec1f9480-e020-11eb-94cf-a640f41e7533.png)

после создания группы ее пользователи не имеют никаких прав доступа.

1.3 Политика паролей.

![image](https://user-images.githubusercontent.com/58170246/124957224-85e74180-e021-11eb-81f7-ab0f79c14a67.png)

Изменение политики паролей затронет всех пользователей AWS. 

чтоб войти под именем пользователя 

![image](https://user-images.githubusercontent.com/58170246/124960286-d3b17900-e024-11eb-8d32-ca0768398070.png)

![image](https://user-images.githubusercontent.com/58170246/124960569-212de600-e025-11eb-873a-d83603201681.png)


2. IAM Policies

политика, документ который гарантирует 1 илинесколько правв доступа. Политика запрета, преобладают политику доступа. 

![image](https://user-images.githubusercontent.com/58170246/124962594-7c60d800-e027-11eb-9e3a-ce2ba1fc10b0.png)

* означает все

Можем создать собственную политику

![image](https://user-images.githubusercontent.com/58170246/124963078-0c9f1d00-e028-11eb-8f54-82d9f29b5fa9.png)

![image](https://user-images.githubusercontent.com/58170246/124963341-5ab42080-e028-11eb-8ff0-9bddc71dcab1.png)

![image](https://user-images.githubusercontent.com/58170246/124963411-715a7780-e028-11eb-9be6-0b72973b5963.png)

![image](https://user-images.githubusercontent.com/58170246/124963439-7cada300-e028-11eb-96df-0a2c236250ba.png)

Политики могут быть применины к пользователям и группам но не к сервисам!!


3. IAM users

![image](https://user-images.githubusercontent.com/58170246/124963806-ec239280-e028-11eb-87f0-3438dade5968.png)

добавим политику admin, разрешает доступ ко всем ресурсам AWS. Теперь может создавать и управлять другими пользователями. 

![image](https://user-images.githubusercontent.com/58170246/124964170-5e947280-e029-11eb-9587-a9377b56849f.png)

Создадим под админом рядового пользователя.

![image](https://user-images.githubusercontent.com/58170246/124964997-5426a880-e02a-11eb-97c3-847e96157e02.png)

![image](https://user-images.githubusercontent.com/58170246/124965249-905a0900-e02a-11eb-9914-79e786074db2.png)

Обладает политикой доступа к S3

4 - IAM groups

 создаем новую группу и добавим политику доступа.
 
 ![image](https://user-images.githubusercontent.com/58170246/124966219-b8963780-e02b-11eb-8f11-8c6b3097a774.png)

 создаем пользователей и добавляем в даную группу. Мы можем создавать сразу несколько пользователей. 
 
 ![image](https://user-images.githubusercontent.com/58170246/124966680-4114d800-e02c-11eb-8ada-972430509f3b.png)
 
 И сразу можем добавлять в одну  из групп.
 
![image](https://user-images.githubusercontent.com/58170246/124966868-73bed080-e02c-11eb-9381-ee7f98cfa468.png)

Оба добавлены и имеют полный доступ к сервису S3

![image](https://user-images.githubusercontent.com/58170246/124967102-b8e30280-e02c-11eb-8482-2a70794e1170.png)

добавим 1 пользователя в dev лишив политики доступа S3.

![image](https://user-images.githubusercontent.com/58170246/124967650-55a5a000-e02d-11eb-812f-06772f9466d8.png)


5 - IAM Roles

Роли необходимый элемент для работы с сервисом S3. Вместо политик к сервисам применяем роли. Инстанс обладает только одной примененной ролью.

![image](https://user-images.githubusercontent.com/58170246/125044202-69401d80-e0a4-11eb-8338-d164af488ea1.png)

создаем роль EC2, которая разрешит сервису EC2  получить доступ к корзине S3. Доступ к роле обеспечивается согласно политики, которая к даной роле применена. Политика полного доступа к S3, обеспечит EC2 полный доступ к ресурсам S3

![image](https://user-images.githubusercontent.com/58170246/125044932-2468b680-e0a5-11eb-80b8-90b69278c086.png)


![image](https://user-images.githubusercontent.com/58170246/125045177-5f6aea00-e0a5-11eb-83a3-948cb90711d0.png)

при создании инстанса роль применена

![image](https://user-images.githubusercontent.com/58170246/125045830-17989280-e0a6-11eb-9ced-6f0977b8cb48.png)


при выборе даной роли наш инстанс  получит полный доступ к S3. Доступно изменение ролипосле создания инстанса. 


6 - IAM STS (Security Token Servise) 

-временный  безопасный доступ доверенных пользователей к нашим  ресурсам.

-доступ предоставляется временно (от нескольких минут, до нескольких часов)

-STS API запрос включает в себя -токен дезопасности, идентификатор ключа безопасности,  секретный  члюч доступа.

при запросе API будут сгенерированы ключи 

7 - API Keys in IAM (програмный интерфейс приложения).

![image](https://user-images.githubusercontent.com/58170246/125048165-50d20200-e0a8-11eb-94b0-f0ba95411179.png)

на последнем  шаге можем получить секретный  ключь. Если мы его не сохраним,  то дельше  мы можем сгененрировать новый!!

![image](https://user-images.githubusercontent.com/58170246/125048511-b0c8a880-e0a8-11eb-99d9-dfed5213890e.png)

поэтому сохраняем в отдельной дериктории. 

Если он утрачен, то сперва деактивируем старый. Иактивируем новый. 

Хранить секретный ключ на инстансе не рекомендуется.


Без разрешений суперпользователя настройка акаунта запрещена.

Чтоб админу разрешить изменение в акаунте, через рут пользователя 

![image](https://user-images.githubusercontent.com/58170246/125049830-0fdaed00-e0aa-11eb-99de-6bcc3da34674.png)

СЕТЕВОЕ ВЗАИМОДЕЙСТВИЕ (виртуальное приватное облако)
1 Знакомство с VPC
VPC- расположено врамках выбраного региона AWS
Охватывает несколко зон доступности
возможность запуска инстансов в подсети
Только 5 VPC в регионе.
5 интернет шлюзов в регионе
50 клиентских шлюзов в регионе

50 VPN в регионе
200 таблиц маршрутизации и.т.д

![image](https://user-images.githubusercontent.com/58170246/125051843-08b4de80-e0ac-11eb-8f1e-ce63ec8807e2.png)

одно виртуальное облако создается с акаунтом AWS

![image](https://user-images.githubusercontent.com/58170246/125052244-6d703900-e0ac-11eb-85a0-f2c5d0572309.png)

3 Основы сетевой маршрутизации

интернет шлюз в VPS (internet gateways)

![image](https://user-images.githubusercontent.com/58170246/125059652-39991180-e0b4-11eb-97bf-fd77195f4303.png)

Шлюз созданный вместе с виртуальным облаком по умолчанию. Разрешает наладит связь между инстансами в VPC и сетью интернет. Шлюз эластичный=подстраисается под показания текущей нагрузки. обладает высокой отказоустойчивостью. Предоставляет преобразование сетьевых адресов=в NAT для инстансов которые имеют публичный IP адрес. Шлюз не может быть отключен от VPC, если там находятся активные ресурсы AWS. 

Для отключения шлюза 

![image](https://user-images.githubusercontent.com/58170246/125060525-2470b280-e0b5-11eb-8783-b41020017c53.png)

после отключения даный шлюз можно использовать для подключения к другой VPS


![image](https://user-images.githubusercontent.com/58170246/125060775-5eda4f80-e0b5-11eb-8ab7-b0d397f66a95.png)

таблицы маршрутизации

набор правил= маршруты, для определения маршрутов отправки трафика.

Есть назначения (диапазон SIDR (диапазон IP адресов которым будет доставлен трафик)) и цель (идентификатор куда даные будут направлены).

![image](https://user-images.githubusercontent.com/58170246/125061893-7a922580-e0b6-11eb-9663-eb2aecd1cfd8.png)

Входящий и исходящий трафик направляется согласно таблице маршрутизации. 

Можем редактировать маршрут с целью интернетшлюза, ноне с целью локал.

Подсети. 

подсеть может существовать только в рамках 1 зоны доступности. Подсети должны быть связаны  с таблицей маршрутизации. Есть приватные и публичные (подключен интернет шлюз).

![image](https://user-images.githubusercontent.com/58170246/125062825-7a465a00-e0b7-11eb-925a-9bfdc12c7cab.png)

Создадим таблицу маршрутизации

![image](https://user-images.githubusercontent.com/58170246/125063036-b1b50680-e0b7-11eb-91d8-60d50da327ee.png)

Получаем сеть локал, без интернет шлюза

![image](https://user-images.githubusercontent.com/58170246/125063206-df01b480-e0b7-11eb-9781-38c17fa66aec.png)

Подсеть будет считаться приватной.

4  Основы безопасности VPC

Контроль сетьевого доступа (ACL)

![image](https://user-images.githubusercontent.com/58170246/125063689-749d4400-e0b8-11eb-90e8-5a5450d28748.png)

поддерживает правила разрешения или запрета входящего или исходящего трафика.

Не имеет статуса по умолчанию. Правила определены по приоритету. Чемниже значение тем выше приоритет трафика. 

![image](https://user-images.githubusercontent.com/58170246/125064436-584dd700-e0b9-11eb-8141-89e3e9f24c46.png)

Правило 80 позволяет поступать трафику типа SSH по протоколу TSP через 22 порт со всех адресов

Правило 90. Правило для HTTP. Позволяет поступать трафику по протоколу TSP через 80 порт.
чередуется согласно установленому номеру!!

один ACL может быть применен к продсети. и один к множеству подсетей.

Групы безопасности. (обеспечивает безопасность на уровне инстансов)

устанавливают только правила разрешающие прием илиотправку (запрета нет!!)

![image](https://user-images.githubusercontent.com/58170246/125065583-a6170f00-e0ba-11eb-818b-e422e0f152b6.png)

СЕРВЕРНОЕ ВЫЧИСЛЕНИЕ


1 – Основы EC2

Основная вычислительная платформа AWS. предоставляет виртуальные серверы в облаке. Один вертуальный сервер =инстанс. но также инстанс может относится к RDS-базы данных (сервис от AWS). Спроектированы как традиционные сервера но свозможностью масштабируемости в зависимости от нагрузки. Образ машины амазон. Тип инстанса (оперативная память), сетевой интерфейс, тип хранилища (EBS, или хранилище инстанса). Присоздании инстанса ему должна быть назначена группа безопасности (у уровню виртуальгого приватного облака VPC). Каждый инстанс должен быть расположенн в определенной VPC (зоне доступности и подсети). В каждой зонедоступностинесколько подсетей. При создании инстанса должны указать в какой подсетион должен быть расположен. При создании инстанса мы имеем возможность установки программ загрузки инстанса, которые будут выполнены автоматически при загрузке инстанса (budstreping). Для организации данных можем использовать тегги. Для логин аутентификаци используется зашифровання пара ключей. Существуют лимиты на количество инстансов.

![image](https://user-images.githubusercontent.com/58170246/125157350-3022ae80-e173-11eb-9a15-26c96128cfe0.png)

Но можно запросить повышение лимита. 

![image](https://user-images.githubusercontent.com/58170246/125157393-6829f180-e173-11eb-9228-ca4b83120f02.png)

2 – Варианты покупки

по требованию-выбираем, оплачиваем, юзаем, когда хотим прекращаем.-наиболее затратный, и надежный. (можеи мспользовать на протячжении минуты, часа, дня недели). оплата только за время работы. Оплата может быть посекундная (только к образам машин амазон и убунту) после 60 секунд за каждую дополнительную секунду, почасовая-ко всем остальным операционным системам-выдновс, редхет, сентуэс-оплата за каличество целых часов.  

резервированое-![image](https://user-images.githubusercontent.com/58170246/125158001-c6a49f00-e176-11eb-8d3e-e679b7c6aadc.png), преобрести инстанс на установленный промежуток времени. от 1 до 3 лет-платим за фиксированное время использования инстанса. Не зависит от показаний использования. 

спотовое-порог оплаты на использование инстанса (цена равна или меньше на использованый порог). Ненадежный. Оплачивается посекундно и почасово.  

3 – AMI и виртуализация

![image](https://user-images.githubusercontent.com/58170246/125158212-20f22f80-e178-11eb-9ac2-4a57ae993f27.png)

AMI- содержит некоторуюначальную коннфигурацию, включает операционную систему, пакеты с програмным обеспечением, тип корневого хранилища, типы виртуализации, с автомасштабируемостью. Можем создать собственный AMI, выбрать его на торговой площадке. 

Виртуализация-создание виртуальной версии чего либо.

Виртуальный сервер запущен на физическом сервере. мы делим физическое оборудование с другими пользователями. используется специальный гипервизер XEN. 2 параметра виртуализации HVM-аппаратная виртуальная машина, операционную систему запускаем сразу в виртуальной машине, может использовать расшерение сети и PV-паравиртуальзация, возможность запуска модифицированной гостевой операционной системы без аппаратной виртуализации. 

4 – Типы инстансов

![image](https://user-images.githubusercontent.com/58170246/125159012-649b6800-e17d-11eb-9404-5f134fad2c20.png)

Фильтрация по необходимомутипу

![image](https://user-images.githubusercontent.com/58170246/125159032-80067300-e17d-11eb-993b-dcaf8e9a96c2.png)


5 – Публичный̆, приватный̆ и эластичный̆ IP адрес

![image](https://user-images.githubusercontent.com/58170246/125159067-b5ab5c00-e17d-11eb-9e72-b3467b1815f2.png)

приватный IP для комуникации инстансов внутри сети (не доступен из вне VPC). Не может быть точкой доставки трафика интернета.

Публичный для сети интернет. (к примеру через SSH с даным инстансом на прямую)

Модифицировать IP для подсети.

![image](https://user-images.githubusercontent.com/58170246/125159338-73831a00-e17f-11eb-887b-6e719e2e9de8.png)

![image](https://user-images.githubusercontent.com/58170246/125159360-931a4280-e17f-11eb-8757-0a8a7edb6c4b.png)

![image](https://user-images.githubusercontent.com/58170246/125159404-c65cd180-e17f-11eb-9125-b92bdafd7b58.png)

 Даному инстансу не пудет назначен публичный IP при нахождении вданной подсети.
 
 Эластические IP для динамических вычислений в облаке. Публичные.Заменяет публичный адрес.
 
 ![image](https://user-images.githubusercontent.com/58170246/125159560-db863000-e180-11eb-9f37-8af1eeb6c007.png)

![image](https://user-images.githubusercontent.com/58170246/125159574-f35db400-e180-11eb-9470-b1e9b6e1ac10.png)

6 – Bootstrapping

Набор команд, которые выполняются автоматически при запуске инстанса.

запустили апаче2

![image](https://user-images.githubusercontent.com/58170246/125159734-dd042800-e181-11eb-899f-82a8b338c053.png)

для просмотра этих данных необходимо выполнит команды.

![image](https://user-images.githubusercontent.com/58170246/125159753-0624b880-e182-11eb-844e-f5a5089d015c.png)


7 – Конфигурация хранилища

хранилища EBS -не присоеденинн к машине. Расположенны й датацентре
количество операций ввода и вывода IOPS, 1 IOPS 256 к.б, если нужно больше- используют больше IOPS.
оптимизированный EBS пропускная способность соответствует заявленной

![image](https://user-images.githubusercontent.com/58170246/125161690-691b4d00-e18c-11eb-83df-4e28c216a001.png)

![image](https://user-images.githubusercontent.com/58170246/125161731-99fb8200-e18c-11eb-900a-002df0c30790.png)

Новые разделы показывают максимальную производительность сразу после создания.

EBS общего назначения ![image](https://user-images.githubusercontent.com/58170246/125161789-01b1cd00-e18d-11eb-9189-c2d693ebcea2.png) среда розработки и тестирования. для малых инстансов с базами данных. 1 гБ-16 трБ, 100/3000 (минимальная пропускная способность в 100 IOPS и 3000 IOPS во время пиковых.  t2mikro-предоставление дополнительной пропускной способности во время пиковых нагрузок. 

с фиксированным для большихбаз данных.
![image](https://user-images.githubusercontent.com/58170246/125162216-535b5700-e18f-11eb-8860-861878d4cde2.png)

магнетик, самый недорогой. для приложений которые не требуют высокой производительности. 
![image](https://user-images.githubusercontent.com/58170246/125162269-8b629a00-e18f-11eb-8124-f8bfcf59f2cf.png)

и хранилища инстанса EBS могут существовать вне инстанса, и быть переподключен. тип хранилища не может быть 



8 – Группа безопасности

RDP установка соединения через протокол удаленного рабочего стола. 

![image](https://user-images.githubusercontent.com/58170246/125162587-65d69000-e191-11eb-92d2-554b1f3e46e9.png)


9– Создание пары ключей и соединение через SSH

pm файл при использовании аутентификации с помощью линукс необходимо изменить права доступа к файлу с помощью команды "chmod 400 имя-файла-ключа"

![image](https://user-images.githubusercontent.com/58170246/125163749-404c8500-e197-11eb-802b-8127ff64af67.png)

![image](https://user-images.githubusercontent.com/58170246/125163760-59edcc80-e197-11eb-8844-21b6c01fbd16.png)

11 – Создание снапшота


12– Группы расположения
 
 Максимально низкой задержки между инстансами. Если Инстанс не входил в группу то мы и добавит в группу не сможем. близко расположены физически.
 
 ![image](https://user-images.githubusercontent.com/58170246/125170142-15bdf480-e1b6-11eb-80d6-eb0d699a5c93.png)
 
 один тип инстансов в одной группе расположения. групы расположения не могут быть соединины. Инстансы должны поддерживать скорость в 10 Gb
 
 ![image](https://user-images.githubusercontent.com/58170246/125170256-c0ceae00-e1b6-11eb-9ace-f625379d81da.png)


13 – Эластичная файловая система (EFS)

![image](https://user-images.githubusercontent.com/58170246/125170278-e0fe6d00-e1b6-11eb-9d23-dd31f38600e9.png)

EFS сетевое хранилище. расширение предостовляемого пространства по мере необходимости.  Инстансы которые  используют EFS всегда будут необходимый им обьем пространства  за счет масштабируемости EFS

![image](https://user-images.githubusercontent.com/58170246/125170333-55391080-e1b7-11eb-8bef-9bac5f8897bb.png)

EFS может быть использовано несколькими инстансами одновременно (EFS общее хранилище данных). может быть монтирована на локальных домашних серверах при рямом  соединении  с AWS, что позволяет перенести  данные с локальных серверов на EFS или использовать в качестве хранилищь роезервных копий. Оплачивается только фактически предоставленный  обьем данных. В отличии от EBS-оплачивается максимальный предоставленный  обьем. 

![image](https://user-images.githubusercontent.com/58170246/125171305-3db05680-e1bc-11eb-8b81-4c8c55144433.png)

Создадим  2 инстанса и примонтируем к EFS.


![image](https://user-images.githubusercontent.com/58170246/125173484-38590900-e1c8-11eb-9b53-5367a6447ee0.png)


![image](https://user-images.githubusercontent.com/58170246/125173346-83265100-e1c7-11eb-8b69-61ed3167f8e3.png)

долгое монтирование означает что группа безопасности не дает завершить монтирование. добавляем группу безопасности по умолчанию к даному инстансу. данная группа безопасности разрешает инстансам взаимодействовать с EFS

![image](https://user-images.githubusercontent.com/58170246/125173669-05fbdb80-e1c9-11eb-8556-f3fba4838b89.png)

выбераем группу default

![image](https://user-images.githubusercontent.com/58170246/125173722-4ce9d100-e1c9-11eb-88f0-5647c739323b.png)

























