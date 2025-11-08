# Research and Development Assignment — AI Curve Fitting

### 🎯 Objective
To estimate the unknown parameters **θ**, **M**, and **X** in the given parametric curve:

\[
x = \left(t*\cos(\theta) - e^{M|t|}\sin(0.3t)\sin(\theta) + X\right)
\]
\[
y = \left(42 + t*\sin(\theta) + e^{M|t|}\sin(0.3t)\cos(\theta)\right)
\]

using the provided dataset of points `(x, y)` for \( 6 < t < 60 \).

---

### 🧩 Data
Dataset provided as: **xy_data.csv**

| Variable | Range |
|-----------|--------|
| \( 0° < \theta < 50° \) | \( -0.05 < M < 0.05 \) | \( 0 < X < 100 \) |
| \( 6 < t < 60 \) |

---

### 🧠 Approach

1. **Model Definition**  
   Defined a Python function for \(x(t)\) and \(y(t)\) based on given parametric equations.

2. **Parameter Initialization**  
   Started with random guesses for θ, M, and X within the allowed ranges.

3. **Optimization**  
   Used **SciPy’s `minimize` (L-BFGS-B)** algorithm to minimize the **L1 distance** between the predicted and observed points.

4. **Evaluation**  
   Compared the fitted curve against actual data points using Matplotlib visualization.

---

### 🧮 Final Results

| Parameter | Symbol | Optimal Value |
|------------|---------|---------------|
| Angle | \( \theta \) | 28.1275° |
| Exponential Coeff | \( M \) | 0.02133 |
| Offset | \( X \) | 54.901 |

---

### ✅ Final Parametric Equation (LaTeX Form)

\[
\left(t*\cos(0.491) - e^{0.02133|t|}\sin(0.3t)\sin(0.491) + 54.901,\ 42 + t*\sin(0.491) + e^{0.02133|t|}\sin(0.3t)\cos(0.491)\right)
\]

---

### 🔗 Desmos Visualization
You can view the curve directly here:  
[Desmos Link](https://www.desmos.com/calculator/rfj91yrxob)

Paste the equation and set value of t
   (6<t<60)


---

### 💻 Code

The full implementation (data loading, visualization, optimization, and plotting) is available in  
`curve_fitting.ipynb`.

---

### 📈 Libraries Used
- Python 3.x  
- NumPy  
- Pandas  
- Matplotlib  
- SciPy

---

### ✍️ Author
Siddharth B — Research and Development / AI Assignment (Curve Parameter Estimation)




