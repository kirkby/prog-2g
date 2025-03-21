# Årsopgave i programmering 

Læs disse punkter **grundigt** før du går i gang

- Løs så mange opgaver som du kan i løbet af projektet
- Der må ikke bruges AI, heller ikke Copilot
- Få hver løsning godkendt før du går videre til næste opgave
- Man må gerne samarbejde men alle afleverer individuelt
- Husk at kommentere koden efter python-standarder

**github**
- Gemme din arbejde i github når du er færdig med en opgave
- Gem kun kode der fungerer i github

## Forberedelser 
Repo: https://github.com/kirkby/prog-2g/tree/main/aarsopgave

- [ ] Opret en mappe ved navn "aarsopgave" der hvor du har din kode.
- [ ] Hent filerne fra repo'et og læg dem i den nye mappe
- [ ] Åben VS Code (Nuf)
- [ ] Vælg File->Open Folder og tilføj mappen "aarsopgave"
- [ ] Vælg File->Save workspace og giv den navnet "aarsopgave"
- [ ] Kontroller af koden fungerer

#### Opret Github repo
- [ ] Opret konto hos github.com
- [ ] Tilføj din login oplysninger i accounts (nederste venstre hjørne)
- [ ] Tilføj en fil README.MD med en kort beskrivelse af projektet
- [ ] Skub din README.md op i dit repo. 

## Filer
Opgaven består af følgende filer:
- main.py
- price_list.py
- shopping_list.py
- price_list.csv

## Klasser
Opgaven består af følgende klasser:

**PriceList**  
Denne klasse håndterer en prisliste (en list af produkter med priser).
Til klassen hører en csv-fil med data, `price_list.csv`.

**ShoppingList**  
Denne klasse håndterer en indkøbsliste af produkter.

## Opgave A
Lav en ny udgave af `shopping_list` som tilføjer antal, således
at man angive flere af samme produkt, fx 2 Boosters.

:information_source: Tip: skift datatype for listen `items` i klassen `shopping_list` fra "liste" [] (list) til "opslagsliste" {} (dictionary)

Test det med at oprette en instans af objektet `shopping_list` og test alle dens metoder - `add()`, `remove()`, `get_items()` 

## Opgave B
Tilføj en produktbeskrivelse til hvert produkt på `price_list`.

:information_source:Tip: opdater klassen price_list og datafilen, brug en dictionary.  
:information_source:Tip: fx dictionary med denne struktur
```
{'Booster': {descriptions:'Kongen af energidrikke','price':25}}
```
  
Test det med at oprette en instans af objektet `price_list` og udskriv listen af produkter med pris og beskrivelse.

## Opgave C
Byg klassen `price_list` ind i klassen `shopping_list` så denne klasse selv kan beregne priser. Håndter den situation hvor varen ikke er på prislisten.

:information_source: Tip: klassen `shopping_list` skal have en variabel som er en instans af `price_list`.
Lav en metode som looper gennem alle varer på shoppinglisten, og for hvert enkelt vare henter prisen i prislisten.
Brug metoden `get_price` i `price_list` til at hente prisen for hvert enkelt vare.
Loop gennem alle varer og udskriv prisen.

```
def __init__(self):
        self.items = []
        self.price_list = PriceList()
```

Test det med at oprette en instans af objektet `shopping_list` og udskriv listen af produkter med priser.

## Opgave D
Lav en metode i `shopping_list` som udskriver det samlede beløb for alle varer på listen.

:information_source: Tip: Loop gennem listen og lægge alle beløbene sammen. 
```
def __init__(self):
        self.items = []
        self.price_list = PriceList()
```


Test det med at udskrive det samlede beløb for alle varer på indkøbslisten.

## Opgave E
Lav en menu i jeres main.py. Giv brugeren mulighed for at vælge hvilken funktion han vil bruge.

```
>python3 main.py
Annas indkøbsliste
MENU (vælg 1-5)
(1) Tilføj produkt til indkøbsliste
(2) Slet produkt fra indkøbsliste
(3) Udskriv indkøbsliste
(4) Tilføj produkt til prisliste
(5) Gem prisliste til fil
(osv.)
(Q) Quit
```

:information_source: Tip: Se tidligere opgaver hvordan man laver en menu.

## Opgave F
Lad klassen `price_list` hente prislisten fra nettet, fx herfra:
curl https://kirkby.github.io/price_list.json

Tjek data med curl
``` bash 
mkm@MacBookAir ~ % curl -s https://kirkby.github.io/price_list.json
{
    "Booster": 25,
    "Velo": 54,
    "Pizza": 85,
    "Big Mac Menu": 75
}%  
```

Tip: kig i de gamle eksempler og find en løsning på hvordan man requester data fra et api.


Bemærk: denne liste har ikke produktbeskrivelser. Hvad gør vi så? Kan man lægge det på sit egen github?

## Opgave G
Har du mere tid?  
Giv din app en grænseflade med `tkinter`.  

