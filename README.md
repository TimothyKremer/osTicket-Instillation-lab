# osTicket-Instillation-lab
#  Project summary
This is project is a tehcnical walkthrough and implementation guide for deploying the osTicket support ticketing system on a Windows 10 Microsoft Virtual Machine.
### Environments Used 
-Microsoft Azure 

-windows 10 Virtual Machine 
### Technologies Applications Services used
-Azure Virtual Machines

-PHP 7.3.8

-Internet Information  Services

-PHP Manager for IIS

-URL rewrite Module

-HeidiSQL (For database management)
# Video demonstration
https://youtu.be/_pYx7E2v0IM
# Demonstration
![showing creation of virtual machine](https://github.com/user-attachments/assets/dbc055f5-f575-4492-b739-5cd328c2e8b3)
I navigated to virtual machines ins Microsft azure and than clicked create virtual machine. I clicked create new resource group called osTicket. I named the virtual machine
osticket-vm and put the region in us-west-2. For the image I set the vm with Windows 10 pro version 22h2-x6Gen2. And as for the size I gave the vm Standard D2s_2vcpus 8 GIB memory.

I set the username as labuser and the password as Cyberlab123! I let the asure automatically create a new network. I than created the virtual machine.
![showing remote desktop into vm](https://github.com/user-attachments/assets/3c8c107c-11a8-495d-b755-3002e6dd5ef3)
Once the vm had depoyed I used the public Ip address and the username and password to remote desktop into the virtual machine. Once I was logged into the vm I grabed the osTicket installation files proved and downloaded them inside the vm. Once downloaded I proceeded to draged the compressed filles onto the the desktop. I than extracted the files.
![showing download of os ticket files](https://github.com/user-attachments/assets/fae9c075-49bd-412d-aac7-6e0e63828f50)




