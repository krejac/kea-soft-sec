[[_Softwaresikkerhed]]

# Initial Overview of Software Security

**Todays reading**: AoST chapter 2: How Vulnerabilities Get into All Software

## Lecture notes
*Fortsat fra sidst*

Programmeringssproget C er et "unsafe" sprog.

### Brug analyseværktøjer
**Statisk analyse**
> Finder fejl uden at køre programmet; typisk findes konstruktioner som indeholder fejl, brug af forkerte funktioner m.v.
	
**Dynamisk analyse**
> Findes ved at køre programmet, typisk i et specielt miljø.

### Demo-time
Buffer overflow på en raspberry pi.

*Takeaway*: Hvis du kan få et program til at fejle konsistent, vil man ofte kunne udnytte dette til at få afviklet arbitrær kode.

Hint: Skriv exploitkode ind i bufferen og slut af med et hop til den exploitkode du lige har skrevet ind i bufferen før dit hop.

Mitigering:
[W^X](https://en.wikipedia.org/wiki/W%5EX) (Write XOR Execute) - Først i OpenBSD
[Address Space Layout Randomization](https://en.wikipedia.org/wiki/Address_space_layout_randomization) - Først i OpenBSD

---

*Så kom vi til dagens tekst... How Vulnerabilities Get into All Software*


Keywords: *Input validation*, *Weak Structural Security*, *Principle of Least Privilege*, *Principle of Least Authority*, *Principle of Fail-Safe defaults*, *Principle of Economy of Mechanism*, *Principle of Complete Mediation*, 

Slides: [[2-initial-overview-sw-security.pdf]]



#KEA/Softwaresikkerhed 