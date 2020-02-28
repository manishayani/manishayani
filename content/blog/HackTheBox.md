---
title: "Sprint 5"
type: portfolio
Date: 2020-02-23T20:22:12+06:00
description : "This is meta description"
caption: Reflection
image: images/blog/HackTheBox/banner.png
Category: ["Invite Challenge","Hack The Box"]
submitDate: 24 February, 2020
Location: UTS
---

1. Open Inspect Element by right clickong on the page or Ctrl + Shift + I

![Collaboration](/images/blog/HackTheBox/page_source.PNG)

2. We will see there is a javascript running inviteapi.min.js

3. Select the link and paste it in another tab url, we will see the actual script

![Collaboration](/images/blog/HackTheBox/script.PNG)

4. There is a function towards the end of script with the name of makeInviteCode. This looks interesting.

5. Go back to inspect element window and click on Console tab. Try running the makeInviteCode() Funcction.

![function](/images/blog/HackTheBox/function.PNG)

We see that an object is generated but the data is encoded in base ROT13 type.

6. Go to google and search for base 64 decoder and decode the data

![decoded_text](/images/blog/HackTheBox/decoded_text.PNG)

After decoding we see that there is a message stating that in order to get invite code we need to generate a post request.

7. Open terminal and use the curl command to generate a POST request

> curl -X POST https://www.hacthebox.eu/api/invite/generate

![encoded_key](/images/blog/HackTheBox/encoded_key.PNG)

From the above generated key we can deduce that the text is in base64 format as there is '=' at the end. Now lets, decode the text

8. Open any base64 decoder and decode the text

![serial_key](/images/blog/HackTheBox/serial_key.PNG)

Upon pasting this on the invite code screen on hack the box, we will be able to register.

