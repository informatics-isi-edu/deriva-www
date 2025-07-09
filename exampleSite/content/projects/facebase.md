---
title: "FaceBase"
date: 2018-11-18T12:33:46+10:00
draft: false
featured: true
weight: 1
---

FaceBase is an NIH-funded, open community hub that curates and serves more than 1,100 FAIR datasets in craniofacial and dental biology.  Powered by the DERIVA platform, the repository supports self-curation by researchers, integrates interactive imaging and single-cell viewers, and assigns DOIs for every dataset to ensure citation and reuse.  
<!--more-->

## Why FaceBase is based on DERIVA

| Requirement | DERIVA capability |
|-------------|-------------------|
| **Evolving, project-defined schema** | Model-adaptive interfaces auto-generate search, browse, and edit pages when tables change. |
| **Self-curation at scale** | Web and desktop tools validate metadata, enforce controlled vocabularies, and version large file uploads without curator intervention. |
| **Proven FAIR compliance** | Persistent IDs, fixity checks, and rich provenance satisfy NIDCR and publisher mandates. |
| **Automation hooks** | QC pipelines, DOI minting, and thumbnail generation run immediately after ingest, cutting manual effort. |

## Impact to date

* 30 new contributing projects onboarded between 2019-2022.  
* Over 1,100 public datasets, covering 40+ assay types and ~4.5 TB of files.  
* 7,600 unique visitors and ~45,000 file downloads in a recent six-month window.  
* Cited in 210 publications, including secondary analyses that revealed regulatory networks in cleft-lip development.

## Example workflow

1. **Investigator** uploads raw sequencing files and sample metadata via `deriva-cli`.  
2. **Automated QC** checks checksums, validates ontology terms, and flags gaps on a dashboard.  
3. **Chaise UI** allows the lab to edit records in bulk and link processed outputs.  
4. **Release** button publishes the dataset, assigns a DOI, and makes it discoverable on FaceBase and Google Dataset Search.

## Lessons for other consortia

FaceBase demonstrates that **researcher-driven curation** is viable when tooling guides users and integrates QC early in the data lifecycle.  By choosing a schema-agnostic platform, the hub accommodated new imaging and single-cell modalities without database rewrites, and DERIVA’s versioned storage preserved every update for reproducibility.

*For more details see:* R.E. Schuler et al., *Journal of Dental Research* 2022.

[← Back to all projects](/projects/)
