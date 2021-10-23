[[_Softwaresikkerhed]]

# SDLC and risk ranking

**Todays reading**: AoST chapter 2

Supporting litterature: 24-deadly introduction before page 1

Supporting litterature: _Secure Programming for Linux and Unix HOWTO_

## Lecture Notes
*Forsat fra sidst...*

For at sikre mod bufferoverflow har eks. BSD implementeret "Stack Protection".

### Cryptography
[[2-initial-overview-sw-security.pdf]]

- WEP er lort.
- Lær mere om krypto her: [A Graduate Course in Applied Cryptography](https://toc.cryptobook.us) inkl. gratis bog.

#### Basic Cryptography introduction  
- Cryptography or cryptology is the practice and study of techniques for secure communication  
- Modern cryptography is heavily based on mathematical theory and computer science practice;  cryptographic algorithms are designed around computational hardness assumptions, making such  algorithms hard to break in practice by any adversary  
- Symmetric-key cryptography refers to encryption methods in which both the sender and receiver share the same key, to ensure confidentiality, example algorithm *AES* 
- Public-key cryptography (like RSA) uses two related keys, a key pair of a public key and a private key. This allows for easier key exchanges, and can provide confidentiality, and methods for signatures and other services  

Source: https://en.wikipedia.org/wiki/Cryptography

- Moderne CPU'er har ofte AES NI (AES New Instruction) indbygget til hurtig kryptering direkte i CPU'en.

- I 2001 blev der vedtaget en ny standard algoritme Advanced Encryption Standard (AES) som afløser Data Encryption Standard (DES).
	- (AES god; DES dårlig)

**Hashing**
- HASH algoritmer giver en næsten unik værdi baseret på input værdien ændres radikalt selv ved små ændringer i input.
- MD5 og SHA-1 er idag gamle og skal ikke bruges mere


**Key Exchange**
- Revolution: Diffie–Hellman key exchange
	- Se grafisk fremstilling på slide 58 i [[2-initial-overview-sw-security.pdf]].

---

### Secure Software Development Lifecycle
[[3-SDLC-and-risk-ranking.pdf]]

- Brug style guides (á la PEP-8 for Python)

> *A full lifecycle approach is the only way to achieve secure software.*
– Chris Wysopal

**Functional specification needs to evaluate security**
- Completeness
- Consistency
- Feasibility
- Testability
- Priority
- Regulations

**Phases of SSDL**   
Phase 1: Security Guidelines, Rules, and Regulations   
Phase 2: Security requirements: attack use cases   
Phase 3: Architectural and design reviews/threat modelling    
Phase 4: Secure coding guidelines   
Phase 5: Black/gray/white box testing   
Phase 6: Determining exploitability   

... og bagefter: 

 **Deploying Applications Securely**
- Having secure defaults helps
- Good initial file permissions
- Make sure application can be patched
- Track and prioritize identified vulnerabilities
- Make it easy to report vulnerabilities to the organization


**Secure Coding Best Practices Handbook from [[secure-coding-best-practices-handbook-veracode-guide.pdf|Veracode]] **
#01 Verify for Security Early and Often
#02 Parameterize Queries
#03 Encode Data
#04 Validate All Inputs
#05 Implement Identity and Authentication Controls
#06 Implement Access Controls
#07 Protect Data
#08 Implement Logging and Intrusion Detection
#09 Leverage Security Frameworks and Libraries
#10 Monitor Error and Exception Handling

**Roles and Responsibilities**
- Make it clear who has responsibility for security at various phases
- Program or product manager should write the security policies
- Product or project manager also responsible for certification processes
- Architects and developers are responsible for providing design and implementation
- QA/testers drive critical analyses of the system and build tests
- Security process managers oversee threat modelling, security assessments, and secure coding training

**Risk-Based Security Testing**

>Focus testing on areas where difficulty of attack is least and the impact is highest.
–Chris Wysopal

- Time and resources are constrained
- Software development must be prioritized
- Threat modelling / risk modelling exist to help this
   - Identify threat paths
   - Identify threats
   - Identify vulnerabilities
   - Rank/prioritize the vulnerabilities

[[software-security-exercises.pdf]]

#KEA/Softwaresikkerhed 
