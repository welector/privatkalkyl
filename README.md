# privatkalkyl

Beta av **privatkalkyl.se** — svenska kalkylatorer för privatekonomi, en HOBL-based service. Första verktyget är en bröllopsbudget.

Sajten är en enda fristående HTML-fil. Den behöver ingen server, ingen databas och inget byggsteg — allt körs i besökarens webbläsare.

## Filer

| Fil | Beskrivning |
| --- | --- |
| `index.html` | Hela sajten, självständig och färdig att publicera |
| `README.md` | Den här filen |
| `.gitignore` | Ignorerar skräpfiler från operativsystem och editorer |

## Publicera med GitHub Pages

1. Ladda upp filerna i det här repot (`Add file → Upload files` på repots startsida).
2. Gå till **Settings → Pages**.
3. Under *Build and deployment*, välj **Deploy from a branch**.
4. Välj branch `main` och mapp `/ (root)`. Spara.
5. Efter någon minut ligger sajten på `https://welector.github.io/privatkalkyl/`.

## Koppla domänen privatkalkyl.se

1. Lägg till domänen under **Settings → Pages → Custom domain**. GitHub skapar då en `CNAME`-fil i repot åt dig.
2. Hos din domänleverantör pekar du domänen till GitHub Pages:
   - `A`-poster för `privatkalkyl.se` till `185.199.108.153`, `185.199.109.153`, `185.199.110.153` och `185.199.111.153`
   - `CNAME`-post för `www` till `welector.github.io`
3. Kryssa i **Enforce HTTPS** när certifikatet är utfärdat (kan ta upp till en timme).

## Integritet

Sajten har en integritetssektion längst ned (`#integritet`) som beskriver att inga uppgifter samlas in, att budgeten lagras i besökarens egen webbläsare och att inga cookies eller spårningsverktyg används.

**Innan lansering:** kontrollera att e-postadressen `hej@privatkalkyl.se` finns och tas emot — den står som kontaktväg i både integritetssektionen och sidfoten.

Om ni senare inför konton, molnlagring, statistikverktyg eller annonser måste den sektionen uppdateras och en samtyckesbanner läggas till.

## Att veta om betan

- Användarens budget sparas i webbläsarens `localStorage`. Inget skickas till någon server, och det finns inget konto — data försvinner om besökaren rensar webbläsardata eller byter enhet.
- Besökaren kan exportera sin budget till en CSV-fil som öppnas i Excel, och läsa in samma fil igen.

## Nästa steg

Sidan renderas med JavaScript och har i dag en enda URL. Inför skarp drift bör innehållet flyttas till en riktig sidstruktur med egna adresser per kalkylator och artikel (`/brollopsbudget`, `/guider/...`), server-renderad HTML, sitemap och metadata per sida — det är vad som krävs för att guiderna ska ge effekt i sök.
