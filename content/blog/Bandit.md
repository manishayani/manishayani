---
title: "Bandit"
type: portfolio
Date: 2020-02-04T16:54:54+06:00
description : "This is meta description"
caption: Learning Journal
image: images/blog/bandit.jpg
Category: ["reflection","sprint 3"]
submitDate: 08 February, 2020
Location: UTS
---
### INTRODUCTION
Bandit is a wargame which is for beginners to increase their linux commands skills. This game is the first step for other high level war games. This game was advised by the tutor to improve command skills and get a little hands-on on linux terminal. To play around Bandit I used my Kali Linux Os. The Instruction of the games and how to reach the next level are clearly mentioned. To have a proper understanding of the commands I have made a Learning journal for this game and keeps on updating it whenever required.

## LEARNING JOURNAL

SSH
> ssh [domain_name] -p [port_number] -l [username]

A Filename with - cannot be open directly, we have to use 
> cat ./-

Filename with the space cannot be opened directly. It needs to be put in quotes.

Hidden Files won't be displayed normally when used ls command

To display hidden files in the directory use the -a option of the ls command to view all the files in the directory

To open the hidden files use 
> cat .hidden

Use file command to get the extension of the file
> file [directory]
For current directory
> file *

But this won't work in case where the filename starts with '-'  because the compiler considers it as an option. Therefore we need to specify the full path of the directory.

Find command can be used to search for file types with different properties

>find * -type f -size 1033c ! -executable -readable

An '!' mark can be used in front of any option to negate its output

> 2>/dev/null
This Command can be used to filter out the output on console to not show the errors

Difference Between find and Grep is that Find command is used to search for a file with some different properties whereas grep is used to search within a file (regex).
