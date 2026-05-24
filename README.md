# McCabe–Thiele Interactive Tool

**Course:** 01202311 Unit Operations II  
**Department of Chemical Engineering · Kasetsart University**  
**Dr. Khemmathin Lueangwattanapong**

---

## What this is

A standalone interactive tool for teaching and exploring the **McCabe–Thiele graphical construction** for binary distillation. Runs entirely in the browser — no installation, no server, no login required.

**Live tool → [your-username.github.io/mccabe-thiele](https://your-username.github.io/mccabe-thiele)**  
*(update this link after deploying)*

---

## Features

- **Equilibrium curve** computed from constant relative volatility α
- **Enriching and stripping operating lines** derived from material balances
- **q-line** with continuous feed-condition slider (−0.5 to +1.5) and live description of the physical meaning at each q value
- **Step-by-step tray construction** — click once per tray, or reveal all at once
- **Feed tray** identified automatically and marked with ★
- **Sensitivity chart** — N theoretical vs R/R_min, current design point highlighted
- **Keyboard shortcuts** — `Space` to step, `A` for all, `Esc` to reset

## Verified presets

| System | α | Notes |
|---|---|---|
| Benzene–Toluene | 2.47 | Matches Geankoplis Table 26.1-1 geometric mean. Parameters from Example 26.4-1. |
| Methanol–Water | ≈ 3.46 | Rough mid-range estimate. System is non-ideal; α varies 2.5 → 6.4. |
| n-Heptane / n-Octane | 2.16 | From Antoine equations at ~110 °C. Near-ideal; constant-α is a good approximation. |

## Important note on accuracy

The tool uses **constant relative volatility α** throughout — the standard undergraduate approximation. For systems where α varies significantly (methanol–water), the stage count will differ from a construction using actual VLE data. This is intentional and makes a useful teaching point.

---

## Deploying / updating

The entire tool is a single file: **`index.html`**. To update the tool, simply replace `index.html` with a new version and push to the `main` branch. GitHub Pages redeploys automatically within ~30 seconds.

## Keyboard shortcuts

| Key | Action |
|---|---|
| `Space` | Add one theoretical stage |
| `A` | Show all stages at once |
| `Esc` | Reset / clear stages |

---

*Built with plain HTML, CSS, and JavaScript. No dependencies. Works offline after first load.*
