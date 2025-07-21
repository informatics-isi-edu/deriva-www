---
title: "ReBuilding A Kidney Consortium"
date: 2018-11-28T15:15:34+10:00
featured: true
draft: true
weight: 5
---

The (Re)Building a Kidney (RBK) consortium used DERIVA to operate an open-access data hub that integrated imaging, single-cell sequencing, and protocol metadata from laboratories studying kidney repair and regeneration.  The hub enabled FAIR sharing of more than 250 datasets.  
<!--more-->

RBK was an NIDDK-funded consortium of research projects working to optimize approaches for the isolation, expansion, and differentiation of appropriate kidney cell types and their integration into complex structures that replicate human kidney function.

## Why RBK selected DERIVA

| Challenge | DERIVA capability |
|-----------|-------------------|
| Diverse assay types (Bulk RNA-seq, scRNA-seq, organoid images) | **Schema-agnostic catalog** let curators add tables for new modalities without downtime. |
| Self-deposit by scientists | Browser-based forms validated controlled vocabularies (e.g. Uberon anatomy) and file checksums at upload. |
| Provenance from raw data to figures | Versioned object store (Hatrac) plus BagIt/BDBag bundles preserved every processing step and maintained fixity. |
| Open discovery by the kidney community | Chaise provided faceted search on assay, species, injury model; each dataset page exposed JSON-LD for Google Dataset Search. |

## Impact while on DERIVA<sup>1</sup>

* **250 + datasets** covering transcriptomics, imaging, metabolomics, and protocols.  
* Single-cell & single-nucleus RNA-seq collections totalled **> 1 billion reads** and informed the 2022 *Kidney International* special report on AKI→CKD transition.  
* **18 consortium groups** deposited data; validation time fell from days to **< 2 hours** once automated QC was deployed.  
* Datasets cited in **60 + publications**, including first maps of maladaptive proximal-tubule repair and zebrafish neonephrogenesis.

## Typical submission workflow

1. **Lab** exports metadata and raw files; uses DERIVA command line tools to upload many or large files.  
2. **Sandbox catalog** ingests the package, validates ontologies, and emails a preview link.  
3. **Curator** reviews QC dashboard, edits metadata in Chaise.  
4. **Release** toggles ACLs, mints a DOI via EZID, and promotes the dataset to the public RBK portal.


## Lessons for future repair & regeneration consortia

* **Schema-first, code-second** approach lets scientists, not DB admins, evolve the model as biology evolves.  
* **Continuous FAIRness** avoids costly, post-hoc harmonisation when datasets exceed terabytes.  
* **Sandbox → public release workflow** balances rapid sharing with quality control and fosters contributor trust.

---

<sup>1</sup> Naved B.A. *et al.* “Kidney Repair and Regeneration: Perspectives of the NIDDK (Re)Building a Kidney Consortium,” *Kidney International* 101 (2022): 845-853. DOI 10.1016/j.kint.2022.02.023

[← Back to all projects](/projects/)
