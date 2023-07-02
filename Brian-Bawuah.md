# Brian Bawuah

Hij gaat het hebben over immersive environments of the web.

Brian houdt van hiken en hij houdt van Lego (vooral Lego technic) en hij houdt van planten en games en skeeleren. Hij werkt bij Team rockstars IT.

Hij is vorig jaar afgestudeerd en hij gaat het daarover hebben.

# Afstudeerproject

Vorig jaar was de lockdown nog een onderwerp en allerlei partijen kwamen met nieuwe ideeën, zoals gebruikers die samen kwamen in een immersive virtual reality omgeving. Artiesten werden vanuit hun kwamer gestreamd, maar hadden toch het gevoel dat ze samen waren en hij wilde hiermee iets gaan doen voor zijn afstudeer project.

Projecten zoals:

- Secret sky 2021
- Horizon venues

waren zijn inspiratie. Hij heeft zijn afstudeer project samen met het stedelijk museum gemaakt en wilde kijken hoe hij het stedelijk museum dichterbij de gebruiker brengen.

## Wat heeft hij gemaakt?

In zijn applicatie kunnen mensen een eigen character maken en overal naartoe lopen en expressions kunnen gebruikers plaatsen bij bepaalde kunstwerken.

### Eisen

Hij heeft bepaalde eisen met het stedelijk museum besproken, zo moet het:

- Ondersteunt worden in een vr omgeving en desktop omgeving
- Aansluiten op huidige situatie
  etc.

## Proces

Hij is eerst begonnen met schetsen voor een 3D-omgeving en hij heeft de minor virtual reality gedaan en vervolgens brown-boxing (immersieve ervaring tot leven te brengen met karton), waar veel aandacht wordt besteed aan het prototypen van die omgevingen. D.m.v. een arduino heeft hij interacties toegevoegd bijvoorbeeld temperatuur. Hij heeft 3 thema gebieden gemaakt en 4 centrale gebieden waar gebruikers specifieke kunstwerken kunnen bekijken.

Toen hij het gevoel had waar hij mee verder kon, bedacht hij hoe hij het in een 3D omegving kan plaatsen. Hij heeft hiervoor Blender gebruikt. Hij heeft alles wel van scratch moeten leren, maar het was wel goed gelukt.

Hoe krijg je dit op het web? Hij heeft dus Unity gebruikt met een (nev?) Mesh. Hij heeft geselecteerd waar je wel en niet mag lopen in Unity. Je kan zo bijv. niet op het water lopen.

## Eindresultaat

Op basis van een foto gaat hij je eigen avatar maken.

## Korte demo

Hij heeft laten zien dat hij alle fancy en technische dingetjes weggehaald (wel in een repo gezet). Hij is begonnen met 2 blobs, die kunnen navigeren. 1 gebruiker is een desktop gebruiker en de ander een vr gebruiker en die beweegt door te teleporteren.

Dit gebeurd allemaal in het HTML canvas element, waarin je graphics kan tekenen, d.m.v. web-GL / Three.js. Hiermee kan je makkelijk een 3d scene kan bouwen. Web-xr is een extra API die een verbinding kan maken tussen een VR headset (immersiveweb.dev). Niet alleen voor VR, ook voor augmented reality.

Hij heeft ook gebruik gemaakt van NXT.js. React 3viber kan je ook met three.js gebruiken en dat maakt het makkelijk om een 3D-scene op te zetten.

Verder heeft hij ook websockets gebruikt (colliseuse voor een multiplayer game enviroment en dat gebeurd voornamelijk op de server).

Voor de characters heeft hij readyplayerme gebruikt en die kan je gebruiken in een 3D-omgeving.

Hij heeft ook Mixamo gebruikt om animaties te koppelen aan een character. Hij heeft zelf 4 of 5 animaties gemaakt die hij op een character gebruikt.

### UDP en TPC

Web RTC is ook een manier om een verbinding te leggen tussen andere gebruikers en die gebruikt hij voor de groepscall (zoom gebruikt t ook). Peer js heeft het makkelijker gemaakt om een groep call op te zetten. Het is op een TCP en UDP protocol (hoe je data over het netwerk verstuurd). Een chat bericht wordt verstuurd en dan moet je wachten voor het pakket is aangekomen. Het zou heel vervelend zijn als dit in een call gebeurd. Bij een UDP protocol, dan maakt het niet uit of een pakket aankomt of niet, die blijft versturen. Het maakt de gebruikerservaring veel fijner.

### Functionaliteiten verder

Je kan ook users muten, omdat dit uit onderzoek bleek dat gebruikers dit willen.

# Reflectie

Ik vond dit wel een interessante presentatie. Er waren veel onderwerpen aan bod gekomen, waar ik wel eens verder van heb gehoord, waardoor het wel makkelijker is om dingen te volgen. Ik vond het ook echt cool om te weten dat hij characters heeft gebruikt die hij niet zelf heeft gemaakt en hetzelfde geldt voor animaties.
