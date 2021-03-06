# TASK 2.1
## PART 1. HYPERVISORS
1. Hypervisor is a technology for deploying software on physical hardware using virtualization. Hyper-V, KVM, ESXi. - run directly on the hardware and do not require the installation of any operating system. VMware Workstation, Oracle Virtual Box, OpenVZ - you an operating system - through of it you can access the hardware.
2. Oracle Virtual Box is a Type 2 hypervisor and must be installed on the host operating system as a software application. VMware Player, Workstation and Fusion are Type 2 hypervisors and must also be installed on the underlying host operating system. VMware ESXi is a Type 1 hypervisor and must be installed on a platform without an operating system. VMware and Virtual Box support hardware virtualization. Oracle Virtual Box is a cross-platform solution that can be installed on Linux, Windows, Solaris, macOS, FreeBSD. 
## PART 2. WORK WITH VIRTUALBOX
1. First run VirtualBox and Virtual Machine (VM).
1.1 Get acquainted with the structure of the user manual VirtualBox[1](see list of references in the end of the document)

1.2 From the official VirtualBox site [2] download the latest stable version of VirtualBox according to the host operating system (OS) installed on the student's workplace. For Windows, the file may be called, for example, VirtualBox-6.1.10-138449-Win.exe. Install VirtualBox.

1.3 Download the latest stable version of Ubuntu Desktop or Ubuntu Server from the official site [3].

