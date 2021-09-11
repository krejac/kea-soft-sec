[[_Softwaresikkerhed]]

# Initial Overview of Software Security

**Todays reading**: AoST chapter 2: How Vulnerabilities Get into All Software

## Lecture notes
*Fortsat fra sidst*

Programmeringssproget C er et "unsafe" sprog. Gammelt, forventer at programmøren ved hvad han laver.

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

### Pricipper

#### Principle of Least Privilege
> The principle of least privilege states that a subject should be given only those
privileges that it needs in order to complete the task.

#### Principle of Least Authority
> The principle of least authority states that a subject should be given only the
authority that it needs in order to complete its task.

#### Principle of Fail-Safe defaults
> The principle of fail-safe defaults states that, unless a subject is given explicit
access to an object, it should be denied access to that object.

#### Principle of Economy of Mechanism
> The principle of economy of mechanism states that security mechanisms should
be as simple as possible.

#### Principle of Complete Mediation
> The principle of complete mediation requires that all accesses to objects be
checked to ensure that they are allowed.

#### Principle of Open Design
> The principle of open design states that the security of a mechanism should not
depend on the secrecy of its design or implementation.

#### Principle of Separation of Privilege
> The principle of separation of privilege states that a system should not grant
permission based on a single condition.

#### Principle of Least Common Mechanism
> The principle of least common mechanism states that mechanisms used to
access resources should not be shared.

#### Principle of Least Astonishment
> The principle of least astonishment states that security mechanisms should be
designed so that users understand the reason that the mechanism works they way it does and that using the mechanism is simple.

### Buffer Overflow
Slide 30 + 31 skal kunne forklares.

Forhindres ved at have skrivbar og eksekverbar hukommelse adsklidt.

### Local vs. remote exploits
**Local vs. remote** angiver om et exploit er rettet mod en sårbarhed lokalt på maskinen, eksempelvis opnå højere privilegier, eller beregnet til at udnytter sårbarheder over netværk.
**Remote root exploit** - den type man frygter mest, idet det er et exploit program der når det afvikles giver angriberen fuld kontrol, root user er administrator på Unix, over netværket.
**Zero-day exploits** dem som ikke offentliggøres – dem som hackere holder for sig selv. Dag 0 henviser til at ingen kender til dem før de offentliggøres og ofte er der umiddelbart ingen rettelser til de sårbarheder.

Keywords: *Input validation*, *Weak Structural Security*, 
Slides: [[2-initial-overview-sw-security.pdf]]



#KEA/Softwaresikkerhed 