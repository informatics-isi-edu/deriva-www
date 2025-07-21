---
title: "Pancreatic β-Cell Consortium"
date: 2018-11-28T15:15:34+10:00
featured: true
draft: false
weight: 5
---

The Pancreatic β-Cell Consortium (PBCC) uses DERIVA to archive, curate, and share heterogeneous data on β-cell biology and whole-cell modelling, ranging from soft-X-ray tomography and mass-spectrometry to computational models.  DERIVA’s model-driven interface lets bench scientists, not DBAs, evolve the schema as new assays appear.  
<!--more-->

## Why PBCC chose DERIVA

| Requirement | DERIVA capability |
|-------------|-------------------|
| **Rapid schema evolution** as new imaging and omics assays are added | Scientists edit the ER model directly; Chaise UI and APIs update automatically. |
| **Self-curation by labs** across several institutions | Web forms enforce controlled vocabularies; role-based access keeps embargoed data private until release. |
| **Link raw data → processed data → whole-cell models** | Versioned object store (Hatrac) + provenance tables track every transformation and parameter set. |
| **FAIR dissemination to the wider diabetes community** | DOIs minted on release; landing pages expose rich JSON-LD for Google Dataset Search. |

## Impact so far

* **Six data types** (SXT, fluorescence imaging, proteomics, transcriptomics, model meshes, simulation outputs) stored under one evolving schema.  
* **Schema refactor completed by a domain scientist**—195 notebook cells, 65 DDL statements, zero DBA time—demonstrating that biologists can maintain complex relational models themselves.  
* Public portal (data.betacell.isrd.isi.edu) serves curated datasets to modelling groups exploring β-cell electrophysiology and glucose-stimulated insulin secretion.  

## Typical workflow

1. **Lab uploads** raw files plus minimal metadata via `deriva-cli`; QC checks fire automatically.  
2. **Curator refines** metadata in Chaise, linking specimens to protocols and controlled vocabularies (NCBI Taxon, MGI gene IDs).  
3. **Data scientist** executes a Jupyter notebook that generates processed volumes or whole-cell meshes and pushes results back as a new `ProcessedDataset`.  
4. **Release** toggles ACLs, assigns DOIs, and publishes the record to the public PBCC portal.

## Lessons for other cell-modelling projects

* **Schema-agnostic tools** cut the lag between experimental innovation and repository support.  
* **Executable notebooks** provide both the evolution script and provenance for review, making database change transparent to collaborators and funders.  
* **Continuous FAIRness**—ingest-time identifiers and provenance—avoids costly post-hoc curation when datasets reach terabyte scale.

*Reference*: R.E. Schuler et al., “Database Evolution by Scientists, for Scientists: A Case Study,” *Proc. IEEE e-Science 2023*.

[← Back to all projects](/projects/)
