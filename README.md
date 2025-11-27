# CE462A – Stormwater Drainage Design Project  
### IDF Analysis | Hyetograph | Rational Method | Manning’s Formula for Pipe Sizing  

This repository contains the complete implementation of an **urban stormwater drainage design** project completed for **CE462A – Project-02 (Villupuram site)**.

The work includes:
- Rainfall statistical analysis  
- IDF curve generation  
- Design storm hyetograph development  
- Basin-wise peak discharge estimation  
- Hydraulic design of pipe network using Manning’s equation  

---

## 📁 Repository Contents  

| File / Folder | Description |
|---------------|-------------|
| **CE462.ipynb** | Complete Google Colab notebook with code, plots, analysis & outputs. |
| **CE462.py** | Python script version of the full workflow. |
| **Dataset2.xlsx** | Input rainfall dataset used for IDF analysis. |
| **IDF_Results.xlsx** | Computed rainfall intensities for all return periods. |
| **Drainage_Design_Results.xlsx** | Basin discharge + pipe adequacy results. |
| **/figures** | Folder containing all generated plots. |

**Figures included:**
- `IDF_Curves.png`  
- `Hyetograph.png`  
- `Manning_Capacity_vs_Diameter.png`

---

## 📘 Project Overview  

This project performs a **complete hydrologic + hydraulic simulation** for a drainage system in a residential catchment.

---

### **1️⃣ IDF Curve Generation**

Steps performed:
- Extract rainfall values from `Dataset2.xlsx`  
- Fit **Lognormal** and **Gumbel** distributions  
- Perform **Kolmogorov–Smirnov (KS) test**  
- Select the best-fit distribution for each duration  
- Generate IDF curves for:  
  **2, 5, 10, 15, 30, 50 years**

📈 **Output:**  
`figures/IDF_Curves.png`

---

### **2️⃣ Development of a Design Hyetograph**

- Design storm duration: **1.5 hours**  
- Selected return period: **T = 25 years**  
- Interpolated intensity from IDF results  
- Compute total design rainfall depth  
- Apply a **6-interval symmetric hyetograph pattern**

📊 **Output:**  
`figures/Hyetograph.png`

---

### **3️⃣ Basin-wise Peak Discharge (Rational Method)**  

For each basin:
- Time of concentration using **Kerby’s equation**
- Rainfall intensity from optimized IDF equation  
- Weighted runoff coefficient:  
  residential + lawn + paved  
- Peak discharge:

\[
Q = 0.00278 \, C \, I \, A
\]

All values stored in:  
`Drainage_Design_Results.xlsx`

---

### **4️⃣ Pipe Sizing using Manning’s Formula**

For each pipe section:

\[
Q = \frac{1}{n} A R^{2/3} S^{1/2}
\]

- Diameters tested: **0.30 m to 1.25 m**  
- Smallest diameter satisfying required discharge chosen  
- Capacity vs diameter plotted for all sections  

📈 **Output:**  
`figures/Manning_Capacity_vs_Diameter.png`

---

## 🛠 Software Requirements  

To run the project:

- Python 3.8+
- NumPy  
- Pandas  
- SciPy  
- Matplotlib  
- OpenPyXL  

---

## ▶️ How to Run  

### **Option 1 — Run in Google Colab**
Upload all files and run:


CE462.ipynb
---

### **Option 2 — Run Locally**

Install packages:

```bash
pip install numpy pandas scipy matplotlib openpyxl


Run the script:
python CE462.py




