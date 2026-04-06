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

1.Check internet using Firefox.  
  
2.Open LibreOffice and type a document.  
  
3.Open files.  
  
4.Install a Software in APP center.  
  
5.Practice basic commands.  
  
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
  
6.Basic commands 2:   
  
ps-e : List all running processes onr the system  
top : Dispaly real time process resource usage  
ls : List files  
ls -la : List all files  
ls -alt : List files sorted by modification time  
  
**Outpust are shown in the screenshouts below:**  
![bc](images/basic-commands1.png)
![bc](images/basic-commands2.png)
![bc](images/basic-commands3.png)
  
7.File Operations:  
  
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
  
8.System Information  
  
uname -a : Dispaly kernel version,hostname,OS,etc.  
lsb_release -a : Show Linux distribution information  
hostnamectl : Display system hostname and related details  
  
**Outputs are shown in the screenshots below:**
![SI](images/system-information1.png)
![SI](images/system-information2.png)
  
9.User Permission
  
whoami : Show the Currently loggen in name  
sudo whoami : Execute 'whoami' as superuser  
sudo adduser testuser : Create a new user named 'testuser'  
  
**Oupputs are shown in the screenshot below:**
![UP](images/user-permission1.png)
![UP](images/user-permission2.png)
  
10.Network Configuration
  
ip a : Show all network interfaces and their IP addressed (private IPs)  
ping -c 4 8.8.8.8 : Send 4 ICMP packets to google DNS to test conectivity  
  
**Outputs are shown in the screenshots below:**
![NC](images/network-configuration1.png)
![NC](images/network-configuration2.png)
  
**Ubuntu network settings window:**
![NC](images/network-configuration3.png)
  
11.Modifying/etc/hosts
  
sudo nano /etc/hosts : Edit the hosts file  
ping -c 2 mytestalias : Test if the alias resolves to 127.0.0.1  
  
**Outputs are shown in the screenshots below:**
![M](images/modify-etc,hosts1.png)
![M](images/modify-etc,hosts2.png)
  
12.DNS Query
  
nslookup google.com : Query DNS records for google.com  
sudo apt install whois -y: Install the whois tool  
whois google.com | head -20 : Query domain registration infomations (first 20 lines)  
  
**Outputs are shown in the screenshots below:**
![DNS](images/dns-query1.png)
![DNS](images/dns-query2.png)
![DNS](images/dns-query3.png)
  
13.Public IP vs Private IP
ip a : Dispaly Private IP address  
Explanation: Private IPs are used only within loal networks and cannot be routed on the internet.Public IPs are globally unique and identify a device on the internet.  
  
**Private IP Screenshot:**
![PI](images/public-ipVSprivate-ip1.png)
  
