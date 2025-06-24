# 🎬 Film Gender Classification

In this project, we worked with a real-world dataset of Hollywood movies to build a model that predicts whether the lead actor in a film is male or female — based on things like word counts, cast composition, and the year of release.

The task is framed as a binary classification problem, and it's related to broader discussions around gender balance in film dialogue. Instead of focusing on the social aspect, we approached it from a machine learning perspective — looking at patterns in the data and seeing how well different models can perform.

---

### 🧠 What We Tried

We explored a few different classification methods to see which one works best for this problem. Each model was tuned and evaluated using cross-validation.

Here’s what we tested:

- **Logistic Regression** – a simple baseline that gives us a good starting point.
- **Linear & Quadratic Discriminant Analysis (LDA & QDA)** – to model decision boundaries using assumptions on the data distribution.
- **k-Nearest Neighbors (k-NN)** – to classify based on similarity to nearby films in the feature space.
- **Random Forest** – to capture more complex patterns using an ensemble of decision trees.
- **Naive baseline** – a simple rule-based classifier that always predicts “male” as the lead. Useful for comparison.

Each method was tested using k-fold cross-validation to get a more reliable estimate of performance.

---

### 📁 The Dataset

The dataset includes information from over 1,000 Hollywood movies. For each film, we have metadata like:

- Number of male and female actors with major speaking roles  
- Word counts by gender  
- Age of the lead and co-lead  
- Gross earnings of the film  
- Year of release  

The goal was to predict the **gender of the lead actor**, which is defined as the person who speaks the most in the film. So, even though each film has one male and one female lead, the task is to figure out which one talks more — based on these features.

---

### 📂 Repository Structure

Here’s how the repo is organized to keep things clean and easy to follow:

- `notebooks/` – Main analysis notebook with code, models, and results  
- `data/` – Contains the training and test datasets (`train.csv`, `test.csv`)  
- `scripts/` – Extra Python scripts, like one for checking prediction format  
- `results/` – Placeholder for final predictions or any plots/output files  

---

### ▶️ How to Run It

To try out the models or reproduce the results, you can follow the steps in the main notebook inside `notebooks/`.

Once it’s available, it’ll walk through:

1. Loading and transforming the data  
2. Running different classification models  
3. Comparing their performance  
4. Making predictions on the test set  

If you're running this in your own environment, make sure you have Python 3 installed, along with the usual machine learning libraries:

```bash
pip install pandas scikit-learn matplotlib seaborn

You can also run everything in a Jupyter environment like VS Code, JupyterLab, or Google Colab.

---

### ✅ What We Found

After testing different models, we found that **Quadratic Discriminant Analysis (QDA)** gave the best results, with the lowest misclassification rate on the validation data.

The feature engineering step — where we transformed raw word counts into percentages and created a co-lead word feature — helped improve accuracy across all models.

Interestingly, even a simple rule that always predicted "male" as the lead performed surprisingly well, showing some clear imbalance in the data.

---

### 💡 Ideas for Improvement

A few things that could be interesting to try in the future:

- Use more recent data or extend the dataset with additional features like genre or budget  
- Try more advanced models like gradient boosting or neural networks  
- Dive deeper into explainability: which features matter most, and how do they influence predictions?  
- Investigate fairness metrics, since the task touches on gender-related patterns  

---
