# 🧩 Customer Personality Analysis – Clustering

## 📌 Problem Statement
Customer Personality Analysis helps businesses better understand their **ideal customers**.  
By segmenting customers into groups based on their demographics and purchasing behavior, companies can:

- 🎯 Target the right audience with tailored marketing campaigns  
- ⚡ Optimize resource allocation  
- 🛍️ Improve product personalization and customer satisfaction  

Instead of broadcasting campaigns to everyone, clustering helps identify which customers are most likely to respond — leading to **higher ROI and lower churn**.

---

## 🛠️ Approach

### 1. Data Import & Cleaning
- Loaded the **`marketing_campaign.csv`** dataset  
- Removed missing values and duplicates  
- Converted `Dt_Customer` into `datetime`  

### 2. Feature Engineering
- Derived new features:  
  - `Age` (from `Year_Birth`)  
  - `Spent` (total amount spent across categories)  
  - `Living_With` (simplified marital status: *Alone* / *Partner*)  
  - `Children`, `Family_Size`, `Is_Parent`  
- Grouped education into **Undergraduate, Graduate, Postgraduate**  
- Dropped redundant/unnecessary columns  

### 3. Exploratory Data Analysis (EDA)
- Visualized relationships between **Income, Spending, and Age**  
- Checked distributions of numerical and categorical features  
- Verified no rare categories  

### 4. Outlier Detection & Removal
- Detected outliers via **boxplots** and **IQR rule**  
- Removed extreme values in **Age** (>100) and **Income** (>600,000)  

### 5. Encoding & Scaling
- Encoded categorical variables (`Education`, `Living_With`)  
- Scaled numerical features using **StandardScaler**  

### 6. Dimensionality Reduction (PCA)
- Applied **Principal Component Analysis (PCA)** to reduce features to 3 dimensions  
- Retained maximum variance for clustering visualization  

### 7. Clustering
- Applied **K-Means** and **Agglomerative Clustering**  
- Used **Elbow Method (KElbowVisualizer)** to determine optimal clusters  
- Final segmentation: **4 clusters**  

### 8. Cluster Profiling
- Analyzed clusters by **Income, Spending, Age, Family Size, Parenthood, Promotions, Deals Purchased**  
- Built detailed customer profiles for business insights  

---

## 📊 Outcomes & Insights

The analysis revealed **4 customer clusters**:

### **Cluster 0 – Younger Families (Low Income & Low Spending)**
- Mostly parents with family size ≈ 3  
- Younger age group  
- Limited spending power  

### **Cluster 1 – Older Families with Teens (Moderate Income, Deals Responders)**
- Parents, family size 2–4  
- Many with teenagers  
- More responsive to **deals**, less to campaigns  

### **Cluster 2 – Affluent Couples (High Income & High Spending)**
- Mostly couples, no kids, small family size (1–2)  
- Span across all ages  
- **High spenders & high income** → prime customers  
- Less responsive to deals/campaigns  

### **Cluster 3 – Older Families (Average Income, Low Spending)**
- Parents with larger families (up to 5)  
- Relatively older  
- Low-to-moderate spenders  

---

## 🚀 Key Business Takeaways
- **Cluster 2 (High-Income Couples)** → best target for **premium campaigns**  
- **Cluster 1 (Families with Teens)** → respond well to **discounts & deals**  
- **Cluster 0 & 3** → price-sensitive, require **affordable offers or tailored retention strategies**  
- Overall campaign response was **low**, highlighting need for **better personalization**  

---

## 🛠️ Tech Stack
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Seaborn, Matplotlib, Plotly, Scikit-learn, Yellowbrick  
- **Techniques:** Data Cleaning, Feature Engineering, Outlier Detection, PCA, Clustering (K-Means, Agglomerative)  

---

## ✅ Conclusion
This project shows how **unsupervised learning (clustering)** can uncover meaningful customer segments.  
By understanding these profiles, businesses can:  
✔ Increase campaign effectiveness  
✔ Reduce marketing costs  
✔ Improve personalization and customer retention  

---

## ✅ Data Source
https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis

