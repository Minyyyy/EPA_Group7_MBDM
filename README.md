# EPA_Group7_MBDM
MBDM_Group7
An integrated strategy for the Ijssel River Area 


### Created by
```
Group 7 - Perspective of Dikering 1

Jonas Besselink
Fenna Cleuren
Dorris Corsten
Eva Hogervorst 
Abhiramini Rajiv
Mohammed Sufiyan
```

### Project Description
Given that the Ijssel river area may experience flooding in the years to come, a strategy on appropriate policy measures needs to be developed. 
Policy advice given from the perspective of DikeRing 1 - Doesburg. 
Policy advice  is given recognising that the situation is subject to deep uncertainty.
Policy advice is based on exploratory modeling results, conducted with the EMA_Workbench. 
Project is done in light of TU Delft, EPA course "Model-based Decision Making".

### Folder structure
- code
  * Open exploration
  * Scenario Discovery
  * Sensitivity Analysis
  * Optimization
  * Robustness
- data (contains data files as initially provided by course) 
- documentation (contains information and inspiration files as initially provided by course)
- final reports (contains final analysis and political reflection) 
- results (contains analysis results saved as gz and csv files)

#### Overview of the project

```
Overview of the project:

(0) Generate_basecase_disag_loc_and_time.ipynb -> We start off by running a base case. This results in base_case_without_NaN.csv
(1) Generate_open_exploration_random_policies.ipynb -> We do open exploration for 400 scenarios with 100 policy options. This results in policies_fully_disaggregated.tar.gz
(2) Compare_basecase_policies.ipynb -> Compares the basecase and policies. It imports base_case_without_NaN.csv and policies_fully_disaggregated.tar.gz and puts them into one dataframe. 
We compare and analyze the base case and the policies and visualize the differences. We also conduct the PRIM analysis and the vulnerability analysis/SOBOL in this file.
(3) Sensitivity Analysisi.pynb -> The sensitivity analysis is conducted in this notebook.
(4) Scen_Disc_Policy_Exploration.ipynb -> The PRIM analysis is conducted in this notebook. 
(5) problem_formulation_modified.py -> This file contains the modified problem formulation.
(6) Multi-Scenario MORDM with worst case scenarios.ipynb -> A set of worst-case scenarios is generated and a set of candidate policies is generated that optimizes 
at mitigating and/or preventing the harm from these scenarios. This set of policies is output as pickle_results_list_2000nfe. It also outputs the data on convergence as 
pickle_convergence_list_2000nfe
(7) Re-evaluation_candidate_strategies.ipynb -> This uses the candidate policies set from pickle_results_list_2000nfe to test each policy under 1000 scenarios. 
This outputs results_reevaluation.pickle
(8) Evaluate_robustness.ipynb -> Evaluates the results from results_reevaluation.pickle using two robustness metrics.
```
