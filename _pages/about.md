---
permalink: /
title: "Description"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Welcome! I am an Assistant Professor of Biomedical Informatics at the University of Pittsburgh and a practicing child and adolescent psychiatrist in the Center for Autism and Developmental Disorders. My research develops computational methods for treatment discovery, with a natural emphasis on causal discovery and inference. We have created approaches that pinpoint root causes of disease, detect subtle treatment effects in randomized trials, and overcome latent confounding in observational studies. I gravitate toward problems that appear simple but reward deep thought, often yielding solutions that seem obvious only in hindsight. Ultimately, my goal is to produce foundational insights that translate into better patient outcomes.

My work currently falls into three primary themes listed below, alongside occasional projects that do not fit into the categories. For manuscripts under review, I typically provide a corresponding preprint.

Outcome Learning
======
_I develop data-adaptive methods for constructing composite outcomes that are explicitly aligned with the scientific or clinical task. Rather than treating outcomes as fixed, these approaches learn clinically interpretable outcome measures optimized for prediction, treatment differentiation, or causal analysis, with applications across psychiatry._

- Strobl, Eric V. ["Task-Aligned Outcome Learning in Psychiatry: Reducing Endpoint Dilution."](https://ericstrobl.github.io/files/Outcome_Learning_Perspective.pdf) Eric V. Strobl's Personal Webpage (2026): ericstrobl.github.io Accessed March 4 2026.

This Perspective articulates why outcome learning matters and provides practical guidance for using it responsibly, without sliding into endpoint shopping. I host it here because many preprint servers do not accept Perspective articles.
- Strobl, Eric V. "Oxytocin Enhances Social-Emotional Reciprocity in Autism." medRxiv (2025): 2025-07.
  
Using our SCORE algorithm, I detected subtle but consistent oxytocin effects on social-emotional reciprocity---an area where conventional total scores and subscores have repeatedly produced null or inconsistent findings.
- Strobl, Eric V. "Mendelianization: Concentrating Polygenic Signal into a Single Causal Locus." medRxiv (2025): 2025-10.
  
I used outcome learning to construct outcomes that concentrate polygenic association signal onto a single locus, improving interpretability and downstream causal localization.
- Strobl, Eric V. "Learning Causally Predictable Outcomes from Psychiatric Longitudinal Data." Biocomputing 2026: Proceedings of the Pacific Symposium. 2025.
  
I showed that the transient nature of certain treatments can enable robust causal inference from longitudinal psychiatric data, even when latent confounding is present.
- Strobl, Eric. "Predicting the Predictable in the Psychiatric High Risk." Machine Learning for Healthcare Conference. PMLR, 2025.

Instead of prespecifying outcomes, I developed SCORE to learn outcomes that are both clinically interpretable and genuinely predictable over time, revealing actionable structure in high-risk cohorts that standard outcome definitions often obscure.
- Strobl, Eric V. "Consistent differential effects of bupropion and mirtazapine in major depression." Journal of Affective Disorders 388 (2025): 119551.

Using our Supervised Varimax algorithm, I identified consistent and clinically meaningful differential effects between bupropion and mirtazapine---addressing a long-standing gap where randomized trials have struggled to separate these medications despite clear differences in clinical practice.
- Strobl, Eric V. "Unique Behavior Profiles that Specify Mental Distress in Autism." medRxiv (2025): 2025-02.

I linked caregiver-observed behavior patterns to specific forms of mental distress, enabling more precise clinical interpretation for patients who cannot reliably communicate internal states and revealing autism-specific internalizing and externalizing profiles. I further organized these interpretations into clinician-familiar diagnostic categories to facilitate translation to routine practice.
- Strobl, Eric V., and Semmie Kim. "Learning outcomes that maximally differentiate psychiatric treatments." medRxiv (2024): 2024-12. 

We introduced Supervised Varimax to learn outcome measures that amplify clinically meaningful treatment differences, supporting precision psychiatry in settings where standard endpoints show minimal or no differential effects.

Root Causal Analysis
======
_I formalize ``root causes'' in biomedical systems and develop methods to detect them directly from data. Conceptually, these methods aim to identify the initiating drivers of disease processes across genetic, transcriptomic, and neuroimaging modalities._

- Strobl, Eric V. "Extracting Root-Causal Brain Activity Driving Psychopathology from Resting State fMRI." arXiv preprint arXiv:2602.07233 (2026).

I extended root causal analysis to resting-state fMRI, proposing a framework for isolating brain activity patterns that initiate psychopathology-related processes rather than reflecting downstream consequences.
- Strobl, Eric V., and Eric Gamazon. "Discovering root causal genes with high-throughput perturbations." Elife 13 (2025): RP100949.

We introduced the first method to identify root causal genes -- the initial expression changes driving disease -- by learning causal gene order from Perturb-seq data and transferring it to bulk RNA-seq, enabling precise patient-specific discovery of disease origins.
- Strobl, Eric V., and Eric R. Gamazon. "Transcriptome-wide root causal inference." PLOS Computational Biology 21.9 (2025): e1013461.

We developed a transcriptome-wide approach that uses genetic variation as instrumental variables to infer root causal genes without requiring Perturb-seq data.
- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes with the heteroscedastic noise model." Journal of Computational Science 72 (2023): 102099.

We developd GRCI for identifying patient-specific root causes under heteroscedastic noise and derived identifiability conditions showing when this causal model is uniquely recoverable.
- Strobl, Eric V., Thomas A. Lasko, and Eric R. Gamazon. "Mitigating pathogenesis for target discovery and disease subtyping." Computers in biology and medicine 171 (2024): 108122.

We connected root causal analysis to pathogenesis and introduced an estimator for how root causal effects change under intervention versus no intervention, supporting both target discovery and disease subtyping.
- Strobl, Eric V. "Counterfactual formulation of patient-specific root causes of disease." Journal of Biomedical Informatics 150 (2024): 104585.

I formalized patient-specific root causes at the counterfactual level, aligning clinical notions of a root cause with a precise causal definition at the top rung of Pearl's ladder.
- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes of disease." Proceedings of the 13th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics. 2022.

We defined patient-specific root causes and presented the first efficient discovery method in this setting, leveraging LiNGAM to enable practical estimation.
- Strobl, Eric, and Thomas A. Lasko. "Sample-specific root causal inference with latent variables." Conference on Causal Learning and Reasoning. PMLR, 2023.

We generalized the above LiNGAM-based approach to accommodate latent variables, expanding applicability to more realistic biomedical settings where unmeasured factors are unavoidable.

Causal Discovery
======
_I develop causal discovery methods for learning causal graphs from observational data under progressively weaker and more realistic assumptions, including missingness, selection effects, latent variables, cycles, and distributional heterogeneity._

- Strobl, Eric V., Kun Zhang, and Shyam Visweswaran. "Approximate kernel-based conditional independence tests for fast non-parametric causal discovery." Journal of Causal Inference 7.1 (2019): 20180017.

We designed computationally efficient kernel-based conditional independence tests that make nonparametric causal discovery feasible at larger scales.
- Strobl, Eric V., Shyam Visweswaran, and Peter L. Spirtes. "Fast causal inference with non-random missingness by test-wise deletion." International journal of data science and analytics 6.1 (2018): 47-62.

We improved sample efficiency by deleting only the observations required for each conditional independence test, treating missingness as an additional layer of selection bias.
- Strobl, Eric V. "A constraint-based algorithm for causal discovery with cycles, latent variables and selection bias." International Journal of Data Science and Analytics 8.1 (2019): 33-56.

I introduced a constraint-based algorithm that jointly handles cycles, latent variables, and selection bias.
- Strobl, Eric V. "Causal discovery with a mixture of DAGs." Machine Learning 112.11 (2023): 4201-4225.

I extended causal discovery to settings generated by mixtures of DAGs and reinterpreted cycles as regime switching rather than equilibrium SEM structure.
- Strobl, Eric V. "Automated hyperparameter selection for the PC algorithm." Pattern Recognition Letters 151 (2021): 288-293.

I proposed a stability-based modification to PC that selects the significance threshold automatically, reducing sensitivity to arbitrary hyperparameter choices and improving robustness in practice.
- Strobl, Eric V., Peter L. Spirtes, and Shyam Visweswaran. "Estimating and controlling the false discovery rate of the pc algorithm using edge-specific p-values." ACM Transactions on Intelligent Systems and Technology (TIST) 10.5 (2019): 1-37.

We derived edge-specific p-value bounds for PC and use them to control false discoveries, enabling more principled uncertainty quantification in learned causal graphs.

