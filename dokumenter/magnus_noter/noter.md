
## Kodegennemgang af registrering og checkout

Observationerne bygger på en statisk gennemgang af kildekoden og SQLite-skemaet.

- **E-mail ved registrering.** Systemet gemmer den indtastede adresse og logger brugeren ind uden at bekræfte ejerskabet af adressen. [Registrering](../../WebGoat.NET/Controllers/AccountController.cs#L86)
- **Adgangskodekrav.** Registreringen tillader meget korte adgangskoder. Hvis en kunde vælger en let gættelig adgangskode, øger det risikoen for kontoovertagelse. [Adgangskodeindstillinger](../../WebGoat.NET/Startup.cs#L74)
- **Beregning af ordrebeløb.** Kurven mangler grænsekontrol af det samlede vareantal. En beregningsfejl kan derfor give et for lavt beløb, som checkout gemmer i den simulerede betaling. [Varekurv](../../WebGoat.NET/Controllers/CartController.cs#L59) · [Checkout](../../WebGoat.NET/Controllers/CheckoutController.cs#L154)
- **Fejlvisning ved checkout.** Udviklerfejlsiden er aktiv i alle miljøer. En ubehandlet fejl kan vise en stacktrace med interne oplysninger om applikationen. [Fejlhåndtering](../../WebGoat.NET/Startup.cs#L130)





