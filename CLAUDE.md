# martincarlsson.se

## Vad det här är
Personlig ensidessajt för Martin Carlsson, Tierp. Syftet är att Google ska koppla
sökningar på "Martin Carlsson" (särskilt "Martin Carlsson Tierp" och "Martin Carlsson
Länsförsäkringar") till rätt person. Namnet är vanligt; sida 1 på Google ägs idag av en
läkare, en hockeyspelare och en Sweden Rock-redaktör. Sajten är det tydliga "hemmet"
för just den här Martin Carlsson.

Live på https://martincarlsson.se sedan 2026-09-26 (GitHub Pages, egen domän, https).

## Om Martin (den du jobbar med)
- Kallas "Chefen". Senior inom IT men inte utvecklare: kan läsa kod, skriver den inte.
- Vill ha korta, tydliga steg-för-steg-instruktioner när han ska göra något själv.
- Gillar rak kommunikation, humor och att bli motsagd när något låter för bra.
- Dagtid: Chef Trygghetstjänster på Länsförsäkringar Gävleborg, ansvarig för Alf
  (proaktiv trygghetstjänst för smarta hem).
- Kvällar och helger: medgrundare av Successifier AB tillsammans med huvudgrundaren
  Rickard Collander. Fokus just nu: supportifier.se (AI-kunskapsbas för kundservice
  hos små och medelstora företag). Sajter: successifier.com, successifier.se.
- Politik: Moderaterna i Tierps kommun. Efter valet 2026 andra ersättare i
  kommunfullmäktige. Politikkortet länkar till kommunens webb-tv från fullmäktige.
- LinkedIn: https://www.linkedin.com/in/martincarlsson/ (nyligen bytt från
  martincarlsson1; publik profil är påslagen). Instagram: @martinizi.
  Facebook: https://www.facebook.com/martin.carlsson. E-post: martin.carlsson@gmail.com
  (visas på sajten, men aldrig i klartext i källkoden, se Teknik).

## Teknik
- Ren statisk HTML, ingen byggprocess, inga ramverk, inga npm-paket. Håll det så.
- Filer: index.html (allt innehåll, CSS, JavaScript och schema.org Person-markering i
  en fil), martin-carlsson.jpg (porträtt 880x1100, ~145 KB), martin-carlsson-og.jpg
  (delningsbild 1200x630 för og:image), robots.txt, sitemap.xml, .nojekyll, CNAME.
- CNAME innehåller `martincarlsson.se` och skapades av GitHub när domänen kopplades.
  Ta inte bort den, då slutar domänen fungera.
- Hostas på GitHub Pages från branchen main, mappen / (root). Enforce HTTPS är på.
  DNS ligger hos one.com: fyra A-poster för @ till GitHubs IP-adresser
  (185.199.108–111.153) och CNAME för www till martinizi81.github.io.
- Fonter från Google Fonts (Bricolage Grotesque, Source Sans 3, IBM Plex Mono).
- Design (sedan 2026-09-26): stor typografi i hjälten med "Carlsson" som kontur,
  porträttet i bågform med flytande skylt, rullande textremsa (ticker), "Fel Martin?"-
  ruta, de tre rollerna som bento-kort, quiz, kontaktlänkar som chips. Mjuka
  färgfläckar i bakgrunden animeras långsamt. Sektioner tonas in vid skroll via
  IntersectionObserver; utan JavaScript visas allt direkt.
- Sidan har ljust och mörkt tema via CSS-variabler i :root. Behåll båda.
- All rörelse stängs av vid prefers-reduced-motion. Behåll det.
- Quizet "Vilken Martin Carlsson letar du efter?": fyra frågor, svar i slumpad ordning,
  tangenter A–D, resultat via aria-live. Ingen data sparas eller skickas. Inga påståenden
  om de andra Martin Carlsson utöver yrke (läkare, hockeyspelare, Sweden Rock-redaktör).
- E-posten ligger baklänges i två data-attribut (data-u, data-d) och sätts ihop i
  webbläsaren först när besökaren klickar "Klicka för att visa adressen". Kopiera-knapp
  med kvittens; markeringsförsök ger en knuff mot knappen; Ctrl+C kopierar ändå rätt.
  Lägg aldrig adressen i klartext i HTML eller i schema.org.
