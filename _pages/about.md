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

Outcome Learning
======
_I develop data-adaptive methods for constructing composite outcomes that are explicitly aligned with the scientific or clinical task. Rather than treating outcomes as fixed, these approaches learn clinically interpretable outcome measures optimized for prediction, treatment differentiation, or causal analysis, with applications across psychiatry._

- Strobl, Eric V. (2026) Task-aligned outcome learning in psychiatry: reducing endpoint dilution. Front. Psychiatry 17:1832978. doi: 10.3389/fpsyt.2026.1832978.

I wrote this Perspective because whenever I introduced outcome learning in psychiatry, many of the same thoughtful questions kept coming up about motivation, endpoint shopping, and statistical validity. Rather than address them piecemeal each time, I wanted to collect the reasoning and practical safeguards in one place. The paper now serves as a concise introduction to the framework and a reference for the concerns that often arise when people first encounter the idea.
- Strobl, Eric V., and Semmie Kim. 2026. “Learning Outcomes That Maximally Differentiate Psychiatric Treatments,” International Journal of Methods in Psychiatric Research: e70074.

This work grew out of a disconnect I kept seeing between the literature and clinical practice. I would read that psychiatric medications showed little or no meaningful difference, even though clinicians often distinguish them quite clearly by the pattern of symptoms they affect. At the same time, much of the field seemed to move on to explaining this through patient heterogeneity, which felt like jumping ahead before asking whether the outcome itself was obscuring the difference. Supervised Varimax was an attempt to formalize how psychiatrists already think about medications by comparing patterns of effects across symptoms rather than relying on a single total score.  
- Strobl, Eric V. "Consistent differential effects of bupropion and mirtazapine in major depression." Journal of Affective Disorders 388 (2025): 119551.

I used this study as an additional check that Supervised Varimax was recovering the same kinds of medication differences that psychiatrists recognize in clinic. I chose bupropion and mirtazapine because both stand out from many other antidepressants, and from each other, in their clinical effect profiles. I therefore examined three contrasts: bupropion versus other antidepressants, mirtazapine versus other antidepressants, and bupropion versus mirtazapine. The algorithm closely recovered these recognizable treatment patterns, suggesting that the formalism maps well onto the intuition clinicians already use when distinguishing medications in practice.
- Strobl, Eric V. "Unique Behavior Profiles that Specify Mental Distress in Autism." Journal of Autism and Developmental Disorders (in press)

This project grew directly out of clinic. I kept seeing caregivers describe striking behavior changes in children with autism who were nonverbal or could not reliably explain what they were feeling. Rather than chalking these behaviors up to a generic signal of distress, I wondered whether specific patterns could be deduced from them. I found that caregiver-observed behaviors could distinguish different forms of mental distress and reveal autism-specific internalizing and externalizing profiles. I then mapped these patterns onto clinician-familiar diagnostic categories, and the resulting framework has become genuinely useful to me in my own clinical practice.
- Strobl, Eric. "Predicting the Predictable in the Psychiatric High Risk." Machine Learning for Healthcare Conference. PMLR, 2025.

I developed SCORE after becoming perplexed by the psychosis prodrome literature, where increasingly rich datasets often still failed to predict who would later develop psychosis. I started thinking more generally about what we can actually predict about the future. Comically, I realized that I can predict that my lawn will be mowed sometime in the next two weeks, but I certainly cannot predict the stock market. That made me wonder why we prespecify outcomes and then force algorithms to predict them, rather than first asking which aspects of the future are actually predictable. SCORE grew out of that question by learning clinically interpretable outcomes that the available data can genuinely predict.
- Strobl, Eric V. "Learning Causally Predictable Outcomes from Psychiatric Longitudinal Data." Biocomputing 2026: Proceedings of the Pacific Symposium. 2025.
  
This work came from stepping back from the latent-confounding problem, which often seemed nearly impossible to solve in full generality, and asking whether longitudinal medical data contain some special structure that could make the problem easier. I realized that past treatment history can provide exactly that structure when its effects are transient and therefore do not directly determine the later outcomes being considered. Once I also allowed the outcome itself to be learned rather than fixed in advance, that historical information could be used to search for outcomes whose treatment effects remain causally identifiable even in the presence of latent confounding.
- Strobl, Eric V. “Oxytocin Enhances Social-Emotional Reciprocity in Autism.” medRxiv (2025): 2025-07.

I had worked on oxytocin as an undergraduate, and years later I wondered whether it was worth revisiting. The large SOARS-B trial had been negative, but after reading the paper I suspected that the prespecified outcomes were not sensitive to the effects oxytocin was actually producing. I therefore used SCORE to learn a treatment-sensitive outcome directly from the randomized data, with bootstrap and permutation procedures to control Type I error. The result may be controversial because oxytocin has a long history of conflicting findings and this runs against a pivotal negative trial, but that history may itself reflect an outcome problem. For subtle, multidimensional treatment effects, it can be nearly impossible to guess the right endpoint in advance, especially when the effect does not follow conventional factor structure. Rather than repeatedly guessing, we can let the randomized treatment contrast help reveal what the treatment actually changes.
- Strobl, Eric V. "Mendelianization: Concentrating polygenic signal into a single causal locus." Genetic Epidemiology 50.6 (2026): e70053.
  
I used outcome learning to construct phenotypes that concentrate polygenic association signal onto individual genetic loci, improving interpretability and causal localization. This work grew out of both my outcome-learning research and my interest in identifying genetic root causes of disease. A central goal was to base causal localization on assumptions stated directly in terms of genetic architecture, while avoiding abstract causal inference assumptions such as consistency, exclusion restriction, or an underlying DAG whenever possible.

