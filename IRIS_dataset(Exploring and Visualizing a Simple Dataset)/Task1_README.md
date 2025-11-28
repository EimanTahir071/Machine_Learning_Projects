```markdown
# Task 1 — Exploring and Visualizing the Iris Dataset

## Objective
Load, inspect, and visualize the Iris dataset to understand feature relationships, distributions, and possible outliers.

## Dataset
- Iris dataset (built into seaborn / scikit-learn)
- No external download required when using seaborn.load_dataset('iris').

## Notebook
- Filename: Task1_Iris_notebook.py (Jupyter-style .py) or Task1_Iris_notebook.ipynb
- Location: / (or the folder where you put it)

## Environment / Requirements
- Python 3.8+
- Key packages:
  - pandas
  - numpy
  - seaborn
  - matplotlib

Install:
pip install pandas numpy matplotlib seaborn

## What this notebook does (step-by-step)
1. Imports libraries and sets plotting style.
2. Loads the Iris dataset using seaborn.
3. Prints dataset shape, column names, and .head().
4. Runs .info() and .describe() to summarize the data.
5. Visualizations:
   - Pairplot / scatter plots colored by species to show feature relationships.
   - Histograms for each numeric feature to view distributions.
   - Boxplots per species to identify outliers.
   - Correlation heatmap for numeric features.
6. Provides short insights and observations.

## How to run
1. Open the notebook in Jupyter:
   jupyter notebook Task1_Iris_notebook.py
2. Execute cells top-to-bottom.
3. Save outputs and screenshots of key plots if required.

## Expected outputs / Deliverables
- Pairplot showing separability of species (petal measurements usually separable).
- Histograms and boxplots for feature distributions and outliers.
- Correlation heatmap and summary statistics.
- Short written conclusions in the notebook.

## Tips & Extensions
- Try comparing seaborn.load_dataset('iris') with sklearn.datasets.load_iris() to see different representations.
- Add KDE plots or violin plots to show density differences between species.
- Use PCA to visualize the dataset in 2D.

## Submission Checklist
- Notebook with code cells and Markdown explanations.
- README file (this file).
- Push to GitHub and include a link when submitting.
```