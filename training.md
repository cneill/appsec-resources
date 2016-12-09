# Learning Application Security 

## Introduction

Some of the oldest known application security issues continue to affect projects
today. Being aware of these issues, as well as techniques for exploiting and
mitigating them, will aid in your testing efforts and help you to avoid
vulnerabilities in your own code. The resources below should help you learn more
about common security issues, and how to prevent these issues from surfacing in
new products/product features.

Some links and sections have :star:s next to them to denote what I consider to
be *essential* knowledge for understanding application security.

## Table of Contents

0. [OWASP Top 10](#star-owasp-top-10)
0. [Security guides and overviews](#security-guides-and-overviews)
0. [AppSec topics](#appsec-topics)
0. [AppSec presentations](#appsec-presentations)
0. [Interesting case studies](#interesting-case-studies)
0. [Test your skills](#test-your-skills)
0. [Stay up to date](#stay-up-to-date)
0. [Useful references](#useful-references)

## :star: OWASP Top 10

The [OWASP Top 10](https://www.owasp.org/index.php/Top_10_2013-Top_10) is a list
of common vulnerabilities, as assessed by [OWASP, the Open Web Application Security Project.](https://www.owasp.org/index.php/Main_Page)
It is re-evaluated periodically based on the findings that they see in the wild.
OWASP's wiki has some very helpful articles about testing for and fixing many
common security issues.

Understanding the basics of each of these is essential to any security engineer.

The top 10 issues for 2013 are:

1. **[Injection (such as SQL or LDAP injection)](https://www.owasp.org/index.php/Top_10_2013-A1-Injection)**
2. **[Broken authentication and session management](https://www.owasp.org/index.php/Top_10_2013-A2-Broken_Authentication_and_Session_Management)**
3. **[Cross-site scripting](https://www.owasp.org/index.php/Top_10_2013-A3-Cross-Site_Scripting_%28XSS%29)**
4. **[Insecure direct object references](https://www.owasp.org/index.php/Top_10_2013-A4-Insecure_Direct_Object_References)**
5. **[Security misconfiguration](https://www.owasp.org/index.php/Top_10_2013-A5-Security_Misconfiguration)**
6. **[Sensitive data exposure](https://www.owasp.org/index.php/Top_10_2013-A6-Sensitive_Data_Exposure)**
7. **[Missing function level access control](https://www.owasp.org/index.php/Top_10_2013-A7-Missing_Function_Level_Access_Control)**
8. **[Cross-site request forgery](https://www.owasp.org/index.php/Top_10_2013-A8-Cross-Site_Request_Forgery_%28CSRF%29)**
9. **[Using components with known vulnerabilities](https://www.owasp.org/index.php/Top_10_2013-A9-Using_Components_with_Known_Vulnerabilities)**
10. **[Unvalidated redirects and forwards](https://www.owasp.org/index.php/Top_10_2013-A10-Unvalidated_Redirects_and_Forwards)**

#### Cheat Sheets

- [Cross Site Scripting Prevention Cheat Sheet](https://www.owasp.org/index.php/XSS_%28Cross_Site_Scripting%29_Prevention_Cheat_Sheet) -
    Describes methods for detecting and preventing [Cross-site scripting](http://en.wikipedia.org/wiki/Cross-site_scripting) in webapps.
- [SQL Injection Prevention Cheat Sheet](https://www.owasp.org/index.php/SQL_Injection_Prevention_Cheat_Sheet) - Describes methods for detecting and preventing [SQL injection](http://en.wikipedia.org/wiki/SQL_injection) in webapps.
- [HTML5 Security Cheat Sheet](https://www.owasp.org/index.php/HTML5_Security_Cheat_Sheet) - Security considerations for HTML5 apps
- [REST Security Cheat Sheet](https://www.owasp.org/index.php/REST_Security_Cheat_Sheet) - Security considerations for REST APIs
- [Google Application Security - Cross-Site Scripting](https://www.google.com/about/appsecurity/learning/xss/) - Guide explaining how to test for and prevent XSS, from Google

## Security Guides and Overviews

- [The Basics of Web Application Security](http://martinfowler.com/articles/web-security-basics.html) - Blog post describing some of the more common issues in web application security (e.g. XSS, SQL injection...)
- [2016 Guide to User Data Security](https://www.inversoft.com/guides/2016-guide-to-user-data-security) - This is an in-depth guide to setting up cloud-based apps in a secure way. It covers how to securely configure cloud services/users/etc., set up infrastructure, and avoid introducing vulnerabilities through programming errors, at a high level.
- [Security Guide for Developers](https://github.com/FallibleInc/security-guide-for-developers) - A work-in-progress project to document security best practices for a developer audience. Includes a very handy [security checklist](https://github.com/FallibleInc/security-guide-for-developers/blob/master/security-checklist.md) for secure applications.
- [Introduction to Microsoft Secure Development Lifecycle](http://download.microsoft.com/download/9/3/5/935520EC-D9E2-413E-BEA7-0B865A79B18C/Introduction%20to%20the%20Microsoft%20Security%20Development%20Lifecycle%20%28SDL%29.ppsx) - A great introductory slideshow describing Microsoft's method of doing secure software development. We borrow heavily from this model on the Rackspace Security Engineering team, conducting threat modeling sessions with all new products to understand the system-level interactions and the "trust boundaries" that exist between systems, for example.

## AppSec Topics

### The Basics

- :star: [Ten Immutable Laws of Security](https://blogs.technet.microsoft.com/rhalbheer/2011/06/16/ten-immutable-laws-of-security-version-2-0/) - High-level security principles to keep in mind.

### Web servers / Browsers

- [Exotic HTTP Headers](https://peteris.rocks/blog/exotic-http-headers/) - This lists most of the common HTTP headers that are used by web applications to ensure security from the browser perspective.


### Handling User Passwords

- [Password Hashing: Why and How](http://ithare.com/password-hashing-why-and-how/) - This is a high-level overview of how and why to use well-tested approaches to password storage. More of a philosophical than technical talk. Read this one, then the one below.
- [How to Safely Store Your Users' Passwords in 2016](https://paragonie.com/blog/2016/02/how-safely-store-password-in-2016) - Solid implementation of current best-practice password hashing in several languages. Very specific (i.e. mostly "how", not much "why")

### Operations

- [Choosing Secure Passwords](https://www.schneier.com/blog/archives/2014/03/choosing_secure_1.html) - Guide on how to think about choosing secure passwords from Bruce Schneier.
- [HowTo: Privacy & Security Conscious Browsing](https://gist.github.com/atcuno/3425484ac5cce5298932) - Tips for how to safely configure your browser to avoid unnecessary exposure to security issues.
- [A Week with a Rails Security Strategy](http://bauland42.com/articles/a-week-with-a-rails-security-strategy/) - A short guide to creating a daily practice of maintaining your application security posture.
- [Secure Secure Shell](https://stribika.github.io/2015/01/04/secure-secure-shell.html) - A guide to tightening security in OpenSSH

### Cryptography

- :star: [The Cryptographic Doom Principle](https://moxie.org/blog/the-cryptographic-doom-principle/) - A short must-read for anyone implementing or auditing crypto systems
- [crypto101.io](https://www.crypto101.io/) - Overview of the building blocks of cryptography - cryptographic hash/MAC algorithms, popular ciphers, SSL/TLS, and much more.
- [The First Few Milliseconds of an HTTPS Connection](http://www.moserware.com/2009/06/first-few-milliseconds-of-https.html) - In-depth details about how TLS works as a protocol

## AppSec Presentations

### Slide Deck Presentations

- [**(ADVANCED)** Giant bags of mostly water](http://slides.com/mricon/giant-bags-of-mostly-water) - This presentation hits on a lot of high-level changes that security organizations need to invest in to make user-error less likely in their organizations. More of a philosophical presentation than a technical one.

### Video Presentations

#### DEFCON
- [DEFCON 24 Presentations](https://www.youtube.com/playlist?list=PL9fPq3eQfaaAvXV3hJc4yHuNxoviVckoE) (2016)
- [DEFCON 23 Presentations](https://www.youtube.com/playlist?list=PL9fPq3eQfaaBuHqVvDzPoWxznYYmyx5UX) (2015)
- [DEFCON 22 Presentations](https://www.youtube.com/playlist?list=PL9fPq3eQfaaBCdjbKFYjosh1s1EkaYdsQ) (2014)

#### Black Hat
- [Black Hat USA 2016 Videos](https://www.youtube.com/playlist?list=PLH15HpR5qRsXm0-rMacuWBxWcB2fmsmEw)
- [Black Hat USA 2015 Videos](https://www.youtube.com/playlist?list=PLH15HpR5qRsXF78lrpWP2JKpPJs_AFnD7)
- [Black Hat USA 2014 Videos](https://www.youtube.com/playlist?list=PLH15HpR5qRsUBgeytB_T4xnKzr4Iv3upj)

#### AppSec USA
- [AppSec USA 2016 Presentations](https://www.youtube.com/playlist?list=PLpr-xdpM8wG8DPozMmcbwBjFn15RtC75N)
- [AppSec USA 2015 Presentations](https://www.youtube.com/playlist?list=PLpr-xdpM8wG93dG_L9QKs0W1cD-esQEzU)
- [AppSec USA 2014 Presentations](https://www.youtube.com/playlist?list=PLpr-xdpM8wG8jz9QpzQeLeB0914Ysq-Cl)

## Interesting Case Studies

- [**(XSS)** OX (Guard): Stored Cross-Site Scripting via Email Attachment](https://hackerone.com/reports/165275) - An interesting XSS and CSP bypass vulnerability in an encrypted email service.
- [**(XSS)** AddToAny Share Buttons WordPress Plugin DOM-Based XSS](https://inventropy.us/blog/addtoany-share-buttons-wordpress-plugin-dom-based-xss) - A walk-through (by yours truly) about tracing down a DOM-based cross-site scripting issue in a WordPress plugin.
- [**(CRLF)** blog.trello.com CRLF Injection](https://hackerone.com/reports/45514) - Example of header injection by adding a CRLF to the `Location` header
- [**(SSRF)** Blind SSRF on synthetics.newrelic.com](https://hackerone.com/reports/141304) - This shows how server-side request forgery can be used to retrieve e.g. AWS instance metadata
- [**(AuthN/AuthZ)** How to steal $2,999.99 in less than 2 minutes with Venmo and Siri](http://www.martinvigo.com/steal-2999-99-minute-venmo-siri/) - An example of a vulnerability resulting from several features interacting that weren't intended (or known) to interact, because they were in components made by two different companies (Apple's iOS and Venmo, a money-charging service that uses SMS)
- [**(Sessions/Crypto)** Anatomy of a Crypto Vulnerability](https://alexgaynor.net/2016/mar/14/anatomy-of-a-crypto-vulnerability/) - A walk-through describing cryptographic weaknesses in a Python session-management framework.
- [**(Sessions/Crypto/Mobile/IDOR/AuthN)** The Bank Job](https://boris.in/blog/2016/the-bank-job/) - A walk-through of multiple security issues in a bank's online banking services, including insecure SSL/TLS, insecure session management, and indirect object reference.
- [**(Crypto)** A Tale of Lost Entropy](https://inventropy.us/blog/a-tale-of-lost-entropy) - A walk-through (by yours truly) discussing a weak Node.JS cryptography implementation

## Test Your Skills

- [**(XSS)** Google XSS Game](https://xss-game.appspot.com/) - An introduction to finding XSS vulnerabilities
- [**(XSS)** Escape](http://escape.alf.nu/) - Much more in-depth examples than above, organized like a game where the objective is finding the shortest "exploit" that pops up an alert box
- [**(ALL)** Google Gruyere](https://google-gruyere.appspot.com/) - A "lab" to test your skills finding a number of different vulnerabilities. Get started [here](https://google-gruyere.appspot.com/part1).
- [**(ALL)** Hack This Site](https://www.hackthissite.org/) - Site with all kinds of "wargames" for testing your hacking skills, and tutorials about security concepts
- [**(ALL)** Over The Wire Wargames](http://overthewire.org/wargames/) - Very in-depth "wargames" for learning different aspects of security and testing your skills
- [**(ALL)** OWASP WebGoat](https://www.owasp.org/index.php/Category:OWASP_WebGoat_Project) - This is a Java/.NET web app that has been deliberately implemented with multiple security vulnerabilities. Can you find/patch them all?
- [**(SQLi)** CodeBashing SQL Injection Demo](https://www.codebashing.com/sql_demo)
- [**(PROGRAMMING)** Stockfighter.io](https://www.stockfighter.io/) - Programming challenges related to security and stock trading.

## Stay up-to-date

### News Sites & Blogs
- [/r/netsec](https://www.reddit.com/r/netsec/) - Subreddit with news relevant to network security, application security, etc.
- [Hacker News](https://news.ycombinator.com/) - News relevant to startups, technology, programming, and sometimes security
- [Sustainable Application Security](https://blog.secodis.com/) - Blog covering the intersection of security and ops/devops.

### Mailing Lists
- [OSS-Sec](http://seclists.org/oss-sec/) - Open-source Software Security list with vulnerability announcements, CVE requests, and new research (more popular than FD these days)
- [Full Disclosure](http://seclists.org/fulldisclosure/) - Vulnerability announcements, CVE requests, new research
- [Websec Weekly](https://websecweekly.org/) - Roundup of interesting vulnerability reports from HackerOne and popular discussions on /r/netsec
- [Apple Product Security](https://lists.apple.com/mailman/listinfo/security-announce/) - Apple's list for announcing security vulnerabilities/updates

## Useful References

### Lists-of-lists

- [Troy Hunt's ultimate list of security links](https://www.troyhunt.com/troys-ultimate-list-of-security-links/?m=1) - List of relevant security links from a well-known security researcher at Microsoft.
- [j.haddix's Pentesting bookmarks](https://github.com/jhaddix/pentest-bookmarks/blob/master/wiki/BookmarksList.wiki) - Lengthy list of bookmarks in various application security categories. No descriptions on the individual links :persevere:

### Further Training Resources

**Free**
- [Cyber Security Base](https://cybersecuritybase.github.io/) - A course created by F-Security and the University of Helsinki to teach security skills.
- [Hacksplaining](https://www.hacksplaining.com/) - An immersive walk-through of numerous security issues, with animations and examples.

**Paid**
- [Coursera Cybersecurity Course](https://www.coursera.org/specialization/cybersecurity/7?utm_medium=courseDescripTop) - If you find that cybersecurity is interesting to you, Coursera offers a certificate program that covers several broad topics in cybersecurity like software security, hardware security, and cryptography.
- [CodeBashing](https://www.codebashing.com/) - Application security training for teams / businesses

### Books

- [The Web Application Hacker's Handbook](https://www.amazon.com/Web-Application-Hackers-Handbook-Exploiting/dp/1118026470) by Dafydd Stuttard and Marcus Pinto
- [The Tangled Web](https://www.amazon.com/Tangled-Web-Securing-Modern-Applications/dp/1593273886) by Michal Zalewski

### Miscellaneous

- [List of naughty strings](https://github.com/minimaxir/big-list-of-naughty-strings) - A list of strings that can cause various issues - unicode decode errors, spam/profanity filter triggers, XSS, memory exhaustion, etc.
