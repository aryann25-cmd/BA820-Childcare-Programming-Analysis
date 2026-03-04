## Childcare Stress, Quantified: Mapping U.S. County Dynamics (2008–2018)

**BA820: Unsupervised Machine Learning | Team 13** <br><br>

**Contributors:** 
1. **Aryan Jain** (*aryann25-cmd*)
   
2. **Ansh Gupta** (*anshgupta0604*)
   
3. **Yashaswini Reddy Vari** (*vyreddy-code*)
   
4. **Xiaoqing Ye** (*xiaoqye*)

---

###  Project Motivation:
Childcare is the "silent infrastructure" of the American economy, yet its costs are analyzed through broad national averages that obscure local realities. As Business Analytics students, we realized that "childcare stress" is not a monolith; it is a multi-dimensional crisis driven by varying economic archetypes. This project uses unsupervised learning to map the scale of childcare burdens across **2,360+ U.S. counties** over a decade. We aim to look beyond the hype of short-term economic shocks to understand the actual ecosystem of affordability. The goal is straightforward: to identify which regions are truly in "The Participation Trap" and provide data-driven insights for **Policy Makers**, **Urban Planners**, and **Advocacy Groups**.

---

###  The Data
This project utilizes the **National Database of Childcare Prices (NDCP)**, the most comprehensive federal repository of county-level childcare costs in the U.S. spanning 2008–2018.

#### Data Structure & Composition
* **Scope:** 2,360+ U.S. counties with 10 years of longitudinal features.
* **Feature Categories:** * **Economic:** Median Household Income (MHI), unemployment rates, and poverty metrics.
    * **Labor:** Female Labor Force Participation Rates (FLFPR) and household composition.
    * **Market:** Price points for infant, toddler, and school-age care across center and family-based providers.

---

###  Research Questions

#### 1. The Participation Trap
* **Focus:** Do counties naturally cluster into distinct "Affordability Archetypes" based on the joint distribution of cost burden and labor participation? Can we track the movement of counties into "Stress" states over a decade?

#### 2. Supply-Side Premiums
* **Focus:** Can we segment counties into "Market Archetypes" using **Gaussian Mixture Models (GMM)**? Specifically, identifying where the infant care cost premium is disproportionately high, implying severe supply-side constraints.

#### 3. Structural Trajectories
* **Focus:** Can we detect long-run "Trajectory Typologies" that differentiate counties by cost-growth velocity? Did the 2008 recession fundamentally disrupt these paths, or are they governed by persistent structural factors?

#### 4. Contextual Anomaly Detection
* **Focus:** Can we isolate "Stable Anomalies"—counties that defy all economic logic—using **Bootstrap Robustness Testing** to filter out statistical noise and identify true policy outliers?

---

###  Planned Analysis & Refinements 
* **Probabilistic Clustering:** Replacing baseline K-Means with **GMM** ($k=8$) to move beyond binary "High/Low" labels and account for structurally ambiguous counties.
* **Validation Rigor:** Utilizing the **Adjusted Rand Index (ARI)** to prove cluster stability and **Bootstrap Resampling** (100 iterations) to ensure anomalous signals are stable across data subsets.
* **Temporal Tracking:** Constructing **Transition Matrices** to visualize the profile deterioration of counties from 2008 to 2018.



---

###  Repository Structure
* `data/`: Raw and processed versions of the NDCP dataset.
* `notebooks/`: 
    * `Integrated_Analysis_M5.ipynb`: Master dashboard and final synthesis of all four pillars.
    * `Individual_Refinements/`: Refined M4 notebooks covering GMM, Bootstrap, and Trajectory validation.
* `reports/`: Documentation for project milestones M1 through M5.

---

