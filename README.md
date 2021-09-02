#KEA/Softwaresikkerhed 

# Softwaresikkerhed MOC

[Softwaresikkerhed](https://kompetence.kea.dk/kurser-fag/softwaresikkerhed) er en del af KEAs Diplomuddannelse i [[Diplom i IT-sikkerhed]]. 

## Oversigt over kursusgange

[[Kursusgang 0]] - **Welcome, goals and expectations Prepare Virtual Machines - bring laptop**

Create a good starting point for learning Introduce lecturer and students Concrete Expectations Prepare tools for the exercises

[[Kursusgang 1]] - **Lab setup and Programming Knowledge**

Do some initial programming

[[Kursusgang 3]] - **Initial Overview of Software Security**

Get an overview of the subject

[[Kursusgang 4]] - **SDLC and risk ranking**

[[Kursusgang 5]] - **Web Application Security: Recon**

[[Kursusgang 6]] - **Web Application Security: Recon and Offensive**

[[Kursusgang 7]] - **Hacking Web Applications: Offensive**

[[Kursusgang 8]] - **Software Programming & Memory Corruption**

[[Kursusgang 9]] - **Program Building blocks and exploitation**

[[Kursusgang 10]] - **Strings and Pointers**

[[Kursusgang 11]] - **Network Attacks Intro**

[[Kursusgang 12]] - **Fuzzing intro**

[[Kursusgang 13]] - **Security Design and Defense**

[[Kursusgang 14]] - **General questions and summary**

We will do a practice exam and talk about exam subjects.


---

## Goals[](#goals)

The module is centered around software security including software quality, software flaws, vulnerabilities, software APIs, error handling and software architecture.

Teaching material will primarily be English, but the teaching will be in Danish.

See more about the course in the official curriculum which can be downloaded from the main page [https://kompetence.kea.dk/uddannelser/it-digitalt/diplom-i-it-sikkerhed](https://kompetence.kea.dk/uddannelser/it-digitalt/diplom-i-it-sikkerhed)

-   near the top "Download studieordningen".
    

## Exam[](#exam)

Date 26/10 2021

## Teaching Methods[](#teaching-methods)

-   Lecture lessons
    
-   Group exercises and cases, including practical exercises with laptop
    

## Teaching dates - fall 2021[](#teaching-dates-fall-2021)

31/8, 2/9, 7/9, 9/9, 14/9, 16/9, 21/9, 23/9, 28/9, 30/10, 5/10, 7/10, 12/10, 14/10

Make sure to mark dates in your calendar - some weeks will have lessons tuesday/thursdays.

## Hardware[](#hardware)

Since we are going to be doing exercises, each team will need two virtual machines.

The following are two recommended models:

-   One based on Debian, running software servers and web applications
    
-   One based on Kali Linux, running attacks against software
    

Read more about these at [https://github.com/kramse/kramse-labs](https://github.com/kramse/kramse-labs)

## Course reading list[](#course-reading-list)

This course uses three books and a number of supporting resources.

Primary literature:

-   The Art of Software Security Testing Identifying Software Security Flaws,
    
    Chris Wysopal, 2006, ISBN: 9780321304865, named AoST or the Green Book
    
-   Web Application Security, Andrew Hoffman, 2020, ISBN: 9781492053118 called WAS below
    
-   Hacking, 2nd Edition: The Art of Exploitation, Jon Erickson, February 2008, ISBN-13: 9781593271442, called just hacking below
    

It is recommended to buy the _Pwning OWASP Juice Shop_ Official companion guide to the OWASP Juice Shop.

From [https://leanpub.com/juice-shop](https://leanpub.com/juice-shop) - suggested price USD 5.99

It is recommended to buy these books listed above.

### Supporting literature:

-   24 Deadly Sins of Software Security: Programming Flaws and How to Fix Them, Michael Howard, David LeBlanc, John Viega, ISBN: 9780071626750, 2010 The McGraw-Hill Companies, named 24-deadly below
    
	Additional software security problems, listed language agnostically and with small examples. Highly recommended for programmers.

-   Linux Basics for Hackers Getting Started with Networking, Scripting, and Security in Kali by OccupyTheWeb, December 2018, 248 pp. ISBN-13: 978-1-59327-855-7 - shortened LBfH
    
	This book introduces the Linux operating system commands, using Kali Linux as example. The tools presented include a lot of generic Unix tools. If you have no experience with Linux or Unix it is recommended to buy this book.

-   Kali Linux Revealed Mastering the Penetration Testing Distribution [https://www.kali.org/download-kali-linux-revealed-book/](https://www.kali.org/download-kali-linux-revealed-book/) - shortened KLR
    

We will also use the OWASP Juice Shop Tool Project as a running example. This is an application which is modern AND designed to have security flaws.

Read more about this project at [https://www.owasp.org/index.php/OWASP_Juice_Shop_Project](https://www.owasp.org/index.php/OWASP_Juice_Shop_Project) and [https://github.com/bkimminich/juice-shop](https://github.com/bkimminich/juice-shop)

### Supporting Internet resources

Also the course will use internet links and pages. These can be downloaded from the internet often for free and may be gathered by the instructor for easy download.

#### System Design and Architecture

-   [Security by Design Principles, OWASP](https://www.owasp.org/index.php/Security_by_Design_Principles)
    
-   Wikipedia article about Privacy by Design
    
    [Privacy by Design](https://en.wikipedia.org/wiki/Privacy_by_design)
    
-   This in danish summarizing the implications of General Data Protection Regulation (GDPR)
    
    [https://www.dubex.dk/aktuelt/nyheder/det-skal-du-vide-om-privacy-by-design-ny-vejledning](https://www.dubex.dk/aktuelt/nyheder/det-skal-du-vide-om-privacy-by-design-ny-vejledning)
    
-   Article recommends doing Privacy Impact Assessment (PIA) [https://itb.dk/persondataforordningen/privacy-by-design-default/](https://itb.dk/persondataforordningen/privacy-by-design-default/)
    
-   ENISA, EU security office, reports about Privacy by Design [Privacy and Data Protection by Design](https://www.enisa.europa.eu/publications/privacy-and-data-protection-by-design) and
    
    [Privacy by design in big data](https://www.enisa.europa.eu/publications/big-data-protection)
    

#### Control Hijacking Attacks

-   [Smashing The Stack For Fun And Profit](http://www.phrack.com/issues.html?issue=49&id=14#article), Aleph One
    
-   [Bypassing non-executable-stack during exploitation using return-to-libc](http://css.csail.mit.edu/6.858/2014/readings/return-to-libc.pdf)
    
    by c0ntex.
    
-   [Basic Integer Overflows](http://www.phrack.com/issues.html?issue=60&id=10#article) by blexim.
    
-   [Return-Oriented Programming:Systems, Languages, and Applications](https://hovav.net/ucsd/dist/rop.pdf)
    
    Ryan Roemer, Erik Buchanan, Hovav Shacam and Stefan Savage University of California, San Diego
    
-   [MITRE ATT&CK](https://attack.mitre.org/) a globally-accessible knowledge base of adversary tactics and techniques based on real-world observations, read the [ATT&CK 101 Blog Post](https://medium.com/mitre-attack/att-ck-101-17074d3bc62)
    

#### OS Security and secure coding

-   [Secure Coding Best Practices Handbook](https://info.veracode.com/secure-coding-best-practices-hand-book-guide-resource.html) Veracode
    
-   [Secure Programming for Linux and Unix HOWTO](http://www.dwheeler.com/secure-programs/)), David Wheeler.
    
-   [Setuid demystified](http://www.cs.berkeley.edu/~daw/papers/setuid-usenix02.pdf) by Hao Chen, David Wagner, and Drew Dean.
    
-   [Removing ROP Gadgets from OpenBSD](https://www.openbsd.org/papers/asiabsdcon2019-rop-paper.pdf) Todd Mortimer mortimer@openbsd.org
    
-   [TCP Synfloods - an old yet current problem, and improving pf's response to it](http://quigon.bsws.de/papers/2017/bsdcan/)
    
    Henning Brauer, BSDCan 2017
    

#### Exploiting Hardware Bugs and Crypto Related

-   [Bug Attacks on RSA](https://css.csail.mit.edu/6.858/2011/readings/rsa-bug-attacks.pdf), by Eli Biham, Yaniv Carmeli, and Adi Shamir.
    
-   [Using Memory Errors to Attack a Virtual Machine](https://www.cs.princeton.edu/~appel/papers/memerr.pdf) by Sudhakar Govindavajhala and Andrew
    
    Appel
    
-   [Flipping Bits in Memory Without Accessing Them: An Experimental Study of DRAM Disturbance Errors](http://users.ece.cmu.edu/~yoonguk/papers/kim-isca14.pdf) Yoongu Kim, Ross Daly, Jeremie Kim, Chris Fallin, Ji Hye Lee, Donghyuk Lee, Chris Wilkerson, Konrad Lai, Onur Mutlu, see also [Explo
    
    iting the DRAM rowhammer bug to gain kernel privileges]([https://googleprojectzero.blogspot.com/2015/03/exploiting-dram-rowhammer-bug-to-gain.html](https://googleprojectzero.blogspot.com/2015/03/exploiting-dram-rowhammer-bug-to-gain.html))
    
-   _A Graduate Course in Applied Cryptography_ By Dan Boneh and Victor Shoup [https://toc.cryptobook.us/](https://toc.cryptobook.us/)
 