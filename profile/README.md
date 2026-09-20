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

- De **landelijke voorziening WOZ** levert alleen aan afnemers die de wet aanwijst: gemeenten,
  waterschappen en de Belastingdienst, bestuursorganen met een wettelijke taak, en als derde
  groep verzekeraars, hypotheekverstrekkers en door NRVT gecertificeerde validatie-instituten.
  Bron: [artikel 37a Wet WOZ](https://wetten.overheid.nl/BWBR0007119/2024-01-01/0/HoofdstukVI/Artikel37a/)
  en [Kadaster, WOZ voor afnemers](https://www.kadaster.nl/zakelijk/registraties/landelijke-voorzieningen/woz/woz-voor-afnemers),
  gecontroleerd op 20 september 2026.
- Het **WOZ-waardeloket** is een raadpleegsite zonder API en staat geautomatiseerd onttrekken
  niet toe.
- **WOZ+** is een licentieproduct met een aansluittraject.

WozApi is de self-serve route: account aanmaken, 10 gratis credits, eerste call binnen een paar
minuten. 1 credit is 1 uniek adres; hetzelfde adres binnen 7 dagen opnieuw opvragen is gratis.

## Open cijfers

We publiceren de ontwikkeling van de gemiddelde WOZ-waarde
[per provincie en per gemeente](https://woz-api.nl/woz-waarde-ontwikkeling), met een
downloadbare dataset. Bron: CBS StatLine, vrij te gebruiken met bronvermelding.
