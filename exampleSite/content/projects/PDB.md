---
title: "Protein Data Bank (PDB)"
date: 2018-11-28T15:15:34+10:00
featured: true
draft: false
weight: 2
---

PDB-IHM is the integrated pipeline that now archives and validates all Protein Data Bank entries derived from integrative and hybrid methods.  Built on the DERIVA platform, it enables depositors to upload complex multi-scale models, curators to run automated validation, and the wwPDB to release FAIR integrative structures alongside conventional X-ray, NMR, and cryo-EM data.  
<!--more-->

## Why PDB-IHM adopted DERIVA

| Requirement | DERIVA capability |
|-------------|-------------------|
| **Rich, evolving data standard (IHMCIF)** | Schema changes propagate automatically to the web UI and API without code rewrites. |
| **End-to-end provenance** | Versioned object store links every restraint, model, and validation report to its accession code. |
| **Bulk deposition at consortium scale** | REST and Python APIs handle collections of hundreds of entries in a single workflow run. |
| **Weekly, synchronized public release** | Timed workflows package mmCIF, validation PDFs, and holdings files for wwPDB distribution. |

## Impact since unification (Aug 2024 → Jun 2025)

* **≈ 350 integrative entries** released with 4-character PDB IDs and DOIs.  
* **15 experimental data types** captured (cross-link MS, SAS, FRET, 3DEM, etc.).  
* **>60 TB** of associated restraint and model files stored with fixity and version history.  
* Validation reports streamed to depositors cut curator review time by **40 %**. :contentReference[oaicite:5]{index=5}

## Typical deposition workflow

1. **Research team** converts modeling results to IHMCIF with `python-ihm` and uploads via the PDB-IHM REST API.  
2. **Automated DERIVA workflow** checks dictionary compliance, generates preliminary validation, and assigns a provisional PDB code.  
3. **Curator** reviews flags in the Chaise interface, toggles manual vs. auto steps as needed.  
4. **Release process** packages mmCIF, BinaryCIF, and validation PDFs; hand-off to wwPDB weekly release at 00:00 UTC Wednesday.

## Lessons for future repositories

* **Dictionary-driven catalogues** avoid hard-coding scientific edge cases.  
* **Fine-grained ACLs** let external depositors see only their entries while curators see all, improving security and usability.  
* **Timed release hooks** make it straightforward to embed DERIVA workflows in larger consortium schedules (e.g., wwPDB weekly cycle).

For technical details see: *Vallat B. et al.* “PDB-IHM: A System for Deposition, Curation, Validation, and Dissemination of Integrative Structures,” *J. Mol. Biol.* 437 (2025) 168963.

[← Back to all projects](/projects/)
