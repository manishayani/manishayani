---
title: "Mr Robot CTF"
type: portfolio
Date: 2020-02-14T13:02:45+06:00
description : "This is meta description"
caption: Learning Journal
image: images/blog/mrrobot.jpg
Category: ["Learning Journal"]
submitDate: 14 February, 2020
Location: UTS
---
### INTRODUCTION
Mr Robot is a vulnerable machine available on VulnHub. It is designed for Teaching and Learning purposes. This machine is designed after the famous TV series “Mr Robot”. The main aim of this challenge is to find three flags. Capturing each flag increases the difficulty level of the challenge.

To set up the Mr Robot Vm, first, download and install the OpenVPN client and install the config file available on the website

After setting up the VPN, then open the Kali and Mr Robot Vm in VMware or VirtualBox.

![machine_setup](/images/blog/machine_setup.PNG)

1. The First step is to use the netdiscover command to locate the IP of the machine. At the start, I was not able to get the desired result, as network settings were not configured properly, but after I configured the network setting from VM settings I was able to locate the IP of the machine.

![Network Problem](/images/blog/network_problem.PNG)

The command is:
> sudo netdiscover -i eth0

![Netdiscover](/images/blog/netdiscover.PNG)

2. I tried going to the browser with the IP I found during on netdiscover (192.168.88.130)

![Web](/images/blog/web.PNG)

After browsing a little bit on the web, the website just had different videos and images.

3. I had the IP now, so now I used port scanning tool (nmap) to listen for the open ports.

> nmap -sC -sV 192.168.88.130

![nmap](/images/blog/nmap.PNG)

From the above image, we can see that there are 2 active ports 80(http) and 443(https). Nothing much available here.

4. I tried looking at the page source, to see if I can find a lead but still nothing much available

![nmap](/images/blog/page_source.PNG)

5. So, next, I tried using the nikto Vulnerability Assessment tool to see vulnerabilities iin the system if any

> nikto -h 192.168.88.130

![Nikto](/images/blog/nikto.PNG)

After looking into the results and seeing various files, we landed onto a wordpress admin page

![Wordpress](/images/blog/wordpress.PNG)

6. I saw a tool in the application manager, called wpscan which is wordpress security scanner, I used it.
> wpscan -url 192.168.88.130

![Wordpress](/images/blog/wordpress.PNG)
 
7. I found a file named robots.txt. I typed the file name in the URL and found this

![Robots](/images/blog/robots.PNG)

Then typing the above file name in the browser, I found the first flag in the file named "key-1-of-3.txt"

![key1](/images/blog/key1.PNG)

8. We also found a file name fsocity.dic. It is a dictonary file which may contain username and password. Upon looking into the file I found that the file has many duplicate values, so I decided to sort the file and also remove the duplicates.
> cat  fsocity.dic | sort -u | uniq > abcd.dic

9. Now we have to Bruteforce the username and Password from the fscocity.dic to gain access.
We can try this, but this is very resource intensive

> wpscan --url 192.168.88.130 --passwords abcd.dic --usernames abcd.dic

So, we need to have an efficient approach, for this we can use burpsuite

10. We now  run the Burpsuite to fetch the post request

![burpsuite](/images/blog/burpsuite.PNG)

11. Now we use this post request and use hydra to bruteforce and get the username

![hydra](/images/blog/hydra.PNG)

Now once we got the username, we could do the same to bruteforce the password

12. I'll be using Wordpress Security Scanner to bruteforce

> wpscan -v --url 192.168.88.130 --passwords abcd.dic --usernames Elliot

![wpscan1](/images/blog/wpscan1.PNG)

![loggedin](/images/blog/loggedin.PNG)

To Be Continued ...

