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

---

<style>

th, td{
  font-size: 12px !important;
  min-width: 60px;
  padding-top: 0.5rem;
  padding-right: 0.75rem;
  padding-bottom: 0.5rem;
  padding-left: 0.75rem;
  background-color: #fff;
  border-bottom: 1px solid rgba(232, 242, 232, 0.5);
  border-left: 1px solid #e8f2e8;
  }
  @media (min-width: 31.25rem) {
    th,
    td {
      font-size: 14px !important; } }
  th:first-of-type,
  td:first-of-type {
    border-left: 0; 
}

td.best {
    color: black;
    font-weight: 800;
}

th{
    color: black;
    font-weight: 800;
}
th.model {
    min-width: 120px;
    font-weight: 800;

}

#hit {
    text-align: center;
}

#recall {
    text-align: center;
}

.avg{
    font-weight: 800;
    color: black;
    /* color: green; */
    text-decoration: underline;
    font-style: italic;
}

</style>

<style>
/* Tooltip container */
.tooltip {
}

/* Tooltip text */
.tooltip .tooltiptext {
  visibility: hidden;
  width: 200px;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;
 
  /* Position the tooltip text - see examples below! */
  position: absolute;
  z-index: 1;
}

/* Show the tooltip text when you mouse over the tooltip container */
.tooltip:hover .tooltiptext {
  visibility: visible;
}
</style>





## Submission Instruction
{: .no_toc}
If you have a model and would like to make a submission, you can create a submission [***here***](https://opencsr-leaderboard.herokuapp.com){: target="_blank"} and evaluate your predictions (see the format below). 
Your submission will be reviewed by our team and added to the leaderboard here.

### Submission Format
{: .no_toc}
Please submit a ***.jsonl*** file follows the format below, each line is for a question
```json
{"qid": "ACTAAP_2014_7_6", "predictions":["apple", "banana", "car",  "...."]}
{"qid": "ACTAAP_2014_7_7", "predictions":["apple", "banana", "car",  "...."]}
{"qid": "ACTAAP_2014_7_8", "predictions":["apple", "banana", "car",  "...."]}
...
```




## Results 
{: .no_toc}


### Metric = Hit@50 Acc
{: .no_toc}

<table id="hit">
<thead>
   <tr>
    <th class="model">Model </th>
    <th>Participant</th>
    <th>ARC</th>			
    <th>QASC</th>
    <th>OBQA</th>
    <th class="avg">Overall</th>
  </tr>
  
</thead>
<tbody>
   <tr>
    <td> <a href="" target="_blank">BM25 </a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>56.95</td>
    <td>58.50</td>
    <td>53.99</td>
    <td>56.48</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DPR</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>68.67</td>
    <td>69.36</td>
    <td>62.30</td>
    <td>66.78</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DrKIT </a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>67.63</td>
    <td>67.49</td>
    <td>61.74</td>
    <td>65.62</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DrFact</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>71.60</td>
    <td>72.01</td>
    <td>69.01</td>
    <td>70.87</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">BM25+Reranker</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>76.87</td>
    <td>75.75</td>
    <td>79.23</td>
    <td>77.28</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DPR+Reranker</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>76.72</td>
    <td>81.66</td>
    <td>77.16</td>
    <td>78.51</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DrKIT+Reranker</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>78.44</td>
    <td>84.00</td>
    <td>79.25</td>
    <td>80.56</td>
  </tr>
  <tr>
    <td class="best"> <a href="" target="_blank">DrFact+Reranker</a></td>
    <td class="best" class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td class="best">84.19</td>
    <td class="best">89.87</td>
    <td class="best">85.78</td>
    <td class="best">86.61</td>
  </tr>
</tbody>
</table>


### Metric = Recall@50 Acc
{: .no_toc}

<table id="hit">
<thead>
   <tr>
    <th class="model">Model </th>
    <th>Participant</th>
    <th>ARC</th>			
    <th>QASC</th>
    <th>OBQA</th>
    <th class="avg">Overall</th>
  </tr>
  
</thead>
<tbody>
  <tr>
    <td> <a href="" target="_blank">BM25</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>21.12</td>
    <td>16.33</td>
    <td>14.27</td>
    <td>17.24</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DPR</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>28.93</td>
    <td>23.19</td>
    <td>18.11</td>
    <td>23.41</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DrKIT</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>27.57</td>
    <td>21.25</td>
    <td>18.18</td>
    <td>22.33</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DrFact</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>31.48</td>
    <td>23.29</td>
    <td>21.27</td>
    <td>25.35</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">BM25+Reranker</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>39.11</td>
    <td>29.03</td>
    <td>36.38</td>
    <td>34.84</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DPR+Reranker</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>43.78</td>
    <td>40.72</td>
    <td>36.18</td>
    <td>40.23</td>
  </tr>
  <tr>
    <td> <a href="" target="_blank">DrKIT+Reranker</a></td>
    <td class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td>43.14</td>
    <td>39.20</td>
    <td>35.12</td>
    <td>39.15</td>
  </tr>
  <tr>
    <td class="best"> <a href="" target="_blank">DrFact+Reranker</a></td>
    <td class="best" class="tooltip"><a>USC-INK</a> <span class="tooltiptext">yuchen.lin@usc.edu <br> 2021-01-01</span> </td>
    <td class="best">47.73</td>
    <td class="best">44.30</td>
    <td class="best">39.60</td>
    <td class="best">43.88</td>
  </tr>
</tbody>
</table>