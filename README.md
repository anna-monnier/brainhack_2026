# 🧠 Inter-Brain Synchrony in Autism: A Hyperscanning EEG Study

<a href="https://github.com/anna-monnier">
  <img src="https://avatars.githubusercontent.com/u/52865298?v=4?s=100" width="100px;" alt=""/>
  <br /><sub><b>anna-monnier</b></sub>
</a>

### Short bio: a "generative neurophenomenology" PhD !

I am a PhD student in Psychiatric Sciences at Université de Montréal, at CHU Sainte-Justine !
I am passionnated about consciousness phenomena, also in psychiatry, and my work is at the intersection of 
- EEG & ECG hyperscanning, 
- Social neuroscience, 
- and Phenomenology (subjective, first-person methods). 

This practice is called Generative Neurophenomenology [1]

## Introduction

The project is a larger study examining 🧠 **interpersonal synchrony** in **80 dyads** (mother-child pairs, autistic and non-autistic) in relation with the felt experience of 👥 **Togetherness** (feeling one with a partner) ! This big project collect EEG & ECG Hyperscanning data, videos and different forms of subjective experience (likert scales and more data)

BUT ... Let's keep it simple to start !!! 
Here, we focus only on a small sample of my piloting data, and focus on **EEG data** — in correlation with likert scales. 

📄 [Project poster](docs/Poster.pdf)

---

## Goal

My goal is to **explore** inter-brain synchrony patterns between mothers and child (autistic or non-autistic), and to check if their neural dynamics relate to the subjective experience they reported.

---

## Data

Data collected under approved ethics protocols; raw data not publicly shared

10 Tasks

| 1 min | 1 min | 2 min | 2 min | 1 min | 1 min | 2 min | 2 min | 1 min | 1 min |
|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
| 👁️ Yeux ouverts |  🙈  Yeux fermés | 🤚 **Imitation spontanée** | 🗣️  **Planification journée** | 👁️ Yeux ouverts |  🙈  Yeux fermés | 🗣️  **Planification journée** | 🤚 **Imitation spontanée** | 👁️ Yeux ouverts | 👁️ Yeux fermés |

- **Participants**: 9 pilot dyads (autistic and non-autistic child + mother)
- **EEG**: Dual EGI HydroCel system (hyperscanning), continuous recording during 10 tasks (resting states and cooperative tasks)
- **Subjective measure**: Inclusion of the Other in the Self scale (IOS, 1–7 Likert) / task

![IOS Scale](docs/ios.png)

---

## Tools & Methods (the pipelines used and produced in my lab are not public yet)

| Tool | Use |
|------|-----|
| [ppsp-hyperscanning-pipeline](https://github.com/ppsp-team/ppsp-hyperscanning-pipeline) | Main hyperscanning pipeline (adapted for our dataset) |
| `MNE-Python` | EEG preprocessing, filtering, ICA, connectivity |
| `PyPREP` | Automated bad channel detection and interpolation |
| `pandas` / `numpy` | Data handling and manipulation |
| `scikit-learn` | Machine learning (group classification) |
| `matplotlib` / `seaborn` | Visualization |
| `Git / GitHub` | Version control and reproducibility |
| `Claude Code` | Agentic pipeline development and adaptation |

### Pipeline overview

```mermaid
flowchart TD
    A[📂 Raw EGI .mff files] --> B[🔍 Quality Check]
    B --> C[📋 BIDSification\n+ IOS ratings integration]
    C --> D[⚙️ Preprocessing\nFiltering · PyPREP · ICA]
    D --> E[✂️ Epoching]
    E --> F[🎵 Frequency Band Analysis\nDelta · Theta · Alpha · Beta · Gamma]
    F --> G[🔗 Connectivity\nPLV · Transfer Entropy · AdjCircCorr]
    G --> H[📊 Integration\nEEG × IOS correlation]
    H --> I[📈 Statistics\nMixed models · Permutation tests · ML classification]
```
---

## Deliverables

1. ⬜ Adapted EEG preprocessing pipeline for our EGI dataset
2. ⬜ Inter-brain connectivity analysis (PLV, transfer entropy) for 9 pilot dyads
3. ⬜ Statistical comparison of inter-brain synchrony between groups (autistic/non-autistic dyads) and across the 10 tasks
4. ⬜ Correlation between task-averaged inter-brain synchrony and IOS ratings per task
5. ⬜ Jupyter Notebook going through analyses
6. ⬜ Documented, reproducible GitHub repository (but still private for the moment)

---

## Visualization

The challenge of my project is to start with average data per tasks (tasks of 1 or 2 minutes) to a relevant choice of metrics and a vizualisation of the dynamics of the synchronisation (directionality, switches, metastability, evolution of regimes of synchrony...)

*Coming soon — inter-brain connectivity maps, PLV topographies, IOS correlation plots*

---

## Skills I Want to Learn

- Becoming autonomous in analysing and adapting the pipelines of my lab to my data !!!
- Exploring the potentiality of vizualisations

1. ⬜ **EEG preprocessing in Python** — MNE-Python, PyPREP ...
2. ⬜ **Hyperscanning connectivity analysis** — PLV, wPLI, transfer entropy, Adjusted CirrCorr
3. ⬜ **Agentic coding with Claude Code** — using AI to assist pipeline adaptation
4. ⬜ **Git & GitHub workflows** — branching, pull requests, reproducible science
5. ⬜ **Statistics for small neuroimaging datasets** — mixed models, permutation tests, LOOCV
6. ⬜ **Data visualization** — connectivity maps, topographies, inter-brain synchrony plots
---

## References and acknowledgements

This work is part of a CIHR-funded project (2024–2028)

- *reference list to be completed*
[1] Monnier, A., Adel, L., & Dumas, G. (2025). [Now is the time: operationalizing generative neurophenomenology through interpersonal methods](https://academic.oup.com/nc/article/2025/1/niaf052/8405712). *Neuroscience of Consciousness*, 2025(1), niaf052.
