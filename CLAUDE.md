# martincarlsson.se

## Vad det här är
Personlig ensidessajt för Martin Carlsson, Tierp. Syftet är att Google ska koppla
sökningar på "Martin Carlsson" (särskilt "Martin Carlsson Tierp" och "Martin Carlsson
Länsförsäkringar") till rätt person. Namnet är vanligt; sida 1 på Google ägs idag av en
läkare, en hockeyspelare och en Sweden Rock-redaktör. Sajten är det tydliga "hemmet"
för just den här Martin Carlsson.

## Om Martin (den du jobbar med)
- Kallas "Chefen". Senior inom IT men inte utvecklare: kan läsa kod, skriver den inte.
- Vill ha korta, tydliga steg-för-steg-instruktioner när han ska göra något själv.
- Gillar rak kommunikation, humor och att bli motsagd när något låter för bra.
- Dagtid: Chef Trygghetstjänster på Länsförsäkringar Gävleborg, ansvarig för Alf
  (proaktiv trygghetstjänst för smarta hem).
- Kvällar och helger: medgrundare av Successifier AB tillsammans med huvudgrundaren
  Rickard Collander. Fokus just nu: supportifier.se (AI-kunskapsbas för kundservice
  hos små och medelstora företag). Sajter: successifier.com, successifier.se.
- Politik: Moderaterna i Tierps kommun, kandiderade till kommunfullmäktige 2026.
- LinkedIn: https://www.linkedin.com/in/martincarlsson/ (nyligen bytt från
  martincarlsson1; publik profil är påslagen). Instagram: @martinizi.

## Teknik
- Ren statisk HTML, ingen byggprocess, inga ramverk, inga npm-paket. Håll det så.
- Filer: index.html (allt innehåll, CSS och schema.org Person-markering i en fil),
  robots.txt, sitemap.xml, .nojekyll.
- Hostas på GitHub Pages från branchen main, mappen / (root).
- Fonter från Google Fonts (Bricolage Grotesque, Source Sans 3, IBM Plex Mono).
- Sidan har ljust och mörkt tema via CSS-variabler i :root. Behåll båda.
- Språk: svenska. lang="sv" på html-elementet.

## Arbetssätt (viktigt)
- En ändring i taget. Gör ändringen på en egen gren och skapa en pull request så
  Martin kan se diffen och godkänna. Pusha aldrig direkt till main utan att fråga.
- Förklara vad du ändrat i vanlig svenska, inte i kodtermer.
- Uppfinn inga fakta om Martin. Om något saknas (datum, titlar, resultat): fråga.
- Rör inte schema.org-blocket (<script type="application/ld+json">) utan att säga
  till; det är det som talar om för Google vem sidan handlar om. Uppdatera det när
  länkar eller titlar ändras i synligt innehåll.
- Lägg INTE till någon CNAME-fil förrän domänen är registrerad och DNS pekar rätt.
  Gör man det innan slutar github.io-adressen fungera.

## Öppna punkter
- Domänen martincarlsson.se är ännu inte registrerad (ledig hos Internetstiftelsen
  2026-09-26). Martin registrerar den som privatperson hos t.ex. Loopia.
- När domänen finns: (1) DNS hos registraren: fyra A-poster för @ till
  185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 samt CNAME för
  www till Martinizi81.github.io. (2) Lägg till CNAME-fil i repot med
  innehållet martincarlsson.se. (3) Sätt custom domain + Enforce HTTPS under
  Settings → Pages. (4) Uppdatera sitemap.xml/canonical om något pekar fel.
- Därefter: anmäl sajten i Google Search Console och skicka in sitemap.xml.
- Innehåll som väntar på besked från Martin: valresultat/uppdrag efter valet 2026
  (texten säger idag bara "kandiderade"), och vilken e-postadress som ska visas
  (förslag: martin@martincarlsson.se, ej inlagd ännu).
- Framtida idéer, ej beslutade: länka Rickard Collander, lägga till foto, en kort
  "Skrivet"-sektion med länkar till inlägg.
