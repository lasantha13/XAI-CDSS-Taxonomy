# XAI Techniques for AI-Based Clinical Decision Support Systems: 
# A Taxonomic Selection Guide

## Overview

This repository accompanies the following publication:

> [Author names]. "[Full paper title]". [Journal Name], [Year]. DOI: [paper DOI]

This paper presents a taxonomic guide to assist developers and researchers 
in selecting appropriate Explainable AI (XAI) techniques for AI-based 
Clinical Decision Support Systems (AI-CDSS). The guide was developed 
through a rapid review of peer-reviewed literature and preprints, 
yielding 183 included studies and 86 identified XAI techniques.

---

## Repository Contents

| File | Description |
|---|---|
| `README.md` | This file — overview and guidance |
| `taxonomy_tables.md` | Complete taxonomic mapping of 86 XAI techniques across three CDSS input data types |

---

## Taxonomy Structure

The taxonomy organises XAI techniques across three selection guide tables 
based on CDSS input data type:

- **Table 1** — Structured/tabular data inputs
- **Table 2** — Image data inputs  
- **Table 3** — Other data inputs (text, time-series, multimodal)

Each table maps XAI techniques across five dimensions:
1. CDSS Output Type
2. Model Dependency
3. XAI Approach
4. Explainable Scope
5. XAI Technique with representative Clinical Scenarios and references

See `taxonomy_tables.md` for the complete tables.

---

## How to Use the Taxonomy

1. Identify your **CDSS input data type** (structured, image, or other)
   and navigate to the corresponding table in `taxonomy_tables.md`
2. Filter by your **CDSS output type** 
   (e.g. binary classification, risk score, recommendation)
3. Filter by your **model dependency** preference 
   (model-agnostic or model-specific)
4. Review the matching XAI techniques and their associated 
   clinical scenarios to identify the most appropriate method 
   for your use case

---

## How Reported Counts Were Derived

- **341 initial records** were identified through database searches 
  across [list your databases e.g. PubMed, Scopus, IEEE Xplore, 
  and preprint servers], conducted in [month/year of search]
- **183 studies** were included following title/abstract screening 
  and full-text review applying the inclusion and exclusion criteria 
  reported in the manuscript
- **86 XAI techniques** were identified by extracting unique technique 
  names from all included studies. Recognised variants were consolidated 
  under a single label (for example, Grad-CAM and Gradient-weighted 
  Class Activation Mapping were treated as one technique)

Full details of the search strategy, inclusion and exclusion criteria, 
and screening methodology are reported in the published manuscript 
(see DOI above).

---

## Data Availability

The screening log and extracted dataset underlying this review are 
available from the corresponding author upon reasonable request. 
Please contact [corresponding author email].

---

## Citation

If you use this taxonomy in your work, please cite the original paper:

> [Full citation in your target journal format]

---

## License

[Choose one: e.g. Creative Commons CC BY 4.0]

---

## Contact

For questions regarding the taxonomy or repository content, 
please contact [corresponding author name] at [email address].
