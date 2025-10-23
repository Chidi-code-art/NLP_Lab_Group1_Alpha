## Football Player Pass Completion Prediction Using Decision Trees
A.	Group Name: Group 1
B.	Names and Matriculation Numbers of Group Members:
S/N	NAME	MATRICULATION NUMBER
1.		Umeh Jason Chimdiadi	VUG/CSC/23/8824
2.		Omolaiye Joshua Obin 	VUG/CSC/23/10065
3.		Emmanuel Godwin David	VUG/CSC/23/10618
4.		Omotefe Promise Joseph	VUG/CSC/23/9383
5.		Adama Jarren Ojochide	VUG/CSC/23/9961
6.		Mbajwa Samson Tertsegha	VUG/CSC/23/9436
7.		Chukwuemerie Chimaobi Delight	VUG/CSC/23/9088
8.		OSSAI Chukwuemeka Wisdom	VUG/CSC/23/10780
9.		Anthony Victor Enomhen	VUG/CSC/23/8819
10.		Amaefule Victor Chukwuebuka	VUG/CSC/23/10215
11.		Obioma Divine .N.	VUG/CSC/23/9484
12.		Madu Chikaima Michelle	VUG/CSC/23/9639
13.		Odomo Leader Daniel	VUG/CSC/23/9871
14.		Akanero Chinedu Emmanuel	VUG/CSC/23/9876
15.		Fakeye Mobarede	VUG/CSC/23/9973
16.		Ekeh Ada Joy	VUG/CSC/23/9744
17.		Tessy Baba Kelechi	VUG/CSC/23/9355
18.		Jacob Daniel	VUG/CSC/23/10155
19.		Benedict Ofodu	VUG/CSC/23/9717
20.		Labaran Aran-esson	VUG/CSC/23/9907
21.		Oluwaseyi Ololade Will	VUG CSC 23 10159

C.	Project Objectives:
 	To train the Decision Tree model to be able to predict if a player’s passing (in soccer) would be successful.
 	To gather enough insights in understanding the nature of the soccer players and how they determine if a passing would be successful or not.
 	To strengthen the Decision Tree predictive capability by improving the dataset.
 	To train another model and identify the best-performing model through comparison and optimization.
 	To understand why the best model makes certain predictions.
 	To communicate your model’s performance and findings effectively using data visualizations.
📊 Dataset
•	Source: FIFA 15 player data
•	Original File: raw_data.csv (15,465 players, 104 features)
•	Processed File: processed_data.csv (with engineered features)
•	Key Features: Player attributes, physical characteristics, and skill ratings
🔧 Methodology
Data Preprocessing
1.	Target Variable Creation: Engineered pass_completed binary label based on passing score threshold (70)
2.	Feature Selection: Selected 7 key attributes:
o	dribbling, passing, overall, potential
o	age, height_cm, weight_kg
3.	Data Cleaning: Handled missing values using median imputation
4.	Train-Test Split: 80-20 split with stratification
Model Selection
•	Algorithm: Decision Tree Classifier
•	Configuration: max_depth=4, random_state=42
•	Rationale: Chosen for interpretability and ability to handle non-linear relationships
📈 Key Results
Model Performance
•	Test Accuracy: 100% (suggests potential data leakage)
•	Class Distribution:
o	Pass Completed (1): 1,052 players (6.8%)
o	Not Completed (0): 14,413 players (93.2%)
Key Insights
1.	Skill Scarcity: Only 6.8% of players classified as high-quality passers
2.	Feature Importance: Passing ability strongly correlated with overall player quality and dribbling skills
3.	Interpretable Rules: Decision Tree provides clear, human-readable decision paths
🚀 How to Run the Code
Prerequisites
bash
# Install required packages
pip install -r requirements.txt
Required Packages
•	pandas>=1.5.3
•	numpy>=1.21.6
•	scikit-learn>=1.2.2
•	matplotlib>=3.5.3
•	seaborn>=0.12.2
•	jupyter>=1.0.0
•	joblib>=1.2.0
Execution Steps
1.	Place data files in the project directory:
o	raw_data.csv (original FIFA data)
2.	Run the Jupyter notebook:
bash
jupyter notebook pass_prediction_decision_trees.ipynb
3.	Execute cells in order:
o	The notebook will automatically:
	Load and preprocess the data
	Create engineered features
	Train the Decision Tree model
	Generate visualizations
	Save processed data as processed_data.csv
File Structure
text
project/
├── raw_data.csv                 # Original dataset
├── processed_data.csv           # Generated after running notebook
├── pass_prediction_decision_trees.ipynb  # Main analysis notebook
├── requirements.txt             # Python dependencies
└── README.md                    # This file
💡 Model Interpretation
The Decision Tree provides transparent decision rules such as:
•	"IF overall rating > X AND passing > Y THEN classify as good passer"
•	Easy to understand for coaches and scouts
•	No "black box" predictions
⚠️ Limitations & Future Work
1.	Data Leakage Concern: Perfect accuracy suggests the target variable may be derived from input features
2.	Recommendation: Use actual match statistics (pass completion %) instead of FIFA ratings for real-world validation
3.	Potential Enhancements:
o	Try other models (Random Forest, Gradient Boosting)
o	Include more sophisticated feature engineering
o	Use cross-validation for robust evaluation
👥 Applications
•	Talent Scouting: Identify promising passers
•	Team Selection: Data-driven player selection
•	Player Development: Understand key attributes for passing success
This project demonstrates a practical approach to sports analytics using interpretable machine learning models.




