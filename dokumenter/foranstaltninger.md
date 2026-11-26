# tekniske foranstaltninger

## generelle principper

### fail fast 
hvis der er en regel der ikke er overholdt eller en precondition der ikke er overholdt er det bedre at fail fast, end at forvente det bliver grebet et andet sted i systemet, reglerne og kontrakterne skal håndhæves igennem koden.
Dette kan bedst gøres ved at bruge best practice af at tjekke alle pre conditions i starten af en metode før der bliver foretaget andre handlinger. (kan gøres med simple if statements der smider en exception)

kan læses om i kapitel 4.2


### entity's
bruger konto er f.eks. entitys, det er en entity hvor nogen attributter kan ændre sig, her kan man f.eks. oprette unique user ids til at identificiere konto'er, så er brugeren fri til at skifte f.eks. email, adresse, kredit kort osv. kunde konto'en skal beholde det samme unikke id, selvom attributer bliver ændret.

**kontroller om dette er overholdt i koden** 


### eksplicit vs implicit data 

implicit er ting der er en konsensus om uden en samtale om det, alting burde i software udvikling være eksplicit, altså hvis vi falder over noget vi mener er implicit, så skal det  stadig diskuteres sådan det bliver implicit. Det gør at vi kan oprette regler for den del af koden, f.eks. quantitys vil altid have sine regler overholdt, fordi de er koblet direkte til oprettelsen af variablen.

## ID 1

### Domæne primitiver
Dette misbrugstilfælde vil benefite meget af korrekte domæner primitiver, f.eks. vores varer og antal af varer skal være domæne primiter der er opsat efter forståelsen for firmaet, det kan hjælpe med at opretholde invarians sådan at en værdi, eller et objekt er valid, invarians skal oprettes første gang en værdi eller et objekt bliver skabt. Værdien eller objektet skal være invariant til punktet hvor at hvis den er oprettet, så er den altid valid, ellers ville den ikke eksistere.

INTET i et domæne primitiv må være en generisk data type.

for eksempel skal antal af varer aldrig bare være int varer = 0 men det skal være sat op som en kompleks data type med regler.
Eksempel kan findes på side 222 i secure by design.

Fordelen er at ved oprettelse af domæne primitiver kan de bruges i de API'er man skal arbejde med, sådan at input validering er garanteret fordi alle værdier er på forhånd defineret til at overholde et vis sæt regler.

### DTO klasser
det er vigtigt ikke at give Domæne primitiver direkte til frontend'en, det er her en DTO klasse kommer ind og frakobler domæne primitivet, reglerne kan stadig overholdes i en DTO, men DTO'en er det eneste vi præsentere, sådan man kan udvikle back'enden uden at bekymre sig over f.eks. en RESt api i frontend'en.


## ID 2 



## ID 3 

Til at forhindre misbrug af svar på blog indlæg er det muligt gennem overholdelse af sikkerhedsprincippier som input validering og input sanitering sådan at intet indsat i disse felter bliver anset som kode. 

her kan inddrages kapitel 4.3 i secure by design, det omhandler input validering og hvordan man analysere input på forskellige måder.  

her er der emner som f.eks. syntax, altså om data formattet er rigtigt, lexical content, har dataen de rigtige karakterer og encoding og Semantics.

### længde 
for eksempel giver det ikke mening at have mere end 300-400 karakterer i et blog svar, lidt ligesom reglerne på twitter.
dette kan kontrolleres enten gennem content length headeren eller ved input i c# koden.



### Lexical content
Hvis dataen inderholder andet end punktummer, mellemrum, bogstaver samt tal så burde data'en smides ud da der ikke er behov for andet i data'en da det er simple tekst svar vi forventer i tekst feltet.

Hvis regler ikke overholdes skal der f.eks. komme en exception som illegalargument exception.


** vil vi beholde anonymt svar mulighed?**

**kan et regex bruges i blog indlæg?**
