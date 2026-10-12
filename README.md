# Linear Regression

A hands-on introduction to linear regression. You will fit simple and multiple regression models with scikit-learn, measure how well they fit, add categorical features with dummy variables, and use statsmodels when you need the statistics behind a model. The notebooks alternate between worked lessons and short exercises so you can practise each idea as you go. Two optional notebooks go further: checking the assumptions of linear regression, and writing gradient descent, the algorithm that fits a line, from scratch.

## Learning Objectives

By the end of this repository, you should be able to:

- Train a simple linear regression model with scikit-learn and calculate its slope, intercept and $R^2$.
- Train a multiple linear regression model and compare models with $R^2$ and adjusted $R^2$.
- Encode categorical variables as dummy variables, dropping one column to avoid the dummy variable trap, and calculate each category's difference from the reference category.
- Fit an OLS model with statsmodels and extract the coefficients, $R^2$ and p-values from its summary.

With the optional notebooks, you can also:

- Plot the residuals of a model and run a Breusch-Pagan test to check the assumptions of linear regression.
- Implement gradient descent from scratch to recover a known slope and intercept, and compare how different learning rates decide whether it converges or diverges.

## Learning Path

Work through the notebooks in this order:

| File / Folder                                                                                      | Description                                                                                                                 |
| -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [**01 - Simple Linear Regression**](01_simple_linear_regression.ipynb)                        | Fit your first linear regression model with scikit-learn and measure its fit with $R^2$.                                   |
| [**02 - Exercise: Simple Linear Regression**](02_exercise_simple_linear_regression.ipynb)     | Practise simple linear regression on your own.                                                                              |
| [**03 - Multiple Linear Regression**](03_multiple_linear_regression.ipynb)                    | Model a target from several features at once, and see the fitted plane in 3D.                                               |
| [**04 - Exercise: Multiple Linear Regression**](04_exercise_multiple_linear_regression.ipynb) | Practise multiple linear regression on your own.                                                                            |
| [**05 - Categorical Variables**](05_categorical_variables.ipynb)                              | Encode categorical features as dummy variables and read their coefficients. W3D3 builds on it with scikit-learn's encoders. |
| [**06 - Linear Regression with statsmodels**](06_linear_regression_statsmodels.ipynb)         | Fit an OLS model, read its statistical summary, and learn when to use statsmodels instead of scikit-learn.                  |
| [**07 - Checking the Assumptions**](07_checking_assumptions.ipynb)                            | Optional: check each assumption with residual plots and tests, and fix a failing model.                                     |
| [**08 - Exercise: Gradient Descent**](08_exercise_gradient_descent.ipynb)                     | Optional: write the algorithm that finds the line. Bonus: solve the same problem in one step with the normal equation.      |

Notebooks 07 and 08 are optional: work through them if you have time left.

### Additional Folders and Files

| File / Folder                             | Description                                                                                         |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------- |
| [**Data**](data/)                    | Datasets used across the notebooks (cars, car seats and utility bills).                             |
| [**Assets**](assets/)                | Figures displayed in the notebooks. The Mermaid sources of the diagrams are in `assets/diagrams/`. |
| [**Solutions**](solutions/)          | Worked solutions, added later in the course.                                                        |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies.                                                             |
| [**uv.lock**](uv.lock)               | Dependency lock file.                                                                               |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it, including the `< >` brackets, with your own value. For example, `cd <repo-name>` becomes `cd amle-linear-regression`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in `.venv/`.

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by uv sync.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**Scikit-Learn linear models guide**](https://scikit-learn.org/stable/modules/linear_model.html): The official user guide for linear regression and related models.
- [**Statsmodels regression docs**](https://www.statsmodels.org/stable/regression.html): OLS and other linear models, with full statistical summaries.
- [**Seaborn regression plots**](https://seaborn.pydata.org/tutorial/regression.html): Visualising linear relationships between variables.
- [**An Introduction to Statistical Learning**](https://www.statlearning.com/): A free textbook whose chapter on linear regression covers the theory in depth (R and Python editions).
- [**Ordinary Least Squares example (scikit-learn)**](https://scikit-learn.org/stable/auto_examples/linear_model/plot_ols_ridge.html): A worked example fitting LinearRegression on a real dataset.
