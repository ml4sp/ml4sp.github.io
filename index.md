---
layout: page
title: 2nd Workshop on Machine Learning on Solvers and Provers (ML4SP)
---
<!-- <div class="venue" style="font-size: 27px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <a target="_blank" href="https://neurips.cc/virtual/2023/tutorial/73946"><strong>Video Recording</strong></a>
</div> -->

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>Lisbon, Portugal </strong>
</div>

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>18 July, 2026 (Saturday) </strong>
</div>

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>As part of <a href="https://www.floc26.org/" style="color: #007bff; text-decoration: none;">FLoC 2026</a></strong>
</div>

<!-- <div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>James McCune Smith Learning Hub, <a target="_blank" href="https://www.gla.ac.uk/">University of Glasgow</a>, Glasgow, Scotland</strong>
</div> -->

<!-- <div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>Invited Talks Workshop</strong>
</div> -->

<!-- <div class="venue" style="font-size: 20px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <a target="_blank" href="https://aaai.org/conference/aaai/aaai-25/tutorial-and-lab-list/#TH24">(AAAI 2025 website)</a>
</div> -->

<!-- <div class="sharethis-inline-share-buttons"></div> -->
<!-- <meta name="thumbnail" content="https://ml-for-solvers.github.io/img/aaai-small.jpeg" /> -->

<hr>

<nav style="text-align: center;">
  <a href="#topics">Topics</a> |
  <a href="#submission">Submission</a> |  
  <a href="#dates">Dates</a> |
  <a href="#registration">Registration</a> |
  <a href="#invited-talks">Invited Talks</a> | 
  <a href="#schedule">Schedule</a> |
  <a href="#organizers">Organizers</a>
</nav>

<hr>

# Topics

Machine learning (ML) has had a substantial impact on SAT/SMT and CP solvers, as well as automated theorem provers. Recent advances have demonstrated the power of ML to inform solver heuristics, guide proof search, and optimize algorithm portfolios. Despite growing interest in this direction, work on ML for solvers and provers is often scattered across multiple research communities – SAT, SMT, CP, theorem proving, formal methods, and machine learning – with few opportunities for focused interaction. 

The ML4SP workshop aims to bring together researchers and practitioners working at the intersection of machine learning and formal reasoning systems. It provides a forum for the presentation of recent work, the exchange of ideas, and the fostering of collaboration between these communities.

Topics of interest include, *but are not limited to*, ML-driven approaches for:
- Heuristics (branching, restarts, ...) in CP, SAT, SMT, and MIP solvers
- Tactic selection and proof guidance in automated and interactive theorem provers
- Algorithm selection, parameter tuning and algorithm configuration, and portfolio solvers
- End-to-end learning for solvers and provers
- Benchmark generation and instance hardness prediction
- Applications of ML-enhanced reasoning in verification, synthesis, planning, and related areas
- Leveraging large language models (LLMs) for solver heuristics and proof guidance

