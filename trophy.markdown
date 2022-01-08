---
layout: page
title: Trophies
permalink: /trophies/
---

To defend any kind of ecosystem it is necessary to know how an attacker would approach software bugs and misconfigurations to gain access to systems. There are different Online Services that offer environments for White Hat Hackers to practise these skills in a save (legal) environment without harming anyone.  
Below you can find some of the machines I did to practise "hacking" with a short description. For some of them I have done a writeup (short walkthrough), you can find these in my blog posts or cross linked within the descriptions below.  
Furthermore bug bounty programs are an excellant place to further practise the skill of hacking in a real world setting. If possible I will list my disclosed bug bounties down below too.  

------  
  
To analyze and consult businesses and people in terms of security it is necessary to be able to understand and think like an attacker - to create a reasonable defense strategy you have to master attacking. A very fitting quote in this regard is the following:  
  
> "Attack is the secret of defence; defence is the planning of an attack"  
*Chun Yu's comment on Sun Tsu's ART of WAR (3/18)*

### [Hack The Box](https://www.hackthebox.eu/)  

I just started to do HTB active machines as part of a new habit of mine. Every day I will work on HTB for the next month and display my progress and my throughts in regard to the boxes I have done. My goal is to move from the EASY machines bit by bit towards INSANE.  

> Current Rank: NOOB and 66,6% towards Script Kiddie
> Ownership: 3,33% of HTB pwned

#### Optimum - easy
This machine was very straight forward. After finding the public available CVE vulnerability and a slight modification of the available exploit it was possible to gain access as a low privileged user to the machine. The privilege escalation phase was a litte harder but it was only a matter of the right tool. 
This is an easy and well put together Windows based machine where all phases of a penetration test can be practised.  

Tools used:  
- [searchsploit](https://www.exploit-db.com/searchsploit)
- [AutoRecon](https://github.com/Tib3rius/AutoRecon)
- [WinPEAS](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS)
- [wesng](https://github.com/bitsadmin/wesng)
- [Sherlock](https://github.com/rasta-mouse/Sherlock)
- diverse UNIX CLI tools

#### Previse - easy
With some fiddeling around with the  website and HTTP status codes I was able to create myself a user. This took me some time because I was thinking to complicated. 
Note for my future self: Think simple 
After finding an information disclosure I was able to retreive a DB account and was able to detect a flaw in how the PHP code handles a function. This lead to a manual exploitable RCE. After abusing the RCE to get a service level reverse shell a little research on the system  with the already disclosed information and password cracking gave me user access via ssh. Finally, enumeration showed me the $PATH to gain full admin level access to the machine.

Tools used:
- [AutoRecon](https://github.com/Tib3rius/AutoRecon)
- [Burp Suite Community Edition] (https://portswigger.net/burp/communitydownload)
- [hashcat] (https://hashcat.net/hashcat/)
- diverse UNIX CLI tools

<style>
.footer-heading {
  display: none;
}
</style>
