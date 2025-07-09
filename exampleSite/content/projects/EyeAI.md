---
title: "EyeAI"
date: 2018-11-28T15:15:26+10:00
featured: true
draft: false
weight: 3
---

EyeAI combines DERIVA-ML with GPU-based notebooks to create a fully traceable pipeline for glaucoma detection from fundus photographs, spanning data ingest, feature extraction, model training, and clinical review.  By treating each dataset, feature set, workflow, and execution as a first-class, versioned artefact, the project shows how DERIVA-ML delivers continuous FAIRness for real-world medical AI.  
<!--more-->

## Why DERIVA-ML underpins EyeAI

| Challenge | DERIVA-ML Capability |
|-----------|----------------------|
| Multimodal, noisy clinical data | Unified domain + ML schemas; data checked and versioned on ingest |
| Rapid feature & model iteration | Model-driven UI updates automatically when schema changes |
| Reproducible, auditable runs | Six-artefact data model (Dataset, Feature, Workflow, Execution, Asset, CV) captures every run |
| Sensitive patient data | Fine-grained Globus Auth roles (reader / writer / curator) with embargo support |

## Impact to date¹

* **>70 datasets**, **130 executions**, **142 trained models** stored with DOIs  
* **13 clinicians** provided independent labels; inter-rater metrics computed automatically  
* Label-efficiency study trained 142 models across **36 data subsets**, with 71 retrains done by editing only execution configs  
* Optic-nerve detector re-trained in one day after performance drift, demonstrating end-to-end reproducibility

## Typical workflow

1. **Ingest** — fundus JPEGs and metadata uploaded; Minid + BDBag generated.  
2. **Feature engineering** — VGG19 model crops optic-nerve region, stores SVG as *Image Annotation* Feature.  
3. **Model training** — VGG19 and RETFound classifiers trained via notebook; parameters, ROC figure, and model file auto-uploaded as Execution Assets.  
4. **Review** — Chaise UI lets ophthalmologists inspect predictions and trace back to raw images.

## Lessons for other ML health projects

* Continuous FAIRness (“all data, all the time”) prevents data cascades.  
* Controlled vocabularies plus Minid-based datasets make label auditing straightforward.  
* Workflows stay in plain notebooks; DERIVA-ML adds the provenance layer without locking teams into new tools.

---

¹ Figures from Li Z. *et al.*, “From Data to Decision: Data-Centric Infrastructure for Reproducible ML in Collaborative eScience,” arXiv 2506.16051 (2025) and Li Z. *et al.*, “DERIVA-ML: Continuous FAIRness for Reproducible Machine Learning Models,” arXiv 2407.01608 (2024).

[← Back to all projects](/projects/)
