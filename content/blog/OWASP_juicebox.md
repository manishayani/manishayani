---
title: "OWASP Juice Shop"
type: portfolio
Date: 2020-02-07T16:54:54+06:00
description : "This is meta description"
caption: Learning Journal
image: images/blog/OWASP-JuiceShop.png
Category: ["Learning Journal"]
submitDate: 07 February, 2020
Location: UTS
---
## Challenge 1 -> SQL Injection

This was the basic and one of the easiest challenges to solve. First, I visited the login screen and typed random name and password combination which gave me prompt of invalid username or Password. Then I typed “‘“ a single quote mark in the username and password field. This time the error was “[object object]”. Since I have worked on SQL before, I know that this error is thrown when there is a syntax error. So now this time I used one of the classic SQL Injection syntax, available on the internet that is ‘1 = 1 -- ‘. After entering it into username and password text boxes, I got logged in to the system.
