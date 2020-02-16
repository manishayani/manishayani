---
title: "Sprint 2"
type: portfolio
Date: 2020-01-22T16:54:54+06:00
description : "This is meta description"
caption: Reflection
image: images/blog/week-2.jpeg
Category: ["reflection","sprint 2"]
submitDate: 03 February, 2020
Location: UTS
---
### INTRODUCTION

Week 2 of the Summer Studio was quite intense, as it was off on Monday where classes are usually held on, but due to a public holiday, it was held on Tuesday. The session began with standup meeting, where everyone spoke about what they feel about summer studio and what are their goals for this week, etc. I also spoke about not liking the Hugo and markdown language and the reason for not using markup language instead of markdown language. To which Jason clarified later on that markdown language is a type of markup language (getting me puzzled again) and any language can be used for the creation of website. The tutor is just concerned about the Content in it.

## Group Formation
The tutor asked us to form a group of 3 or 4 for a presentation to give on Thursday. This is a part which I hate. I find it very uncomfortable to talk to people for forming groups. Luckily, I formed a group with the students sitting right next to me. The Next task was to find a suitable reconnaissance tool to present on. At that moment, I even didn't know what reconnaissance tools are. A quick google search gave me all the details needed. Tools that are used to collect data about a target device are termed as Reconnaissance tools. So, all four of us began searching for the appropriate tool. After a few minutes we decided on Nmap or Nessus, but unfortunately, both these tools were taken or had a hefty cost so ultimately, we finalized on Nikto Vulnerability Scanner.

![Collaboration](/images/blog/collab.PNG)

Then we began the discussion on dividing the workload among the group, and everyone chose a pointer to research and present. We created our private group on Microsoft teams and created a shared google doc and ppt. We decided on a deadline by 6 pm on Wednesday.


## Pen testing Methodology
The tutors explained to us about the cycle of Pen testing Methodology which involves Information Gathering, Footprint & Scanning, Vulnerability assessment, Exploitation and Finally Reporting. Larry and Jason explained to us how the cycle works and each step is to be carried out. The duration and mode of the cycle differ from project to project and from company to company. For Information gathering, there are multiple tools available including Google Search (known as Google Dorks). The list includes Nmap, RedHawk, Raccoon etc. These tools are also called Reconnaissance Tools.

The second step, footprint & Scanning involves automated scans on data collected during the previous stage. The next step is documenting, and analysis of the vulnerabilities found in the previous stage. The fourth stage is Exploitation which involves testing the vulnerability if it's actually exploitable such as (Buffer Overflow, Dirty COW, SQL injection etc). The Last stage is intended to document all the findings and generate a clear, concise report with pieces of evidence to be presented to the stakeholders.

## Insights from the talk with Patrick Kelso
After having a great talk with Patrick Kelso, a part of UTS IT Security Team, I realized that having a good grasp on Linux commands is very important to get going in the industry. I had learned Linux commands during my bachelors but I needed a lot of polishing yet. I started rebuilding on my Linux commands and scripting skills. This is something I wish to carry out on a regular basis.

![Linux Email](/images/blog/linux_email.PNG)

One of the suggestions that Patrick gave for improving an industrial presence is by having a linux.com email address. He asserted that during the start of his career, he got multiple job offers just because he had a linux.com email address. This is something I found very interesting, so I went looking into it. I found that to get a linux.com email address you just need to contribute $50 USD to linuxfoundation.com and the benefits are great. So, I am planning to get my own linux.com email address very soon.

## Insights from the talk with Robert Mitchell
After lunch, we had a great talk from Rob Mitchell, who is currently working with GitLab. He gave a presentation on Social Engineering and History of IT Security. I liked the fact that even after graduating in Analytic Philosophy, he worked hard and got himself into the IT security industry. This implies that having a passion for something can take you places. 
Robert also gave his opinion on the next big thing in IT. According to him, the next big thing would be IoT because these devices are full of data with very minimal processing power and no security at all. He even gave his views on the value of certification in Industry. He asserted certification is a good starting point but not a prerequisite. There are ways in which one could get a job without certificates. One of them being through efficient Networking.

He went on to tell us about how hectic things become in the industry when there is an emergency. He said that there have been times when he was at the office for around 16 hours when they got information about a threat they might face before the launch of the product.

## Challenges Faced
For this week, I encountered a series of problems, first being the presentation itself. I am not very comfortable in working with groups, I like working independently but I know that it is not possible all the time. Especially in the industry, I am looking forward to pursuing my career in. Thus, I took it as another learning opportunity and a way to prepare myself for future roles.

![Collaboration Problem](/images/blog/collab_problem.PNG)

Secondly, we were expected to have Kali Linux installed on our systems by then. The requirement was to have it installed in any virtualisation software such as Vmware, Virtualbox etc. But I am not a big fan of virtualisation software and instead prefer to dual boot my system. I have set up dual-booting multiple times already. In a year I try 7-8 different Linux distros. It is one of my favourite hobbies to try different platforms and explore their strengths and weaknesses. Even though I had dual-booted Kali-Windows before, this time it wasn't working out. And I had little idea of what was wrong. First, the installation got stuck on 'configuring the device'. After googling the issue, I found that I needed to make it into a DD image instead of ISO image.

