# CE462A – Project 1: IDF Analysis & Urban Drainage Design  
### IDF Analysis | Hyetograph | Rational Method | Manning’s Pipe Sizing  

This repository contains the complete implementation of an **urban stormwater drainage design** project completed for **CE462A – Project-02 (Villupuram site)**.

---

## 📁 Repository Contents

| File / Folder | Description |
|---------------|-------------|
| **CE462.ipynb** | Full Colab notebook with code, plots, and outputs. |
| **CE462.py** | Python script version of the workflow. |
| **Dataset2.xlsx** | Input rainfall dataset for IDF analysis. |
| **IDF_Results.xlsx** | Computed rainfall intensities for all return periods. |
| **Drainage_Design_Results.xlsx** | Basin discharge & pipe adequacy outputs. |
| **/figures** | Folder containing all generated plots. |

Figures include:  
- `IDF_Curves.png`  
- `Hyetograph.png`  
- `Manning_Capacity_vs_Diameter.png`

---

## 📘 Project Overview  

This project performs a **complete hydrologic + hydraulic simulation** for a residential catchment drainage system.

---

## 1️⃣ IDF Curve Generation
- Extract rainfall values from `Dataset2.xlsx`
- Fit **Lognormal** and **Gumbel** distributions  
- Perform **KS test**
- Choose best-fit distribution  
- Generate IDF curves for **2, 5, 10, 15, 30, 50 years**

📈 Output: `figures/IDF_Curves.png`

---

## 2️⃣ Development of a Design Hyetograph

- Duration: **1.5 hours**  
- Return period: **T = 25 years**  
- Intensity from IDF interpolation  
- Apply **6-interval symmetric pattern**

📊 Output: `figures/Hyetograph.png`

---

## 3️⃣ Basin-wise Peak Discharge (Rational Method)

\[
Q = 0.00278\, C \, I \, A
\]

Stored in:  
`Drainage_Design_Results.xlsx`

---

## 4️⃣ Pipe Sizing using Manning’s Formula

\[
Q = \frac{1}{n} A R^{2/3} S^{1/2}
\]

📈 Output: `figures/Manning_Capacity_vs_Diameter.png`

---

## 🛠 Software Requirements
- Python 3.8+
- NumPy  
- Pandas  
- SciPy  
- Matplotlib  
- OpenPyXL  

---

## ▶️ How to Run

### Option 1 — Google Colab  
Upload all files and run:


---

### Option 2 — Run Locally

Install packages:

```bash
pip install numpy pandas scipy matplotlib openpyxl


python CE462.py


📄 Summary of Results

IDF curves generated using best-fit probability distribution

Hyetograph developed for a T = 25-year storm

Basin-wise runoff calculated using Rational Method

Pipes sized to safely convey peak flows

All outputs exported to Excel


---

# 🔥 IMPORTANT  
The key fix is this:

After the line:


You MUST close the code block:





