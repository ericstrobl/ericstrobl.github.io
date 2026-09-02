---
permalink: /
title: "Description"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Welcome! I am an Assistant Professor of Biomedical Informatics at the University of Pittsburgh and a practicing child and adolescent psychiatrist in the Center for Autism and Developmental Disorders. My research develops computational methods for treatment discovery, with a natural emphasis on causal discovery and inference. We have developed approaches for identifying root causes of disease, detecting subtle treatment effects in randomized trials, and addressing latent confounding in observational studies. I tend to gravitate toward problems that appear simple at first but reveal deeper structure when examined closely. Ultimately, my goal is to develop methods that improve how we understand disease and, hopefully, translate into better patient outcomes.

My work currently falls into three primary themes, along with occasional projects that sit outside these categories. Some manuscripts naturally span more than one area, but I list each under a single theme for simplicity. I have also included short first-person accounts of the journeys behind many of these papers. Research articles usually explain a project in terms of the surrounding literature, but that is often different from the real reason the problem was pursued. These descriptions are meant to capture some of the first-person curiosity, uncertainty, and clinical or scientific observations that led to each project. 

For manuscripts under review, I typically provide a corresponding preprint. Finally, I only update this website periodically, so please check my [Google Scholar profile](https://scholar.google.com/citations?hl=en&user=aimJiz4AAAAJ&view_op=list_works&sortby=pubdate) for recent updates.


[Outcome Learning](#outcome-learning) ·
[Root Cause Analysis](#root-cause-analysis) ·
[Causal Discovery & Inference](#causal-discovery-and-inference) ·
[Other Work](#others)

## Outcome Learning

_I develop data-adaptive methods for constructing composite outcomes that are explicitly aligned with the scientific or clinical task. Rather than treating outcomes as fixed, these approaches learn clinically interpretable outcome measures optimized for prediction, treatment differentiation, or causal analysis, with applications across psychiatry._

- Strobl, Eric V. (2026) Task-aligned outcome learning in psychiatry: reducing endpoint dilution. Front. Psychiatry 17:1832978. doi: 10.3389/fpsyt.2026.1832978.

I wrote this Perspective to provide a general introduction to outcome learning in psychiatry and to address recurring questions about motivation, endpoint selection, and statistical validity. The paper summarizes the rationale for the framework together with practical safeguards for its application.

- Strobl, Eric V., and Semmie Kim. 2026. “Learning Outcomes That Maximally Differentiate Psychiatric Treatments,” International Journal of Methods in Psychiatric Research: e70074.

This work was motivated by a difference between how psychiatric medications are often compared in the literature and how their effects are considered clinically. Studies frequently compare treatments using total symptom scores, whereas clinicians may distinguish medications according to the particular symptoms they affect. Supervised Varimax formalizes this latter perspective by identifying patterns of treatment effects across symptoms rather than relying on a single prespecified total score.

- Strobl, Eric V. "Consistent differential effects of bupropion and mirtazapine in major depression." Journal of Affective Disorders 388 (2025): 119551.

I used this study to evaluate whether Supervised Varimax recovered established differences in the clinical effect profiles of antidepressants. I examined three contrasts: bupropion versus other antidepressants, mirtazapine versus other antidepressants, and bupropion versus mirtazapine. The algorithm recovered recognizable treatment-specific patterns, providing evidence that the formalism captures clinically relevant differences among medications.

- Strobl, Eric V. "Unique Behavior Profiles that Specify Mental Distress in Autism." Journal of Autism and Developmental Disorders (in press)

This project was motivated by clinical observations that children with autism who are nonverbal or have difficulty communicating their internal states may show changes in observable behavior during periods of mental distress. I investigated whether specific behavioral patterns could distinguish different forms of distress rather than serving only as nonspecific indicators. Caregiver-observed behaviors differentiated several forms of mental distress and identified autism-specific internalizing and externalizing profiles. I subsequently related these patterns to clinician-familiar diagnostic categories, providing a framework that can also inform clinical interpretation.

- Strobl, Eric. "Predicting the Predictable in the Psychiatric High Risk." Machine Learning for Healthcare Conference. PMLR, 2025.

I developed SCORE in response to a recurring problem in psychosis-risk prediction: increasingly rich datasets do not necessarily make a prespecified clinical outcome highly predictable. More generally, some aspects of future health may be substantially more predictable than others. This motivated an alternative to fixing the prediction target in advance. SCORE instead learns clinically interpretable outcomes whose future values can be predicted from the available data.

- Strobl, Eric V. "Learning Causally Predictable Outcomes from Psychiatric Longitudinal Data." Biocomputing 2026: Proceedings of the Pacific Symposium. 2025.

This work considers whether longitudinal medical data contain structure that can support causal inference under latent confounding. Past treatment history can provide such information when treatment effects are transient and therefore do not directly determine the later outcomes under consideration. By allowing the outcome itself to be learned rather than fixed in advance, this historical information can be used to identify outcomes whose treatment effects remain causally identifiable in the presence of latent confounding.

- Strobl, Eric V. “Oxytocin Enhances Social-Emotional Reciprocity in Autism.” medRxiv (2025): 2025-07.

I had previously worked on oxytocin and later revisited the question using outcome learning. Although the large SOARS-B trial did not find benefit on its prespecified primary outcomes, I considered whether those endpoints might have been insensitive to a more specific multidimensional treatment effect. I therefore used SCORE to learn a treatment-sensitive outcome from the randomized data, with bootstrap and permutation procedures for Type I error control. The resulting analysis identified an effect that was not apparent using the original endpoints. More generally, subtle multidimensional treatment effects may be difficult to capture with prespecified summary measures, particularly when they do not follow conventional factor structure. Outcome learning provides a data-adaptive approach for identifying such treatment-responsive dimensions while retaining formal inferential safeguards.

- Strobl, Eric V. "Mendelianization: Concentrating polygenic signal into a single causal locus." Genetic Epidemiology 50.6 (2026): e70053.

I used outcome learning to construct phenotypes that concentrate polygenic association signal onto individual genetic loci, improving interpretability and causal localization. This work combines outcome learning with the problem of identifying genetic root causes of disease. A central goal was to formulate causal localization assumptions directly in terms of genetic architecture while avoiding more abstract assumptions such as consistency, exclusion restriction, or an underlying DAG whenever possible.

## Root Cause Analysis

_This line of work asks whether the causes of disease can be defined and identified at the level of an individual patient. From a treatment perspective, understanding the processes that initiate disease in a particular patient may support more causally targeted interventions. I therefore developed a framework for defining and identifying patient-specific root causes._

- Strobl, Eric V. "Extracting Root-Causal Brain Activity Driving Psychopathology from Resting State fMRI." arXiv preprint arXiv:2602.07233 (2026).

I extended root causal analysis to resting-state fMRI, proposing a framework for isolating brain activity patterns that initiate psychopathology-related processes rather than reflecting downstream consequences.

- Strobl, Eric V., and Eric Gamazon. "Discovering root causal genes with high-throughput perturbations." Elife 13 (2025): RP100949.

We introduced a method for identifying root causal genes—the initial expression changes driving disease—by learning causal gene order from Perturb-seq data and transferring it to bulk RNA-seq for patient-specific analysis.

- Strobl, Eric V., and Eric R. Gamazon. "Transcriptome-wide root causal inference." PLOS Computational Biology 21.9 (2025): e1013461.

We developed a transcriptome-wide approach that uses genetic variation as instrumental variables to infer root causal genes without requiring Perturb-seq data.

- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes with the heteroscedastic noise model." Journal of Computational Science 72 (2023): 102099.

We developed GRCI for identifying patient-specific root causes under heteroscedastic noise and derived identifiability conditions establishing when the corresponding causal model is uniquely recoverable.

- Strobl, Eric V., Thomas A. Lasko, and Eric R. Gamazon. "Mitigating pathogenesis for target discovery and disease subtyping." Computers in Biology and Medicine 171 (2024): 108122.

We connected root causal analysis to pathogenesis and introduced an estimator for how root causal effects change under intervention versus no intervention, supporting both target discovery and disease subtyping.

- Strobl, Eric V. "Counterfactual formulation of patient-specific root causes of disease." Journal of Biomedical Informatics 150 (2024): 104585.

I formalized patient-specific root causes at the counterfactual level, relating the clinical concept of a root cause to a precise causal definition at the counterfactual level of Pearl's causal hierarchy.

- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes of disease." Proceedings of the 13th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics. 2022.

We defined patient-specific root causes and presented an efficient discovery method based on LiNGAM.

- Strobl, Eric, and Thomas A. Lasko. "Sample-specific root causal inference with latent variables." Conference on Causal Learning and Reasoning. PMLR, 2023.

We generalized the LiNGAM-based approach to accommodate latent variables, extending its applicability to biomedical settings with unmeasured factors.

## Causal Discovery and Inference

_I develop methods for causal discovery and causal inference from observational data, particularly focusing on complications such as missingness, selection effects, latent variables, cycles, measurement error, and distributional heterogeneity._

- Strobl, Eric V. "COMPACT: Spectral Adjustment Scores from a Complete and Irreducible Causal Criterion." arXiv:2608.10305 (2026).

This work reconsidered the usual characterization of the propensity score as the coarsest balancing score and asked whether adjustment could instead be derived more directly from causal requirements. COMPACT uses a minimal set of conditional and unconditional independence relations to constrain the causal graph structure relevant to adjustment. The resulting structural criterion reduces to a generalized eigenvalue decomposition, yielding a spectral algorithm for constructing low-dimensional adjustment scores.

- Strobl, Eric V. "Fast Nonparametric Conditional Independence Testing via Two-Stage Regression." arXiv:2606.18011 (2026).

I developed BLITZ, a sub-second nonparametric conditional independence test designed to maintain Type I error control under complex nonlinear structure. Flexible nonparametric tests often incur substantial computational costs because they require fitting complex nuisance models. BLITZ instead derives the nuisance-estimation requirements directly from the product-form test statistic and reduces their complexity at multiple stages. This allows relatively simple and computationally efficient models to satisfy the conditions required for valid inference.

- Strobl, Eric V., Kun Zhang, and Shyam Visweswaran. "Approximate kernel-based conditional independence tests for fast non-parametric causal discovery." Journal of Causal Inference 7.1 (2019): 20180017.

We designed computationally efficient kernel-based conditional independence tests that make nonparametric causal discovery feasible at larger scales.

- Strobl, Eric V., Shyam Visweswaran, and Peter L. Spirtes. "Fast causal inference with non-random missingness by test-wise deletion." International Journal of Data Science and Analytics 6.1 (2018): 47-62.

This project addressed causal discovery in datasets with substantial missingness, where complete-case analysis can discard otherwise usable observations. We represented missingness as a variable-specific form of selection and used the ability of FCI to accommodate selection bias. The resulting test-wise deletion procedure allows the relevant selection set to vary across conditional independence tests, preserving additional data while remaining sound under appropriate assumptions.

- Strobl, Eric V. "A constraint-based algorithm for causal discovery with cycles, latent variables and selection bias." International Journal of Data Science and Analytics 8.1 (2019): 33-56.

This work addressed causal discovery in the simultaneous presence of cycles, latent variables, and selection bias. I developed a constraint-based method that incorporates valid orientation rules for reasoning about these three complications within a common framework.

- Strobl, Eric V. "Causal discovery with a mixture of DAGs." Machine Learning 112.11 (2023): 4201-4225.

This project examined an alternative representation of cyclic causal systems. Structural equation models often represent cycles through equilibrium relationships, whereas many biological processes can also be viewed as sequential interactions occurring across different regimes or time points. I therefore studied mixtures of DAGs, in which an apparent cycle can arise from variation among multiple acyclic causal regimes. This representation substantially improved causal discovery performance in the settings considered, suggesting that mixtures of acyclic structures may provide a useful model for some systems that appear cyclic in aggregate.

- Strobl, Eric V. "Automated hyperparameter selection for the PC algorithm." Pattern Recognition Letters 151 (2021): 288-293.

I proposed a stability-based modification to PC that selects the significance threshold automatically, reducing sensitivity to arbitrary hyperparameter choices and improving robustness in practice.

- Strobl, Eric V., Peter L. Spirtes, and Shyam Visweswaran. "Estimating and controlling the false discovery rate of the PC algorithm using edge-specific p-values." ACM Transactions on Intelligent Systems and Technology (TIST) 10.5 (2019): 1-37.

We derived edge-specific p-value bounds for PC and used them to control false discoveries, enabling more principled uncertainty quantification in learned causal graphs.

## Others

- Strobl, Eric V. "Global Interpretability via Automated Preprocessing: A Framework Inspired by Psychiatric Questionnaires." arXiv:2602.23459 (2026).

This work considers global model interpretability in settings where nonlinear predictive relationships are important. Instance-specific explanations such as SHAP values vary across patients and outcomes, whereas some clinical applications benefit from a single interpretable model. I therefore studied a decomposition in which nonlinear structure is captured through an interpretable preprocessing step followed by a linear predictive model. The preprocessing is constrained to preserve the meaning of the original variables while extracting nonlinear structure relevant to prediction.
