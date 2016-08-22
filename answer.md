1. **nslookup** do

(nslookup is the name of a program that) lets an Internet server administrator or any computer user enter a host name (for example, "whatis.com") and find out the corresponding IP address. It will also do reverse name lookup and find the host name for an IP address you specify.

2. To display the top most process utilizing CPU process:

```
ps -eo %cpu,comm,pid,euser | sort -nr | head -10

ps axo ruser,%cpu,comm,pid,euser | sort -nr | head -n 10
```
3. To check all open ports on a Linux machine and block the unused ports

```
netstat -tulp
netstat -tulpn

nmap -sU localhost for udp
nmap -v localhost for tcp

netstat -t(tcp)
netstat -u(udp)or
netstat -tulpn
```
to verfy the open ports

to block u have to use iptable & tcp_wrappers( hosts.deny
file)

To Block Ports for eg.22 and 80 as requested
> iptables -t filter -A INPUT -s!192.168.0.0/24 (IP which you want to allow) -p tcp -d (destination server IP) --dport
22 -j DROP

> iptables -t filter -A INPUT -s!192.168.0.0/24(IP which you
want to allow) -p tcp -d (destination server IP) --dport
80 -j DROP

4. Linux and the different with UNIX?

Linux Is Just a Kernel.

Linux is just a kernel. All Linux distributions includes GUI system + GNU utilities (such as cp, mv, ls,date, bash etc) + installation & management tools + GNU c/c++ Compilers + Editors (vi) + and various applications (such as OpenOffice, Firefox).

However, most UNIX operating systems are considered as a complete operating system as everything come from a single source or vendor.

[standard diffrent](https://www.linux.com/answers/what-standard-difference-bw-linux-and-unix)

[more](http://www.cyberciti.biz/faq/what-is-the-difference-between-linux-and-unix/)

5. The boot process of Unix System: .
[reference 1](https://www.safaribooksonline.com/library/view/essential-system-administration/0596003439/ch04s01.html)

[reference 2](http://www.thegeekstuff.com/2011/02/linux-boot-process/?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+TheGeekStuff+(The+Geek+Stuff))

[reference 3](http://www.golinuxhub.com/2014/03/step-by-step-linux-boot-process.html)
