---
layout: page
title: Machine Learning for Solvers and Provers (ML4SP)
---
<!-- <div class="venue" style="font-size: 27px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <a target="_blank" href="https://neurips.cc/virtual/2023/tutorial/73946"><strong>Video Recording</strong></a>
</div> -->

<!-- <div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>Room 118A, <a target="_blank" href="https://g.co/kgs/jLhwXps">Pennsylvania Convention Center</a>, Philadelphia</strong>
</div>

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>26 February 2025, 2–6 PM ET</strong>
</div>

<div class="venue" style="font-size: 20px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <a target="_blank" href="https://aaai.org/conference/aaai/aaai-25/tutorial-and-lab-list/#TH24">(AAAI 2025 website)</a>
</div> -->

<!-- <div class="sharethis-inline-share-buttons"></div> -->
<!-- <meta name="thumbnail" content="https://ml-for-solvers.github.io/img/aaai-small.jpeg" /> -->

<nav>
  <a href="#co-chairs">Panelists</a> |
  <a href="#overview">Overview</a> |
  <a href="#scope">Schedule</a> |
  <a href="#organizers">Presenters</a> |
</nav>

<hr>

# Co-chairs
<div class="container" style="margin-top: 25px;margin-bottom: 40px;">
  <div class="row">
    {% for p in site.data.cochairs %}
    {% if forloop.index<=6 %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.cochairs %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>6 and forloop.index<=10%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
</div>
<hr>

# Overview

Learning and reasoning have been the two foundational pillars of AI since its inception, yet it is only in the past decade that interactions between these fields have become increasingly prominent.
In particular, machine learning (ML) has had a substantial impact on SAT/SMT and CP solvers, as well as automated theorem provers. Recent advances have demonstrated the power of ML to inform solver heuristics, guide proof search, and optimize algorithm portfolios. 

Despite growing interest in this direction, work on ML for solvers and provers is often scattered across multiple research communities — SAT, SMT, CP, theorem proving, formal methods, and machine learning - with few opportunities for focused interaction. This workshop aims to bring together researchers and practitioners working at the intersection of machine learning and formal reasoning systems. It provides a forum for the presentation of recent work, the exchange of ideas, and the fostering of collaboration between these communities.

<hr>

# Scope

Topics of interest include, but are not limited to, the use of various machine learning (ML) techniques in:

- Heuristics (branching, restarts,...) for SAT, SMT, and CP solvers
- Tactic selection and proof guidance in automated and interactive theorem provers
- Algorithm selection, algorithm configuration, and portfolio solvers
- End-to-end learning for solvers and provers
- Benchmark generation and instance hardness prediction
- Applications of ML-enhanced reasoning in verification, synthesis, planning, and related areas

<hr>

# Organizers
<div class="container" style="margin-top: 25px;margin-bottom: 40px;">
  <div class="row">
    {% for p in site.data.organizers %}
    {% if forloop.index<=5 %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.organizers %}
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
