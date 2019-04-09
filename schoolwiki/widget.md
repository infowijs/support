# Schoolwiki Widget

De Schoolwiki widget is een zoekknop die u op uw website kunt plaatsen om gebruikers in staat te stellen direct te zoeken binnen de Schoolwiki van uw school.


## Widget code

Voeg de volgende code toe aan uw website om de widget te laten verschijnen:

```html
<script src="https://subdomein.schoolwiki.nl/widget.js" crossorigin="anonymous"></script>
<script>
schoolwiki.init({
   school: 'schoolnaam'
})
</script>
```

Vervang in de bovenstaande code de volgende zaken:

- In regel 1: vervang `subdomein.schoolwiki.nl` door de domeinnaam van uw Schoolwiki-omgeving.
- in regel 4: vervang schoolnaam door de naam van uw school, zoals deze te vinden is aan het einde van de URL als u op de Schoolwiki van de betreffende school bent. Voorbeeld: `https://infoscholen.schoolwiki.nl/infowijs-colllege` → `infowijs-college`.

**Belangrijk:** plaats deze code onderaan uw pagina, net voor de `</body>` tag. Weet u niet hoe of waar u deze code dient te plaatsen, neem dan contact op met uw webbeheerder, of met Infowijs.


## Widget aanpassen

Het is mogelijk om enkele zaken in het widget aan te passen.


### Configuratie parameters
Deze zaken kunnen doorgeven worden aan `schoolwiki.init`. Alle onderstaande properties zijn optioneel.

- `school`: slug van de school. Wordt gebruikt om zoekresultaten te filteren op de betreffende school.
- `color`: accentkleur van de button.
- `title`: geef een titel weer boven de Schoolwiki-button.
- `position`: `left` of `right`, om aan te geven of de button links- of rechtsonder dient te verschijnen. Standaardwaarde is `right`.
- `disabled`: als deze een boolean waarde `true` mee krijgt, wordt de button niet automatisch gerendeerd. Dit kan later handmatig gedaan worden via `schoolwiki.render()` (zie onderstaand).


### JavaScript API
De volgende functies kunnen handmatig aangeroepen worden via JavaScript:

- `schoolwiki.init(config)`: configuratie instellen en button renderen. Verplicht voordat een van de andere functies aangeroepen wordt.
- `schoolwiki.render()`: render Schoolwiki button met nieuwe configuratie.
- `schoolwiki.setConfig(config)`: config instellingen vervangen.
- `schoolwiki.show()`: geef Schoolwiki zoekveld weer.
- `schoolwiki.hide()`: verberg Schoolwiki zoekveld.
- `schoolwiki.destroy()`: verwijder het Schoolwiki widget van de pagina.
- `schoolwiki.search(query)`: open resultaten-venster met een bepaalde zoekterm.
