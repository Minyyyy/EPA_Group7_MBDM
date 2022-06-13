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

(1) Generate_basecase_disag_loc_and_time.ipynb -> We start off by running a base case. This results in base_case_without_NaN.csv
(2) Generate_open_exploration_random_policies.ipynb -> We do open exploration for 400 scenarios with 100 policy options. This results in policies_fully_disaggregated.tar.gz
(3) Compare_basecase_policies.ipynb -> Compares the basecase and policies. It imports base_case_without_NaN.csv and policies_fully_disaggregated.tar.gz and puts them into one dataframe. 
We compare and analyze the base case and the policies and visualize the differences. We also conduct the PRIM analysis and the vulnerability analysis/SOBOL in this file.
(4) problem_formulation_modified.py -> This file contains the modified problem formulation.
(5) min_max_values.ipynb -> This generates outcome_ranges.csv. This is a very small csv file in which the maximum and minimum values of the open exploration are saved. For the optimization, the algorithm requires the maximum and minimum values as input.
(6) MORDM_policies_optimization.ipynb -> In this notebook the optimization over policy levers is conducted. It calls the function from problem_formulation_modified.ipynb function and the minimum and maximum values from the outcome_ranges.csv file.
