# Data dictionary

Every locked parameter, its value, its class, and where it appears. This file is the source of
truth: if a number changes anywhere, it changes here first.

| Parameter | Value | Class | Used in |
|---|---|---|---|
| Car distance | 20.0 km | illustrative | carbon model |
| Car factor | 0.21 kg/vehicle-km | sourced (DEFRA 2024) | carbon model |
| Car CO₂e | +4.2 kg | computed | planner, dashboard |
| Transit distance | 21.8 km | illustrative | carbon model |
| Transit factor | 0.11 kg/km | sourced (representative range) | carbon model |
| Transit CO₂e | +2.4 kg | computed | planner |
| Shuttle distance | 20.7 km | illustrative | carbon model |
| Shuttle factor | 0.15 kg/km | sourced (representative range) | carbon model |
| Shuttle CO₂e | +3.1 kg | computed | planner |
| Avoided, eco | 1.8 kg | computed | headline, planner |
| Avoided, shuttle | 1.1 kg | computed | planner |
| Eco fare | $3.50 (bundled) | illustrative | planner |
| Shuttle fare | $5.00 | illustrative | planner |
| Car cost | $18.00 (about $15 parking + $3 fuel) | illustrative split | planner |
| Eco pre-gate | 12 min | illustrative | totals |
| Shuttle pre-gate | 8 min | illustrative | totals |
| Car pre-gate | 33 min | illustrative | totals |
| Gate presets | 6 / 12 / 30 min | illustrative | presets |
| Status bands | under 10 / 10 to 16 / 17 and above | definition | UI, docs |
| Growth rate | +6.5 wait-min per hour | illustrative | trend |
| Trend | Gate C 14 min crosses HEAVY in about 28 min | computed | dashboard |
| Cohort | 1,900 | illustrative | scenario panel |
| Car share | 72% to 38% | illustrative | scenario panel |
| Converted trips | 646 | computed | scenario panel |
| Avoided, match | about 1.2 t | computed | scenario panel |
| Savings, match | about $9.4K | computed | scenario panel |
| Sensitivity | about 1.0 t / about $9.1K | computed | scenario panel |
| Upper bound | about 3.4 t / about $27.5K (KPI 3.42 t) | computed | panel, KPI |
| Mode split | 34 / 18 / 12 / 4 / 32 % | illustrative | impact panel |
| Intensity | 171 / 41 / 28 / 0 g per fan-km | illustrative | impact panel |
| KPI adoption | 68% | scenario assumption | KPI tile |
| KPI fans | 24,318 | modeled | KPI tile |
| KPI congestion | 7.2/10 | modeled | KPI tile |
