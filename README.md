# Bioequivalence---Module-2---Project-
Bioequivalence study and pharmacokinetic analysis using Python
# Pharmacokinetic Bioequivalence Analysis using Python

## 📌 Project Overview
This project performs a complete statistical evaluation of bioequivalence between a generic drug formulation and a reference innovator product, strictly following regulatory guidelines (EMA/FDA). 

The analysis evaluates whether the 90% Confidence Interval for the Geometric Mean Ratio (GMR) of the Area Under the Curve (\(\text{AUC}_{0-t}\)) falls within the standard acceptance range of **80.00% to 125.00%**.
🛠️ Technologies & Libraries UsedPython 3.xNumPy – Efficient array manipulation and arithmetic operationsSciPy (scipy.stats) – Standard Error of the Mean (SEM) and Student's t-distribution quantiles (ppf)Jupyter Notebook / VS Code – Interactive data processing and LaTeX markdown reporting

🔬 Mathematical & Statistical MethodologyTrapezoidal Rule ($\text{AUC}$ Calculation):$$\text{AUC}_n = \frac{C_{n-1} + C_n}{2} \times (t_n - t_{n-1})$$Log-Transformation ($\ln$):Pharmaco-kinetic data are assumed to follow a log-normal distribution. Logarithmic transformation converts multiplicative ratios into additive differences:$$\Delta \ln(\text{AUC}) = \ln(\text{AUC}_{\text{generic}}) - \ln(\text{AUC}_{\text{reference}})$$90% Confidence Interval Estimation:$$\text{Margin of Error} = t_{\text{crit}} \times \text{SEM}$$$$\text{CI}_{\text{log}} = \text{Mean Difference} \pm (t_{\text{crit}} \times \text{SEM})$$where $t_{\text{crit}}$ is obtained using scipy.stats.t.ppf(0.95, df=n-1).Regulatory Decision Criteria:The log confidence limits are exponentiated ($\exp$) to back-transform to the percentage ratio scale:$$\text{Decision:} \quad 80.00\% \le \text{Lower CI} \quad \text{and} \quad \text{Upper CI} \le 125.00\%$$

🚀 How to Run the ProjectClone this repository:Bashgit clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)

Open VS Code or JupyterLab.Ensure required libraries are installed:Bashpip install numpy scipy
Run all cells in Bioequivalence.ipynb.

📊 Summary of ResultsSample Size ($n$): 12 crossover subjectsPoint Estimate (GMR): 98.30%90% Confidence Interval: [98.10%, 98.51%]Conclusion: The generic product is BIOEQUIVALENT to the reference drug as the 90% CI lies entirely within the regulatory window $[80.00\%, 125.00\%]$.