![Kali Bootable Disk 1](/images/blog/kali_bootable.png)
![Kali Bootable Disk 2](/images/blog/kali_bootable2.png)

Then after everything seemed fine, I got stuck on 'configuring the network' window. I waited for some time, but it became clear that something was wrong. I went back to my best friend (Google :>) to look for the issue but didn't find anything to help. I waited for the next class so as to ask the tutor if they could help me to deal with this issue. Funnily enough, when I started the installation with the tutor, there was no network problem and it worked as expected (a moment of embarrassment in my head). A little brainstorming later I came to the conclusion that there might be a problem with my Wi-Fi at home.

![Network Configure Problem](/images/blog/configure_network.jpeg)

So now that everything seemed okay, one last thing that was remaining was installing Nvidia GPU drivers to enhance speed and support CUDA. I searched Google for the installation guide, and without looking at the source, I opened the first link that appeared (a rookie mistake). I followed the full guide that included typing some commands on to the terminal without even realising that I tampered the booting files the last command was to reboot the system, and that's where it all went haywire. The system restarted and loaded a couple of startup programs and then got stuck on 'Resuming from Hibernation'. I wasted the entire Thursday class resolving this issue. One of the tutors, Jason suggested me to leave it as Nvidia is proprietary software and Kali is open source that does not go hand in hand. But I am a little stubborn and kept on trying. Eventually, after wasting the entire Thursday, I decided to drop it.

![Resuming From Hibernation](/images/blog/resume_hibernation.png)

## How do I plan to resolve these issues?
Collaboration is my Achilles' heel, but I have realized that in order to take a career path in Cybersecurity, teamwork is a skill of utmost importance and I needed to work on it. So from now on I will try to actively participate in group activities and be more open to ideas from other teammates. Stepping out of my comfort zone is the first move towards this goal.
I also need to get my time management skills in order. And for that, I will assess the importance of the task that I am doing and prioritizing them. If a task is of great importance then spending more time on it is acceptable but if the task is of less importance, then a lot of time on it is something I should avoid. Reprioritizing is likely to enhance my productivity and save me from pointless fatigue.

## Goals for the next week
1. Prepare fully for the content of the class and try not to deviate from the tasks allocated
2. Optimising Time Management skills
3. More Collaborations with the others
4. Active Participating in the class

## Achieving the SLOs

## 1. Engage with stakeholders to identify a problem or scope a defined problem.

This week we had two speakers from the industry, I got a chance to converse with them after their talk and gained valuable insights with their views on the problems and industry scenario.

## 2. Apply design and systems thinking to respond to a defined or newly identified problem.

Our presentation highlighted the characteristics and use-case scenarios of 'Nikto' as a popular industrial vulnerability scanner. Our presentation demonstrated how Nikto can be used to gather information about a vulnerability and the usefulness of that information in determining the extent and scope of the attack.
Design thinking conveys that people would prefer to take steps to safeguard from data theft. Nikto as a tool steps into scan web servers for dangerous files/CGIs, outdated server software and other problems that may shape up an attack. The need for patched software is highlighted by it.

## 3. Apply technical skills to develop, model and/or evaluate designs.

When our team started reading about Nikto, one of the first things that we understood was the need to get familiar with Perl and Linux commands. Once the prerequisites are in order using the tool is a fairly easy task.
Using it in a sandbox environment explained how such a small command can be used to gather crucial information like server name, user/command privileges etc. Some tinkering with this data and it was clear that these details are highly valuable for someone who is looking to exploit.
This was perhaps the most fun SLO for this week. A lot of opportunities to discover new things and try tools practically.

## 4. Demonstrate effective collaboration and communication skills.

I tried to communicate effectively for the group presentation this week. We started our own group chat on Microsoft Teams and also divided the work. Each member contributed equally and there was no conflict of Interests. We even set a deadline for the work and everybody was expected to complete it by then. Later, I took the initiative to make presentation slides with all the content provided by teammates. With everyone's inputs and suggestions, the presentation was easily completed.
I learnt effective Collaboration and Communication make a task so much easier and better to complete. Just because of proper coordination amongst the team, everyone had a positive feeling about completing the presentation by giving in their 100%. In turn, also learning what everyone had discovered while completing their individual tasks.

## 5. Conduct critical self, peer, and group review and performance evaluation.

a. As a part of self-review, I feel that I am getting more information about the industry, clearing my mind as to what field in cybersecurity I want to head into. Also, I need to improve my bash scripting skills in order and do a little more of networking than what I am doing right now.

b. The tutors also provided me with feedback. They said that the website design was good, the expectation part was also good, but the only thing lacking was a proper reflection. My Reflection was too short and that is why it was below par, as a result, I do not pass for week 1. So improving on that I am putting my heart out and making my reflection as informative this week as I can.