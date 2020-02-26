---
title: "Sprint 5 Deliverable"
type: portfolio
Date: 2020-02-23T20:22:12+06:00
description : "This is meta description"
caption: Deliverable
image: images/blog/OpenAdmin1.jpg
Category: ["reflection","sprint 5"]
submitDate: 24 February, 2020
Location: UTS
---

## Gathering Information

First step would be to gather information about the system so as to find vulnerabilities.

1. Starting with the NMap Scan.

> nmap -sC -sV -p- -o nmap_scan.txt 10.10.10.171

-sC is used to run default nmap scripts
-sV is used to get the version information.
-p- is used to search for all the ports.
-o is used to store the scan result in file.

![nmap](/images/blog/OpenAdmin/nmap_scan.PNG)

There are two services ports running 22 and 80. Port 22 is ssh and 80 is for http i.e a web server is running.

2. Open the IP on a web browser.

![web_server](/images/blog/OpenAdmin/web_server.PNG)

we found that a default apache web server loads in.

Now Lets Find any sub directories on the server.

3. Open dirbuster and enter the full url in the target URL

![dirbuster](/images/blog/OpenAdmin/dirbuster.PNG)

For files with list of dirs/files, head on to /usr/share/dirbuster/wordlists and select any wordlist.
Hit start.


After the scanning is finished, we see that there are number of files and directories available.

![dirbuster1](/images/blog/OpenAdmin/dirbuster1.PNG)

After going through it, we land on to ona page, which is a login page

4. Go on to ona page on browser

![login_page](/images/blog/OpenAdmin/login_page.PNG)

We see that there is a notification shown that the server is v18.1.1 but we dont know of what. After clicking on to the download butoon we are directed to Opennetadmin website. This clarifies that the server is running Open Net Admin v18.1.1.

## Exploitation

Upon Googling I found an exploit for OpenNetServer V18.1.1 on exploit-db.

The Exploit is an XSS code that provides us with a shell.

5. Download the XSS code and enter the following command to convert the code into linux suitable format.
link -> https://www.exploit-db.com/exploits/47691
> dos2unix 47691.sh

This step is important because the file may have been created in another OS, so the EOF character is each OS is different, this command helps in converting the file into linux readable fomat.

6. Run the script
> sh 47681.sh 10.10.10.171

![initial_shell](/images/blog/OpenAdmin/initial_shell.PNG)

Now that we got the shell, lets look for any meaningfull data. Since this shell has limited access we do not have much to look for.

After looking into all the directories, I found a file name database-_settings.inc.php which is a database config file

![database_config_file](/images/blog/OpenAdmin/database_config_file.PNG)

From the file we have a password but we are not sure whose password it is.

Lets see if we can find the list of users

7. Head on to /etc/passwd to have a look of list of users

> cd /etc/passwd

![list_of_users](/images/blog/OpenAdmin/list_of_users.PNG)

There are only two users who have shell access that is jimmy and joanna.

8. Use the w command to see list of logged in users
>w

There are chances that the password we found in the database file can be of the jimmy or joanna. lets try it on the login page.

That didnt work, Lets try it using ssh it

9. ssh into the ip using jimmy as host
> ssh jimmy@10.10.10.171

![jimmy_login](/images/blog/OpenAdmin/jimmy_login.PNG) 

Now lets look for any file of importance.


