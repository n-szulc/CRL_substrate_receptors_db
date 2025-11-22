# 📚 Cullin–RING Ligase Substrate Receptors Database


This programming-friendly dataset catalogs **267 substrate receptors of cullin–RING ligases** supported by low-throughput experimental evidence, excluding discovery proteomics unless followed by targeted validation. For each substrate receptor, we prioritized primary sources to substantiate its cullin assignment(s) and annotated germline disease associations and tissue specificity where available.

## 📋 Table of Contents

  - [Column Guide](#column-guide)
  - [The "Semicolon & Ampersand" Logic](#the-semicolon--ampersand-logic)
  - [How to Cite](#how-to-cite)
  - [Contact](#contact)

-----

## 🗝️ Column Guide

### 🏷️ Primary Name

Preferred gene/protein symbol per UniProt. One substrate receptor (SR) per row.

### 🔄 Alternative Names

Synonyms from UniProt, separated by commas.

### ⚙️ Associated Cullin(s)

The cullin core(s) the SR associates with.

  * Semicolon (`;`) separates distinct cullin assignments for the same SR.
  * Accepted values: CUL1, CUL2, CUL3, CUL4, CUL5, CUL7.

### 📄 Associated Cullin(s) Evidence

Primary reference(s) supporting the cullin assignment(s).

  * Semicolon (`;`) separates entries aligned in order with the **Associated Cullin(s)** column.
  * Within a single entry, an ampersand (`&`) joins multiple PMIDs that support the same calling.
  * *Example:* `10437795 & 11158290; 31092637` → the first two PMIDs support the first cullin; the last PMID supports the second.
  * Populated with PMIDs; if a PMID isn’t available, a URL is provided.

### 🧐 Associated Cullin(s) Comment

Optional qualifier per cullin assignment.

  * Accepted values: `Probable` or `Atypical`.
  * Semicolon (`;`) separates entries aligned with the **Associated Cullin(s)** column.
  * If blank, the calling(s) is treated as established (i.e., not “probable”).

### 🧬 Type

SR class. The accepted values are:

  * **F-box** - CUL1 adaptors
  * **VHL-box** - CUL2 adaptors
  * **BTB** - CUL3 adaptors (BTB/Kelch)
  * **DCAF/WD40** - CUL4 adaptors (WD-repeat DDB1 binders)
  * **CRL4 non-DCAF** - CUL4 adaptors lacking canonical DWD/WDxR
  * **SOCS-box** - CUL5 adaptors
  * **Other** — SRs that don’t fit the above classes

### 🏥 OMIM Number

OMIM entry number(s) for OMIM-curated diseases linked to the SR (not to a specific cullin calling).

  * Semicolon (`;`) separates distinct OMIM entries.

### 🩺 OMIM Phenotype

Exact phenotype name(s) as written in the OMIM database.

  * Semicolon (`;`) separates entries positionally aligned with the **OMIM Number** column.

### 🧪 Disease (non-OMIM)

Manually curated description(s) of human disease occurrences from primary literature or reviews that are not listed in OMIM.

  * Semicolon (`;`) separates distinct non-OMIM diseases.

### 📑 Disease (non-OMIM) Evidence

Reference(s) for each non-OMIM disease.

  * Semicolon (`;`) separates sources positionally aligned with the **Disease (non-OMIM)** column.
  * Accepts PMIDs; if a PMID isn’t available, provides a URL.

### 🗂️ Disease Category

Broad category for every disease linked to the SR, covering both OMIM and non-OMIM entries. Categories were chosen to reflect the predominant and defining clinical features, prioritizing core pathophysiology over secondary manifestations. For multisystem disorders, classification was based on the system most critically and consistently affected across reported cases.

  * Semicolon (`;`) separates categories in the same order the diseases are listed: first all OMIM phenotypes, then all non-OMIM diseases.

### 🧠 Tissue Specificity

Tissues where the SR shows relatively enriched expression based on RNA expression data from the Human Protein Atlas.

  * If blank, interpret as more ubiquitous expression (not necessarily uniform across all tissues).

-----

## 🧩 The "Semicolon & Ampersand" Logic

We use semicolon-separated lists in three independent blocks of columns. Alignment is positional within each block only.

**Block A — Cullin Callings (three columns together):**

  * `Associated Cullin(s)`
  * `Associated Cullin(s) Evidence`
  * `Associated Cullin(s) Comment`
  * *Logic:* Items are aligned by semicolon position (one-to-one). Inside the Evidence column, an ampersand (`&`) joins multiple PMIDs for the same single calling.

**Block B — OMIM Diseases (two columns together):**

  * `OMIM Number`
  * `OMIM Phenotype`
  * *Logic:* Items are aligned by semicolon position (one-to-one).

**Block C — non-OMIM Diseases (two columns together):**

  * `Disease (non-OMIM)`
  * `Disease (non-OMIM) Evidence`
  * *Logic:* Items are aligned by semicolon position (one-to-one).

**Note:** The `Disease Category` column spans both OMIM and non-OMIM disease lists (its semicolons cover the combined list, in that order). The semicolon/ampersand alignment applies only to the blocks above. Other columns are free text and do not participate in positional alignment.

-----

## ✒️ How to Cite

If you use this database in your research, please cite the review article:

> **Szulc, N.A. & Pokrzywa, W. (2025)** Cullin–RING receptors in rare disease biology. *Trends in Cell Biology*. [DOI: To be updated]

-----

## 📧 Contact

For questions, corrections, or additions to the database, please contact the authors:

  * **Natalia A. Szulc:** nszulc@iimcb.gov.pl
  * **Wojciech Pokrzywa:** wpokrzywa@iimcb.gov.pl

See also [pokrzywalab.com](https://pokrzywalab.com)
