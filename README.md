# Bayesian-Analysis
#### *"Using uncertainty as the brush, coloring with prior beliefs, and composing with a hierarchical structure — creating the statistical art of small-sample analysis! --- Ting Lu"*
Bayesian analysis is a statistical approach that estimates parameter posterior distributions using the Bayesian theorem, incorporating prior information and observed data through MCMC sampling.

## Introduction
This repository contains 3 classic Bayesian analysis scenarios and related analysis processes including [Bayesian Hierarchical Modeling](https://en.wikipedia.org/wiki/Bayesian_hierarchical_modeling), [Hierarchical Linear Mixed Model](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2883299/), [Hierarchical Poisson Model](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3783969/), [MCMC Sampling](https://en.wikipedia.org/wiki/Markov_chain_Monte_Carlo), [Gibbs Sampling](https://en.wikipedia.org/wiki/Gibbs_sampling), [Metropolis-Hastings sampling](https://en.wikipedia.org/wiki/Metropolis%E2%80%93Hastings_algorithm), [Randomized Clinical Trial(Experimental Studies)](https://www.cancerresearchuk.org/about-cancer/find-a-clinical-trial/what-clinical-trials-are/randomised-trials#:~:text=Randomised%20trials%20have%20at%20least,phase%202%20trials%20are%20randomised.) etc.

## Study 1. Belgian Lifestyle Improvement and Cholesterol Intake Variability Study (BLICIVS): 
This study assesses lifestyle improvement campaigns in Western Europe, focusing on smoking cessation and reducing saturated fat consumption. Around 1990, a dietary survey, the [**Inter-regional Belgian Bank Employee Nutrition Study (IBBENS)**](https://pubmed.ncbi.nlm.nih.gov/8194492/) was set up to compare the dietary intake in different geographical areas in Belgium. The IBBENS study was performed in eight subsidiaries of one bank situated in seven Dutch-speaking cities in the north and in one French-speaking city in the south of Belgium. It examines **cholesterol intake variability** among 563 healthy employees(371 male and 192 female) of a Belgian bank, aged 38.3 on average, across **8 subsidiaries**. Data is collected through a 3-day food record and interviews. To contrast the variability of cholesterol intake (chol) in mg/day between the subsidiaries to the variability within 8 subsidiaries, I created the following analysis plan: 

 - [Here is the detailed code process](https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/tree/main/Study1-Cholesterol-Intake-Variability)
 - EDA
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/EDA.png" width="60%">
</div>

 - **Bayesian hierarchical normal model**:
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/IBB.png" width="60%">
</div>

 - Prior setting (for Bayesian hierarchical normal model)
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/IBB2.png" width="60%">
</div>

- Gibbs sampling (MCMC sampling): Markov Chain Convergence Diagnosis: Trace Plot & ACF Plot & ESS
- Posterior Inference (posterior mean and variance & 95% credible interval, variability comparison, shrinkage evaluation) 
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/var.png" width="100%">
</div>
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/shrinkage.png" width="100%">
</div>

## Study 2. Multicenter RCT Comparing Oral Medications for Toenail Dermatophyte Onychomycosis: Itraconazole vs. Lamisil: 
This study aims to discern the overall efficacy of the treatments and identify potential differences between the two medication regimens.In a comprehensive double-blinded multicenter **Randomized Clinical Trial (RCT)** spanning 36 centers, a total of 298 participants, including both sportsmen and elderly individuals, underwent treatment for toenail dermatophyte onychomycosis. They were administered one of two oral medications: **Itraconazole at 250 mg daily (treatment group 0) or Lamisil at 250 mg daily (treatment group 1)**. The treatment course extended over 12 weeks, with assessments conducted at multiple time points, including 0, 1, 2, 3, 6, 9, and 12 months. The primary metric for evaluating treatment response was the measurement of unaffected nail length for the big toenail.

 - [Here is the detailed code process](https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/tree/main/Study2-Multicenter-RCT)
 - EDA
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/loess.png" width="60%">
</div>

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/t0.png" width="60%">
</div>

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/t1.png" width="60%">
</div>

 - **Linear fixed effect model** & Prior setting

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/fix.png" width="60%">
</div>

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/fixPr.png" width="60%">
</div>

 - **Linear mixed effect model** & Prior setting (with random intercept and slope)

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/mix.png" width="60%">
</div>

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/mixPr.png" width="60%">
</div>

 - Gibbs sampling (MCMC sampling): Markov Chain Convergence Diagnosis: Trace Plot & ESS

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/trace.png" width="60%">
</div>

 - Posterior Inference (posterior mean and variance & 95% credible interval): Fixed effect model vs. Mixed effect model

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study2-Multicenter-RCT/vs.png" width="60%">
</div>

## Study 3. Exploring Highest Disease Rates in 6 Neighboring Counties: 
This study investigating the impact of PCB Contamination to disease rate in six neighboring counties over a five-year period. **The number of occurrences of a rare, nongenetic birth defect** in a five-year period for six neighboring counties is y = (1, 3, 2, 12, 1, 1). The counties have populations of 2 = (33, 14, 27, 90, 12, 17), given in thousands. The second county has higher rates of toxic chemicals (PCBs) present in soil samples, and it is of interest to know if this town has a high disease rate as well.  
 - [Here is the detailed code process](https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/tree/main/Study3-Disease-Rate)
 - Hierarchical Poisson Model & Gamma Prior
   <div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study3-Disease-Rate/poi.png" width="60%">
</div>
 - Posterior Distribution (full conditional distribution of diseases rate)
    <div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study3-Disease-Rate/con.png" width="60%">
</div>
   <div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study3-Disease-Rate/fullcon.png" width="60%">
</div>
 - Acceptance Ratio
   <div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study3-Disease-Rate/AcceptR.png" width="60%">
</div>
 - **Metropolis-Hastings Sampling (MCMC sampling)**
 - Posterior vs. Observsed vs. Prior (Disease rate in each county)
    <div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study3-Disease-Rate/Post_i.png" width="60%">
</div>
   <div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study3-Disease-Rate/Post_all.png" width="60%">
</div>
 - Disease rate County 2 vs. County i
    <div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study3-Disease-Rate/2nd.png" width="60%">
</div>

## Bayesian Analysis Advantages
 - **Robustness for Small Sample Data**: In scenarios such as Phase I clinical trials to assess new medical treatments or drug effects, where budget and safety considerations limit the number of patients enrolled, Bayesian analysis can provide robust parameter estimates by incorporating prior knowledge.
 - **Uncertainty Modeling**: Unlike traditional frequentist statistics, which provide fixed parameter values, Bayesian analysis offers **probability distributions for parameter estimation**. This allows for a better understanding of parameter variability and inherent uncertainty.
 - **Hierarchical Models (Mixed Effects Models)**: Bayesian analysis treats parameters as random variables and flexibly introduces parameters at different hierarchical levels, capturing more variability. For instance, in medical research, patients, hospitals, and regions may exhibit varying levels of variability.

## Bayesian Analysis Disadvantages:
 - **Computationally expensive for large samples**
 - **Subjective Prior Selection**: The choice of prior distributions is subjective and may depend on domain expertise. Sensitivity analysis is often necessary when dealing with different prior distributions.

## Prior Distribution Choices:

 - [Non-informative Prior](https://www.sciencedirect.com/topics/mathematics/noninformative-prior): When no specific domain knowledge is available or neutrality is desired, non-informative priors, such as uniform, normal, or broad distributions, can be used. These distributions do not introduce excessive prior information.
 - [Conjugate Prior](https://towardsdatascience.com/conjugate-prior-explained-75957dc80bfb): Conjugate priors are selected to simplify calculations by ensuring that the posterior distribution belongs to the same distribution family as the prior. For example, the Beta distribution is a conjugate prior for Bernoulli and binomial distributions, while the Gamma distribution is a conjugate prior for the Poisson distribution, and the normal distribution is a conjugate prior for the normal distribution.
 - [Informative Prior](https://en.wikipedia.org/wiki/Prior_probability#:~:text=An%20informative%20prior%20expresses%20specific,the%20temperature%20at%20noon%20tomorrow.) Informational priors are based on domain knowledge or similar research experience. They provide information about the possible range of parameters and whether parameters should exhibit specific characteristics, such as symmetry or non-negativity.

## Acknowledgement
The analysis processes referenced materials from the course - [NYU - GPHGU 2372 - Applied Bayesian Analysis in Public Health](https://www.coursicle.com/nyu/courses/GPHGU/2372/). As a graduate of this course in 2022, I would like to express my sincere gratitude to the course instructor [Dr. Hai Shu](https://publichealth.nyu.edu/faculty/hai-shu).










