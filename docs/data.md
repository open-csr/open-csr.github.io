---
layout: default
title: Data
nav_order: 2
# toc_list: true
last_modified_date: April 1st 2021
permalink: /data
has_toc: true
---

## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}


---

## The OpenCSR Datasets
We present the three datasets used for studying OpenCSR, which we got by reformatting the multiple-choice QA datasets -- ARC, OBQA, and QASC. 

<!-- ### Raw Datasets -->

[Download](){: .btn .btn-blue .fs-2 target="_blank"}

This zip file contains train/dev/test data in *jsonl* format (i.e., each line is a dictionary in json) for ARC, OBQA, and QASC. Note that the gold annotations (i.e.,`all_answer_concepts` items) for the test sets are hidden for hosting [a shared task](/leaderboard) to fairly compare the submissions. 
Below are two examples for **training/validation** instances:

```json
// Example 1
{
  "_id": "OBQA-257",  
    // unique example id
  "question": "Global warming is lowering the world's amount of ( ___ ) ",  
    // input: question text
  "question_concepts": ["global warming", "global", "warming", "world", "amount"],  
    // supplmentary info: simple concept matching over the question text.
  "original_choice_text": "ice", 
    // supplmentary info: correct choice of the original data
  "all_answer_concepts": ["ice"],
    // output: answer concepts that a model needs to retrieve
  "all_answer_concepts_decomp": ["ice"]
    // supplmentary info: the decomposition of the "all_answer_concepts"
}

// Example 2
{
  "_id": "ARC-Mercury_7267873", 
  "question": "What provide the best evidence that life could develop on Mars?", 
  "question_concepts": ["evidence", "life", "develop", "mars"], 
  "original_choice_text": "its ice and organic molecules", 
  "all_answer_concepts": ["organic molecule", "ice"],
  "all_answer_concepts_decomp": ["organic molecule", "ice", "organic", "molecule"]
}
```
<!-- 
// Example 3
{
  "_id": "ARC-Mercury_400056", // unique example id
  "question": "What plant trait is inherited?", // task input: question text
  "entities": ["plant", "trait"], 
    // optional info: simple concept matching.
  "original_choice": "the shape of its leaves", 
    // optional info: correct choice of the original data  
  "all_answer_concepts": ["shape", "leaf"]
    // output: answer concepts that a model needs to retrieve (as many as possible)
}

 -->

Here is an example of the *test* data (the last two items are hidden):

```json
{
  "_id": "ARC-Mercury_SC_400328", 
    // unique example id
  "question": "What item is used for protection from chemical splashing?", 
  "question_concepts": ["chemical splashing", "item", "use", "protection", "chemical"], 
    // supplmentary info: simple concept matching over the question text.
  "original_choice_text": "safety goggle", 
    // hidden info.
  "all_answer_concepts": ["safety goggle", "lab coat", "rubber boot", "protective glove", "face shield", "helmet", "shoe", "glass", "goggle", "glove", "coverall"] 
    // hidden info; used for evaluaiton. 
    // The first one is from the original choice, and others are from our crowdsourcing.
}
```



**Please also cite the papers of these original datasets if you use the data here.** 
```bib
@article{clark2018think,
  title={Think you have solved question answering? try arc, the ai2 reasoning challenge},
  author={Clark, Peter and Cowhey, Isaac and Etzioni, Oren and Khot, Tushar and Sabharwal, Ashish and Schoenick, Carissa and Tafjord, Oyvind},
  journal={arXiv preprint arXiv:1803.05457},
  year={2018}
}

@inproceedings{mihaylov2018can,
    title = "Can a Suit of Armor Conduct Electricity? A New Dataset for Open Book Question Answering",
    author = "Mihaylov, Todor  and Clark, Peter  and Khot, Tushar  and Sabharwal, Ashish",
    booktitle = "Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing",
    year = "2018"
}

@inproceedings{khot2020qasc,
  author    = {Tushar Khot and  Peter Clark and Michal Guerquin and Peter Jansen and Ashish Sabharwal},
  title     = {QASC: A Dataset for Question Answering via Sentence Composition},
  booktitle = {The Thirty-Fourth AAAI Conference on Artificial Intelligence, AAAI
               2020, New York, NY, USA, February 7-12, 2020},
  year      = {2020}
}
```
<!-- 
### Preprocessed Dataset

This zip file contains the same data as above, while it also includes results of basic preprocessing steps, e.g., lemmatization,  -->


## The Commonsense Knowledge Corpus

[Download](){: .btn .btn-blue .fs-2 target="_blank"}

We use the [GenericsKB](https://allenai.org/data/genericskb){: target="_blank"} as our knowledge corpus. We preprocess the coprus, extract the frequent concepts, and finally link the facts to their mentioned concepts. The link contains two files:

- `gkb_best.drfact_format.jsonl` consists of generics commonsense facts, each of which is a statement of common knowledge. (See an example below.)
- `gkb_best.vocab.txt` is the vocabulary of the concepts (i.e., noun chunks) sorted by their frequency.

Here is an example json line for the commonsense fact: "_Trees remove dust and pollution from the air._"
```json
{
    "id": "gkb-best#934338", "url": "gkb-best#934338",
    "context": "Trees remove dust and pollution from the air .",
    "mentions": [
        { "kb_id": "tree", "start": 0, "text": "Trees", "sent_id": 0 },
        { "kb_id": "dust", "start": 13, "text": "dust", "sent_id": 0 },
        { "kb_id": "pollution", "start": 22, "text": "pollution", "sent_id": 0 },
        { "kb_id": "air", "start": 41, "text": "air", "sent_id": 0 }
    ],
    "title": "Trees", "kb_id": "tree"
}
```


**Please also cite the GenericsKB paper if you use the data here.**

```bib
@article{Bhakthavatsalam2020GenericsKBAK,
  title={GenericsKB: A Knowledge Base of Generic Statements},
  author={Sumithra Bhakthavatsalam and Chloe Anastasiades and P. Clark},
  journal={ArXiv},
  year={2020},
  volume={abs/2005.00660}
}
```