
Configuring DHCP, DNS servers and dynamic routing using OSPF protocol

https://askubuntu.com/questions/148638/how-do-i-enable-the-universe-repository

http://integrator.adior.ru/index.php/virtualbox-setup/53-probros-portov-v-virtualnuyu-mashinu-virtualbox

https://wikiroot.ru/question/podelitysya-virtualynoy-mashinoy-virtualbox-s-drugim-polyzovatelem

https://sandilands.info/sgordon/building-internal-network-virtualbox

https://learningtechnix.wordpress.com/2020/04/25/linux-dynamic-dns-ddns-setup/

https://www.ekzorchik.ru/2012/12/ubuntu-10-dnsmasq-office-network/



1. Use already created internal-network for three VMs (VM1-VM3). VM1 has NAT and internal, VM2, VM3 – internal only interfaces.


2-3. Install and configure DHCP server on VM1. 


![image](https://user-images.githubusercontent.com/58170246/135495779-3bf12ebc-1379-4bc2-9662-f464e28f7b7e.png)


![image](https://user-images.githubusercontent.com/58170246/135495595-6796daf7-1925-4247-aec9-5ec5cd528d05.png)

![image](https://user-images.githubusercontent.com/58170246/135495661-08cfab6e-56b6-4392-8729-78d8324ae363.png)


(3 ways: using VBoxManage, DNSMASQ and ISC-DHSPSERVER). 

# разрешить динамическую аренду адресов и срок аренды (12 годин)

![image](https://user-images.githubusercontent.com/58170246/135495297-cea2c268-4655-4186-9cf0-3160cdd2480b.png)


You should use at least 2 of them.

Check VM2 and VM3 for obtaining network addresses from DHCP server.

Using VBoxManage:

vboxmanage dhcpserver add --netname intnet --ip 192.168.20.1 --netmask 255.255.255.0 --lowerip 192.168.20.100 --upperip 192.168.20.150 --enable

