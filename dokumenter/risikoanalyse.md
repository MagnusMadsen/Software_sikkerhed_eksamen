# risiko analyse

Risiko analysen bliver udarbejdet efter et skema'er sådan vi følger ISO 27005 hvor der står det skal være kvalitativt. det medføre vi ender med en skema der ser ud som nedenstående. 

|            |     |     | Sandsynlighed |     |     |     |
| :--------: | :-: | :-: | :-----------: | :-: | :-: | --- |
|            |     |  1  |       2       |  3  |  4  | 5   |
|            |  1  |     |               |     |     |     |
| Konsekvens |  2  |     |               |     |     |     |
|            |  3  |     |               |    |     |     |
|            |  4  |     |               |     |     |     |
|            |  5  |     |               |     |     |     |


| **Konsekvens** | **Beskrivelse** |
|---------------|-----------------|
| **1 - Meget lav** | Der er en meget lille konsekvens, hvis hændelsen opstår. Det samlede økonomiske tab er **under 2.500 kr.**, fx ved en mindre fejlrettelse. |
| **2 - Lav** | Der er en lille konsekvens, hvis hændelsen opstår. Det samlede økonomiske tab er **fra 2.500 kr. til under 10.000 kr.**, fx ved udgifter til fejlfinding og udbedring. |
| **3 - Mellem** | Der er en moderat konsekvens, hvis hændelsen opstår. Det samlede økonomiske tab er **fra 10.000 kr. til under 25.000 kr.**, fx ved tabt indtjening under et kort driftsstop. |
| **4 - Høj** | Der er en stor konsekvens, hvis hændelsen opstår. Det samlede økonomiske tab er **fra 25.000 kr. til under 75.000 kr.**, fx ved tabt indtjening under et længere driftsstop og udgifter til ekstern bistand. |
| **5 - Meget høj** | Der er en meget stor konsekvens, hvis hændelsen opstår. Det samlede økonomiske tab er **75.000 kr. eller mere**, fx ved omfattende genopretning og erstatningsudgifter. |


| **Sandsynlighed** | **Beskrivelse** |
|------------------|-----------------|
| **1 - Meget lav** | Sårbarheden kræver meget specifikke forhold, avanceret viden eller intern adgang for at kunne udnyttes. Der findes ingen kendte angreb eller aktive trusselsaktører, der målretter denne type sårbarhed. |
| **2 - Lav** | Sårbarheden kan udnyttes, men kræver betydelige ressourcer, specialiseret viden eller adgang til systemer, som normalt er utilgængelige for angribere. Der findes få kendte eksempler på misbrug. |
| **3 - Mellem** | Sårbarheden kan udnyttes af en erfaren angriber med almindeligt tilgængelige værktøjer og viden. Der findes kendte angrebsmetoder, men de kræver en vis indsats eller særlige betingelser. |
| **4 - Høj** | Sårbarheden kan relativt let udnyttes af eksterne angribere. Offentligt tilgængelige værktøjer eller exploits eksisterer, og lignende sårbarheder ses regelmæssigt udnyttet i praksis. |
| **5 - Meget høj** | Sårbarheden er let at udnytte over internettet uden særlige forudsætninger. Automatiserede angreb, bots eller kendte exploits gør det sandsynligt, at den vil blive forsøgt udnyttet løbende mod webshoppen. |



## Brugstilfælde 1: Bestilling af varer

|            |     |     | **Sandsynlighed** |     |     |     |
| :--------: | :-: | :-: | :-----------: | :-: | :-: | --- |
|            |     |  1  |       2       |  3  |  4  | 5   |
|            |  1  |     |               |     |     |     |
| **Konsekvens** |  2  |     |               |     |     |     |
|            |  3  |     |               |  X  |     |     |
|            |  4  |     |               |     |     |     |
|            |  5  |     |               |     |     |     |


kan risikoen overføres?

ja, dette kan overføres men er ikke hensigstmæssigt på baggrund af at webshoppen er firmaets primære indkomst, så at være afhængig af et andet firma er ikke optimalt. 


kan risikoen minimeres?


der er tekniske foranstaltninger der kan tages i brug som vil mindske risikoen ned til at være meget lav i sandsynlighed og konsekvens.

## Brugstilfælde 2: Oprettelse af kundekonto


|            |     |     | **Sandsynlighed** |     |     |     |
| :--------: | :-: | :-: | :-----------: | :-: | :-: | --- |
|            |     |  1  |       2       |  3  |  4  | 5   |
|            |  1  |     |               |     |     |     |
| **Konsekvens** |  2  |     |               |     |     |     |
|            |  3  |     |               |  X  |     |     |
|            |  4  |     |               |     |     |     |
|            |  5  |     |               |     |     |     |

kan risikoen overføres?

ja, dette kan overføres men er ikke hensigstmæssigt på baggrund af at webshoppen er firmaets primære indkomst, så at være afhængig af et andet firma er ikke optimalt. 

kan risikoen minimeres?


der er tekniske foranstaltninger der kan tages i brug som vil mindske risikoen ned til at være meget lav i sandsynlighed og konsekvens.


## Brugstilfælde 3: Svar på blogindlæg


|            |     |     | **Sandsynlighed** |     |     |     |
| :--------: | :-: | :-: | :-----------: | :-: | :-: | --- |
|            |     |  1  |       2       |  3  |  4  | 5   |
|            |  1  |     |               |     |     |     |
| **Konsekvens** |  2  |     |               |     |     |     |
|            |  3  |     |               |  X  |     |     |
|            |  4  |     |               |     |     |     |
|            |  5  |     |               |     |     |     |

kan risikoen overføres?

ja, dette kan overføres men er ikke hensigstmæssigt på baggrund af at webshoppen er firmaets primære indkomst, så at være afhængig af et andet firma er ikke optimalt. 


kan risikoen minimeres?

der er tekniske foranstaltninger der kan tages i brug som vil mindske risikoen ned til at være meget lav i sandsynlighed og konsekvens.




## brugstilfælde 1 


## brugstilfælde 2 

## brugstilfælde 3 

