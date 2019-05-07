# Ticketo
Met Ticketo kan een gebruiker eenvoudig aankopen inventariseren door de bonnetjes in te scannen. Zo staan de bonnetjes op één plek en zijn ze altijd in handbereik!

Ga voor app 2 naar de volgende commit: https://github.com/HANICA-MAD/dha-app2-lucas-bos-nils-groen/commit/f860448bc906edcaa6f494af14b442d6669c7dfd

### Installatie

1. Zorg dat je Node.JS, Ionic en Cordova hebt geinstalleerd.
2. Navigeer naar de map "ticketo" via de terminal
3. Run het command `npm install`.
4. Met het command `ionic serve` wordt de applicatie in de browser getoond, hier werken minder onderdelen omdat de app voor een telefoon is bedoeld.
5. Met het command `ionic cordova build ios/android` wordt de app gebouwd voor IOS of Android.
6. In het mapje 'platforms' komt het IOS/android project te staan.



### Voordelen

- Inkt vervaagt niet van de bonnetjes
- De bonnetjes kunnen in verschillende categorieën gezet worden (automatisch/handmatig?)
- Met behulp van geolocatie is het bekend waar de aankoop was
- Totaalbedragen kunnen berekend worden
- Bonnetjes staan veilig achter een login



### Requirements

Must:

- De gebruiker moet kunnen inloggen (Nils)
- De gebruiker kan een foto maken van de bon (Lucas)
- De gebruiker kan de details van de bon bekijken (Lucas)
- De gebruiker kan de details van de bon bewerken (Lucas)
- De gebruiker kan de bon verwijderen (Nils)

Should:
- De app kan de bon uitlezen met OCR (Nils)
- De gebruiker kan de bonnen categoriseren (Lucas)
- De app kan de bon categoriseren (Lucas)

Could:
- De app kan totaalbedragen weergeven (Lucas)
- De app kan de locatie van de bon op een map weergeven (Nils)
- De gebruiker kan de locatie van de bon aanpassen (Nils)
- De gebruiker kan meerdere foto’s toevoegen aan een bon (Lucas) (Image Slider where there is a default)



### Sensoren

- Camera
- Geolocation



### HTTP integratie

- Gebruik maken van @angular/common/http
- Gebruik maken van post en fetch naar een open firebase database



### Schermontwerp

![Storyboard](./Storyboard.jpeg)

Componenten:

- Buttons
- Tabs
- Inputs



### Reflectie

#### Demo feedback

##### Tips

- Barcode van de bon aan details toevoegen, dit is belangrijk voor het bedrijf
  - Dit is zeker waar. In de huidige app kan de barcode met de foto alsnog gevonden worden
- Automatisch datum invullen bij het aanmaken van een bon
  - Toegevoegd aan de app

##### Tops

- Mooi design
- Origineel idee

#### Verbeterpunten

- De pointers op de map hadden groter kunnen zijn en klikbaar, dat ze navigeren naar de detailpagina
- Meerdere afbeeldingen kunnen toevoegen per bon
- OCR implementeren om bijvoorbeeld de totaalprijs uit de bon te halen
- Loginpagina/registreerpagina design verbeteren

#### Hybrid vs Native

##### Beter in hybrid

- Design is makkelijk aan te passen met HTML en CSS
- Prototypen is makkelijk omdat het een webapp is
- CRUD operaties zijn eenvoudig

##### Beter in native

- Een map toevoegen, met amper 10 regels was de volledige map met pointers toegevoegd
- Flow van de applicatie, met de storyboard is de flow inzichtelijk en gemakkelijk te bewerken
- Geolocation uit een afbeelding halen is haast onmogelijk zonder externe package in hybrid
- Afbeeldingen opslaan op de telefoon is gemakkelijk in native
- Base64 afbeeldingen laden enorm langzaam in hybrid
- Geen problemen met permissions voor sensoren

