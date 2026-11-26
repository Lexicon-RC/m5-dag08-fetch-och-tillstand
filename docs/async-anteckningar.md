# Funktionen falskFetch

## Hur fungerar falskFetch?

falskFetch "fejkar" en riktig fetch som gör HTTP-förfrågan över nätverket. Den falska fetchen returnerar ett enkelt objekt med ok, status och json baserat på parametrarna data och status.

## Varför ska vi testa med en falsk fetch istället för den riktiga?

Det finns flera anledningar bl.a.

1. Testerna blir snabbare, behöver inte vänta på nätverket
2. Testerna blir kontrollerbara, d.v.s. svarar alltid som beskrivet och är inte beroende av yttre faktorer som t.ex. att API:et är nere
3. Enkelt att testa ovanliga svar som inte är så lätta att få från API-servar
