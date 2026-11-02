# Methodology

## Analytical reasoning chain
1. Observed: fans converge on few corridors in a 90-min window (Exhibition Place event traffic
   reports).
2. Modeled: gate throughput about 120 fans per lane-hour (IAVM venue guidelines).
3. Conceptual relationship: wait approximates arrivals divided by throughput; this informs the shape
   of the match-clock presets. Exact preset values (6, 12, 30 min) are illustrative scenario
   parameters, not computed from a measured arrival count.
4. Compared: three modes on time, cost and CO₂e. CO₂e factors from DEFRA 2024 (car) and
   representative published ranges (transit, shuttle); fares from TTC published rates.
5. Scaled: single-fan results times a converted-trips cohort. Illustrative, not predictive.

## Sourced vs illustrative

Sourced:
- DEFRA 2024 car factor: 0.21 kg per vehicle-km, single occupant
- TTC PRESTO base fare: about $3.35
- Published event parking rates: $15 to $20
- IAVM gate throughput standard: 120 fans per lane-hour
- Transit and shuttle CO₂e factors: 0.11 and 0.15 kg per km, as representative published ranges for
  urban transit and diesel shuttle emissions, not venue-specific measurement

Illustrative (scenario parameters):
- Trip distances (car 20.0 km, transit 21.8 km, shuttle 20.7 km)
- Pre-gate time components (eco 12, shuttle 8, car 33 min)
- Cohort size (1,900) and mode-shift percentages (72% to 38% car share)
- Gate-wait curve and its assumed growth rate (+6.5 wait-min per hour)
- Eco-route bundled fare components beyond the PRESTO base ($3.50 total)

## Two independent layers
The time model (door-to-gate components) and the carbon model (factor times routed distance) are
calibrated separately. They are not outputs of a single origin-destination simulation. Combining the
two layers to derive implied speeds is outside their intended use.

## Status bands and presets
Bands (single definition used everywhere): CLEAR under 10 min, MODERATE 10 to 16, HEAVY 17 and above.

Presets (total door-to-gate, min):
- Quiet 12:00, network gate 6: eco 18, shuttle 14, car 39
- Rising 17:30, network gate 12 (headline): eco 24, shuttle 20, car 45
- Peak 18:45, end-state worst case, individual gates 17 to 30, worst-case 30 used in totals:
  eco 42, shuttle 38, car 63

Note: the 12-min eco pre-gate component and the 12-min Rising network-average gate wait are two
unrelated figures that happen to share the same value.

## Cohort math
1,900 attendees (illustrative round number, about one stand section). Baseline car share 72% equals
1,368 car trips. Scenario car share 38%. Converted car trips: 646. Avoided CO₂e: 646 times 1.8 kg,
about 1.2 t. Traveler savings: 646 times $14.50, about $9.4K.

Sensitivity: a 70/30 eco-shuttle split gives about 1.0 t and about $9.1K, confirming the result is
not eco-split dependent.

Upper bound (separate hypothetical cohort, 1,900 car trips fully converted): baseline about 8.0 t,
all-eco about 4.6 t, avoided about 3.4 t, savings about $27.5K. The dashboard KPI 3.42 t refers to
this upper-bound case. Both cohorts use the same round number (1,900) purely for narrative
simplicity; they represent different hypothetical populations.

## Limitations
- Simulated data; no live city feeds connected.
- Scenario modeling and desk research; no user testing or live operational data.
- One deep Toronto scenario; US applicability via planning-level transferability checks (MetLife,
  Lumen Field), not deployment.
- Peak arrival modeled; post-match egress not modeled.
- Default eco route assumes micromobility access; step-free alternatives planned, not built.
- In-vehicle and parking-search component held constant (33 min) across match-clock states.
- Cost figures use flat bundled values, not itemized real-time pricing.
- Carbon factors from DEFRA (UK); Canada/US-specific factors would differ slightly.
