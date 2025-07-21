---
title: "Common Fund Data Ecosystem"
date: 2018-11-28T15:15:34+10:00
featured: true
draft: false
weight: 5
---

The NIH Common Fund Data Ecosystem (CFDE) used DERIVA to prototype its first cross-program metadata catalog and search portal, harmonising descriptions from 11 Data Coordination Centers (DCCs) into a single schema (C2M2) and ingest workflow.  
<!--more-->

## How DERIVA accelerated the CFDE pilot

| Challenge | DERIVA capability |
|-----------|-------------------|
| Ingest heterogeneous metadata from multiple DCCs | **Model-driven schema (ERMrest)** let each DCC map local tables to the Crosscut Metadata Model without code changes. |
| Quarterly submissions, preview, and approval | **Versioned staging catalogs** gave DCCs a private area to validate TSV packages and run automated QC before release. |
| Search across millions of assets | **Chaise UI + full-text index** provided faceted search on controlled vocabularies (anatomy, assay, disease, file type). |
| DOI-ready landing pages | Out-of-the-box templates exposed JSON-LD and downloadable BDBag bundles for every collection. |

## Impact during the DERIVA phase (2020 – 2023)<sup>1</sup>

* **3.0 million files**, **1.7 million biosamples**, and **34 k subjects** discoverable in the portal.  
* **11 DCCs** mapped their metadata to C2M2 and submitted quarterly packages.  
* **Six working groups** (ontologies, identifiers, user-experience, etc.) met bi-weekly using DERIVA preview catalogs.  
* Usability tests showed **40 % reduction** in time to locate relevant datasets compared with Google or individual program portals.

## Submission workflow

1. Each DCC exported TSVs for files, biosamples, subjects, projects, collections.  
2. `cfde-submit` packaged the TSVs into a BDBag and uploaded via Globus Flows.  
3. DERIVA loaded the package into a **sandbox catalog**, ran validation, and emailed a preview link.  
4. After curator approval, the package was merged into the **public catalog** on the next quarterly release.

## Lessons learned

* **Incremental adoption**: DCCs began with minimal inventories and iterated toward richer relationships without refactoring.  
* **Separation of concerns**: DERIVA handled ingest, versioning, and UI while CFDE engineers focussed on the C2M2 schema and community governance.  
* **Easy off-ramp**: Because all metadata lived in a relational catalog with well-defined APIs, migrating to the successor platform required only new export scripts—no data loss.

<sup>1</sup> A. L. Charbonneau *et al.* “Making Common Fund Data More Findable: Catalyzing a Data Ecosystem.” *GigaScience* 11 (2022): giac105. DOI 10.1093/gigascience/giac105.

[← Back to all projects](/projects/)
