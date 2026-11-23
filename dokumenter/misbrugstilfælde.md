## Brugstilfælde 1: Bestilling af varer

| Felt | Beskrivelse |
|---|---|
| **Brugstilfælde** | Bestilling af varer |
| **Forudsætning** | Kunden har en kunde konto. |
| **Eksempel** | Kunden kan vælge varer fra produktsiden og lægge dem i en indkøbskurv. Under bestillingen skal kunden indtaste de nødvendige oplysninger, såsom navn på modtager, adresse, by, region, postnummer og land. Kunden skal desuden vælge leveringsmetode og kreditkort informationer herunder registeringsnummer, konto nummer, sikkerhedskode, som betalingen skal gennemføres med. |

### Misbrugstilfælde 1: Brud på domæne primitiver ved ændring af antal af varer der lægges i kurven



| Felt | Beskrivelse |
|---|---|
| **Misbrugstilfælde** | bestilling af negative antal af varer  |
| **Forudsætning** |trusselsaktør har adgang til siden med produkter samt indkøbskurv|
| **Eksempel** | ændring af antal af varer til at være et som vil medføre at trusselsaktøren anskaffer penge istedet for at betale for varen. |
| **Foranstaltning** | sikre at antallet af varer aldrig kan gå under nul. |


---

## Brugstilfælde 2: Oprettelse af kundekonto på webgoat.net

| Felt | Beskrivelse |
|---|---|
| **Brugstilfælde** | Oprettelse af kundekonto på webgoat.net |
| **Forudsætning** | Kunden har en aktiv e-mail. |
| **Eksempel** | Kunden indtaster kontooplysninger såsom brugernavn, e-mail, firmanavn, adgangskode og bekræftelse af adgangskode. Kunden indtaster desuden adresse oplysninger såsom adresse, by, region, postnummer og land. Når kunden har indtastet alle oplysninger og godkendt oprettelsen, skal kunden sendes videre til forsiden og samtidig logges ind på sin kundekonto. |

### Misbrugstilfælde 2: Brute-forcing af login siden


| Felt | Beskrivelse |
|---|---|
| **Misbrugstilfælde** | overtagelse af en kunde konto gennem brute-forcing |
| **Forudsætning** |trusselsaktør har adgang til login mulighed|
| **Eksempel** | trusselsaktøren har adgang til login og kan brute force på password eller/samt brugernavn, trusselsaktør har mulighed for indsættelse af kode . |
| **Foranstaltning** | login siden skal have et max antal forsøg på et vis tidsrum. |

---

## Brugstilfælde 3: Svar på blogindlæg

| Felt | Beskrivelse |
|---|---|
| **Brugstilfælde** | Svar på blogindlæg |
| **Forudsætning** | Kunden har adgang til blog siden. |
| **Eksempel** | Kunden skal have mulighed for at skrive og indsende svar eller kommentarer til virksomhedens blogindlæg. Dette skal kunne foregå enten ved, at kunden er logget ind med sin egen konto, eller ved at kunden kan indsende et svar uden at skulle logge ind. |



## missbrugstilfælde 3: kode injection på blog siden
| Felt | Beskrivelse |
|---|---|
| **Misbrugstilfælde** | Svar på blogindlæg med malicious kode |
| **Forudsætning** | trusselsaktør har adgang til blog siden. |
| **Eksempel** | trusselsaktøren har adgang til blog siden og kan oprette svar med henblik på at misbruge siden. |
| **Foranstaltning** | tekniske foranstaltninger i mod misbrug af svar på blogsiden. |


