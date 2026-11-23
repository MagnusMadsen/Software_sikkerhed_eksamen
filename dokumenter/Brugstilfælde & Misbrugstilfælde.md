## Brugstilfælde 1: Bestilling af varer

| Felt              | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Brugstilfælde** | Bestilling af varer                                                                                                                                                                                                                                                                                                                                                        |
| **Forudsætning**  | Kunden har en kunde konto.                                                                                                                                                                                                                                                                                                                                                 |
| **Eksempel**      | Kunden kan vælge varer fra produktsiden og lægge dem i en indkøbskurv. Under bestillingen skal kunden indtaste de nødvendige oplysninger: navn på modtager, adresse, by, region, postnummer og land. Kunden skal desuden vælge leveringsmetode og kreditkort informationer herunder registeringsnummer, konto nummer, sikkerhedskode, som betalingen skal gennemføres med. |

### Misbrugstilfælde 1: Brud på domæne primitiver ved ændring af antal af varer der lægges i kurven

| Felt                 | Beskrivelse                                                                                                                   |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Misbrugstilfælde** | bestilling af negative antal af varer                                                                                         |
| **Forudsætning**     | trusselsaktør har adgang til siden med produkter samt indkøbskurv                                                             |
| **Eksempel**         | ændring af antal af varer til at være negativt som medføre at trusselsaktøren modtager penge istedet for at betale for varen. |
| **Foranstaltning**   | sikre at antallet af varer aldrig kan gå under nul.                                                                           |

CIA: I indkøbskurven brydes integriteten (I), når et negativt vareantal giver en forkert ordresum og kan føre til en uberettiget udbetaling.

---

---

## Brugstilfælde 2: Oprettelse af kundekonto

| Felt              | Beskrivelse                                                                                                                                                                                                                                                                                                                                                  |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Brugstilfælde** | Oprettelse af kundekonto                                                                                                                                                                                                                                                                                                                                     |
| **Forudsætning**  | Kunden har en aktiv e-mail.                                                                                                                                                                                                                                                                                                                                  |
| **Eksempel**      | Kunden indtaster kontooplysninger: brugernavn, e-mail, firmanavn, adgangskode og bekræftelse af adgangskode. Kunden indtaster desuden adresse oplysninger såsom adresse, by, region, postnummer og land. Når kunden har indtastet alle oplysninger og godkendt oprettelsen, skal kunden sendes videre til forsiden og samtidig logges ind på sin kundekonto. |

### Misbrugstilfælde 2:  Misbrug af login siden

| Felt                 | Beskrivelse                                                                                                                      |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Misbrugstilfælde** | Overtagelse af en kunde konto gennem misbrug af loginside                                                                        |
| **Forudsætning**     | Trusselsaktør har adgang til login siden                                                                                         |
| **Eksempel**         | Trusselsaktøren har adgang til login og kan misbruge password og brugernavn, trusselsaktør har mulighed for indsættelse af kode. |
| **Foranstaltning**   | Login siden skal have et max antal forsøg på et vis tidsrum samt afvisning af specifikke specialtegn.                            |

CIA: Ved kontoovertagelse brydes fortroligheden (C), når en uvedkommende får adgang til kundedata. Uautoriserede ændringer af data bryder også integriteten (I).

---

---
## Brugstilfælde 3: Svar på blogindlæg

| Felt              | Beskrivelse                                                                                                                                                                                                                                       |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Brugstilfælde** | Kommentar på blogindl                                                                                                                                                                                                                             |
| **Forudsætning**  | Har adgang til blog sid                                                                                                                                                                                                                           |
| **Eksempel**    Skal have mulighed for at skrive og indsende kommentarer til virksomhedens blogindlæg. Dette skal kunne foregå enten ved, at kunden er logget ind med sin egen konto, eller ved at brugeren kan indsende et svar uden at skulle være logget ind. ind. |

## Misbrugstilfælde 3: Misbrug på blog siden
| Felt                 | Beskrivelse                                                                                                                                                |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Misbrugstilfælde** | Svar på blogindlæg med hensigt på misbrug                                                                                                                  |
| **Forudsætning**     | Trusselsaktør har adgang til blog siden.                                                                                                                   |
| **Eksempel**         | Trusselsaktøren har adgang til blog siden og kan oprette svar med henblik på at misbruge siden til at anskaffe informationer og udnytte svagheder i siden. |
| **Foranstaltning**   | Tekniske foranstaltninger i mod misbrug af svar på blogsiden <br><br>Afvisning af specifikke specialtegn,                                                  |

CIA: På bloggen brydes integriteten (I), hvis en kommentar manipulerer sidens visning for andre. Fortroligheden (C) brydes, hvis beskyttede oplysninger afsløres.


---

---