![image](https://user-images.githubusercontent.com/58170246/124380285-96678700-dcc4-11eb-845b-0d181e86a06b.png)

1.4 Create VM1 and install Ubuntu using the instructions [1, chapter 1.8]. Set machine name as "host machine name"_"student last name"

![image](https://user-images.githubusercontent.com/58170246/124380349-dc244f80-dcc4-11eb-8836-02df7bd821f9.png)

1.5 Get acquainted with thepossibilities of VM1 control -start, stop, reboot, save state, use Host key and keyboard shortcuts, mouse capture, etc. [1, ch.1.9].

![image](https://user-images.githubusercontent.com/58170246/124380395-1392fc00-dcc5-11eb-9c4c-44337a1165d1.png)

1.6 Clone an existing VM1 by creating a VM2 [1, ch.1.14].

![image](https://user-images.githubusercontent.com/58170246/124380434-3f15e680-dcc5-11eb-98ed-a6fbebb36b14.png)

![image](https://user-images.githubusercontent.com/58170246/124380439-44733100-dcc5-11eb-86a9-99a51c4a7dc9.png)

![image](https://user-images.githubusercontent.com/58170246/124380446-4c32d580-dcc5-11eb-9b6a-3c026e409f28.png)

1.7 Create a group of two VM: VM1, VM2 and learn the functions related to groups [1, ch.1.10].

![image](https://user-images.githubusercontent.com/58170246/124381420-1e508f80-dccb-11eb-893b-ce429738cf07.png)

![image](https://user-images.githubusercontent.com/58170246/124381661-573d3400-dccc-11eb-8ccf-35c105914aff.png)

![image](https://user-images.githubusercontent.com/58170246/124381681-7a67e380-dccc-11eb-9e94-76ccb195a4a4.png)

1.8 For VM1, changing its state, take several different snapshots, forming a branched tree of snapshots[1, ch.1.11].

![image](https://user-images.githubusercontent.com/58170246/124381708-9a97a280-dccc-11eb-8c9a-50b499b20581.png)

1.9 Export VM1. Save the *.ova file to disk. Import VM from *.ova file[1, ch.1.15].

![image](https://user-images.githubusercontent.com/58170246/124381914-8b652480-dccd-11eb-828b-fcdbf5d33845.png)

![image](https://user-images.githubusercontent.com/58170246/124381945-aafc4d00-dccd-11eb-82e7-1fd47235fcdc.png)

![image](https://user-images.githubusercontent.com/58170246/124381957-ba7b9600-dccd-11eb-96d5-b3448bc63915.png)

![image](https://user-images.githubusercontent.com/58170246/124383943-d4ba7180-dcd7-11eb-8605-0a945ab640a2.png)

![image](https://user-images.githubusercontent.com/58170246/124384033-41357080-dcd8-11eb-808a-2cd70b0bfc70.png)

![image](https://user-images.githubusercontent.com/58170246/124384047-53171380-dcd8-11eb-9b26-a04e934e2a3b.png)


2. Configuration of virtual machines


2.1 Explore VM configuration options (general settings, system settings, display, storage, audio, network, etc.).

![image](https://user-images.githubusercontent.com/58170246/124384305-362f1000-dcd9-11eb-976d-eabe81e09bc2.png)

2.2 Configure the USB to connect the USB ports of the host machine to the VM [1, ch.3.11].

![image](https://user-images.githubusercontent.com/58170246/124384339-5a8aec80-dcd9-11eb-8605-cdf28f942018.png)

![image](https://user-images.githubusercontent.com/58170246/124384894-18af7580-dcdc-11eb-9bf7-243a91da6d6d.png)


2.3 Configure a shared folder to exchange data between the virtual machine and the host [1, ch.4.3].

sudo adduser iryna vboxsf

![image](https://user-images.githubusercontent.com/58170246/124385608-261a2f00-dcdf-11eb-88e4-0584f5b92a37.png)

![image](https://user-images.githubusercontent.com/58170246/124395134-0f89cd00-dd0b-11eb-9fd2-93d02e067da5.png)

![image](https://user-images.githubusercontent.com/58170246/124385377-ebfc5d80-dcdd-11eb-95ec-a117f389edeb.png)


2.4 Configure  different  network  modes  for  VM1,  VM2.  Check  the  connection between VM1, VM2, Host, Internet for different network modes. You can use the pingcommand to do this. Make a table of possible connections.

Intnet VM1, VM2,

changed the name of one host -hostname losst-pc

![image](https://user-images.githubusercontent.com/58170246/124396144-968d7400-dd10-11eb-9a12-8675525c2dc0.png)

Host-only

![image](https://user-images.githubusercontent.com/58170246/124396723-e9b4f600-dd13-11eb-8c19-033901a66ba7.png)

![image](https://user-images.githubusercontent.com/58170246/124396689-c25e2900-dd13-11eb-9235-7fb2bb860d34.png)




3. Work with CLI through VBoxManage.

3.1 Run the cmd.exe command line.

3.2 Examine  the  purpose  and  execute  the  basic  commands  of  VBoxManage list, showvminfo, createvm, startvm, modifyvm, clonevm, snapshot, controlvm[1, ch.8].


## PART 3. WORK WITH VAGRANT

1. Download the required version of Vagrant according to the instructions [5] and according  to  the  host  operating  system  (OS)  installed  on  the  student's  workplace.  For Windows, the file may be called, for example, vagrant_2.2.0_x86_64.msi. Install Vagrant. Check  the  path  to  Vagrant  bin  in  the  Path  variable (My  computer -> Properties -> Advanced system settings -> Advanced -> Environment Variables).

2. Run the powershell. Create a folder "student name" (in English). In this example, create a folder vagrant_test. Next, go to the folder.

3. Initialize the environment with the default Vagrant box:init hashicorp/precise64

4. Run vagrant upand watch for messages during VM boot and startup.

5. Connect  to  the  VM  using  the  program  PuTTY  (can  be  downloaded  from  [6]), using SSH, IP address and port listed above (127.0.0.1:2222). By default, login -vagrantand password are also vagrant

6. Record the date and time by executing the datecommand

7. Stop and delete the created VM.

8. Create your own Vagrant box[7]

9. (optional)Createa  test  environment  from  a  few  servers.  Servers'  parameters are chosen independently by the student.

https://github.com/IrynaOliynyk/IrynaOliynyk-DevOps_online_Lviv_2021-Q3/blob/main/m2/task2.1/Vagrantfile








