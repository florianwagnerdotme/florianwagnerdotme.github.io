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
  
*"Attack is the secret of defence; defence is the planning of an attack"*  
*- Chun Yu's comment on Sun Tsu's ART of WAR (3/18)*

### [Hack The Box](https://www.hackthebox.eu/)  
#### Optimum - easy
This machine was very straight forward. After finding the public available CVE vulnerability and a slight modification of the available exploit it was possible to gain access as a low privileged user to the machine. The privilege escalation phase was a litte harder but it was only a matter of the right tool. 
This is an easy and well put together Windows based machine where all phases of a penetration test can be practised.  
Tools used:  
- [searchsploit](https://www.exploit-db.com/searchsploit)
- [AutoRecon](https://github.com/Tib3rius/AutoRecon)
- [WinPEAS](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS)
- [wesng](https://github.com/bitsadmin/wesng)
- [Sherlock](https://github.com/rasta-mouse/Sherlock)

<style>
.footer-heading {
  display: none;
}
</style>