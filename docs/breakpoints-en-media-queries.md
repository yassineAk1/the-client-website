# The Client - Website

<!--

De studenten leren veel over layout en layout modes.
We vragen veel responsive in de DoD's.
Is het misschien logischer in een workshop in te gaan op media queries? En daarin de leesregels introduceren bij het bepalen van een breakpoint of fluid layout?

Via kolommen. En dan de 'design' vraag: Hoe breed is een kolom?
Een kolom is een telefoon, dat is ook een leuke benadering.


En media query uitleggen. En mee laten spelen in hun Learning Journal. opdrachtje ... 

-->

## Breakpoints & Media queries

Afgelopen week heb je voor [je opdrachtgever](sprint-planning.md) een [prototype in HTML gemaakt](prototyping.md), waar je [feedback](code-design-review-prototype-en-html.md) op hebt gehad tijdens de Code/Design review. Maandag heb je wat geleerd over [Layout Modes in CSS](layout-in-css.md), en daarmee geoefend in [de deeltaak](https://github.com/fdnd-task/layout-in-css).

Vandaag ga je er voor zorgen dat verschillende schermformaten een andere layout krijgen: _Responsive Design_. Ook ga je leren hoe _breakpoints_ werken, en hoe je _media queries_ op een handige manier in kunt zetten.


### Breakpoints

Het is eigenlijk heel makkelijk. Stephen Hay beschrijft dit zo in zijn boek, _Responsive Design Workflow_:

> Start with the small screen first, then expand until it looks like shit. Time for a breakpoint!

Op een klein scherm beginnen dus, je scherm groter maken totdat het _lelijk_ wordt. En _dat_ is het moment waarop je een _breakpoint_ nodig hebt. Maar hoe weet je wanneer het _lelijk_ is?

Voor _tekst_ bestaan een aantal vuistregels. En aangezien we tot nu toe kale HTML hebben, met vooral tekst, kunnen we die vuistregels inzetten. Bij tekst moet je er altijd voor zorgen dat het _goed leesbaar_ is.


#### Goed leesbare teksten

Deze basisregels voor goed leesbare teksten kun je toepassen op je ontwerp:

- Tekst is minimaal 16px groot
- De regelafstand van langere teksten is 1.4 (140%)
- De optimale lengte van de regels is 10–12 woorden

In CSS kunnen we hiervoor `font-size`, `line-height` en `max-width` gebruiken, waar we eerst mee gaan oefenen.

#### Opdracht

Maak in je Learning Journal `leesbare-teksten.html` aan en kopieer daarin de volgende HTML:

```html
<!doctype html>
<html lang="la">
    <head>
        <title lang="nl">Goed leesbare teksten</title>
        <meta name="viewport" content="width=device-width">
        <style>
            body {
            }
            p {
                /*max-width: 20ch;*/
            }
            .p1 { font-size: 12px; }
            .p2 { font-size: 20px; }
            .p3 { font-size: 160%; }
            .p4 { font-size: 2vw; }
        </style>
    </head>
    <body>
        <p class="p1">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque convallis scelerisque ipsum sed tempor. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Phasellus tincidunt neque at rutrum semper. Morbi molestie, nibh vitae dictum gravida, eros sapien facilisis risus, id fringilla lectus augue a nisi. Duis non vestibulum sapien. Curabitur non congue dui. Pellentesque erat arcu, porta vel finibus non, iaculis non diam. Mauris a nulla ac mi sollicitudin suscipit. Duis tincidunt volutpat sapien ac bibendum. Morbi eu ipsum dolor. Proin accumsan faucibus interdum.</p>
        <p class="p2">Nulla viverra orci pharetra efficitur ornare. Duis venenatis, justo nec dictum commodo, metus sapien euismod velit, in bibendum elit nibh vitae ipsum. Mauris lacinia nec justo ac bibendum. Sed scelerisque a sapien ac ultricies. Aenean felis ipsum, scelerisque quis urna ac, blandit venenatis odio. Praesent vitae varius odio, quis pellentesque libero. Proin ac justo imperdiet, porttitor elit vitae, gravida arcu. Curabitur nec dolor pharetra, aliquam elit pretium, imperdiet lectus. Pellentesque dictum ante a nisl eleifend semper. Ut pulvinar velit eu turpis mollis rutrum. Vestibulum pharetra mi nec ullamcorper dignissim. Phasellus tempus turpis quis dui venenatis, eget tristique ante sollicitudin. Vestibulum faucibus tortor et varius hendrerit. Suspendisse ut lacinia velit. Donec eu tempus purus, non lacinia purus.</p>
        <p class="p3">Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Sed id metus est. Mauris nisl velit, volutpat vel semper non, volutpat eget urna. Praesent laoreet diam ut aliquam laoreet. Sed porttitor, dui eget interdum sagittis, enim risus posuere urna, in scelerisque erat urna eget ante. Nullam velit lacus, mollis suscipit euismod sit amet, volutpat eget ex. Nullam rhoncus diam at pellentesque faucibus. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas lorem lorem, laoreet a metus ac, ornare commodo risus. Sed nulla mi, fringilla lacinia eleifend in, vestibulum ut velit.</p>
        <p class="p4">Fusce a nulla nec lorem facilisis hendrerit. Duis lacinia ornare aliquet. Proin nec ligula viverra, fermentum libero eget, sodales sapien. In in nunc massa. Sed eget feugiat arcu, vitae gravida tortor. Donec ultrices ligula sit amet hendrerit egestas. Donec sagittis fringilla libero, quis gravida nunc pulvinar vitae. Integer malesuada purus at felis rhoncus, sit amet posuere sapien faucibus. Ut facilisis felis quis elit rutrum, dapibus porttitor elit tempor. Etiam ullamcorper arcu mattis felis pulvinar tempor. Curabitur sit amet massa porttitor, varius orci et, elementum nulla. Etiam viverra ultrices lorem ac viverra. Nunc convallis eget lorem sit amet condimentum. In augue diam, ultricies at lacinia vitae, eleifend id urna. Aenean tempor lacus lectus, ac ultrices nibh efficitur ac.</p>
    </body>
</html>
```

Experimenteer in je editor en browser met deze code, en geef alle paragrafen een prettige _regellengte_. Je kunt de breedte bepalen met `em`, `px` of bijvoorbeeld `ch` _units_. Probeer uit welke waardes je kan gebruiken om een goede regellengte te krijgen. Bv `max-width: 60ch` of `max-width: 20em`. Tel hoeveel woorden er maximaal op een regel staan.

Geef de `body` met `line-height` een _regelafstand_ die lekker werkt. Experimenteer met verschillende _units_. Wat gebeurt er als je `1.4` gebruikt? Wat als je `150%` gebruikt? Kun je hiervoor ook `px` gebruiken? Wat werkt het handigst?

💪 Een extra uitdaging nodig? Onderzoek eens hoe je de vierde alinea met een `clamp()` zo kunt maken dat die nooit kleiner wordt dan 16 pixels.


#### Bronnen

- [Web Design is 95% Typography](https://ia.net/topics/the-web-is-all-about-typography-period)
- [How We Read](https://alistapart.com/article/how-we-read)
- [Fundamental text and font styling @ MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)
- [`font-size` @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)
- [`line-height` @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
- [`max-width` @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width)
- [`ch` unit @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/length#ch)
- [`clamp()` @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp)


### Media queries

Zoals je net gezien hebt, kun je door de breedte van tekst bepalen wanneer iets _lelijk_ wordt. Of onhandig te lezen.

Op kleine schermen gebruik je vaak één kolom voor je hele layout. De standaard _Flow Layout_ met een `max-width` werkt hier heel goed voor. Dit noemen we ook wel de _One Column Layout_.

Zodra je meer ruimte op je scherm hebt, kun je meerdere _kolommen_ naast elkaar gaan zetten, met andere Layout Modes. Sommige elementen zullen over meerdere kolommen lopen (zoals een header of footer), sommige elementen zul je gaan opsplitsen. Ook hierbij gelden nog steeds de vuistregels voor leesbare teksten.

> Start with the small screen first, then expand until it looks like shit. Time for a breakpoint!

https://github.com/user-attachments/assets/0e31c1b0-d190-4b90-b07e-eb2c470c7257


Met een _media query_ kun je het breakpoint omzetten in code:

```css
body {
    font-family: sans-serif;
    font-size: 20px;
    line-height: 1.4;

    /* Dit is ons eerste breakpoint, waarbij we het body element in Grid Layout zetten */
    @media (min-width: 678px) {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
}
```

Simpel. Twee vuistregels die hierbij belangrijk zijn om het simpel te houden:

- We gebruiken het _Mobile First_ principe, te zien aan de `min-width` media query.
- We gebruiken _CSS Nesting_ voor media queries, waardoor we de `body` selector niet hoeven te herhalen.

Als je `max-width` media queries gebruikt, of geen gebruikt maakt van CSS Nesting, wordt het snel onoverzichtelijk. (Let op: we hebben het hier niet over de `max-width` property, die de maximale breedte van een element bepaalt.)

🆕 CSS Nesting bestaat pas een paar jaar. Veel tutorials en artikelen op het Web (en “AI” tools die hiermee gevuld zijn) maken er daarom dus nog geen gebruik van. Hou hier rekening mee als je zelf op zoek gaat naar oplossingen.

💡 Door Mobile First te werken, werk je met _Progressive Enhancement_, een belangrijk principe van het Web: je begint simpel op kleine schermen, en maakt het steeds complexer op schermen en browsers die meer aan kunnen.

#### Opdracht

Breid je `leesbare-teksten.html` experiment uit met media queries. Zet je devtools open, begin op een klein scherm, resize je scherm, bepaal wanneer je een breakpoint nodig hebt, en bepaal wat er dan gebeurt. Nest je media query in je selectors.

Varieer met je `font-size` en `line-height`, voeg headings toe met een andere tekstgrootte, voeg plaatjes toe, of een footer die over meerdere kolommen loopt op verschillende breedtes.

💪 Probeer extra breakpoints toe te voegen en tussen meer _Layout Modes_ te switchen op verschillende breakpoints.

#### Bronnen

- [Media queries @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries)
- [CSS nesting @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting/Using_CSS_nesting)
- 💪 [Je kunt media queries ook nesten](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting/Nesting_at-rules#multiple_nested_media_at-rules)
- 💪💪 Media queries al helemaal onder de knie? Kijk eens naar [Container Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_containment/Container_queries)


## En nu, voor komende vrijdag?

Als je geoefend hebt met Layout Modes, breakpoints, Mobile First werken en geneste Media Queries, kun je verder met de opdracht voor de opdrachtgever.

Begin met je HTML op een klein scherm, _expand until it looks like shit_, voeg breakpoints via media queries toe, en verander de layout. Gebruik voor elk breakpoint breakdown schetsen voor de layout, zoals je bij de Layout in CSS deeltaak hebt geoefend.

Vergeet niet regelmatig je werk te committen en te pushen, waardoor je iteratief werkt.

Vrijdag gaan we kijken hoe ver je bent gekomen met het combineren hiervan, krijg je feedback op je voortgang, en geef je andere studenten feedback op hun voortgang.
