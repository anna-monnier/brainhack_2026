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

The large project examine 🧠 **interpersonal synchrony** in **80 dyads** (mother-child pairs, autistic and non-autistic) 
in relation with the felt experience of 👥 **Togetherness** (feeling one with a partner) ! 
It includes EEG & ECG Hyperscanning data, videos + various forms of subjective experience (likert scales and more qualitative data)

📄 [Project poster](docs/Poster.pdf)

---

## Goal

My goal is thus to **explore** inter-brain synchrony patterns between mothers and child (autistic or non-autistic) of the pilot **EEG data** (9 dyads)
I want to to check if their neural dynamics relate to the subjective experience they reported. — So, also in correlation with likert scales. 

---

## Data

Data collected under approved ethics protocols; raw data not publicly shared

10 Tasks

| 1 min | 1 min | 2 min | 2 min | 1 min | 1 min | 2 min | 2 min | 1 min | 1 min |
|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
| 👁️ Yeux ouverts |  🙈  Yeux fermés | 🤚 **Imitation spontanée** | 🗣️  **Planification journée** | 👁️ Yeux ouverts |  🙈  Yeux fermés | 🗣️  **Planification journée** | 🤚 **Imitation spontanée** | 👁️ Yeux ouverts | 👁️ Yeux fermés |

- **Participants**: 9 pilot dyads (autistic and non-autistic child + mother)
- **EEG**: Dual 128 EGI HydroCel system (high density hyperscanning), continuous recording during the 10 tasks
- **Subjective measure**: Inclusion of the Other in the Self scale (IOS, 1–7 Likert) after each of the 10 tasks

![IOS Scale](docs/ios.png)

---

## Tools & Methods (the pipelines used and produced in my lab are not public yet)

| Tool | Use |
|------|-----|
| `Git / GitHub` | Version control and reproducibility |
| `Claude Code` | Agentic pipeline development and adaptation |
| [ppsp-hyperscanning-pipeline](https://github.com/ppsp-team/ppsp-hyperscanning-pipeline) | Main hyperscanning pipeline (adapted for our dataset) |
| `MNE-Python` | EEG preprocessing, filtering, ICA, connectivity |
| `PyPREP` | Automated bad channel detection and interpolation |
| `AutoReject` | Automated epoch rejection based on peak-to-peak amplitude |
| `ICALabel` | Automated ICA component classification (brain vs artifact) |
| [HyPyP](https://github.com/ppsp-team/HyPyP) | Hyperscanning connectivity analysis (PLV, transfer entropy) |
| `pandas` / `numpy` | Data handling and manipulation |
| `matplotlib` / `seaborn` | Visualization |
| `scikit-learn` | Machine learning (group classification) |

### Pipeline overview

```mermaid
flowchart TD
    A[📂 Raw XDF files] --> B[🔍 Quality Check]
    B --> C[📋 BIDSification]
    C --> C1[🧠 EEG conversion\nXDF → BrainVision]
    C --> C2[📊 IOS ratings integration\nphenotype/ + events.tsv]
    C1 --> D[⚙️ Preprocessing\nFiltering · PyPREP · ICA]
    C2 --> D
    D --> D1[📏 Benchmarking\nQuality metrics validation]
    D1 --> E[✂️ Epoching]
    E --> E1[🎯 Task epochs\n10 tasks × IOS rating]
    E --> E2[⭐ Peak connection moments\nManual annotation ~15s]
    E1 --> F[🎵 Frequency Band Analysis\nDelta · Theta · Alpha · Beta · Gamma]
    E2 --> F
    F --> G[🔗 Connectivity\nPLV · Transfer Entropy · AdjCircCorr]
    G --> H[📊 Integration\nEEG × IOS correlation]
    H --> I[📈 Statistics\nMixed models · Permutation tests · ML classification]

    style A fill:#2d6a4f,color:#fff
    style B fill:#2d6a4f,color:#fff
```
---

## Deliverables

1. ⬜ Adapted EEG preprocessing pipeline for our EGI dataset (reproducible GitHub repository with synthetic data)
2. ⬜ Inter-brain connectivity analysis (PLV, transfer entropy) for 9 pilot dyads
3. ⬜ Statistical comparison of inter-brain synchrony between groups (autistic/non-autistic dyads) and across the 10 tasks
4. ⬜ Correlation between task-averaged inter-brain synchrony and IOS ratings per task
5. ⬜ Jupyter Notebook going through preprocessing 
5. ⬜ Jupyter Notebook going through analyses 

---

## Visualization

The challenge of my project is to start with average data per tasks (tasks of 1 or 2 minutes) to a relevant choice of metrics and a vizualisation of the dynamics of the synchronisation (directionality, switches, metastability, evolution of regimes of synchrony...)

*Coming soon — inter-brain connectivity maps, PLV topographies, IOS correlation plots*

---

## Skills I Want to Learn

- Becoming autonomous in analysing and adapting the pipelines of my lab to my data !!!
- Exploring the potentiality of vizualisations

1. ⬜ **Agentic coding with Claude Code** — using AI to assist pipeline adaptation
2. ⬜ **Git & GitHub workflows** — branching, pull requests, reproducible science

1. ⬜ **EEG preprocessing in Python** — MNE-Python, PyPREP ...
2. ⬜ **Hyperscanning connectivity analysis** — PLV, wPLI, transfer entropy, Adjusted CirrCorr

1. ⬜ **Statistics for small neuroimaging datasets** — mixed models, permutation tests, LOOCV
2. ⬜ **Data visualization** — connectivity maps, topographies, inter-brain synchrony plots
---

## References and acknowledgements

This work is part of a CIHR-funded project (2024–2028)

- *reference list to be completed*
[1] Monnier, A., Adel, L., & Dumas, G. (2025). [Now is the time: operationalizing generative neurophenomenology through interpersonal methods](https://academic.oup.com/nc/article/2025/1/niaf052/8405712). *Neuroscience of Consciousness*, 2025(1), niaf052.
