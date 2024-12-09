---
layout: post
title:  "Kris Krypto, Burp Sweet, and the Anthem Conspiracy"
post-image: "https://florianwagner.me/assets/images/KrisAndBurpSweet.jpg"
description: A humorous yet sharp look into the misadventures of a pet store worker by day, hacker at night and his burping pet, uncovering corporate evil at the company next door.
tags: 
- hacking story
- cybersecurity
- Kris Krypto
- cyber thrillers
---

By day, Kris Krypto was an unassuming guy living in the corner apartment of a 25th-story building. He nodded politely in the hallways, avoided small talk, and quietly worked his shifts at a pet store around the block. By night, Kris transformed into a sarcastic digital phantom, uncovering secrets others worked tirelessly to bury — or at least wished to. His trusty companion was **Burp Sweet**, a peculiar dog with a perpetually drooling tongue that couldn’t stay in his mouth and a habit of burping at all the wrong moments, tastefully named after his favorite tool.

"Burp," Kris said as he booted up his multi-monitor rig, "tonight we’re taking on Anthem Technologies."  
Burp Sweet, perched on a pile of discarded hoodies, blinked lazily, his long tongue flopping sideways in a gesture of approval.

# Act 1: The First Breach

Kris began with reconnaissance. A quick **Nmap** scan illuminated the usual suspects: **Port 80** for their website and **Port 3389** for RDP.

"Port 3389? You might as well hang a ‘Hack Me’ sign on your front door," Kris muttered, shaking his head. Burp Sweet burped softly from his hoodie throne, providing moral support in his own unique way.

Switching to **Burp Suite**, Kris intercepted the company’s web traffic. Within minutes, he found their `robots.txt` file.  
"Ah, the infamous `robots.txt`—the digital equivalent of saying, ‘Please don’t look here.’ What fail awaits me now?" Kris opened the file and promptly let out a mocking gasp. "A password? WTF?! Anthem, why? but thanks, we should always be greatful for the little things in life."  
Burp Sweet yawned in apparent boredom, unimpressed by the company’s security posture.

# Act 2: Cracking the CMS

A quick **ffuf** scan revealed a promising endpoint: `/umbraco`.  
"Umbraco CMS," Kris said, typing furiously. "Fantastic choice if you’re aiming for the kind of security held together with duct tape and a hope."

He guessed the administrator’s email—**SG@anthem.com**—thanks to some casual LinkedIn recon on Simon Gärtner, Anthem’s overconfident IT admin, who had bragged online about the tech stack he managed and accidentally disclosed information. Paired with the password from `robots.txt`, the CMS dashboard loaded instantly.  
"Ka-ching! Welcome to the admin panel," Kris said, spreading his arms theatrically. From his hoodie throne, Burp Sweet let out a low burp, as if punctuating Kris’s sarcasm.

# Act 3: Digging for Dirt

Kris poked around the CMS for anything juicy. It didn’t take long to find a folder labeled **Project Anthemis**. Inside were encrypted memos. With practiced ease, Kris cracked the non-standard encryption algorithm and uncovered Anthem’s dirty secret: plans to sell fake security solutions while secretly harvesting client data.

"Wow, Anthem," Kris said, scrolling through the files. "You’re not just bad at security—you’re *profiting* off it. That’s almost... artistic in its villainy. Chapeau."  
Burp Sweet hopped down from his hoodie throne and plodded over to Kris’s desk, resting his head on Kris’s lap. Kris scratched the dog’s ears absently.  
"What do you think, Burp? Classic corporate evil, isn´t it?"  
Burp Sweet responded with a soft burp, which Kris took as agreement.

# Act 4: The Mid-Level Breach

Using the credentials he’d gathered, Kris initiated a remote desktop connection via **Port 3389**. The desktop of a mid-level IT employee appeared on his screen.

"First public facing RDP open, then no 2FA? Really? It’s like they want me here," Kris muttered, digging through the employee’s files.  

Eventually, he found a folder labeled **Executive Session Notes**. Inside was a document outlining Anthem’s plan to falsify safety certifications for a network security product riddled with vulnerabilities.  
"Perfect. Selling Swiss cheese and calling it a fortress. Classic corporate playbook," Kris said, saving the files to his encrypted drive.  
Burp Sweet had settled at Kris’s feet, snuggling close for warmth. Kris glanced down, smirking. "Thanks for the support, buddy. I can´t understand why anyone wanted to get rid of you."

# Act 5: Climbing Higher

Kris needed access to the executive archives. Poking around further, he found a locked folder: `C:\backup\restore.txt`.  
"Oh no, a locked file. Whatever shall I do?" Kris said mockingly as he adjusted the permissions, added himself and opened it. Inside was a password: **ChangeMeBaby1MoreTime**.  
Kris stared at the screen, then burst out laughing. "That’s the actual admin password? Who comes up with this stuff-a bored intern only listening to boybands all day long?"  
Burp Sweet, startled by Kris’s laughter, let out a loud, gurgling burp, wagging his tail.  
"Exactly, Burp," Kris said, grinning. "They’re a joke, and we’re the punchline."

# Act 6: The Smoking Gun

Armed with admin credentials, Kris logged back in as **Administrator**. The desktop was sparse but contained a single folder: **CONFIDENTIAL_other_budget**. Inside were financial records, emails, and contracts that painted a damning picture of Anthem’s operations.

The documents detailed money laundering schemes, bribes disguised as consulting fees, and funding for clandestine surveillance software designed to harvest user data under the guise of "enhancing security."  
"Wow, Anthem, you’ve outdone yourselves," Kris said, leaning back. "You’re not just breaking the law—you mess with it without regrets."  
Burp Sweet climbed onto Kris’s lap, his tongue hanging lazily as he let out one final triumphant burp.  
"Couldn’t have said it better myself," Kris said, saving the files.

# The Aftermath

As the first hints of dawn crept through the blinds, Kris powered down his rig. Next door, Anthem’s employees would soon shuffle into work, blissfully unaware of the storm about to crash down on them. Kris hadn’t yet decided whether to leak the information, sell it, or use it as leverage.  
"Decisions, decisions," Kris said, stretching. He glanced down at Burp Sweet, who was already snoring softly. "You’ve earned your rest, buddy. MVP - Most Valuable Pet - of the night."

Burp Sweet burped softly in his sleep, his tongue twitching slightly. Kris chuckled, giving the dog a pat before heading to bed.  
"Sweet dreams, Anthem. And maybe next time, don’t store your secrets behind a password that sounds like a rejected boy band lyric."

--------------------------------------

--> Based on TryHackMe's Anthem: [TryHackMeAnthem]


I hope you liked it!

All the best, 

FLOW


[TryHackMeAnthem]: https://tryhackme.com/r/room/anthem
