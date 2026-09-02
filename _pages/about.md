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
[Other Work](#other-works)

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

- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes of disease." Proceedings of the 13th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics. 2022.

This paper provides the initial formulation of patient-specific root causal inference using a linear non-Gaussian acyclic model (LiNGAM), chosen as a simple identifiable structural equation model. Root causes are represented by exogenous error terms, or patient-specific shocks to variables, whose downstream effects contribute to the diagnostic outcome; the formulation is interventional rather than counterfactual and quantifies each error term's patient-specific contribution using Shapley values. The main methodological contribution is Root Causal Inference (RCI), which efficiently identifies the relevant exogenous errors and estimates their effects on diagnosis rather than relying on generic ICA or LiNGAM causal-discovery procedures. The algorithm also modifies DirectLiNGAM to recover only the error terms relevant to the diagnostic outcome and to reduce the computational cost of their extraction.

- Strobl, Eric, and Thomas A. Lasko. "Sample-specific root causal inference with latent variables." Conference on Causal Learning and Reasoning. PMLR, 2023.

The study generalizes the original LiNGAM-based root causal inference framework to settings with latent confounding. It introduces Extract Errors with Latents (EEL), which recovers individual exogenous error terms when the model permits and otherwise recovers them up to contamination by other error terms lying on specific causal paths. EEL also constructs a dependency graph over the recovered errors, identifying the smallest dependent sets needed for efficient computation of patient-specific Shapley contributions. This extends root causal inference beyond the fully observed setting without requiring recovery of the complete underlying causal graph.

- Strobl, Eric V., and Thomas A. Lasko. "Identifying patient-specific root causes with the heteroscedastic noise model." Journal of Computational Science 72 (2023): 102099.

This paper extends the original LiNGAM-based root causal inference framework to the heteroscedastic noise model, allowing nonlinear causal relationships and covariate-dependent noise. It proves identifiability of the full causal DAG under this model, substantially generalizing simpler additive-noise formulations. The paper also introduces Generalized Root Causal Inference (GRCI), which estimates the causal structure, extracts the exogenous error terms needed for patient-specific root-cause analysis, and computes their sample-specific contributions. The algorithm uses a two-stage procedure based on the conditional mean and mean absolute deviation, making minimal assumptions beyond the heteroscedastic noise model while providing accurate and robust root-cause recovery.

- Strobl, Eric V. "Counterfactual formulation of patient-specific root causes of disease." Journal of Biomedical Informatics 150 (2024): 104585.

This paper reformulates patient-specific root causes at the counterfactual level. Earlier work used an interventional formulation in which root causal effects were defined by intervening on exogenous error terms. Building on the recently developed framework of backtracking counterfactuals, this paper instead formalizes the clinical process of reasoning backward from a patient's observed disease state toward its upstream causes while preserving the factual patient data and causal mechanisms. The resulting definition places patient-specific root causes on the counterfactual level of Pearl's causal hierarchy and provides a more rigorous causal formulation of the clinical concept of a root cause.

- Strobl, Eric V., Thomas A. Lasko, and Eric R. Gamazon. "Mitigating pathogenesis for target discovery and disease subtyping." Computers in Biology and Medicine 171 (2024): 108122.

This study connects patient-specific root causal analysis to the clinical concept of disease pathogenesis by representing pathogenesis through the effects of root causes on downstream disease processes. It introduces Treated Root causal Effects (TREs) to quantify how interventions modify those pathogenic effects. The framework uses TREs to identify intervention targets that mitigate pathogenesis and to subtype patients according to similarities in how their pathogenic mechanisms respond to treatment. This provides a direct connection between causal modeling, treatment-target discovery, and clinically interpretable concepts of pathogenesis and disease heterogeneity.

- Strobl, Eric V., and Eric Gamazon. "Discovering root causal genes with high-throughput perturbations." Elife 13 (2025): RP100949.

This study uses Perturb-seq data to recover causal ordering among genes in order to identify root causal genes, defined as the first gene-expression changes induced by the underlying genetic or non-genetic root causes of disease. A central contribution is the Root Causal Strength (RCS), a model-free measure of the magnitude of a patient-specific root-causal effect that can be computed from observed gene expression without recovering the underlying exogenous error terms or specifying their functional form or distribution. Perturb-seq is used to identify the causal structure needed to estimate RCS, while bulk RNA-seq provides patient-level expression and disease information. The resulting RCSP algorithm therefore combines high-throughput perturbation data for causal ordering with bulk transcriptomic data for patient-specific identification of the genes at which upstream root causes first enter the gene-expression system.

- Strobl, Eric V., and Eric R. Gamazon. "Transcriptome-wide root causal inference." PLOS Computational Biology 21.9 (2025): e1013461.

This study follows the Perturb-seq approach by replacing experimental perturbations with genetic variants as instrumental variables for transcriptome-wide root causal inference. It introduces the conditional root causal effect (CRCE), a functionally model-free measure of the patient-specific causal effect of the genetic and non-genetic factors that first perturb a gene expression level. The TWRCI algorithm introduces Competitive Regression, which uses the relative predictive relationships between genetic variants, gene expression levels, and the phenotype to determine which variable a variant most directly perturbs and thereby infer causal ordering among gene expression levels. This ordering is used to reconstruct the gene-expression DAG and identify root causal genes from observational genotype and bulk RNA-seq data. The resulting CRCEs can also be decomposed into genetic and non-genetic components of the root causal effect.

- Strobl, Eric V. "Extracting Root-Causal Brain Activity Driving Psychopathology from Resting State fMRI." arXiv preprint arXiv:2602.07233 (2026).

This study extends root causal analysis to resting-state fMRI using a LiNGAM-inspired bilevel structural causal model. The model represents brain activity as arising from a low-dimensional set of independent latent sources with localized direct effects that subsequently propagate through voxel-to-voxel interactions. A shared mixing structure across subjects permits standardized fMRI time points to be concatenated for ICA-based recovery of the latent sources. The SOURCE algorithm then learns clinically interpretable symptom outcomes that are selectively associated with a small subset of these sources and identifies the corresponding root-proximal brain regions. The resulting framework therefore combines causal source separation, cross-subject temporal pooling, spatial localization, and outcome learning to isolate brain activity patterns that may initiate psychopathology-related processes.

## Causal Discovery and Inference

_This line of work develops methods for causal discovery and causal inference from observational data, particularly focusing on complications such as missingness, selection effects, latent variables, cycles, measurement error, and distributional heterogeneity._

- Strobl, Eric V. "COMPACT: Spectral Adjustment Scores from a Complete and Irreducible Causal Criterion." arXiv:2608.10305 (2026).

This work examines whether covariate adjustment can be derived directly from causal requirements rather than from balancing alone. COMPACT uses a minimal set of conditional and unconditional independence relations to constrain the causal graph structure relevant to adjustment. The structural criterion reduces to a generalized eigenvalue decomposition, yielding low-dimensional spectral adjustment scores derived from the causal problem.

- Strobl, Eric V. "Fast Nonparametric Conditional Independence Testing via Two-Stage Regression." arXiv:2606.18011 (2026).

This work develops BLITZ, a sub-second nonparametric conditional independence test designed to maintain Type I error control under complex nonlinear structure. Flexible nonparametric tests often incur substantial computational costs because they require fitting complex nuisance models. BLITZ instead derives the nuisance-estimation requirements from the product-form test statistic and reduces their complexity at multiple stages. This allows relatively simple and computationally efficient models to satisfy the conditions required for valid nonparametric conditional independence inference.

- Strobl, Eric V., Kun Zhang, and Shyam Visweswaran. "Approximate kernel-based conditional independence tests for fast non-parametric causal discovery." Journal of Causal Inference 7.1 (2019): 20180017.

The paper introduces RCIT and RCoT as scalable nonparametric conditional independence tests for causal discovery. Both methods replace expensive kernel computations with random Fourier features and use relatively small feature representations for the non-conditioning variables. Conditional expectations are estimated with nearly unregularized regression so that limited Fourier-feature representations tend toward overfitting rather than underfitting; for the residual-product criterion, residual dependence caused by underfitting is more problematic. This allows accurate conditional independence testing with substantially fewer Fourier features. RCoT further simplifies RCIT by testing residual dependence directly through cross-covariances of the transformed non-conditioning variables after conditioning on Z. In practice, these approximations retain much of the accuracy of kernel-based conditional independence testing while reducing computational complexity to approximately linear scaling with sample size.

- Strobl, Eric V., Shyam Visweswaran, and Peter L. Spirtes. "Fast causal inference with non-random missingness by test-wise deletion." International Journal of Data Science and Analytics 6.1 (2018): 47-62.

This project addresses causal discovery in datasets with substantial non-random missingness, where complete-case analysis can discard otherwise usable observations. The approach represents missingness as a variable-specific form of selection and uses the ability of FCI to accommodate selection bias. Test-wise deletion allows the relevant selection set to vary across conditional independence tests, preserving additional data while remaining sound under appropriate assumptions.

- Strobl, Eric V. "A constraint-based algorithm for causal discovery with cycles, latent variables and selection bias." International Journal of Data Science and Analytics 8.1 (2019): 33-56.

This paper develops Cyclic Causal Inference (CCI) for constraint-based causal discovery in the simultaneous presence of cycles, latent variables, and selection bias. The approach extends FCI-style reasoning to cyclic systems by weakening orientation conditions to those that remain sufficient when acyclicity can no longer be assumed and by incorporating long-range conditional-independence relations that can distinguish cyclic structures with identical local patterns. The paper also establishes that inducing paths, D-SEP sets, and computable Possible-D-SEP sets remain sufficient for skeleton discovery in the cyclic setting. CCI therefore preserves much of the latent-variable and selection-bias machinery of FCI while generalizing the graphical and orientation theory needed to accommodate feedback cycles.

- Strobl, Eric V. "Causal discovery with a mixture of DAGs." Machine Learning 112.11 (2023): 4201-4225.

This project studies a representation in which an apparently cyclic causal system can arise from variation among multiple acyclic causal regimes. Structural equation models often represent cycles through equilibrium relationships, whereas biological processes can also involve sequential interactions across different regimes or time points. A mixture of DAGs provides a representation of the latter setting in which aggregate data can exhibit apparent cyclic structure even when the component regimes are acyclic. This representation substantially improved causal discovery performance in the settings considered.

- Strobl, Eric V. "Automated hyperparameter selection for the PC algorithm." Pattern Recognition Letters 151 (2021): 288-293.

The paper develops AutoPC to remove the need to specify a single Type I error threshold $\alpha$ for the PC algorithm. Instead, the user supplies a set of plausible alpha values, and AutoPC selects among them using an internal stability criterion. For each candidate alpha, PC first estimates a causal equivalence class and is then rerun with conditional independence tests restricted to the possible-parent sets implied by that estimate. The theoretical basis is that, when the estimated equivalence class is correct, these restricted conditioning sets remain sufficient to recover the same graph. AutoPC therefore selects the alpha value for which the unrestricted and theoretically restricted PC runs are most consistent, providing an unsupervised approach to hyperparameter selection for causal discovery.

- Strobl, Eric V., Peter L. Spirtes, and Shyam Visweswaran. "Estimating and controlling the false discovery rate of the PC algorithm using edge-specific p-values." ACM Transactions on Intelligent Systems and Technology (TIST) 10.5 (2019): 1-37.

The paper develops PC-p to provide statistical error control for individual edges learned by the PC algorithm when exact edge-specific p-values are not directly available. It derives upper bounds on edge-specific p-values by combining the p-values from the conditional independence tests performed during causal discovery. PC-p deliberately uses a relatively liberal initial Type I error threshold to reduce Type II errors, allowing the algorithm to perform more of the tests needed to obtain valid p-value bounds; additional modifications prevent Type II errors from propagating through graph orientation. The resulting bounded edge-specific p-values can then be used with standard multiple-testing procedures, such as Benjamini-Yekutieli, to estimate and control the false discovery rate of the learned causal graph.

## Other Works

- Strobl, Eric V. "Global Interpretability via Automated Preprocessing: A Framework Inspired by Psychiatric Questionnaires." arXiv:2602.23459 (2026).

This work considers global model interpretability in settings with nonlinear predictive relationships. Instance-specific explanations such as SHAP values vary across patients and outcomes, whereas some clinical applications benefit from a single interpretable model. The paper shows how nonlinear longitudinal prediction can be decomposed into an interpretable nonlinear preprocessing step followed by a simple linear predictive model, while retaining Bayes-optimal predictive flexibility in the population. The preprocessing maintains alignment with the original variables while extracting the nonlinear structure needed for prediction.

