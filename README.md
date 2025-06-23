# Apriori-Algorithm-for-Pattern-Discovery
Goal: Apply data mining techniques for association rule mining. Task: Create a custom transaction dataset of shopping items. Use the mlxtend or apyori library in Python to: Generate frequent itemsets Derive rules with support and confidence > 0.4

# 🛒 Market Basket Analysis using Apriori Algorithm

This project applies **association rule mining** using the **Apriori algorithm** on a small custom dataset of shopping transactions. It demonstrates how frequent itemsets and association rules can be derived to understand customer purchasing patterns.

---

## 📌 Objective

To discover frequent item combinations and generate strong association rules using data mining techniques, with support and confidence thresholds > 0.4.

---

## 🛠️ Tools & Libraries

- Python
- `pandas`
- `mlxtend`
- `matplotlib`
- `networkx` (for visualization)

---

## 📂 Dataset

A **custom transaction dataset** simulating customer shopping carts:

```text
[
    ['milk', 'bread', 'butter'],
    ['beer', 'bread'],
    ['milk', 'bread', 'butter'],
    ['milk', 'bread'],
    ['bread', 'butter'],
    ['milk', 'butter'],
    ['beer', 'bread'],
    ['milk', 'bread', 'butter'],
    ['milk', 'bread'],
    ['milk', 'bread', 'butter']
]
Saved as: shopping_transactions.csv

Methodology
Transaction Encoding: Convert transaction lists into one-hot encoded DataFrame using TransactionEncoder.

Frequent Itemsets: Generate frequent itemsets using the Apriori algorithm (min_support=0.4).

Association Rules: Derive rules from itemsets (min_confidence=0.4).

Filtering: Keep only rules with both support and confidence > 0.4.

Visualization: Draw item relationships using a directed graph (confidence as edge weight).

📊 Output
✅ Frequent Itemsets (Sample)
Itemset	Support
{bread}	1.0
{milk}	0.8
{bread, milk}	0.8
{bread, butter}	0.6
{milk, butter}	0.6

✅ Sample Rules
Antecedent	Consequent	Support	Confidence	Lift
{milk, bread}	{butter}	0.6	0.75	1.25
{milk}	{bread}	0.8	1.00	1.00

🕸️ Network Graph
Visualizing item-to-item rule connections

Nodes = items; Edges = rules; Edge weight = confidence

📁 Files
File	Description
shopping_transactions.csv	Raw dataset
association_rules.csv	Filtered rules with metrics
apriori_project.ipynb	Main notebook with code & plots

📚 Key Learnings
Apriori is effective in finding patterns in transaction data.

Association rules can help with recommendation engines and promotions.

Threshold tuning (support/confidence) impacts the quality of discovered rules.

💡 Future Enhancements
Use real retail datasets (e.g., Groceries, Retail Sales)

Explore FP-Growth algorithm for performance

Build a web app for interactive rule generation
