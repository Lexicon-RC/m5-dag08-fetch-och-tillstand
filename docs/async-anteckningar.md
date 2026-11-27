# Utsätt sidan för fel

1. Offline i listan No throttling, ladda om och se felet

   > Failed to Load Page
   > ERR_INTERNET_DISCONNECTED (-106)
   > URL: http://localhost:5173/?stad=kiruna

2. Slow 3G, ladda om

   > Laddar… en stund innan vädret visas

3. Ändra "data/meny.json" till "data/finns-inte.json" och se vad som händer

   > Istället för menykorten blev det ett felmeddelande:
   > Något gick fel: Unexpected token '&lt;', "&lt;!DOCTYPE "... is not valid JSON
   > med en försök igen-knapp

4. Töm meny.json till [] och se tomt.

   > Inga rätter hittades.

# Funktionen falskFetch

## Hur fungerar falskFetch?

falskFetch "fejkar" en riktig fetch som gör HTTP-förfrågan över nätverket. Den falska fetchen returnerar ett enkelt objekt med ok, status och json baserat på parametrarna data och status.

## Varför ska vi testa med en falsk fetch istället för den riktiga?

Det finns flera anledningar bl.a.

1. Testerna blir snabbare, behöver inte vänta på nätverket
2. Testerna blir kontrollerbara, d.v.s. svarar alltid som beskrivet och är inte beroende av yttre faktorer som t.ex. att API:et är nere
3. Enkelt att testa ovanliga svar som inte är så lätta att få från API-servar
