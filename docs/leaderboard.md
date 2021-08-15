---
layout: default
title: Leaderboard
nav_order: 5
toc_list: true
last_modified_date: Jun 5th 2021
permalink: /leaderboard
---

# Leaderboard
{: .no_toc}





## Submission Instruction
If you have a model and would like to make a submission, you can create a submission [***here***](https://opencsr-leaderboard.herokuapp.com) and evaluate your predictions. 


### Submission Format
Please submit a ***.jsonl*** file follows the format below, each line is for a question
```json
{"qid": "ACTAAP_2014_7_6", "predictions":["apple", "banana", "car",  "...."]}
{"qid": "ACTAAP_2014_7_7", "predictions":["apple", "banana", "car",  "...."]}
{"qid": "ACTAAP_2014_7_8", "predictions":["apple", "banana", "car",  "...."]}
...
```

Your submission will be reviewed by the X-CSR team and added to the leaderboard.