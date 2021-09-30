[[_Softwaresikkerhed]]

# Hacking Web Applications: Offensive

**Todays reading**: 

*Part II. Offense, chapters 9-16*
- 9. Introduction to Hacking Web Applications
- 10. Cross-Site Scripting (XSS)
- 11. Cross-Site Request Forgery (CSRF)
- 12. XML External Entity (XXE)
- 13. Injection
- 14. Denial of Service (DoS)
- 15. Exploiting Third-Party Dependencies
- 16. Part II Summary

## Lecture Notes
[[6-web-app-hacking-offensive.pdf]]

- Bør kende til og kunne forklare principperne i overskrifterne fra "Todays reading".

### Cross-Site Scripting (XSS)

> Cross-Site Scripting (XSS) vulnerabilities are some of the most common vulnerabili‐ ties throughout the internet, and have appeared as a direct response to the increasing amount of user interaction in today’s web applications. At its core, an XSS attack functions by taking advantage of the fact that web applications execute scripts on users’ browsers. Any type of dynamically created script that is executed puts a web application at risk if the script being executed can be contamina‐ ted or modified in any way—in particular by an end user.

XSS attacks are categorized a number of ways, with the big three being:
- Stored (the code is stored on a database prior to execution)
- Reflected (the code is not stored in a database, but reflected by a server)
- DOM-based (code is both stored and executed in the browser)

Note: attacks the user, his/her data mostly.

### Cross-Site Request Forgery (CSRF)
> Sometimes we already know an API endpoint exists that would allow us to perform an operation we wish to perform, but we do not have access to that endpoint because it requires privileged access (e.g., an admin account).
> In this chapter, we will be building Cross-Site Request Forgery (CSRF) exploits that result in an admin or privileged account performing an operation on our behalf rather than using a JavaScript code snippet.
> CSRF attacks take advantage of the way browsers operate and the trust relationship between a website and the browser. By finding API calls that rely on this relationship to ensure security — but yield too much trust to the browser — we can craft links and forms that with a little bit of effort can cause a user to make requests on his or her own behalf—unknown to the user generating the request.

- Often seen in small CPE routers in homes, if the user activates and evil link, their router might be reconfigured or taken over

### XML External Entity (XXE)
> XML External Entity (XXE) is a classification of attack that is often very simple to execute, but with devastating results. This classification of attack relies on an improperly configured XML parser within an application’s code.
> Generally speaking, almost all XXE attack vulnerabilities are found as a result of an API endpoint that accepts an XML (or XML-like) payload. You may think that HTTP endpoints accepting XML is uncommon, but XML-like formats include SVG, HTML/DOM, PDF (XFDF), and RTF. These XML-like formats share many common similarities with the XML spec, and as result, many XML parsers also accept them as inputs.
> The magic behind an XXE attack is that the XML specification includes a special annotation for importing external files. This special directive, called an external entity, is interpreted on the machine on which the XML file is evaluated. This means that a specially crafted XML payload sent to a server’s XML parser could result in compromising files in that server’s file structure.

- Include file X, and the XML parser does as instructed!
- Often I consider these along the same lines as Java serialization attacks, sending data in JAVA that gets converted/expanded etc.

### Injection
> One of the most commonly known types of attacks against a web application is SQL injection. SQL injection is a type of injection attack that specifically targets SQL databases, allowing a malicious user to either provide their own parameters to an existing SQL query, or to escape an SQL query and provide their own query. Naturally, this typically results in a compromised database because of the escalated permissions the SQL interpreter is given by default.
> SQL injection is the most common form of injection, but not the only form. Injection attacks have twomajor components: an interpreter and a payload from a user that is somehow read into the interpreter. This means that injection attacks can occur against command-line utilities like FFMPEG (a video compressor) as well as against databases (like the traditional SQL injection case).

- Injecting SQL commands, perform database actions
- Escape into the operating system via SQL, easier in the old days
- Escape into shell from URL parameters, often happens
- Compare to shellshock vuln, sending data that later ends up in the Unix shells

### Denial of Service (DoS)
> Perhaps one of the most popular types of attacks, and the most widely publicized, is the distributed denial of service (DDoS) attack. This attack is a form of denial of service (DoS), in which a large network of devices flood a server with requests, slowing down the server or rendering it unusable for legitimate users.
> DoS attacks come in many forms, from the well-known distributed version that involves thousands or more coordinated devices, to code-level DoS that affects a single user as a result of a faulty regex implementation, resulting in long times to validate a string of text. DoS attacks also range in seriousness from reducing an active server, to a functionless electric bill, to causing a user’s web page to load slightly slower than usual or pausing their video midbuffer.
> Because of this, it is very difficult to test for DoS attacks (in particular, the less severe ones). Most bug bounty programs outright ban DoS submissions to prevent bounty hunters from interfering with regular application usage.

- There have been some hash-based attacks and attacks using data to create bad performance, see PHP security advisories

### Exploiting Third-Party Dependencies
> The rampant use of third-party dependencies, in particular from the OSS realm, has created an easy-to-overlook gap in the security of many web applications. A hacker, bug bounty hunter, or penetration tester can take advantage of these integrations and jumpstart their search for live vulnerabilities. Third-party dependencies can be attacked a number of ways, from shoddy integrations to fourth-party code or just by finding known exploits discovered by other researchers or companies.
 
-  Be careful what you include in your environment
-  En afart kunne også være et "supply chain attack"

#KEA/Softwaresikkerhed 