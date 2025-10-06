---
layout: page
title: Machine Learning for Solvers and Provers (ML4SP)
---
<!-- <div class="venue" style="font-size: 27px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <a target="_blank" href="https://neurips.cc/virtual/2023/tutorial/73946"><strong>Video Recording</strong></a>
</div> -->

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>JMS 630 (please watch for possible last-minute room changes onsite)</strong>
</div>

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>James McCune Smith Learning Hub, <a target="_blank" href="https://www.gla.ac.uk/">University of Glasgow</a>, Glasgow, Scotland</strong>
</div>

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>Sunday, 10 August, 2025</strong>
</div>

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>11 AM to 5 PM</strong>
</div>

<div class="venue" style="font-size: 24px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <strong>Invited Talks Workshop</strong>
</div>

<!-- <div class="venue" style="font-size: 20px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <a target="_blank" href="https://aaai.org/conference/aaai/aaai-25/tutorial-and-lab-list/#TH24">(AAAI 2025 website)</a>
</div> -->

<!-- <div class="sharethis-inline-share-buttons"></div> -->
<!-- <meta name="thumbnail" content="https://ml-for-solvers.github.io/img/aaai-small.jpeg" /> -->

<nav>
  <a href="#co-chairs">Co-chairs</a> |
  <a href="#invited-talks">Invited Talks</a> |
  <a href="#overview">Overview</a> |
  <a href="#schedule">Schedule</a> |
  <a href="#talk-details">Talk Details</a> |
  <a href="#scope">Scope</a> |
  <a href="#organizers">Organizers</a> |
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

# Invited Talks
<div class="container" style="margin-top: 25px;margin-bottom: 40px;">
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
</div>
<hr>

# Overview

Learning and reasoning have been the two foundational pillars of AI since its inception, yet it is only in the past decade that interactions between these fields have become increasingly prominent.
In particular, machine learning (ML) has had a substantial impact on SAT/SMT and CP solvers, as well as automated theorem provers. Recent advances have demonstrated the power of ML to inform solver heuristics, guide proof search, and optimize algorithm portfolios. 

Despite growing interest in this direction, work on ML for solvers and provers is often scattered across multiple research communities — SAT, SMT, CP, theorem proving, formal methods, and machine learning - with few opportunities for focused interaction. This workshop aims to bring together researchers and practitioners working at the intersection of machine learning and formal reasoning systems. It provides a forum for the presentation of recent work, the exchange of ideas, and the fostering of collaboration between these communities.

<hr>

# Schedule

