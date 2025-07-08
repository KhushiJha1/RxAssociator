#  RxAssociator

**RxAssociator** is a data-driven analysis tool designed to uncover hidden relationships between prescription drug side effects using the **Apriori algorithm**. The project applies **association rule mining** on real-world medical data to identify frequent symptom combinations and generate human-readable, interpretable rules.


##  Problem Statement

Side effects from prescription drugs can vary from minor discomforts to severe health risks. Identifying which symptoms frequently co-occur can help:

- Healthcare professionals detect risky combinations early
- Patients make informed decisions
- Pharma companies improve drug labeling and testing

This project explores those patterns by mining association rules from side effect data and visualizing meaningful trends.


##  Objectives

- Clean and preprocess medical side effect data
- Convert text-based symptom reports into structured format
- Use Apriori algorithm to discover frequently co-occurring side effects
- Generate readable association rules using metrics like **support**, **confidence**, and **lift**
- Visualize and interpret top rules to inform real-world use


##  Dataset Summary

The dataset includes:

- `drug_name`: Name of the prescribed medication  
- `condition`: The condition being treated  
- `side_effects`: Comma-separated list of reported side effects  
- `no_of_reviews`: Number of user-submitted reviews  
- `rating`: Average rating for the drug's effectiveness  


##  Tech Stack

| Tool/Library              | Purpose                                  |
|--------------------------|------------------------------------------|
| `pandas`, `numpy`        | Data manipulation and analysis           |
| `matplotlib`, `seaborn`  | Data visualization                       |
| `mlxtend`                | Apriori algorithm & association rules    |
| `sklearn.preprocessing`  | Label encoding, standard scaling         |


##  Key Steps

1. **Data Cleaning**  
   Removed invalid/missing side effects and filtered out long descriptive entries.

2. **Preprocessing**  
   Converted side effects into list format, applied one-hot encoding using `TransactionEncoder`.

3. **Apriori Mining**  
   Extracted frequent itemsets with `min_support=0.01` and max pair length of 2.

4. **Rule Generation**  
   Applied `association_rules()` with `min_confidence=0.5` to detect high-confidence symptom combinations.

5. **Visualization**  
   Plotted correlation heatmap and sorted top 10 rules by confidence and lift.
   
##  Future Work

- Add more features (age group, drug class, gender) for deeper insights  
- Use network graphs to visualize rules as symptom maps  
- Build an interactive dashboard with Streamlit or Plotly  

##  Use Cases

- Pharmacovigilance & clinical research  
- Patient safety monitoring tools  
- Drug recommendation engines  


---

## ⭐ If you found this helpful...

Give it a ⭐ on GitHub to support this research-oriented effort in healthcare and AI!
