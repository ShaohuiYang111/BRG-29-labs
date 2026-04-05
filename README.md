# BRG-29-labs labs report

## Student information
**Student name:Shaohui Yang**  
**Kaplan ID: CT0382031**  
**Murdoch ID: 35920041**  

## Day 1a-1

Install virtualbox on the host machine.

Downloaded Ubuntu desktop ISO.

Created a new VM:

RAM:4096 MB
HD:20GB

Completed installation and system configuration.

## Day 1a-2

labs:

#1.Check internet using Firefox.  
  
#2.Open LibreOffice and type a document.  
  
#3.Open files.  
  
#4.Install a Software in APP center.  
  
#5.Practice basic commands.  
  
pwd  
ls /  
cd /etc  
cd  
mkdir dir1  
cd dir1  
touch hello world.text  
ls -l  
cd ..  
**Outputs are shown in the screenshot below:**  
![Firefox](images/firefox.png)
![LibreOffice](images/libreoffice-writer.png)
![file](images/files.png)
![software centre](images/software-centre.png)
![basic commands](images/basic-commands.png)
  
#6.Basic commands 2:   
  
ps-e : List all running processes onr the system  
top : Dispaly real time process resource usage  
ls : List files  
ls -la : List all files  
ls -alt : List files sorted by modification time  
  
**Outpust are shown in the screenshouts below:**  
![bc](images/basic-commands1.png)
![bc](images/basic-commands2.png)
![bc](images/basic-commands3.png)
  
#7.File Operations:  
  
touch testfile.txt : Create an empty file  
nano testfile.txt : Open the file  
cat testfile.txt : Displat the entire file content  
less testfile.txt : View file content page by page  
cp testfile.txt copy.txt : Copy the file  
mv copy.txt moved.txt : rename/move the file  
rm moved.txt : Delete the file  
  
**Output are shown in the screenshouts below:**
![FO](images/file-operation1.png)
![FO](images/file-operation2.png)
![FO](images/file-operation3.png)
  
#8.System Information  
  
uname -a : Dispaly kernel version,hostname,OS,etc.  
lsb_release -a : Show Linux distribution information  
hostnamectl : Display system hostname and related details  
  
**Outputs are shown in the screenshots below:**
![SI](images/system-information1.png)
![SI](images/system-information2.png)
  
#9.User Permission
  
whoami : Show the Currently loggen in name  
sudo whoami : Execute 'whoami' as superuser  
sudo adduser testuser : Create a new user named 'testuser'  
  
**Oupputs are shown in the screenshot below:**
![UP](images/user-permission1.png)
![UP](images/user-permission2.png)
  
#10.Network Configuration
  
ip a : Show all network interfaces and their IP addressed (private IPs)  
ping -c 4 8.8.8.8 : Send 4 ICMP packets to google DNS to test conectivity  
  
**Outputs are shown in the screenshots below:**
![NC](images/network-configuration1.png)
![NC](images/network-configuration2.png)
  
**Ubuntu network settings window:**
![NC](images/network-configuration3.png)
  
#11.Modifying/etc/hosts
  
sudo nano /etc/hosts : Edit the hosts file  
ping -c 2 mytestalias : Test if the alias resolves to 127.0.0.1  
  
**Outputs are shown in the screenshots below:**
![M](images/modify-etc,hosts1.png)
![M](images/modify-etc,hosts2.png)
  
#12.DNS Query
  
nslookup google.com : Query DNS records for google.com  
sudo apt install whois -y: Install the whois tool  
whois google.com | head -20 : Query domain registration infomations (first 20 lines)  
  
**Outputs are shown in the screenshots below:**
![DNS](images/dns-query1.png)
![DNS](images/dns-query2.png)
![DNS](images/dns-query3.png)
  
#13.Public IP vs Private IP
ip a : Dispaly Private IP address  
Explanation: Private IPs are used only within loal networks and cannot be routed on the internet.Public IPs are globally unique and identify a device on the internet.  
  
**Private IP Screenshot:**
![PI](images/public-ipVSprivate-ip1.png)
  
**Public IP (open https://whatismyipaddress.com/ in Firefox):**
![PI](images/public-ipVSprivate-ip2.png)
  
#14.Hard ware Information
lsusb : List USB devices  
lspci : list PCI devices  
less /proc/cpuinfo : View CPU details page by page  
  
**Outputs are shown in the screenshots below:**
![HWI](images/HW-information1.png)
![HWI](images/HW-information2.png)
![HWI](images/HW-information3.png)
  
**Settings-About:**
![HWI](images/HW-information4.png)
  
#15.Output Redirection
lsusb > output_of_lsusb : Redirect output of 'lsusb' to a file  
cat output_of_lsub : Display the file conte  
less output_of_lsusb : View the file page by page  
rm output_of_lsusb : Delete the file  
  
**Outputs is shown in the screenshot below:**
![OR](images/output-redirection1.png)
  
#16.Software Installation Methods
*SaaS* : Access Google Docs
![SIM](images/SW-installation-method1.png)
  
*Binary package(.deb)*
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb : Download Chrome .deb package  
sudo dpkg -i google0chrome-stable_current_amd64/deb : Install the .deb package  
sudo apt-get install -f : Fix any missing dependencies  
![SIM](images/SW-installation-method2.png)
![SIM](images/SM-installation-mothod3.png)
  
*Software centre installation*
Open App center and install Steam
![SIM](images/SM-installation-method4.png)
![SIM](images/SM-installation-method5.png)
  
#17.APT Commands
sudo apt update : Update package list from repositories  
sudo apt upgrade -y : Upgrade all installed packages  
sudo apt install vlc -y : Install VLC media player  
less /etc/apt/sources.list : View APT repository configuration  
  
**Outputs are shown in the screenshots below:**
![APT](images/APT-commands1.png)
![APT](images/APT-commands2.png)
  
#18.Compiling a C Program
Source code : hello_world.c:
#include <stdio.h>
int main(){
printf("Hello,World!\n");
return 0;
}
  
Compilation command: gcc hello_world.c -o hello_world_executable  
Excution : ./hello_world_executable  
Output : Hello, World!  
**Screenshots:**
![CACP](images/complie-the-c-program1.png)
![CACP](images/complie-the-c-program2.png)
![CACP](images/complie-the-c-program3.png)
  
**19.Reflection**
19.1 Which file editors are best for remote access and why?  
Answer : I think nano is the best one i used, because it's teminal-based.And it's very convenient to use.  
19.2 Compare software installation mehods:SaaS vs binaries vs repos vs dource.  
Answer : SaaS requires no installation but depends on internet.Binaries are easy but may have dependency issues.Repos manage denpendencies automatically.Source complilation offers flexibility but is more complex.  
19.3 How did using CLI imporve your understanding of linux?
Answer : CLI gave me direct interaction with the kernel,taught me about file permissions,process management,pipelines,and made me more efficient than GUI.  

