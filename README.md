# Ethical Hacking Intro: Network Port Scanning with Nmap

<h2>Description</h2>
In this Ethical Hacking Lab in TCM's Practical Help Desk Course, I learned to install nmap, run an initial scan, and an aggressive scan against the target "scanme.nmap.org".
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux CLI</b> 

<h2>Environments Used </h2>

- <b>Linux Mint 22</b> 

<br />
<br />
Installing nmap with "sudo nala install nmap". I prefer nala over apt for package installation because of its parallel package downloads, the ability to select the fastest mirrors, and package transaction history.

![1) installing nmap](https://github.com/user-attachments/assets/64fa4a96-d25b-4fe3-9ed8-7a258e14b7c5)

<br />
<br />
For my initial nmap scan, I used "nmap -v scanme.nmap.org" and found ports 22, 9929, and 31337 open on the target scanme.nmap.org.

![2) nmap scan shows open ports](https://github.com/user-attachments/assets/e1662cbf-d6f9-4c73-97e0-84df2a759a31)

<br />
<br />
For my aggressive scan on the target, I used "nmap -p- -A -T4 scanme.nmap.org".
-p specifies which ports I wanted to scan and using '-' after it specified it to scan all ports.
The -A option enables aggressive scanning which attempts to detect operating systems and application details.
Finally -T was used to indicate the speed of the scan from 1-5  (slowest to fastest). Since I wasn't worried about detection, I opted for a speed of -T4.
The scan showed the version details of its SSH server: "OpenSSH 6.6.1p1" along with numerous ssh-hostkeys. 

![3) detailed nmap scan ](https://github.com/user-attachments/assets/1e0fc106-4919-4fed-a896-63837519b5a6)

<br />
<br />
