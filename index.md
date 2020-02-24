LATHUND
# HTML, CSS & JavaScript

## HTML 
HyperText Markup Language
``<!-- Så här skriver du en en kommentar i HTML -->``

```markdown
<!DOCTYPE html>
<html>
<head> <!-- START-TAGG -->
	<title></title>
</head> <!-- SLUT-TAGG -->
<body>
</body>
</html>
```
### ID & Class
Utöver att man kan ha olika element för olika innehåll, kan man även “döpa” sitt innehåll.

Ett ID är alltid unikt, enbart ett element kan ha ett specifikt ID.
```html
<img id=”flower-img” class=”gallery-img” src=”image/blomma.png” />
```

En class är mer generellt - flera element som ska ha samma egenskaper. 

```html
<img class=”gallery-img” src=”image/cat.png” />
<img class=”gallery-img” src=”image/puppy.png” />
```
## Taggar
### Dokumentstruktur

```html 
<html> <!-- Definierar att dokumentet -->
<head> <!-- Huvudet, innehåller metainformation -->
<title> <!-- Anger sidans namn -->
<body> <!-- Kroppen, hela sidans synliga innehåll -->
```

### Blockelement
Rubriker. Finns `h1-h6`
```html
<h1>Detta är rubriken</h1>
<h2>Detta är and andranivås rubrik<h2>
```
En `<div>`  står för divider, används för att hålla isär innehåll från varandra
```html
<div>...</div>
```

I en paragraf `<p>` är det alltid mycket text, med andra ord en paragraf. Paragrafer används också i Word och det brukar skapas mellanrum mellan de olika paragraferna (styckena).
```html
<p>Här kan det rymmas text i form av långa paragrafer</p>
```

Bild med attributet source(`src`) med länk till var bilden finns.
```html
<img src=”image/blomma.png” />
```
Länk till en sida kräver attribut med länkvägen. 
```html
<a href=”tomatsoppa.html”>Till receptet</a>
```
En dropdownlista med val som man kan välja. 
```html
<select>
  <option value=”1”>1</option>
  <option value=”2”>2</option>
  <option value=”3”>3</option>
</select>
```
Sorterad lista (orderd list, `ol`) med listans punkter (List item, `li`):
1. Kaffe
2. Te
3.  Mjölk
```html
<ol>
  <li>Kaffe</li>
  <li>Te</li>
  <li>Mjölk</li>
</ol>
```

#### Tabell
En tabell byggs upp av en table tagg, som visar var tabellen börjar och slutar. 

I den finns table head `thead` och table body `tbody`. 

I tabellhuvudet skapas en rad (`tr`, som står för table row) med `th`-taggar. Varje `th`-tag fungerar som en rubrik till sin kolumn. 

I `tbody` finns flera rader/tablerows, som i sin tur innehåller data i table data-taggar. 
Thead har bara en rad, medan tbodyn kan ha flera rader.
| Mängd | Enhet |
| ----------- | ----------- |
| 1 | dl |

```html
<table>
  <thead>
    <tr>
      <th>Mängd</th>
      <th>Enhet</th> 
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>dl</td> 
    </tr>
  </tbody>
</table>
```

## CSS
Cascading Style Sheets
`/* Så här skriver du en kommentar i CSS */`
`// Detta fungerar också som enrads kommentar i CSS`

### Selectors
```css
* {} /* Väljer alla element */
div {} /* Väljer alla div element */
div, h1 {} /* Väljer alla div och h1 element */
.classname {} /* Väljer alla element med klassen */
#idname {} /* Väljer element med id:t*/
```


### Pseudo klass
Css koden vi skriver till en selector med pseudo klassen `:hover` bestämmer vad som ska hända när vi för musen över elementet
```css
a:hover{}
```

### Properties & Values
```css
width: 200px; /* Sätter bredden */
height: 200px; /* Sätter höjden */
border: 1px solid #000000; /*Sätter en border(ram)runt elementet (1px tjock, heldragen linje, färgen svart) */
background-color: #000000; /* Sätter bakgrundsfärgen */
```

### Text properties 
```css
font-family: ‘Open Sans’; /* Sätter textens typsnitt */
font-size: 32px; /* Sätter textens storlek */
font-weight: 300; /* Sätter textens tjocklek */
color: #000000; /* Sätter textens färg */
text-transform: uppercase; /* Sätter texten till versaler*/
```

### Margin & Padding
_Margin = orange (sätter utrymme utanför “ramen”)_
_Padding = grön (sätter utrymme innanför “ramen”)_
```css
margin: 20px;
/* 
   margin-top: 20px;
   margin-bottom: 20px;
   margin-left: 20px;
   margin-right: 20px; 
*/
padding: 20px;
```

## JavaScript
`/* Så här skriver du en kommentar i JavaScript */`
`// Detta fungerar också som enrads kommentar i JavaScript`

### Variabler
```js
var minVariabel = 0;
```
Namngivet objekt som används för att hålla ett värde.


### Selectors
```js
getElementById(‘id’) // ID - ger ett objekt
getElementByClassName(‘klass’) // CSS-klass - ger en lista
getElementByTagName(‘td’) // HTML tag - ger en lista
```


### Events
Attributet onclick gör så att den angivna funktionen körs  vid klick på HTML-elementet
```js
<li onclick=”myFunction()”> Skala och hacka löken.</li>
```

### Funktion
En funktion skrivs genom att definierar `function` funktionens namn.. 
Inom `{}` skrivs uppgiften funktionen skall utföra.

```js
function minFunktion(p1, p2) {
    return p1 + p2;
}
```

### If / Else statement
Kontrollerar om något är sant eller falskt och utför uppgiften därefter.
```js
if (a = 0) {
    return "sant";
  } else {
    return "INTE sant";
}
```

### Array
Används för att lagra flera värden i en enda variabel.
```js
var klader = [ ‘strumpa’, ‘byxa’, ‘tröja’, ‘bh’ ]
klader[1]; //Motsvarar byxa
```

### Loop
Loopar är används för att exekvera ett kodblock ett antal gånger.
Om du vill köra samma kod om och om igen.
```js
for (var i = 0; i < klader.length; i+1) {
	console.log(klader[i]);
}
```
