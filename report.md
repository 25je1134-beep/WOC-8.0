**WOC 8.0 FINAL REPORT**



**Candidate Details:**

\- **Name:** Cheshant Kumar Patel

\- **Admission Number:** 25JE1134

\- **Project Title: Binary Buzz - Machine Learning Classification**



**1. Implementation Tasks:**

During the Winter of Code, I developed a custom utility library to handle core machine learning tasks.

**- Balanced Accuracy Function:** I implemented a manual function to calculate accuracy by averaging the True Positive Rate (TPR) and True Negative Rate (TNR), which is more reliable for imbalanced datasets.

**- Threshold Optimizer**: I created a tool that uses np.logspace to test 25 different threshold values (epsilon) to find the exact point where the **model's balanced accuracy is maximized.**



**2. Kaggle Competition: Binary Buz**z

I submitted two distinct approaches for the competition:



**Approach 1: Logistic Regression**

\- Method: Used *L2 regularization* with a liblinear solver.

\- **Hyperparameters:** I tested a range of C values from 0.001 to 100.

\- Result: The best performance was achieved with C=100, yielding a validation accuracy of 0.7976 and a test accuracy of 0.7028.



**Approach 2: Neural Network (Final Approach)**

**- Architecture:** A 3-layer Sequential model with 25 neurons (ReLU), 10 neurons (ReLU), and 1 output neuron (Linear).

**- Optimization:** The model was trained for 50 epochs using Binary Cross-Entropy loss.

\- Result: This model achieved a high training balanced accuracy of 0.9599 and a test balanced accuracy of 0.7132.



**3. Observations \& Key Findings:**

**- The Power of Thresholding:** In the Neural Network model, the default 0.5 threshold was not optimal. By using my custom compute\_epsilon function, I found that a threshold of 1e-08 provided the best results.

**- Convergence:** The Neural Network converged efficiently, with the loss decreasing from 45.32 to 0.11 by the end of training.

**- Complexity:** With 3072 features, the Neural Network's ability to capture non-linear relationships allowed it to slightly outperform the Logistic Regression baseline on the test set.



**Technical Model Improvements**

**Data Scaling**: Ensure you are using StandardScaler consistently. Normalizing high-dimensional data often leads to faster convergence and better performance for both Logistic Regression and Neural Networks.



**Enhanced Documentation \& Visualization**

**Advanced Plotting:** Add a **Learning Curve** plot to your report. This graph shows training vs. validation error over time and is the best way to prove to mentors that you understand how to diagnose overfitting and underfitting.



**4. Conclusion:**

**The Winter of Code was a valuable experience in building ML models from the ground up. The combination of deep learning and custom metric optimization proved to be the most effective strategy for the Binary Buzz competition.**


