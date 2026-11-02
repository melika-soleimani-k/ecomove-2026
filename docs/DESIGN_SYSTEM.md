# Design system (v1.0)

Dark-first, high-contrast tokens for night-match readability. 100% token coverage across both
screens.

## Color tokens

| Token | Hex | Role |
|---|---|---|
| --bg | #0B0E14 | app background |
| --surface | #101624 | cards and panels |
| --ink | #E8EDF6 | primary text |
| --muted | #8B96AB | secondary text |
| --eco | #10B981 | eco, clear, success |
| --transit | #06B6D4 | interactive, transit, CTA |
| --ai | #8B5CF6 | shuttles, AI routing |
| --heavy | #EF4444 | heavy congestion, LIVE |
| --moderate | #F59E0B | moderate, warnings |

## Type
Plus Jakarta Sans for display and headers, Inter for body, JetBrains Mono for live data readouts.
Scale: display 44/1.1, H1 26/1.2, H2 18, kicker 12 uppercase with 0.2em tracking, body 15/1.6,
data readouts tabular.

## Radius and motion
Radius: 8 (buttons, inputs), 12 (chip rows, QR card), 18 (panels, cards), 999 (badges, toggles).
Motion: micro 150ms ease-out (hover, chips), state 300ms cubic(.2,.7,.2,1) (toggles, selects),
scene 500 to 700ms same curve (view entry), ambient 2.6 to 12s loop (LIVE pulse, map flow).

## Layout
Breakpoints: mobile under 640 (stacked), tablet 640 to 1120 (map above sidebar), desktop 1120 and
above (map plus 348px rail). Grid: 12 columns, 24px gutters, max-width 1440. Map min-height 520.

## Handoff
The in-app `05 Handoff Tokens` view exports the same :root block used here, so React
implementations inherit identical values.
