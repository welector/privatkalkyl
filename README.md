# privatkalkyl

Beta av **privatkalkyl.se**: svenska kalkyler och budgetar för privatekonomi. Bröllopsbudgeten är klar att använda. Bolånekalkyl, bilkalkyl, hushållsbudget, evenemangsbudget och starta eget-kalkyl finns som utkast, tillsammans med guider till varje kalkyl.

Sajten är en enda fristående HTML-fil. Den behöver ingen server, ingen databas och inget byggsteg. Allt körs i besökarens webbläsare. Typsnitten (Fraunces och Figtree) hämtas från Google Fonts, med systemtypsnitt som reserv.

## Filer

| Fil | Beskrivning |
| --- | --- |
| `index.html` | Hela sajten, färdig att publicera |
| `CNAME` | Kopplar GitHub Pages till domänen privatkalkyl.se |
| `README.md` | Den här filen |

## Publicering

Sajten publiceras med GitHub Pages från branch `main`, mapp `/ (root)`. En ändring i `main` syns på privatkalkyl.se efter ett par minuter.

Domänen ligger hos Loopia. DNS:

- Fyra `A`-poster för `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153` och `185.199.111.153`
- `CNAME` för `www`: `welector.github.io.`
- En `TXT`-post för `@` med verifieringen till Google Search Console. Låt den ligga kvar.

Repot måste vara publikt för att GitHub Pages ska fungera med ett gratiskonto.

## Integritet

Sajten har en integritetssektion (`#integritet`) som beskriver att inga uppgifter samlas in, att det besökaren fyller i lagras i den egna webbläsaren och att inga cookies eller spårningsverktyg används.

**Innan lansering:** kontrollera att e-postadressen `hej@privatkalkyl.se` finns och tas emot. Den står i integritetssektionen och sidfoten.

Om sajten senare får konton, molnlagring, statistikverktyg eller annonser måste integritetssektionen uppdateras och en samtyckesbanner läggas till.

## Att veta om betan

- Varje kalkyl sparar sina siffror i webbläsarens `localStorage`, med en egen nyckel per kalkyl. Inget skickas till någon server och det finns inga konton.
- Besökaren kan exportera en kalkyl till en CSV-fil som öppnas i Excel, och läsa in samma fil igen.
- Startvärdena i kalkylerna är exempel, inte uppmätta snittpriser. Guiderna saknar ännu prisuppgifter med källa.

## Nästa steg

Sajten har i dag en enda URL. För att guiderna ska ge effekt i sök behöver innehållet delas upp i egna sidor per kalkyl och guide (`/brollopsbudget`, `/guider/...`), med metadata per sida och en `sitemap.xml`.