Root Cause Analysis
======
_This line of work grew out of a simple question: if we care about the causes of disease, why not try to directly identify the root causes in an individual patient? I knew that even framing the problem this way would draw substantial skepticism and resistance. Still, I could not dismiss the question simply because it fell outside the usual way of thinking. From a treatment perspective, identifying what actually initiates disease in a particular patient seemed too important to ignore. I therefore pursued a framework for patient-specific root causes despite the pushback, because I believed the question could ultimately help move medicine toward more causally targeted treatments._

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

Causal Discovery and Inference
======
_I develop methods for causal discovery and causal inference from observational data, particularly focusing on real complications such as missingness, selection effects, latent variables, cycles, measurement error, and distributional heterogeneity._

- Strobl, Eric V. "COMPACT: Spectral Adjustment Scores from a Complete and Irreducible Causal Criterion." arXiv:2608.10305 (2026).
  
I had long been curious about the usual justification for the propensity score as the coarsest balancing score. Since the ultimate goal is causal inference, I wondered whether adjustment could instead be derived more directly from the causal problem itself. That led to COMPACT, where a minimal set of conditional and unconditional independence relations is used to maximally constrain the causal graph structure relevant to adjustment. I especially liked that this structural criterion ultimately collapsed to a generalized eigenvalue decomposition, turning an abstract causal argument into a simple spectral algorithm.

- Strobl, Eric V. "Fast Nonparametric Conditional Independence Testing via Two-Stage Regression." arXiv:2606.18011 (2026).

I developed BLITZ, a sub-second nonparametric conditional independence test that maintains strong Type I error control under complex nonlinear structure. It was one of the hardest methodological problems I have worked on because greater flexibility seemed to come with an unavoidable computational cost. The breakthrough was to stop asking how to fit increasingly powerful models and instead ask what the product-form test statistic actually requires for validity, then make those requirements as easy as possible to satisfy in practice. BLITZ does this by reducing the complexity of the nuisance estimation problem at multiple levels, allowing simple, fast models to meet the conditions needed for accurate inference.

- Strobl, Eric V., Kun Zhang, and Shyam Visweswaran. "Approximate kernel-based conditional independence tests for fast non-parametric causal discovery." Journal of Causal Inference 7.1 (2019): 20180017.

We designed computationally efficient kernel-based conditional independence tests that make nonparametric causal discovery feasible at larger scales.
- Strobl, Eric V., Shyam Visweswaran, and Peter L. Spirtes. "Fast causal inference with non-random missingness by test-wise deletion." International journal of data science and analytics 6.1 (2018): 47-62.

I pursued this project while working with real datasets that had substantial missingness, where throwing away otherwise usable samples seemed unnecessarily wasteful. I realized that missingness could be viewed as an additional, variable-specific layer of selection bias. Since FCI already handles selection bias, I developed a test-wise deletion approach that lets the relevant selection set change with each conditional independence test, preserving more data while retaining soundness under suitable assumptions.
- Strobl, Eric V. "A constraint-based algorithm for causal discovery with cycles, latent variables and selection bias." International Journal of Data Science and Analytics 8.1 (2019): 33-56.

I pursued this project after my PhD, during clinical rotations in medical school, because I wanted to take on a genuinely difficult open problem in causal discovery. At the time, jointly handling cycles, latent variables, and selection bias was still unresolved. I thought that even if I could not prove a complete solution, it might still be useful to build an algorithm that incorporated as many valid orientation rules as possible. That effort led to a constraint-based method designed to reason about all three complications simultaneously.
- Strobl, Eric V. "Causal discovery with a mixture of DAGs." Machine Learning 112.11 (2023): 4201-4225.

I pursued this project because I was perplexed by how cycles are usually represented in structural equation models, as a kind of instantaneous equilibrium. In biology and medicine, however, I had often been taught to think of cycles sequentially: A causes B, then B causes A, and so on over time. At the same time, I was somewhat disappointed by how causal discovery algorithms performed in practice. Putting those two observations together led me to study mixtures of DAGs, where an apparent cycle can instead arise from switching among multiple acyclic causal regimes. What struck me was that this representation substantially improved causal discovery performance relative to assuming a single DAG, which made me wonder whether the more sequential view of cycles I had learned in biology may sometimes be a better description of nature than equilibrium-cycle models.
- Strobl, Eric V. "Automated hyperparameter selection for the PC algorithm." Pattern Recognition Letters 151 (2021): 288-293.

I proposed a stability-based modification to PC that selects the significance threshold automatically, reducing sensitivity to arbitrary hyperparameter choices and improving robustness in practice.
- Strobl, Eric V., Peter L. Spirtes, and Shyam Visweswaran. "Estimating and controlling the false discovery rate of the pc algorithm using edge-specific p-values." ACM Transactions on Intelligent Systems and Technology (TIST) 10.5 (2019): 1-37.

We derived edge-specific p-value bounds for PC and use them to control false discoveries, enabling more principled uncertainty quantification in learned causal graphs.


Others
======
- Strobl, Eric V. "Global Interpretability via Automated Preprocessing: A Framework Inspired by Psychiatric Questionnaires." arXiv:2602.23459 (2026).

I took a stab at a problem outside my usual comfort zone: model interpretability. Instance-specific explanations such as SHAP values felt too unstable for clinical use because they can change across patients and outcomes, so I wanted a single interpretable model that still retained nonlinear predictive accuracy. The key realization was that a nonlinear prediction problem could be decomposed into an interpretable nonlinear preprocessing step followed by a simple linear model. What made this work was that the nonlinearity was not arbitrary; it had to behave like genuine preprocessing, preserving the meaning of the original variables while extracting the structure needed for prediction.
