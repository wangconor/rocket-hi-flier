# Estes Hi-Flier OpenRocket Simulation

OpenRocket simulation file for the Estes Hi-Flier #2178, built from physical measurements of my kit components and cross-referenced against known Estes specifications.

## Key Finding: Minimum Diameter Design

The Hi-Flier is a **minimum-diameter rocket** — the BT-20 body tube doubles as the motor mount. There is no separate motor tube or centering rings. The 18mm motor slides directly into the body tube and is held by an external engine hook and Mylar retainer sleeve. A green fiber engine block ring is glued inside the tube to prevent the motor from sliding forward.

## Measurements

All components were measured with a ruler and a kitchen scale (1g resolution). Tube dimensions were corrected to published Estes BT-20 specifications since ruler measurements lack the precision needed for thin-wall tubes.

| Component | Parameter | Measured | Value Used in Sim | Notes |
|---|---|---|---|---|
| **Nose Cone** | Shape | Ogive | Ogive | PNC-20A |
| | Length | 71 mm | 71 mm | |
| | Shoulder length | 14 mm | 14 mm | |
| | Shoulder diameter | 16 mm | 16 mm | |
| | Base diameter | 18 mm | 18.69 mm | Corrected to BT-20 OD |
| | Mass | 12 g | 12 g | Includes clay ballast + plug |
| **Body Tube** | Length | 229 mm | 229 mm | |
| | Outer diameter | 17 mm | 18.69 mm | Corrected to BT-20 spec |
| | Inner diameter | 15 mm | 18.03 mm | Corrected to BT-20 spec |
| | Wall thickness | ~1 mm | 0.33 mm | BT-20 spec: 0.013" |
| | Mass | 3 g | 3 g | |
| **Engine Block** | Outer diameter | 18 mm | 18 mm | Green fiber ring |
| | Inner diameter | 14 mm | 14 mm | |
| | Thickness | 2 mm | 2 mm | |
| | Mass | 1 g | 1 g | |
| **Retainer Sleeve** | Length | 69 mm | 69 mm | Clear Mylar, exterior |
| | Mass | 2 g | 2 g | |
| **Engine Hook** | Length | 82 mm | 82 mm | Metal clip, external |
| | Mass | 1 g | 1 g | |
| **Fins (x3)** | Root chord | 107 mm | 107 mm | Laser-cut balsa |
| | Tip chord | 21 mm | 21 mm | |
| | Span | 35 mm | 35 mm | |
| | Sweep length | 81 mm | 81 mm | |
| | Thickness | 1.5 mm | 1.5 mm | |
| | Mass (each) | ~0.67 g | 0.67 g | |
| **Launch Lug** | — | Not measured | Standard 1/8" defaults | |
| **Streamer** | — | Not measured | 305 x 25 mm (Estes spec) | |
| **Shock Cord** | — | Not measured | 305 mm (Estes spec) | 

## Simulation Conditions

All simulations run with OpenRocket default settings:
- Wind: 2 m/s average, 10% turbulence
- Atmosphere: ISA standard (15°C, 1013.25 mbar)
- Launch rod: 100 cm, vertical
- Launch site: 28.61°N, -80.6°E (Cape Canaveral default)

## Simulation Results

Total mass without motor: **21.3 g**

Stability: **4.72 cal** (CG: 13.7 cm, CP: 22.5 cm) — very stable due to 12g nose clay.

| Motor | Apogee | Max Velocity | Time to Apogee | Ground Hit Velocity |
|---|---|---|---|---|
| A8-3 | 113 m (370 ft) | 57 m/s | 4.65 s | 22.8 m/s |
| B6-4 | 237 m (780 ft) | 96 m/s | 6.18 s | 23.7 m/s |
| C6-5 | 432 m (1,420 ft) | 142 m/s | 7.93 s | 23.6 m/s |

Planned first flight: **B6-4**

## Files

- `Estes_Hi-Flier_2178.ork` — OpenRocket simulation file

## TODO

- [ ] Weigh finished rocket (with paint) and update mass override
- [ ] Measure CG by balancing on finger, compare to simulated 13.7 cm
- [ ] Fly on B6-4, record observed altitude and flight behavior
- [ ] Compare actual vs. simulated performance
