# ParkMap Sverige

> AI-driven parkeringsdata for hela Sverige — ett Maxine Platform-projekt.

## Live

| URL | Beskrivning |
|-----|-------------|
| [maxineplatform.com](https://maxineplatform.com) | Maxine Platform — huvudsida |
| [maxineplatform.com/parkmap/](https://maxineplatform.com/parkmap/) | ParkMap kartapp (Luleå pilot) |
| [maxineplatform.com/data/regions/norrbotten/lulea.geojson](https://maxineplatform.com/data/regions/norrbotten/lulea.geojson) | GeoJSON API — Luleå zoner |

## Struktur

```
/
├── index.html                          # Maxine Platform landing page
├── CNAME                               # GitHub Pages custom domain
├── .nojekyll                           # Bypass Jekyll
├── parkmap/
│   └── index.html                      # Leaflet.js kartapp (dark theme)
└── data/
    ├── schema/
    │   └── parkmap-geojson-schema.json  # GeoJSON Feature schema
    ├── operators/
    │   └── lulea-operators.json         # Operatörer med färg, typ, kontakt
    └── regions/
        └── norrbotten/
            └── lulea.geojson           # 93 parkeringszoner
```

## Operatörer (Luleå pilot)

| Operatör | Typ | Färg |
|----------|-----|------|
| Luleå kommun | Kommun | 🔵 `#3b82f6` |
| Aimo Park | Privat | 🟠 `#f97316` |
| Lulebo | Kommunalt bolag | 🟣 `#a855f7` |
| APCOA | Privat | 🔴 `#ef4444` |
| Swedavia | Statligt bolag | 🔵 `#06b6d4` |
| Galären | Privat | 🟡 `#eab308` |

## Tech

- **Kartapp**: Leaflet.js + CartoDB dark tiles + GeoJSON overlay
- **Data**: Genererad av `parkmap-agent` (Factory 10) — AI-scraper med 6 crew-agenter
- **Hosting**: GitHub Pages via `main` branch
- **Domän**: `maxineplatform.com` (Cloudflare DNS)

## Roadmap

- [ ] Fler kommuner: Boden, Piteå, Kiruna
- [ ] Realtidspriser via operatörs-API:er
- [ ] Automatisk daglig uppdatering via CI/CD
- [ ] Sökbar operatörslista per region

---

*En del av [Maxine Platform](https://maxineplatform.com) — The Cognitive OS for the Autonomous Enterprise.*
