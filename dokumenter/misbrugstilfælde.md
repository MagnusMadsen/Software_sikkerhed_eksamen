## Brugstilfælde: Bestilling af varer

| Felt | Beskrivelse |
|---|---|
| **Brugstilfælde** | Bestilling af varer |
| **Forudsætning** | Kunden har en kunde konto. |
| **Eksempel** | Kunden kan vælge varer fra produktsiden og lægge dem i en indkøbskurv. Under bestillingen skal kunden kunne indtaste de nødvendige oplysninger, såsom navn på modtager, adresse, by, region, postnummer og land. Kunden skal desuden kunne vælge leveringsmetode og det kreditkort, som betalingen skal gennemføres med. |

### Misbrugstilfælde 2: Bestilling af varer

**Forudsætning: Kunden har en kundekonto og varer i kurven.**

**En kunde får registreret en ordre til et lavere beløb end den korrekte pris for varer og levering. Det rammer integriteten af ordredata og kan give webshoppen et økonomisk tab.**

---

## Brugstilfælde: Oprettelse af kundekonto på webgoat.net

| Felt | Beskrivelse |
|---|---|
| **Brugstilfælde** | Oprettelse af kundekonto på webgoat.net |
| **Forudsætning** | Kunden har en aktiv e-mail. |
| **Eksempel** | Kunden indtaster kontooplysninger såsom brugernavn, e-mail, firmanavn, adgangskode og bekræftelse af adgangskode. Kunden indtaster desuden adresseoplysninger såsom adresse, by, region, postnummer og land. Når kunden har indtastet alle oplysninger og godkendt oprettelsen, bliver kunden sendt videre til forsiden og samtidig logget ind på sin kundekonto. |

### Misbrugstilfælde 1: Oprettelse af kundekonto

**Forudsætning: Overtage en kundekonto med en svag adgangskode** 

**En uvedkommende får adgang til en konto, der blev oprettet med en let gættelig adgangskode, og kan læse eller ændre kundens oplysninger. Det rammer fortrolighed og integritet.** 


---

## Brugstilfælde: Svar på blogindlæg

| Felt | Beskrivelse |
|---|---|
| **Brugstilfælde** | Svar på blogindlæg |
| **Forudsætning** | Kunden har adgang til blog siden. |
| **Eksempel** | Kunden skal have mulighed for at skrive og indsende svar eller kommentarer til virksomhedens blogindlæg. Dette skal kunne foregå enten ved, at kunden er logget ind med sin egen konto, eller ved at kunden kan indsende et svar uden at skulle logge ind. |



## missbrugstilfælde: svar på blog indlæg 
| Felt | Beskrivelse |
|---|---|
| **Misbrugstilfælde** | Svar på blogindlæg med malicious kode |
| **Forudsætning** | trusselsaktør har adgang til blog siden. |
| **Eksempel** | trusselsaktøren har adgang til blog siden og kan oprette svar med kode stykker i, enten til SQL-injection eller scripting. |
| **Foranstaltning** | svar feltet har korrekt input validering og tillader ikke kode som bruger input, kode bliver sorteret fra eller saniteret sådan det ikke bliver behandlet som kode men som rene strings. |


