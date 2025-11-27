# CE462A_Project1_IDF_Analysis
Stormwater Drainage | IDF Analysis | Hyetograph | Rational Method | Pipe Sizing using Manning’s Formula

This repository contains the full implementation of an urban stormwater drainage design project completed for CE462A – Project-02 (Villupuram site).
The work includes rainfall analysis, IDF curve generation, hyetograph development, peak runoff estimation, and hydraulic design of pipe networks.

              File                                                Description                                                                     
  --------------------------------  ------------------------------------------------------------------------------- 
    CE462.ipynb                      Google Colab notebook containing the complete code, plots, and outputs.         
    CE462.py                         Python script version of the full workflow.                                     
    Dataset2.xlsx                    Input rainfall dataset used for IDF analysis.                                   
    IDF_Results.xlsx                 Computed rainfall intensities for various return periods.                       
    Drainage_Design_Results.xlsx     Basin-wise discharge + pipe adequacy results.                                   
    figures                          Folder containing all generated plots (IDF curves, hyetograph, Manning curves). 
  -------------------------------   ---------------------------------------------------------------------------------

📘 Project Overview

This project performs a complete hydrologic + hydraulic simulation for the drainage system design of a residential catchment.

1️⃣ IDF Curve Generation

Extract rainfall values from Dataset2.xlsx

Fit Lognormal and Gumbel distributions

Perform KS test and choose best distribution

Generate IDF curves for return periods:
2, 5, 10, 15, 30, 50 years


📈 Output Plot:

figures/IDF_Curves.png


2️⃣ Development of a Design Hyetograph

Design storm duration: 1.5 hours

Selected return period: T = 25 years

Use IDF values → compute total depth

Apply a 6-interval symmetric rainfall pattern


📊 Output Plot:

figures/Hyetograph.png



3️⃣ Basin-wise Peak Discharge (Rational Method)

For every basin:

Time of concentration via Kerby’s equation

Intensity from optimized IDF equation

Weighted runoff coefficient (Residential, Lawn, Paved)

Peak discharge:

𝑄 = 0.00278 * 𝐶 * 𝐼 * 𝐴


Results stored in:

Drainage_Design_Results.xlsx



4️⃣ Pipe Sizing using Manning’s Formula

For each pipe section:
Q = 1/n * A * R^2/3 * S^1/2

Diameters tested: 0.3 m – 1.25 m

Adopt smallest diameter satisfying required Q

Plot capacity vs diameter for each section

📈 Output Plot:

figures/Manning_Capacity_vs_Diameter.png


🛠 Software Requirements

Python 3.8+
NumPy
Pandas
SciPy
Matplotlib
OpenPyXL (for Excel output) 


▶️ How to Run

Option 1 — Run in Google Colab
Just upload all files and run CE462.ipynb

Option 2 — Run Locally
pip install numpy pandas scipy matplotlib openpyxl
python ce462.py


📄 Results Summary

Complete IDF analysis and optimized IDF equation parameters
Hyetograph for design storm
Basin-wise runoff calculation
Suitable pipe diameters for all sections using Manning's formula
All results exported to Excel

