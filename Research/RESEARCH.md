# QD Research Platform — Research Documentation

**Quantum Dot–Assisted Diagnostic Prototype — Neurology & Oncology**

## 📋 Overview

This research prototype explores how engineered quantum dot (QD) nanoparticles could address molecular-imaging gaps across different diseases. It began as a single-disease tool for Mesial Temporal Sclerosis (MTS) and has been rebuilt around a shared, disease-agnostic engine — the same material-comparison and targeting logic now also drives an oncology (solid tumor imaging) module, with Alzheimer's disease and diabetes planned next.

The core architectural idea: **separate what's the same for every disease from what's different.** QD photophysics (Phase 1) doesn't change based on what you're imaging. Biomarkers, conjugation targets, and anatomy (Phases 2–3) do. Each disease module supplies its own biomarker panel, staging/grading system, and 3D anatomical model, all running through the same three-phase pipeline.

## 🎯 Shared Scientific Foundation

### Quantum Dots as an Imaging Platform

Quantum dots (2–15 nm semiconductor nanocrystals) offer, relative to conventional organic fluorescent dyes:

- Size-tunable, bright, photostable emission — including into the near-infrared (NIR-I: ~650–900 nm, NIR-II: ~1000–1700 nm) windows where tissue scattering and absorption are minimized.
- True multiplexing — several narrow, non-overlapping emission peaks imaged simultaneously.
- Versatile surface functionalization for antibody/peptide-based biomarker targeting.

**The seven QD materials modelled** (shared across all disease modules; only the recommended weighting changes per module/context):

| Material | Character | Toxicity | Brightness (QY) |
|---|---|---|---|
| InP/ZnS | Cadmium-free, versatile | Low | 65% |
| CuInS₂/ZnS | Broad, deep-tissue emission | Low | 50% |
| Ag₂S | Deepest imaging (NIR-II) | Low–Moderate | 12% |
| Silicon QDs | Biodegradable, very safe | Very Low | 35% |
| Carbon QDs | Extremely safe, shallow use | Very Low | 40% |
| Graphene QDs | Sensing over imaging | Very Low | 25% |
| CdSe/ZnS | Brightest, but toxic (reference standard only) | High | 80% |

**Scoring methodology**: multi-criteria decision analysis. Each material is scored against six weighted parameters — tissue window (emission), quantum yield, biocompatibility, size/delivery, photostability, and conjugation ease — using user-adjustable 0–10 weights, producing a live, transparent weighted score out of 100. This is a real, standard technique from decision science, applied here to nanomaterial selection so every ranking is explainable rather than a black box.

## 🧠 Module: Mesial Temporal Sclerosis (MTS)

### Pathology

- Characterized by selective neuronal loss (primarily CA1, CA4, hilus), reactive gliosis, mossy fiber sprouting, and granule cell dispersion.
- The most common structural cause of drug-resistant focal (temporal lobe) epilepsy.
- ILAE classification (Types 1a, 1b, 2, 3) guides prognosis and surgical outcomes.

**Diagnostic challenges**: MRI misses 15–30% of cases, especially subtle subfield involvement; limited cellular/molecular resolution pre-surgery; post-surgical histology is definitive but too late to inform planning.

### Anatomy modelled

Six hippocampal subfields: **CA1** (most vulnerable, "Sommer sector"), **CA2** (comparatively resistant), **CA3** (mossy-fibre zone), **CA4/Hilus** (severely affected in Types 1a/3), **Dentate Gyrus** (mossy fibre sprouting, granule cell dispersion), **Subiculum** (relatively spared).

### Biomarker panel

| Biomarker | Flags | Priority |
|---|---|---|
| GFAP | Reactive astrogliosis | High |
| NeuN | Neuronal density | High |
| NPY | Mossy fibre sprouting | Medium |
| Prox1 | Granule cell dispersion | Medium |
| Iba1 | Neuroinflammation | Low |
| mTOR / pS6 | Signalling dysregulation | Low |

### Imaging contexts

**Ex Vivo** (post-surgical tissue — lower BBB requirement, full histology access) vs. **In Vivo** (living patient — BBB penetration and biocompatibility become critical). The In Vivo channel uses **RVG-29**, a rabies-virus-glycoprotein-derived peptide that binds nAChR on blood-brain-barrier endothelium — a real, published BBB-crossing strategy — conjugated to PEG-coated Ag₂S or Silicon QDs.

## 🧬 Module: Oncology — Solid Tumor Imaging

### Pathology

Solid tumors outgrow the normal organization of surrounding tissue, developing irregular, leaky vasculature and distinct internal zones as oxygen and nutrients diffuse inward from the periphery. Precisely imaging these zones and grading tumor differentiation has direct value for diagnosis, treatment planning, and image-guided surgery.

### Anatomy modelled

