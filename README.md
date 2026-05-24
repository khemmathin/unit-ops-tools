# McCabe–Thiele Interactive Tool

**Course:** 01202311 Unit Operations II  
**Department of Chemical Engineering · Kasetsart University**  
**Dr. Khemmathin Lueangwattanapong**

**Live tool → [khemmathin.github.io/mccabe-thiele](https://khemmathin.github.io/mccabe-thiele)**

---

## What this is

A standalone interactive McCabe–Thiele construction tool for binary distillation. Runs entirely in the browser — no installation, no server, no login required.

---

## Features

**Real VLE data — no constant-α approximation**

| System | VLE Source | Notes |
|---|---|---|
| Benzene–Toluene | Geankoplis Table 26.1-1 · Raoult sweep | Matches textbook exactly · α = 2.37–2.54 |
| Methanol–Water | NIST / Gmehling DECHEMA (tabulated x,y) | Non-ideal · α = 2.5–7.6 · pressure fixed |
| Ethanol–Water | Chu et al. (1950) / NIST (tabulated x,y) | Lab system · azeotrope at x = 0.894 · pressure fixed |
| n-Heptane/n-Octane | Antoine + Raoult (NIST constants) | Near-ideal · pressure adjustable |
| Custom System | User-supplied Antoine A, B, C | Any ideal binary pair |

**Diagram**
- Equilibrium curve from real VLE data
- Enriching and stripping operating lines
- q-line with continuous slider (−0.5 to +1.5) and live description
- Step-by-step tray construction — feed tray marked with ★
- Azeotrope marker and warning for ethanol–water

**Analysis panels**
- Sensitivity chart: N theoretical vs R/R_min
- α variation table: x, T, y, α at 10 compositions — shows how α changes along the column
- R_min computed numerically (handles both q-line pinch and tangent pinch)
- N_min computed by stage-stepping at total reflux

**Controls**
- Pressure slider (active for Antoine systems)
- SI / °F·mmHg unit toggle
- Keyboard: `Space` step · `A` all · `Esc` reset
- Responsive: desktop, tablet, mobile

---

## Deploying / updating

The entire tool is a single file: **`index.html`**. Replace it and push to `main` — GitHub Pages redeploys in ~30 seconds.

---

*Built with plain HTML, CSS, and JavaScript. No dependencies. Works offline after first load.*
