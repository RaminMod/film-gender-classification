# Film Gender Classification

In this project, we worked with a real-world dataset of Hollywood movies to build a model that predicts whether the lead actor in a film is male or female — based on things like word counts, cast composition, and the year of release.

The task is framed as a binary classification problem, and it's related to broader discussions around gender balance in film dialogue. Instead of focusing on the social aspect, we approached it from a machine learning perspective — looking at patterns in the data and seeing how well different models can perform.


We explored a few different classification methods to see which one works best for this problem. Each model was tuned and evaluated using cross-validation.

Here’s what we tested:

- **Logistic Regression** – a simple baseline that gives us a good starting point.
- **Linear & Quadratic Discriminant Analysis (LDA & QDA)** – to model decision boundaries using assumptions on the data distribution.
- **k-Nearest Neighbors (k-NN)** – to classify based on similarity to nearby films in the feature space.
- **Random Forest** – to capture more complex patterns using an ensemble of decision trees.
- **Naive baseline** – a simple rule-based classifier that always predicts “male” as the lead. Useful for comparison.

Each method was tested using k-fold cross-validation to get a more reliable estimate of performance.


The dataset includes information from over 1,000 Hollywood movies. For each film, we have metadata like:

- Number of male and female actors with major speaking roles
- Word counts by gender
- Age of the lead and co-lead
- Gross earnings of the film
- Year of release

The goal was to predict the **gender of the lead actor**, which is defined as the person who speaks the most in the film. So, even though each film has one male and one female lead, the task is to figure out which one talks more — based on these features.

Here’s how the repo is organized to keep things clean and easy to follow:

- `notebooks/` – Main analysis notebook with code, models, and results
- `data/` – Contains the training and test datasets (`train.csv`, `test.csv`)
- `scripts/` – Extra Python scripts, like one for checking prediction format
- `results/` – Placeholder for final predictions or any plots/output files