A schematic five-zone radial cross-section, reflecting real tumor microarchitecture: **Necrotic core** (beyond the diffusion limit — dead tissue), **Hypoxic zone** (low-oxygen viable tissue, HIF-1α-driven), **Proliferative rim** (actively dividing, well-oxygenated edge), **Angiogenic margin** (dense, leaky neovasculature), **Peritumoral stroma** (invasive front, immune infiltrate).

**Grading system**: tumor grade (Grade 1 well-differentiated → Grade 4 undifferentiated/anaplastic) — a real, cancer-type-general histopathology concept (e.g. Gleason grading in prostate cancer, Nottingham grading in breast cancer) — used in place of a disease-specific staging system, since it generalizes across solid tumor types.

### Biomarker panel

| Biomarker | Flags | Priority |
|---|---|---|
| HER2 | Overexpressed growth receptor (~20% of breast/gastric cancers) | High |
| EGFR | Pan-carcinoma growth receptor | High |
| VEGFR2 | Tumor angiogenesis marker | High |
| Folate Receptor α | Overexpressed in ovarian/lung/breast cancer | Medium |
| CA IX | Hypoxia marker (HIF-1α-induced) | Medium |
| Ki-67 | Proliferation index (ex vivo only) | Low |

Notably, the real-world clinical analogue of folate-receptor targeting — **pafolacianine (Cytalux)** — is FDA-approved and already used in fluorescence-guided ovarian cancer surgery today. It uses a conventional small-molecule dye, not a quantum dot; it validates the *targeting mechanism*, not the QD material itself. No QD-based imaging agent has yet been approved for clinical use.

### Imaging contexts

**Passive (EPR)** — exploits the Enhanced Permeability and Retention effect: tumor vasculature is leaky enough that a properly-sized (~20–200 nm), PEG-coated QD carrier accumulates in tumor tissue with no targeting ligand required. **Active (Receptor-targeted)** — conjugates an antibody or peptide (HER2, EGFR, or the **RGD** tripeptide, which binds integrin αvβ3 on angiogenic endothelium — the oncology analogue of MTS's RVG-29) directly to the QD surface for receptor-specific binding. Switching contexts changes Phase 1's default weighting: conjugation ease is nearly irrelevant for passive targeting and dominant for active targeting.

## 🚀 Clinical & Research Potential

- **Intraoperative guidance**: real-time fluorescence margin assessment (already clinically precedented via pafolacianine and indocyanine green for other targets).
- **Pre-operative characterization**: subfield-level MTS typing or tumor-zone mapping from biopsy material.
- **Research tool**: quantitative, standardized severity/grade mapping and transparent, adjustable multi-criteria material selection.
- **Future**: in vivo imaging with BBB- or vasculature-targeted formulations; a theranostic (diagnosis + therapy delivery) extension of the same targeting logic.

## ⚠️ Fundamental Limitation: Optical Penetration Depth

Fluorescence-based imaging — quantum-dot-based or otherwise — is bounded by a real physical constraint that engineering cannot design around: visible-to-near-infrared light is strongly scattered and absorbed by tissue (hemoglobin, melanin, water, lipids), limiting useful imaging depth to roughly a few millimetres to a couple of centimetres, even in the best NIR-II window. This is why the platform is positioned as complementary to — not a replacement for — MRI, CT, and PET, which use radio waves, X-rays, and gamma rays respectively: forms of radiation that interact with tissue far more weakly and can reach anywhere in the body. QD-based fluorescence imaging is realistically suited to contexts with direct or near-direct optical access: open or laparoscopic surgery, endoscopy, and biopsy/ex vivo analysis.

## 📄 Roadmap

- **Alzheimer's disease** — reuses the MTS module's hippocampal 3D geometry (same organ, different pathology); real amyloid-beta/tau-targeted nanoparticle-imaging literature exists; Braak staging maps onto the preset-severity-pattern concept the way ILAE typing does for MTS.
- **Diabetes** — a structurally different module built around glucose biosensing (FRET-based) or pancreatic islet mass imaging, rather than fixed-anatomy structural imaging — deliberately chosen to prove the platform generalizes beyond a "colour a 3D organ" pattern.
- Integration with real MRI/histology data; expanded QD library; exportable reports and simulation parameters.

*Autism spectrum disorder was considered as a fourth candidate module and set aside: unlike MTS or a solid tumor, it has no single anatomical lesion and no broadly accepted molecular biomarker, and building a biomarker panel for it today would present speculative targets with the same apparent evidentiary footing as the other modules' real, published markers.*

## ⚠️ Disclaimer

**Research prototype only** — not intended for clinical diagnostic use. For educational and exploratory purposes. No real patient data is used or produced by any module. Every numeric score, biomarker panel, and severity value is a simplified, illustrative representation built for research and learning, not a measured or clinically-validated result.

---

*Version 0.3 — 2026*
*Interdisciplinary prototype bridging quantum nanotechnology with disease-specific biomedical targeting across neurology and oncology.*
