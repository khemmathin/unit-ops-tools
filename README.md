# 01202311 Unit Operations II — Interactive Tools

**Department of Chemical Engineering · Kasetsart University**  
**Dr. Khemmathin Lueangwattanapong**

---

## Tools

### McCabe–Thiele Construction
**[khemmathin.github.io/unit-ops-tools/mccabe-thiele.html](https://khemmathin.github.io/unit-ops-tools/mccabe-thiele.html)**  
`mccabe-thiele.html`

Interactive binary distillation design tool covering Lectures L01–L04. Step-by-step tray construction on a real VLE x-y diagram.

### Flash Drum Explorer
**[khemmathin.github.io/unit-ops-tools/flash_drum.html](https://khemmathin.github.io/unit-ops-tools/flash_drum.html)**  
`flash_drum.html`

Single equilibrium stage (flash) tool for Lecture L02a. Graphical solution on the x-y diagram with an integrated Degrees of Freedom analysis panel.

---

## VLE Systems (both tools)

| System | VLE Source | Type |
|---|---|---|
| n-Pentane / n-Heptane | Antoine + Raoult (NIST) · 1 atm | Ideal · α ≈ 6–8 |
| Benzene–Toluene | Geankoplis Table 26.1-1 · Raoult sweep | Ideal · α = 2.37–2.54 |
| Methanol–Water | NIST / Gmehling DECHEMA tabulated (x,y) | Non-ideal · α = 2.5–7.6 |
| Ethanol–Water | Chu et al. (1950) / NIST tabulated (x,y) | Non-ideal · azeotrope x = 0.894 |
| n-Heptane / n-Octane | Antoine + Raoult (NIST) | Ideal · α = 2.13–2.24 |
| Custom | User-supplied Antoine A, B, C | Any ideal binary |

All tabulated systems use PCHIP (monotone cubic) interpolation for smooth equilibrium curves.

---

## McCabe–Thiele features

**Diagram**
- Real VLE equilibrium curve (no constant-α approximation)
- Enriching and stripping operating lines
- q-line with continuous slider (−0.5 to +1.5) and live feed condition description
- Step-by-step tray construction — optimum feed tray marked with ★
- Azeotrope marker and warning for ethanol–water

**Analysis panels**
- Sensitivity chart: N theoretical vs R/R_min
- α variation table: x, T, y, α at sampled compositions
- R_min: numerical scan handling both q-line pinch and tangent pinch
- N_min: stage-stepping at total reflux

**Controls**
- Editable number inputs alongside all sliders for exact value entry
- Pressure slider with SI (kPa) / imperial (mmHg) unit toggle
- Temperature unit toggle: °C / °F
- Keyboard: `Space` step · `A` all · `Esc` reset
- Total condenser · CMO assumed

---

## Flash Drum features

**Diagram**
- Real VLE equilibrium curve (same engine as McCabe–Thiele)
- Operating line through feed point (z_F, z_F) with slope −L/V
- Live solution point (x, y) as gold dot on equilibrium curve
- Limiting case markers: vertical (V/F → 0, all liquid) · horizontal (V/F → 1, all vapour)
- Azeotrope marker for ethanol–water

**Degrees of Freedom panel**
Three-column analysis updated live as sliders move:
1. Material balance — the operating line equation and why it alone leaves infinite solutions
2. Equilibrium condition — the VLE curve and why it alone leaves infinite solutions
3. Intersection — 2 equations · 2 unknowns · 0 DoF · unique (x, y); Gibbs Phase Rule noted

**Process schematic**
- SVG diagram: feed → heater → valve → drum → vapour + liquid products
- Liquid fill level in drum responds to V/F slider
- Stream compositions and flow ratios labelled live

**Controls**
- Editable number inputs alongside all sliders
- Specification: z_F (feed composition) and V/F (vapour fraction) — matches Geankoplis §26.3C
- Default preset: n-pentane/n-heptane at z_F = 0.40, V/F = 0.40 → x = 0.22, y = 0.66 (L02a worked example)

---

## Repository structure

```
unit-ops-tools/
├── mccabe-thiele.html   ← McCabe–Thiele construction tool
├── flash_drum.html      ← Flash Drum Explorer
└── README.md
```

## Deployment

Each tool is a single self-contained file — no build step, no dependencies, works offline after first load. Replace the file and push to `main`; GitHub Pages redeploys in ~30 seconds.

---

*Plain HTML · CSS · JavaScript. No frameworks. No external dependencies.*
