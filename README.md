# QD Research Platform

**Quantum Dot–Assisted Diagnostic Research Prototype — Neurology & Oncology**

An interactive computational research platform exploring how engineered quantum dot nanoparticles could enable multi-channel molecular imaging across different diseases. Built around a shared three-phase engine — material selection, targeting strategy, 3D visualization — that plugs into disease-specific modules.

[![Project Banner](https://github.com/DhrithiAlex/qd-mts-research-platform/raw/main/Media/Thumbnail.png)](Media/Thumbnail.png)

## 🎯 Overview

This platform began as a single-disease prototype for **Mesial Temporal Sclerosis (MTS)** — the most common structural cause of drug-resistant temporal lobe epilepsy — and has since been rebuilt around a reusable, disease-agnostic engine, so the same material-comparison and targeting logic can support entirely different diseases without being rewritten from scratch.

**Two modules are complete:**

- **Mesial Temporal Sclerosis (MTS)** — hippocampal subfield mapping, ILAE classification, and multi-channel biomarker targeting for epilepsy surgical planning. Current imaging (MRI) often misses subtle or early-stage changes, contributing to a 30–40% seizure-recurrence rate after resection.
- **Oncology — Solid Tumor Imaging** — a five-zone tumor microenvironment model, tumor grading, and passive (EPR) vs. active (receptor-targeted) delivery strategies for fluorescence-guided tumor imaging.

**Two more are planned:** Alzheimer's disease (reusing the hippocampal 3D geometry) and diabetes (a structurally different, biosensor-based module). See [Roadmap](#-roadmap).

## ✨ Key Features

### Shared engine (every module)

- **Phase 1 — Material Optimizer**
  Real-time weighted ranking of 7 QD candidates (InP/ZnS, CuInS₂/ZnS, Ag₂S, Silicon QDs, Carbon QDs, Graphene QDs, CdSe/ZnS) against six criteria: tissue window, quantum yield, biocompatibility, size/delivery, photostability, and conjugation ease. Each module supplies its own two imaging contexts with different default weightings.

- **Phase 2 — Targeting Strategy**
  Multi-channel biomarker labelling panel with real conjugation chemistries (EDC/NHS coupling, streptavidin–biotin, peptide targeting).

- **Phase 3 — Interactive 3D Model**
  Rotatable, zoomable Three.js visualization, colour-coded by severity, with a simulated QD fluorescence particle overlay. Degrades gracefully to a fully-functional data view if WebGL isn't available in the browser.

### 🧠 MTS module

- Hippocampal subfields: CA1, CA2, CA3, CA4/Hilus, Dentate Gyrus, Subiculum
- ILAE MTS classification presets (Types 1a, 1b, 2, 3)
- Biomarkers: GFAP, NeuN, NPY, Prox1, Iba1, mTOR/pS6
- Imaging contexts: **Ex Vivo** / **In Vivo** (BBB penetration via RVG-29 peptide)

### 🧬 Oncology module

- Five-zone schematic tumor cross-section: necrotic core, hypoxic zone, proliferative rim, angiogenic margin, peritumoral stroma
- Tumor grade presets (Grade 1 – Grade 4)
- Biomarkers: HER2, EGFR, VEGFR2, Folate Receptor α, CA IX, Ki-67
- Imaging contexts: **Passive (EPR)** / **Active (receptor-targeted, via RGD peptide)**

### Additional highlights

- Module selector in the header — switch disease modules without losing your place
- Responsive dark UI, emission spectrum comparison chart, real-time diagnostic readout
- Self-contained single-file app — no build step, no dependencies

## 📚 Research Documentation

- **[RESEARCH.md](Research/RESEARCH.md)** — scientific rationale, biomarker details, and methodology for both modules.
- **[QD_Research_Platform_Explained.pdf](Research/QD_Research_Platform_Explained.pdf)** — a comprehensive, plain-language guide to the whole platform: how quantum dots work, the shared architecture, both disease modules in full detail, safety considerations, and limitations — written to be clear to readers with no nanotechnology background as well as domain experts.

## 🛠️ Tech Stack

- **Core**: HTML5, CSS3 (custom properties, Grid/Flexbox), vanilla JavaScript
- **Visualization**: Three.js (3D rendering & particle systems), Chart.js (radar, bar, line charts)
- **Architecture**: Self-contained single-file web application, disease modules defined in a shared `DISEASE_MODULES` registry — no build step required

## 🚀 Quick Start

1. Clone or download the repository
2. Open `QD_Research_Platform.html` in any modern browser (Chrome/Edge/Firefox recommended)
3. Use the **Research Module** selector at the top to switch between MTS and Oncology
4. No installation or server required

**Live Demo**: [Open the Simulator](https://dhrithialex.github.io/qd-mts-research-platform/QD_Research_Platform.html)

## ⚠️ Disclaimer

**Research prototype only — not for clinical diagnostic use.** No real patient data is used or produced anywhere in the platform. Every disease module is explicitly labelled "Not for clinical use — computational model only," and every score, biomarker panel, and severity value shown is a simplified, illustrative representation built for research and learning.

## 🎨 Gallery

### Neurology (MTS) Module

[![Hippocampus Simulator](https://github.com/DhrithiAlex/qd-mts-research-platform/raw/main/Media/Hippocampus_Simulated.png)](Media/Hippocampus_Simulated.png)
[![Material Optimizer](https://github.com/DhrithiAlex/qd-mts-research-platform/raw/main/Media/Material_Optimizer.png)](Media/Material_Optimizer.png)
[![Targeting Strategy](https://github.com/DhrithiAlex/qd-mts-research-platform/raw/main/Media/Targeting_Strategy.png)](Media/Targeting_Strategy.png)

### Oncology Module

[![Oncology Module View 1](https://github.com/DhrithiAlex/qd-mts-research-platform/raw/main/Media/Oncology_1.png)](Media/Oncology_1.png)
[![Oncology Module View 2](https://github.com/DhrithiAlex/qd-mts-research-platform/raw/main/Media/Oncology_2.png)](Media/Oncology_2.png)

## 🔮 Roadmap

- **Alzheimer's disease module** — reuses the hippocampal 3D geometry already built for MTS; real amyloid-beta/tau-targeted imaging literature; Braak staging as the severity preset system.
- **Diabetes module** — a structurally different addition built around a glucose-biosensor mechanic rather than fixed-anatomy imaging, to demonstrate the platform can flex beyond structural imaging.
- Integration with real MRI/histology data
- Expanded QD library and AI-assisted scoring
- Exportable reports and simulation parameters

*(A fourth candidate disease, autism spectrum disorder, was considered and set aside — it currently lacks the kind of specific anatomical lesion or accepted molecular biomarker the other modules are built around.)*

## 📄 License

MIT License — fork, extend, or use as inspiration for related neurotech/quantum research.

## 🙋‍♀️ About

Built as a conceptual bridge between quantum nanotechnology and disease-specific biomedical targeting — demonstrating a reusable research framework, not a single-purpose tool. Showcases interdisciplinary work across materials science, biomedical targeting logic, and interactive visualization.

---

**Star this repo if you find it useful!** Contributions, feedback, and collaborations welcome.

*Version 0.3 — 2026*
