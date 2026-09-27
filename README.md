# 🎮 Video Game Score Prediction: Console Analysis

## 📌 Project Overview
This analysis explores the relationship between the console a video game is released on and its final review score. By understanding this dynamic, developers and marketers can gain valuable insights into platform-specific performance and reception in the competitive gaming industry.

## 🗄️ Dataset
* **Source:** "Video Games" dataset collected from GameSpot by mohamedhanyyy via Kaggle.
* **Size:** 14,802 video game records.
* **Key Attributes:**
  * `Console`: The platform the game runs on (e.g., PC, XONE, PS4).
  * `GameName`: The title of the game.
  * `Review`: Textual review summary ("Early Access", "Good", "Great", "Superb", "Fair").
  * `Score`: Review rating scaled from 1 to 10.

## 🛠️ Data Preprocessing & Tools
* **Environment:** PyCharm IDE, Python (Pandas, Matplotlib, Seaborn, Scikit-Learn).
* **Encoding:** Applied Label Encoding to categorical variables like `Console` to translate them into numerical representations for machine learning algorithms.
* **Scaling:** Normalized features using `StandardScaler` to ensure all inputs contribute equally, preventing distortion from varying feature ranges and improving convergence speed.

## 🤖 Classification Techniques Evaluated
1. **Logistic Regression:** Models the probability of scores based on console type, offering straightforward interpretability.
2. **Decision Tree:** Provides a visual representation of the decision-making process behind score predictions.
3. **Random Forest:** An ensemble method aggregating multiple decision trees to reduce the risk of overfitting and provide robust estimates.
4. **Support Vector Machine (SVM):** Identifies the optimal hyperplane separating rating classes, maximizing the margin for robust classification.
5. **K-Nearest Neighbors (KNN):** Classifies games based on the similarity of their closest data points/neighbors.

## 📊 Key Findings & Model Performance
Models were evaluated using multi-class confusion matrices to track exact score predictions (1-10):

* **Top Performers (SVM & KNN):** Both the Support Vector Machine and K-Nearest Neighbors models achieved exceptional accuracy with perfect classifications across all tested score categories (accurately predicting 326 instances of score 9 and 22 instances of score 6 with zero misclassifications).
* **Decision Tree:** Exhibited strong performance with perfect classifications for scores 8 and 9, demonstrating a solid grasp of diverse score ranges.
* **Random Forest:** Demonstrated highly reliable classification with only minor discrepancies (e.g., predicting one score 7 as a 6, and two score 8s as 2s).
* **Logistic Regression:** Accurately classified the vast majority of extreme scores (e.g., 868 instances of score 5) but misclassified 6 instances of score 6 as score 7, indicating reliable overall performance with room for refinement in lower score categories.

## 💡 Conclusion
The console a game is released on holds predictive power over its final score. Advanced models like SVM and KNN are highly capable of capturing these complex data patterns without error in the test subsets, providing a robust toolset for analyzing video game success metrics.

## 📁 Repository Structure
* `video-game-score-prediction-console-analysis.ipynb`: The complete Python codebase containing data preprocessing, feature scaling, model training, evaluation metrics, and confusion matrix visualizations.
* `Games.csv`: The dataset used for model training and testing.
