---
layout: default
title: Methods
nav_order: 3
has_children: true
has_toc: false
permalink: /methods/
---

# Methods
{: .no_toc}

<!-- 
## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc} -->


---

[**The site is under active updating. The links to the datasets and code will be updated asap.  Please come back and check it out in a few days.**](){: .btn .btn-red .fs-4 target="_blank"}

# Methods for OpenCSR

We show the instructions for running four retrieval approaches to the OpenCSR task --- [**BM25**](bm25) (off-the-shelf), [**DPR**](dpr) (EMNLP2020), [**DrKIT**](drkit) (ICLR 2020) and [**DrFact**](drkit) (ours, NAACL 2021), as well as a [**Concept Re-ranker**](reranker) to boost the performance by learning with cross-attention. 

Note that there is a relative dependency of these four methods: training the DPR model needs the results from BM25 (to create training data); DrFact needs to reuse DPR's fact index and single-hop results (for creating distant supervision); DrFact and DrKIT share many utility functions (sparse matrix operation and indexing scripts).  We detailed the detailed instructions in individual pages.

## Folder structure 

- drfact_data/
    - datasets/
- drfact_data/
    - knowledge_corpus/
- baseline_methods/
    - BM25/
    - DPR/
    - MCQA/     **_(i.e., Concept Re-ranker)_**
- language-master/  **_(for DrKIT)_**
- drfact/   



## Comparisions of the four methods 

![Comparisions](/images/comparisions.png){: style="text-align:center; display:block; margin-left: auto; margin-right: auto;" width="95%"}