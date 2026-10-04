# Bioequivalence---Module-2---Project-
Bioequivalence study and pharmacokinetic analysis using Python
# Pharmacokinetic Bioequivalence Analysis using Python

## 📌 Project Overview
This project performs one statistical evaluation of bioequivalence between a generic drug formulation and a reference innovator product, strictly following regulatory guidelines (EMA/FDA). 

The analysis evaluates whether the 90% Confidence Interval for the Geometric Mean Ratio (GMR) of the Area Under the Curve falls within the standard acceptance range of **80.00% to 125.00%**.


🛠️ Technologies & Libraries in Python:
NumPy – Efficient array manipulation and arithmetic operations
SciPy (scipy.stats) – Standard Error of the Mean (SEM) and Student's t-distribution quantiles (ppf)
Jupyter Notebook / VS Code – Interactive data processing and LaTeX markdown reporting

🔬 Mathematical & Statistical MethodologyTrapezoidal Rule
Log-Transformation:Pharmaco-kinetic data are assumed to follow a log-normal distribution. Logarithmic transformation converts multiplicative ratios into additive differences:
Confidence Interval Estimation: is obtained using scipy.stats.t.ppf(0.95, df=n-1).
Regulatory Decision Criteria:The log confidence limits are exponentiated to back-transform to the percentage ratio scale

🚀 How to Run the ProjectClone this repository:Bashgit clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)

Open VS Code or JupyterLab.Ensure required libraries are installed:Bashpip install numpy scipy
Run all cells in Bioequivalence.ipynb.

📊 Summary of ResultsSample Size : 12 crossover subjectsPoint Estimate (GMR): 
