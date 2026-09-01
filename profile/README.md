<img src="https://raw.githubusercontent.com/WozApi/.github/main/profile/logo.png" alt="" width="88" align="right">

# WozApi

**WOZ-waarde, BAG-adresgegevens en kadastrale percelen van elk Nederlands adres via 1
API-endpoint.** Voor developers, proptech, fintech, makelaardij, notariaat en datateams.

[woz-api.nl](https://woz-api.nl) &middot; [API-documentatie](https://woz-api.nl/swagger/index.html) &middot; [Prijzen](https://woz-api.nl/woz-api-prijs)

## Clientlibraries

| Taal | Repository |
|---|---|
| Python, Node.js en .NET | [wozapi-clients](https://github.com/WozApi/wozapi-clients) |

Alle drie zonder externe afhankelijkheden, MIT-licentie.

```python
from wozapi import WozApi

client = WozApi("jouw-api-key")
adres = client.adres("Spuistraat 36C, 1012 TT Amsterdam")
print(adres["woz"][0]["vastgesteldeWaarde"])
```

## Waarom deze API bestaat

De officiële routes naar WOZ-data zijn voor de meeste bouwers gesloten:

- De **WOZ API Bevragen** van het Kadaster is alleen voor gemeenten en vereist een OIN plus een
  PKIoverheid-certificaat.
- Het **WOZ-waardeloket** is een raadpleegsite zonder API en staat geautomatiseerd onttrekken
  niet toe.
- **WOZ+** is een licentieproduct met een aansluittraject.

WozApi is de self-serve route: account aanmaken, 10 gratis credits, eerste call binnen een paar
minuten. 1 credit is 1 uniek adres; hetzelfde adres binnen 7 dagen opnieuw opvragen is gratis.

## Open cijfers

We publiceren de ontwikkeling van de gemiddelde WOZ-waarde
[per provincie en per gemeente](https://woz-api.nl/woz-waarde-ontwikkeling), met een
downloadbare dataset. Bron: CBS StatLine, vrij te gebruiken met bronvermelding.
