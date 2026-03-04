---
permalink: /
title: "Description"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Welcome! I am an Assistant Professor of Biomedical Informatics at the University of Pittsburgh and a practicing child and adolescent psychiatrist in the Center for Autism and Developmental Disorders. My research develops computational methods for treatment discovery, with a natural emphasis on causal discovery and inference. We have created approaches that pinpoint root causes of disease, detect subtle treatment effects in randomized trials, and overcome latent confounding in observational studies. I gravitate toward problems that appear simple but reward deep thought, often yielding solutions that seem obvious only in hindsight. Ultimately, my goal is to produce foundational insights that translate into better patient outcomes.

Currently, my research can be divided into 3 categories:

Outcome Learning
======
The goal is to learn the appropriate composite outcome measure in a data-adaptive fashion. The composite outcome should be task-aligned and optimized for the task at hand using data. We devise new algorithms and apply them to a variety of problems in psychiatry.

- Strobl, Eric V. "Oxytocin Enhances Social-Emotional Reciprocity in Autism." medRxiv (2025): 2025-07.
I uncovered subtle effects of oxytocin on social-emotional reciprocity using our SCORE algorithm -- addressing a long-standing challenge in the field, where conventional total scores and subscores have repeatedly failed to detect consistent benefits.
- Strobl, Eric V. "Mendelianization: Concentrating Polygenic Signal into a Single Causal Locus." medRxiv (2025): 2025-10.
I used outcome learning to learn outcomes that concentrate genetic assocation at a single locus.
- Strobl, Eric V. "Learning Causally Predictable Outcomes from Psychiatric Longitudinal Data." Biocomputing 2026: Proceedings of the Pacific Symposium. 2025.
I demonstrate that the transient nature of certain treatments enables robust causal inference, even in the presence of latent confounders.
- Strobl, Eric. "Predicting the Predictable in the Psychiatric High Risk." Machine Learning for Healthcare Conference. PMLR, 2025.
Outcomes are often predefined and treated as fixed, limiting discovery. Our SCORE algorithm instead lets data reveal clinically interpretable outcomes that are genuinely predictable over time, uncovering novel and actionable patterns in high-risk populations that conventional approaches overlook.
- (Discovery) **Bupropion and mirtazapine show consistent differential effects among antidepressants** [[paper](https://www.sciencedirect.com/science/article/pii/S0165032725009930)]: We identified consistent, clinically meaningful differential effects of bupropion and mirtazapine using our Supervised Varimax algorithm, addressing a long-standing problem in psychiatry where randomized controlled trials have failed to distinguish these medications despite clear clinical differences.
- (Discovery) **Distinct aberrant behavior profiles reveal hidden mental distress in autism** [[paper](https://www.medrxiv.org/content/10.1101/2025.02.01.25321517v2)]: Caregivers of patients with autism often observe non-specific behaviors, but many patients cannot communicate their distress, leaving clinicians to guess at the causes. We developed a method that links behavior patterns to specific types of mental distress, enabling clinicians to understand even non-verbal patients. This reveals actionable clinical patterns unique to autism and clarifies subtle internalizing and externalizing symptoms.
- (Invention) **Learning outcomes that maximally differentiate psychiatric treatments** [[paper](https://www.medrxiv.org/content/10.1101/2024.12.03.24318424v4)]: We developed the Supervised Varimax technique to identify outcome measures that reveal large, clinically meaningful differences between psychiatric treatments, enabling precision psychiatry in settings where standard analyses detect little to no differential effect.

Root Causal Analysis
======
Theory that formalizes what root causes are in the context of biomedicine, and methods that detect them automatically from data. We have applied this to genetic, transcriptomic, and neuroimaging data thus far.

- Strobl, Eric V. "Extracting Root-Causal Brain Activity Driving Psychopathology from Resting State fMRI." arXiv preprint arXiv:2602.07233 (2026).
We extended root causal analysis beyond clinic and -omic type data to resting state fMRI.
- Strobl, Eric V., and Eric Gamazon. "Discovering root causal genes with high-throughput perturbations." Elife 13 (2025): RP100949.
We introduced the first method to identify root causal genes -- the initial expression changes driving disease -- by learning causal gene order from Perturb-seq data and transferring it to bulk RNA-seq, enabling precise patient-specific discovery of disease origins.
- Strobl, Eric V., and Eric R. Gamazon. "Transcriptome-wide root causal inference." PLOS Computational Biology 21.9 (2025): e1013461.
We created a method that does not rely on Perturb-seq but instead uses genetic data as instrumental variables to discovery root causal genes.
- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes with the heteroscedastic noise model." Journal of Computational Science 72 (2023): 102099.
We developed an algorithm called GRCI that can discover the root causes of a target variable with heteroscedastic noise. We also derived the conditions when a heteroscedastic noise causal model is uniquely identifiable. 
- Strobl, Eric V., Thomas A. Lasko, and Eric R. Gamazon. "Mitigating pathogenesis for target discovery and disease subtyping." Computers in biology and medicine 171 (2024): 108122.
We connected root causal analysis to the medical study of pathogenesis, and introduced an algorithm that estimates the difference of root causal effects under intervention vs no intervention.
- Strobl, Eric V. "Counterfactual formulation of patient-specific root causes of disease." Journal of Biomedical Informatics 150 (2024): 104585.
I connected how physicians conceptualize root causes to a mathematical definition of patient-specific root causes of disease at the counterfactual level (highest level of Pearl's ladder).
- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes of disease." Proceedings of the 13th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics. 2022.
We defined root causes of disease and introduced the first efficient way of discovering them using the LiNGAM model.
- Strobl, Eric, and Thomas A. Lasko. "Sample-specific root causal inference with latent variables." Conference on Causal Learning and Reasoning. PMLR, 2023.
We generalized the above paper with LiNGAM to accodomate latent variables.

Causal Discovery
======
Methods that discovery causal graphs from data under progressively weaker and realistic assumptions.

- Strobl, Eric V., Kun Zhang, and Shyam Visweswaran. "Approximate kernel-based conditional independence tests for fast non-parametric causal discovery." Journal of Causal Inference 7.1 (2019): 20180017.
We developed very fast conditional independence tests to enable non-parametric causal discovery.
- Strobl, Eric V., Shyam Visweswaran, and Peter L. Spirtes. "Fast causal inference with non-random missingness by test-wise deletion." International journal of data science and analytics 6.1 (2018): 47-62.
We make causal discovery algorithms sample efficient with test-wise deletion (only deleting samples needed for each test) by conceptualizing missingness as a second layer of selection bias.
- Strobl, Eric V. "A constraint-based algorithm for causal discovery with cycles, latent variables and selection bias." International Journal of Data Science and Analytics 8.1 (2019): 33-56.
I developed a constraint-based algorithm that can handle cycles, latent variables and selection bias simultaneously.


