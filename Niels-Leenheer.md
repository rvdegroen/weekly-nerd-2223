# Wie is Niels Leenheer?

Niels heeft HTML5 test ontwikkeld en hij is een web developer. Hij maakt webapplicaties in Nederland. Veel kapperszaken maken gebruik van zijn product, waarbij de gebruikers een plaats kunnen reserveren. Hij organiseert 1 van de grootste web congressen. Hij heeft een eigen bedrijf dat heet Salonnen.

# Nieuwe browser API's: project FUGU

Hij gaat het hebben over nieuwe browsers API's en dingen die langzamerhand mogelijk worden i.p.v. 5 jaar geleden, zoals project Fugu.Het is gebasseerd op chromium. Dit project heeft als doel om het gat tussen webapplicaties en native applicaties te vullen.

Het is beperkt om wat er mogelijk is op het web, zoals:

- het openen van een bestand op het web. Project Fugu maakt dit wel mogelijk: je kan een bestand openen via het web bijvoorbeeld.

- Project Fugu heeft verschillende API's die worden gebruikt voor het storen van data.

- Je kan er ook voor zorgen dat je scherm niet in slaap valt.

- WebUSB: je kan er via het web bonnetjes printen.

- WebTransport

- Origin Private File System

Daarom heb je tegenwoordig ook een webversie van photoshop, dit komt doordat project Fugu dit mogelijk maakt.

In het verleden was dit allemaal niet mogelijk zonder een native applicatie ernaast te gebruiken. Nu kan dat wel.

## Is dit veilig?

Beveiliging is de vraag in kwestie. Veiligheid is zeker een ding, omdat je allemaal meer mogelijkheden hebt en deze dingen kunnen misbruikt worden. We lopen hierdoor wel een hoger risico.

We moeten uitgaan van wat mensen willen gebruiken en als je dan een browser met project Fugu gebruikt, dan is dit wel binnen de browser.

Binnen de browser mag inprincipe niks, tenzij je toestemming geeft (als je dit via de web doet).

Bij native applicaties kan je alles wel.

## Hardware API's

Niels had het over wat je met al deze API's kan en vooral de hardware API's.

### Voorbeeld 1: kleur van een lamp veranderen met web bluetooth API

Hij heeft een lamp aangesloten met een bluetooth chip en die kan hij bedienen met de web bluetooth API.

Als hij de API aan zet, dan moet hij een apparaat kiezen. De web app weet hier niks van, pas als er 1 is gekozen, dan weet de web app, wat er is gekozen.

Bluetooth werk met services en characteristics en id's: een soort object met properties en die kunnen een bepaalde waarde hebben.

Van de service haalt hij een characteristic op en kan hij daarmee waardes opschrijven. De waarde bestaatuit uit 3 bytes: RGB.
Dat is het enigste wat je nodig hebt om de kleur van een lamp te veranderen.

Daar kan je een applicatie omheen bouwen.

### Voorbeeld 2: printer met usb

Hij heeft een gameboy printer (online) laten zien, die hij normaal voor de kassabonnen voor logo's wordt geprint.

De printer spreekt een bepaalde taal: ESCPOS (ESC/POST): het is ontwikkeld in de jaren '70 en hij heeft daar een bibliotheek voor geschreven.

### Voorbeeld 3: API voor beweging

De meeste API's, zoals de gamepad API's geven oppervlakkige informatie terug.

### Voorbeeld 4: lego auto die wordt bedient via bluetooth en google

Omdat hij met bluetooth 2 communicatie, kan hij de commando's EN status uitlezen (als hij recht op of staande staat).

Hij heeft custom properties in CSS gemaakt (d.m.v. animations te gebruiken).

# Reflectie

Ik vond de presentatie heel interessant, leuke voorbeelden en leuke demo's had alleen soms een beetje moeite om het te volgen i.v.m. de structuur van de presentatie, maar dat ligt meer aan mijn concentratie vermogen.
