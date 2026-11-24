## STRIDE 

### Tjekliste for brugstilfælde

Fluebenene viser de relevante STRIDE-kategorier og omfatter mulige følgevirkninger som læsning eller ændring af kundedata efter en kontoovertagelse.

| **Brugstilfælde** | **Spoofing** | **Tampering** | **Repudiation** | **Information Disclosure** | **Denial of Service** | **Elevation of Privilege** |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| **1. Bestilling af varer** |  | ✔ |  |  |  |  |
| **2. Oprettelse af kundekonto** | ✔ | ✔ |  | ✔ |  |  |
| **3. Svar på blogindlæg** |  | ✔ |  | ✔ |  |  |

### Skabelon til vurdering af misbrugstilfælde

| ID | Misbrugstilfælde | Berørt systemdel | STRIDE-kategori | Beskrivelse af trussel | Teknisk foranstaltning | CIA-relevans |
|----|------------------|------------------|-----------------|-----------------------|------------------------|-------------|
| 1 | Titel på misbrugstilfælde | Login-side, API, webshop, database osv. | Spoofing / Tampering / Repudiation / Information Disclosure / Denial of Service / Elevation of Privilege | Kort beskrivelse af angrebet og dets konsekvens | F.eks. Rate Limiting, MFA, Inputvalidering, Kryptering, Logging | Confidentiality / Integrity / Availability |

Den ovenstående model er den vi vil bruge til oprettelse af vores STRIDE model og den måde vi vil vurdere vores misbrugstilfælde efter. 


---

---

## Misbrugstilfælde 1: Bestilling af negativt antal af varer


| ID | Misbrugstilfælde | Berørt systemdel | STRIDE-kategori | Beskrivelse af trussel | Teknisk foranstaltning | CIA-relevans |
|----|------------------|------------------|-----------------|-----------------------|------------------------|-------------|
| 1 | Bestilling af negativt antal af varer| Webshop | Tampering - ændring af værdier | Ved ændring af antallet af varer i HTTP requesten til et negativt antal kan det ende ud i at trussels aktøren anskaffer penge istedet for at betale penge | validering af input samt overholdelselse af domæne primitiver|Integrity |
___ 

## Misbrugstilfælde 2: misbrug af kundekonto/login

| ID | Misbrugstilfælde | Berørt systemdel | STRIDE-kategori | Beskrivelse af trussel | Teknisk foranstaltning | CIA-relevans |
|----|------------------|------------------|-----------------|-----------------------|------------------------|-------------|
| 2 |misbrug af kundekonto/login | login siden | Spoofing  | ved at have adgang til login siden med password og brugernavn felter er der mulighed for misbrug af kontoen via bruteforcing, som kan ende med en konto bliver overtaget | her kan vi bruge rate-limiting til at forhindre brute-forcing angreb | Confidentiality  |

--- 

## Misbrugstilfælde 3: misbrug af svar på blogindlæg

| ID  | Misbrugstilfælde              | Berørt systemdel | STRIDE-kategori | Beskrivelse af trussel                                                                                                                                                                          | Teknisk foranstaltning                                                                         | CIA-relevans                |
| --- | ----------------------------- | ---------------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | --------------------------- |
| 3   | misbrug af svar på blogindlæg | blog-siden       | Tampering       | Hvis bloggen fortolker kommentarer som som f.eks. HTML eller andet kode, kan en trusselsaktør indsende skadeligt indhold, der ændrer sidens visning for andre besøgende og i nogle tilfælde afslører beskyttede oplysninger | Brug inputvalidering og HTML-kodning ved visning, så kommentarer gengives som almindelig tekst | Confidentiality / Integrity |


--- 


