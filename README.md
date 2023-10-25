# Bayesian-Analysis-Biostatistics



## Introduction
This repository contains 3 classic Bayesian analysis scenarios and related analysis processes including [Bayesian Hierarchical Modeling](https://en.wikipedia.org/wiki/Bayesian_hierarchical_modeling), [Bayesian Hierarchical Linear Mixed Model](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2883299/), [Bayesian Hierarchical Poisson Regression Model](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3783969/), [MCMC Sampling](https://en.wikipedia.org/wiki/Markov_chain_Monte_Carlo), [Gibbs Sampling](https://en.wikipedia.org/wiki/Gibbs_sampling), [Metropolis-Hastings algorithm](https://en.wikipedia.org/wiki/Metropolis%E2%80%93Hastings_algorithm), [Randomized Clinical Trial(Experimental Studies)](https://www.cancerresearchuk.org/about-cancer/find-a-clinical-trial/what-clinical-trials-are/randomised-trials#:~:text=Randomised%20trials%20have%20at%20least,phase%202%20trials%20are%20randomised.)

## Study 1. Belgian Lifestyle Improvement and Cholesterol Intake Variability Study (BLICIVS): 
This study assesses lifestyle improvement campaigns in Western Europe, focusing on smoking cessation and reducing saturated fat consumption. It examines **cholesterol intake variability** among 563 healthy employees(371 male and 192 female) of a Belgian bank, aged 38.3 on average, across **8 subsidiaries**. Data is collected through a 3-day food record and interviews. To contrast the variability of cholesterol intake (chol) in mg/day between the subsidiaries to the variability within 8 subsidiaries, I created the following analysis plan: 

 - [Here is the detailed code process](https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/tree/main/Study1-Cholesterol-Intake-Variability)

<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/EDA.png" width="60%">
</div>

### Bayesian hierarchical normal model:
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/IBB.png" width="60%">
</div>

### Prior setting (for Bayesian hierarchical normal model)
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/IBB2.png" width="60%">
</div>

### Gibbs sampling (MCMC sampling)
### MCMC Diagnosis: Trace Plot & ACF Plot & ESS
### Posterior Inference (posterior mean and variance & 95% credible interval, shrinkage evaluation) 
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/var.png" width="80%">
</div>
<div align="center">
  <img src="https://github.com/Ting-DS/Bayesian-Analysis-Biostatistics/blob/main/Study1-Cholesterol-Intake-Variability/shrinkage.png" width="80%">
</div>

## Study 2. Multicenter RCT Comparing Oral Medications for Toenail Dermatophyte Onychomycosis: Itraconazole vs. Lamisil: 
This study aims to discern the overall efficacy of the treatments and identify potential differences between the two medication regimens.In a comprehensive double-blinded multicenter **Randomized Clinical Trial (RCT)** spanning 36 centers, a total of 298 participants, including both sportsmen and elderly individuals, underwent treatment for toenail dermatophyte onychomycosis. They were administered one of two oral medications: **Itraconazole at 250 mg daily (treatment group 0) or Lamisil at 250 mg daily (treatment group 1)**. The treatment course extended over 12 weeks, with assessments conducted at multiple time points, including 0, 1, 2, 3, 6, 9, and 12 months. The primary metric for evaluating treatment response was the measurement of unaffected nail length for the big toenail. 

## Study 3. Exploring Disease Rates in Six Neighboring Counties and their Association with PCB Contamination: 
This study investigating the impact of PCB Contamination to disease rate in six neighboring counties over a five-year period. **The number of occurrences of a rare, nongenetic birth defect** in a five-year period for six neighboring counties is y = (1, 3, 2, 12, 1, 1). The counties have populations of 2 = (33, 14, 27, 90, 12, 17), given in thousands. The second county has higher rates of toxic chemicals (PCBs) present in soil samples, and it is of interest to know if this town has a high disease rate as well.

## Acknowledgement
The analysis processes referenced materials from the course - [NYU - GPHGU 2372 - Applied Bayesian Analysis in Public Health](https://www.coursicle.com/nyu/courses/GPHGU/2372/). As a graduate of this course in 2022, I would like to express my sincere gratitude to the course instructor [Dr. Hai Shu](https://publichealth.nyu.edu/faculty/hai-shu).










