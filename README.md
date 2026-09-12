# Locked Map Card

Tynd wrapper omkring Home Assistants indbyggede `map`-kort: låser panoreringen til den position du angav i konfigurationen, men lader zoom-knapperne blive ved med at virke (det indbyggede kort låser normalt begge dele sammen).

```yaml
type: custom:locked-map-card
lock_pan: true
entities:
  - person.familie
  - device_tracker.bil
```

## Config

Accepterer al almindelig `map`-kort-konfiguration (`entities`, `hours_to_show`, `default_zoom`, osv.) — den sendes videre uændret til det indre kort.

| Felt | Type | Standard |
|---|---|---|
| `lock_pan` | bool | — forbruges af wrapperen (låser panorering) og strippes før resten af config sendes til det indlejrede `map`-kort |

## Installation

1. Kopiér `locked-map-card.js` til `/config/www/`.
2. Tilføj som Lovelace-resource: `/local/locked-map-card.js?v=1`, type `module`.
3. Brug det som et almindeligt map-kort, med `lock_pan: true` hvis panoreringen skal låses.
