---
layout: default
title: 1. Genome Assembly
parent: Modules
nav_order: 1
---

# Module 1: Genome Assembly

Genome assembly is the process of reconstructing a genome sequence from the short or long DNA fragments produced by sequencing machines. Because no current technology can read an entire chromosome in one pass, sequencers produce millions of overlapping reads that must be computationally stitched back together.

## Short Reads vs Long Reads

Two major paradigms exist for sequencing and assembly:

| Feature | Short Reads (Illumina) | Long Reads (PacBio / ONT) |
| :--- | :--- | :--- |
| **Read length** | 150 – 300 bp | 10 kb – 100+ kb |
| **Error rate** | Very low (~0.1%) | Higher (~1–5%) raw error |
| **Repeat resolution** | Difficult | Excellent |
| **Cost per base** | Low | Higher |
| **Best for** | SNP calling, small genomes | Structural variants, repeat-rich genomes |

## Learning Objectives

- Understand the difference between short-read and long-read assembly strategies
- Run a short-read assembly using Velvet/SPAdes in Galaxy
- Run a long-read assembly using Flye in Galaxy
- Assess assembly quality with QUAST and BUSCO

## Hands-on Tutorials

### Hands-on 1 — Short Read Assembly
Using *Xanthomonas oryzae* pv. *oryzae* Illumina reads as a model organism.

**Galaxy Training Network tutorial:**
[General Introduction to Assembly](https://training.galaxyproject.org/training-material/topics/assembly/tutorials/general-introduction/tutorial.html)

**Key tools used:**
- **Velvet / SPAdes** — de novo assemblers for short reads
- **QUAST** — assembly quality statistics
- **BUSCO** — benchmarking assembly completeness

---

### Hands-on 2 & 3 — Long Read Assembly (PacBio)
Using a subset of rice (*Oryza sativa*) chromosome 9 PacBio data.

**Galaxy Training Network tutorial:**
[Large Genome Assembly and Polishing](https://training.galaxyproject.org/training-material/topics/assembly/tutorials/largegenome/tutorial.html#large-genome-assembly-and-polishing)

**Key tools used:**
- **Flye** — de novo assembler for single-molecule long reads
- **QUAST** — assembly quality statistics
- **BUSCO** — completeness assessment

## Key Concepts

**N50** — A summary statistic for assembly quality. Half of the total assembled bases are in contigs of N50 length or longer. A higher N50 generally indicates a more contiguous assembly.

**Contig vs Scaffold** — A *contig* is a contiguous assembled sequence with no gaps. A *scaffold* is a higher-order structure where contigs are ordered and oriented using additional information (e.g., paired-end reads, Hi-C), with gaps filled by Ns.

**Polishing** — For long-read assemblies with higher raw error rates, a polishing step uses high-accuracy short reads to correct base-level errors in the draft assembly.

## Useful Resources

- [Sequence Read Archive (SRA) — Xanthomonas oryzae data](https://www.ncbi.nlm.nih.gov/sra/?term=xanthomonas+oryzae+pv+oryzae)
- [Galaxy Training Network — Assembly Tutorials](https://training.galaxyproject.org/training-material/topics/assembly/)
