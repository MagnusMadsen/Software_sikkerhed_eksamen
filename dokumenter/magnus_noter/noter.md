



Brugstilfælde: Oprettelse af kundekonto på webgoat.net 

forudsætning: at kunden har en aktiv mail 

kunden indtaster konto information: username, E-mail, Company name, Password, confirm password, kunden indtaster adresse informationer: Address, city, Region/state, postal code, country. Når kunden har indtastet alle information og godkender bliver kunden sendt videre ind på forsiden samtidig med at de bliver logget ind på deres kunde konto. 




### Brugstilfælde 1: Oprettelse af kundekonto på webgoat.net 

**Forudsætning: at kunden har en aktiv mail** 

**Tekst** 


Account Information
User Name  
E-mail  
Company Name  
Password  
Confirm Password  

My address information (Optional)
Address  
City  
Region/State  
Postal Code  
Country 


### Misbrugstilfælde 1: Oprettelse af kundekonto

**Forudsætning: Overtage en kundekonto med en svag adgangskode** 

**En uvedkommende får adgang til en konto, der blev oprettet med en let gættelig adgangskode, og kan læse eller ændre kundens oplysninger. Det rammer fortrolighed og integritet.** 

### Misbrugstilfælde 2: Bestilling af varer

**Forudsætning: Kunden har en kundekonto og varer i kurven.**

**En kunde får registreret en ordre til et lavere beløb end den korrekte pris for varer og levering. Det rammer integriteten af ordredata og kan give webshoppen et økonomisk tab.**

### Misbrugstilfælde 3: Svar på blogindlæg

**Forudsætning: Der findes et blogindlæg, hvor besøgende kan indsende kommentarer.**

**En besøgende offentliggør en kommentar, der ændrer visningen af blogsiden for andre læsere. Det rammer integriteten af bloggens visning og kan vildlede læserne.**









## Kodegennemgang af registrering og checkout

Observationerne bygger på en statisk gennemgang af kildekoden og SQLite-skemaet.

- **E-mail ved registrering.** Systemet gemmer den indtastede adresse og logger brugeren ind uden at bekræfte ejerskabet af adressen. [Registrering](../../WebGoat.NET/Controllers/AccountController.cs#L86)
- **Adgangskodekrav.** Registreringen tillader meget korte adgangskoder. Hvis en kunde vælger en let gættelig adgangskode, øger det risikoen for kontoovertagelse. [Adgangskodeindstillinger](../../WebGoat.NET/Startup.cs#L74)
- **Beregning af ordrebeløb.** Kurven mangler grænsekontrol af det samlede vareantal. En beregningsfejl kan derfor give et for lavt beløb, som checkout gemmer i den simulerede betaling. [Varekurv](../../WebGoat.NET/Controllers/CartController.cs#L59) · [Checkout](../../WebGoat.NET/Controllers/CheckoutController.cs#L154)
- **Fejlvisning ved checkout.** Udviklerfejlsiden er aktiv i alle miljøer. En ubehandlet fejl kan vise en stacktrace med interne oplysninger om applikationen. [Fejlhåndtering](../../WebGoat.NET/Startup.cs#L130)





