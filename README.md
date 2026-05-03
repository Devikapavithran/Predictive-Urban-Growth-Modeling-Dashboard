# PS-3 · Predictive Urban Growth Modeling Dashboard

**A predictive geospatial analytics engine that identifies real estate investment hotspots by fusing municipal declarations, market intelligence, and OSINT signals into a unified Growth Velocity Score — projected over a 24–60 month horizon.**

[🚀 Live Demo](https://devikapavithran.github.io/Predictive-Urban-Growth-Modeling-Dashboard/) &nbsp;·&nbsp; [📄 Problem Statement](#problem-statement) &nbsp;·&nbsp; [⚙️ Features](#features) &nbsp;·&nbsp; [🧠 How It Works](#how-it-works)

</div>

---

## Problem Statement

Real estate firms face significant financial risk when committing capital to new developments without a data-driven understanding of **"High-Growth Zones."** The core challenges are:

- **Data Fragmentation** — Municipal Corporation declarations are disconnected from market sentiment data on portals like 99acres or MagicBricks
- **The Insight Gap** — No unified system to correlate rent and selling prices with upcoming government projects like metro lines, sewage expansions, or zoning changes
- **Subjective Forecasting** — Expansion strategies rely on gut feeling rather than multi-dimensional analysis of supply, demand, and legislative intent

> **The objective:** Build a Predictive Geospatial Analytics Engine that identifies future hotspots by correlating municipal lead indicators against market demand indicators — projected onto a heat-mapped dashboard over a 24–60 month horizon.

## Features

### 🗺️ Interactive Geospatial Heat Map
- 12 urban growth zones rendered on a tactical dark terrain map using HTML5 Canvas
- Heat blobs scaled by Growth Velocity Score — color gradient from yellow (low) to deep red (critical)
- Click any zone node on the map or in the sidebar to drill into full analytics
- Real-time pulse animations on high-GVS zones indicating active growth pressure

### 🔀 4 Toggleable Intelligence Layers
| Layer | What It Shows |
|---|---|
| `HEAT MAP` | GVS heat blobs — full growth velocity picture across all zones |
| `MUNICIPAL` | Pulsing rings showing municipal declaration intensity per zone |
| `MARKET` | Blue rings showing 99acres/MagicBricks activity depth |
| `INFRA PROJECTS` | Dashed amber corridors showing proposed infrastructure linkages |

### 📊 Growth Velocity Score (GVS) Engine
- Each zone scored 0–100 across 4 weighted components:
  - **Municipal Declarations** — CLU changes, infrastructure tenders, public works
  - **Market Activity** — listing density, price/sqft trends, portal search volume
  - **OSINT Sentiment** — news NLP, social signals, developer buzz
  - **Listing Density** — supply saturation and absorption rates
- GVS formula weights municipal data as the **lead indicator** and market data as the **demand indicator** — mirroring the correlation model from the problem statement

### 📈 Appreciation Forecast (24 / 36 / 60 Month Horizons)
- Per-zone forecast bars covering Price Appreciation, Rental Yield Delta, Market Depth, Infrastructure Impact, and Overall ROI Score
- Horizon selector (24 / 36 / 60 months) dynamically recalculates all forecast values
- Directly implements the PS-3 requirement for projecting findings over a **24–60 month development horizon**

### 📡 Live Intelligence Feed
- Per-zone signal feed showing government tender notifications, market spike alerts, and OSINT-flagged developer activity
- Color-coded by source type: green (government), blue (market), purple (OSINT)
- Simulated continuous data stream at the bottom showing ingestion from municipal portals, 99acres, MagicBricks, and NLP pipelines

### 🏙️ Zone KPI Panel
- Real-time KPIs per selected zone: Price/Sq Ft, Rental Yield %, Price Velocity %/yr, GVS Score
- Component breakdown bars showing exact contribution of each data source to the GVS

---

## How It Works

```
Multi-Source Data Ingestion
          │
    ┌─────┴──────────────────────┐
    ▼                            ▼
Municipal Declarations      Market Intelligence
(CLU, Tenders, Infra)      (99acres, MagicBricks,
                            Listing Density, Pricing)
    │                            │
    └──────────┬─────────────────┘
               ▼
       OSINT Sentiment Layer
       (News NLP, Social Signals,
        Developer Activity)
               │
               ▼
    ┌──────────────────────┐
    │  Correlation Engine   │
    │                      │
    │  GVS = w1×Municipal  │
    │      + w2×Market     │
    │      + w3×OSINT      │
    │      + w4×Listing    │
    └──────────┬───────────┘
               │
               ▼
    ┌──────────────────────┐
    │  Trend Analysis       │
    │  Rental Yield Delta   │
    │  RTM vs UC Price Gap  │
    │  Appreciation Velocity│
    └──────────┬───────────┘
               │
               ▼
    ┌──────────────────────┐
    │  Heat-Mapped Dashboard│
    │  24 / 36 / 60 Month   │
    │  Projection Horizon   │
    └──────────────────────┘
```

### GVS Scoring Tiers

| GVS Range | Classification | Action Signal |
|---|---|---|
| 85 – 100 | 🔴 Critical Growth | Immediate first-mover entry |
| 75 – 84 | 🟠 High Growth | Prioritize for acquisition |
| 65 – 74 | 🟡 Moderate Growth | Monitor — watch for triggers |
| Below 65 | 🔵 Low / Stable | Hold — no immediate action |

---

## Data Sources Modeled

| Data Stream | Source Type | Analytical Value |
|---|---|---|
| Municipal Declarations | Government Portals / PDFs | Anticipates new roads, utilities, and transport hubs |
| Listing Density | 99acres / MagicBricks | Measures developer activity and competition saturation |
| Pricing Velocity | Real Estate Portals | Tracks appreciation rate — RTM vs Under Construction |
| Rental Absorption | Online Portals | Indicates actual residency demand and population shift |
| OSINT Signals | News NLP / Social | Developer buzz, corporate relocations, zoning news |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Rendering | HTML5 Canvas API — terrain map, heat blobs, node animations |
| Frontend | Vanilla JavaScript — zero framework, zero dependencies |
| Fonts | Syne + JetBrains Mono (Google Fonts) |
| Intelligence Engine | Custom GVS scoring with weighted multi-source correlation |
| Deployment | GitHub Pages — single file, instant load |

---

## Problem Statement Coverage

| PS-3 Requirement | Implementation |
|---|---|
| Public sector ingestion (municipal tenders, CLU) | Municipal layer with per-zone tender signal feed |
| Market intelligence ingestion (99acres, MagicBricks) | Market layer with listing density and pricing velocity |
| Correlation model — lead vs demand indicator | GVS formula weights municipal as lead, market as demand |
| Trend analysis — rental yield vs selling price delta | Per-zone Rental Yield KPI + Appreciation Velocity metric |
| Visual projection — heat-mapped dashboard | Heat map layer with color-scaled GVS blobs |
| 24–60 month horizon | Horizon selector with dynamic forecast recalculation |

---



## Author

**Devika Pavithran**
Built as part of a senior-level intelligence systems and AI engineering challenge.
