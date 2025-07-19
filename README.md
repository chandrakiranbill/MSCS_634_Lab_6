# MSCS_634 
  

## Lab 6: Association Rule Mining Using Apriori and FP-Growth  

### Student Name:   **Chandra Kiran Billingi**  

---

## 📝 Purpose of the Lab  

The purpose of this lab was to apply **Association Rule Mining (ARM)** techniques to a **grocery shopping dataset** to uncover purchasing patterns between products. Specifically, this lab focused on the **Apriori** and **FP-Growth** algorithms to identify **frequent itemsets** and generate **association rules** based on metrics like **support**, **confidence**, and **lift**.  
Visualization through **Heatmaps** and **Scatter Plots** was used to help interpret the strength and nature of relationships between items.

---

## 🔧 Steps Performed  

###  Data Preparation  
- Loaded the **Groceries dataset** containing shopping basket transactions.  
- Converted transactional data into a **one-hot encoded dataframe** suitable for association rule mining.

### Frequent Itemsets Generation  
- **Apriori Algorithm**: Applied with `min_support=0.01`.  
- **FP-Growth Algorithm**: Applied with `min_support=0.01`.  
- Frequent itemsets were identified using both methods and compared.

### Association Rule Generation  
- Extracted association rules from both algorithms 
- Evaluated key metrics: **support**, **confidence**, **lift**.

###  Visualization  
- Created ** Heatmaps** for both Apriori and FP-Growth top 20 rules using `seaborn`.  
- Compared similarities and differences between the two algorithms visually.

---

## 📊 Key Insights & Results  

### 🔍 Frequent Itemsets  
- **Organic Raspberries**, **Organic Strawberries**, and **Organic Hass Avocado** consistently appeared as frequent itemsets.  
- These items often co-occurred in customer baskets.

### 🔗 Association Rules  
- High **lift** was consistently observed between combinations of organic fruit products.  
- Strongest associations found:  
  - **Organic Raspberries** ↔ **Organic Strawberries**  
  - **Organic Hass Avocado** ↔ **Organic Raspberries**  
  - **Bananas** ↔ **Organic Fuji Apple**  

### 📈 Lift Heatmap Observations  
- **FP-Growth** produced slightly higher **lift** values compared to **Apriori**.
- Both algorithms showed clear clusters of strong associations among similar product categories (organic fruits).
- **Organic Strawberries** & **Organic Raspberries** stood out as having the strongest mutual influence.

---

## 📉 Challenges & Decisions  

- **Threshold Selection**: Balancing between too few or too many rules required tuning `min_support` and `confidence`.
- **Interpretation of Metrics**: Carefully interpreting **lift** to avoid misleading conclusions from frequent but trivial associations.
- **Efficiency**: Noted Apriori as more computationally efficient than Fp-grwoth for this dataset size.
- **Visualization Limitations**: Focused only on **top 20 rules** to keep heatmaps interpretable and actionable.

---

## 🔑 Conclusions  

- **Association Rule Mining** is a powerful tool for uncovering hidden relationships in shopping behavior.
- **FP-Growth** is preferable for larger datasets due to efficiency.
- Visualization through **Lift Heatmaps** enhances the interpretability of rule strength and supports practical decision-making.
- Strong associations among organic fruits suggest bundling or marketing strategies could leverage these insights.

---
