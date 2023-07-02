# Inhoud

- [Inhoud](#inhoud)
- [Wie is Kilian Valkhof?](#wie-is-kilian-valkhof-)
- [Waar gaat Kilian Valkhof het over hebben?](#waar-gaat-kilian-valkhof-het-over-hebben-)
- [Choose the least powerful language suitable for a given purpose](#choose-the-least-powerful-language-suitable-for-a-given-purpose)
- [Custom toggles](#custom-toggles)
- [Datalist](#datalist)
- [Color ipv colorpicker](#color-ipv-colorpicker)
- [Complex page transitions](#complex-page-transitions)
  - [Smooth scroll](#smooth-scroll)
  - [Scroll margin top voor onder de heading](#scroll-margin-top-voor-onder-de-heading)
- [Target helder laten zien als je scrollt](#target-helder-laten-zien-als-je-scrollt)
- [Position sticky](#position-sticky)
- [Carousels](#carousels)
- [Lazy loading](#lazy-loading)
- [Force downloads attribute](#force-downloads-attribute)
- [Accordions and modals](#accordions-and-modals)
- [Dialogs](#dialogs)
- [JS ontwijken in de toekomst](#js-ontwijken-in-de-toekomst)
- [Selectmenu](#selectmenu)
- [Container queries](#container-queries)
- [:has parent selector](#-has-parent-selector)
- [Scroll linked animations](#scroll-linked-animations)
- [Take-aways](#take-aways)

# Wie is Kilian Valkhof?

Hij heeft een eigen bedrijf en maakt een browser om responsive websites mee te testen (Polypane). Voor ons is Polypane gratis (polypane.app/github-students) voor een jaar. Polypane is geschreven in Electron (is JS). Hij vindt JS tof maar CSS ook. Hij reist graag de wereld over om over CSS te praten. Hij maakt ook heel lang al websites. Hij deel van het electron governance (Teams)

# Waar gaat Kilian Valkhof het over hebben?

De presentatie heet "stop using JS for that" en hij geeft deze vaak voor "hardcore" CSS developers.

# Choose the least powerful language suitable for a given purpose

Als je iets in HTML kan doen, doe het in HTML. Als je iets in CSS kan doen, doe dat dan. Als laatst kijk je pas naar Javascript.

Javascript kan kapot gaan en is declaratief. Je browser moet dit bij kunnen houden en dat kan niet altijd.

# Custom toggles

- Input op de Label i.p.v. `for` gebruiken bij label - Normaal hoor je for bij een label te gebruiken. Dit hoeft niet als je input in de label staat, want dan is het logisch dat de label bij de input hoort.

- Input elementen kan je stylen:
  Replaced content = rendered je design en houdt gaten over voor vormen en afbeeldingen, deze wordt vervangen en dan hebben wij geen controle over hebben. Dat merk je aan dat je geen `pseudo` elementen kan gebruiken.
  Voor `for` controls is dat vervelend, want ze zijn "lelijk".
  Oplossing: `input { appearance: none }`, vervolgens kan je `:checked` ook kan stylen.

- Outline stylen voor de input: `outline-color: transparent`, maar je wilt
  `:focus` met `outline:none` EN `:focus-visible` met `outline 2px solid`.
  Met `outline-color: transparent` is deze wel zichtbaar met hoog contrast vgm.

# Datalist

Form die je kan filteren met een `datalist` element.

```
<input> list="frameworks"/>
<datalist id ="frameworks">
    <option> Bootstrap </option>
    <option Tailwind </option>
</datalist>

```

# Color ipv colorpicker

Ipv `colorpicker` te gebruiken kan je `color` gebruiken.

```
// colorpicker
<input type="color">

// Voor alle input elementen in je browser zeggen dat je darkmode gebruikt.
// Browser vervangt alle elementen in dark-mode elementen.

input {
    color-scheme: dark;
}

// of als je beide wilt afhankelijk welke mode je gebruikt

input {
    color-scheme: dark light;
}

```

# Complex page transitions

## Smooth scroll

Als je van de bovenkant naar de onderkant ligt, dan springt de pagina en heb je geen idee waar je bent op de pagina. Je mist context. Zou mooier zijn als je klikt en langzaam scrollt:

Vroeger jQuery, maar nu kan je met css doen:

```
// voor elke link wordt ernaar toe gescrollt

html {
    scroll-behavior: smooth;
}

// accesibilty: mensen die slecht tegen beweging kunnen (is de standaard):
// alleen als mensen geen beweging erg vinden, dan aan

@media (
    preference-reduced-motion: no preference;
) {
    html {
        scroll-behavior: smooth;
    }
}

// In javascript kan je dat ook doen met:

window.scrollTo((
    top: 1000
    behavior: smooth;
))


```

## Scroll margin top voor onder de heading

```
// scroll-margin top werkt als margin top, werkt ALLEEN tijdens scrollen en stopt onder de header. Dus de tekst verdwijnt niet achter de header

#my-target {
scroll-marging-top: 100px;
}

```

# Target helder laten zien als je scrollt

Je kan je

```

#my-target:target {
    outline: 10px solid deeppink;
    transition: 1s ease-in-out outline;
}

```

# Position sticky

Voerger: position fixed, is best wel lastig, want je kan het alleen positioneren aan de hand van de viewport. Vaak wil je dat de element wel in beeld blijft, maar alleen in context van een ander element. In JS heb je inview elementen voor.

In CSS kan je `sticky` gebruiken. Werkt als position relative, tot deze een grenswaarde bereikt. Values die je hebt is hetzelfde als absolute of fixed.

```

div {
    position: sticky;
}

div > .sticky {
    position: sticky;
    top: 50;
}

```

# Carousels

Heb je javascript voor nodig, kan je goed doen met scroll-snap. Verteld waar bepaalde elementen moet stoppen met scrollen.

```

// html

<div>
    <div class="option1"></div>
    <div class="option12"></div>
</div>

// css

// welke kant scrollen

.scroller {
    scroll-snap-type: x mandatory
    }

// waar de afbeelding laten zien

.scroller div {
    scroll-snap-align: start;
}

//// scroll snap naar center of center afbeelding laten zien

.scroller2 {
    scroll-snap-mandatory: x mandatory;
}

.scroller2 div {
    scroll-snap-align-center;
}

```

# Lazy loading

Niet alle afbeeldingen hoeven direct zichtbaar te zijn. Je kan je website hiermee sneller laden.
Doe dit NIET voor de afbeeldingen bovenaan de website, anders laden deze minder snel.

```
<img
src="xyz.png"
loading="lazy"
alt="xyz">

```

# Force downloads attribute

Net als lazy loading, maar dan downloads. Een rapport dat mag niet in de browser gelaad worden, maar moet gedownload worden

```

<a
href="link"
download></a>

```

# Accordions and modals

Accordians zijn handig als je veel content hebt, dat het wel georganiseerd is. Details te tonen en summary te verbergen.

```
// html

// accordion

<details>
    <summary>text</summary>
    <p>cyz</p>
<details>

// accordion die open staat met open attribute

<details open>
    <summary>text</summary>
    <p>cyz</p>
<details>

// css

// marker weghalen van het pijltje van de accordion

summary::market {
    content="icon/leeg"
}

// open marker

[open] summary::market {
    content="icon/leeg"
}

// summary is klikbaar, maar heeft geen indicatie, wel handig als je dit wel toevoegt

summary:hover {
    cursor: pointer;
    background: pink;
}

```

# Dialogs

Wel klein beetje js voor nodig. Dialog is een betere alert of confirm, zoals je die in js hebt. Dialog staat boven je pagina en zorgt ervoor dat de focus in het element blijft en geen andere elemente erover heen kunnen staan. Tegenstelling tot alert prompt confirm in js, dan wordt niks stop gezegd (js loopt en loopt pas verder las het ene lijntje klaar is).

Dialogs zitten in de top-layer, dus hoef je geen z-index toe te voegen.

```
// html
// dialog is verborgen en laat je zien met show model zien

<dialog>
    <form method="dialog">
</dialog>

// js functie om de dialog te laten zien

<button onclick="$$(`dialog`).showModel">
    Show the dialog
</button>

// css
// dialog backdrop (laagje ertussen in kan je ook stylen)
// backdrop is 100vh en 100vw

dialog::backdrop {
    background: white;
    backdrop-filter: blur;
}


```

Je kan ook 2 buttons gebruiken in de dialog, maar dat is te veel code om het te snel te typen.

# JS ontwijken in de toekomst

Met masonry layout:

```
// maak van dit grid een masonry lay-out en komt uit in 2023 voor alle browsers.
// kan je lezen in interop 2023
// Het plaatje past zich aan in het grid.

.container {
    display:grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: masonry;
}

```

# Selectmenu

Nieuwe select, heet selectmenu, want select mag niet vervangen worden. Het is een dropdown. Ieder onderddeel is stijlbaar, select niet:

```
// html

<selectmenu>
    <option>Option 1</option>
    <option>Option 2</option>
</selectmenu>

// css

selectmenu::part(button) {

}

selectmenu::part(listbox) {

}

selectmenu::part(marker) {

}

selectmenu option {

}

```

Het is nog steeds in ontwikkeling.

# Container queries

mediaqueries kijkt naar afmetingen van je browser, met container queries kan je kijken naar de afmetingen van je element.

```

.cardcontainer {
    container-type: inline-size;
}

.card {
    display: flex;
    flex-direction: column;
}

.card img {
    flex: 0 0 50 =cqw;
    aspect-ratio: 1;
    object-fit: cover;
}

$container (min-width: 400px) {
    .card {
        flex-direction: row;
    }
}

```

het komt er nog aan, is nu nog niet helemaal niet beschikbaar.

# :has parent selector

Ik wil een element stylen op basis van z'n inhoud.

```

form:has(#other:checked) #other-text {
    dislay: block;
}

```

voor meer uitleg: www.polypane.app/where-is-has

# Scroll linked animations

Bepaalde css animaties (keyframes), linken aan de scroll positie van de html element en ieder element dat kan scrollen. Je kan bv. een cover flow maken met alleen css. Kan ook met scrollsnap. Reflectie is ook met css gedaan.

3d transform van 0 in het midden. Meer naar ene kant 0%, andere kant 100%.

Over 2/3 versies kan het in chrome zitten.

Voorbeeld bekijken: bram.us

# Take-aways

Belangrijke punten nog van de presentatie:

- Alles die wordt vertoond kan cool zijn, maar kan in de toekomt veranderen en beter worden.
- Als je 1x iets leert hoef je dat niet opnieuw te leren.
