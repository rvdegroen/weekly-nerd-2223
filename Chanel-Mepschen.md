# Chanel Mepschen

Chanel is front-end developer bij Triple en ze houdt van games en bordspelletjes en sporten. Zelf heeft ze de minor webdev ook gedaan. Ze is afgestudeerd in 2018 en toen is ze begonnen bij Triple. Ze doen hosting, gadets, smart-tv applicaties. Ze zijn erg gegroeid en hebben ze 2 bedrijven over genomen, zoals OKE en NIX en Code azuur. Ze hebben klaten zoals, NLZIET, Heineken en Ajax.

# Hoe ziet een gemiddelde front-end setup eruit bij Triple?

## Basics

- Git

Ze gebruiken version control.

1. Roll-back - naar een oudere versie terug gaan
2. Debugging - pin-pointen sinds welke versie het mis gaat
3. Waarom is dit gemaakt? - soms kom je een stukje code tegen, dat je wilt weten waarom zoiets is geschreven

- Werkwijze

1. create branch
2. commit en push
3. create pull request
4. code naar main
5. deployment

- NPM

Gebruiken ze veel. Iemand heeft soms 1000s uren in een package gestopt, dus dat is handig. Betekent niet dat je alles van NPM moet pakken (malicious code). Als er een bug is in een andere package, dan moet je wachten tot het is opgelost. Downloads zijn ook erg belangrijk om te weten of een package okay is.

## Setup

Meeste keuzes zijn voor haar gemaakt.

- Vanilla, library of framework

In vanilla js, moet je vaak dingen herhalen, soms is dit ook niet nodig, maar klanten willen vaak dingen af hebben, waardoor een framework handig is.

- Hoe kunnen we sneller schatbare applicaties maken?

Ze zijn over gegaan naar React en Next.js. Het nadeel is omdat de DOM bestaat nog niet bij het laden bij React en daarom hebben ze NEXT.js en dat is server-side render. React is voor het bouwen van componenten. Paar maanden geleden hebben ze besloten om over te gaan naar Svelte. Met een React breekt een smartTV app, en daarom gebruiken zij dus Svelte (ook voor web sinds een paar maanden geleden). Svelte is lichter en hebben minder code dan React en mensen van school kunnen dit veel sneller oppakken dan React.

## Early error catching

Voorbeeld functie: ze maakt een fout in haar code en daar komt ze pas achter in de browser, dit kost tijd. Dus hoe vind je zulke problemen? Hier gebruiken zij standaard TypeScript voor. TypeScript zorgt ervoor dat je gelijk je fouten ziet.

## Code formatting & fixing

Hoe zorgen ze voor constitentie:

- ESLint
- Prettier

## CSS minder foutgevoelig en makkelijk te maken?

- Sass gebruiken

Je kan door items heen loopen

## Hoe zet de browser het op zodat deze het wel gebruikt?

- Vite, voorheen webpack (zwaarder).
- Model replacement, het moment dat je iets aanpast in je modules, dan gaat hij het automatisch verversen.

## Live zetten van statisch en SRR pagina's

### FTP

is fourgevoelig, want er zijn geen lagen om te testen of je code wel goed is?

### Azure / Azure DevOps gebruiken zij ervoor

- Pipelines, code reviews

# Dev / acc / prod

- als je pushed: naar dev omgeving
- acceptatie voor klant te bekijken
- naar productie

# Process

- lokaal
- remote
- main
- dev
- acc
- prod

# Reflectie

Ik vond de presentatie zeer interessant en het gaf me meer inzicht in de werkflow van een bedrijf op een hele duidelijke manier. Chanel kwam met veel voorbeelden en alles wat ze zei, kwam heel duidelijk over. Dit was echt één van de beste presentaties die waarde voor mij toevoegde.
