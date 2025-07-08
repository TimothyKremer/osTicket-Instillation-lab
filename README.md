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

I set the username as labuser and the password as Cyberlab123! I let the azure automatically create a new network. I than created the virtual machine.

![showing remote desktop into vm](https://github.com/user-attachments/assets/3c8c107c-11a8-495d-b755-3002e6dd5ef3)

Once the vm had depoyed I used the public Ip address and the username and password to remote desktop into the virtual machine. Once I was logged into the vm I grabed the osTicket installation files proved and downloaded them inside the vm. Once downloaded I proceeded to draged the compressed files onto the the desktop. I than extracted the files.

![showing download of os ticket files](https://github.com/user-attachments/assets/fae9c075-49bd-412d-aac7-6e0e63828f50)

Next I needed to enable information serivice and CGI. I navigated to controll panal and then clicked uninstall a program under programs. I clicked on Turn Windows features on or off. I enabled  internet information services and than CGI. I than allowed windows to make the necessary changes. 
![showing download enablling of cgi](https://github.com/user-attachments/assets/815d671b-3f9a-4bd4-af0a-a260786e2533)

After windows completed the requested changes I next needed to install the PHP manager. I navigated to the osTicket installation files and then procedied to download PHP manager for IIs. 
![installing php manager for IIS](https://github.com/user-attachments/assets/249ba4fe-732d-492c-b833-f7b4bc1f77b9)

After PHP manager was installed I then needed to install rewrite_amd64_en-us. I downloaded it form the osTicket instilation files.  
![image](https://github.com/user-attachments/assets/b761d57c-6105-46a8-95b7-d56039b9a880)


Next I created a folder named PHP on the cdrive and then installed php.7.3.8. After that I extracted the php 7.3.8 folder into the PHP folder on the C drive.
After that I installed VC_redistx86.
![image](https://github.com/user-attachments/assets/b54187a4-9b55-4dca-8f81-8d59d0600919)


Next I downloaded MYSQL Server. I chose typical setup type and also standard configuration. As far as the root pasword I chose the word root. 
![image](https://github.com/user-attachments/assets/f81184c3-9a9f-42de-ab8c-ea89dea757ff)


After installing MYSQL server I needed to register a new PHP version in PHP manager in internet information Services. I navigated to internet information serivices manager and then clicked on PHP Manager and then clicked on new PHP version. I was prompted to get the php excutiable file so I navigated to the PHP folder and than clicked on php.cgi and then pressed ok.
![image](https://github.com/user-attachments/assets/234e4e50-936d-42f3-a030-5a3a6a70670e)


After that I restarted the server by right clicking on osticket-vm in the connections and then clicked stop and then start.
![image](https://github.com/user-attachments/assets/17e0abe5-cfcf-4c54-bc60-7b098944cf34)

After that I navigated to the osTicket installation files and extracted osTicket on the the osTicket instalation file folder. 
Afterthat I navigated to the windows c drive and than to the intepub folder and then the www.root folder and then moved the upload folder from the osTicket file into the www.root folder and then named the upload folder to osTicket.
![image](https://github.com/user-attachments/assets/bd33d3c4-59f6-49e4-90d8-31ea4fdaf263)


I than restarted the server again using the same steps as before in IIS.After restarting the server again i clicked on the browse 80 folder under actions and launched the osTicket installation web page in internet explore.
![image](https://github.com/user-attachments/assets/f9ef46e2-7d2d-4a02-bdb8-f25fb8d926ff)

I than needed to install some recommended prererquisites. I navigated to IIS and then clicked on PHP manager and then enabled three php extensions  php_imap.dll,  php_intl.dll, and  php_opcache.dll
![image](https://github.com/user-attachments/assets/56404625-262b-408e-a92b-6a79d01f1938)

After that I renamed the ost-sample config.php folder to ost-config.php and right clicked the folders to get to properties and than removed inherited permissions and than gave full controll to everyone. 
![image](https://github.com/user-attachments/assets/a82dc531-37f3-48eb-b559-d54562b98658)

I than clicked continue on the osTicket installation web page filled out the information requested for system settings and Admin user.

Lastly I downloaded HeidiSQL and then created a database with the userame being root and the pasword being root and then filled at the informaion in data base settings.
![image](https://github.com/user-attachments/assets/75663502-0264-49de-896b-03ca35267608)


At this point osTicket installed
![image](https://github.com/user-attachments/assets/4d48e24d-58fa-48bb-bd44-c52a767339cf)


