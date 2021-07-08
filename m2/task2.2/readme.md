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

Роли необходимый элемент для работы с сервисом S3. Вместо политик к сервисам применяем роли. 



6 - IAM STS

7 - API Keys in IAM


