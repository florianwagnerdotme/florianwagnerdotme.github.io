---
layout: post
title:  "Hacking Mobile Apps - easier done than said!"
date:   2021-10-15 12:00:00 +0200
categories: mobile app hacking
---
With people spending a [larger percentage][timeSpentOnline] of their time on their mobile phones than they do on their desktop/laptop there is an increasing market for hackers to steal data, surveil people, compromise bank accounts and many more threats. Millions of new app releases within Apple's App Store and Google's Play Store occur every day, which will impact mobile devices of businesses and casual users alike. While businesses attempt to deal with these issues by using a so called [Mobile Device Management][mdm] system to deploy endpoint security mechanisms to protect against these threats on their devices, people like you and me (at least privately) are dependent on the security patches of mostly Apple, Google and the developers of the mobile apps we use.       
I would say it is far more likely that you get digitally robbed by some hackers than being robbed physically on the street. In most cases it is easier too. It can happen everywhere and at any time. Especially if you are [using Apple Pay][applePayRobbery] with a VISA card right now. ;-)  
But, why is that so?  
Well, today everything has to be online, quickly available and easy to use with the tiny computers that we are carrying around every day, everywhere we go **PERIOD** - if it makes sense or not. I would rather like to have some of the following security features than some apps out there, what do you think :-) ? 
  
![phone security by XKCD]({{ site.url }}/assets/phone_security.png){: .center-image}

[from XKCD](https://xkcd.com/1934/) - CC BY-NC 2.5, 04/10/21  

# About Mobile App Security and Data Privacy

Out of my experience, the current overall security and data privacy state of iOS and Android Apps is disappointing. If you look into apps for a couple of hours you will often see insecure communication and cookies, leaked authorization data, outdated library usage and privacy violation issues.  
Most of these problems could be addressed already during the initial management phases and planned out as a "security by design" paradigm.
Then, if you go for a deep dive into network and dynamic analysis of the app you will find even scarier things lurking in the deep which are either listed within the [OWASP Mobile Top 10][mobileTop10] or the [OWASP Web Top 10][webTop10] security vulnerabilities. The reason why there are mostly web vulnerabilities found is that most apps make use of Web Views which are available for both [iOS][webViewiOS] and [Android][webViewAndroid]. They make a cross platform development for apps easier with the negative effect that an improper configuration of them can lead to severe security vulnerabilities due to web vulnerabilities. 
Furthermore, most mobile apps rely on user tracking to make money which is, out of a business point of view, ok, **but** from my point of view they must always:
1. Inform the user before gathering the user's behaviour to make money.
2. Never violate any local applicable law, like GDPR in Europe.
3. At best give the user an option to opt out the tracking when the user first opens the app.

In conclusion, for our society mobile security is one of the most important fields of security that is out there. Security flaws in standards and vulnelrabilities in software are impacting everyone, from businesses to private people. The "security by design" paradigm should be followed and used as early in the planning phase of an app as possible.  

# “Education is the key to unlock the golden door of freedom.” 
> George Washington Carver

I have spent the last 6 years dealing with security issues surrounding mobile devices, mobile operating systems and their mobile apps. Within the last year I did a deep dive into the practise of hacking these mobile device's, apps and features to find security issues and report them to contribute to the mobile security field.  

While Apple, Goggle and most developers try to keep up to date with the webb and flow of security issues along with their fixes, there is still a lot to do to keep hackers from abusing their power for evil purposes.  
Because all help in my field of expertise is welcome and needed, I will soon publish open source tools and articles on how to start with the mobile hacking of apps and the identification of security issues within mobile devices. Like in George Washington Carver's quote, knowledge and continuous education will give freedom to those who seek it.   
While freedom is objective please keep care, once you start down the dark path it will forever dominate your destiny. Choose the right one and contribute to the security of everyone.
 
---
Thank you very much for reading my first article and feel free to tell me if you agree or disagree. Subscribe and share!
  
All the best,  
Florian

[webViewAndroid]: https://developer.android.com/guide/webapps/webview
[webViewiOS]: https://developer.apple.com/design/human-interface-guidelines/ios/views/web-views/
[mobileTop10]: https://owasp.org/www-project-mobile-top-10/
[webTop10]: https://owasp.org/www-project-top-ten/       
[mdm]: https://en.wikipedia.org/wiki/Mobile_device_management
[timeSpentOnline]: https://www.statista.com/statistics/319732/daily-time-spent-online-device/
[applePayRobbery]: https://thehackernews.com/2021/10/apple-pay-can-be-abused-to-make.html

<style>
.center-image
{
    margin: 0 auto;
    display: block;
}
</style>
