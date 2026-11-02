# EcoMove 2026

**FIFA World Cup Host-City Mobility Readiness Platform**

[Live prototype](https://melika-ux.github.io/ecomove-2026/) ·
[Figma file](https://www.figma.com/design/yjJT4FPQpFr8abyhuHAfTW/final-eco-move-design?node-id=0-1&t=GPs58K2js8ZGCC4e-1) ·
[Hackathon entry](https://devpost.com/software/ecomove-2026)

![license](https://img.shields.io/badge/license-MIT-green)
![status](https://img.shields.io/badge/status-concept%20prototype-blue)
![data](https://img.shields.io/badge/data-simulated-orange)
![build](https://img.shields.io/badge/build-dependency--free-brightgreen)

EcoMove 2026 is a mobility-readiness concept for FIFA World Cup 2026 host cities. It pairs a
simulated match-day operations dashboard for city operators with a fan-facing eco route planner,
and both screens read the same match-clock scenario state. Toronto and BMO Field (Match 14) are the
demonstration case; the method was checked at planning level against MetLife Stadium (New York/NJ)
and Lumen Field (Seattle).

Built solo for the Rice University Urban Sustainability Hackathon (World Cup 2026 HACK),
Track 1: Transportation & Access. Official entry.

> Honest by design: every figure here is either sourced (published factors, fares, standards) or
> illustrative (scenario parameters), and the product labels them modeled or simulated in the UI.
> There are no live city feeds and no negative-carbon claims anywhere.

## Screens

### 1. Simulated operations dashboard
- Modeled KPIs, each labeled on its tile: 3.42 t CO₂e saved (upper-bound case), 68% transit adoption
  (scenario assumption), 24,318 active eco-fans, 7.2/10 congestion index
- Custom SVG traffic map with labeled road states (GARDINER EXPY HEAVY, DUFFERIN SLOW, KING ST
  FLOWING) and toggleable layers: transit, shuttles, traffic, micro-mobility, fan zones
- Gate Access panel with per-gate security waits and one shared vocabulary: CLEAR under 10 min,
  MODERATE 10 to 16, HEAVY 17 and above
- Match-clock presets (Quiet 12:00, Rising 17:30, Peak 18:45); at peak all four gates read HEAVY
  (17 to 30 min waits)
- Modeled outlook: at +6.5 wait-min per hour, Gate C at 14 min crosses HEAVY in about 28 min
- Sustainability impact: mode split (Transit 34%, E-Shuttle 18%, Bike/Scooter 12%, Walking 4%,
  Private car 32%) and per-fan-km intensity (CAR 171g, SHUTTLE 41g, TRANSIT 28g, BIKE 0g)
- City selector demonstrating the transferability template: Toronto, MetLife, Seattle

### 2. Fan eco route planner
- Trip setup (origin, venue plus gate, arrival time) and three honest options on time, fare, CO₂e:

| Option | Time | Fare | CO₂e |
|---|---|---|---|
| Eco Route (recommended) | 24 min | $3.50 | +2.4 kg (1.8 avoided vs driving) |
| Fast Express Shuttle | 20 min | $5.00 | +3.1 kg (1.1 avoided) |
| Standard Drive (baseline) | 45 min | $18.00 | +4.2 kg |

- Multimodal timeline: transit 6, walk 3, scooter 3 (illustrative 12-min pre-gate sequence covering
  the last mile)[cite: 2]
- QR Digital Fan Pass: one QR bundling transit, shuttle, dock and gate entry, one scan per touchpoint[cite: 2]
- The car is never hidden: honest comparison is a design principle, not a compromise[cite: 2]

## Modeled results

| Metric | Car baseline | Eco route | Impact |
|---|---|---|---|
| Door-to-gate time | 45 min | 24 min | -47% |
| Trip cost | $18.00 | $3.50 | -81% |
| CO₂e per fan | +4.2 kg | +2.4 kg | 1.8 kg avoided |
| Match-day scale | 72% car share | 38% car share (646 converted) | ~1.2 t avoided, ~$9.4K saved (3.42 t upper bound) |

All values are modeled against the Match 14 scenario; see [docs/METHODOLOGY.md](docs/METHODOLOGY.md)
for the sourced-versus-illustrative split[cite: 2].

## Quick start

No build step, no dependencies[cite: 2].

```bash
# option 1: open directly
open index.html

# option 2: serve locally
python3 -m http.server 8000
# then visit http://localhost:8000
