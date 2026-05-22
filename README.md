# brainhack_2026
<a href="https://github.com/anna-monnier">
  <img src="https://avatars.githubusercontent.com/u/52865298?v=4?s=100" width="100px;" alt=""/>
  <br /><sub><b>anna-monnier</b></sub>
</a>
# 🧠 Inter-Brain Synchrony in Autism: A Hyperscanning EEG Study

### Neurophenomenology meets social neuroscience

---

<a href="https://github.com/anna-monnier">
  <img src="https://avatars.githubusercontent.com/u/52865298?v=4?s=100" width="100px;" alt=""/>
  <br /><sub><b>anna-monnier</b></sub>
</a>

---

## Introduction

This project is the **first analytical step** of a larger study examining interpersonal synchrony in autism. 
The full cohort will include **80 autistic/non-autistic dyads** (child-mother pairs) recorded across **three modalities: EEG, ECG, and movement kinematics**. 

In this 1st phase, we focus on **EEG hyperscanning** — simultaneous dual-brain recordings during naturalistic social interaction. The goal is to characterize inter-brain synchrony patterns between mothers and child (autistic or non-autistic), and to relate these neural dynamics to subjective experience.

The study combines:
- **Dual EEG hyperscanning** to measure inter-brain connectivity
- **Subjective measures** including the *Inclusion of the Other in the Self* scale (IOS, Likert 1–7), a validated measure of felt interpersonal closeness

This work is part of a CIHR-funded project (2024–2028) and is grounded in a **neurophenomenological framework**, moving beyond a deficit-based view of autism toward a neurodiversity-affirming approach to social connection.

📄 [Project poster](docs/poster.pdf)

---

## Objectives

During this Brainhack, I aim to:

1. Adapt in a dedicated Branch and run the [PPSP hyperscanning EEG pipeline](https://github.com/ppsp-team/ppsp-hyperscanning-pipeline) on our pilot dataset (9 dyads)
2. Bidsify the data
3. Implement robust EEG preprocessing using a PyPREP-based approach for automated bad channel and artefacts detection
4. Compute inter-brain connectivity metrics (Phase-Locking Value, transfer entropy...) for each of the 10 tasks
5. Relate EEG connectivity to IOS subjective ratings
6. Run group statistics between autistic and non-autistic group
TBC. Build a reproducible, documented pipeline ready to scale to 80 dyads

---

## Data

- **Participants**: 9 pilot dyads (autistic and non-autistic child + mother)
- **EEG**: Dual EGI HydroCel system (hyperscanning), continuous recording during 10 tasks (resting states and cooperative tasks)
- **Subjective measure**: Inclusion of the Other in the Self scale (IOS, 1–7 Likert)
- **Clinical Not open data**: Data collected under approved ethics protocols; raw data not publicly shared

---

## Tools & Methods

The pipeline is built on **Bash, VSCode, Python and MNE-Python** as its foundation, and developed with the assistance of **Claude Code** for pipeline adaptation and documentation.

| Tool | Use |
|------|-----|
| `MNE-Python` | EEG preprocessing, filtering, ICA, connectivity |
| [ppsp-hyperscanning-pipeline](https://github.com/ppsp-team/ppsp-hyperscanning-pipeline) | Main hyperscanning pipeline (adapted for our dataset) |
| `PyPREP` | Automated bad channel detection and interpolation |
| `Claude Code` | Agentic pipeline development and adaptation |
| `pandas` / `numpy` | Data handling and manipulation |
| `scikit-learn` | Machine learning (group classification) |
| `matplotlib` / `seaborn` | Visualization |
| `Git / GitHub` | Version control and reproducibility |

### Pipeline overview

1. **Raw data import** — EGI `.mff` files → MNE Raw objects
2. **Preprocessing** — filtering (1–40 Hz), bad channel detection (PyPREP), ICA artifact removal
3. **Epoching** — segmentation around interaction events
4. **Connectivity** — Phase-Locking Value (PLV) and transfer entropy between dyad brains
5. **Integration** — correlation with IOS ratings

---

## Deliverables

1. ✅ Adapted EEG preprocessing pipeline for our EGI dataset
2. ✅ Inter-brain connectivity analysis (PLV, transfer entropy) for 9 pilot dyads
3. ✅ Correlation between (avergaed!) neural synchrony and IOS subjective ratings per task
4. ✅ Documented, reproducible GitHub repository

---

## Visualization

The challenge of my project is to start with average data per tasks (tasks of 1 or 2 minutes) to a relevant choice of metrics and a vizualisation of the dynamics of the synchronisation (directionality, switches, metastability, evolution of regimes of synchrony...)
*Coming soon — inter-brain connectivity maps, PLV topographies, IOS correlation plots*

---

## Skills I Want to Learn

1. **EEG preprocessing in Python** — MNE-Python, ICA, PyPREP bad channel detection
2. **Hyperscanning connectivity analysis** — PLV, wPLI, transfer entropy
3. **Agentic coding with Claude Code** — using AI to assist pipeline development
4. **Git & GitHub workflows** — branching, pull requests, reproducible science
5. **Machine learning for small neuroimaging datasets** — cross-validation, LOOCV
6. **Integrating neural and subjective data** — correlating EEG metrics with IOS ratings

---

## References

- *reference list to be completed*