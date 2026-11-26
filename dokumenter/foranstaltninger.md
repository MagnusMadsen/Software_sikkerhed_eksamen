# tekniske foranstaltninger

## generelle principper

### fail fast 
hvis der er en regel der ikke er overholdt eller en precondition der ikke er overholdt er det bedre at fail fast, end at forvente det bliver grebet et andet sted i systemet, reglerne og kontrakterne skal håndhæves igennem koden.
Dette kan bedst gøres ved at bruge best practice af at tjekke alle pre conditions i starten af en metode før der bliver foretaget andre handlinger. (kan gøres med simple if statements der smider en exception)

kan læses om i kapitel 4.2





## ID 1

### Domæne primitiver
Dette misbrugstilfælde vil benefite meget af korrekte domæner primitiver, f.eks. vores varer og antal af varer skal være domæne primiter der er opsat efter forståelsen for firmaet, det kan hjælpe med at opretholde invarians sådan at en værdi, eller et objekt er valid, invarians skal oprettes første gang en værdi eller et objekt bliver skabt. Værdien eller objektet skal være invariant til punktet hvor at hvis den er oprettet, så er den altid valid, ellers ville den ikke eksistere.

INTET i et domæne primitiv må være en generisk data type.

for eksempel skal antal af varer aldrig bare være int varer = 0 men det skal være sat op som en kompleks data type med regler.
 Eksempel kan findes på side 222 i secure by design.


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
