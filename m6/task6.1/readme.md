Networking with Linux 

1.Create virtual machines connection according to figure 1:

https://qna.habr.com/q/702327

![image](https://user-images.githubusercontent.com/58170246/129625046-72f91d78-08df-4e3e-bd53-73eca07e48c4.png)




2.VM2 has one interface (internal), VM1 has 2 interfaces (NAT and internal). Configure  all networkinterfaces in order to make VM2 has an access to the Internet (iptables, forward, masquerade).  

I. Перша, назвемо її Сервер, грає роль шлюзу

Також встановлено сервіс dnsmasq для призначення ip-адрес хостам в Intnet.

Для забезпечення Інтернет-з'єднання на Клієнта, включив маськарадінг в iptables:
iptables -t nat -A POSTROUTING -o enp0s3 -j MASQUERADE

А також форфардінг портів:
sysctl -w net.ipv4.conf.all.forwarding = 1

![image](https://user-images.githubusercontent.com/58170246/135130505-2501c821-483a-43bd-ad1c-2d924db5e041.png)

![image](https://user-images.githubusercontent.com/58170246/135130969-7325a7ce-b77f-42cf-80dd-fe09fffae82d.png)


vm2

![image](https://user-images.githubusercontent.com/58170246/135136933-35bc4785-d248-49fd-b5dd-74f1b1b3d7cd.png)



3.Check the route from VM2 to Host. 

4.Check the access to the Internet, (just ping, for example, 8.8.8.8). 

![image](https://user-images.githubusercontent.com/58170246/135140732-ed1f4d29-9b32-4614-9136-325c2ffbefe2.png)

![image](https://user-images.githubusercontent.com/58170246/135142069-74f6c99a-d307-4404-bc74-94b1ffa236ef.png)



![image](https://user-images.githubusercontent.com/58170246/135304874-d8d09c60-1e7b-4008-8374-f7948b4e2ebb.png)

https://askubuntu.com/questions/148638/how-do-i-enable-the-universe-repository




5.Determine, which  resource has an IP address 8.8.8.8.

![image](https://user-images.githubusercontent.com/58170246/135336414-5a7fc720-c859-4455-94f2-5c80fe49174e.png)




6.Determine, which  IP address belongs to resource epam.com. 

7.Determine the default gateway for your HOST and display routing table. 

8.Trace the route to google.com. 

