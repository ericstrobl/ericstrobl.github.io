---
permalink: /
title: "Description"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Welcome! I am an Assistant Professor of Biomedical Informatics at the University of Pittsburgh and a practicing child and adolescent psychiatrist in the Center for Autism and Developmental Disorders. My research develops computational methods for biomedical and clinical problems, with an emphasis on causal discovery and inference. A recurring feature of this work is to formulate methods around the scientific question and available evidence rather than assuming a fixed statistical representation in advance. This has led to methods for identifying patient-specific root causes of disease, learning outcomes for prediction and treatment-effect detection, and addressing latent confounding in observational studies. The overall goal is to improve causal and predictive analysis of disease in ways that can support better treatment decisions and patient outcomes.

My research currently falls into three primary themes, along with several projects outside these categories. Some manuscripts overlap across areas, but each is listed under a single theme for simplicity. Brief summaries are included for many papers to describe the scientific motivation, methodological contribution, and relationship to the broader research program. These summaries provide context that may not be apparent from the publication title or abstract alone.

For manuscripts under review, I typically provide a corresponding preprint. Finally, I only update this website periodically, so please check my [Google Scholar profile](https://scholar.google.com/citations?hl=en&user=aimJiz4AAAAJ&view_op=list_works&sortby=pubdate) for recent updates.


[Outcome Learning](#outcome-learning) ·
[Root Cause Analysis](#root-cause-analysis) ·
[Causal Discovery & Inference](#causal-discovery-and-inference) ·
[Other Work](#others)

## Outcome Learning

_This line of work develops data-adaptive methods for constructing composite outcomes that are explicitly aligned with the scientific or clinical task. Rather than treating outcomes as fixed, these approaches learn clinically interpretable outcome measures optimized for prediction, treatment differentiation, or causal analysis, with applications across psychiatry and other areas of medicine._

- Strobl, Eric V. (2026) Task-aligned outcome learning in psychiatry: reducing endpoint dilution. Front. Psychiatry 17:1832978. doi: 10.3389/fpsyt.2026.1832978.

This Perspective provides a general introduction to outcome learning in psychiatry and addresses questions about motivation, endpoint selection, and statistical validity. The paper summarizes the rationale for treating the outcome as a learnable object and describes practical safeguards for data-adaptive outcome construction.

- Strobl, Eric V., and Semmie Kim. 2026. “Learning Outcomes That Maximally Differentiate Psychiatric Treatments,” International Journal of Methods in Psychiatric Research: e70074.

This work addresses a difference between how psychiatric medications are often compared statistically and how their effects may be distinguished clinically. Studies frequently compare treatments using total symptom scores, whereas medications may differ in the particular symptoms they affect. Supervised Varimax learns composite outcomes that maximize treatment differentiation across symptoms rather than relying on a single prespecified total score.

- Strobl, Eric V. "Consistent differential effects of bupropion and mirtazapine in major depression." Journal of Affective Disorders 388 (2025): 119551.

This study evaluated whether Supervised Varimax could recover established differences in antidepressant effect profiles from individual randomized trials rather than meta-analyses. Three contrasts were examined: bupropion versus other antidepressants, mirtazapine versus other antidepressants, and bupropion versus mirtazapine. The algorithm recovered recognizable treatment-specific patterns, providing evidence that the learned outcome representation captures clinically relevant differences among medications.

- Strobl, Eric V. "Unique Behavior Profiles that Specify Mental Distress in Autism." Journal of Autism and Developmental Disorders (in press)

This project was motivated by clinical observations that children with autism who are nonverbal or have difficulty communicating their internal states may show changes in observable behavior during periods of mental distress. The study investigated whether specific behavioral patterns could distinguish different forms of distress rather than serving only as nonspecific indicators. Caregiver-observed behaviors differentiated several forms of mental distress and identified autism-specific internalizing and externalizing profiles. These patterns were subsequently related to clinician-familiar diagnostic categories, providing a framework that can also inform clinical interpretation.

- Strobl, Eric. "Predicting the Predictable in the Psychiatric High Risk." Machine Learning for Healthcare Conference. PMLR, 2025.

This work developed SCORE in response to a general problem in prediction: increasingly rich datasets do not necessarily make a prespecified clinical outcome highly predictable. Some aspects of future health may be substantially more predictable than others. SCORE therefore treats the prediction target itself as learnable and constructs clinically interpretable outcomes whose future values can be predicted from the available data.

- Strobl, Eric V. "Learning Causally Predictable Outcomes from Psychiatric Longitudinal Data." Biocomputing 2026: Proceedings of the Pacific Symposium. 2025.

This work considers whether longitudinal medical data contain structure that can support causal inference under latent confounding. Past treatment history can provide such information when treatment effects are transient and therefore do not directly determine the later outcomes under consideration. By treating the outcome as a learnable object rather than fixing it in advance, the method uses historical treatment information to identify outcomes whose treatment effects remain causally identifiable in the presence of latent confounding.

- Strobl, Eric V. “Oxytocin Enhances Social-Emotional Reciprocity in Autism.” medRxiv (2025): 2025-07.

This study applied outcome learning to the SOARS-B randomized trial to examine whether oxytocin effects might be detectable beyond the prespecified primary outcomes. SCORE was used to learn a treatment-sensitive outcome from the randomized data, with bootstrap and permutation procedures for Type I error control. The analysis identified an effect that was not apparent using the original endpoints. More generally, subtle treatment effects may be difficult to capture with prespecified summary measures, particularly when they do not follow conventional factor structure. Outcome learning provides a data-adaptive approach for identifying such treatment-responsive dimensions while retaining formal inferential safeguards.

- Strobl, Eric V. "Mendelianization: Concentrating polygenic signal into a single causal locus." Genetic Epidemiology 50.6 (2026): e70053.

This work used outcome learning to construct phenotypes that concentrate polygenic association signal onto individual genetic loci, improving interpretability and causal localization. Mendelianization grew in part out of earlier work on patient-specific root causes, but replaces the previous DAG-based formulation with assumptions stated directly in terms of genetic architecture and avoids reliance on functional genomic data. The resulting framework makes the phenotype itself learnable and bases causal localization on assumptions more directly connected to observed genetic association structure.

## Root Cause Analysis

_This line of work addresses whether the causes that initiate disease can be defined and identified at the level of an individual patient. From a treatment perspective, identifying patient-specific initiating causes could support more causally targeted interventions. The resulting framework defines and estimates patient-specific root causes rather than only population-level causal effects._

- Strobl, Eric V. "Extracting Root-Causal Brain Activity Driving Psychopathology from Resting State fMRI." arXiv preprint arXiv:2602.07233 (2026).

This study extends root causal analysis to resting-state fMRI. The framework aims to identify brain activity patterns that initiate psychopathology-related processes rather than activity that primarily reflects downstream consequences.

- Strobl, Eric V., and Eric Gamazon. "Discovering root causal genes with high-throughput perturbations." Elife 13 (2025): RP100949.

The study introduces a method for identifying root causal genes, defined as the initial expression changes that drive downstream disease-related molecular processes. Causal gene order is learned from Perturb-seq data and transferred to bulk RNA-seq for patient-specific root-cause analysis.

- Strobl, Eric V., and Eric R. Gamazon. "Transcriptome-wide root causal inference." PLOS Computational Biology 21.9 (2025): e1013461.

The paper develops a transcriptome-wide approach for inferring root causal genes using genetic variation as instrumental variables. This formulation permits root-causal analysis without requiring Perturb-seq data.

- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes with the heteroscedastic noise model." Journal of Computational Science 72 (2023): 102099.

The paper develops GRCI for identifying patient-specific root causes under heteroscedastic noise and derives identifiability conditions establishing when the corresponding causal model is uniquely recoverable.

- Strobl, Eric V., Thomas A. Lasko, and Eric R. Gamazon. "Mitigating pathogenesis for target discovery and disease subtyping." Computers in Biology and Medicine 171 (2024): 108122.

This study connects root causal analysis to pathogenesis and introduces an estimator for how root causal effects change under intervention versus no intervention. The framework supports both intervention-target discovery and disease subtyping based on causal pathogenesis.

- Strobl, Eric V. "Counterfactual formulation of patient-specific root causes of disease." Journal of Biomedical Informatics 150 (2024): 104585.

The paper formalizes patient-specific root causes at the counterfactual level. The framework relates the clinical concept of a root cause to a precise patient-specific causal definition at the counterfactual level of Pearl's causal hierarchy.

- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes of disease." Proceedings of the 13th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics. 2022.

This work defines patient-specific root causes and presents an efficient discovery method based on LiNGAM.

- Strobl, Eric, and Thomas A. Lasko. "Sample-specific root causal inference with latent variables." Conference on Causal Learning and Reasoning. PMLR, 2023.

The study generalizes the LiNGAM-based approach to accommodate latent variables, extending patient-specific root causal inference to settings with unmeasured factors.

## Causal Discovery and Inference

_This line of work develops methods for causal discovery and causal inference from observational data, particularly focusing on complications such as missingness, selection effects, latent variables, cycles, measurement error, and distributional heterogeneity._

- Strobl, Eric V. "COMPACT: Spectral Adjustment Scores from a Complete and Irreducible Causal Criterion." arXiv:2608.10305 (2026).

This work examines whether covariate adjustment can be derived directly from causal requirements rather than from balancing alone. COMPACT uses a minimal set of conditional and unconditional independence relations to constrain the causal graph structure relevant to adjustment. The structural criterion reduces to a generalized eigenvalue decomposition, yielding low-dimensional spectral adjustment scores derived from the causal problem.

- Strobl, Eric V. "Fast Nonparametric Conditional Independence Testing via Two-Stage Regression." arXiv:2606.18011 (2026).

This work develops BLITZ, a sub-second nonparametric conditional independence test designed to maintain Type I error control under complex nonlinear structure. Flexible nonparametric tests often incur substantial computational costs because they require fitting complex nuisance models. BLITZ instead derives the nuisance-estimation requirements from the product-form test statistic and reduces their complexity at multiple stages. This allows relatively simple and computationally efficient models to satisfy the conditions required for valid nonparametric conditional independence inference.

- Strobl, Eric V., Kun Zhang, and Shyam Visweswaran. "Approximate kernel-based conditional independence tests for fast non-parametric causal discovery." Journal of Causal Inference 7.1 (2019): 20180017.

The paper introduces computationally efficient kernel-based conditional independence tests using approximations that make nonparametric causal discovery feasible at larger scales.

- Strobl, Eric V., Shyam Visweswaran, and Peter L. Spirtes. "Fast causal inference with non-random missingness by test-wise deletion." International Journal of Data Science and Analytics 6.1 (2018): 47-62.

This project addresses causal discovery in datasets with substantial non-random missingness, where complete-case analysis can discard otherwise usable observations. The approach represents missingness as a variable-specific form of selection and uses the ability of FCI to accommodate selection bias. Test-wise deletion allows the relevant selection set to vary across conditional independence tests, preserving additional data while remaining sound under appropriate assumptions.

- Strobl, Eric V. "A constraint-based algorithm for causal discovery with cycles, latent variables and selection bias." International Journal of Data Science and Analytics 8.1 (2019): 33-56.

This work addresses causal discovery in the simultaneous presence of cycles, latent variables, and selection bias. The paper develops a constraint-based method that incorporates orientation rules for reasoning about all three complications within a common causal discovery framework.

- Strobl, Eric V. "Causal discovery with a mixture of DAGs." Machine Learning 112.11 (2023): 4201-4225.

This project studies a representation in which an apparently cyclic causal system can arise from variation among multiple acyclic causal regimes. Structural equation models often represent cycles through equilibrium relationships, whereas biological processes can also involve sequential interactions across different regimes or time points. A mixture of DAGs provides a representation of the latter setting in which aggregate data can exhibit apparent cyclic structure even when the component regimes are acyclic. This representation substantially improved causal discovery performance in the settings considered.

- Strobl, Eric V. "Automated hyperparameter selection for the PC algorithm." Pattern Recognition Letters 151 (2021): 288-293.

The paper proposes a stability-based modification to the PC algorithm that selects the significance threshold automatically, reducing sensitivity to arbitrary hyperparameter choices and improving robustness in causal discovery.

- Strobl, Eric V., Peter L. Spirtes, and Shyam Visweswaran. "Estimating and controlling the false discovery rate of the PC algorithm using edge-specific p-values." ACM Transactions on Intelligent Systems and Technology (TIST) 10.5 (2019): 1-37.

The paper derives edge-specific p-value bounds for the PC algorithm and uses them to control the false discovery rate, providing uncertainty quantification for individual edges in learned causal graphs.

## Others

- Strobl, Eric V. "Global Interpretability via Automated Preprocessing: A Framework Inspired by Psychiatric Questionnaires." arXiv:2602.23459 (2026).

This work considers global model interpretability in settings with general nonlinear predictive relationships. Instance-specific explanations such as SHAP values vary across patients and outcomes, whereas some clinical applications benefit from a single interpretable model. The paper shows how a general nonlinear prediction problem can be decomposed into an interpretable nonlinear preprocessing step followed by a simple linear predictive model, while retaining nonlinear predictive performance. The preprocessing is constrained to preserve the meaning of the original variables while extracting the nonlinear structure needed for prediction.

