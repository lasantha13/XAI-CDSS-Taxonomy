# XAI Techniques for AI-Based Clinical Decision Support Systems: 
# A Taxonomic Selection Guide

## Overview

This repository accompanies the following publication:

>R A D L M K Ranwala 1*, Libby Roughead 1, Jean-Pierre Calabretto 2 and Andre Q. Andrade 1 . "A Taxonomic Guide to Explainable AI (XAI) Technique 
Selection in Clinical Decision Support Systems
". Information Journal, 2026. DOI: [DOI]
>
>1 Adelaide University of South Australia - Quality Use of Medicines and Pharmacy Research Centre, Clinical and Health Sciences, Level 6, Playford Building, Frome Road, Adelaide 5000, South Australia, Australia

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

- **Table 3** — Structured/tabular data inputs
- **Table 4** — Image data inputs  
- **Table 5** — Other data inputs (text, time-series, multimodal)

Each table maps XAI techniques across five dimensions:
1. CDSS Output Type
2. Model Dependency
3. XAI Approach
4. Explainable Scope
5. XAI Technique with representative Clinical Scenarios and references

See `taxonomy_tables.md` for the complete tables.

---

## How to Use the Taxonomy
To select suitable XAI techniques for an AI-CDSS using the XAI user guide table (Table 3, Table 4, Table 5), users must answer five key questions related to their system. 
1.	What is the input data type of the CDSS?
2.	What is the output type of the CDSS?
3.	Should the explanation be designed for a specific AI model or work across different models?
4.	Should explanations be built into the CDSS, or applied after its development? 
5.	Should the explanation provide overall model behaviour or focus on individual prediction reasoning, or both?

---

## How Reported Counts Were Derived

- **341 initial records** were identified through database searches 
  across [Scopus, IEEE Xplore,and preprint servers] published up to 31st December 2024.
- **183 studies** were included following title/abstract screening 
  and full-text review applying the inclusion and exclusion criteria 
  reported in the manuscript
- **86 XAI techniques** were identified by extracting unique technique 
  names from all included studies. 
Full details of the search strategy, inclusion and exclusion criteria, 
and screening methodology are reported in the published manuscript 
(see DOI above).

---

## Data Availability

The screening log and extracted dataset underlying this review are 
available from the corresponding author upon reasonable request. 
Please contact a3151038@adelaide.edu.au.

---

## Citation

If you use this taxonomy in your work, please cite the original paper:

> [Full citation in your target journal format]

---
## Contact

For questions regarding the taxonomy or repository content, 
please contact Dr Lasantha Ranwala at a3151038@adelaide.edu.au.