| Time | Event | Speaker |
|------|-------|---------|
| 11:00 - 11:45 | [Machine Learning Guidance for an Automatic Theorem Prover](#machine-learning-guidance-for-an-automatic-theorem-prover) | Martin Suda |
| 11:45 - 12:30 | [Automated Streamliner Selection via Algorithm Configuration and Selection](#automated-streamliner-selection-via-algorithm-configuration-and-selection) | Nguyen Dang |
| 12:30 - 13:30 | Lunch Break | |
| 13:30 - 14:15 | [Machine Learning for Quantifiers](#machine-learning-for-quantifiers) | Mikoláš Janota |
| 14:15 - 15:00 | [Applying Machine Learning to Improve SAT Solvers: Some Highlights](#applying-machine-learning-to-improve-sat-solvers-some-highlights) | Sean Holden |
| 15:00 - 15:30 | Coffee Break | |
| 15:30 - 16:15 | [ML-guided search for Mixed Integer Linear Programming](#ml-guided-search-for-mixed-integer-linear-programming) | Bistra Dilkina |
| 16:15 - 17:00 | **Panel:** Future of Machine Learning for Solvers/Provers | **Panelists:** Nguyen Dang, Sean Holden, Mikoláš Janota, Martin Suda, Stefan Szeider<br>**Moderator:** Vijay Ganesh |

<hr>

# Talk Details

## Machine Learning Guidance for an Automatic Theorem Prover
*Speaker: [Martin Suda](https://people.ciirc.cvut.cz/~sudamar2/)* | [**Slides**](slides/Suda.pdf)

In automatic theorem provers (ATPs) based on saturation---the predominant paradigm---the most promising applications of machine learning (ML) target the so-called clause selection heuristic, which helps decide which lemma to consider next for inference. The most promising systems in this category invariably learn from past successes: the lemmas that ultimately appeared in discovered proofs. In this talk, I will outline how such systems work, including those based on supervised learning and those inspired by reinforcement learning. I will also share general insights from my experience developing a neurally guided clause selection heuristic in the ATP Vampire.

**Speaker Bio:**  
Martin Suda is a senior researcher at the CIIRC institute of the Czech Technical University in Prague and the head of the Automated Reasoning Group there. His primary research interest is automated theorem proving and how it can be boosted through the techniques of machine learning. He is one of the main developers of the award-winning automatic theorem prover Vampire.

## Automated Streamliner Selection via Algorithm Configuration and Selection
*Speaker: [Nguyen Dang](https://ndangtt.github.io/)* | [**Slides**](slides/Dang.pdf)

Many algorithms have parameters that can significantly impact their performance. Automated algorithm configuration is a family of general-purpose techniques aimed at finding the best parameter setting of an algorithm on a given problem. Automated algorithm selection, a closely related area, focuses on selecting the best algorithm among a given set of algorithms for a specific instance of a problem. Owing to their general-purpose nature, these techniques are broadly applicable across a wide range of domains. In this talk, I will present our work on combining algorithm configuration and algorithm selection to automate the generation and selection of streamliner constraints. Streamliners are heuristic constraints added to a constraint model to reduce the search space, resulting in solving speedup. However, since streamliners do not preserve correctness, they must be selected carefully to avoid pruning valid solutions. Our empirical results indicate the effectiveness of our approach where substantial solving speed up is achieved in various cases.

**Speaker Bio:**  
Nguyen Dang is a Lecturer (Assistant Professor) at the University of St Andrews. She received a PhD degree from KU Leuven in 2018 and was awarded a Leverhulme Early Career fellowship in 2020. Her research interests include automated algorithm configuration, automated algorithm selection, as well as their applications in both constraint programming and black-box optimisation. Her work in automated algorithm configuration has received best paper awards at GECCO'2017 and GECCO'2022, and nominations for best paper award at FOGA'2023 and GECCO'2025.

## Machine Learning for Quantifiers
*Speaker: [Mikoláš Janota](https://people.ciirc.cvut.cz/~janotmik/)* | [**Slides**](slides/Janota.pdf)

Reasoning with quantifiers is inherently difficult. Adding quantifiers to a language typically significantly increases its computational complexity or leads to undecidability. Yet, quantifiers enable us to express properties over large or infinite domains. In this talk we will look at ML techniques that attempt to help automated reasoning with quantifiers. We will focus mainly on Quantified Boolean Formulas and Satisfiability Modulo Theories, where quantifiers are tackled by instantiation-based techniques.

**Speaker Bio:**  
Mikoláš Janota is a researcher at the Czech Institute of Informatics, Robotics and Cybernetics (CIIRC) at the Czech Technical University in Prague, where he leads the Formal Methods group. His work focuses on automated reasoning, formal verification, and logic-based problem solving, including SAT, MaxSAT, QBF, and SMT. He has contributed to tools like Z3 and developed award-winning solvers such as RAReQS and QESTO. With a background spanning Charles University, University College Dublin, and postdoctoral roles in Portugal and the UK, he currently explores the integration of machine learning with logic solvers under an ERC CZ grant.

## Applying Machine Learning to Improve SAT Solvers: Some Highlights
*Speaker: [Sean Holden](https://www.cl.cam.ac.uk/~sbh11/)* | [**Slides**](slides/Holden.pdf)

Modern state-of-the-art SAT-solvers rely on numerous sophisticated data-structures and algorithms to achieve their performance. Several of the algorithms involved can be considered machine learning algorithms, and in recent years a great deal of effort has been focused on using machine learning directly to improve the performance of SAT solvers. This talk will present a selection of highlights from research in this area.

**Speaker Bio:**  
Sean Holden is University Associate Professor of Computer Science at the University of Cambridge, and Director of Studies in Computing at Trinity College, Cambridge. He has published in various areas of theoretical and applied machine learning, including computational learning theory, Bayesian inference and applications in drug design, sports science, wearable computing and organelle proteomics. He currently works on machine learning for automated theorem proving, and is responsible for the Connect++ connection prover.

## ML-guided search for Mixed Integer Linear Programming
*Speaker: [Bistra Dilkina](https://viterbi.usc.edu/directory/faculty/Dilkina/Bistra)* | [**Slides**](slides/Dilkina.pdf)

Many real-world applications that require combinatorial optimization involve solving repeatedly similar instances of the same problem over different data (objective and constraint coefficients). Hence, they provide the opportunity to learn to search more effectively by leveraging historical instances. We design approaches to effectively augment established state-of-the-art Mixed Integer Linear programming (MILP) solvers with ML-guided components to significantly improve performance. In particular, many important (heuristic) tasks in MILP solving involve choosing subsets of variables, and we demonstrate that Contrastive Loss is particularly well-suited for training in this setting by learning from both positive and negative examples of candidate sets. We will further discuss the potential of learning across multiple domains when historical examples are limited, and the impressive power of multi-task learning across different ML-guided solving techniques for any given problem domain, setting a key stepping stone to a foundation model for ML-guided MILP solving.

**Speaker Bio:** 
Dr. Bistra Dilkina is an associate professor of computer science at the University of Southern California (USC), co-director of the USC Center of AI in Society, and leads the USC Site for the NSF AI Institute for Advances in Optimization (AI4OPT). Her research and teaching are centered around the integration of machine learning and discrete optimization, with a strong focus on AI applications in computational sustainability and social impact, such as wildlife conservation and disaster resilience. Her research has contributed significant advances to machine-learning-guided combinatorial solving, including mathematical programming and AI planning, as well as to decision-focused learning, where combinatorial reasoning is integrated into machine-learning pipelines. 


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
