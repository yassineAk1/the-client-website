# The Client - Website

Ontwerp en maak een website voor een opdrachtgever en bespreek het resultaat tijdens de Sprint Review.

De instructie van deze leertaak staan in de [INSTRUCTIONS](https://github.com/fdnd-task/the-client-website/blob/main/docs/INSTRUCTIONS.md)



## Inhoudsopgave Readme


  * [Beschrijving](#beschrijving)
  * [Kenmerken](#kenmerken)
  * [Bronnen](#bronnen)
  * [Licentie](#licentie)



## Beschrijving
<!-- In de Beschrijving staat hoe je project er uit ziet, hoe het werkt en wat je er mee kan. -->
<!-- Voeg een mooie poster visual toe 📸 -->
<!-- Voeg een link toe naar Github Pages 🌐-->
Dit project is een redesign van de Milledoni-website, een inspiratieplatform dat gebruikers helpt bij het vinden van het perfecte cadeau. Het doel van de opdracht is om een fris, modern en responsive ontwerp te maken dat aansluit bij hedendaagse gebruiksnormen.

De website bevat een homepagina met een filtersysteem, een overzicht van cadeau-ideeën, een zoekfunctie en een nieuwsbriefinschrijving in de footer. 

Gebruikers kunnen filteren op relatie, leeftijd en gelegenheid om een geschikt cadeau te vinden. De lay-out schaalt automatisch mee met verschillende schermgroottes, waardoor de site ook op mobiel goed leesbaar blijft.

  
## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met Javascript gedaan en hoe? Misschien heb je een framwork of library gebruikt? -->
HTML

De HTML-structuur is semantisch opgebouwd met duidelijke secties:
<header> met het logo en navigatie-iconen
<main> met de filters, cadeaulijst en zoekbalk
<footer> met een nieuwsbriefformulier, navigatiekolommen en juridische links

  Belangrijke elementen:

<fieldset> en <legend> samen met <select>  en <option> worden gebruikt in een label voor de filteropties, wat de toegankelijkheid verbetert.

https://github.com/yassineAk1/the-client-website/blob/main/index.html#L28-L38

<picture> zorgt voor verschillende logo’s afhankelijk van schermbreedte.
logo op klein scherm: 

<img width="447" height="207" alt="Screenshot 2025-10-08 115803" src="https://github.com/user-attachments/assets/3c5ba303-92c2-42c6-b2ef-755a9de93871" />

<img width="672" height="175" alt="Screenshot 2025-10-08 115841" src="https://github.com/user-attachments/assets/84c001dc-5e54-4268-b24b-400ade685829" />


logo op groot scherm:
 
<img width="672" height="175" alt="Screenshot 2025-10-08 115841" src="https://github.com/user-attachments/assets/4e33ee4d-6898-4efb-b2d6-626a05df5ac9" />

CSS

Belangrijkste stijlen en technieken:

Flexbox voor lay-out in de header, navigatie en footer.
CSS Grid voor de cadeauvermeldingen in .gifts, met auto-fit en minmax() voor een dynamisch kolommenrooster.
Responsive design met media queries binnen componenten zoals .newsletter-form en .footer-links.
Toegankelijkheidsaanpassingen via .visually-hidden voor verborgen maar leesbare labels.



## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