- "Mitt Tierp" (sedan 2026-10-02): tre ställen Martin själv valt ur en lista från
  Upplev Norduppland: Leufstabruk Bryggeri, Tierp Arena, Central Hotellet Tierp
  (centralhotellettierp.se; sajten svarar 403 på curl/robotar men 200 med vanlig
  webbläsar-User-Agent, så testa med -A "Mozilla/5.0 ..."). Plus "Lokala nyheter" med vanliga
  länkar till Nya Tierpsposten och tierp.se. Lägg aldrig till ställen Martin inte
  själv valt, och skriv bara fakta om dem, inte påhittade omdömen.
- Språk: svenska. lang="sv" på html-elementet.

## Arbetssätt (viktigt)
- En ändring i taget. Gör ändringen på en egen gren och skapa en pull request så
  Martin kan se diffen och godkänna. Pusha aldrig direkt till main utan att fråga.
  Mergea bara när Martin uttryckligen ber om det i den aktuella PR:en.
- Förklara vad du ändrat i vanlig svenska, inte i kodtermer.
- Uppfinn inga fakta om Martin. Om något saknas (datum, titlar, resultat): fråga.
- Rör inte schema.org-blocket (<script type="application/ld+json">) utan att säga
  till; det är det som talar om för Google vem sidan handlar om. Uppdatera det när
  länkar eller titlar ändras i synligt innehåll (sameAs ska spegla länkarna under
  "Hitta mig", utom e-post).
- Visa förhandsbilder innan Martin godkänner. Skärmdumpar kan tas med den
  förinstallerade Chromium (/opt/pw-browsers/chromium-*/chrome-linux/chrome,
  --headless=new --screenshot). Chromium vägrar fönster smalare än 500 px, så
  mobilvy testas genom att ladda sidan i en 390 px bred iframe. Google Fonts laddas
  inte i sandlådan, så skärmdumpar visar ersättningstypsnitt. Använd
  --force-prefers-reduced-motion så att intoningar inte fångas halvvägs.
- Bilder till sajten hämtas enklast via Google Drive med "Alla som har länken" och
  curl mot https://drive.google.com/uc?export=download&id=... (bilder som klistras
  in i chatten sparas inte som filer). Ta bort EXIF-data när bilder sparas om.

## Klart sedan lanseringen (2026-09-27)
- Google Search Console: domänegendomen martincarlsson.se verifierad (TXT hos one.com),
  sitemap.xml inskickad och läst av Google samma dag ("Lyckades", 1 sida). En gammal
  egendom http://www.martincarlsson.se (från 2012) ligger kvar och kan tas bort; den
  visar att domänen har historik hos Google sedan 2012.
- Bing Webmaster Tools: importerad från Search Console. Sidan indexerad, inga SEO-fel,
  Bing läser både JSON-LD och OpenGraph.
- Inlänkar: martincarlsson.se är inlagd på LinkedIn, Facebook och Instagram.
- LinkedIn-inlägg om sajten publicerat 2026-09-27:
  https://www.linkedin.com/feed/update/urn:li:activity:7509898090208927744/
- GitHub: kontot mc1successifier (det Claude jobbar som) har skrivrättighet på repot.

## Öppna punkter
- Avstämning 2026-10-11 (påminnelse satt i Claude): syns sajten på "Martin Carlsson
  Tierp" och "Martin Carlsson Länsförsäkringar" i Google och Bing?
- "Läsvärt" (egen sida /lasvart/ med Martins kommentarer och eget RSS-flöde) är
  beslutat 2026-10-02 men väntar på 4–5 artiklar med kommentarer från Martin.
  Automatiskt nyhetsflöde från andra sajter är medvetet bortvalt (okontrollerade
  rubriker bredvid Martins namn, kräver byggprocess, ger inget på Google).
- Framtida idéer, ej beslutade: länka Rickard Collander, en kort "Skrivet"-sektion
  med länkar till inlägg, egen e-postadress på domänen (martin@martincarlsson.se)
  i stället för Gmail.
