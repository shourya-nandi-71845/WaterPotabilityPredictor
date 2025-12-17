# WaterPotabilityPredictor
A basic ML model for predicting water potability using physiochemical parameters


INTRODUCTION :- 
This is my first project as an AIML and technology enthusiast and was developed as part of my FSP coursework at Techno Main Salt Lake (TMSL). Water potability assessment is a complex task due to the wide variation in physicochemical properties and the presence of diverse pollutants that alter water quality. This project aims to classify water samples as potable or non-potable using supervised machine learning techniques trained on chemical and physical water quality parameters.


ABSTRACT :- 
This project applies supervised machine learning techniques to classify water samples as potable or non-potable using water quality attributes such as pH, hardness, solids, chloramines, sulfate, conductivity, organic carbon, trihalomethanes, and turbidity. The dataset was preprocessed to handle missing values, scale features, and address class imbalance using stratified splitting and class weighting. A Random Forest classifier was trained and evaluated using accuracy, confusion matrix, precision, recall, and F1-score. The optimized model achieved an accuracy of approximately 71%, demonstrating strong detection of non-potable water while highlighting areas for improvement in potable water identification.


DATA ORGANISATION & COLLECTION :- 
Dataset: water_potability.csv
Samples: 3,276
Features: pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, Turbidity
Target: Potability (0 = Not Potable, 1 = Potable)


EXPLORATORY DATA ANALYSIS (EDA) :- 
Exploratory Data Analysis was done to understand the feature distributions, detect the missing values, and study correlations using statistical summaries and visualizations.
It was found that the dataset is imbalanced as it had 1998 samples for "non potable" and 1278 samples for "potable."


DATA PREPROCESSING :- 
Missing values were handled using statistical imputation. Median imputation was applied to the pH and Trihalomethanes features due to skewness and extreme values, while mean imputation was used for the Sulfate feature as it showed a relatively balanced distribution.

Standard Scaler was used to fit the data values for a better computational accuracy.


MACHINE LEARNING MODEL :- 
Train-test split was used to preserve class distribution. It was done for a 20% test sample.
Stratified splitting was used to maintain the original class distribution in both training and testing sets.
Now, different ML algorithms were compared and checked for the highest accuracy of the ML model.

"Random Forest" performed best due to its ability to capture non-linear relationships and robustness to outliers.


EVALUATION :- 
Model performance was evaluated using accuracy, confusion matrix, precision, recall, and F1-score, with particular focus on recall for potable water to minimize unsafe predictions.
The optimized Random Forest model achieved an accuracy of 71%, showing strong performance in identifying non-potable water with a recall of 95%. While precision for potable water is high (81%), the recall remains moderate (33%), indicating that some safe water samples are still misclassified. Overall, the model prioritizes safety by minimizing false positives, with scope for further improvement in potable water detection. This trade-off reflects a safety-oriented model design, where minimizing unsafe predictions is prioritized over maximizing potable water detection.


LIMITATIONS :- 
-Class imbalance impacts the recall of potable water samples.
-Absence of real-time and location-specific data limits generalization.
-The dataset does not include temporal variations, which may affect seasonal water quality changes.


CONCLUSION :- 
The study successfully applied a Random Forest model to predict water potability with reasonable 71% accuracy predictions. While the model performs well in identifying non-potable water, further optimization is required to enhance the detection of potable samples. The results validate the potential of machine learning in water quality analysis.
