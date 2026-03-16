📌 Project Overview
This project is a comparative study of consumer preferences and sustainability awareness in the skincare markets of Hong Kong and the Mainland Greater Bay Area (GBA), conducted as a Final Year Project. Addressing the counter-intuitive phenomenon of "low skincare spending in a high-income region (Hong Kong)" observed in preliminary data, this project utilizes deep data mining to isolate structural sample biases (e.g., a high proportion of students). By introducing a gender dimension and employing Exploratory Data Analysis (EDA) alongside Machine Learning algorithms, it reconstructs the consumption decision-making logic of the skincare market, providing precise segmentation strategies for beauty brands.

🔬 Datasets
hk_skincare_data.csv: Hong Kong market sample (n=98), characterized by a younger demographic and a high proportion of students
mainland_skincare_data.csv: Mainland GBA market sample (n=132), featuring a broader professional distribution.

🔬 Core Methodologies & Findings
The data mining workflow is divided into three progressive phases:
Phase 1: Exploratory Data Analysis (Basic Behavioral Funnel)
Quantified retention rates across the "Cleanser -> Toner -> Moisturizer -> Serum/Eye Cream" funnel to compare the complexity of skincare routines between the two regions and across genders.
Key Insights:Regional Differences: The Mainland market leans towards a "full-suite routine (cleanse + tone + moisturize + eye care)," whereas the Hong Kong market favors "minimalist cleansing." This is the direct cause of the difference in average basket size. Gender Funnel: Females demonstrate a deep "full-suite funnel," while males experience a drastic drop-off after basic cleansing (cleanser retention >80%, but drops to 19% for toner and 7% for serum). The root cause of low total spending among males is the premature end of their skincare routine, not a lack of absolute purchasing power.
Phase 2: Pseudo-Conjoint Analysis via Random Forest
Traditional 1-5 ratings struggle to measure the "trade-off utility" in real-world purchases. This project trained a Random Forest Classifier, using gender as the Target and the 7 attribute ratings as Features, to quantify the decision-making gap through "Feature Importance."
Key Insights:The most critical watersheds distinguishing male and female skincare decisions are not "Price" or "Brand Reputation," but "Product Reviews & Recommendations" (17.9%) and "Eco-friendly Packaging" (17.2%). Females rely heavily on social proof/word-of-mouth and have some awareness of green/sustainable beauty. Males, conversely, exhibit linear, "blind-buy" decision-making and are highly desensitized to eco-friendly concepts.
Phase 3: Unsupervised Learning (K-means Deep Clustering of the Male Market)To break the stereotype that "men don't do skincare," all male samples were extracted. Dimensions such as the number of skincare steps, spending tiers, and efficacy preferences were fed into a K-means clustering algorithm ($K=2$).Key Insights (Consumer Personas):Cluster 0 - Minimalist Men: The absolute majority of the male market. Characterized by few steps and low spending; indifferent to ingredients and eco-friendliness; highly prone to falling into the low-price cleanser price war.Cluster 1 - Refined Men: A high-net-worth potential segment. Skincare steps extend to sunscreen and moisturizer; emphasis on specific ingredients and efficacy spikes significantly; their willingness to pay rivals that of female consumers.

🛠️ Tech Stack
Python 3.x
Data Processing: pandas, numpy
Machine Learning: scikit-learn (RandomForestClassifier, KMeans, StandardScaler)
Data Visualization: matplotlib, seaborn
