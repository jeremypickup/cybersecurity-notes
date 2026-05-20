# Love

nmap -p- --min-rate=1000 -sC -sV 10.129.48.103

We have HTTP on port 80 and 5000, HTTPS, SMB, and MYSQL

![image.png](image.png)

![image.png](image%201.png)

 before that  I need to add the domain and subdomain in the host’s file.

sudo vim /etc/hosts

![image.png](image%202.png)

We have a voting system for this web application using PHP programming language so let’s use feroxbuster:

feroxbuster -u [http://10.129.48.103](http://10.129.48.103/) -q -k

![image.png](image%203.png)

I don’t find anything interesting let’s use Searchsploit to check if we find any exploit.

I found RCE :49445.py but need cred.

![image.png](image%204.png)

this sudo domain works on HTTP and I found this page.

![image.png](image%205.png)

I have input take URL, Let’s test SSRF

http://localhost:5000

 admin : @LoveIsInTheAir!!!! 

![image.png](image%206.png)

Now i need to copied this file

![image.png](image%207.png)

then r**evise file**

![image.png](image%208.png)

**implement it**

![image.png](image%209.png)

![image.png](image%2010.png)

![image.png](image%2011.png)

[Love 提權](https://www.notion.so/Love-3516b41a378480d6bdded127019afae6?pvs=21)