**Public IP (open https://whatismyipaddress.com/ in Firefox):**
![PI](images/public-ipVSprivate-ip2.png)
  
14.Hard ware Information
susb : List USB devices  
lspci : list PCI devices  
less /proc/cpuinfo : View CPU details page by page  
  
**Outputs are shown in the screenshots below:**
![HWI](images/HW-information1.png)
![HWI](images/HW-information2.png)
![HWI](images/HW-information3.png)
  
**Settings-About:**
![HWI](images/HW-information4.png)
  
15.Output Redirection
lsusb > output_of_lsusb : Redirect output of 'lsusb' to a file  
cat output_of_lsub : Display the file conte  
less output_of_lsusb : View the file page by page  
rm output_of_lsusb : Delete the file  
  
**Outputs is shown in the screenshot below:**
![OR](images/output-redirection1.png)
  
16.Software Installation Methods
*SaaS* : Access Google Docs
![SIM](images/SW-installation-method1.png)
  
*Binary package(.deb)*
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb : Download Chrome .deb package  
sudo dpkg -i google0chrome-stable_current_amd64/deb : Install the .deb package  
sudo apt-get install -f : Fix any missing dependencies  
![SIM](images/SW-installation-method2.png)
![SIM](images/SW-installation-mothod3.png)
  
*Software centre installation*
Open App center and install Steam
![SIM](images/SW-installation-method4.png)
![SIM](images/SW-installation-method5.png)
  
17.APT Commands
sudo apt update : Update package list from repositories  
sudo apt upgrade -y : Upgrade all installed packages  
sudo apt install vlc -y : Install VLC media player  
less /etc/apt/sources.list : View APT repository configuration  
  
**Outputs are shown in the screenshots below:**
![APT](images/APT-commands1.png)
![APT](images/APT-commands2.png)
  
18.Compiling a C Program
Source code : hello_world.c:
include <stdio.h>
int main(){
printf("Hello,World!\n");
return 0;
}
  
Compilation command: gcc hello_world.c -o hello_world_executable  
Excution : ./hello_world_executable  
Output : Hello, World!  
**Screenshots:**
![CACP](images/compile-the-c-program1.png)
![CACP](images/compile-the-c-program2.png)
![CACP](images/compile-the-c-program3.png)
  
**19.Reflection**
19.1 Which file editors are best for remote access and why?  
Answer : I think nano is the best one i used, because it's teminal-based.And it's very convenient to use.  
19.2 Compare software installation mehods:SaaS vs binaries vs repos vs dource.  
Answer : SaaS requires no installation but depends on internet.Binaries are easy but may have dependency issues.Repos manage denpendencies automatically.Source complilation offers flexibility but is more complex.  
19.3 How did using CLI imporve your understanding of linux?
Answer : CLI gave me direct interaction with the kernel,taught me about file permissions,process management,pipelines,and made me more efficient than GUI.  

## Lab 1b : Lixux Services
Update package list : sudo apt update
  
Install apache : sudo install apaches2 -y
  
Tested on web Http : 127.0.0.1
  
Install SSH and Nmap : sudo apt install openssh-servernmap -y
  
Get IP Address : ip a
  
Nmap port Scan : nmap 127.0.0.1 
Port 80(http) and 22(SSH) are open 
  
Stop and remove Apache to see port 80 disappear : sudo systemctl stop apache2 then sudo apt remove apache2 -y
Scan again : nmap 127.0.0.1  
Port 80 is gone  
  
Reinstall Apache : sudo apt insatll apache2 -y  
  
Modify index.html Page  
sudo nano /var/www/hetl/index.hetm  
  
Replace content  
  
save content and then refresh browser at http://127.0.0.1
  
Enabled firwall allowing http ports 80 : sudo ufw enable and sudo ufw allow 80
  
Test SSH login to localhost : ssh lcalhost
  
Creat a new user : sudo addsuer testuser2
  
Creat a directory and download a sample book from Project Gutenberg :
mkdir books  
cd books  
wget https://www.gutenberg.org/files/84/84-0.txt -O frankenstein.txt  
cd ..  
  
Create a tar archive : 
tar cf books.tar books  
ls -lh boks.tar  
  
Compress the tar archive with bzip2 : 
bzip2 books.tar  
ls -ls book.tar.bz2  
  
Decompress: first bunzip2, then extract tar : 
bunzip2 books.tar.bz2  
tar -xvf books.tar  

**Screenshots:**  
![A](images/install-apache1.png)
![A](images/install-apache2.png)
![SSH](images/install-ssh.png)
![IP](images/ipa1.png)
![NPC](images/nmap-port-scan1.png)
![NPC](images/nmap-port-scan2.png)
![NPC](images/nmap-port-scan3.png)
![MI](images/modify-index1.png)
![MI](images/modify-index2.png)
![CUF](images/configure-ufw-firewall1.png)
![SSH](images/enable-ssh1.png)
![USER](images/create-a-new-user1.png)
![BOOK](images/book1.png)
![BOOK](images/book2.png)
![LIST](images/LS.png)
  
## Labs 1b : Linux Permissions
  
Create users with default home directories :
sduo adduser alice  
sudo adduser bob  
sudo adduser mallory  
Create group, add alice and bob to the group, Then Verify it :
sudo groupadd sharedgroup  
sudo usermod -aG sharedgroup alice  
sudo usermod -aG sharedgroup bob  
grep sharedgroup /etc/group  
Create shared directory :
sudo mkdir /home/shared  
Create ten File :
sudo touch /home/shared/file{1..10}  
Set Permissions :
sudo chmod 750 /home/shared  
Verify Access as Each User and Delete mallory from group  
Clean up :
sudo rm -r /home/shared  

**Screenshots:**  
![NU](images/new-user1.png)
![NU](images/new-user2.png)
![NU](images/new-user3.png)
![S](images/sharegroup1.png)
![S](images/sharegroup2.png)
![D](images/d1.png)
![T](iamges/t1.png)
![UT](images/user-test1.png)
![UT](images/user-test2.png)
![UT](images/user-test3.png)
![FP](images/file-permission.png)
![D](images/delete.png)
![C](images/clean.png)
  
# Lab 1b : Linux Searching Files
1.Creating files  
mkdir lab1b  
cd lab1b  
  
2.Create 3 files in lab1b  
touch file.txt file1.txt notes.log  
  
3.pipe text into files  
echo "Hello" -> file.txt  
echo "Lab 1b" -> file1.txt  
echo "Shaohui" -> notes.log  
  
4.Find files with -name  
find . -name "file.txt"  
find . -name "*.txt"  
find . -type d  
  
5.Test what inside of the files  
grep "Lab" file1.txt  
grep -i "LAB" file1.txt  
grep "Hello" *  
grep -r "Shaohui"  
  
6.Combitionation uses of grep and find  
find . -name "*.txt" -exec grep "Lab" {} \;
  
**Screenshots**
![SF](images/searching-files1.png)
![SF](images/searching-files2.png)
![SF](images/searching-files3.png)
![SF](images/searching-files4.png)
![SF](images/searching-files5.png)
  
# Lab 2a: Total cost of Ownership (TCO)
1.Overview  
This report compares the **Total Cost of Ownership (TCO)** of two printers over 5 years, based on a typical office printing load.
  
Printer A : HP LaserJet MFP M42523dn  
Printer B : Epson Ecotan L6279  
  
2.Common Assumputions  
Time period for 5 years  
Weekly print volume : 750 pages  
Electricity rate : 0.29 SGD/kWh  
Paper cost (500 sheets) : 5.40 SGD  
Weeks per year : 52  
**Total pages printed : 195,000 pages**  
**Total operating hours : 10,400 hours**  
3.Reflection  
3.1 Which printer has lower tco and why?  
Epson EcoTank L6279 - mainly because ink bottles are much cheaper per page than laser toner(SGD 0.0213 vs 0.0243 per page). Even though it may need repalcement during the period, its running costs are lower.  
  
3.2 Would the answer chanfe for a home user printing only 5 pages/week?  
Yes. At 5 pages/week, total pages over 5 years = 1,300. Both printers would have very low consumable usage, so the initial purchase price becomes dominant. The HP laser would be more expensive (764 vs 439 SGD), but ink may dry out in the Epson if used rarely. A cheap black and white laser might be best.  
  
3.3 Other non-financial fators to consider?  
Colour printing (Epson does colour, HP is mono)  
Print speed (HP are faster)  
Wireless/ mobile printing (Epson supports Wi-Fi)  
Duplex (both support)  
Scanner quality  
  
**Screenshots:**
![TCO](images/TCO1.png)
![TCO](images/TCO2.png)
![TCO](images/TCO3.png)
  
## Lab 2b : AWS Ubuntu Apache CLI
1.EC2 Instance configuration  
Region : Asia Pacific  
AMI : Ubuntu 24.04 LTS  
Instance type : t3.micro (Free tier)  
Security group : apache-sg  
SSH (22) - source 0.0.0.0/0  
HTTP (80) - source 0.0.0.0/0  
  
2.Instance Running And Public IP  
Public IPv4 address : 54.206.196.14  
Instance state : Running  
  
3.Connect via EC2 Instance Connect (browser-based terminal)  
Used AWS console's built-in terminal  
  
4.Install Apache  
sudo apt update  
sudo apt install apache2 -y  
sudo systemctl start apache2  
sudo systemctl enable apache2  
systemctl status apache2  
  
5.Test web access
Open browser : http://54.206.196.14  
  
6.Stop Instance  
After completing the lab,the instance was stopped to no more charges  
  
REFLECTION:  
The EC2 instance connect feature simplifies SSH access without key management  
Always stop instances after lab work  
Securitu groups must allow HTTP (port 80) for public web access  
  
**Screenshots**
![AWS](images/AWS7.png)
![AWS](images/AWS6.png)
![AWS](images/AWS1.png)
![AWS](images/AWS2.png)
![AWS](images/AWS3.png)
![AWS](images/AWS4.png)
![AWS](images/AWS5.png)

## Lab 2b ： Bash Scripting
1.File System Operations  
All commands were executed in the AWS EC2 instance (Ubuntu 24.04).  
mkdir LabFiles  
cd LabFiles  
touch notes.txt  
echo "This is a note" > notes.txt  
cat notes.txt  
cp notes.txt notes_backup.txt  
mv notes_backup.txt old_notes.txt  
rm old_notes.txt  
cd ..  
ls -l  
2.Basic Bash Script  
nano hello_Shaohui.sh  
Make executable and run:  
chmod 777 hello_Shaohui.sh  
./hello_Shaohui.sh  
3.Loop and Conditional Script  
nano system_info.sh  
Input 3 20 -1  
4.System Monitoring Script  
nano resource_monitor.sh  
chmod 777 resource_monitor.sh  
./resource_monitor.sh  
  
REFLECTION:
1. What command did you use to create a new directory?
mkdir LabFiles

2. How can you view the contents of a file without opening it in a GUI?
Use terminal commands such as cat, less, head, tail, or nano/vim (text-based editors).

3. What is the purpose of chmod 777?
It gives read, write, and execute permissions to all users (owner, group, others). This is very permissive and should be used cautiously, but for lab scripts it ensures the script can be run by anyone.

4. What does #!/bin/bash do at the start of a script?
It is a shebang line that tells the system to use the Bash interpreter located at /bin/bash to execute the script.

5. What happens when invalid input is entered into a script?
It depends on how the script is written. If no validation is implemented, the script may behave unpredictably (e.g., compare an empty string with a number, causing an error). In our system_info.sh script, invalid input (e.g., a letter) would cause the numeric comparison to fail and might produce an error message. Good scripts include input validation to handle such cases gracefully.

6. What output does free -h show?
It shows the system’s memory (RAM) and swap usage in human-readable format (e.g., KiB, MiB, GiB), including total, used, free, shared, buff/cache, and available memory.
**Screenshots:**
![F](images/file1.png)
![BBS](images/basic-bash-scrip1.png)
![BBS](images/basic-bash-scrip2.png)
![L](images/loop1.png)
![L](images/loop2.png)
![M](images/monitoring1.png)
![M](images/monitoring2.png)
![M](images/monitoring3.png)

## Lab 3a : Domain, DNS and TLS Certificates
1.  Launch EC2 Instance and Configure Security Group
nbound rules (allowing SSH, HTTP, HTTPS):
SSH (22) – source `0.0.0.0/0`
HTTP (80) – source `0.0.0.0/0`
HTTPS (443) – source `0.0.0.0/0`

2. Install Apache
sudo systemctl start apache2
sudo systemctl enable apache2
sudo systemctl status apache2

3. Register Free Domain (DuckDNS)
Registered shaohuilabs.duckdns.org at duckdns.org
Set A record to point to EC2 public IP: 3.26.43.158

4. Verify DNS Resolution
nslookup shaohuilabs.duckdns.org

5. Install Certbot and Obtain TLS Certificate
sudo apt install certbot python3-certbot-apache -y
sudo certbot --apache -d shaohuilabs.duckdns.org

6. Test HTTPS Access
Open browser and visit https://shaohuilabs.duckdns.org

7. Test Automatic Renewal (Dry Run)
sudo certbot renew --dry-run

**Screenshots:**
![DNS](images/DNS2.png)
![DNS](images/DNS3.png)
![DNS](images/DNS1.png)
![DNS](images/DNS4.png)
![DNS](images/DNS5.png)
![DNS](images/DNS6.png)
![DNS](images/DNS7.png)
![DNS](images/DNS8.png)

REFLECTION:
1. What is the role of DNS in Internet presence?
DNS translates human-readable domain names (e.g., shaohuilabs.duckdns.org) into machine-readable IP addresses, allowing users to access services without memorizing numbers.

2. Why does DNS propagation take time?
DNS changes are cached by resolvers and ISPs. The TTL (Time To Live) value determines how long old records are kept. Propagation can take minutes to hours.

3. How does Let's Encrypt validate domain ownership?
Let's Encrypt uses HTTP-01 challenge (placing a temporary file on the web server) or DNS-01 challenge (adding a TXT record). In this lab, HTTP-01 was used – Certbot created a file under /.well-known/acme-challenge/ and Let's Encrypt fetched it over port 80.

4. What are the risks if TLS is not configured on a public-facing site?
Data transmitted in plaintext (eavesdropping)
Man-in-the-middle attacks
  
Browser warnings ("Not Secure")
  
Poor SEO ranking
  
Loss of user trust
  
5. What could happen if you leave your cloud VM running for months?
Accumulated charges (even t2.micro costs about $8-10/month)
  
Potential security vulnerabilities if not updated
  
Wasted credits (if using student credits)
  
Incurred debt if credit expires

## Lab 3b : Server Automation
1. Created the following structure inside /home/ubuntu/Documents:
text
Documents/
├── file1.txt
├── file2.txt
└── subdir/
    └── file3.txt
2.Basic Script Working
Initial script (/home/ubuntu/testscript) performing recursive copy and zip.
Script content:
#!/bin/bash
now=$(date +"%d_%m_%y")
mkdir -p /home/ubuntu/backup
cp -R /home/ubuntu/Documents/* /home/ubuntu/backup/
cd /home/ubuntu || exit
zip -r "${now}.zip" backup
cp "${now}.zip" /home/ubuntu/
echo "Backup completed: ${now}.zip"
Execute permission granted and tested:
chmod 777 /home/ubuntu/testscript
/home/ubuntu/testscript
3.Script Moved to /usr/bin and Tested
sudo mv /home/ubuntu/testscript /usr/bin/testscript
testscript
4.ZIP Archive with Date Filename
5. Cronjob Set Up for Hourly Backup
Crontab entry added to run the script every hour:
0 * * * * /usr/bin/testscript >> /home/ubuntu/cron_backup.log 2>&1
Verify with:
crontab -l
6.Successful Cron Execution Verified
ls -lh /home/ubuntu/*.zip
tail /home/ubuntu/cron_backup.log
**Screenshots：**
