# Wie is Hidde?

Hidde is toegankelijkheids expert. Hij werkt voor W3C web accesibility om de standaarden duidelijker te maken.

# Pop-overs

Eerst was content linear, today it can overlap in all sort of ways. Overlappende content kan bijvoorbeeld een artikel waar ook een audio speler bij zit en wat je kan doen met de audio speler (soort van uitleg) en dat wil je op een toegankelijke manier doen (als je inzoomt moet het niet stuk gaan).

# Non-modal dialogs and modal popovers

Er zijn ook verschillen tusdden dialogs en pop-overs

1. Modal vs non-modal = an element that is modal is the only thing you can interact with, the rest of the page is "on-earth". Pop-overs.

- een pop-up of pop-over zou modal moeten zijn, zodat je attentie daar naartoe gaat.

- A modal element is a drastic measure.

2. Non-modal = bijvoorbeeld rechtermuis knop op je bureaulad, je kan er mee interacteren, maar de rest kan je ook mee interacteren. Menu knoppen die je kan uitklappen zijn ook non-modal.

# light dismiss vs explicit dismiss

Light dismiss = als je pop-over hebt dat vanzelf weer weg gaat (als je een andere opent of als je scrolt).

Explicit dismiss = je moet erop klikken, zodat deze verdwijnt.

# Z-index vs top-later

Z-index = kan je bepalen waarop iets ligt.

Top-layer = een laag bovenop de allerhoogste z-index.

# Backdrop

Sommige elementen hebben een backdrop, dan zitten er elementen achter. Bij een top-layer heb je dat "gratis". Dit kan je doen met `::backdrop`.

# Keyboard focus trap

Sometimes you want to prevent users form exiting a component with their tab key. For example, think of a calendar, that you dont want to exit.

# Dialog

It's a component that contains content and you want the user to make a choice.

Dialog comes with semantics, that it comes in the top-later, maar je kan ook een div met een `role="dialog"` geven, dan krijg je alleen semantics, maar dan kom 't niet in de top-layer.

## Mono dialog

Je kan niet buiten de content van een dialog.
Vaak wel in de top-layer.
Close on esc nodig.

## Non modal dialog

Je hebt focus op andere dingen van de pagina.
Niet in de top-layer.
Soms heb je esc wel nodig op iets te closen, soms niet.

# Popover

Ligt bovenop de pagina, maar waarmee je de rest van de pagina nog wel wat kan doen. Een popover is hierdoor non modal.

Popover is helemaal nieuw en het is een attribuut. Als je de att toevoegt op een element, dan krijgt het een aantal behaviours. En je doet dit voor een element dat boven op andere elementen komen. Je krijgt geen semantics, maar je kan wel roles toevoegen, zoals dialog, menu, note.

Kan worden gebruikt voor:

- datepickers
- tooltips

# Anchor positioning

Je kan t.o.v. een ander element positioneren.

# Disclosure widgets

Elements that show and hide certain parts of the content like frequently asked questions or expendable menus.

Je kan <details> <summary> question <summary> <details> gebruiken. Je kan ook een button gebruiken met `aria-controls` en `aria-expanded="true"` (uitgeklapt). Met details summary, krijg je dit "gratis".

Het voordeel van details, is dat je met aria-expended niet zelf hoeft te kiezen dat je dit hoeft te doen, want de browsers doet dit al.

# Tips

- Schrijf op wat je leert

Je kan nu nog geen popovers gebruiken, maar wel in experimental chromium, mocht ik dit willen gebruiken.

- Pop-over = non modal
- Dialog = modal

# Reflectie

De presentatie was wel interessant, omdat dit dingen zijn waar ik niet van af wist. Eigenlijk ken ik `dialog` pas net, maar heb ik nooit gebruik. Nu heb ik wel het idee dat ik dit wil gebruiken, omdat ik het snap. Ik vond hem wel een beetje snel gaan. De engelse tekst en het nederlands spreken vond ik ook een beetje onhandig voor het snel typen (en het snel spreken).
