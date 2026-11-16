# Fatbike Boy

Een gratis arcadespel in pixel art, in je browser. Rijd op je fatbike door de straat en bezorg vuurwerk op oudejaarsavond, maar niet in tuinen met een verbodsbordje.

Gemaakt in de geest van bezorgspellen uit de arcadetijd, zoals Paperboy (Atari Games, 1985), maar volledig nieuw: eigen code, eigen pixel art en een eigen verhaal. Dit project is onafhankelijk en niet gelieerd aan Atari Games of de rechthebbenden van Paperboy.

Gemaakt door Harold, met hulp van Claude (Anthropic).

**Speel het:** https://haaarold.github.io/Fatbike-boy/

## Over het spel

- Je gooit vuurwerk op de gele tegel bij klanten en krijgt punten, met een bonus voor treffers op rij
- Vuurwerkvrije tuinen (verbodsbordje) geven een klacht, bij drie klachten ben je af
- Ontwijk auto's, kliko's, putten, honden en scooters, bij drie botsingen is je accu leeg
- Rode pakketten vullen je voorraad aan, oliebollen geven punten
- Elke straat is drukker en sneller, met een vuurwerkfinale aan het einde
- Geen account, geen cookies, geen statistieken, geen advertenties
- Je beste score wordt alleen in je eigen browser bewaard

Vuurwerk is in het echt gevaarlijk. Dit is een spel met pixels en grapjes en geen oproep om vuurwerk te gooien.

## Besturing

| Op de computer | Op telefoon en tablet |
| --- | --- |
| Pijltjestoetsen of A en D om te sturen | Pijlknoppen onder het speelveld |
| Spatiebalk om te gooien | Rode knop, of tik op het speelveld |

## Techniek

Gewoon HTML, CSS en JavaScript, zonder build-stap en zonder frameworks.

```
index.html      homepage met uitleg en SEO
spel/index.html het spel zelf (canvas van 160 x 220 pixels, alles in code getekend)
img/            schermafbeeldingen, favicon en social image
sitemap.xml     voor zoekmachines
robots.txt
```

De pixel art wordt in `spel/index.html` met code op een canvas getekend en geschaald met `image-rendering: pixelated`. Geluid is optioneel en wordt met de Web Audio API in code gemaakt.

### Lokaal draaien

```
git clone https://github.com/haaarold/Fatbike-boy.git
cd Fatbike-boy
python3 -m http.server 8000
```

Open daarna http://localhost:8000.

### Publiceren met GitHub Pages

1. Ga in de repository naar **Settings > Pages**.
2. Kies bij Source **Deploy from a branch**, dan branch `main` en map `/ (root)`, en tik op Save.
3. Na een minuut staat de site op `https://<gebruikersnaam>.github.io/Fatbike-boy/`.

Gebruik je een andere naam of een eigen domein? Pas dan de URL aan in `index.html`, `spel/index.html`, `sitemap.xml` en `robots.txt` (zoek op `haaarold.github.io`).

## Meewerken

Ideeën voor nieuwe obstakels, een betere moeilijkheidsgraad of vertalingen zijn welkom via een issue of pull request. De straten worden gebouwd in de functie `maakStraat()` in `spel/index.html`.

## Licentie

De code en teksten staan onder de [MIT-licentie](LICENSE). Je mag ze vrij gebruiken, aanpassen en delen.

De lettertypes Pixelify Sans en Figtree komen van Google Fonts en hebben een eigen open licentie (SIL Open Font License).