This is a 2nd year of the workshop. The [1st ML4SP workshop](https://ml4sp.github.io/2025/) (invited talks only) was organized at [SoCS](https://socs25.search-conference.org/)/[SAT](https://satisfiability.org/SAT25/)/[CP 2025](https://cp2025.a4cp.org/cfp.html) in Glasgow.

<hr>

# Submission

We welcome submissions describing **previously published work**, **ongoing research**, and **position papers and early-stage ideas** intended to stimulate discussion. 
Submission should be in PDF form, following the [LIPIcs guidelines](https://submission.dagstuhl.de/series/details/5#author). They can be:
- *Extended abstracts* (up to two pages, excluding references); or 
- *Full papers* (up to 15 pages, excluding references). 

All submissions will be reviewed by the PC members. A presentation time slot will be given to each accepted submission. 

**Submission link:** [https://submissions.floc26.org/ml4sp/](https://submissions.floc26.org/ml4sp/)

<hr>

# Dates

- Submission deadline: **15 May 2026 (AoE)**
- Result notification: 25 May 2026
- Camera ready: 2 July 2026
- Workshop day: 18 July 2026


<hr>

# Registration

Please register via [FLoC’26 registration page](https://www.floc26.org/registration)

<hr>

# Invited Talks

TBA

<!-- <div class="container" style="margin-top: 25px;margin-bottom: 40px;">
  <div class="row">
    {% for p in site.data.invitedtalks %}
    {% if forloop.index<=6 %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.invitedtalks %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>6 and forloop.index<=10%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
</div> -->
<hr>

# Schedule

TBA

<!-- | Time | Event | Speaker |
|------|-------|---------|
| 11:00 - 11:45 | [Machine Learning Guidance for an Automatic Theorem Prover](#machine-learning-guidance-for-an-automatic-theorem-prover) | Martin Suda |
| 11:45 - 12:30 | [Automated Streamliner Selection via Algorithm Configuration and Selection](#automated-streamliner-selection-via-algorithm-configuration-and-selection) | Nguyen Dang |
| 12:30 - 13:30 | Lunch Break | |
| 13:30 - 14:15 | [Machine Learning for Quantifiers](#machine-learning-for-quantifiers) | Mikoláš Janota |
| 14:15 - 15:00 | [Applying Machine Learning to Improve SAT Solvers: Some Highlights](#applying-machine-learning-to-improve-sat-solvers-some-highlights) | Sean Holden |
| 15:00 - 15:30 | Coffee Break | |
| 15:30 - 16:15 | [ML-guided search for Mixed Integer Linear Programming](#ml-guided-search-for-mixed-integer-linear-programming) | Bistra Dilkina |
| 16:15 - 17:00 | **Panel:** Future of Machine Learning for Solvers/Provers | **Panelists:** Nguyen Dang, Sean Holden, Mikoláš Janota, Martin Suda, Stefan Szeider<br>**Moderator:** Vijay Ganesh | -->

<hr>

# Organizers
<div class="container" style="margin-top: 25px;margin-bottom: 40px;">
  <div class="row">
    {% for p in site.data['2026'].organizers %}
    {% if forloop.index<=5 %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data['2026'].organizers %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>5 and forloop.index<=10%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
</div>
<hr>


<!-- 
# Panelists
<div class="container" style="margin-top: 20px;margin-bottom: 0px;">
  <div class="row">
    {% for p in site.data.panelists %}
    {% if forloop.index<=5 %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.panelists %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>5 and forloop.index<=10%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.panelists %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>10%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
</div>
<hr>


# Materials and Open-Source Tools

* **[Video Recording](https://neurips.cc/virtual/2023/tutorial/73946)**
* [Slides](./img/NeurIPS2023-Tutorial-ML4TP.pdf)
* [Demo: Using LLMs in Lean](https://github.com/yangky11/lean4-example/tree/ml4tp-tutorial)
* [Demo: Training LLMs for Tactic Generation and Combining with Proof Search](https://github.com/yangky11/ml4tp-tutorial/blob/main/main.ipynb)
* [A Survey on Deep Learning for Theorem Proving](https://arxiv.org/abs/2404.09939)

## Lean 

* [LeanDojo](https://github.com/lean-dojo/LeanDojo): Extracting data and interacting with Lean
* [ReProver](https://github.com/lean-dojo/ReProver): Training and evaluating language models for theorem proving
* [LLMStep](https://github.com/wellecks/llmstep): Using language models to suggest proof steps
* [Lean Copilot](https://github.com/lean-dojo/LeanCopilot): Using language models to suggest proof steps, search for proofs, and select premises

## Isabelle

* [PISA](https://github.com/albertqjiang/Portal-to-ISAbelle): Extracting data and interacting with Isabelle
* [Draft, Sketch, and Prove](https://github.com/albertqjiang/draft_sketch_prove): Implementation of "Draft, Sketch, and Prove: Guiding Formal Theorem Provers with Informal Proofs"


## Coq

* [CoqGym](https://github.com/princeton-vl/CoqGym): Extracting data and interacting with Coq
* [Tactician](https://coq-tactician.github.io/): KNNs and random forests + online learning for synthesizing proofs
* [Proverbot9001](https://github.com/UCSD-PL/proverbot9001): RNNs for synthesizing proofs
* [coq-synthesis](https://github.com/agrarpan/coq-synthesis): Coq plugin for using Proverbot9001 in the proof assistant
* [CoqPyt](https://github.com/sr-lab/coqpyt): Interacting with Coq

## Others

* [HOList](https://sites.google.com/view/holist/home): Extracting data and interacting with HOL Light
* [INT](https://github.com/albertqjiang/INT): Synthetic theorem proving benchmark on inequalities


# Citation

<p>If you find this tutorial useful, please cite:</p>
<div class="container" style="margin-top: 20px;margin-bottom: 0px;">
{% raw %}
<pre><code>@misc{ml4tptutorial2023,
  author = {First, Emily and Jiang, Albert and Yang, Kaiyu},
  title = {{NeurIPS} Tutorial on Machine Learning for Theorem Proving},
  year = {2023},
  howpublished = {\url{https://machine-learning-for-theorem-proving.github.io}},
}</code></pre>
{% endraw %}
</div>
<hr>

Contact: <machine.learning.4.theorem.proving@gmail.com>. -->
