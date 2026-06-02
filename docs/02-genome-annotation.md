---
layout: default
title: 2. Genome Annotation
parent: Modules
nav_order: 2
---

# Module 2: Genome Annotation

Genome annotation is the process of identifying and labeling functional elements in a genome assembly — including genes, repetitive elements, regulatory regions, and non-coding RNAs. A raw assembly is just a string of nucleotides; annotation transforms it into a biologically interpretable resource.

## Types of Annotation

| Type | What it finds | Examples |
| :--- | :--- | :--- |
| **Structural** | Gene boundaries, exons, introns, UTRs | BRAKER3, Helixer |
| **Functional** | Gene function, protein domains | BLAST, InterProScan |
| **Repeat** | Transposable elements, repeat families | RepeatMasker |
| **Quality** | Annotation completeness | BUSCO, OMArk |

## Learning Objectives

- Mask repetitive elements before gene prediction
- Predict gene structures using evidence-based and ab initio methods
- Assess annotation completeness and quality
- Visualize annotated features in a genome browser

## Hands-on Tutorials

### Hands-on 1 — Getting Started
Introduction to genome annotation tools and workflows in Galaxy.

**Galaxy Training Network tutorials:**
[Genome Annotation Tutorials](https://training.galaxyproject.org/training-material/topics/genome-annotation/)

---

### Hands-on 2 — Basic Gene Structure Annotation
Gene structure annotation for sequences not yet at contig/scaffold level.

**Key tools used:**
- **RepeatMasker** — identify and soft-mask repetitive elements
- **RNA-STAR** — align RNA-seq reads to the genome for splice site evidence
- **BRAKER3** — ab initio gene prediction with RNA-seq and protein evidence
- **GFFread** — process and convert GFF/GTF annotation files

---

### Hands-on 3 & 4 — Annotation Using Pipelines
Running complete annotation pipelines in Galaxy and assessing outputs.

**Key tools used:**
- **Helixer** — deep learning–based gene structure prediction
- **BUSCO** — benchmarking annotation completeness using conserved gene sets
- **OMArk** — proteome quality assessment

---

### Hands-on 4 — Visualization with WebIGV
Exploring annotated features interactively in the browser.

**Key tools used:**
- **JBrowse / WebIGV** — view GFF annotation tracks alongside the assembly sequence

## Key Concepts

**GFF3 / GTF** — Standard file formats for storing genome annotation. GFF3 (Generic Feature Format version 3) and GTF (Gene Transfer Format) describe genomic features with their chromosomal coordinates.

**Evidence-based vs Ab Initio** — Evidence-based annotation uses experimental data (RNA-seq, protein homology) to guide gene finding. Ab initio prediction relies solely on statistical models trained on known gene structures.

**Repeat masking** — Before gene prediction, repetitive sequences are masked (replaced with lowercase letters or Ns) to prevent them from confusing gene finders.

**BUSCO score** — Measures the percentage of expected conserved genes found in an assembly or annotation. A high complete BUSCO score indicates a high-quality, near-complete result.

## Useful Resources

- [Galaxy Training Network — Genome Annotation](https://training.galaxyproject.org/training-material/topics/genome-annotation/)
- [BRAKER3 on ToolShed](https://toolshed.g2.bx.psu.edu/)
- [Oryza Base](https://shigen.nig.ac.jp/rice/oryzabase/)
- [RAP-DB Curated Gene List](https://rapdb.dna.naro.go.jp/curated_genes/curated_gene_list.html)
- [Rice Genome Annotation Project](https://rice.uga.edu/)
