---
title: "Synapse"
date: 2018-11-28T15:14:39+10:00
featured: true
draft: false
weight: 4
---

The “Mapping the Dynamic Synaptome” project uses DERIVA to capture, curate, and share single-synapse–resolution imaging of larval zebrafish brains, revealing region-specific synapse gain and loss during memory formation.  All raw and processed data are available through the Synapse repository powered by DERIVA, with persistent DOIs for every figure and dataset.  
<!--more-->

## Why DERIVA underpins the Synaptome map

| Challenge | DERIVA feature |
|-----------|----------------|
| **Continuous FAIR capture** of multi-TB SPIM volumes, behavioral videos, and analysis tables | “Continuous FAIRness” data-lifecycle model: files land in Hatrac object store, metadata in ERMrest, DOIs minted on ingest :contentReference[oaicite:6]{index=6} |
| **Evolving schema** (new imaging channels, QC metrics) | Model-driven UI (Chaise) updates automatically—no code rewrites |
| **Link raw ↔ analysis ↔ publication** | Each figure in the PNAS paper resolves to underlying datasets via DERIVA landing pages :contentReference[oaicite:7]{index=7} |
| **Reproducible analytics** | Versioned CSV exports feed Python notebooks; provenance tracked back to original OME-TIFF stacks |

## Impact

* **11 learner fish**, **6 partial learners**, **33 control animals** imaged twice at single-synapse resolution.  
* **≈ 1,155 synapses per fish** were detected (0.5 % of total pallial synapses) and mapped in 3-D :contentReference[oaicite:8]{index=8}.  
* Ventrolateral pallium showed **net 30 % synapse gain** while dorsomedial pallium showed loss—first in-vivo structural map of memory at synapse scale :contentReference[oaicite:9]{index=9}.  
* All datasets publicly released on **synapse.isrd.isi.edu** with six figure-level DOIs (e.g., 10.25551/1/1-1Z06).

## Typical workflow

1. **Imaging session** – Selective-plane illumination microscope writes OME-TIFF stacks (~20 GB/fish).  
2. **Automated ingest** – DERIVA watcher uploads files, extracts metadata, creates draft records.  
3. **Curator review** – Chaise interface confirms ROI bounds and QC metrics; synapse-detection CSV attached.  
4. **Publication** – “Release” changes ACLs, mints DOIs, and exposes data through the public Synapse portal and Google Dataset Search.

## Lessons for future atlases

* **FAIR at acquisition time** avoids post-hoc wrangling when datasets hit terabyte scale.  
* Schema-agnostic UI lets neurobiology teams iterate on QC metrics without waiting for database admins.  
* Region-specific statistics can be derived directly from DERIVA queries—no bespoke ETL needed.

*Reference:* Dempsey WP et al. “Regional Synapse Gain and Loss Accompany Memory Formation in Larval Zebrafish,” *PNAS* 119 (3): e2107661119 (2022). :contentReference[oaicite:10]{index=10}

[← Back to all projects](/projects/)
