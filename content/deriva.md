---
title: 'The DERIVA Platform'
date: 2018-02-22T17:01:34+07:00
---

The Discovery Environment for Relational Information and Versioned Assets (DERIVA) is an open-source, model-driven platform that turns any research dataset — imaging, ‘omics, models, protocols, and much more — into a continuously FAIR, version-controlled, and citable asset.  

Built at the USC Information Sciences Institute, the stack has powered a broad array of NIH-funded biomedical research consortia such as FaceBase, PDB-IHM, and the Common Fund Data Ecosystem.  

## Why DERIVA?

Modern science generates heterogeneous files faster than curators can harmonise them and at an unprecedented breadth and depth.  Common tools such as Dropbox or lab wikis can store files, but they don’t track where the data came from or how it has changed; meanwhile, large laboratory information-management systems tend to be rigid and hard to update when researchers switch to new experiments or instruments.

DERIVA sits in the middle:

* **Schema-adaptive** – scientists edit the ER model; the UI and APIs update automatically.  
* **Continuous FAIRness** – persistent IDs and provenance are minted at ingest, not after publication.  
* **Self-curation at scale** – web, CLI, and desktop tools let labs deposit data while curators review QC dashboards.  
* **End-to-end versioning** – every file revision and database row is traceable and recoverable.

## What researchers can do with DERIVA

* **Ingest** and richly describe diverse scientific assets.  
* **Query & discover** via faceted search, SQL, or Python SDK.  
* **Link** raw data → processed outputs → figures with full provenance.  
* **Share** data collections privately or publicly with DOI landing pages.  
* **Enforce access control** down to the row or object level.  

![Screenshot of the search page for facebase.org](/images/search-page.png)
*Screenshot of the main search page for FaceBase*

## Core components

| Layer | Component | Purpose |
|-------|-----------|---------|
| **Client Applications** | **Chaise** (model-driven web UI) <br> **deriva-qt** (desktop GUI) <br> **deriva-cli** (bulk ingest) | Curate, browse, and upload data |
| **Client Libraries** | **deriva-py** (Python SDK) <br> **ERMrestJS** (JS client) | Automate ingest, QC, and analytics |
| **Server Services** | **ERMrest** (relational metadata) <br> **Hatrac** (object store) <br> **ERMresolve** (ID resolver) <br> **IOBoxD** (export service) | Version data, mint IDs, serve APIs |
| **Orchestration** | Flow-based automation and scheduled tasks | Validation, DOI minting, QC reports |

All services communicate over open REST/HTTP; deployments range from a single VM to Kubernetes clusters.
<!--
## Proven impact

* **over 4 million files** and **over 250 TB** managed across FaceBase, RBK/GUDMAP, PDB-IHM, PBCC, CFDE, and EyeAI.  
* **Hundreds of DOIs** minted; datasets cited in **>300 publications**.  
* Data-centric ML workflows (DERIVA-ML) cut model re-training time by **40 %** in EyeAI glaucoma study.  
-->

## Governance & licensing

DERIVA is released under the Apache 2.0 licence. Work is funded by multiple NIH grants (NIDCR, NIDCD, NIDDK, NIGMS, NLM, NEI) and maintained by the Informatics Systems Research Division at USC ISI.  

<!--
---

## Suggested figure updates

ChatGPT suggested the following update. But could just verify the Core Components table above and once that's confirmed - can generate a figure representing it.

```

┌─────────────────────────────┐
\|  Client Apps (Chaise, Qt)   |
\|  Libraries (Python, JS)     |
└────────────┬────────────────┘
│ REST/HTTPS
┌────────────┴────────────────┐
\|  Metadata (ERMrest)         |
\|  Object Store (Hatrac)      |
\|  ID Resolver (ERMresolve)   |
└────────────┬────────────────┘
│
┌────────────┴────────────────┐
\|  Storage & Compute Fabric   |
\|  (POSIX, S3, Globus, GPU)   |
└─────────────────────────────┘

````
*Show clear separation between UI, services, and infrastructure.*
-->
