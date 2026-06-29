# QD-MTS Research Documentation

**Quantum Dot–Assisted Diagnostic Prototype for Mesial Temporal Sclerosis**

## 📋 Overview

This research prototype explores the application of engineered quantum dot nanoparticles to address key diagnostic gaps in Mesial Temporal Sclerosis (MTS) — the most common structural cause of drug-resistant temporal lobe epilepsy.

Current clinical tools (high-resolution MRI, EEG, PET) frequently miss subtle or early-stage hippocampal changes, leading to incomplete surgical resections and persistent seizures in 30–40% of patients. This platform demonstrates how quantum dots could enable multi-channel, molecular-level visualization of MTS pathology for better pre-operative planning and intraoperative guidance.

## 🎯 Scientific Foundation

### Mesial Temporal Sclerosis (MTS)
- Characterized by selective neuronal loss (primarily CA1, CA4, hilus), reactive gliosis, mossy fiber sprouting, and granule cell dispersion.
- Affects millions globally; major cause of refractory focal epilepsy.
- ILAE classification (Types 1a, 1b, 2, 3) guides prognosis and surgical outcomes.

**Diagnostic Challenges**:
- MRI misses 15–30% of cases, especially subtle subfield involvement.
- Limited cellular/molecular resolution pre-surgery.
- Post-surgical histology is definitive but too late for planning.

### Quantum Dots in Neuroscience
Quantum dots (2–10 nm semiconductor nanocrystals) offer:
- Size-tunable, bright, photostable NIR emission (deep tissue penetration).
- Versatile surface functionalization for biomarker targeting.
- Multi-modal potential (imaging + sensing + delivery).

**Targeted Biomarkers**:
- **GFAP** — Reactive astrogliosis
- **NeuN** — Neuronal density/loss
- **NPY / Prox1** — Mossy fiber sprouting & granule cell dispersion
- **Iba1** — Microglial activation
- Others (mTOR/pS6, etc.)

## 🧪 Platform Architecture

The interactive simulator consists of three integrated phases:

### Phase 1 — Material Optimizer
- Compares 7 QD candidates (InP/ZnS, CuInS₂/ZnS, Ag₂S, Silicon QDs, etc.).
- Weighted scoring across key parameters (Tissue Window, Quantum Yield, Biocompatibility, BBB Penetration, Photostability, Conjugation Ease).
- Ex Vivo vs In Vivo mode switching.

### Phase 2 — Targeting Strategy
- Multi-channel labelling panel for simultaneous biomarker detection.
- Conjugation protocols (EDC/NHS, streptavidin-biotin, thiol-maleimide).
- Spectral compatibility guidance.

### Phase 3 — 3D Hippocampal Model
- Interactive coronal 3D visualization of the right hippocampus (Three.js).
- ILAE subtype presets + manual severity sliders.
- Dynamic QD fluorescence particle simulation (density scales with pathology).

## 🚀 Clinical & Research Potential

- **Intraoperative guidance**: Real-time fluorescence margin assessment.
- **Pre-operative typing**: Subfield-level MTS characterization from biopsies.
- **Research tool**: Quantitative, standardized MTS severity mapping.
- **Future**: In vivo imaging with BBB-crossing formulations (e.g., RVG-29 + Silicon/Ag₂S QDs).

## 📄 Roadmap

See the full `QD_MTS_Platform_Documentation.pdf` for detailed translation phases (A–D), challenges, and references.

## ⚠️ Disclaimer

**Research prototype only** — Not intended for clinical diagnostic use. For educational and exploratory purposes.

---

*Version 0.2 — 2026*  
*Interdisciplinary prototype bridging quantum nanotechnology and clinical neurology.*
