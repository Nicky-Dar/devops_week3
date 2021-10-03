# devops_week3

 
![image](https://user-images.githubusercontent.com/88620315/135764650-86052165-a9a1-4de9-acb0-ea9a7fae15b4.png)
# TEXT EDIOR
by default there is a nano text editor already in ubuntu, to see the nano version you can use the following command:
>nano –version

to create a file with the nano text editor

> nano [nama file]

press the command to display shortcuts help

CTRL + G

press the command to search for a specific word

CTRL + W

press the command to save, without closing the nano text editor application

CTRL + O

press the command to enter the contents of the other files into the and it will be combined

CTRL + R
 
press the command to replace the word

CTRL + \ 
  
press the command to select text

ALT + A

press the command to copy the selected text

ALT + 6

press the command to paste the copied text

CTRL + U

press the command to move the cursor to the beginning

CTRL + A

press the command to move the cursor to the end

CTRL + E

press the command to cut the text after being selected

CTRL + K

press the command to justify the text, later the text will be one line parallel to the first line

CTRL + J

press the command to tell the cursor position is on the line where

CTRL + C

press the command to exit the editor and you will be asked for changes to confirm whether the changes will be saved press Y for yes and N for no then press enter

CTRL+X

# TEXT MANIPULATION

#### SORT

can be used to sort the contents of a file. Sort can also be combined with the pipe “|” to display the output of a command.

create a file with the name [filename] and can be filled with numbers and words.

nano [filename]

perform ASC with the command.
sort [filename]

do a DESC with that command
sort -r [filename]

Show row selection
sort [filename] | line
 
#### CUT
cut is used to print some part of the contents of a file.
Create file as with name [filename]

nano [filename]

To do the cut, type the command, and give the number until how many letters are taken
cut c 1-5 [filename]

#### CAT
cat is one of the commands that serves to list the contents or contents of a file in standard output
To be able to view the contents of the file

cat [filename]

To create a new file and enter text

cat > [filename]

Merge two or more files into one file

cat [filename 1] [filename 2] [filename 3]>[filename 4]

Combination of cat and sort, for sorting

cat [filename]| sort

Display two files at the same time

cat [filename 1] [filename 2]

Numbering the string

cat -n [filename]

## monitoring sistem
#### Htop:
htop is an interactive program for monitoring system processes and managing processes. Htop provides a complete list of running processes, so you can see which processes are consuming a lot of CPU/RAM resources.
 ![image](https://user-images.githubusercontent.com/88620315/135764620-0c5f2ee2-a4c3-4bf7-bcdb-4170523a523d.png)
#### LSOF

lsof is a command to see all files that are currently open, lsof itself stands for list open files

Lsof

Lsof -u user

Lsof -i :[port]
 ![image](https://user-images.githubusercontent.com/88620315/135764606-9e268349-e74e-48e7-a5d6-2901581e6b5b.png)

 ![image](https://user-images.githubusercontent.com/88620315/135764592-c243b8cc-6aa5-435e-b1db-2f89def9c8be.png)


#### PROCESS STATUS

Knowing the list of processes running on the system, ps stands for ststus process

Ps -f -u user
![image](https://user-images.githubusercontent.com/88620315/135764573-9f70e387-3237-43ef-bf43-b7378ccde91f.png)


ps -aux
 ![image](https://user-images.githubusercontent.com/88620315/135764538-9efb8440-79a3-4723-a807-d7fd1fad9a6a.png)


## firewall 
Firewall is computer hardware or software that controls access in and out of websites, in other words a firewall is an important element for computer security.

Network firewall is also a command that can be used to secure a server, the tool commonly used is iptables / ufw

Iptables is a Linux module that provides direct support for the kernel starting from version 2.4 for system security and other purposes. Iptables can be used to define a set of port-based security rules securing specific hosts.

UFW Ubuntu is equipped with an application that makes it easy to configure the firewall, the application is ufw (uncomplicated firewall) which is presented as an iptables front-end.
if you receive the command error not found install ufw, then when the next command.

>sudo ufw status

first install the ufw

>sudo apt install ufw -y

for block all incoming access

>sudo ufw default deny incoming

check the installed ufw.

>sudo ufw status

open all outgoing access.

>sudo ufw default allow outgoing

displaying applications supported by ufw, you will get a list of application profiles.

>sudo ufw app list

Nginx Full: This profile opens both port 80 (normal and unencrypted web traffic) and port 443 (TLS/SSL encrypted traffic) 

Nginx HTTP: This profile opens only port 80 (normal and unencrypted web traffic) Nginx HTTPS: This profile only opens port 443 (TLS/SSL encrypted traffic)

allow outside access for nginx applications.
>sudo ufw "nginx full"

open port 80.
>Sudo ufw allow 80

open access for port 80 with tcp connection.
>sudo ufw allow 80/tcp

opened access for port 80 with udp connection.
>sudo ufw allow 80/udp

blocking access to port 80.
>sudo ufw deny 80

delete port 80 configuration
>sudo ufw delete deny 80

we can check with systemd init system to make sure the service is running.
>systemctl status nginx
 
 ![image](https://user-images.githubusercontent.com/88620315/135764481-1cbe791f-9c6d-483a-8d62-0c8253894792.png)

>Sudo ufw default allow/deny incoming/outgoing
 ![image](https://user-images.githubusercontent.com/88620315/135764700-7272f1df-3243-4dc0-922d-38daf416b328.png)

>Sudo ufw app list

 ![image](https://user-images.githubusercontent.com/88620315/135764683-05c9f1ef-329d-44db-b084-13a85d2edd97.png)
![image](https://user-images.githubusercontent.com/88620315/135764688-ed44dff3-d479-4f77-9917-07dc6b4118b9.png)

 
https://cmsmanajer.com/register
 ![image](https://user-images.githubusercontent.com/88620315/135764722-9c226ed9-bae6-44d1-b1df-db0d872f3f5b.png)

52.221.182.149
 ![image](https://user-images.githubusercontent.com/88620315/135764728-494e291f-69ee-4303-b460-72bd602cf495.png)
 
 
Curl localhost:80
 
![image](https://user-images.githubusercontent.com/88620315/135764741-4bdd66a9-e002-4723-aaf0-e1d14e760d90.png)

# SYSTEM PERFORMANCE
vmstat is a tool to display memory and swap usage, then it will also provide information about processes, system interrupts, I/O speed and CPU statistics in real time.

type the command to install, in order to use vmstat
>sudo apt install sysstat -y

type the command, to run vmstat
>vmstat

to display more detailed information can type the following command
>vmstat -sSM

vmstat only displays data based on a collection of previous data, meaning that it is not as real-time as in monitoring tools.
to display vmstat in realtime 5 second 10 times.
>vmstat 5 10

Iostat will display the data with our infrastructure information.
display system input/output information, see how long the device is active in relation to speed.
>lostat

nmon nmon for monitoring with more complete data, you can use nmon.
install nmon first
>sudo apt install nmon -y

run the following command to display an information.

>nmon

press n to display network
press c to display cpu
press d to display disc
